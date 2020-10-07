---
title: Verwalten verschlüsselter Daten
description: Erfahren Sie, wie Sie verschlüsselte Daten verwalten.
page-status-flag: never-activated
uuid: d909d26a-cf50-46af-ae09-f0fd7258ca27
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 75b83165-dcbd-4bb7-b703-ed769f489b16
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 100%

---


# Verwalten verschlüsselter Daten {#managing-encrypted-data}

## Informationen zu Vorab-Bearbeitungsetappen {#about-preprocessing-stages}

In manchen Fällen müssen die Daten, die Sie auf Campaign-Server importieren möchten, verschlüsselt werden, z. B. wenn sie PII-Daten enthalten.

Um ausgehende Daten verschlüsseln oder eingehende Daten entschlüsseln zu können, müssen Sie die GPG-Schlüssel über das [Control Panel](https://docs.adobe.com/content/help/de-DE/control-panel/using/instances-settings/gpg-keys-management.html) verwalten.

>[!NOTE]
>
>Das Control Panel steht allen auf AWS gehosteten Kunden zur Verfügung (mit Ausnahme von Kunden, die ihre Marketing-Instanzen auf einer lokalen Plattform hosten).

Wenn Sie nicht zur Verwendung von Control Panel berechtigt sind, wenden Sie sich an die Kundenunterstützung von Adobe, um die erforderlichen Verschlüsselungs-/Entschlüsselungsbefehle für Ihre Instanz zu erhalten. Senden Sie dazu eine Anfrage mit folgenden Angaben:

* Dem **Titel**, der in der Campaign-Benutzeroberfläche angezeigt wird, zum Verwenden des Befehls. Beispiel: &quot;Datei verschlüsseln&quot;.
* Dem **Befehl** zum Installieren in Ihrer Instanz.

Sobald die Anfrage verarbeitet wurde, stehen im Feld **[!UICONTROL Vorab-Bearbeitungsetappe]** der Aktivitäten **[!UICONTROL Datei laden]** und **[!UICONTROL Dateiextraktion]** die Verschlüsselungs-/Entschlüsselungsbefehle zur Verfügung. Diese können Sie zum Entschlüsseln oder Verschlüsseln der Dateien verwenden, die Sie importieren oder exportieren möchten.

![](assets/preprocessing-encryption.png)

**Verwandte Themen:**

* [Datei laden](../../automating/using/load-file.md)
* [Dateiextraktion](../../automating/using/extract-file.md)

## Anwendungsfall: Importieren von Daten, die mit einem vom Control Panel generierten Schlüssel verschlüsselt wurden {#use-case-gpg-decrypt}

In diesem Anwendungsfall erstellen wir einen Workflow, um Daten, die in einem externen System verschlüsselt wurden, mithilfe eines im Control Panel generierten Schlüssels zu importieren.

In [diesem Abschnitt](https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/administrating/control-panel/gpg-key-management/decrypting-data.html) finden Sie außerdem ein Video, in dem gezeigt wird, wie Daten mit einem GPG-Schlüssel entschlüsselt werden können.

Die Schritte zum Ausführen dieses Anwendungsfalls lauten wie folgt:

1. Verwenden Sie das Control Panel, um ein Schlüsselpaar (öffentlich/privat) zu generieren. Ausführliche Anweisungen finden Sie in der [Control Panel-Dokumentation](https://docs.adobe.com/content/help/de-DE/control-panel/using/instances-settings/gpg-keys-management.html#decrypting-data).

   * Der öffentliche Schlüssel wird mit dem externen System geteilt, das ihn zum Verschlüsseln der an Campaign zu sendenden Daten verwendet.
   * Der private Schlüssel wird von Campaign verwendet, um die eingehenden verschlüsselten Daten zu entschlüsseln.

   ![](assets/gpg_generate.png)

1. Verwenden Sie im externen System den vom Control Panel heruntergeladenen öffentlichen Schlüssel, um die Daten für den Import in Campaign Standard zu verschlüsseln.

   ![](assets/do-not-localize/gpg_external.png)

1. Erstellen Sie einen Workflow in Campaign Standard, um die verschlüsselten Daten zu importieren und mithilfe des über das Control Panel installierten privaten Schlüssels zu entschlüsseln. Zu diesem Zweck wird folgender Workflow erstellt:

   ![](assets/gpg_workflow.png)

   * Aktivität **[!UICONTROL Dateiübertragung]**: Überträgt die Datei von einer externen Quelle an Campaign. In diesem Beispiel soll die Datei von einem SFTP-Server übertragen werden.
   * Aktivität **[!UICONTROL Datei laden]**: Lädt die Daten aus der Datei in die Datenbank und entschlüsselt sie mithilfe des im Control Panel generierten privaten Schlüssels.

1. Öffnen Sie die Aktivität **[!UICONTROL Dateiübertragung]** und konfigurieren Sie sie entsprechend Ihren Anforderungen. Globale Konzepte zur Konfiguration der Aktivität finden Sie in [diesem Abschnitt](../../automating/using/load-file.md).

   Geben Sie im Tab **[!UICONTROL Protokoll]** Details zum SFTP-Server und der verschlüsselten .gpg-Datei an, die Sie übertragen möchten.

   ![](assets/gpg_transfer.png)

1. Öffnen Sie die Aktivität **[!UICONTROL Datei laden]** und konfigurieren Sie sie entsprechend Ihren Anforderungen. Globale Konzepte zur Konfiguration der Aktivität finden Sie in [diesem Abschnitt](../../automating/using/load-file.md).

   Fügen Sie der Aktivität eine Vorab-Bearbeitungsetappe hinzu, um die eingehenden Daten zu entschlüsseln. Wählen Sie dazu in der Liste die Option **[!UICONTROL Entschlüsselungs-GPG]** aus.

   >[!NOTE]
   >
   >Beachten Sie, dass Sie den privaten Schlüssel zum Entschlüsseln der Daten nicht angeben müssen. Der private Schlüssel wird im Control Panel gespeichert, das den zur Entschlüsselung der Datei zu verwendenden Schlüssel automatisch erkennt.

   ![](assets/gpg_load.png)

1. Wählen Sie **[!UICONTROL OK]** aus, um die Konfiguration der Aktivität zu bestätigen.

1. Sie können den Workflow jetzt ausführen.

## Anwendungsfall: Verschlüsseln und Exportieren von Daten mit einem im Control Panel installierten Schlüssel {#use-case-gpg-encrypt}

In diesem Anwendungsfall wird ein Workflow erstellt, um Daten mit einem im Control Panel installierten Schlüssel zu verschlüsseln und zu exportieren.

In [diesem Abschnitt](https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/administrating/control-panel/gpg-key-management/using-a-gpg-key-to-encrypt-data.html) finden Sie außerdem ein Video, in dem die Verwendung eines GPG-Schlüssels zum Verschlüsseln von Daten veranschaulicht wird.

Die Schritte zum Ausführen dieses Anwendungsfalls lauten wie folgt:

1. Generieren Sie ein GPG-Schlüsselpaar (öffentlich/privat) mit einem GPG-Dienstprogramm und installieren Sie dann den öffentlichen Schlüssel im Control Panel. Ausführliche Anweisungen finden Sie in der [Control Panel-Dokumentation](https://docs.adobe.com/content/help/de-DE/control-panel/using/instances-settings/gpg-keys-management.html#encrypting-data).

   ![](assets/gpg_install.png)

1. Erstellen Sie einen Workflow in Campaign Standard, um die Daten mithilfe des über das Control Panel installierten privaten Schlüssels zu verschlüsseln und zu exportieren. Zu diesem Zweck wird folgender Workflow erstellt:

   ![](assets/gpg-workflow-export.png)

   * Aktivität **[!UICONTROL Abfrage]**: In diesem Beispiel möchten wir eine Abfrage ausführen, die auf die Daten aus der Datenbank abzielt, die wir exportieren möchten.
   * Aktivität **[!UICONTROL Dateiextraktion]**: Verschlüsselt und extrahiert die Daten in eine Datei.
   * Aktivität **[!UICONTROL Dateiübertragung]**: Sendet die Datei mit den verschlüsselten Daten an einen SFTP-Server.

1. Konfigurieren Sie die Aktivität **[!UICONTROL Abfrage]** so, dass sie auf die gewünschten Daten aus der Datenbank abzielt. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../automating/using/query.md).

1. Öffnen Sie die Aktivität **[!UICONTROL Dateiextraktion]** und konfigurieren Sie sie dann entsprechend Ihren Anforderungen (Ausgabedatei, Spalten, Format usw.). Globale Konzepte zur Konfiguration der Aktivität finden Sie in [diesem Abschnitt](../../automating/using/extract-file.md).

   Fügen Sie der Aktivität eine Vorab-Bearbeitungsetappe hinzu, um die zu extrahierenden Daten zu verschlüsseln. Wählen Sie dazu den GPG-Schlüssel zur Verschlüsselung der Daten aus.

   ![](assets/gpg-extract-stage.png)

   >[!NOTE]
   >
   >Der Wert in Klammern ist der **Kommentar**, den Sie beim Generieren des Schlüsselpaars mit Ihrem GPG-Verschlüsselungs-Tool definiert haben. Stellen Sie sicher, dass Sie den richtigen passenden Schlüssel auswählen, andernfalls kann der Empfänger die Datei nicht entschlüsseln.

1. Öffnen Sie die Aktivität **[!UICONTROL Dateiübertragung]** und geben Sie dann den SFTP-Server an, an den Sie die Datei senden möchten. Globale Konzepte zur Konfiguration der Aktivität finden Sie in [diesem Abschnitt](../../automating/using/transfer-file.md).

   ![](assets/gpg-transfer-encrypt.png)

1. Sie können den Workflow jetzt ausführen. Nach der Ausführung werden die über die Abfrage abgerufenen Daten in eine verschlüsselte .gpg-Datei für den SFTP-Server exportiert.

   ![](assets/do-not-localize/gpg-sftp-encrypt.png)

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
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 26f8f7855a30fe90dbfee4bb2b5ee55c7bf4e02b
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 14%

---


# Verwalten verschlüsselter Daten {#managing-encrypted-data}

## Grundlagen zu Vorverarbeitungsstufen {#about-preprocessing-stages}

In manchen Fällen müssen die Daten, die Sie auf Campaign-Server importieren möchten, verschlüsselt werden, z. B. wenn sie PII-Daten enthalten.

Um ausgehende Daten verschlüsseln oder eingehende Daten entschlüsseln zu können, müssen Sie GPG-Schlüssel über die [Systemsteuerung](https://docs.adobe.com/content/help/en/control-panel/using/instances-settings/gpg-keys-management.html)verwalten.

>[!NOTE]
>
>Systemsteuerung steht allen auf AWS gehosteten Kunden zur Verfügung (mit Ausnahme von Kunden, die ihre Marketinginstanzen auf einer lokalen Plattform hosten).

Wenn Sie nicht berechtigt sind, die Systemsteuerung zu verwenden, müssen Sie sich an den Adobe-Kundendienst wenden, damit diese Ihrer Instanz die erforderlichen Verschlüsselungs-/Entschlüsselungsbefehle bereitstellen. Senden Sie dazu eine Anfrage mit folgenden Angaben:

* Dem **Titel**, der in der Campaign-Benutzeroberfläche angezeigt wird, zum Verwenden des Befehls. Beispiel: &quot;Datei verschlüsseln&quot;.
* Dem **Befehl** zum Installieren in Ihrer Instanz.

Once the request is processed, the encryption / decryption commands will be available in the **[!UICONTROL Pre-processing stage]** field from the **[!UICONTROL Load file]** and **[!UICONTROL Extract file]** activities. Diese können Sie zum Entschlüsseln oder Verschlüsseln der Dateien verwenden, die Sie importieren oder exportieren möchten.

![](assets/preprocessing-encryption.png)

**Verwandte Themen:**

* [Datei laden](../../automating/using/load-file.md)
* [Dateiextraktion](../../automating/using/extract-file.md)

## Verwendungsfall: Importieren von Daten, die mit einem von der Systemsteuerung generierten Schlüssel verschlüsselt wurden {#use-case-gpg-decrypt}

In diesem Fall erstellen wir einen Workflow, um Daten zu importieren, die in einem externen System verschlüsselt wurden, und dabei einen in der Systemsteuerung generierten Schlüssel zu verwenden.

Die Schritte zum Ausführen dieses Anwendungsfalls lauten wie folgt:

1. Verwenden Sie die Systemsteuerung, um ein Schlüsselpaar (öffentlich/privat) zu generieren. Ausführliche Anweisungen finden Sie in der Dokumentation zur [Systemsteuerung](https://docs.adobe.com/content/help/en/control-panel/using/instances-settings/gpg-keys-management.html#decrypting-data).

   * Der öffentliche Schlüssel wird mit dem Drittsystem geteilt, das ihn zum Verschlüsseln der an Campaign zu sendenden Daten verwendet.
   * Der private Schlüssel wird von Campaign verwendet, um die eingehenden verschlüsselten Daten zu entschlüsseln.

   ![](assets/gpg_generate.png)

1. Verwenden Sie im externen System den aus der Systemsteuerung heruntergeladenen öffentlichen Schlüssel, um die Daten für den Import in Campaign Standard zu verschlüsseln.

   ![](assets/gpg_external.png)

1. Erstellen Sie in Campaign Standard einen Arbeitsablauf, um die verschlüsselten Daten zu importieren und mithilfe des über die Systemsteuerung installierten privaten Schlüssels zu entschlüsseln. Dazu erstellen wir einen Workflow wie folgt:

   ![](assets/gpg_workflow.png)

   * **[!UICONTROL Aktivität der Übertragungsdatei]** : Wandelt die Datei von einer externen Quelle in eine Kampagne um. In diesem Beispiel möchten wir die Datei von einem SFTP-Server übertragen.
   * **[!UICONTROL Datei]** laden: Lädt die Daten aus der Datei in die Datenbank und entschlüsselt sie mithilfe des in der Systemsteuerung generierten privaten Schlüssels.

1. Öffnen Sie die Aktivität **[!UICONTROL für die Übertragungsdatei]** und konfigurieren Sie sie entsprechend Ihren Anforderungen. Globale Konzepte zur Konfiguration der Aktivität finden Sie in [diesem Abschnitt](../../automating/using/load-file.md).

   Geben Sie auf der Registerkarte &quot; **[!UICONTROL Protokoll]** &quot;Details zum sftp-Server und der verschlüsselten GPG-Datei an, die Sie übertragen möchten.

   ![](assets/gpg_transfer.png)

1. Öffnen Sie die Aktivität **[!UICONTROL Datei]** laden und konfigurieren Sie sie dann entsprechend Ihren Anforderungen. Globale Konzepte zur Konfiguration der Aktivität finden Sie in [diesem Abschnitt](../../automating/using/load-file.md).

   Hinzufügen eine Vorverarbeitungsstufe zur Aktivität, um die eingehenden Daten zu entschlüsseln. Wählen Sie dazu in der Liste die Option &quot;GPG **[!UICONTROL entschlüsseln&quot;]** .

   >[!NOTE]
   >
   >Beachten Sie, dass Sie den privaten Schlüssel zum Entschlüsseln der Daten nicht angeben müssen. Der private Schlüssel wird in der Systemsteuerung gespeichert, die automatisch den Schlüssel erkennt, der zum Entschlüsseln der Datei verwendet wird.

   ![](assets/gpg_load.png)

1. Click **[!UICONTROL OK]** to confirm the activity configuration.

1. Sie können den Workflow jetzt ausführen.

## Verwendungsfall: Verschlüsseln und Exportieren von Daten mit einem in der Systemsteuerung installierten Schlüssel {#use-case-gpg-encrypt}

In diesem Fall erstellen wir einen Workflow, um Daten mithilfe eines in der Systemsteuerung installierten Schlüssels zu verschlüsseln und zu exportieren.

Die Schritte zum Ausführen dieses Anwendungsfalls lauten wie folgt:

1. Generieren Sie ein GPG-Schlüsselpaar (öffentlich/privat) mit einem GPG-Dienstprogramm und installieren Sie dann den öffentlichen Schlüssel in der Systemsteuerung. Ausführliche Anweisungen finden Sie in der Dokumentation zur [Systemsteuerung](https://docs.adobe.com/content/help/en/control-panel/using/instances-settings/gpg-keys-management.html#encrypting-data).

   ![](assets/gpg_install.png)

1. Erstellen Sie in Campaign Standard einen Arbeitsablauf, um die Daten zu exportieren und mit dem privaten Schlüssel zu exportieren, der über die Systemsteuerung installiert wurde. Dazu erstellen wir einen Workflow wie folgt:

   ![](assets/gpg-workflow-export.png)

   * **[!UICONTROL Aktivität der Abfrage]** : In diesem Beispiel möchten wir eine Abfrage ausführen, um die Daten aus der Datenbank, die wir exportieren möchten, Zielgruppe.
   * **[!UICONTROL Aktivität der Datei]** extrahieren: Verschlüsselt und extrahiert die Daten in eine Datei.
   * **[!UICONTROL Aktivität der Übertragungsdatei]** : Sendet die Datei mit den verschlüsselten Daten an einen SFTP-Server.

1. Konfigurieren Sie die Aktivität der **[!UICONTROL Abfrage]** , um die gewünschten Daten aus der Datenbank Zielgruppe. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../automating/using/query.md).

1. Öffnen Sie die Aktivität **[!UICONTROL Extract file]** und konfigurieren Sie sie dann entsprechend Ihren Anforderungen (Ausgabedatei, Spalten, Format usw.). Globale Konzepte zur Konfiguration der Aktivität finden Sie in [diesem Abschnitt](../../automating/using/extract-file.md).

   Hinzufügen eine Vorverarbeitungsstufe zur Aktivität, um die zu extrahierenden Daten zu verschlüsseln. Wählen Sie dazu den GPG-Verschlüsselungsschlüssel aus, der zum Verschlüsseln der Daten verwendet werden soll.

   ![](assets/gpg-extract-stage.png)

   >[!NOTE]
   >
   >Der Wert in Klammern ist der **Kommentar** , den Sie beim Generieren des Schlüsselpaars mit Ihrem GPG-Verschlüsselungstool definiert haben. Stellen Sie sicher, dass Sie den richtigen passenden Schlüssel auswählen, andernfalls kann der Empfänger die Datei nicht entschlüsseln.

1. Öffnen Sie die Aktivität für die **[!UICONTROL Übertragungsdatei]** und geben Sie dann den SFTP-Server an, an den Sie die Datei senden möchten. Globale Konzepte zur Konfiguration der Aktivität finden Sie in [diesem Abschnitt](../../automating/using/transfer-file.md).

   ![](assets/gpg-transfer-encrypt.png)

1. Sie können den Workflow jetzt ausführen. Nach der Ausführung wird die Zielgruppe der Daten durch die Abfrage in eine verschlüsselte GPG-Datei exportiert.

   ![](assets/gpg-sftp-encrypt.png)

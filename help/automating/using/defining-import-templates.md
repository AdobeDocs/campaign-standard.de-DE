---
title: Importvorlagen konfigurieren
description: Importvorlagen ermöglichen die Einschränkung der nötigen Einstellungen und den rascheren Datenimport.
page-status-flag: never-activated
uuid: 651eb57c-adac-4e3e-b454-b39aea1f0484
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
discoiquuid: 85d13147-fb31-446a-8476-f112c841fb82
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 44d6126023e9411477ccd7ffc07ecde806e7976d
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 100%

---


# Importvorlagen konfigurieren{#defining-import-templates}

Mit Importvorlagen kann der Administrator gewisse technische Importparameter konfigurieren. Diese Vorlagen können dann den Standardbenutzern zur Verfügung gestellt werden, um Datei-Uploads durchzuführen.

Eine Importvorlage wird vom funktionalen Administrator konfiguriert. Der Zugriff erfolgt über **[!UICONTROL Ressourcen]** > **[!UICONTROL Vorlagen]** > **[!UICONTROL Importvorlagen]**.

![](assets/import_template_list.png)

Drei schreibgeschützte Vorlagen stehen standardmäßig zur Verfügung:

* **[!UICONTROL Aktualisierung von Briefpost-Quarantänen und Versandlogs]**: Diese Vorlage dient als Grundlage für neue Importe, mit denen Briefpost-Quarantänen und -Versandlogs aktualisiert werden können. Der dieser Vorlage zugrunde liegende Workflow enthält die folgenden Aktivitäten:
* **[!UICONTROL Datenimport]**: Diese Vorlage ermöglicht Importe, die Daten aus einer Datei zur Datenbank hinzufügen. Der dieser Vorlage zugrunde liegende Workflow enthält die folgenden Aktivitäten:

   * **[!UICONTROL Datei laden]** - lädt Daten einer Datei auf den Adobe-Campaign-Server.
   * **[!UICONTROL Daten-Update]** - fügt die in der Datei enthaltenen Daten zur Datenbank hinzu.

* **[!UICONTROL Listenimport]**: Diese Vorlage ermöglicht Importe, die ausgehend von den Daten einer Datei Audiences vom Typ **Liste** erstellen. Der dieser Vorlage zugrunde liegende Workflow enthält die folgenden Aktivitäten:

   * **[!UICONTROL Datei laden]** - lädt Daten einer Datei auf den Adobe-Campaign-Server.
   * **[!UICONTROL Abstimmung]** - ordnet, wenn möglich, den importierten Daten eine Zielgruppendimension zu. Dies erlaubt im Anschluss die Erstellung einer Audience vom Typ **Liste**. Sollte die Zielgruppendimension der importierten Daten nicht bekannt sein, ist die erstellte Audience vom Typ **Datei**. Siehe [Zielgruppendimensionen und Ressourcen](../../automating/using/query.md#targeting-dimensions-and-resources).
   * **[!UICONTROL Audience-Speicherung]** - speichert die importierten Daten als Audience vom Typ **Liste**. Der Name der gespeicherten Audience entspricht dem Namen der importierten Datei, dem das Datum und die Uhrzeit des Imports als Suffix beigefügt werden. Beispiel: &#39;profiles_20150406_151448&#39;.

Diese Standardvorlagen sind schreibgeschützt und für Standardbenutzer nicht sichtbar. Um eine Vorlage zu erstellen, die Benutzer verwenden können, gehen Sie folgendermaßen vor:

1. Duplizieren Sie eine der Standardvorlagen. Die duplizierte Vorlage enthält drei Tabs:

   * **[!UICONTROL Eigenschaften]** mit den allgemeinen Eigenschaften der Importvorlage. Dieser Tab ermöglicht es insbesondere, die Vorlage zu aktivieren und eine Beispieldatei zu laden.
   * **[!UICONTROL Workflow]** zur Konfiguration des Import-Workflows. In diesem Tab werden die einzelnen Aktivitäten zur Ausführung des Imports definiert. Diese sind für den Benutzer, der sich letztlich des vereinfachten Imports bedient, nicht sichtbar.
   * **[!UICONTROL Ausgeführte Importe]** mit der Liste der anhand dieser Vorlage realisierten Importe. Angezeigt werden Status, Details und Ergebnisse aller auf der Vorlage beruhenden Importe. Von dieser Liste aus können Sie direkt auf den (für den Import durchführenden Endbenutzer verborgen ausgeführten) Workflow zugreifen.

1. Passen Sie im **[!UICONTROL Eigenschaften]**-Tab den Titel der Vorlage an und fügen Sie eine Beschreibung hinzu. Letztere ist für die Benutzer sichtbar, sobald die Vorlage verfügbar gemacht wurde.

   ![](assets/simplified_import_model1.png)

1. Gehen Sie in den **[!UICONTROL Workflow]**-Tab. Ergänzen Sie hier bei Bedarf den standardmäßig angebotenen Workflow mit weiteren Aktivitäten.

   Weiterführende Informationen zur Konfiguration der Workflow-Aktivitäten erfahren Sie im Anwendungsbeispiel in diesem Abschnitt: [Beispiel: Import-Workflow-Vorlage](../../automating/using/creating-import-workflow-templates.md). In diesem Anwendungsbeispiel wird gezeigt, wie ein Workflow für den wiederholten Import von Profilen aus einer CRM-Lösung in der Adobe-Campaign-Datenbank erstellt wird.

1. Speichern Sie die Vorlage, damit die Konfiguration des Workflows berücksichtigt wird.
1. Laden Sie im **[!UICONTROL Eigenschaften]**-Tab eine Beispieldatei. Neben den für den Import erforderlichen Spalten kann die Beispieldatei auch Daten enthalten, die es ermöglichen, den vereinfachten Import nach der Workflow-Erstellung zu testen. Die Beispieldatei steht nun auch späteren Benutzern zur Verfügung, die mithilfe der Vorlage einen Import durchführen.

   ![](assets/import_template_sample.png)

   Sie kann beispielsweise heruntergeladen und mit den zu importierenden Daten ausgefüllt werden. Dieser Zweck sollte bei der Auswahl der Beispieldatei berücksichtigt werden. Speichern Sie die Vorlage.

1. Die Beispieldatei wird fortan berücksichtigt. Sie können sie jederzeit lokal herunterladen, um ihren Inhalt zu prüfen. Verwenden Sie zur Auswahl einer anderen Beispieldatei die Option **[!UICONTROL Andere Beispieldatei verwenden]**.

   ![](assets/simplified_import_model2.png)

1. Gehen Sie erneut in den **[!UICONTROL Workflow]**-Tab und öffnen Sie die **[!UICONTROL Datei laden]**-Aktivität, um die Spaltenkonfiguration der zuvor geladenen Beispieldatei zu prüfen und gegebenenfalls anzupassen.
1. Testen Sie den Import, indem Sie den Workflow starten. Hierzu muss die im Schritt **5** geladene Beispieldatei Daten enthalten.

   Die Daten der Beispieldatei werden dann importiert. Verwenden Sie fiktive Daten in geringem Umfang, um die Kapazität Ihrer Datenbank nicht zu überfordern.

1. Prüfen Sie nun das Workflow-Ausführungsprotokoll, auf das Sie über die entsprechende Schaltfläche in der Symbolleiste zugreifen können. Sollten Fehler aufgetreten sein, ist die Konfiguration der Aktivitäten zu prüfen.

   ![](assets/simplified_import_model3.png)

1. Setzen Sie im **[!UICONTROL Eigenschaften]**-Tab den **[!UICONTROL mportvorlagen-Status]** auf **[!UICONTROL Verfügbar]** und speichern Sie die Vorlage. Wenn die Vorlage nicht mehr verwendet werden soll, können Sie den **[!UICONTROL Importvorlagen-Status]** auf **[!UICONTROL Archiviert]** setzen.

Der Vorlagen-Workflow kann geändert werden, indem die Beispieldatei erneut hochgeladen und die Konfiguration **[!UICONTROL Datei laden]** überprüft wird.

Die Importvorlage ist jetzt für Benutzer zum Hochladen von Dateien verfügbar.

**Verwandte Themen:**

* [Workflows](../../automating/using/get-started-workflows.md)
* [Datenimport und -export](../../automating/using/about-data-import-and-export.md)
* [Beispiel: Import-Workflow-Vorlage](../../automating/using/creating-import-workflow-templates.md)


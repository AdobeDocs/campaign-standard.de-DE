---
title: Dateiextraktion
description: Die Dateiextraktionsaktivität erlaubt den Export von in Adobe Campaign enthaltenen Daten in Form von externen Dateien.
page-status-flag: never-activated
uuid: 631f0fbd-9e8d-4f77-a338-fcb7f4fc1774
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: a06509f9-4731-4187-b43d-3bfa361284d3
context-tags: fileExport,main
internal: n
snippet: y
translation-type: ht
source-git-commit: 15e5aebdd67e8f5ddee89506c0469a101d94d2e8
workflow-type: ht
source-wordcount: '445'
ht-degree: 100%

---


# Dateiextraktion{#extract-file}

## Beschreibung {#description}

![](assets/export.png)

Die Aktivität **[!UICONTROL Dateiextraktion]** erlaubt den Export von in Adobe Campaign enthaltenen Daten in Form von externen Dateien.

## Anwendungskontext {#context-of-use}

Die Art der Datenextraktion wird im Zuge der Aktivitätskonfiguration definiert.

>[!CAUTION]
>
>Die Aktivität **[!UICONTROL Dateiextraktion]** kann nur im Anschluss an eine **[!UICONTROL Abfrage]**-Aktivität verwendet werden.

**Verwandte Themen:**

* [Anwendungsfall: Profile in eine externe Datei exportieren](../../automating/using/exporting-profiles-in-file.md)

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Dateiextraktion]** in den Workflow-Arbeitsbereich.

   ![](assets/wkf_data_export1.png)

1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der im Schnellzugriff angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Geben Sie den Titel der **Ausgabedatei** an. Der Dateiname wird automatisch mit dem Datum und der Uhrzeit der Erstellung ergänzt, um seine Eindeutigkeit zu gewährleisten, z. B.: Empfänger_20150815_081532.txt für eine Datei, die am 15. August 2015 um 8.15 Uhr und 32 Sekunden erstellt wurde.

   >[!NOTE]
   >
   >Sie können den Dateinamen mit der in diesem Feld befindlichen Funktion **[!UICONTROL formatDate]** spezifizieren.

1. Sie können die Ausgabedatei bei Bedarf komprimieren, indem Sie im Feld **[!UICONTROL Vorab-Bearbeitungsetappe hinzufügen]** die Option **[!UICONTROL Komprimierung]** auswählen. Die Ausgabedatei wird in eine GZIP-Datei (.gz) komprimiert.

   Das Feld **[!UICONTROL Vorab-Bearbeitungsetappe hinzufügen]** ermöglicht Ihnen auch, eine Datei zu verschlüsseln, bevor Sie sie extrahieren. Weitere Informationen zum Arbeiten mit verschlüsselten Dateien finden Sie in [diesem Abschnitt](../../automating/using/managing-encrypted-data.md)

1. Fügen Sie mithilfe der Schaltflächen ![](assets/add_darkgrey-24px.png) oder **[!UICONTROL Element hinzufügen]** eine Ausgabespalte hinzu.

   ![](assets/wkf_data_export2.png)

   Es öffnet sich ein neues Fenster.

   ![](assets/wkf_data_export3.png)

1. Erstellen Sie einen Ausdruck. Hierzu können Sie einen bereits existierenden Ausdruck auswählen oder mit dem **Ausdruckseditor** einen neuen erstellen.
1. Validieren Sie den Ausdruck.

   Der Ausdruck wird den Ausgabespalten hinzugefügt.

1. Erstellen Sie so viele Spalten wie nötig. Klicken Sie zur Bearbeitung der Spalten auf deren Ausdruck oder Titel.

   Wenn Sie Profile exportieren, um sie in einem externen Tool zu verwenden, empfehlen wir auch den Export einer eindeutigen Kennung. Nicht alle Profile verfügen standardmäßig über eine eindeutige Kennung. Dies hängt von der Weise ab, wie sie zur Datenbank hinzugefügt werden. Weiterführende Informationen finden Sie im Abschnitt [Eindeutige Kennung für Profile erstellen](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources).

1. Klicken Sie auf den **[!UICONTROL Dateistruktur]**-Tab, um das Ausgabe-, Datums- und Zahlenformat der zu exportierenden Datei zu konfigurieren.

   Wenn Sie Auflistungswerte exportieren, aktivieren Sie die Option **[!UICONTROL Titel anstelle der internen Werte der Auflistungen exportieren]**. Mit dieser Option können Sie kürzere Titel abrufen, die einfacher verständlich sind als IDs.

1. Wählen Sie im Tab **[!UICONTROL Eigenschaften]** die Option **[!UICONTROL Keine Datei erstellen, wenn die eingehende Transition leer ist]** aus, um zu verhindern, dass leere Dateien erstellt und auf SFTP-Server hochgeladen werden, wenn die eingehende Transition leer ist.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

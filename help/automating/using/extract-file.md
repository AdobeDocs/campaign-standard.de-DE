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
translation-type: tm+mt
source-git-commit: 2a8cb9aa0d018fec9d5b256beba079c5ec3afaf0
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 95%

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

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Dateiextraktion]** in den Workflow-Arbeitsbereich.

   ![](assets/wkf_data_export1.png)

1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der im Schnellzugriff angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Geben Sie den Titel der **Ausgabedatei** an. Der Dateiname wird automatisch mit dem Datum und der Uhrzeit der Erstellung ergänzt, um seine Eindeutigkeit zu gewährleisten, z. B.: Empfänger_20150815_081532.txt für eine Datei, die am 15. August 2015 um 8.15 Uhr und 32 Sekunden erstellt wurde.

   >[!NOTE]
   >
   >Sie können den Dateinamen mit der in diesem Feld befindlichen Funktion **[!UICONTROL formatDate]** spezifizieren.

1. Sie können die Ausgabedatei bei Bedarf komprimieren, indem Sie im Feld **[!UICONTROL Anschlussvorgangsetappe hinzufügen]** die Option **[!UICONTROL Komprimierung]** auswählen. Die Ausgabedatei wird in eine GZIP-Datei (.gz) komprimiert.

   Das **[!UICONTROL Hinzufügen Feld für einen Schritt]** vor der Verarbeitung ermöglicht Ihnen auch, eine Datei zu verschlüsseln, bevor Sie sie extrahieren. Weitere Informationen zum Arbeiten mit verschlüsselten Dateien finden Sie in [diesem Abschnitt](../../automating/using/managing-encrypted-data.md)

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

## Beispiel {#example}

Im folgenden Beispiel wird die Konfiguration einer auf eine **[!UICONTROL Abfrage]** folgenden **[!UICONTROL Dateiextraktion]** erläutert.

Ziel dieses Workflows ist es, eine Profilliste in eine externe Datei zu exportieren, um die Daten außerhalb von Adobe Campaign verwenden zu können.

1. Platzieren Sie eine **[!UICONTROL Dateiextraktion]** im Anschluss an eine **[!UICONTROL Abfrage]** im Workflow-Arbeitsbereich.

   Im vorliegenden Beispiel werden alle Profile im Alter von 18 bis 30 Jahren aus der Datenbank abgefragt.

1. Öffnen Sie die Dateiextraktion, um sie zu konfigurieren.
1. Benennen Sie die Ausgabedatei.
1. Fügen Sie die gewünschten Ausgabespalten hinzu.

   Im vorliegenden Beispiel sind dies E-Mail-Adresse, Alter, Geburtsdatum, Vor- und Nachname der abgefragten Profile.

   ![](assets/wkf_data_export6.png)

1. Gehen Sie in den **[!UICONTROL Dateistruktur]**-Tab und definieren Sie folgende Elemente:

   * CSV als Ausgabeformat,

      ![](assets/wkf_data_export7.png)

   * Datumsformat,

      ![](assets/wkf_data_export9.png)

1. Validieren Sie die Aktivität.
1. Platzieren Sie nun im Anschluss an die **[!UICONTROL Dateiextraktion]** eine **[!UICONTROL Dateiübertragung]**, um die Extraktionsdatei mittels eines externen Kontos abrufen zu können.
1. Öffnen Sie die Aktivität und wählen Sie die Aktion **[!UICONTROL Datei-Upload]** aus.

   ![](assets/wkf_data_export11.png)

1. Wählen Sie ein externes Konto aus und geben Sie den Pfad des Ordners auf dem Server an.

   ![](assets/wkf_data_export12.png)

1. Validieren Sie die Aktivität und speichern Sie den Workflow.
1. Starten Sie den Workflow.

   Nach erfolgreicher Ausführung des Workflows ist die Extraktionsdatei im externen Konto verfügbar.


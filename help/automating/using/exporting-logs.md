---
title: Logs exportieren
description: Mit Sendungen oder Abonnements verknüpfte Log-Daten können mit einem einfachen Workflow exportiert werden.
page-status-flag: never-activated
uuid: 954e919c-0a33-47c3-9a3c-63c7a2a4edc4
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
discoiquuid: ca8a95d8-523f-4085-a2fc-e1d8262cfbae
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 68e825bc3b6b7f94f61875e7da2bc8f63f06d9cb

---


# Logs exportieren{#exporting-logs}

Mit Sendungen oder Abonnements verknüpfte Log-Daten können mit einem einfachen Workflow exportiert werden. Dadurch können Sie die Ergebnisse Ihrer Kampagnen in Ihrem eigenen Business Intelligence Tool analysieren.

By using an **[!UICONTROL Incremental query]** that only retrieves new logs every time the workflow is executed and a simple **[!UICONTROL Extract file]** activity to define the output columns, you can get a file with the format and all the data you need. Then use a **[!UICONTROL Transfer file]** activity to retrieve the final file. Each workflow execution is planned by a **[!UICONTROL Scheduler]**.

Der Log-Export kann von Standardbenutzern durchgeführt werden. Private Ressourcen wie Broadlogs, Trackinglogs, Ausschlusslogs, Abonnentenlogs und Abonnementverlauflogs können nur vom funktionalen Administrator auf **Profile** verwaltet werden.

1. Erstellen Sie einen neuen Workflow wie in [diesem Abschnitt](../../automating/using/building-a-workflow.md#creating-a-workflow) beschrieben.
1. Add a **[!UICONTROL Scheduler]** activity and set it according to your needs. Unten finden Sie ein Beispiel für eine monatliche Ausführung.

   ![](assets/export_logs_scheduler.png)

1. Add an **[!UICONTROL Incremental query]** activity and configure it so that it selects the logs you need. Um beispielsweise alle neuen oder aktualisierten Broadlogs (Versandlogs der Profile) auszuwählen, gehen Sie folgendermaßen vor:

   * In the **[!UICONTROL Properties]** tab, change the target resource to **Delivery logs** (broadLogRcp).

      ![](assets/export_logs_query_properties.png)

   * In the **[!UICONTROL Target]** tab, set a condition to retrieve all delivery logs that correspond to deliveries sent in 2016 or after. Weiterführende Informationen hierzu finden Sie im Abschnitt [Abfragetool](../../automating/using/editing-queries.md#creating-queries).

      ![](assets/export_logs_query_target.png)

   * Wählen Sie auf der **[!UICONTROL Processed data]** Registerkarte das Feld **[!UICONTROL Use a date field]** lastModified **** aus. Bei der nächsten Ausführung des Workflows werden nur Logs abgerufen, die nach der letzten Ausführung geändert oder erstellt wurden.

      ![](assets/export_logs_query_processeddata.png)

      In diesem Tab ist nach der ersten Ausführung des Workflows das Datum der jeweils letzten Ausführung zu sehen, welches wiederum für die nächste Ausführung herangezogen wird. Es wird automatisch bei jeder Ausführung des Workflows aktualisiert. Sie können diesen Wert auch überschreiben, indem Sie einen neuen eingeben.

1. Add an **[!UICONTROL Extract file]** activity that will export the queried data in a file:

   * In the **[!UICONTROL Extraction]** tab, specify the name of the file.

      If you select the **[!UICONTROL Add date and time to the file name]** option, this name will be automatically completed with the date of the export to ensure all extracted files are unique. Wählen Sie die Spalten, die in Ihrer Datei exportiert werden sollen. Hier können Sie Daten von verwandten Ressourcen auswählen, wie etwa Versand- oder Profilinformationen.

      >[!NOTE]
      >
      >To export a unique identifier for each log, select the **[!UICONTROL Delivery log ID]** element.

      Zum Ordnen der endgültigen Datei können Sie eine Sortierung vornehmen. Beispielsweise können Sie wie unten gezeigt das Log-Datum sortieren.

      ![](assets/export_logs_extractfile_extraction.png)

   * In the **[!UICONTROL File structure]** tab, define the format of the output file to match your needs.

      Aktivieren Sie die **[!UICONTROL Export labels instead of internal values of enumerations]** Option, falls Sie Auflistungen exportieren. Mit dieser Option können Sie kürzere Titel abrufen, die einfacher verständlich sind als IDs.

1. Add a **[!UICONTROL Transfer file]** activity and configure it to transfer the newly created file from the Adobe Campaign server to another location where you can access it, such as a SFTP server.

   * In the **[!UICONTROL General]** tab, select **[!UICONTROL File upload]** as the purpose is to send the file from Adobe Campaign to another server.
   * In the **[!UICONTROL Protocol]** tab, specify the transfer parameters and select the [external account](../../administration/using/external-accounts.md#creating-an-external-account) to use.

1. Add an **[!UICONTROL End]** activity to make sure it properly ends and save your workflow.

   ![](assets/export_logs_example_workflow.png)

Jetzt können Sie den Workflow ausführen und die Ausgabedatei auf dem externen Server abrufen.

**Verwandtes Thema:**

[Workflows](../../automating/using/get-started-workflows.md)

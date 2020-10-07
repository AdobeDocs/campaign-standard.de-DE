---
title: Profile in eine externe Datei exportieren
description: In diesem Anwendungsfall wird gezeigt, wie man eine Profilliste in eine externe Datei exportiert, um die Daten außerhalb von Adobe Campaign verwenden zu können.
page-status-flag: never-activated
uuid: 631f0fbd-9e8d-4f77-a338-fcb7f4fc1774
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: a06509f9-4731-4187-b43d-3bfa361284d3
context-tags: fileExport,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 100%

---


# Profile in eine externe Datei exportieren {#exporting-profiles-external-file}

Im folgenden Beispiel wird die Konfiguration einer auf eine **[!UICONTROL Abfrage]** folgenden **[!UICONTROL Dateiextraktion]** erläutert.

Ziel dieses Workflows ist es, eine Profilliste in eine externe Datei zu exportieren, um die Daten außerhalb von Adobe Campaign verwenden zu können.

1. Platzieren Sie eine [Dateiextraktion](../../automating/using/extract-file.md) im Anschluss an eine [Abfrage](../../automating/using/query.md) im Workflow-Arbeitsbereich.

   Im vorliegenden Beispiel werden alle Profile im Alter von 18 bis 30 Jahren aus der Datenbank abgefragt.

1. Öffnen Sie die Aktivität **[!UICONTROL Dateiextraktion]**, um sie zu konfigurieren.
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
1. Platzieren Sie nun im Anschluss an die **[!UICONTROL Dateiextraktion]** eine [Dateiübertragung](../../automating/using/transfer-file.md), um die Extraktionsdatei mittels eines externen Kontos abrufen zu können.
1. Öffnen Sie die Aktivität und wählen Sie die Aktion **[!UICONTROL Datei-Upload]** aus.

   ![](assets/wkf_data_export11.png)

1. Wählen Sie ein externes Konto aus und geben Sie den Pfad des Ordners auf dem Server an.

   ![](assets/wkf_data_export12.png)

1. Validieren Sie die Aktivität und speichern Sie den Workflow.
1. Starten Sie den Workflow.

   Nach erfolgreicher Ausführung des Workflows ist die Extraktionsdatei im externen Konto verfügbar.

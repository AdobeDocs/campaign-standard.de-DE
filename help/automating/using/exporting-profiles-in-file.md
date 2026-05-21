---
title: Profile in eine externe Datei exportieren
description: In diesem Anwendungsfall wird gezeigt, wie man eine Profilliste in eine externe Datei exportiert, um die Daten außerhalb von Adobe Campaign verwenden zu können.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: fileExport,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 3fc286a9-bba4-4e3d-95cd-600eed4943e7
TQID: https://experienceleague.adobe.com/wVo-oDNJNFmaNcb7p6fACNIfrPG-2Y-VbXxXG0P8XTQ
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 240
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

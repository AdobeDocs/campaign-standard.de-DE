---
title: Daten basierend auf einem automatischen Datei-Download aktualisieren
description: Das folgende Beispiel zeigt das Laden einer Datei, die mithilfe einer Dateiübertragung abgerufen wurde. Im Anschluss erlauben die enthaltenen Daten die Aktualisierung der Datenbank.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: fileImport,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 2b21cf45-1c40-4e0e-ae2c-28c9f73e1964
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 100%

---

# Daten basierend auf einem automatischen Datei-Download aktualisieren {#updating-data-automatic-file-download}

Die Ladeaktivität dient in erster Linie der Strukturierung von Daten, die mithilfe der Dateiübertragung in die bereits in der Datenbank vorhandenen Daten integriert werden sollen.

Das folgende Beispiel zeigt das Laden einer Datei, die mithilfe einer Dateiübertragung abgerufen wurde. Im Anschluss erlauben die enthaltenen Daten die Aktualisierung der Datenbank. Dieser Workflow dient der Profilanreicherung der Adobe Campaign-Datenbank oder der Aktualisierung bereits existierender Profile anhand aus der importierten Datei stammender Daten.

![](assets/load_file_workflow_ex1.png)

Gehen Sie wie folgt vor, um den Workflow zu erstellen:

1. Ziehen Sie eine [Dateiübertragung](../../automating/using/transfer-file.md) in den Workflow-Arbeitsbereich.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in der Schnellaktion angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Konfigurieren Sie die Aktivität so, dass sie die gewünschte Datei abruft. Wählen Sie im **[!UICONTROL Protokoll]**-Tab **SFTP** aus.
1. Aktivieren Sie die Option **In einem externen Konto definierte Verbindungsparameter verwenden**.
1. Geben Sie den Namen des externen Kontos an.
1. Geben Sie den **Pfad der Dateien auf dem Remote-Server** an.

   ![](assets/wkf_file_transfer_07.png)

1. Validieren Sie die Aktivität.
1. Ziehen Sie per Drag-and-Drop eine Aktivität [Datei laden](../../automating/using/load-file.md) in Ihren Workflow und platzieren Sie sie nach der Aktivität **[!UICONTROL Datei übertragen]**.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in den Schnellaktionen angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Aktivieren Sie im Tab **[!UICONTROL Ausführung]** im Bereich **[!UICONTROL Zu ladende Datei]** die Option **[!UICONTROL Datei der eingehenden Transition verwenden]**.

   ![](assets/wkf_file_loading8.png)

1. Konfigurieren Sie die Aktivität wie oben beschrieben.
1. Ziehen Sie nun per Drag-and-Drop eine Aktivität [Daten katualisieren](../../automating/using/update-data.md) in Ihren Workflow und platzieren Sie sie nach der Aktivität **[!UICONTROL Datei laden]** und konfigurieren Sie sie.

Starten Sie den Workflow. Die gewünschte Datei wird geladen, die Daten werden extrahiert und die Adobe Campaign-Datenbank wird angereichert.

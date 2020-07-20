---
title: Daten basierend auf einem automatischen Datei-Download aktualisieren
description: 'Das folgende Beispiel zeigt das Laden einer Datei, die mithilfe einer Dateiübertragung abgerufen wurde. Im Anschluss erlauben die enthaltenen Daten die Aktualisierung der Datenbank. '
page-status-flag: never-activated
uuid: 69af12cc-6f82-4977-9f53-aa7bc26f5d7e
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: 584ff893-9b1b-46c9-9628-714ab349ab88
context-tags: fileImport,main
internal: n
snippet: y
translation-type: ht
source-git-commit: 7ffa48365875883a98904d6b344ac005afe26e18
workflow-type: ht
source-wordcount: '296'
ht-degree: 100%

---


# Daten basierend auf einem automatischen Datei-Download aktualisieren {#updating-data-automatic-file-download}

Die Ladeaktivität dient in erster Linie der Strukturierung von Daten, die mithilfe der Dateiübertragung in die bereits in der Datenbank vorhandenen Daten integriert werden sollen.

Das folgende Beispiel zeigt das Laden einer Datei, die mithilfe einer Dateiübertragung abgerufen wurde. Im Anschluss erlauben die enthaltenen Daten die Aktualisierung der Datenbank. Dieser Workflow dient der Profilanreicherung der Adobe-Campaign-Datenbank oder der Aktualisierung bereits existierender Profile anhand aus der importierten Datei stammender Daten.

![](assets/load_file_workflow_ex1.png)

Gehen Sie wie folgt vor, um den Workflow zu erstellen:

1. Ziehen Sie eine [Dateiübertragung](../../automating/using/transfer-file.md) in den Workflow-Arbeitsbereich.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der im Schnellzugriff angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Konfigurieren Sie die Aktivität so, dass sie die gewünschte Datei abruft. Wählen Sie im **[!UICONTROL Protokoll]**-Tab **SFTP** aus.
1. Aktivieren Sie die Option **In einem externen Konto definierte Verbindungsparameter verwenden**.
1. Geben Sie den Namen des externen Kontos an.
1. Geben Sie den **Pfad der Dateien auf dem Remote-Server** an.

   ![](assets/wkf_file_transfer_07.png)

1. Validieren Sie die Aktivität.
1. Schließen Sie eine [Datei laden](../../automating/using/load-file.md)-Aktivität an die Aktivität **[!UICONTROL Dateiübertragung]** an.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in den Quick Actions angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Aktivieren Sie im Tab **[!UICONTROL Ausführung]** im Bereich **[!UICONTROL Zu ladende Datei]** die Option **[!UICONTROL Datei der eingehenden Transition verwenden]**.

   ![](assets/wkf_file_loading8.png)

1. Konfigurieren Sie die Aktivität wie oben beschrieben.
1. Schließen Sie nun ein [Daten-Update](../../automating/using/update-data.md) an die **[!UICONTROL Datei laden]**-Aktivität an und konfigurieren Sie es.

Starten Sie den Workflow. Die gewünschte Datei wird geladen, die Daten werden extrahiert und die Adobe-Campaign-Datenbank wird angereichert.

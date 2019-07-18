---
title: Workflow-Oberfläche
seo-title: Workflow-Oberfläche
description: Workflow-Oberfläche
seo-description: Hier erhalten Sie Informationen über die Benutzeroberfläche und die Optionen zum Erstellen, Bearbeiten und Ausführen von Workflows.
page-status-flag: nie aktiviert
uuid: aafe 33 ed-fa 07-4 dd 9-825 e -242099334 f 1 a
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird automatisiert
content-type: Referenz
topic-tags: about-workflows-and-data-management
discoiquuid: 147 fbb 0 d -17 d 2-444 b-a 215-9 ad 14179 c 549
context-tags: workflow, main; Workflow, Übersicht
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ff0b995533f34dd8eab7a9a82feaab3ceed4ff29

---


# Workflow-Oberfläche{#workflow-interface}

Im Rahmen von Programmen und Kampagnen dienen Workflows der Automatisierung von umfangreichen Arbeitsabläufen.

Die Workflow-Benutzeroberfläche weist folgende Elemente auf:

* [Palette](../../automating/using/workflow-interface.md#palette) mit den verfügbaren Aktivitäten;
* [Arbeitsbereich](../../automating/using/workflow-interface.md#workspace), in dem Aktivitäten angeordnet und konfiguriert werden;
* [Symbolleiste](../../automating/using/workflow-interface.md#action-bar) mit Schaltflächen, die die Interaktion mit dem Workflow und seinen Komponenten ermöglichen.
* [Quick Actions](../../automating/using/workflow-interface.md#quick-actions), die um eine ausgewählte Aktivität herum angezeigt werden und den Schnellzugriff auf diverse Aktionen ermöglichen.

![](assets/wkf_overview.png)

## Palette {#palette}

Die Palette befindet sich auf der linken Bildschirmseite. Die verfügbaren Aktivitäten sind verschiedenen Kategorien zugeordnet:

* [Zielgruppenbestimmung](../../automating/using/about-targeting-activities.md) - Aktivitäten, die der Erstellung von Zielgruppen und der Verwendung bzw. Filterung von Populationen dienen.
* [Ausführung](../../automating/using/about-execution-activities.md) - Aktivitäten, die der Organisation und Ausführung von Workflows dienen.
* [Kanäle](../../automating/using/about-channel-activities.md) - Aktivitäten, die die verschiedenen Kommunikationskanäle repräsentieren.
* [Data Management (ETL)](../../automating/using/about-data-management-activities.md) - Aktivitäten, die dem Umgang mit Daten dienen.

Ziehen Sie die für Ihren Workflow erforderlichen Aktivitäten aus der Palette an die gewünschte Stelle im Arbeitsbereich.

Jede Aktivität muss separat konfiguriert werden, bevor Sie den Workflow starten.

![](assets/workflow_palette.png)

## Arbeitsbereich {#workspace}

Die zentrale Fläche im Editor bildet den Arbeitsbereich des Workflows. Hier werden die verwendeten Aktivitäten abgelegt, mithilfe von Transitionen in Beziehung gesetzt und konfiguriert.

Um zwei Aktivitäten miteinander zu verbinden, ziehen Sie das Ende des Pfeils der ersten Aktivität zur nächsten Aktivität, bis sie miteinander verbunden werden. Sie können die Aktivität auch zur davorliegenden Pfeilspitze ziehen, um diese Aktivität mit der vorhergehenden zu verbinden. Wenn eine der zwei Aktivitäten verschoben wird, bleiben sie trotzdem verbunden.

Bei Aktivitäten, die Daten verarbeiten, enthalten die ausgehenden Transitionen die Zwischenergebnisse. Sie können darauf zugreifen, wenn Sie im Abschnitt **[!UICONTROL Ausführung]** der Workflow-Eigenschaften die Option **Zwischenergebnis festhalten]angekreuzt haben.[!UICONTROL **

Bei Markierung einer Aktivität erscheinen um diese herum die Quick Actions, die den Schnellzugriff auf diverse Aktionen ermöglichen. Um beispielsweise eine Aktivität zu konfigurieren, können Sie diese markieren und mithilfe der Quick-Action-Schaltfläche ![ öffnen.](assets/edit_darkgrey-24px_table.png)

Gewisse Funktionen stehen nur im Arbeitsbereich zur Verfügung:

* Zeichnen einer Auswahlzone um mehrere Aktivitäten und Transitionen, um diese gleichzeitig zu markieren.
* Taste **Strg** + Linksklick zur Auswahl mehrerer Aktivitäten und/oder Transitionen.
* Taste **Enter** zum Zugriff auf die Detailansicht der aktuell ausgewählten Aktivität oder Transition.
* Taste **Entf** zum Löschen der aktuell ausgewählten Aktivität.
* Verwenden Sie **Strg + C**, um die ausgewählten Aktivitäten zu kopieren, und **Strg + V**, um sie in den Arbeitsbereich einzufügen.

![](assets/workflow_workspace.png)

## Symbolleiste {#action-bar}

Je nach im Arbeitsbereich ausgewählten Elementen oder Workflow-Status sind in der Symbolleiste unterschiedliche Schaltflächen verfügbar.

<img height="21px" src="assets/edit_darkgrey-24px.png" /> **[!UICONTROL Open activityes ermöglicht]**<br/>Ihnen, die Eigenschaften des Workflows zu bearbeiten.

<img height="21px" src="assets/play_darkgrey-24px_table.png" /> **[!UICONTROL Startstart]**<br/>startet den Workflow.

<img height="21px" src="assets/pause_darkgrey-24px_table.png" /> **[!UICONTROL Pausepauses]**<br/>des Workflows.

<img height="21px" src="assets/stop_darkgrey-24px_table.png" /> **[!UICONTROL Ausführung des Workflow-]**<br/>Arbeitsablaufs. Eine Wiederaufnahme an der Stelle, an der er gestoppt wurde, ist nicht möglich.

<img height="21px" src="assets/pauseplay_darkgrey-24px_table.png" /> **[!UICONTROL Restartrestarts]**<br/>startet den Workflow.

<img height="21px" src="assets/printpreview_darkgrey-24px_table.png" /> **[!UICONTROL Protokoll und tasksausführungsprotokoll wird geöffnet]**<br/>.

<img height="21px" src="assets/checkcircle_darkgrey-24px_table.png" /> **[!UICONTROL Mehrfachauswahl aktivieren Aktiviert Modus]**<br/>für mehrere Auswahlmöglichkeiten. Der Workflow muss mindestens zwei Aktivitäten enthalten.

<img height="21px" src="assets/closecircle_darkgrey-24px_table.png" /> **[!UICONTROL Deaktivieren Sie Multi-selectiondisables]**<br/>Multi-Selection Mode.<br />

<img height="21px" src="assets/targeted.png" /> **[!UICONTROL Open transitionöffnen]**<br/>Sie den ausgewählten Übergang.<br />

<img height="21px" src="assets/check_darkgrey-24px_table.png" />  **[!UICONTROL Normale executionre]**<br/>-Aktivierung Aktiviert die Auswahl, wenn sie zuvor deaktiviert oder als angehalten gekennzeichnet wurde.<br />

<img height="21px" src="assets/check_pause_darkgrey-24px_table.png" /> **[!UICONTROL Execususpendedanhalten]**<br/>des Workflows für die ausgewählte Aktivität.<br />

<img height="21px" src="assets/checkdisable.png" /> **[!UICONTROL No executiondisables]**<br/>the activity.<br />

<img height="21px" src="assets/delete_darkgrey-24px_table.png" /> **[!UICONTROL Löschen Sie selectionlöscht]**<br/>die ausgewählten Aktivitäten.<br />

<img height="21px" src="assets/copy_24px.png" /> **[!UICONTROL Selectioncopies]**<br/>Die ausgewählten Aktivitäten kopieren.

<img height="21px" src="assets/paste_24px.png" /> **[!UICONTROL Pastepastes]**<br/>die kopierten Aktivitäten.

## Quick Actions {#quick-actions}

Bei Markierung einer Aktivität erscheinen um diese herum die Quick-Action-Schaltflächen, die den direkten Zugriff auf gewisse Funktionen ermöglichen.

<img height="21px" src="assets/edit_darkgrey-24px.png" /> **[!UICONTROL Open activityöffnen]**<br/>Sie die ausgewählte Aktivität.

<img height="21px" src="assets/copy_24px.png" /> **[!UICONTROL Selectioncopies]**<br/>Die ausgewählte Aktivität kopiert.

<img height="21px" src="assets/wkf_dlv_act_params_icon.png" /> **[!UICONTROL Öffnen Sie die erweiterte optionenöffnet die]**<br/>erweiterten Optionen der ausgewählten E-Mail- oder SMS-Bereitstellungsaktivität.

<img height="21px" src="assets/check_darkgrey-24px_table.png" /> **[!UICONTROL Normale executionre]**<br/>-Aktivierung Aktiviert die Auswahl, wenn sie zuvor deaktiviert oder als angehalten gekennzeichnet wurde.

<img height="21px" src="assets/check_pause_darkgrey-24px_table.png" /> **[!UICONTROL Execususpendedanhalten]**<br/>des Workflows für die ausgewählte Aktivität.

<img height="21px" src="assets/checkdisable.png" /> **[!UICONTROL No executiondisables]**<br/>the activity.

<img height="21px" src="assets/pending_darkgrey-24px_table.png" /> **[!UICONTROL Sofortige executionerzwingt]**<br/>sofort die sofortige Verarbeitung der Auswahl. Diese Schaltfläche steht nur für die Aktivitäten <span class="uicontrol">Planung</span> und <span class="uicontrol">Warten</span> zur Verfügung.

<img height="21px" src="assets/delete_darkgrey-24px_table.png" /> **[!UICONTROL Löschen Sie selectionlöscht]**<br/>die ausgewählten Aktivitäten.

## Workflow-Aktivitäten duplizieren {#duplicating-workflow-activities}

Sie können in einem Workflow Aktivitäten duplizieren, indem Sie sie mit Copy &amp; Paste in denselben Workflow oder einen anderen Workflow derselben Campaign-Instanz einfügen.

Die Konfiguration der duplizierten Aktivitäten bleibt dabei unverändert. Bei Versandaktivitäten (E-Mail, SMS, Push-Benachrichtigungen etc.) wird das an die Aktivität angehängte Versandobjekt dupliziert.

>[!NOTE]
>
>Workflow-Aktivitäten einer Instanz können nicht in einer anderen Instanz dupliziert werden. Aktivitäten von technischen Workflows können nicht dupliziert werden.

Um eine Aktivität zu duplizieren, gehen Sie wie folgt vor:

1. Wählen Sie die Aktivität und danach im Schnellzugriff die Schaltfläche **[!UICONTROL Auswahl kopieren]aus.**

   Sie können auch die Tastenkombination **Strg + C** verwenden.

   ![](assets/wkf_copypaste1.png)

1. Rechtsklicken Sie auf den Arbeitsbereich des Ziel-Workflows und wählen Sie dann die Schaltfläche **[!UICONTROL Einfügen]aus.**

   Sie können auch die Tastenkombination **Strg + V** verwenden.

   ![](assets/wkf_copypaste2.png)

1. Die Aktivität wird mit allen zuvor konfigurierten Einstellungen dupliziert.

Sie können auch mehrere Aktivitäten mit Copy &amp; Paste kopieren, sodass ein gesamter Workflow dupliziert werden kann.

Wählen Sie dabei die Aktivitäten aus, indem Sie rund um sie einen Kreis ziehen. Wählen Sie dann in der Symbolleiste die Schaltfläche **[!UICONTROL Auswahl kopieren]** aus (oder drücken Sie **Strg + C**). Danach können Sie die Aktivitäten an der gewünschten Position einfügen.

![](assets/wkf_copypaste3.png)


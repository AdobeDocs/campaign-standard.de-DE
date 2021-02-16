---
solution: Campaign Standard
product: campaign
title: Überschneidende Ausführung geplanter Workflows
description: Erfahren Sie, wie Sie eine überlappende Ausführung geplanter Workflows verhindern können.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
translation-type: tm+mt
source-git-commit: 4a61c988f95dd84797e6e33707651304223045fb
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---


# Überschneidende Ausführung terminierter Workflows{#preventing-overlapping-execution-of-scheduled-workflows}

## Informationen zur geplanten Workflows

In Campaign Standards garantiert das Workflow-Engine, dass eine Workflow-Instanz nur von einem Prozess ausgeführt wird. Das Sperren von Aktivitäten wie Importen, langwierigen Abfragen oder Schreiben in die Datenbank verhindert die Ausführung einer anderen Aufgabe während der Ausführung.

Andererseits blockieren nicht blockierende Aktivitäten nicht die Ausführung anderer Aufgaben (normalerweise warten Aktivitäten auf ein Ereignis wie die **[!UICONTROL Planung]**-Aktivität).

Dies kann zu einem Szenario führen, bei dem ein zeitplanbasierter Workflow Beginn ausführen kann, auch wenn die vorherige Ausführung desselben Workflows noch nicht abgeschlossen ist, was möglicherweise zu unerwarteten Datenproblemen führt.

Daher müssen Sie beim Entwerfen eines geplanten Arbeitsablaufs, der mehrere Aktivitäten umfasst, sicherstellen, dass der Arbeitsablauf erst nach Fertigstellung neu geplant wird. Dazu müssen Sie Ihren Workflow konfigurieren, um die Ausführung zu verhindern, wenn eine oder mehrere Aufgaben einer vorherigen Ausführung noch ausstehen.

## Workflow konfigurieren

Um zu überprüfen, ob eine oder mehrere Aufgaben aus einer vorherigen Workflow-Ausführung noch ausstehen, müssen Sie eine **[!UICONTROL Abfrage]** und eine **[!UICONTROL Test]**-Aktivität verwenden.

1. hinzufügen Sie eine **[!UICONTROL Abfrage]**-Aktivität nach der **[!UICONTROL Planung]**-Aktivität und konfigurieren Sie sie dann wie folgt:

1. Ändern Sie die Ressource der Aktivität in **[!UICONTROL WorkflowTaskDetail]**, was bedeutet, dass die aktuellen Aufgaben des Workflows Zielgruppe werden.

   ![](assets/scheduled-wkf-resource.png)

1. Konfigurieren Sie die Abfrage wie folgt:

   ![](assets/scheduled-wkf-query.png)

   * Die erste Regel Filter die aktuelle Aufgabe (Abfrage2) sowie die nächste Zeitplan-Aufgabe (Plan2) aus, die zum aktuellen Workflow gehört.

      >[!NOTE]
      >
      >Wenn ein **[!UICONTROL Planung]**-Beginn eine Aktivität , wird sofort eine weitere Zeitplan-Aufgabe hinzugefügt, die zur nächsten geplanten Zeit ausgeführt wird, und der Workflow wird Beginn. Daher ist es wichtig, sowohl die Abfrage als auch die Aufgaben des Zeitplans zu filtern, wenn nach ausstehenden Aufgaben aus einer vorherigen Ausführung gesucht wird.

   * Die zweite Regel bestimmt, ob Aufgaben aus einem vorherigen Workflow-Vorgang weiterhin aktiv sind (ausstehend), was dem Ausführungsstatus 0 entspricht.

1. hinzufügen Sie eine **[!UICONTROL Test]**-Aktivität, um die Anzahl der ausstehenden Aufgaben zu prüfen, die von der **[!UICONTROL Abfrage]**-Aktivität zurückgegeben werden. Konfigurieren Sie dazu zwei ausgehende Transitionen.

   ![](assets/scheduled-wkf-test.png)

   * Bei der ersten Transition wird die Workflow-Ausführung fortgesetzt, wenn keine ausstehenden Aufgaben vorhanden sind,
   * Die zweite Transition bricht die Ausführung des Workflows ab, wenn ausstehende Aufgaben vorliegen.

   ![](assets/scheduled-wkf-workflow.png)

Sie können jetzt den Rest des Workflows nach Bedarf konfigurieren. Wenn die Workflow-Ausführung aufgrund ausstehender Aufgaben abgebrochen wird und der Workflow gemäß Zeitplan erneut ausgeführt wird, können Sie diese Schritte ausführen. Dadurch wird sichergestellt, dass der Workflow nur ausgeführt wird, wenn keine aktiven (ausstehenden) Aufgaben von einer vorherigen Ausführung vorhanden sind.

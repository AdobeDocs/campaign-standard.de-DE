---
title: Start und Ende
description: Die Start- und Ende-Aktivitäten markieren grafisch den Anfangs- bzw. den Endpunkt eines Workflows.
audience: automating
content-type: reference
topic-tags: execution-activities
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 1dfc547f-747d-403e-a5b7-a68f56191c71
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 89%

---

# Start und Ende{#start-and-end}

## Beschreibung {#description}

![](assets/start.png)

![](assets/end.png)

**[!UICONTROL Start]** und **[!UICONTROL Ende]** markieren grafisch den Anfangs- bzw. den Endpunkt eines Workflows.

## Anwendungskontext {#context-of-use}

Die Ausführung eines Workflows beginnt mit Aktivitäten ohne eingehende Transition und endet, wenn keine weiteren Aufgaben mehr in Gang sind. Die Verwendung der **[!UICONTROL Start]**- und **[!UICONTROL Ende]**-Aktivitäten dient insbesondere der besseren Übersicht. beispielsweise bei komplexen Workflows.

Es ist empfehlenswert, einen Workflow mit einer **[!UICONTROL Ende]**-Aktivität anstatt mit der letzten Transition abzuschließen. Damit wird gewährleistet, dass der Workflow ordnungsgemäß beendet wird.

## Konfiguration {#configuration}

1. Ziehen Sie einen **[!UICONTROL Start]** oder ein **[!UICONTROL Ende]** in den Workflow-Arbeitsbereich.
1. Platzieren Sie den **[!UICONTROL Start]** vor anderen Aktivitäten wie beispielsweise Abfragen und das **[!UICONTROL Ende]** im Anschluss an eine Aktivitätenfolge.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in der Schnellaktion angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Konfigurieren Sie bei Bedarf die **Ende**-Aktivität dahingehend, dass alle laufenden Aufgaben angehalten werden, sobald ihre eingehende Transition aktiviert wird. Aktivieren Sie hierzu die entsprechende Option.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Einen weiteren Workflow aktivieren     {#triggering-another-workflow}

Über den Tab **[!UICONTROL Externes Signal]** einer **[!UICONTROL Ende]**-Aktivität können Sie einen weiteren Workflow aktivieren. Lesen Sie diesbezüglich auch den Abschnitt [Externes Signal](../../automating/using/external-signal.md).

## Beispiel {#example}

Unten stehende Abbildung zeigt einen komplexen Workflow mit einem **[!UICONTROL Start]** und mehreren **[!UICONTROL Ende]**-Aktivitäten. Die Option **[!UICONTROL Alle laufenden Aufgaben anhalten]** wurde beim ersten **[!UICONTROL Ende]** aktiviert. Nach Abschluss der Aufgabe wird der gesamte Workflow angehalten. Er hat die gleiche Wirkung wie die ![](assets/stop_darkgrey-24px.png) wurde ausgewählt (siehe [Symbolleiste](../../automating/using/workflow-interface.md#action-bar) Abschnitt).

![](assets/wkf_start_end_example.png)

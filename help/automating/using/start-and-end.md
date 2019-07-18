---
title: Start und Ende
seo-title: Start und Ende
description: Start und Ende
seo-description: Die Start- und Ende-Aktivitäten markieren grafisch den Anfangs- bzw. den Endpunkt eines Workflows.
page-status-flag: nie aktiviert
uuid: 146 b 6337-122 c -453 d -8 ffd -5 c 157 db 29217
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird automatisiert
content-type: Referenz
topic-tags: execution-activities
discoiquuid: a 0 a 8 a 725-8 ede -4626-9798-b 86924 b 58 beb
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Start und Ende{#start-and-end}

## Beschreibung {#description}

![](assets/start.png)

![](assets/end.png)

**[!UICONTROL Start]** und **Ende[!UICONTROL markieren grafisch den Anfangs- bzw. den Endpunkt eines Workflows.]**

## Anwendungskontext {#context-of-use}

Die Ausführung eines Workflows beginnt mit Aktivitäten ohne eingehende Transition und endet, wenn keine weiteren Aufgaben mehr in Gang sind. Die Verwendung der **[!UICONTROL Start]**- und **Ende]-Aktivitäten dient insbesondere der besseren Übersicht.[!UICONTROL ** beispielsweise bei komplexen Workflows.

Es ist empfehlenswert, einen Workflow mit einer **[!UICONTROL Ende]-Aktivität anstatt mit der letzten Transition abzuschließen. Damit wird gewährleistet, dass der Workflow ordnungsgemäß beendet wird.**

## Konfiguration {#configuration}

1. Ziehen Sie einen **[!UICONTROL Start]** oder ein **Ende]in den Workflow-Arbeitsbereich.[!UICONTROL **
1. Platzieren Sie den **[!UICONTROL Start]** vor anderen Aktivitäten wie beispielsweise Abfragen und das **Ende]im Anschluss an eine Aktivitätenfolge.[!UICONTROL **
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der ![-Schaltfläche aus den angezeigten Quick Actions.](assets/edit_darkgrey-24px.png)
1. Konfigurieren Sie bei Bedarf die **Ende**-Aktivität dahingehend, dass alle laufenden Aufgaben angehalten werden, sobald ihre eingehende Transition aktiviert wird. Aktivieren Sie hierzu die entsprechende Option.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Einen weiteren Workflow aktivieren {#triggering-another-workflow}

Über den Tab **[!UICONTROL Externes Signal]** einer **Ende]-Aktivität können Sie einen weiteren Workflow aktivieren.[!UICONTROL ** Lesen Sie diesbezüglich auch den Abschnitt [Externes Signal](../../automating/using/external-signal.md).

## Beispiel {#example}

Unten stehende Abbildung zeigt einen komplexen Workflow mit einem **[!UICONTROL Start]** und mehreren **Ende]-Aktivitäten.[!UICONTROL ** Die Option **[!UICONTROL Alle laufenden Aufgaben anhalten]** wurde beim ersten **Ende]aktiviert.[!UICONTROL ** Dies bedeutet, dass nach Abschluss dieser Aufgabe der gesamte Workflow gestoppt wird. Das gleiche Ergebnis kann mit der Schaltfläche ![](assets/stop_darkgrey-24px.png) erzielt werden (siehe den Abschnitt[Symbolleiste](../../automating/using/workflow-interface.md#action-bar)).

![](assets/wkf_start_end_example.png)


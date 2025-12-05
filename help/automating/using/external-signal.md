---
title: Externes Signal
description: Mit dieser Aktivität wird ein Workflow ausgelöst, wenn in einem anderen Workflow gewisse Bedingungen erfüllt werden.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: signal,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: a4fbd6b5-7cfb-44ad-bf3a-f3aabc122b77
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: ht
source-wordcount: '650'
ht-degree: 100%

---

# Externes Signal{#external-signal}

## Beschreibung {#description}

![](assets/signal.png)

Mit der Aktivität **[!UICONTROL Externes Signal]** wird ein Workflow ausgelöst, wenn in einem anderen Workflow oder einem REST-API-Aufruf gewisse Bedingungen erfüllt werden.

## Anwendungskontext {#context-of-use}

Mit der Aktivität **[!UICONTROL Externes Signal]** können unterschiedliche Prozesse organisiert und geplant werden, die Teil derselben Customer Journey in unterschiedlichen Workflows sind. So kann ein Workflow durch einen anderen aktiviert werden, wodurch komplexere Customer Journeys möglich werden. Dies wiederum erlaubt eine bessere Überwachung der Prozesse und eine raschere Reaktion im Fall von Problemen.

Die Aktivität **[!UICONTROL Externes Signal]** ist die erste Aktivität eines Workflows. Sie kann durch die **[!UICONTROL Ende]**-Aktivität eines anderen Workflows oder einen REST-API-Aufruf ausgelöst werden (mehr dazu finden Sie in der [API-Dokumentation](../../api/using/triggering-a-signal-activity.md)).

Nach dem Aufruf können externe Parameter definiert und in den Workflow-Ereignisvariablen verfügbar gemacht werden. Der Vorgang zum Aufrufen eines Workflows mit externen Parametern wird in [diesem Abschnitt](../../automating/using/calling-a-workflow-with-external-parameters.md) beschrieben.

>[!NOTE]
>
>Die Aktivität kann maximal alle 10 Minuten ausgelöst werden.

Beachten Sie, dass die Aktivität **[!UICONTROL Externes Signal]** von mehreren Ereignissen ausgelöst werden kann. In diesem Fall wird das **[!UICONTROL externe Signal]** aktiviert, sobald einer der Ursprungs-Workflows oder API-Aufrufe ausgeführt wird. Dazu müssen nicht alle Ursprungs-Workflows abgeschlossen sein.

**Verwandte Themen**

* [Anwendungsfall: Aktivität &quot;Externes Signal&quot; und Datenimport](../../automating/using/external-signal-data-import.md)
* [Anwendungsfall: Aufruf eines Workflows über eine Datei mithilfe von Parametern, um eine Zielgruppe zu erstellen](../../automating/using/use-case-calling-workflow.md)

## Konfiguration {#configuration}

Bei der Konfiguration eines externes Signals muss zuerst die Aktivität **[!UICONTROL Externes Signal]** im Ziel-Workflow konfiguriert werden. Danach ist die Aktivität **[!UICONTROL Externes Signal]** dieses Workflows verfügbar, um die **[!UICONTROL Ende]**-Aktivität des Ursprungs-Workflows zu konfigurieren.

1. Ziehen Sie die Aktivität **[!UICONTROL Externes Signal]** in den Ziel-Workflow.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in der Schnellaktion angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Bearbeiten Sie den Titel der Aktivität. Diesen Titel benötigen Sie bei der Konfiguration des Ursprungs-Workflows, der das **[!UICONTROL externe Signal]** auslöst.

   Wenn Sie den Workflow mit Parametern aufrufen möchten, deklarieren Sie diese im Bereich **[!UICONTROL Parameter]**. Weitere Informationen hierzu finden Sie auf [dieser Seite](../../automating/using/declaring-parameters-external-signal.md).

   ![](assets/external_signal_configuration.png)

1. Validieren Sie die Konfiguration Ihrer Aktivität, fügen Sie etwaige andere erforderliche Aktivitäten hinzu und speichern Sie Ihren Workflow.

   >[!NOTE]
   >
   >Wenn Sie den Ziel-Workflow in einem anderen Workflow auslösen möchten, gehen Sie folgendermaßen vor. Weiterführende Informationen zum Auslösen des Ziel-Workflows über einen REST-API-Aufruf finden Sie in der [API-Dokumentation](../../api/using/triggering-a-signal-activity.md).

1. Öffnen Sie den Ursprungs-Workflow und wählen Sie eine **[!UICONTROL Ende]**-Aktivität aus. Wenn keine **[!UICONTROL Ende]**-Aktivität verfügbar ist, fügen Sie eine nach der letzten Aktivität eines Workflow-Zweigs hinzu.

   Manche Aktivitäten haben standardmäßig keine ausgehende Transition. Sie können eine ausgehende Transition im Tab **[!UICONTROL Eigenschaften]** dieser Aktivitäten hinzufügen.

   Beispielsweise können Sie für eine **[!UICONTROL Daten-Update]**-Aktivität im Tab **[!UICONTROL Transitionen]** die Option **[!UICONTROL Ausgehende Transition ohne Population]** auswählen. Mit dieser Option können Sie eine Transition hinzufügen, die keine Daten enthält und somit nicht unnötig Platz in Ihrem System belegt. Sie wird nur verwendet, um die zusätzliche **[!UICONTROL Ende]**-Aktivität zu verbinden, die den Ziel-Workflow auslöst.

   ![](assets/external_signal_empty_transition.png)

1. Wählen Sie im Tab **[!UICONTROL Externes Signal]** der **[!UICONTROL Ende]**-Aktivität den Ziel-Workflow sowie die Aktivität **[!UICONTROL Externes Signal]** aus, um diesen Workflow auszulösen.

   Wenn Sie eine **[!UICONTROL Ende]**-Aktivität festlegen, die einen weiteren Workflow auslöst, wird ihrem Symbol ein zusätzliches Signalsymbol hinzugefügt.

   Wenn Sie den Workflow mit Parametern aufrufen möchten, verwenden Sie den Bereich **[!UICONTROL Parameter und Werte]**. Weitere Informationen hierzu finden Sie auf [dieser Seite](../../automating/using/defining-parameters-calling-workflow.md).

   ![](assets/external_signal_end.png)

1. Speichern Sie den Ursprungs-Workflow.

Sobald die **[!UICONTROL Ende]**-Aktivität des Ursprungs-Workflows oder des REST-API-Aufrufs ausgeführt wird, wird der Ziel-Workflow automatisch durch die Aktivität **[!UICONTROL Externes Signal]** ausgelöst.

>[!NOTE]
>
>Der Ziel-Workflow muss manuell gestartet werden, bevor er ausgelöst werden kann. Beim Start wird die **[!UICONTROL externe Aktivität]** aktiviert, die auf das Signal vom Ursprungs-Workflow wartet.

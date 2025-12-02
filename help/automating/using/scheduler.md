---
title: Planung
description: Die Planungsaktivität ermöglicht die Festlegung des Starts eines Workflows oder einer Aktivität auf einen bestimmten Zeitpunkt.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: schedule,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 39f7b216-b3cd-4aa6-b5df-23e6805076df
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 100%

---

# Planung{#scheduler}

## Beschreibung {#description}

![](assets/scheduler.png)

Die Aktivität **[!UICONTROL Planung]** ermöglicht die Festlegung des Starts eines Workflows oder einer Aktivität auf einen bestimmten Zeitpunkt.

## Anwendungskontext {#context-of-use}

Eine **[!UICONTROL Planung]** entspricht einem programmierten Start, daher sind die gleichen Regeln zu beachten wie für die **[!UICONTROL Start]**-Aktivität. So darf die Planung beispielsweise keine eingehende Transition aufweisen.

Je Workflow-Zweig darf zudem nur eine **[!UICONTROL Planung]** verwendet werden. Außerdem muss eine Zeitzone definiert werden. Dadurch können Sie Ihren Workflow in einer bestimmten Zeitzone starten. Andernfalls wird der Workflow in der in den Eigenschaften des Workflows definierten Zeitzone ausgeführt (siehe [Workflow erstellen](../../automating/using/building-a-workflow.md)).

>[!CAUTION]
>
>Das **[!UICONTROL Ausführungsintervall]** der Aktivität kann nicht weniger als 10 Minuten betragen. Dies bedeutet, dass kein Workflow automatisch öfter als alle zehn Minuten durchgeführt werden kann.

Beim Entwerfen eines geplanten Workflows, der mehrere Aktivitäten umfasst, müssen Sie sicherstellen, dass der Workflow erst dann neu geplant wird, wenn er abgeschlossen ist. Dazu müssen Sie Ihren Workflow so konfigurieren, dass seine Ausführung verhindert wird, wenn eine oder mehrere Aufgaben einer vorherigen Ausführung noch ausstehen. Weitere Informationen hierzu finden Sie auf [dieser Seite](../../automating/using/scheduled-workflows-execution.md).

**Verwandte Themen:**

* [Anwendungsfall: Sendungen zum Erstellungsdatum von Profilen erstellen](../../automating/using/workflow-creation-date-query.md)
* [Anwendungsfall: Jeden Dienstag einen E-Mail-Versand erstellen](../../automating/using/workflow-weekly-offer.md)

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Planung]** in den Workflow.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in der Schnellaktion angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Definieren Sie die **[!UICONTROL Ausführungsfrequenz]**:

   * **[!UICONTROL Einmal]** - der Workflow wird nur einmal ausgeführt.
   * **[!UICONTROL Mehrmals pro Tag]** - der Workflow wird wiederholt zu bestimmten Zeiten am Tag ausgeführt.
   * **[!UICONTROL Täglich]** - der Workflow wird jeden Tag einmal zu einem bestimmten Zeitpunkt ausgeführt.
   * **[!UICONTROL Wöchentlich]** - der Workflow wird wiederholt zu bestimmten Zeiten in der Woche ausgeführt.
   * **[!UICONTROL Monatlich]** - der Workflow wird wiederholt zu bestimmten Zeiten im Monat ausgeführt. Sie können die Monate auswählen, in denen der Workflow ausgeführt werden soll. Sie können für die Ausführung von Workflows auch bestimmte Wochentage des Monats auswählen, z. B. am zweiten Dienstag des Monats.
   * **[!UICONTROL Jährlich]** - der Workflow wird wiederholt zu bestimmten Zeiten im Jahr ausgeführt.

1. Konfigurieren Sie die Ausführungsparameter nach Bedarf. Die verfügbaren Optionen variieren je nach der ausgewählten Ausführungsfrequenz (Ausführungszeit oder -tage, Ausführungsintervall usw.).

   >[!NOTE]
   >
   >Mit dem Feld **[!UICONTROL Ausführungsintervall]**, das für die täglichen und monatlichen Ausführungsfrequenzen verfügbar ist, ermöglicht es, den Rhythmus des Workflow-Starts weiter zu verfeinern. Wenn Sie beispielsweise eine tägliche Ausführungsfrequenz wählen und bei der Ausführungsintervall den Wert **2** (Tage) angeben, wird der Workflow alle zwei Tage gestartet. Dieser Wert kann nicht weniger als 10 Minuten betragen. Wenn das Ausführungsintervall den Standardwert **0** aufweist, wird nur die angegebene Ausführungsfrequenz berücksichtigt und der Workflow wird gemäß der angegebenen Ausführungsfrequenz ausgeführt.

   Beim Festlegen der Ausführungsfrequenz auf **[!UICONTROL Mehrmals pro Tag]** können Sie flexibel zwischen der Ausführung des Workflows zu bestimmten Tageszeiten oder in regelmäßigen Abständen am Tag wählen.

   +++ Erfahren Sie, wie Sie die Ausführungsfrequenz **[!UICONTROL Mehrmals am Tag]** konfigurieren

   * Um den Workflow mehrmals zu bestimmten Tageszeiten auszuführen, aktivieren Sie die Option **[!UICONTROL Bestimmte Zeiten]** und klicken Sie dann auf **[!UICONTROL Element hinzufügen]**, um die gewünschte Ausführungszeit anzugeben. Fügen Sie so viele Ausführungszeiten wie nötig hinzu, um Ihre Anforderungen zu erfüllen.

   * Um den Workflow täglich auszuführen, aktivieren Sie die Option **[!UICONTROL Periodisch]** und konfigurieren Sie dann die Ausführungshäufigkeit:

      1. Geben Sie im Feld **[!UICONTROL Ausführungsintervall (z. B. alle 2h)]** das Intervall an, in dem der Workflow jeweils ausgeführt werden soll (z. B. alle 30 Minuten, alle 2 Stunden).

         >[!NOTE]
         >
         >Diese Option ermöglicht auch eine tägliche, monatliche oder jährliche Ausführungsfrequenz. Beachten Sie, dass der Workflow in diesem Fall nicht mehrmals täglich ausgeführt wird, sondern in Abhängigkeit von der in diesem Feld festgelegten Häufigkeit.
         >
         > Wenn Ihr Workflow nicht mehrere Ausführungen innerhalb eines Tages erfordert, sondern stattdessen täglich, monatlich oder jährlich ausgeführt werden muss, empfiehlt es sich, die Optionen **[!UICONTROL Täglich]**, **[!UICONTROL Monatlich]** bzw. **[!UICONTROL Jährlich]** zu verwenden, die in der Dropdown-Liste **[!UICONTROL Ausführungsfrequenz]** verfügbar sind.

      1. Definieren Sie in den Feldern **[!UICONTROL Startzeit]**/**[!UICONTROL Endzeit]** wann die Workflow-Ausführung beginnen und enden soll.

         Wenn keine Endzeit angegeben ist, wird die Ausführung um Mitternacht (00:00:00 Uhr) beendet und die nächste Ausführung beginnt am nächsten Tag zur angegebenen Startzeit.

      1. Wählen Sie im Feld **[!UICONTROL Startdatum]** das Datum aus, an dem die erste Ausführung beginnen soll.

   Im folgenden Beispiel wird die Aktivität so konfiguriert, dass der Workflow ab dem 1. März alle 2 Stunden zwischen 8 und 17 Uhr ausgeführt wird.

   ![](assets/wkf_scheduler_day.png)

   +++

1. Definieren Sie die Ablaufzeit der Ausführungsplanung:

   * **[!UICONTROL Nie]** - der Workflow wird auf Dauer in den angegebenen Intervallen ausgeführt.
   * **[!UICONTROL Nach einer bestimmten Anzahl an Ausführungen]** - der Workflow wird **X** Mal in den angegebenen Intervallen ausgeführt, wobei X gleich dem im Feld **[!UICONTROL Ausführungsanzahl]** angegebenen Wert ist.
   * **[!UICONTROL Bei Erreichen eines bestimmten Datums]** - der Workflow wird in den angegebenen Intervallen ausgeführt, bis das im Feld „Bis zum“ angegebene Datum erreicht ist.

1. Überprüfen Sie den Zeitplan der nächsten zehn Ausführungen Ihres Workflows, indem Sie **[!UICONTROL Vorschau der nächsten Ausführungen]** auswählen.

1. Wählen Sie im Tab **[!UICONTROL Ausführungsoptionen]** im Feld **[!UICONTROL Zeitzone]** aus, in welcher Zeitzone Ihre Planung ausgeführt werden soll.

   Weiterführende Informationen zum Versand von Nachrichten entsprechend der Zeitzone der Empfänger finden Sie in diesem [Abschnitt](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md) und in diesem [Beispiel](../../automating/using/recurring-push-notifications.md) eines wiederkehrenden Workflows.

1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Beispiel  {#example}

Unten stehende Abbildung zeigt eine Planung für einen Workflow, der für einen unbegrenzten Zeitraum alle zwei Wochen montags um 7 Uhr ausgeführt werden soll.

![](assets/wkf_scheduler_example.png)


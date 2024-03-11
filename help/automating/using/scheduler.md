---
title: Planung
description: Die Planungsaktivität ermöglicht die Festlegung des Starts eines Workflows oder einer Aktivität auf einen bestimmten Zeitpunkt.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: schedule,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 39f7b216-b3cd-4aa6-b5df-23e6805076df
source-git-commit: 7deb1147febfcc8956768715a65416806752c92f
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 61%

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

1. Konfigurieren Sie die Ausführungsparameter entsprechend Ihren Anforderungen. Die verfügbaren Optionen variieren je nach der ausgewählten Ausführungshäufigkeit (Ausführungszeit oder -tage, Ausführungsintervall etc.).

   >[!NOTE]
   >
   >Die **[!UICONTROL Wiederholungshäufigkeit]** in den Ausführungsfrequenzen Täglich und Monatlich können Sie die Startzeiten des Workflows festlegen. Wenn Sie beispielsweise eine tägliche Ausführungsfrequenz wählen und bei der Ausführungsintervall den Wert **2** (Tage) angeben, wird der Workflow alle zwei Tage gestartet. Dieser Wert kann nicht weniger als 10 Minuten betragen. Wenn die Wiederholungshäufigkeit auf **0** (auch Standardwert), wird diese Option nicht berücksichtigt und der Workflow wird entsprechend der angegebenen Ausführungshäufigkeit ausgeführt.

   Beim Festlegen der Ausführungsfrequenz auf **[!UICONTROL Mehrmals pro Tag]** können Sie zwischen der Ausführung des Workflows zu bestimmten Tageszeiten oder in regelmäßigen Abständen am Tag wählen.

+++ Erfahren Sie, wie Sie eine **[!UICONTROL &quot;Mehrmals am Tag&quot;]** Ausführungsfrequenz

   * Um den Workflow mehrmals zu bestimmten Zeiten während des Tages auszuführen, aktivieren Sie **[!UICONTROL Bestimmte Zeiten]** und klicken Sie auf **[!UICONTROL Element hinzufügen]** , um die gewünschte Ausführungszeit anzugeben. Fügen Sie so viele Male wie nötig hinzu, um Ihre Anforderungen zu erfüllen.

   * Um den Workflow täglich auszuführen, aktivieren Sie **[!UICONTROL Periodisch]** und konfigurieren Sie dann die Ausführungsdauer:

      1. Im **[!UICONTROL Wiederholungsverarbeitung nach folgender Häufigkeit (z. B. 2h)]** das Intervall angeben, in dem der Workflow ausgeführt werden soll (z. B. alle 30 Minuten, alle 2 Stunden).

         >[!NOTE]
         >
         >Diese Option ermöglicht auch die tägliche, monatliche oder jährliche Wiederholungshäufigkeit. Beachten Sie, dass der Workflow in diesem Fall nicht mehrmals täglich ausgeführt wird, sondern in Abhängigkeit von der in diesem Feld festgelegten Häufigkeit.
         >
         > Wenn Ihr Workflow nicht mehrere Ausführungen innerhalb eines Tages erfordert, sondern stattdessen täglich, monatlich oder jährlich ausgeführt werden muss, empfiehlt es sich, die **[!UICONTROL Täglich]**, **[!UICONTROL Monatlich]** oder **[!UICONTROL Jährlich]** verfügbaren Optionen in **[!UICONTROL Ausführungsfrequenz]** Dropdown-Liste.

      1. Im **[!UICONTROL Starten]**/**[!UICONTROL Ende]** die Uhrzeit, zu der die Workflow-Ausführung beginnen und enden soll.

         Wenn keine Endzeit angegeben ist, wird die Ausführung um 00 Uhr beendet:00:00 Stunden und die nächste Ausführung beginnt am nächsten Tag zur angegebenen Startzeit.

      1. Im **[!UICONTROL Starten]** Datumsfeld das Datum, an dem die erste Ausführung beginnen soll.

   Im folgenden Beispiel wird die Aktivität so konfiguriert, dass der Workflow ab dem 1. März alle 2 Stunden zwischen 8 und 17 Uhr ausgeführt wird.

   ![](assets/wkf_scheduler_day.png)

+++

1. Definieren Sie den Ablauf der Ausführungsplanung:

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

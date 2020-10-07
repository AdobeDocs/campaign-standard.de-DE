---
title: Warten
description: Die Warten-Aktivität ermöglicht das zeitweise Aussetzen der Ausführung eines Teils eines Workflows.
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: wait,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 100%

---


# Warten{#wait}

## Beschreibung {#description}

![](assets/wait.png)

Die **[!UICONTROL Warten]**-Aktivität ermöglicht das zeitweise Aussetzen der Ausführung eines Teils eines Workflows. Die ausgehende Transition der Aktivität wird nach einer Frist aktiviert, die zwischen einigen Sekunden und mehreren Monaten liegen kann, wodurch die Ausführung der im Anschluss folgenden Aktivitäten ermöglicht wird.

## Anwendungskontext {#context-of-use}

Die **[!UICONTROL Warten]**-Aktivität ermöglicht es, einen bestimmten Zeitraum zwischen der Ausführung zweier Aktivitäten zu definieren. Beispielsweise kann man mehrere Tage nach einer E-Mail-Versandaktivität warten, dann die während dieser Zeitspanne erfolgten Öffnungen und Klicks analysieren, bevor man andere Verarbeitungsschritte (Erinnerungs-E-Mail, Audience-Erstellung etc.) unternimmt.

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Warten]**-Aktivität in den Workflow-Arbeitsbereich.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der im Schnellzugriff angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Bestimmen Sie die **[!UICONTROL Dauer]** der Wartezeit zwischen der Aktivierung der eingehenden und der ausgehenden Transition der Aktivität.

   Sie können die Dauer manuell eingeben oder das dafür vorgesehene Auswahltool des Felds verwenden.

   ![](assets/wait_duration.png)

1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Beispiel {#example}

Das folgende Beispiel erläutert die **[!UICONTROL Warten]**-Aktivität anhand eines typischen Fallbeispiels. Darin wird eine E-Mail mit einer Einladung zu einem Ereignis verschickt. 24 Stunden nach dem Versand werden die E-Mail-Versandlogs analysiert und eine Erinnerungs-E-Mail an die Personen gesendet, die die erste E-Mail erhalten, sich aber nicht angemeldet haben.

Der Workflow stellt sich folgendermaßen dar:

![](assets/wait_example_workflow.png)

* Eine erste **[!UICONTROL Abfrage]** ermöglicht die Bestimmung der Zielgruppe, an die die Einladungs-E-Mail versandt wird.
* Ein **[!UICONTROL E-Mail-Versand]** dient dazu, erstmalig die Einladung an die auf diese Weise ausgewählten Profile zu senden.
* Ein **[!UICONTROL Warten]** von 24 Stunden zwischen dem Versand der Einladung und dem Fortgang des Workflows.
* Eine zweite **[!UICONTROL Abfrage]** ermöglicht die Bestimmung der Zielgruppe mit den Profilen, die die erste Mail erhalten, aber nicht den darin enthaltenen Anmelde-Link angeklickt haben.
* Ein zweiter **[!UICONTROL E-Mail-Versand]** dient dazu, eine Einladungs-Erinnerung an die in der zweiten Abfrage ausgewählten Personen zu senden.


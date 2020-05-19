---
title: Lebenszyklus eines Workflows
description: Weitere Informationen zum Workflow-Lebenszyklus
page-status-flag: never-activated
uuid: ff02b74e-53e8-49c6-bf8e-0c729eaa7d25
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 906c85ea-83b7-4268-86da-cd353f1dc591
context-tags: workflow,overview;workflow,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 3ed78fd610b0d134cd1e60f34c93161cb1e5c50f
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 97%

---


# Lebenszyklus eines Workflows {#life-cycle}

Der Lebenszyklus eines Workflows gestaltet sich in drei Hauptetappen:

* **In Bearbeitung** (grau)

   Hierbei handelt es sich um die Phase der Erstellung (siehe [Workflow erstellen](../../automating/using/building-a-workflow.md#creating-a-workflow)). Ein derartiger Workflow wurde noch nicht vom Server übernommen und kann daher problemlos geändert werden.

* **Gestartet** (blau)

   Nach Abschluss der Erstellungsphase kann der Workflow gestartet werden. Daraufhin wird er vom Server übernommen.

* **Abgeschlossen** (grün)

   Ein Workflow ist abgeschlossen, wenn keine Aufgaben mehr zur Verarbeitung anstehen, oder wenn die Ausführung ausdrücklich angehalten wurde.

Nach dem Start kann ein Workflow zwei weitere Status aufweisen:

* **Warnhinweis** (gelb)

   Der Workflow konnte nicht abgeschlossen werden oder er wurde anhand der Schaltflächen ![](assets/pause_darkgrey-24px.png) bzw. ![](assets/check_pause_darkgrey-24px.png) ausgesetzt.

* **Fehlerhaft** (rot)

   Bei der Ausführung des Workflows ist ein Fehler aufgetreten. Die Ausführung wurde angehalten und ein Eingreifen des Benutzers ist erforderlich. Mithilfe der Schaltfläche ![](assets/printpreview_darkgrey-24px.png) gelangen Sie in das Workflow-Protokoll, dem Sie die Fehlerursache entnehmen können (siehe [Monitoring](#monitoring)).

Die Liste der Marketingaktivitäten ermöglicht die Anzeige aller Workflows inklusive ihrer Status. Weiterführende Informationen dazu finden Sie im Abschnitt [Marketingaktivitäten verwalten](../../start/using/marketing-activities.md#about-marketing-activities).

![](assets/wkf_execution_3.png)

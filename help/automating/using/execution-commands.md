---
title: Ausführungsbefehle
description: Erfahren Sie, wie Sie Workflow-Ausführungsbefehle verwenden.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Beginner
exl-id: fddd88b1-603a-465b-b5e7-624632c0d5cd
TQID: https://experienceleague.adobe.com/jDS-3Rz--h6N17JfbijrtOaj8jVDPDW9HiOoiLwPHSY
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 317
ht-degree: 100%

---

# Ausführungsbefehle {#execution-commands}

Die Schaltflächen der Aktionsleiste dienen dazu, die Workflow-Ausführung zu starten, zu verfolgen und eventuell anzupassen. Siehe den Abschnitt [Aktionsleiste](../../automating/using/workflow-interface.md#action-bar).

![](assets/wkf_execution_2.png)

Folgende Aktionen sind möglich:

**Starten**

Die Schaltfläche ![](assets/play_darkgrey-24px.png) löst die Workflow-Ausführung aus. Der Workflow wechselt in den Status **Gestartet** (blau). Wenn der Workflow zuvor ausgesetzt war, handelt es sich um eine Wiederaufnahme, ansonsten werden die ersten Aktivitäten aktiviert.

>[!NOTE]
>
>Der Start eines Workflows ist ein asynchroner Prozess, d. h. der jeweilige Befehl wird gespeichert und erst dann ausgeführt, wenn ein Server verfügbar ist.

**Aussetzen**

Die Schaltfläche ![](assets/pause_darkgrey-24px.png) setzt die Workflow-Ausführung aus. Der Workflow wechselt in den Status **Warnhinweis** (gelb). Bis zur Wiederaufnahme werden keine neuen Aktivitäten aktiviert, laufende Vorgänge werden jedoch fortgeführt.

**Anhalten**

Die Schaltfläche ![](assets/stop_darkgrey-24px.png) hält die Workflow-Ausführung an. Der Workflow wechselt in den Status **Abgeschlossen** (grün). Importe und SQL-Abfragen werden sofort abgebrochen. Sie können den Workflow nicht an der Stelle fortsetzen, an der er gestoppt wurde.

**Neu starten**

Die Schaltfläche ![](assets/pauseplay_darkgrey-24px.png) hält die Workflow-Ausführung zunächst an und startet sie dann neu. In den meisten Fällen ermöglicht dies einen schnelleren Neustart. Dieser Befehl bietet sich vor allem auch dann an, wenn das Anhalten eines Workflows geraume Zeit in Anspruch nimmt, da die Schaltfläche ![](assets/play_darkgrey-24px.png) erst wieder verfügbar ist, wenn der Workflow tatsächlich angehalten wurde.

Wenn im Workflow Aktivitäten markiert sind, stehen weitere Schaltflächen zur Verfügung:

**Vorgezogene Ausführung**

Die Schaltfläche ![](assets/pending_darkgrey-24px.png) bietet die Möglichkeit, so schnell wie möglich die markierten ausstehenden Aufgaben zu starten.

**Normale Ausführung**

Die Schaltfläche ![](assets/check_darkgrey-24px.png) aktiviert ausgesetzte oder deaktivierte Aktivitäten neu.

**Ausführung ab Markierung aussetzen**

Die Schaltfläche ![](assets/check_pause_darkgrey-24px.png) setzt die Ausführung des Workflows ab der ausgewählten Aktivität aus. Diese und alle im gleichen Zweig folgenden Aktivitäten werden nicht ausgeführt.

**Keine Ausführung**

Die Schaltfläche ![](assets/checkdisable.png) deaktiviert die markierten Aktivitäten.

>[!NOTE]
>
>Auf die der Bearbeitung einer bestimmten Aktivität dienenden Aktionen kann auch über die Schnellaktionen zugegriffen werden, die bei der Markierung einer Aktivität angezeigt werden.

---
title: Und-Verknüpfung
description: Die Und-Verknüpfung ermöglicht es, die Ausführung verschiedener Workflow-Zweige zu synchronisieren.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: andjoin,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: b03c6df3-0104-4900-9468-46824d62e0a6
TQID: https://experienceleague.adobe.com/ydaYzPE9SwLuC-d4nVSaFgLLp-R0Kuceq7hUI89aN1Y
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 100%

---

# Und-Verknüpfung{#and-join}

## Beschreibung {#description}

![](assets/and_join.png)

Die **[!UICONTROL Und-Verknüpfung]** ermöglicht es, die Ausführung verschiedener Workflow-Verzweigungen zu synchronisieren.

## Anwendungskontext {#context-of-use}

Bei einer **[!UICONTROL Und-Verknüpfung]** wird die ausgehende Transition erst aktiviert, wenn alle eingehenden Transitionen aktiviert wurden, d. h. wenn alle vorangehenden Aktivitäten beendet sind.

## Konfiguration {#configuration}

1. Ziehen Sie verschiedene Aktivitäten, z. B. Abfragen, in den Workflow-Arbeitsbereich, um mindestens zwei Verzweigungen zu bilden.
1. Ziehen Sie per Drag-and-Drop eine Aktivität **[!UICONTROL Und-Verknüpfung]** in den Workflow.
1. Schließen Sie die Aktivität an die zwei verschiedenen Zweige an, um diese zu synchronisieren.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in der Schnellaktion angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Wählen Sie die in der ausgehenden Transition beizubehaltende Hauptmenge aus. Wenn keine Hauptmenge angegeben wird, wird die in der ausgehenden Transition übermittelte Population nach dem Zufallsprinzip ermittelt.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Beispiel {#example}

Das folgende Beispiel zeigt die Ausführung der zwei Zweige eines Workflows, bevor diese in der **[!UICONTROL Und-Verknüpfung]** zusammenfließen. Die Dateiextraktion kann erst erfolgen, wenn die drei in die **[!UICONTROL Und-Verknüpfung]** eingehenden Transitionen aktiviert wurden.

![](assets/wkf_and-join_example.png)

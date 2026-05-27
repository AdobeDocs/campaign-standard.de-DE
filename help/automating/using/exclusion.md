---
title: Ausschluss
description: Ein Ausschluss ermöglicht es, bestimmten Kriterien entsprechende Elemente aus einer Population auszuschließen.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: exclusion,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: dccb9545-0d7e-4d40-9a8f-2915b4da99a7
TQID: https://experienceleague.adobe.com/46Q9UK-l1t1bBo9PZiasUxF2nqbLs7luEzqOJt7PU1k
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 256
ht-degree: 100%

---

# Ausschluss{#exclusion}

## Beschreibung {#description}

![](assets/exclusion.png)

Ein **[!UICONTROL Ausschluss]** ermöglicht es, gemäß bestimmten Kriterien entsprechende Elemente aus einer Population auszuschließen.

## Anwendungskontext {#context-of-use}

Die **[!UICONTROL Ausschlussaktivität]** wird insbesondere verwendet, um die Populationen der eingehenden Transitionen weiter einzugrenzen.

Aus den verschiedenen eingehenden Transitionen wird eine Hauptmenge bestimmt. Die Elemente der anderen eingehenden Transitionen werden aus der Hauptmenge ausgeschlossen. Die ausgehende Transition der Ausschlussaktivität enthält nur die Elemente der Hauptmenge, die nicht in einer oder mehreren der anderen eingehenden Transitionen enthalten sind.

## Konfiguration {#configuration}

1. Ziehen Sie einen **[!UICONTROL Ausschluss]** in den Workflow-Arbeitsbereich.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in der Schnellaktion angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Wählen Sie im Feld **[!UICONTROL Hauptmenge]** die eingehende Transition aus, Dies ist die Menge, aus der Elemente ausgeschlossen werden. Die eingehenden Transitionen müssen Populationen gleichen Typs enthalten.

   >[!NOTE]
   >
   >Die eingehenden Transitionen müssen Populationen gleichen Typs enthalten. Wenn beispielsweise die Hauptmenge aus Testprofilen besteht, müssen auch die anderen Transitionen Testprofile enthalten.

1. Bei Bedarf können Sie unter Verwendung von [Transitionen](../../automating/using/activity-properties.md) auf erweiterte Optionen zur Ausgabepopulation zugreifen.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Beispiel {#example}

Unten stehende Abbildung zeigt die Konfiguration zweier Abfrageaktivitäten, die alle Profile der Adobe Campaign-Datenbank abrufen, die zwischen 18 und 27 Jahre alt sind bzw. deren E-Mail-Adresse nicht korrekt angegeben ist. Letztere werden dann von der Hauptmenge ausgeschlossen. Auf diese Weise wird in einem eventuell angeschlossenen Versand vermieden, Nachrichten an ungültige Adressen zu versenden.

![](assets/wkf_exclusion_example.png)

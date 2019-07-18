---
title: Ausschluss
seo-title: Ausschluss
description: Ausschluss
seo-description: Ein Ausschluss ermöglicht es, bestimmten Kriterien entsprechende Elemente aus einer Population auszuschließen.
page-status-flag: nie aktiviert
uuid: b 79 e 7 f 73-37 a 0-4 ec 3-ac 5 a -5449 dc 1 b 1 f 22
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird automatisiert
content-type: Referenz
topic-tags: targeting-activities
discoiquuid: d 5312 fcd -43 ad -428 e-bde 9-90 f 062 e 9358 c
context-tags: Ausschluss, Haupt
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e384a0cef325bc01eb5ea050b0f3d926aea9a88f

---


# Ausschluss{#exclusion}

## Beschreibung {#description}

![](assets/exclusion.png)

Ein **[!UICONTROL Ausschluss]ermöglicht es, bestimmten Kriterien entsprechende Elemente aus einer Population auszuschließen.**

## Anwendungskontext {#context-of-use}

Die **[!UICONTROL Ausschlussaktivität]wird insbesondere verwendet, um die Populationen der eingehenden Transitionen weiter einzugrenzen.**

Aus den verschiedenen eingehenden Transitionen wird eine Hauptmenge bestimmt. Die Elemente der anderen eingehenden Transitionen werden aus der Hauptmenge ausgeschlossen. Die ausgehende Transition der Ausschlussaktivität enthält nur die Elemente der Hauptmenge, die nicht in einer oder mehreren der anderen eingehenden Transitionen enthalten sind.

## Konfiguration {#configuration}

1. Ziehen Sie einen **[!UICONTROL Ausschluss]in den Workflow-Arbeitsbereich.**
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der ![-Schaltfläche aus den angezeigten Quick Actions.](assets/edit_darkgrey-24px.png)
1. Wählen Sie im Feld **[!UICONTROL Hauptmenge]die eingehende Transition aus,** aus der die Elemente der anderen eingehenden Transitionen ausgeschlossen werden sollen. Die eingehenden Transitionen müssen Populationen gleichen Typs enthalten.

   >[!NOTE]
   >
   >Die eingehenden Transitionen müssen Populationen gleichen Typs enthalten. Wenn beispielsweise die Hauptmenge aus Testprofilen besteht, müssen auch die anderen Transitionen Testprofile enthalten.

1. Bei Bedarf können Sie unter Verwendung von [Transitionen](../../automating/using/executing-a-workflow.md#managing-an-activity-s-outbound-transitions) auf erweiterte Optionen zur Ausgabepopulation zugreifen.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Beispiel {#example}

Unten stehende Abbildung zeigt die Konfiguration zweier Abfrageaktivitäten, die alle Profile der Adobe-Campaign-Datenbank abrufen, die zwischen 18 und 27 Jahre alt sind bzw. deren E-Mail-Adresse nicht korrekt angegeben ist. Letztere werden dann von der Hauptmenge ausgeschlossen. Auf diese Weise wird in einem eventuell angeschlossenen Versand vermieden, Nachrichten an ungültige Adressen zu versenden.

![](assets/wkf_exclusion_example.png)


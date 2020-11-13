---
title: Und-Verknüpfung
description: Die Und-Verknüpfung ermöglicht es, die Ausführung verschiedener Workflow-Zweige zu synchronisieren.
page-status-flag: never-activated
uuid: 9b54fd4c-9915-400f-a494-74e52c329b8a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 4b55efa2-652e-4493-bfa7-eaee59b383ca
context-tags: andjoin,main
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '183'
ht-degree: 100%

---


# Und-Verknüpfung{#and-join}

## Beschreibung {#description}

![](assets/and_join.png)

Die **[!UICONTROL Und-Verknüpfung]** ermöglicht es, die Ausführung verschiedener Workflow-Zweige zu synchronisieren.

## Anwendungskontext {#context-of-use}

Bei einer **[!UICONTROL Und-Verknüpfung]** wird die ausgehende Transition erst aktiviert, wenn alle eingehenden Transitionen aktiviert wurden, d. h. wenn alle vorangehenden Aktivitäten beendet sind.

## Konfiguration {#configuration}

1. Ziehen Sie verschiedene Aktivitäten, z. B. Abfragen in den Workflow-Arbeitsbereich, um mindestens zwei Zweige zu bilden.
1. Ziehen Sie eine **[!UICONTROL Und-Verknüpfung]** in den Arbeitsbereich.
1. Schließen Sie die Aktivität an die zwei verschiedenen Zweige an, um diese zu synchronisieren.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der im Schnellzugriff angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Wählen Sie die in der ausgehenden Transition beizubehaltende Hauptmenge aus. Wenn keine Hauptmenge angegeben wird, wird die in der ausgehenden Transition übermittelte Population nach dem Zufallsprinzip ermittelt.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Beispiel {#example}

Das folgende Beispiel zeigt die Ausführung der zwei Zweige eines Workflows, bevor diese in der **[!UICONTROL Und-Verknüpfung]** zusammenfließen. Die Dateiextraktion kann erst erfolgen, wenn die drei in die **[!UICONTROL Und-Verknüpfung]** eingehenden Transitionen aktiviert wurden.

![](assets/wkf_and-join_example.png)


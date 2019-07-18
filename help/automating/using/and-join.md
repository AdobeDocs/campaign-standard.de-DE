---
title: Und-Verknüpfung
seo-title: Und-Verknüpfung
description: Und-Verknüpfung
seo-description: Die Und-Verknüpfung ermöglicht es, die Ausführung verschiedener Workflow-Zweige zu synchronisieren.
page-status-flag: nie aktiviert
uuid: 9 b 54 fd 4 c -9915-400 f-a 494-74 e 52 c 329 b 8 a
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird automatisiert
content-type: Referenz
topic-tags: execution-activities
discoiquuid: 4 b 55 efa 2-652 e -4493-bfa 7-eaee 59 b 383 ca
context-tags: Andobe
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e384a0cef325bc01eb5ea050b0f3d926aea9a88f

---


# Und-Verknüpfung{#and-join}

## Beschreibung {#description}

![](assets/and_join.png)

Die **[!UICONTROL Und-Verknüpfung]ermöglicht es, die Ausführung verschiedener Workflow-Zweige zu synchronisieren.**

## Anwendungskontext {#context-of-use}

Bei einer **[!UICONTROL Und-Verknüpfung]wird die ausgehende Transition erst aktiviert, wenn alle eingehenden Transitionen aktiviert wurden, d. h. wenn alle vorangehenden Aktivitäten beendet sind.**

## Konfiguration {#configuration}

1. Ziehen Sie verschiedene Aktivitäten, z. B. Abfragen in den Workflow-Arbeitsbereich, um mindestens zwei Zweige zu bilden.
1. Ziehen Sie eine **[!UICONTROL Und-Verknüpfung]in den Arbeitsbereich.**
1. Schließen Sie die Aktivität an verschiedenen Zweige an, um diese zu synchronisieren.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der ![-Schaltfläche aus den angezeigten Quick Actions.](assets/edit_darkgrey-24px.png)
1. Wählen Sie die in der ausgehenden Transition beizubehaltende Hauptmenge aus. Wenn keine Hauptmenge angegeben wird, wird die in der ausgehenden Transition übermittelte Population nach dem Zufallsprinzip ermittelt.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Beispiel {#example}

Das folgende Beispiel zeigt die Ausführung der zwei Zweige eines Workflows, bevor diese in der **[!UICONTROL Und-Verknüpfung]zusammenfließen.** Die Dateiextraktion kann erst erfolgen, wenn die drei in die **[!UICONTROL Und-Verknüpfung]eingehenden Transitionen aktiviert wurden.**

![](assets/wkf_and-join_example.png)


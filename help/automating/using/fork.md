---
title: Verzweigung
seo-title: Verzweigung
description: Verzweigung
seo-description: Eine Verzweigung erzeugt ausgehende Transitionen, um mehrere Workflow-Aktivitäten parallel zu starten.
page-status-flag: nie aktiviert
uuid: e 4 eaf 69 b -84 ee -4 f 79-8 b 80-99284697 cd 2 c
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird automatisiert
content-type: Referenz
topic-tags: execution-activities
discoiquuid: f 8 ffe 7 af-e 18 c -4599-8 fd 0-fcd 192565323
context-tags: fork, main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e384a0cef325bc01eb5ea050b0f3d926aea9a88f

---


# Verzweigung{#fork}

## Beschreibung {#description}

![](assets/fork.png)

Eine **[!UICONTROL Verzweigung]erzeugt ausgehende Transitionen, um mehrere Workflow-Aktivitäten parallel zu starten.**

## Anwendungskontext {#context-of-use}

Die **[!UICONTROL Verzweigung]ermöglicht insbesondere die unabhängige Ausführung verschiedener Aktivitäten.**

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Verzweigung]in den Workflow-Arbeitsbereich.**
1. Schließen Sie sie an Aktivitäten wie beispielsweise Abfragen an.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der ![-Schaltfläche aus den angezeigten Quick Actions.](assets/edit_darkgrey-24px.png)
1. Definieren Sie die Anzahl an ausgehenden Transitionen. Dies kann durch die Erstellung neuer bzw. Duplizierung oder Löschung bestehender Transitionen erfolgen. Benennen Sie gegebenenfalls die Transitionen.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Beispiel {#example}

Unten stehende Abbildung zeigt die Schnittmenge aus zwei Abfragen. Gesucht werden alle Profile der Adobe-Campaign-Datenbank, die weiblichen Geschlechts sind und die in Berlin leben. Die Verzweigung ermöglicht es dann, mehrere Aktivitäten parallel zu starten: einerseits eine Audience-Speicherung, um die berechnete Population zwischenzuspeichern, und andererseits eine Segmentierung, die es ermöglicht, den Empfängern in den verschiedenen Segmenten eine E-Mail mit segmentspezifischen Inhalten zu senden. Die erste E-Mail richtet sich an alle Berlinerinnen zwischen 18 und 40 Jahren und die zweite an alle Berlinerinnen über 40 Jahre.

![](assets/wkf_fork_example.png)


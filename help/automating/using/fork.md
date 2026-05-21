---
title: Verzweigung
description: Eine Verzweigung erzeugt ausgehende Transitionen, um mehrere Workflow-Aktivitäten parallel zu starten.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: fork,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 1a5e1ecd-b3f1-4dbe-a816-12d27a3bc0f7
TQID: https://experienceleague.adobe.com/1-9VY3TjBBHAb-7bFikis3Ue5eWy5KXKSR4hXxXDLwc
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 216
ht-degree: 100%

---

# Verzweigung{#fork}

## Beschreibung {#description}

![](assets/fork.png)

Eine **[!UICONTROL Verzweigung]** erzeugt ausgehende Transitionen, um mehrere Workflow-Aktivitäten parallel zu starten.

## Anwendungskontext {#context-of-use}

Die Aktivität **[!UICONTROL Verzweigung]** ermöglicht insbesondere die unabhängige Ausführung verschiedener Aktivitäten innerhalb desselben Workflows.

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Verzweigung]** in den Workflow-Arbeitsbereich.
1. Schließen Sie sie an Aktivitäten wie beispielsweise Abfragen an.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in der Schnellaktion angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Definieren Sie die Anzahl an ausgehenden Transitionen. Dies kann durch die Erstellung neuer bzw. Duplizierung oder Löschung bestehender Transitionen erfolgen. Benennen Sie gegebenenfalls die Transitionen.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Beispiel {#example}

Unten stehende Abbildung zeigt die Schnittmenge aus zwei Abfragen. Gesucht werden alle Profile der Adobe Campaign-Datenbank, die weiblichen Geschlechts sind und die in Berlin leben. Die Verzweigung ermöglicht es dann, mehrere Aktivitäten parallel zu starten: einerseits eine Zielgruppen-Speicherung, um die berechnete Population zwischenzuspeichern, und andererseits eine Segmentierung, die es ermöglicht, den Empfängern in den verschiedenen Segmenten eine E-Mail mit segmentspezifischen Inhalten zu senden. Die erste E-Mail richtet sich an alle Berlinerinnen zwischen 18 und 40 Jahren und die zweite an alle Berlinerinnen über 40 Jahre.

![](assets/wkf_fork_example.png)

---
title: Segmentierung nach Altersklassen
description: Auf dieser Seite finden Sie eine auf der Altersklasse beruhende Segmentierung von Datenbankprofilen. Der Zweck des Workflows besteht im Versand einer E-Mail pro Altersklasse.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: segmentation,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: dab7ef86-4776-48f4-be9a-37de316e0dd9
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 100%

---

# Segmentierung nach Altersklassen {#segmentation-age-groups}

Das folgende Beispiel zeigt eine auf der Altersklasse beruhende Segmentierung von Datenbankprofilen.

Der Zweck des Workflows besteht im Versand einer E-Mail pro Altersklasse. Es wird angenommen, dass dieser Workflow Teil einer Testkampagne sein soll. Kein Segment darf daher mehr als 100 Profile enthalten. Letztere werden nach dem Zufallsprinzip ausgewählt, um begrenzte und dabei repräsentative Audiences zu erhalten.

![](assets/wkf_segment_example_4.png)

Der Workflow ist wie folgt gestaltet:

* Mittels der Aktivität [Planung](../../automating/using/segmentation.md) wird das Ausführungsdatum des Workflows bestimmt.
* Mittels einer [Abfrage](../../automating/using/query.md)-Aktivität werden Profile ausgewählt, in denen Geburtsdatum und E-Mail-Adresse angegeben sind.
* Mittels einer [Segmentierung](../../automating/using/segmentation.md) werden drei auf verschiedene ausgehende Transitionen verteilte Segmente erstellt: 18–25 Jahre, 26–32 Jahre und älter als 32 Jahre. Die Auswahl der in den jeweiligen Segmenten enthaltenen Profile geschieht wie folgt:

  ![](assets/wkf_segment_example_3.png)

   * Filterung der Profile nach Alter je nach für das Segment definierter Altersklasse;

     ![](assets/wkf_segment_new_segment.png)

   * Begrenzung der Segmentgröße durch eine **[!UICONTROL Zufällige Auswahl]**, die mit der Beschränkung **[!UICONTROL Maximale Größe]** von 100 einhergeht.

     ![](assets/wkf_segment_example_1.png)

* Mittels der an die ausgehenden Transitionen angeschlossenen [E-Mail-Versand](../../automating/using/email-delivery.md)-Aktivitäten lässt sich für jedes Segment ein spezifischer Inhalt erstellen.

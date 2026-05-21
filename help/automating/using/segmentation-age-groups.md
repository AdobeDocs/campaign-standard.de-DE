---
title: Segmentierung nach Altersklassen
description: Auf dieser Seite finden Sie eine auf der Altersklasse beruhende Segmentierung von Datenbankprofilen. Der Zweck des Workflows besteht im Versand einer E-Mail pro Altersklasse.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: segmentation,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: dab7ef86-4776-48f4-be9a-37de316e0dd9
TQID: https://experienceleague.adobe.com/LkH1qmElMwEn6JGmUaWj7Qpv7arSvLAZixbfJYTi2NQ
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 100%

---

# Segmentierung nach Altersklassen {#segmentation-age-groups}

Das folgende Beispiel zeigt eine auf der Altersklasse beruhende Segmentierung von Datenbankprofilen.

Der Zweck des Workflows besteht im Versand einer E-Mail pro Altersklasse. Es wird angenommen, dass dieser Workflow Teil einer Testkampagne sein soll. Kein Segment darf daher mehr als 100 Profile enthalten. Letztere werden nach dem Zufallsprinzip ausgewählt, um begrenzte und dabei repräsentative Zielgruppen zu erhalten.

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

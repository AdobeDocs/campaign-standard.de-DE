---
title: Segmentierung nach Altersklassen
description: Auf dieser Seite finden Sie eine auf der Altersklasse beruhende Segmentierung von Datenbankprofilen. Der Zweck des Workflows besteht im Versand einer E-Mail pro Altersklasse.
page-status-flag: never-activated
uuid: 77796f18-cad5-4e7a-9d7b-4ed0dd8943bf
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 0ccd9d02-772e-406b-874a-5381dd0c8709
context-tags: segmentation,main
internal: n
snippet: y
translation-type: ht
source-git-commit: 7ffa48365875883a98904d6b344ac005afe26e18
workflow-type: ht
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

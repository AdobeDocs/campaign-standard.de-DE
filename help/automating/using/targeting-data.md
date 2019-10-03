---
title: Zielgruppendaten
seo-title: Zielgruppendaten
description: Zielgruppendaten
seo-description: Hier erhalten Sie Informationen darüber, wie Sie die gewünschten Daten abfragen und auswählen können.
page-status-flag: never-activated
uuid: 0645d6e5-6a7e-4917-874a-7e7725f06abd
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 382ea74e-1662-4c64-96d7-676040586913
internal: n
snippet: y
translation-type: ht
source-git-commit: bb65cbf808a95e8b42b2a682b7c0a9cc6225d920

---


# Zielgruppendaten{#targeting-data}

## Datenauswahl {#selecting-data}

Sie können Daten mit den folgenden Aktivitäten auswählen:

* Eine **[!UICONTROL Abfrage]** dient der Filterung und Extraktion einer Population, die sich aus Elementen der Adobe-Campaign-Datenbank zusammensetzt. Siehe den Abschnitt [Abfrage](../../automating/using/query.md).
* Eine **[!UICONTROL Inkrementelle Abfrage]** dient der Filterung und Extraktion einer Population, die sich aus Elementen der Adobe-Campaign-Datenbank zusammensetzt. Bei jeder neuen Ausführung dieser Aktivität werden die Ergebnisse der vorangehenden Ausführungen ausgeschlossen. Dadurch lassen sich ausschließlich neue Elemente abrufen. Siehe den Abschnitt [Inkrementelle Abfrage](../../automating/using/incremental-query.md).
* Die Aktivität **[!UICONTROL Audience lesen]** ermöglicht es Ihnen, eine vorhandene Audience abzurufen und sie durch zusätzliche Filterbedingungen einzuengen. Siehe den Abschnitt [Audience lesen](../../automating/using/read-audience.md).

## Daten segmentieren {#segmenting-data}

Adobe Campaign bietet die Möglichkeit, eingehende Daten zusammenzufassen oder aber zu segmentieren. Sie können also verschiedene Populationen vereinen, einen Teil daraus ausschließen oder nur die in jeder der Populationen enthaltenen Datensätze verwenden.

* Eine **[!UICONTROL Vereinigung]** dient der Zusammenfassung der Ergebnisse mehrerer Aktivitäten in einer Zielgruppe. Siehe den Abschnitt [Vereinigung](../../automating/using/union.md).
* Eine **[!UICONTROL Schnittmenge]** dient der Extraktion der gemeinsamen Population aus den eingehenden Aktivitäten. Siehe den Abschnitt [Schnittmenge](../../automating/using/intersection.md).
* Ein **[!UICONTROL Ausschluss]** ermöglicht es, bestimmten Kriterien entsprechende Elemente aus einer Population auszuschließen. Siehe den Abschnitt [Ausschluss](../../automating/using/exclusion.md).
* Mit der **[!UICONTROL Segmentierung]** lassen sich von einer durch frühere Aktivitäten berechneten Population ausgehend ein oder mehrere Segment(e) erstellen. Diese können bei Abschluss der Aktivität in einer einzigen oder verschiedenen Transition(en) verarbeitet werden. Siehe den Abschnitt [Segmentierung](../../automating/using/segmentation.md).

## Daten anreichern {#enriching-data}

Identifizierte und abgerufene Daten können angereichert, zusammengefasst und bearbeitet werden, um die Zielgruppenerstellung zu optimieren. Sie können den Zielgruppenbestimmungsvorgang durch Einschluss von nicht im Datamart modellisierten Daten vereinfachen und optimieren.

Mithilfe des Tabs **[!UICONTROL Zusatzdaten]** der Aktivitäten **[!UICONTROL Abfrage]** und **[!UICONTROL Inkrementelle Abfrage]** lassen sich die aus der Abfrage hervorgehenden Daten anreichern und an die Folgeaktivitäten des Workflows übermitteln, in denen sie weiterverwendet werden können. Insbesondere die folgenden Elemente lassen sich hinzufügen:

* einfache Daten
* Aggregate
* Kollektionen

**Verwandte Themen**

* [Anwendungsfall: Erstellung einer einmaligen E-Mail-Versendung pro Woche](../../automating/using/workflow-weekly-offer.md)
* [Anwendungsfall: Erstellung einer Standort-segmentierten Versendung](../../automating/using/workflow-segmentation-location.md)
* [Anwendungsfall: Erstellen von Versendungen mit einem Komplement](../../automating/using/workflow-created-query-with-complement.md)
* [Anwendungsfall: Retargeting-Workflow für eine erneute Versendung an Nicht-Öffner](../../automating/using/workflow-cross-channel-retargeting.md)

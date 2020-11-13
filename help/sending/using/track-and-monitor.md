---
title: Tracken und überwachen von Nachrichten
seo-title: Tracken und überwachen von Nachrichten
page-status-flag: never-activated
uuid: a540efc7-105d-4c7f-a2ee-ade4d22b3445
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
discoiquuid: 0cbc4e92-482f-4dac-a1fb-b738e7127938
index: y
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '414'
ht-degree: 100%

---


# Tracken und überwachen {#track-and-monitor}

Sie haben auf die Senden-Schaltfläche geklickt? Lassen Sie uns sehen, was dann passiert. Nach dem Versand der Nachrichten ermöglicht es Ihnen Adobe Campaign die gesendeten Nachrichten zu verfolgen und festzustellen, wie Ihre Empfänger darauf reagieren. Dadurch können Sie den zukünftigen Versand verbessern und Ihre nächsten Kampagnen optimieren.

## Sendungen überwachen {#monitoring-deliveries}

Um Ihre Kampagnen steuern zu können, müssen Sie zunächst sichergehen, dass Ihre Nachricht bei Ihren Empfängern tatsächlich angekommen ist.

**Tipps**

* In den Versand-Logs können Sie den Status der Nachrichten feststellen.

* Um Erfolge und Fehlschläge beim Versand zu verfolgen, ist Adobe Campaign mit einem E-Mail-Warnsystem ausgestattet, über das Benutzer Benachrichtigungen zu wichtigen Systemaktivitäten erhalten.

* Im Nachrichten-Dashboard können Sie für diese Benachrichtigung mehrere Berichte aufrufen.

Weiterführende Informationen dazu finden Sie unter [Sendungen beobachten](../../sending/using/monitoring-a-delivery.md).

## Tracking {#tracking-deliveries}

Um das Verhalten Ihrer Empfängerprofile besser kennenzulernen, können Sie ihre Reaktion auf einen Versand verfolgen: Empfang, Öffnung, Klicks auf Links, Abmeldungen usw. Siehe die Registerkarte **Trackinglogs** des Versands.

**Tipp**: Das Nachrichten-Tracking ist standardmäßig aktiviert. Um URLs zu konfigurieren, wählen Sie im unteren Bereich des Versandassistenten die Option „URLs anzeigen“ aus. Sie können für jede URL der Nachricht festlegen, ob Sie Tracking aktivieren möchten.

Weitere Informationen hierzu finden Sie im Abschnitt [Tracking-Nachrichten](../../sending/using/tracking-messages.md) und in der Beschreibung der [Tracking-Indikatoren](../../reporting/using/tracking-indicators.md).

## Dynamische Berichte {#dyn-reports}

Dynamische Berichte ermöglichen vollständig anpassbare und in Echtzeit aktualisierte Berichte zur Überwachung Ihrer Kampagnen. Mit Dimensionen, Metriken und Visualisierungen können Sie die Wirkung und den Erfolg Ihrer Kampagnen auf Empfänger messen.

**Tipp**: Vordefinierte Berichte sind verfügbar, mit denen Sie Ihre Kampagnen überwachen können. Diese Berichte können auch angepasst werden, indem Sie einfach Metriken oder Dimensionen per Drag-and-Drop in den Bericht ziehen.

Weitere Informationen hierzu finden Sie im [Reporting-Handbuch](../../reporting/using/about-dynamic-reports.md).

## Klicks

Der Klicks-Bericht stellt den Nachrichteninhalt (HTML und/oder Text) mit dem Prozentsatz der Klicks auf jeden Link dar. Durch die Darstellung des Prozentsatzes der Klicks auf jedem dynamischen Inhalt können Sie messen, welcher Inhalt bei den Empfängern am besten ankommt.

Weiterführende Informationen dazu finden Sie auf der Seite [Klicks-Bericht](../../reporting/using/hot-clicks.md).

## Tipps zur Versandleistung {#performance-tips}

* Bewahren Sie auf der Instanz keine fehlgeschlagenen Sendungen auf, da dadurch temporäre Tabellen gespeichert werden, was wiederum die Leistung beeinträchtigt.

* Entfernen Sie nicht mehr benötigte Sendungen und inaktive Empfänger aus der Datenbank, um eine hohe Qualität der Adressen zu gewährleisten.

* Planen Sie nicht die gleichzeitige Durchführung umfangreicher Sendungen. Beachten Sie, dass es 5 bis 10 Minuten dauern kann, bis die Last gleichmäßig über das System verteilt wurde.

**Verwandte Themen:**

* [Warnungen bei Zustellproblemen erhalten](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Berichte](../../reporting/using/about-dynamic-reports.md)

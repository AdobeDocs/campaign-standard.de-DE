---
title: Nachrichten tracken und überwachen
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: true
description: Erfahren Sie, wie Sie mit Adobe Campaign im Anschluss an den Nachrichtenversand die gesendeten Nachrichten tracken und feststellen können, wie die Empfänger auf sie reagieren.
feature: Deliverability
role: User
level: Intermediate
exl-id: dd3bd672-fb9d-4e82-bdf3-d319f372baaa
TQID: https://experienceleague.adobe.com/500SaHxJS30x-b1g3zGpx9TB7xVmfr1tzJnFv814Q-E
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2:
  - id: a075b2c1-7748-4328-b7f6-343aa314616a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 435
ht-degree: 100%

---

# Verfolgen und überwachen {#track-and-monitor}

Sie haben auf die Schaltfläche „Senden“ geklickt? Sehen wir uns an, was passiert. Nach dem Versand der Nachrichten ermöglicht es Ihnen Adobe Campaign die gesendeten Nachrichten zu verfolgen und festzustellen, wie Ihre Empfänger darauf reagieren. Dadurch können Sie den zukünftigen Versand verbessern und Ihre nächsten Kampagnen optimieren.

## Überwachen von Sendungen {#monitoring-deliveries}

Um Ihre Kampagnen steuern zu können, müssen Sie zunächst sichergehen, dass Ihre Nachricht bei Ihren Empfängern tatsächlich angekommen ist.

**Tipps**

* In den Versand-Logs können Sie den Status der Nachrichten feststellen.

* Um Erfolge und Fehlschläge beim Versand zu verfolgen, ist Adobe Campaign mit einem E-Mail-Warnsystem ausgestattet, über das Benutzer Benachrichtigungen zu wichtigen Systemaktivitäten erhalten.

* Im Nachrichten-Dashboard können Sie für diese Benachrichtigung mehrere Berichte aufrufen.

Weiterführende Informationen dazu finden Sie unter [Sendungen beobachten](../../sending/using/monitoring-a-delivery.md).

## Tracking {#tracking-deliveries}

Um das Verhalten Ihrer Empfängerprofile besser kennenzulernen, können Sie ihre Reaktion auf einen Versand verfolgen: Empfang, Öffnung, Klicks auf Links, Abmeldungen. Weitere Informationen finden Sie auf der Registerkarte **Trackinglogs** des Versands.

**Tipp:** Das Nachrichten-Tracking ist standardmäßig aktiviert. Um URLs zu konfigurieren, wählen Sie im unteren Bereich des Versand-Assistenten die Option „URLs anzeigen“ aus. Sie können für jede URL der Nachricht festlegen, ob Sie die Nachverfolgung aktivieren möchten.

Weitere Informationen hierzu finden Sie im Abschnitt [Tracking-Nachrichten](../../sending/using/tracking-messages.md) und in der Beschreibung der [Tracking-Indikatoren](../../reporting/using/tracking-indicators.md).

## Dynamische Berichte {#dyn-reports}

Dynamische Berichte ermöglichen vollständig anpassbare und in Echtzeit aktualisierte Berichte zur Überwachung Ihrer Kampagnen. Mit Dimensionen, Metriken und Visualisierungen können Sie die Wirkung und den Erfolg Ihrer Kampagnen auf Empfänger messen.

**Tipp**: Native Berichte sind verfügbar, mit denen Sie Ihre Kampagnen überwachen können. Diese Berichte können auch angepasst werden, indem Sie einfach Metriken oder Dimensionen per Drag-and-Drop in den Bericht ziehen.

Weitere Informationen hierzu finden Sie im [Reporting-Handbuch](../../reporting/using/about-dynamic-reports.md).

## Klicks

Der Klicks-Bericht stellt den Nachrichteninhalt (HTML und/oder Text) mit dem Prozentsatz der Klicks auf jeden Link dar. Durch die Darstellung des Prozentsatzes der Klicks auf jedem dynamischen Inhalt können Sie messen, welcher Inhalt bei den Empfängern am besten ankommt.

Weiterführende Informationen dazu finden Sie auf der Seite [Klicks-Bericht](../../reporting/using/hot-clicks.md).

## Tipps zur Versand-Performance {#performance-tips}

* Bewahren Sie auf der Instanz keine fehlgeschlagenen Sendungen auf, da dadurch temporäre Tabellen gespeichert werden, was wiederum die Performance beeinträchtigt.

* Entfernen Sie nicht mehr benötigte Sendungen und inaktive Empfänger aus der Datenbank, um eine hohe Qualität der Adressen zu gewährleisten.

* Versuchen Sie nicht, große Sendungen gleichzeitig zu terminieren. Beachten Sie, dass es 5 bis 10 Minuten dauern kann, bis die Last gleichmäßig über das System verteilt wurde.

**Verwandte Themen:**

* [Warnungen bei Zustellproblemen erhalten](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Berichte](../../reporting/using/about-dynamic-reports.md)

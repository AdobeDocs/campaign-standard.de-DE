---
title: Tracken und Überwachen von Nachrichten
seo-title: Tracken und Überwachen von Nachrichten
page-status-flag: never-activated
uuid: a540efc7-105d-4c7f-a2ee-ade4d22b3445
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
discoiquuid: 0cbc4e92-482f-4dac-a1fb-b738e7127938
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 469d2a8b3f8026087929583affd2c294e2a954bb
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 64%

---


# Tracken und Überwachen {#track-and-monitor}

Sie haben auf die Senden-Schaltfläche geklickt? Lassen Sie uns sehen, was dann passiert. Nach dem Versand der Nachrichten ermöglicht es Ihnen Adobe Campaign die gesendeten Nachrichten zu verfolgen und festzustellen, wie Ihre Empfänger darauf reagieren. Dadurch können Sie den zukünftigen Versand verbessern und Ihre nächsten Kampagnen optimieren.

## Sendungen überwachen {#monitoring-deliveries}

Um Ihre Kampagnen steuern zu können, müssen Sie zunächst sichergehen, dass Ihre Nachricht bei Ihren Empfängern tatsächlich angekommen ist.

**Tipps**

* In den Versand-Logs können Sie den Status der Nachrichten feststellen.

* Um Erfolge und Fehlschläge beim Versand zu verfolgen, ist Adobe Campaign mit einem E-Mail-Warnsystem ausgestattet, über das Benutzer Benachrichtigungen zu wichtigen Systemaktivitäten erhalten.

* Im Nachrichten-Dashboard können Sie für diese Nachricht mehrere Berichte aufrufen.

Weiterführende Informationen dazu finden Sie unter [Sendungen beobachten](../../sending/using/monitoring-a-delivery.md).

## Tracking {#tracking-deliveries}

Um das Verhalten Ihrer zielgerichteten Profil besser zu kennen, können Sie nachverfolgen, wie sie auf einen Versand reagieren: Empfang, Öffnen, Klicks auf Links, Abmeldungen usw. Lesen Sie die Registerkarte &quot; **Trackinglogs** &quot;des Versands.

**Tipp**: Das Nachrichten-Tracking ist standardmäßig aktiviert. Um URLs zu konfigurieren, wählen Sie im unteren Bereich des Versandassistenten die Option „URLs anzeigen“ aus. Sie können für jede URL der Nachricht festlegen, ob Sie Tracking aktivieren möchten.

For more on this, refer to the [Tracking messages](../../sending/using/tracking-messages.md) section and the [Tracking indicators](../../reporting/using/tracking-indicators.md) description.

## Dynamische Berichte {#dyn-reports}

Dynamische Berichte ermöglichen vollständig anpassbare und in Echtzeit aktualisierte Berichte zur Überwachung Ihrer Kampagnen. Mit Dimensionen, Metriken und Visualisierungen können Sie die Wirkung und den Erfolg Ihrer Kampagnen auf Empfänger messen.

**Tipp** : Integrierte Berichte stehen Ihnen zur Überwachung Ihrer Kampagnen zur Verfügung. Sie können diese Berichte jedoch auch anpassen, indem Sie Metriken oder Dimensionen per Drag &amp; Drop in Ihren Bericht ziehen.

Weitere Informationen hierzu finden Sie im [Reporting-Handbuch](../../reporting/using/about-dynamic-reports.md).

## Klicks

Der Bericht &quot;Hotclicks&quot;zeigt den Inhalt der Nachricht (HTML und/oder Text) mit dem Prozentsatz der Klicks auf die einzelnen Links an. Indem Sie den Prozentsatz der Klicks auf jeden dynamischen Inhalt anzeigen, können Sie messen, welcher Inhalt den Empfängern am meisten gefällt.

For more on this, refer to the [Hot click report](../../reporting/using/hot-clicks.md).

## Tipps zur Versand-Performance {#performance-tips}

* Bewahren Sie auf der Instanz keine fehlgeschlagenen Sendungen auf, da dadurch temporäre Tabellen gespeichert werden, was wiederum die Leistung beeinträchtigt.

* Entfernen Sie nicht mehr benötigte Sendungen und inaktive Empfänger aus der Datenbank, um eine hohe Qualität der Adressen zu gewährleisten.

* Planen Sie nicht die gleichzeitige Durchführung umfangreicher Sendungen. Beachten Sie, dass es 5 bis 10 Minuten dauern kann, bis die Last gleichmäßig über das System verteilt wurde.

**Verwandte Themen:**

* [Warnungen bei Zustellproblemen erhalten](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Berichte](../../reporting/using/about-dynamic-reports.md)

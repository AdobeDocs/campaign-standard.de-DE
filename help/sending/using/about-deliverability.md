---
title: Über die Zustellbarkeit in Adobe Campaign Standard
description: Erfahren Sie mehr über Begriffe und Best Practices im Zusammenhang mit der Zustellbarkeit sowie über die Werkzeuge zur Versandoptimierung in Adobe Campaign Standard.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: Deliverability
role: User
level: Intermediate
exl-id: 5e523519-7192-4031-9d96-559af23074d9
source-git-commit: ee7539914aba9df9e7d46144e437c477a7e52168
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 100%

---

# Was ist Zustellbarkeit{#about-deliverability}

Die Zustellbarkeit misst, wie viele Ihrer Nachrichten erfolgreich den Posteingang Ihrer Empfänger erreichen und nicht als unzustellbar zurückgesendet bzw. als Spam gekennzeichnet werden. [Hier erfahren Sie, warum Lieferbarkeit wichtig ist](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/deliverability-strategy-and-definition.html?lang=de#why-deliverability-matters).

Genauer gesagt bezieht sich die E-Mail-Zustellbarkeit auf die Menge der Merkmale, die die Fähigkeit einer Nachricht bestimmen, über eine persönliche E-Mail-Adresse innerhalb kurzer Zeit und mit der erwarteten Qualität in Bezug auf Inhalt und Format ihr Ziel zu erreichen. <!--These characteristics fall into four main categories: data quality, message and content, sending infrastructure, and reputation. Together, they form the foundation of a successful email deliverability program.-->

Einen tieferen Einblick in das Thema der Zustellbarkeit und weitere Informationen zu den wichtigsten Bedingungen, Konzepten und Ansätzen zur Zustellbarkeit erhalten Sie im [Adobe-Handbuch mit den Best Practices zur Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=de).

## Verbessern der Zustellbarkeit {#deliverability-key-points}

Probleme mit der Zustellbarkeit hängen in der Regel mit Maßnahmen zum Schutz vor Spam zusammen, die von Internet-Anbietern und Mailserver-Administratoren implementiert werden.

* Allgemeine Empfehlungen zum Entwerfen erfolgreicher E-Mail-Marketing-Kampagnen finden Sie unter [Strategie und Definition der Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/deliverability-strategy-and-definition.html?lang=de).

* Für spezifischere Empfehlungen zur Optimierung der Zustellbarkeit Ihrer Adobe Campaign-E-Mails empfehlen wir die Verwendung der in diesem Abschnitt aufgeführten Best Practices.

>[!NOTE]
>
>Da Internet-Anbieter gezwungen sind, ständig neue, ausgereifte Filtertechniken zu entwickeln, um ihre Kunden vor Spammern zu schützen, ändern sich die für die Zustellbarkeit von E-Mails geltenden Kriterien und Regeln sehr oft. Konsultieren Sie deshalb das [Adobe-Handbuch mit Best Practices zur Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=de), das regelmäßig aktualisiert wird.

### Zustellrate

Die Zustellrate ist der Anteil der Nachrichten, die die Postfächer der Empfänger im Vergleich zur gesamten Anzahl der versendeten Nachrichten erreicht haben. Um die Zustellbarkeit zu verbessern, können Sie versuchen, diese Rate zu erhöhen.

Bei Adobe Campaign hängt die Zustellrate von zahlreichen Faktoren ab, insbesondere von:

* Korrekte Konfiguration der Instanzen: Wenden Sie sich zwecks Hilfe an Ihren Adobe-Support-Mitarbeiter.
* Legitime Netzwerkkonfiguration: siehe [diesen Abschnitt](../../sending/using/optimize-delivery.md#network-config) und [Einrichtung von Domains und Strategie](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html?lang=de#domain-setup-and-strategy).
* Reputation Ihrer IP-Adresse: siehe [IP-Strategie](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html?lang=de#ip-strategy).
* Qualität der Zieladressen: siehe [Quarantäne-Management](../../sending/using/optimize-delivery.md#quarantine-management).
* Ein niedriger Anteil von [Beschwerden](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html?lang=de) und [Hardbounces](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/bounces.html?lang=de#hard-bounces).
* Inhalt Ihrer Nachricht: Siehe [Kontrollieren von E-Mail-Inhalten](../../sending/using/control-email-content.md).
* Nachrichtenauthentifizierung (SPF, DKIM, DMARC): siehe [diesen Abschnitt](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html?lang=de#authentication).
* Reputation des Absenders: Informationen darüber, wie die wichtigsten Internet-Anbieter die Reputation eines Absenders bewerten, finden Sie in [diesem Abschnitt](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/internet-service-provider-specifics/overview.html?lang=de).

## Campaign-Tools für die Zustellbarkeit {#deliverability-tools}

Adobe Campaign bietet eine Reihe von Tools zur Verfolgung und Verbesserung der Zustellbarkeitsleistung Ihrer Plattform. Auf dieser Seite finden Sie auch die wichtigsten Grundsätze, die Sie beachten sollten, um bei der Verwendung von Campaign die Zustellbarkeit zu optimieren.

### Sorgfältiges Erstellen Ihrer Nachricht

Befolgen Sie beim Konfigurieren, Entwerfen und Testen Ihrer Nachricht die in den folgenden Abschnitten aufgeführten Best Practices. Die Nutzung aller von Adobe Campaign bereitgestellten Funktionen hilft Ihnen, die Zustellbarkeit zu verbessern.

* [Best Practices beim Versand](../../sending/using/delivery-best-practices.md)
* [Kontrollieren von E-Mail-Inhalten](../../sending/using/control-email-content.md)
* [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md)
* [Testversand durchführen](../../sending/using/sending-proofs.md)

### Einverständnis durch doppelten Opt-in überprüfen {#double-opt-in}

Um das Senden von Nachrichten an ungültige Adressen zu vermeiden, unsachgemäße Kommunikation zu minimieren und die Reputation des Absenders zu verbessern, empfiehlt Adobe die Implementierung eines Mechanismus zum doppelten Opt-in. Dadurch können Sie sicherstellen, dass sich Ihre Empfänger absichtlich angemeldet haben.

Weiterführende Informationen dazu finden Sie unter [Funktionsweise des Opt-in- und Opt-out-Verfahrens in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

Weitere Informationen zu Best Practices bei der Erfassung von Kundendaten finden Sie im [Adobe-Handbuch mit Best Practices zur Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/first-impressions/address-collection-and-list-growth.html?lang=de#data-quality-and-hygiene).

### Quarantäne-Management nutzen

Adobe Campaign verwaltet eine Liste, in der Spam-Beschwerden, Hardbounces und Softbounces, die immer wieder auftreten, erfasst werden.

Zum Schutz Ihrer Zustellbarkeit werden die Empfänger, deren Adressen auf dieser Liste stehen, standardmäßig von allen zukünftigen Sendungen ausgeschlossen, da das Senden an diese Kontakte Ihre Reputation beschädigen könnte.

Teilweise werden E-Mails von Providern automatisch als Spam eingestuft, wenn die Anzahl ungültiger Adressen zu hoch ist. Durch die Quarantäne können Sie also vermeiden, von diesen Providern auf eine Blockierungsliste gesetzt zu werden.

Weiterführende Informationen hierzu finden Sie in den folgenden Abschnitten:

* [Ursachen von fehlgeschlagenen Sendungen](../../sending/using/understanding-delivery-failures.md)
* [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md)
* [Quarantäne vs. Blockierungsliste](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist)

### Verwenden von Tools zum Monitoring und Reporting

Verwenden Sie die von Adobe Campaign bereitgestellten Funktionen zur Überwachung der Zustellbarkeit.

Mit Adobe Campaign können Sie anhand einer Reihe von integrierten Echtzeitindikatoren überprüfen, wie gut Ihre Sendungen laufen. <!--For example, you can check the number of messages that are successfully executed, sent and delivered. You can also verify the number of messages that have been opened and the number of messages/links that have been clicked.-->Sie können auch vollständig anpassbare Echtzeitberichte erstellen, um einen besseren Einblick in Ihre Sendungen zu erhalten.

Weiterführende Informationen hierzu finden Sie in den folgenden Abschnitten:

* [Überwachen der Zustellbarkeit](../../sending/using/monitor-deliverability.md)

   <!--[Monitoring a delivery](../../sending/using/monitoring-a-delivery.md)-->
* [Warnungen bei Zustellproblemen erhalten](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Dynamische Berichte](../../reporting/using/about-dynamic-reports.md)

<!--## General recommendations

NOT SURE TO KEEP

Here are a few additional recommendations when it comes to deliverability.

### Send to valid addresses {#valid-addresses}

Spammers often use address generators based on lists of frequent names and first names; in addition, they rarely process technical notifications sent back by mail servers. A high rate of invalid addresses is often interpreted as a sign of spam.

Double opt-in mechanisms and effective handling of technical bounce messages make it possible to avoid this.

### Reduce complaint rate {#reduce-complaint-rate}

ISPs usually have a prominent means of reporting a received message as spam. This makes it possible to identify unreliable sources. By rapidly honoring opt-out requests, making regular use of a given list, verifying consent through a double opt-in system, and implementing feedback loops, you can reduce complaint rates.

<!--Sending to honeypot addresses {#honeypot-addresses}
ISPs and other organizations (refer to https://www.projecthoneypot.org/) make use of mailboxes that do not correspond to physical persons but are created simply to trick spammers. These so-called "honey pot" addresses are published on the Web in order to be collected by spambots and thus catch illegitimate senders. The use of a double opt-in mechanism precludes this sort of address being added to a list. When using a third-party list, you must be sure of the methods employed by its maintainer.-->

<!--## Sending on a regular basis {#regular-deliveries}

Spammers make programmed deliveries to maintain their reputation over time. They sometimes need to adapt their marketing plan to meet the best practices imposed by the ISPs and so, after a peak in reputation (ramp-up), they configure regular deliveries.-->

---
solution: Campaign Standard
product: campaign
title: Über die Zustellbarkeit in Adobe Campaign Standard
description: Erfahren Sie mehr über Begriffe und Best Practices im Zusammenhang mit der Zustellbarkeit sowie über die Werkzeuge zur Versandoptimierung in Adobe Campaign Standard.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: Zustellbarkeit
role: Business Practitioner
level: Fortgeschritten
translation-type: tm+mt
source-git-commit: fb9a6218bb754f803affde1fdf6c6fc01570126f
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 15%

---


# Was ist Zustellbarkeit{#about-deliverability}

Die Zustellbarkeit misst, wie viele Ihrer Nachrichten erfolgreich an die Empfängerpostfächer zugestellt und nicht als unzustellbar zurückgesendet bzw. als Spam gekennzeichnet werden. [Erfahren Sie, warum Lieferbarkeit wichtig ist](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/deliverability-strategy-and-definition.html#why-deliverability-matters).

Genauer gesagt bezieht sich die E-Mail-Zustellbarkeit auf den Satz von Merkmalen, die bestimmen, ob eine Nachricht ihr Ziel erreichen kann, über eine persönliche E-Mail-Adresse, innerhalb kurzer Zeit und mit der erwarteten Qualität in Bezug auf Inhalt und Format. <!--These characteristics fall into four main categories: data quality, message and content, sending infrastructure, and reputation. Together, they form the foundation of a successful email deliverability program.-->

Einen tieferen Einstieg in die Lieferbarkeit und weitere Informationen zu den wichtigsten Lieferbedingungen, -konzepten und -ansätzen finden Sie im Leitfaden [Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html) zur Lieferbarkeit von Adoben.

## Verbesserung der Zustellbarkeit {#deliverability-key-points}

Probleme mit der Lieferbarkeit sind in der Regel mit Maßnahmen zum Schutz vor Spam verknüpft, die von Internet-Dienstleistern und Mailserveradministratoren implementiert werden.

* Allgemeine Empfehlungen zum Entwerfen erfolgreicher E-Mail-Marketing-Kampagnen finden Sie unter [Auslieferungsstrategie und -definition](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/deliverability-strategy-and-definition.html).

* Für spezifischere Empfehlungen zur Optimierung der Zustellbarkeit Ihrer Adobe Campaign-E-Mails empfehlen wir die Verwendung der in diesem Abschnitt aufgeführten Best Practices.

>[!NOTE]
>
>Da ISPs verpflichtet sind, ständig neue, ausgereifte Filtertechniken zu entwickeln, um ihre Kunden vor Spammer zu schützen, ist die Zustellbarkeit von E-Mails durch ständig wechselnde Kriterien und Regeln gekennzeichnet. Vergewissern Sie sich, dass Sie den Leitfaden [Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html) zur Adobe-Bereitstellung lesen, der regelmäßig aktualisiert wird.

### Auslieferungsrate

Die Auslieferungsrate ist die Anzahl der Nachrichten, die die Postfächer der Empfänger im Vergleich zur Anzahl der ausgelieferten Nachrichten erreicht haben. Um die Lieferbarkeit zu verbessern, können Sie diese Rate erhöhen.

Bei Adobe Campaign hängt die Lieferquote von zahlreichen Faktoren ab, insbesondere von:

* Korrekte Konfiguration der Instanzen: Wenden Sie sich zwecks Hilfe an Ihren Kundenbetreuer.
* Legitime Netzwerkkonfiguration: siehe [diesen Abschnitt](../../sending/using/optimize-delivery.md#network-config) und [Domäneneinrichtung und -strategie](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html#domain-setup-and-strategy).
* Ihre IP-Adresse: Name: siehe [IP-Strategie](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html#ip-strategy).
* Qualität der Zieladressen: siehe [Quarantäne-Management](../../sending/using/optimize-delivery.md#quarantine-management).
* niedrige Raten [Beschwerden](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html) und [harte Absprungrate](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/bounces.html#hard-bounces).
* Inhalt Ihrer Nachricht: Siehe [Steuern des E-Mail-Inhalts](../../sending/using/control-email-content.md).
* Nachrichtenauthentifizierung (SPF, DKIM, DMARC): siehe [diesen Abschnitt](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html#authentication).
* Name des Absenders: Informationen darüber, wie die wichtigsten ISPs den Ruf eines Absenders bewerten, finden Sie in [diesem Abschnitt](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/internet-service-provider-specifics/overview.html).

## Kampagne-Bereitstellungs-Tools {#deliverability-tools}

Adobe Campaign bietet eine Reihe von Tools zur Verfolgung und Verbesserung der Bereitstellungsleistung Ihrer Plattform. Auf dieser Seite werden auch die wichtigsten Grundsätze hervorgehoben, die Sie beachten sollten, um die Lieferbarkeit bei der Verwendung der Kampagne zu optimieren.

### Erstellen Sie Ihre Nachricht sorgfältig

Vergewissern Sie sich beim Konfigurieren, Entwerfen und Testen Ihrer Nachricht, dass Sie die in den folgenden Abschnitten genannten Best Practices befolgen. Die Nutzung aller von Adobe Campaign bereitgestellten Funktionen hilft Ihnen, die Lieferbarkeit zu verbessern.

* [Best Practices beim Versand](../../sending/using/delivery-best-practices.md)
* [Kontrollieren von E-Mail-Inhalten](../../sending/using/control-email-content.md)
* [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md)
* [Testversand durchführen](../../sending/using/sending-proofs.md)

### Einwilligung durch Dublette-Teilnahme überprüfen{#double-opt-in}

Um das Senden von Nachrichten an ungültige Adressen zu vermeiden, unsachgemäße Kommunikation zu begrenzen und den Ruf des Absenders zu verbessern, empfiehlt Adobe die Implementierung eines Dublette-Ausschluss-Mechanismus. Dadurch können Sie sicherstellen, dass Ihre Empfänger absichtlich abonniert wurden.

Weitere Informationen hierzu finden Sie unter [Informationen zum Anmelden und Abwählen in der Kampagne](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

Weitere Informationen zu Best Practices bei der Erfassung von Kundendaten finden Sie im Leitfaden [Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/first-impressions/address-collection-and-list-growth.html#data-quality-and-hygiene) zur Adobe-Bereitstellung.

### Quarantäne-Management nutzen

Adobe Campaign verwaltet eine Liste, bei der Spam-Beschwerden, harte Absprünge und weiche Absprünge, die konsistent ablaufen, erfasst werden.

Zum Schutz Ihrer Zustellbarkeit werden die Empfänger, deren Adressen auf dieser Liste liegen, standardmäßig von allen zukünftigen Versänden ausgeschlossen, da das Senden an diese Kontakte Ihren Ruf beschädigen könnte.

Teilweise werden E-Mails von Providern automatisch als Spam eingestuft, wenn die Anzahl ungültiger Adressen zu hoch ist. Durch die Quarantäne können Sie also vermeiden, von diesen Providern auf eine Blockierungsliste gesetzt zu werden.

Weitere Informationen finden Sie in den folgenden Abschnitten:

* [Ursachen für Fehler beim Versand](../../sending/using/understanding-delivery-failures.md)
* [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md)
* [Quarantäne vs. Blockierungsliste](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist)

### Überwachungs- und Berichte-Tools verwenden

Nutzen Sie die von Adobe Campaign angebotenen Funktionen, um Ihre Lieferbarkeit zu überwachen.

Mit Adobe Campaign können Sie die Leistung Ihrer Versand anhand einer Reihe integrierter Echtzeitindikatoren überprüfen. <!--For example, you can check the number of messages that are successfully executed, sent and delivered. You can also verify the number of messages that have been opened and the number of messages/links that have been clicked.-->Sie können auch vollständig anpassbare Echtzeitberichte erstellen, um einen besseren Einblick in Ihre Versand zu erhalten.

Weitere Informationen finden Sie in den folgenden Abschnitten:

* [Zustellbarkeit überwachen](../../sending/using/monitor-deliverability.md)

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

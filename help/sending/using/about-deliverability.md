---
title: Informationen zur Lieferbarkeit in Adobe Campaign Standard
description: Erfahren Sie mehr über die Konzepte und Best Practices im Zusammenhang mit der Zustellbarkeit sowie über die Werkzeuge von Adobe Campaign Standard, mit denen Sie Ihren Versand optimieren können.
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 44049443f8028ed26089ee0d49944ebac6a62111

---


# Informationen zur Bereitstellung{#about-deliverability}

Lieferbarkeit oder wie der Erfolg Ihrer Kampagnen, die den Posteingang Ihrer Empfänger erreichen, ohne zu springen oder als Spam gekennzeichnet zu werden, gemessen wird.

Adobe Campaign Deliverability ist ein kostenpflichtiger Service, der in verschiedenen Angeboten angeboten wird. Kontaktieren Sie die Lieferbarkeit oder den kommerziellen Service.

Die Zulieferungsrate hängt von zahlreichen Faktoren ab, insbesondere:

* Korrekte Konfiguration der Instanzen
* Ruf Ihrer IP-Adresse
* Qualität der Zieladressen
* Niedrige Reklamations- und Absprungraten
* Inhalt Ihrer Nachricht
* Nachrichtenauthentifizierung (SPF, DKIM, DMARC)
* Name des Absenders

## Wichtigste zu prüfende Punkte {#deliverability-key-points}

Um die Auslieferbarkeit Ihrer Adobe Campaign-E-Mails zu optimieren, empfehlen wir die folgenden Best Practices. Probleme mit der Lieferbarkeit stehen in der Regel im Zusammenhang mit Maßnahmen zum Schutz vor Spam, die von Internetdienstanbietern und Mailserver-Administratoren durchgeführt werden.

Die E-Mail-Zustellbarkeit bezieht sich auf den Satz von Merkmalen, die bestimmen, ob eine Nachricht ihr Ziel erreichen kann, über eine persönliche E-Mail-Adresse, innerhalb kurzer Zeit und mit der erwarteten Qualität in Bezug auf Inhalt und Format. Diese Merkmale fallen in vier Hauptkategorien: Datenqualität, Nachrichten und Inhalte, Sendeninfrastruktur und Ruf. Gemeinsam bilden sie die Grundlage eines erfolgreichen E-Mail-Auslieferungsprogramms.

Die Bereitstellungsrate ist die Anzahl der gesendeten E-Mails, die erfolgreich an die Empfänger gesendet wurden.
Hier finden Sie eine Liste der wichtigsten Punkte, die überprüft werden müssen, um eine gute Lieferbarkeit zu gewährleisten.

## Bereitstellungswerkzeuge {#deliverability-tools}

Beginnen Sie zunächst mit der Dokumentation zu den mit Campaign Standard bereitgestellten Bereitstellungswerkzeugen:
* [Best Practices bereitstellen](https://helpx.adobe.com/campaign/kb/delivery-best-practices.html)
* [Personalisieren des Absendernamens](../../designing/using/personalization.md#personalizing-the-sender)
* [Betreffzeile einer E-Mail testen](../../sending/using/testing-subject-line-email.md)
* [Versandzeitpunkt optimieren](../../sending/using/optimizing-the-sending-time.md)
* [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md)
* [E-Mail-Rendering](../../sending/using/email-rendering.md)
* [Sendungen beobachten](../../sending/using/monitoring-a-delivery.md)
* [Warnungen bei Zustellproblemen erhalten](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Ursachen von fehlgeschlagenen Sendungen](../../sending/using/understanding-delivery-failures.md)
* [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md)
* [Quarantäne im Vergleich zur Blacklist](../../sending/using/understanding-quarantine-management.md#quarantine-vs-blacklisting)
* [Dynamische Berichte](../../reporting/using/about-dynamic-reports.md)

## Überprüfen der Netzwerkkonfiguration {#network-configuration}

Spammer versuchen, ihre wahre Identität zu verbergen und machen daher ihre Server schwer zu identifizieren. Eine legitime Netzwerkkonfiguration, die nicht versucht, die Identität des Servers zu verbergen, ist unverzichtbar, um E-Mails in großen Mengen zu senden.

## Senden an gültige Adressen {#valid-addresses}

Spammer verwenden oft Adressgeneratoren, die auf Listen mit häufigen Namen und Vornamen basieren. Außerdem verarbeiten sie selten technische Benachrichtigungen, die von Mail-Servern zurückgesendet werden. Eine hohe Anzahl ungültiger Adressen wird häufig als Spam interpretiert. Doppelte Abmeldemechanismen und eine effektive Handhabung technischer Absprungmeldungen ermöglichen es, dies zu vermeiden.

## Verringerung der Beschwerderate {#reduce-complaint-rate}

ISPs verfügen in der Regel über eine auffällige Möglichkeit, eine empfangene Nachricht als Spam zu melden. Dadurch können unzuverlässige Quellen identifiziert werden. Indem Sie schnell Ausstiegsanfragen beantworten, regelmäßig eine bestimmte Liste verwenden, die Zustimmung durch ein doppeltes Opt-in-System überprüfen und Feedback-Schleifen implementieren, können Sie die Beschwerderaten senken.

## An Honigtopf-Adressen senden {#honeypot-addresses}

ISPs und andere Organisationen (siehe http://www.projecthoneypot.org/) verwenden Postfächer, die nicht mit physischen Personen übereinstimmen, sondern einfach geschaffen werden, um Spammer zu tricksen. Diese so genannten "Honigtopf"-Adressen werden im Internet veröffentlicht, um von Spambots gesammelt und damit illegitime Absender gefangen zu werden. Die Verwendung eines doppelten Opt-in-Mechanismus verhindert, dass eine solche Adresse einer Liste hinzugefügt wird. Wenn Sie eine Drittanbieter-Liste verwenden, müssen Sie sicher sein, welche Methoden der Betreuer verwendet.

## Inhalt der Nachricht anpassen {#adapt-message-content}

In geringerem Maße kann der Inhalt bestimmter Nachrichten dazu führen, dass bestimmte Filter ihn als Spam erkennen. Die Verwendung bestimmter Wörter, die Verwendung von Ausrufezeichen in der Betreffzeile und in den Nachrichten werden als erkennbare Zeichen von Spam gelesen. Spammer sind auch dafür bekannt, Text durch Bilder zu ersetzen, um zu verhindern, dass Text, der gegen sie verstößt, automatisch durch Anti-Spam-Filter analysiert wird. Daraufhin wird möglicherweise eine Meldung (im HTML-Format) mit einem hohen Anteil an Bildern oder Bildern als Anlagen blockiert.

## Regelmäßige Entsendung {#regular-deliveries}

Spammer machen programmierte Lieferungen, um ihren Ruf im Laufe der Zeit zu erhalten. Manchmal müssen sie ihren Marketingplan anpassen, um die von den ISPs auferlegten Best Practices zu erfüllen, und so konfigurieren sie nach einem guten Ruf (Hochfahren) regelmäßige Lieferungen.

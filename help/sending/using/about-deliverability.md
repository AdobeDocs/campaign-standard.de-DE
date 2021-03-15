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
role: Geschäftspraktiker
level: Fortgeschr.
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 99%

---


# Über die Zustellbarkeit{#about-deliverability}

Die Zustellbarkeit misst, wie viele Ihrer Nachrichten erfolgreich an die Empfängerpostfächer zugestellt und nicht als unzustellbar zurückgesendet bzw. als Spam gekennzeichnet werden.

Die Zustellrate hängt u. a. von folgenden Faktoren ab:

* der korrekten Konfiguration Ihrer Instanzen;
* der Reputation Ihrer IP-Adresse;
* der Qualität der Zielkontakte;
* einer niedrigen Anzahl an Beschwerden und Hardbounces;
* Ihren Nachrichteninhalten;
* der Nachrichtenauthentifizierung (SPF, DKIM, DMARC);
* der Reputation des Absenders.

## Wichtigste zu prüfende Punkte {#deliverability-key-points}

Um die Zustellbarkeit Ihrer E-Mails in Adobe Campaign zu optimieren, empfehlen wir, die unten aufgeführten Best Practices einzuhalten. Zustellbarkeitsprobleme resultieren im Allgemeinen aus Schutzmaßnahmen gegen Spam, die von Internetdienstanbietern und Mail-Server-Administratoren eingerichtet werden.

Die E-Mail-Zustellbarkeit hängt von verschiedenen Eigenschaften ab, die bestimmen, ob eine Nachricht innerhalb kurzer Zeit ihr Ziel über eine persönliche E-Mail-Adresse in der erwarteten Qualität bezüglich Inhalt und Format erreicht. Diese Eigenschaften werden in vier Hauptkategorien unterteilt: Datenqualität, Nachricht und Inhalt, Versandinfrastruktur und Reputation. Gemeinsam bilden sie die Grundlage eines erfolgreichen E-Mail-Zustellprogramms.

Die Zustellrate ist die Anzahl der E-Mails, die ihren Empfängern erfolgreich zugestellt wurde.
Folgende Faktoren können die Zustellbarkeit Ihrer E-Mails beeinträchtigen.

## Zustellbarkeits-Tools {#deliverability-tools}

Lesen Sie zunächst den Abschnitt über die Zustellbarkeits-Tools von Campaign Standard.
* [Best Practices beim Versand](../../sending/using/delivery-best-practices.md)
* [Absendername personalisieren](../../designing/using/personalization.md#personalizing-the-sender)
* [Versandzeitpunkt optimieren](../../sending/using/optimizing-the-sending-time.md)
* [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md)
* [E-Mail-Rendering](../../sending/using/email-rendering.md)
* [Versand beobachten](../../sending/using/monitoring-a-delivery.md)
* [Warnungen bei Zustellproblemen erhalten](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Ursachen für Fehler beim Versand](../../sending/using/understanding-delivery-failures.md)
* [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md)
* [Quarantäne vs. Blockierungsliste](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist)
* [Dynamische Berichte](../../reporting/using/about-dynamic-reports.md)

## Prüfen der Netzwerkkonfiguration {#network-configuration}

Spammer versuchen, ihre Identität zu verschleiern, und erschweren zu diesem Zweck die Identifizierung ihrer Server. Daher ist eine ordnungsgemäße Netzwerkkonfiguration, mit der nicht versucht wird, die Identität des Servers zu verbergen, für den Versand großer E-Mail-Mengen von entscheidender Bedeutung.

## Senden an gültige Adressen {#valid-addresses}

Spammer verwenden oft Adressgeneratoren basierend auf Listen häufiger Namen und Vornamen. Zusätzlich beachten sie nur selten von Mailservern zurückgesendete technische Benachrichtigungen. Eine hohe Menge ungültiger Adressen wird daher oft als Hinweis auf Spam betrachtet. Dies können Sie mit einem doppelten Anmeldeverfahren (Double-Opt-in) und der wirksamen Bearbeitung technischer Bounce Messages vermeiden.

## Verringern der Beschwerderate {#reduce-complaint-rate}

ISPs bieten normalerweise die Möglichkeit, eine erhaltene Nachricht als Spam zu melden und dadurch zweifelhafte Quellen zu identifizieren. Sie können die Beschwerderate verringern, indem Sie Abmeldewünsche rasch berücksichtigen, regelmäßig eine entsprechende Liste verwenden, das Einverständnis der Empfänger durch ein doppeltes Anmeldeverfahren verifizieren und Feedback-Schleifen integrieren.

## Versand an eine Spam-Falle (honeypot){#honeypot-addresses}

ISPs und andere Organisationen (siehe https://www.projecthoneypot.org/) verwenden Postfächer, die nicht mit physischen Personen übereinstimmen, sondern ausschließlich eingerichtet werden, um Spammer anzuziehen. Diese so genannten &quot;honeypot&quot;-Adressen werden im Web veröffentlicht, um von Spambots gesammelt zu werden und so eine Erkennung illegitimer Absender zu erlauben. Durch ein Anmeldeverfahren mit doppelter Bestätigung wird verhindert, dass solche Adressen einer Liste hinzugefügt werden. Wenn Sie eine Liste eines Drittanbieters nutzen, müssen Sie wissen, welche Methoden der jeweilige Verwalter anwendet.

## Anpassen des Nachrichteninhalts {#adapt-message-content}

In geringerem Maß kann auch der Nachrichteninhalt dazu führen, dass E-Mails von manchen Filtern als Spam eingestuft werden. Der Einsatz von bestimmten Wörtern oder Ausrufezeichen im Betreff und Text wird als Hinweis auf Spam betrachtet. Oft ersetzen Spammer auch Text durch Bilder, damit der Text von Anti-Spam-Filtern nicht automatisch analysiert werden kann. Darum kann eine Nachricht (im HTML-Format) mit einem hohen Anteil an Bildern oder mit Bildern im Anhang ggf. blockiert werden.

## Regelmäßiges Senden {#regular-deliveries}

Spammer führen programmierte Sendungen durch, um langfristig ihre Reputation zu wahren. Manchmal müssen sie ihren Marketingplan an die Best Practices des jeweiligen ISPs anpassen. Deshalb führen sie nach einer Optimierung ihrer Reputation (ramp-up) regelmäßige Sendungen durch.

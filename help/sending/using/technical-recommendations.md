---
title: Technische Empfehlungen zur Auslieferung für Adobe Campaign Standard
description: Lesen Sie mehr über einige technische Empfehlungen zur Verbesserung der Lieferbarkeit mit Adobe Campaign Standard.
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


# Technische Empfehlungen{#technical-recommendations}

Darüber hinaus werden im Folgenden einige Techniken, Konfigurationen und Tools aufgelistet, mit denen Sie Ihre Bereitstellungsrate verbessern können.

Hier einige Definitionen der wichtigsten technischen Begriffe.

**Rückgängig-DNS** Adobe Campaign prüft, ob ein umgekehrter DNS für eine IP-Adresse angegeben wird und ob dies korrekt auf die IP zurückzeigt.

**MX-Regeln** MX-Regeln werden verwendet, um die Geschwindigkeit zu steuern, mit der die Kampagnen-MTA (Message Transfer Agent) E-Mails an jede einzelne E-Mail-Domäne oder jeden ISP (z.B. hotmail.com, comcast.net) sendet. Diese Regeln basieren in der Regel auf den von den ISPs veröffentlichten Beschränkungen (z. B. nicht mehr als 20 Meldungen pro SMTP-Verbindung).

**TLS** TLS (Transport Layer Security) ist ein Verschlüsselungsprotokoll, mit dem die Verbindung zwischen zwei E-Mail-Servern gesichert und der Inhalt einer E-Mail vor dem Lesen durch andere Personen als die vorgesehenen Empfänger geschützt werden kann.

**SPF** SPF (Sender Policy Framework) ist ein Standard für die E-Mail-Authentifizierung, mit dem der Inhaber einer Domäne angeben kann, welche E-Mail-Server E-Mails für diese Domäne senden dürfen. Dieser Standard verwendet die Domäne in der Kopfzeile "Rückgabepfad" der E-Mail (auch als "Umschlag von"bezeichnet).

**Die DKIM** DKIM (Domain Keys Identified Mail)-Authentifizierung ist eine Nachfolgerin von SPF und verwendet eine Public-Key-Kryptographie, die dem Empfänger-E-Mail-Server ermöglicht, zu überprüfen, ob eine Nachricht tatsächlich von der Person oder Organisation gesendet wurde, von der sie versendet wurde, und ob der Inhalt der Nachricht zwischen dem Zeitpunkt der ursprünglichen Versendung (und dem "Signieren") und dem Zeitpunkt des Eingangs geändert wurde. Dieser Standard verwendet in der Regel die Domäne im Header "From"oder "Sender".

**DMARC** DMARC (domänenbasierte Nachrichtenauthentifizierung, Berichterstellung und Konformität) ist die neueste Form der E-Mail-Authentifizierung. Bei der Entscheidung, ob eine E-Mail weitergeleitet wird oder fehlschlägt, wird sowohl die SPF- als auch die DKIM-Authentifizierung verwendet. DMARC ist einzigartig und leistungsstark in zwei sehr wichtigen Bereichen:
* Konformität: Sie ermöglicht es dem Absender, die ISPs anzuweisen, was mit Nachrichten zu tun ist, die sich nicht authentifizieren können (z. B. nicht akzeptieren).
* Berichterstellung: Der Absender erhält einen detaillierten Bericht mit allen Meldungen, bei denen die DMARC-Authentifizierung fehlgeschlagen ist, sowie der jeweils verwendeten "Von"-Domäne und IP-Adresse. Dadurch kann ein Unternehmen legitime E-Mails identifizieren, bei denen die Authentifizierung fehlschlägt und eine Art "Korrektur"erforderlich ist (z. B. das Hinzufügen von IP-Adressen zu ihrem SPF-Datensatz), sowie die Quellen und die Häufigkeit von Phishing-Versuchen auf ihren E-Mail-Domänen.

DMARC kann die von 250ok generierten Berichte nutzen.

**SMTP** SMTP (Simple Mail Transfer Protocol) ist ein Internetstandard für die E-Mail-Übertragung.

**Dedizierte IPs** Adobe stellt für jeden Kunden eine IP-Strategie mit einer Upload-IP bereit, um einen Ruf zu schaffen und die Bereitstellungsleistung zu optimieren.

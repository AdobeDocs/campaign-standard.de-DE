---
title: Technische Empfehlungen zur Zustellbarkeit für Adobe Campaign Standard
description: Erfahren Sie mehr über verschiedene technische Empfehlungen zur Verbesserung der Zustellbarkeit mit Adobe Campaign Standard.
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
translation-type: ht
source-git-commit: 44049443f8028ed26089ee0d49944ebac6a62111

---


# Technische Empfehlungen{#technical-recommendations}

Zudem enthält die folgende Liste diverse Techniken, Konfigurationen und Werkzeuge zur Verbesserung Ihrer Zustellrate.

Im Folgenden finden Sie einige Definitionen der wichtigsten technischen Begriffe.

**Reverse DNS**: Adobe Campaign prüft, ob für eine IP-Adresse ein Reverse-DNS angegeben ist und ob dieses wirklich auf die IP-Adresse zurückverweist.

**MX-Regeln**: MX-Regeln dienen zum Steuern der Geschwindigkeit, mit der der Campaign-MTA (Message Transfer Agent) E-Mails an die einzelnen E-Mail-Domains oder ISPs (z. B. hotmail.com, comcast.net) sendet. Diese Regeln basieren meist auf den von den ISPs veröffentlichten Beschränkungen (z. B. nicht mehr als 20 Nachrichten pro SMTP-Verbindung).

**TLS**: TLS (Transport Layer Security) ist ein Verschlüsselungsprotokoll zur Sicherung der Verbindung zwischen zwei E-Mail-Servern. Damit wird sichergestellt, dass die E-Mail nur vom beabsichtigten Empfänger gelesen werden kann.

**SPF**: SPF (Sender Policy Framework) ist ein Standard für die E-Mail-Authentifizierung, mit dem der Inhaber einer Domain angeben kann, welche E-Mail-Server E-Mails im Namen dieser Domain senden dürfen. Bei diesem Standard wird die Domain in der Kopfzeile &quot;Return-Path&quot; der E-Mail (auch als &quot;Envelope From&quot;-Adresse bezeichnet) genutzt.

**DKIM**: DKIM (Domain Keys Identified Mail)-Authentifizierung ist ein Nachfolger von SPF und verwendet Public-Key-Verschlüsselung, mit der der E-Mail-Empfangsserver überprüfen kann, ob eine Nachricht tatsächlich von der angegebenen Person oder dem angegebenen Unternehmen gesendet wurde. Ferner kann festgestellt werden, ob die Nachricht zwischen dem Versandzeitpunkt (und der &quot;Signierung&quot; mit DKIM) sowie dem Empfangszeitpunkt verändert wurde. Bei diesem Standard wird in der Regel die Domain im &quot;Von&quot;- oder &quot;Absender&quot;-Header genutzt.

**DMARC** DMARC (Domain-based Message Authentication, Reporting and Conformance) ist die neueste Art der E-Mail-Authentifizierung. Bei der Entscheidung, ob eine E-Mail weitergeleitet wird oder fehlschlägt, kommt sowohl SPF- als auch DKIM-Authentifizierung zum Einsatz. DMARC ist in zwei wichtigen Bereichen einzigartig und extrem leistungsstark:
* Conformance (Konformität) – ermöglicht dem Absender, ISPs anzuweisen, was mit einer Nachricht passieren soll, die nicht authentifiziert werden kann (z. B. nicht akzeptieren).
* Reporting (Berichterstellung) – liefert dem Absender einen detaillierten Bericht mit allen Nachrichten, die die DMARC-Authentifizierung nicht bestanden haben, sowie die jeweils verwendete &quot;Von&quot;-Domain und IP-Adresse. Damit können Unternehmen legitime E-Mails erkennen, die nicht authentifiziert werden konnten und &quot;repariert&quot; werden müssen (z. B. durch Hinzufügen von IP-Adressen zu ihrem SPF-Datensatz), sowie die Quellen und das Vorkommen von Phishing-Versuchen auf ihren E-Mail-Domains identifizieren.

DMARC kann die von 250ok erstellten Berichte nutzen.

**SMTP**: SMTP (Simple Mail Transfer Protocol) ist ein Internet-Standard für die E-Mail-Übertragung.

**Dedizierte IP-Adressen**: Adobe bietet jedem Kunden für die Anlaufphase eine dedizierte IP-Strategie zum Aufbau der Reputation und zur Optimierung der Zustellbarkeit.

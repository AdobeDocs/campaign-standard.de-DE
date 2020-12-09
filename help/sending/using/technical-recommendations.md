---
solution: Campaign Standard
product: campaign
title: Technische Empfehlungen zur Zustellbarkeit für Adobe Campaign Standard
description: Erfahren Sie mehr über verschiedene technische Empfehlungen zur Verbesserung der Zustellbarkeit mit Adobe Campaign Standard.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
translation-type: ht
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: ht
source-wordcount: '465'
ht-degree: 100%

---


# Technische Empfehlungen{#technical-recommendations}

Die folgende Liste enthält diverse Techniken, Konfigurationen und Werkzeuge zur Verbesserung Ihrer Zustellrate. Im Folgenden finden Sie einige Definitionen der wichtigsten technischen Begriffe.

**Reverse DNS**: Adobe Campaign prüft, ob für eine IP-Adresse ein Reverse-DNS angegeben ist und ob dieses wirklich auf die IP zurückverweist.

**MX-Regeln** steuern die Geschwindigkeit, mit der Campaign MTA (Message Transfer Agent) E-Mails an jede E-Mail-Domain oder jeden ISP (z. B. hotmail.com, comcast.net) sendet. Diese Regeln basieren normalerweise auf den Beschränkungen der ISPs (z. B. Pro SMTP-Verbindung dürfen maximal 20 Nachrichten gesendet werden).

**TLS** (Transport Layer Security) ist ein Verschlüsselungsprotokoll zur Sicherung der Verbindung zwischen zwei E-Mail-Servern. Damit wird sichergestellt, dass die E-Mail nur vom beabsichtigten Empfänger gelesen werden kann.

**SPF** (Sender Policy Framework) ist ein E-Mail-Authentifizierungsstandard, mit dem der Besitzer einer Domain bestimmen kann, welche E-Mail-Server E-Mails im Namen dieser Domain versenden dürfen. Dieser Standard verwendet die Domain im &quot;Return-Path&quot;-Header der E-Mail (auch &quot;Envelope From&quot;-Adresse genannt).

**DKIM** (Domain Keys Identified Mail)-Authentifizierung ist ein Nachfolger von SPF und verwendet Public-Key-Verschlüsselung, mit der der E-Mail-Empfangsserver überprüfen kann, ob eine Nachricht tatsächlich von der angegebenen Person oder dem angegebenen Unternehmen gesendet wurde. Ferner kann festgestellt werden, ob die Nachricht zwischen dem Versandzeitpunkt (und &quot;signiert&quot; mit DKIM) und dem Empfangszeitpunkt verändert wurde. Bei diesem Standard wird die Domain im &quot;Von&quot;- oder &quot;Absender&quot;-Header angegeben.

**DMARC** (Domain-based Message Authentication, Reporting and Conformance) ist die aktuellste Form der E-Mail-Authentifizierung. Sie nutzt sowohl SPF als auch DKIM-Authentifizierung, um festzustellen, ob eine E-Mail-Adresse als gültig erachtet wird oder nicht. DMARC ist ein einzigartiges Tool und bietet zwei wichtige wirkungsvolle Funktionen:
* Conformance (Konformität) – ermöglicht dem Absender, ISPs anzuweisen, was mit einer Nachricht passieren soll, die nicht authentifiziert werden kann (z. B. nicht akzeptieren).
* Reporting (Berichterstellung) – liefert dem Absender einen detaillierten Bericht mit allen Nachrichten, die die DMARC-Authentifizierung nicht bestanden haben, sowie die jeweils verwendete &quot;Von&quot;-Domain und IP-Adresse. Damit können Unternehmen legitime E-Mails erkennen, die nicht authentifiziert werden konnten und &quot;repariert&quot; werden müssen (z. B. durch Hinzufügen von IP-Adressen zu ihrem SPF-Datensatz), sowie die Quellen und das Vorkommen von Phishing-Versuchen auf ihren E-Mail-Domains identifizieren.

DMARC kann die von 250ok erstellten Berichte nutzen.

**SMTP** (Simple Mail Transfer Protocol) ist ein Internetstandard für die E-Mail-Übertragung.

**Dedizierte IP-Adressen**: Adobe bietet jedem Kunden für die Anlaufphase eine dedizierte IP-Strategie zum Aufbau der Reputation und zur Optimierung der Zustellbarkeit.

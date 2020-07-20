---
title: Zulassungslisten in Adobe Campaign Standard
description: Erfahren Sie, wie Sie Zulassungslisten mit Adobe Campaign Standard optimieren können.
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
source-git-commit: c89973e2c733d9c0b1c4434e77ef51103ccde0fa
workflow-type: ht
source-wordcount: '330'
ht-degree: 100%

---


# IP-Zertifizierung {#ip-certification}

IP-Zertifizierung ist ein Best Practices-Sendeprogramm, mit dem sichergestellt wird, dass E-Mails ohne Blockierung durch Antispam-Filter oder andere E-Mail-Blockierungssysteme empfangen werden.

Derzeit bieten zwei Anbieter eine IP-Zertifizierung an: Return Path und Certified Senders Alliance.

Zertifizierte Absender werden E-Mail-Zulassungslisten hinzugefügt, die von globalen E-Mail-Anbietern und E-Mail-Sicherheitsunternehmen verwendet werden. Diese kommerziellen Zulassungslisten basieren auf einem System, das es dem Absender erlaubt, beim Eintritt in das System Anti-Spam-Filter ganz zu umgehen oder inkrementelle Punkte zu erhalten.

Das [Zertifizierungsprogramm von Return Path](https://www.validity.com/products/returnpath/certification/) bietet eine Reihe von Vorteilen, darunter die folgenden:
* Eine messbare Steigerung der Posteingangsplatzierung bei führenden E-Mail-Anbietern wie Microsoft, AOL, Yahoo, Gmail, Comcast, Orange, Mail.ru und mehr
* Positive Reputation und bevorzugte Behandlung bei kritischen Filtern wie Cloudmark, SpamAssassin und Cisco Ironport
* Ein Compliance-Team, das rund um die Uhr überwacht, Sicherheitswarnungen bereitstellt und mit Ihnen bei der Lösung von Kompromissen zusammenarbeitet
* E-Mail-Anbieterdaten mit detaillierten Informationen zu KPIs, Platzierung und Zertifizierungsleistung
* Vereinfachtes und schnelleres IP-Warmup, einschließlich einer besseren Reputation und Erkennung bei der Migration oder beim Erhalt einer neuen IP-Adresse

Die Zertifizierung durch [Certified Senders Alliance](https://certified-senders.org/certification-process/) bietet unter anderem folgende Vorteile:
* Zertifizierung von Absendern von kommerziellen E-Mails, die hohe Qualitätsstandards erfüllen können
* Verbesserter Versand und verbesserte Zustellbarkeit von kommerziellen E-Mails, um die Platzierungsrate im Posteingang zu erhöhen und das Filtern von Spam zu reduzieren
* Schutz vor rechtlichen und finanziellen Risiken durch vollständige Einhaltung der Rechtsnormen
* Schutz der Reputation durch frühzeitige Warnungen der CSA-Beschwerdestelle und tägliche Berichte über Spam-Fallen

ISPs können diese Dienste beliebig verwenden und die Anzahl der ISPs variiert je nach Zulassungsliste.

Da jedoch immer mehr ISPs ihre Antispam-Filter auf Grundlage des Verhaltens jedes Posteingangsbesitzers erstellen, anstatt den Nachrichteninhalt selbst zu analysieren, kann die Verwendung der IP-Zertifizierung keine Garantie für die Platzierung im Posteingang oder gar die Bereitstellung sein.

---
title: Whitelists in Adobe Campaign Standard
description: Erfahren Sie, wie Sie Whitelists mit Adobe Campaign Standard optimieren.
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


# Whitelist{#whitelists}

Die wichtigsten Internetdienstanbieter (ISPs) und Webmail-Anbieter verwalten Whitelists von anerkannten E-Mail-Nachrichtensendern. Adobe Campaign unterstützt Sie dabei, sich für die besten Whitelists zu zertifizieren.

Eine E-Mail-Whitelist ist eine Liste von E-Mail-Adressen oder Domänennamen, von denen aus ein E-Mail-Blockierungsprogramm Nachrichten empfangen kann.

Es gibt zwei Arten von Whitelist:
* Nicht-kommerzielle Whitelist
* Kommerzielle Whitelisten

## Nicht-kommerzielle Whitelist {#non-commercial-whitelists}

Um von diesen Whitelists akzeptiert zu werden, muss der Absender eine Reihe von Tests auf der Grundlage einer technischen Überprüfung (sein E-Mail-Server darf kein offener Relais sein, sondern sollte eine statische IP haben) der Infrastruktur oder ihrer Aktivität (Lieferfrequenz, Volumen, Anzahl der Beschwerden) bestehen.

Befolgt der Absender keine dieser Regeln, kann er aus der Whitelist gelöscht werden. Adobe Campaign bietet in seinem **Adobe Campaign E-Mail-Bereitstellungspaket** einen begleitenden Beratungsservice von Experten für den Zertifizierungsprozess für nicht kommerzielle Whitelists.

## Kommerzielle Whitelisten {#commercial-whitelists}

Kommerzielle Whitelists basieren auf einem System, das es dem Absender erlaubt, Antispam-Filter ganz zu umgehen oder inkrementelle Punkte zuzuweisen, wenn er in das System eintritt. Diese zahlenden Whitelists (CPT oder auf Jahresbasis) werden von Systemen wie dem Rücksenderergebnis angeboten.

ISPs können diese Dienste kostenlos nutzen, und die Anzahl der ISPs kann je nach Whitelist variieren. Ein Absender kann daher mit einer Liefergarantie seine Nachrichten sicherer verschicken. Bestimmte Whitelists bieten auch an, Bilder zu öffnen und Links zu aktivieren.

Das Anzeigen in einer Whitelist ist ein unbestreitbarer Vorteil für jede E-Mail-Kampagne. In seinem **Adobe Campaign E-Mail-Bereitstellungspaket** bietet Adobe Campaign einen kommerziellen Whitelist-Zertifizierungsdienst wie CSA und Rückgabepfad-Senderbewertung.
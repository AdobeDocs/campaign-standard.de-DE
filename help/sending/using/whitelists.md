---
title: Whitelists in Adobe Campaign Standard
description: Erfahren Sie, wie Sie Whitelists mit Adobe Campaign Standard optimieren können.
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


# Whitelists{#whitelists}

Die wichtigsten ISPs und Web Mail Provider verwalten Whitelists von anerkannten Absendern von E-Mail-Nachrichten. Adobe Campaign hilft Ihnen dabei, für die besten Whitelists zertifiziert zu werden.

Eine E-Mail-Whitelist ist eine Liste mit E-Mail-Adressen oder Domain-Namen, deren Empfang ein E-Mail-Blockierungsprogramm zulässt.

Es gibt zwei Arten von Whitelists:
* Nicht kommerzielle Whitelists
* Kommerzielle Whitelists

## Nicht kommerzielle Whitelists {#non-commercial-whitelists}

Um von diesen Whitelists akzeptiert zu werden, muss der Absender eine Reihe von Tests bestehen. Diese basieren auf einer technischen Überprüfung der Infrastruktur (der E-Mail-Server darf keine &quot;open relay&quot;-Adressen verwenden, sondern muss eine statische IP-Adresse besitzen) oder der Aktivität (Versandhäufigkeit, Volumen, Anzahl der Beschwerden).

Wenn der Absender eines dieser Kriterien nicht erfüllt, kann er von der Whitelist gestrichen werden. Adobe Campaign bietet im Rahmen seines **Zustellbarkeits-Packages** einen begleitenden Beratungsdienst durch Experten für den Zertifizierungsprozess für nicht kommerzielle Whitelists.

## Kommerzielle Whitelists {#commercial-whitelists}

Kommerzielle Whitelists basieren auf einem System, das es dem Absender erlaubt, beim Eintritt in das System Anti-Spam-Filter ganz zu umgehen oder inkrementelle Punkte zu erhalten. Diese kostenpflichtigen Whitelists (CPT oder auf Jahresbasis) werden von Systemen wie Return Path Sender Score angeboten.

ISPs können diese Dienste beliebig verwenden und die Anzahl der ISPs variiert je nach Whitelist. Ein Absender genießt daher beim Versand seiner Nachrichten mehr Sicherheit, wenn er eine Zustellgarantie besitzt. Manche Whitelists bieten auch das Öffnen von Bildern und Aktivieren von Links an.

Das Erscheinen in einer Whitelist ist zweifelsfrei ein Vorteil für jede E-Mail-Kampagne. Adobe Campaign bietet in seinem **Zustellbarkeits-Package** einen Zertifizierungsdienst für kommerzielle Whitelists wie etwa CSA und Return Path Sender Score.
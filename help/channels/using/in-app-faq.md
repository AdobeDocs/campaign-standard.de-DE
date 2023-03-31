---
title: Häufig gestellte Fragen zu In-App-Nachrichten
description: Häufig gestellte Fragen zu In-App-Nachrichten
audience: channels
content-type: reference
topic-tags: in-app-messaging
context-tags: delivery,triggers,back
feature: In App
role: User
exl-id: 0101773d-b109-49a3-89d4-b4bb226d9ebd
source-git-commit: 597ece8d833a216f0540f801461b08fdc9865024
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 100%

---

# Häufig gestellte Fragen zu In-App-Nachrichten {#in-app-faq}

## Welche Ressourcen wären empfehlenswert, um mehr über den In-App-Kanal in Adobe Campaign Standard zu erfahren? {#resources-inapp}

Sehen Sie sich die folgenden Ressourcen an:

* [Video-Tutorials](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/mobile/in-app/in-app-message-overview.html?lang=de)
* [Blogpost](https://theblog.adobe.com/get-more-out-of-the-new-in-app-message-channel-from-adobe-campaign/)
* [Community-Seite](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-standard/ct-p/adobe-campaign-standard-community)

## Welchen Zweck haben die Campaign-Erweiterungs-APIs setLinkageField und resetLinkageField? {#extensions-apis}

Da In-App-Nachrichten vom SDK aus Campaign abgerufen werden, möchten wir einen sicheren Mechanismus bereitstellen, um sicherzustellen, dass In-App-Nachrichten mit PII-Daten nicht in böswillige Hände geraten. Daher verfügen wir über folgenden Mechanismus, um den sicheren Versand von Nachrichten an das Gerät zu gewährleisten:

* Kunden markieren mobile Profilfelder (Tabelle appSubscriberRcp) als persönlich und vertraulich, wenn sie sicherstellen möchten, dass diese speziellen Informationen sicher zugestellt werden.
* Als solche gekennzeichnete Felder können nur in der Profilvorlage (nicht in der AppSubscriber-Vorlage oder der Broadcast-Vorlage) verwendet werden, in die ein zusätzlicher Sicherheitsmechanismus integriert ist.
* Mit der Profilvorlage erstellte Nachrichten können nur zugestellt werden, wenn sich der Benutzer bei der App angemeldet hat.
* Um diesen sicheren Handshake zu ermöglichen, sollten Entwickler von Mobile Apps zusätzliche Authentifizierungsdetails mithilfe der setLinkageField-API übergeben. Bitte beachten Sie, dass die Verknüpfungsfelder diejenigen sind, die bei der Erweiterung der appSubscriberRcp-Tabelle als Verknüpfung zwischen mobilen Profilen und CRM-Profilen identifiziert werden.
* Sie sollten die auf dem Gerät gespeicherten In-App-Nachrichten leeren und resetLinkagefields zurücksetzen, wenn sich der Benutzer mit resetLinkageField bei der App abmeldet. Dadurch wird sichergestellt, dass ein anderer Benutzer, der sich bei der App anmeldet, nicht die für den vorherigen Benutzer bestimmten Nachrichten sieht.
* Informationen zur Client-seitigen Implementierung dieses Sicherheitsmechanismus finden Sie unter [Mobile SDK-APIs](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/).

## Was muss ich tun, um In-App-Berichte in Campaign zu aktivieren? {#enable-inapp-reporting}

Konfigurieren Sie ein Postback für das In-App-Tracking. Anweisungen dazu finden Sie [hier](../../administration/using/configuring-rules-launch.md#inapp-tracking-postback).

Informationen zur Implementierung des lokalen Benachrichtigungs-Tracking finden Sie auf dieser [Seite](../../administration/using/local-tracking.md).

## Welche Berichte stehen für den In-App-Kanal zur Verfügung? {#report-inapp}

In Adobe Campaign steht für den In-App-Kanal ein vordefinierter Bericht zur Verfügung. In dieser [Dokumentation](../../reporting/using/in-app-report.md) finden Sie weitere Informationen.

Auf dieser [Seite](../../reporting/using/indicator-calculation.md#in-app-delivery) erfahren Sie, wie die einzelnen In-App-Metriken berechnet werden.

## Unterstützen Sie mehrsprachige Inhaltsvarianten für In-App-Nachrichten ähnlich wie für Push-Nachrichten? {#multilingual-inapp}

Für In-App-Nachrichten stehen derzeit keine mehrsprachigen Vorlagen zur Verfügung.

Wenn das Ziel jedoch darin besteht, eine In-App-Nachricht in einer anderen Sprache als Englisch zu senden, können die Inhalte direkt in die verfügbaren Textfelder eingefügt werden.

![](assets/faq_inapp.png)

## Können Campaign-Personalisierungsfelder zu benutzerdefiniertem HTML hinzugefügt werden? {#custom-html-inapp}

Nein, das wird noch nicht unterstützt.

## Ich habe eine Warnmeldung konfiguriert, aber sie wird nicht auf dem Gerät angezeigt. {#alert-message}

Für Warnmeldungen ist mindestens eine Schaltfläche zum Verwerfen erforderlich (der primäre oder sekundäre Dialog sollte eine Aktion zum Verwerfen aufweisen). Andernfalls ist es möglich, die Nachricht zu speichern, sie wird jedoch nicht empfangen.

## Wenn lokale Benachrichtigungen den benutzerdefinierten Ton unter iOS nicht abspielen, wird dann stattdessen der Standardton abgespielt? {#local-notification-sound}

Für einen benutzerdefinierten Ton unter iOS müssen Sie beim Erstellen einer lokalen Benachrichtigung einen Dateinamen mit Erweiterung angeben (z. B. sound.caf). Wenn diese Erweiterung nicht bereitgestellt wird, wird der Standardton verwendet.

## Werden Deeplinks in In-App-Nachrichten unterstützt? {#inapp-deeplinks}

Ja, Deeplinks werden in In-App-Nachrichten unterstützt. Deeplinks sollten Folgendes enthalten:

* Sprache, die besagt, dass das Versand-Tracking deaktiviert werden muss, damit die Deeplinks funktionieren.
* Appsflyer mit Branch als Partner, die das Deeplink-Tracking durchführen können. Weitere Informationen zur Integration von Branch und Adobe Campaign Standard finden Sie auf dieser [Seite](https://help.branch.io/using-branch/docs/adobe-campaign-standard-1).

## Kann eine In-App-Nachricht ausgelöst werden, wenn der Benutzer die App über eine Push-Benachrichtigung startet? {#inapp-push-trigger}

Ja, diese Nachrichten werden auch als Daisy-Chain-Nachrichten bezeichnet. Befolgen Sie die nachstehenden Schritte:

1. Erstellen Sie eine In-App-Nachricht.

1. Definieren Sie ein benutzerdefiniertes Ereignis und wählen Sie es als Ereignis-Trigger für diese In-App-Nachricht aus, beispielsweise &quot;Trigger aus der Herbstvorschau-Push-Benachrichtigung&quot;.

1. Definieren Sie beim Erstellen Ihrer Push-Nachricht eine benutzerdefinierte Variable, deren Wert als Ereignis festgelegt werden kann, das zum Auslösen von In-App-Nachrichten verwendet wird, beispielsweise Schlüssel = &quot;inappkey&quot; und Wert = &quot;Trigger aus der Herbstvorschau-Push-Benachrichtigung&quot;.

1. Implementieren Sie den Ereignis-Trigger im Code der Mobile App wie folgt:

   ![](assets/faq_inapp_2.png)

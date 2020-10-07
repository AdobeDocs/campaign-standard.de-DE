---
title: Häufig gestellte Fragen zur Integration des Adobe Experience Platform SDK und Adobe Campaign
description: Häufig gestellte Fragen zur Integration des Adobe Experience Platform SDK und Adobe Campaign
page-status-flag: never-activated
uuid: 867b1c4b-4c79-4c52-9d0a-ef71993e50a2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 406c955a-b2d2-4099-9918-95f5fa966067
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 100%

---


# Häufig gestellte Fragen zur Integration des Experience Platform SDK {#aep-faq}

Um Push-Benachrichtigungen und In-App-Nachrichten mithilfe der Experience-Platform-SDK-Anwendung zu senden, muss im Adobe Experience Platform SDK eine mobile App eingerichtet und in Adobe Campaign konfiguriert werden.

Im folgenden Abschnitt werden häufig gestellte Fragen zu dieser Synchronisation aufgeführt.

Weitere Informationen zu Push- oder In-App-Benachrichtigungen finden Sie in den folgenden häufig gestellten Fragen:

* [Häufig gestellte Fragen zu Push-Benachrichtigungen](../../channels/using/about-push-notifications.md#push-faq)
* [Häufig gestellte Fragen zu In-App-Nachrichten](../../channels/using/about-in-app-messaging.md#in-app-faq)
* [Häufig gestellte Fragen zur Synchronisierung mit dem technischen Workflows für Launch](../../administration/using/syncwithlaunch-faq.md)

## Nützliche Ressourcen vor dem Start {#resource-mobile-property}

Weitere Informationen zur Integration des Adobe Experience Platform SDK mit Campaign Standard finden Sie in den folgenden Ressourcen:

* Launch/Mobile [Übersichtsvideo](https://www.adobe.com/experience-platform/launch.html#acpl-mobile-video)
* Launch/Mobile [Handbuch mit Tipps und Tricks](https://www.adobe.com/content/dam/www/us/en/experience-platform/launch-tag-manager/pdfs/adobe-cloud-platform-launch-tips-and-tricks-sheet.pdf)

## Ist die Adobe Experience Platform SDK-Integration für sowohl Adobe Campaign Standard als auch Adobe Campaign Classic verfügbar? {#aep-validity}

Ja, die [!DNL Adobe Experience Platform SDK] Integration ist für Adobe Campaign Standard und Adobe Campaign Classic verfügbar. Sie müssen die entsprechende **[!UICONTROL Extension]** über [!DNL Adobe Launch] installieren, um die Integration zu aktivieren.

Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard).

## Welche Funktionen ermöglicht die Adobe Experience Platform SDK-Integration in Adobe Campaign? {#aep-capabilities}

In der folgenden Tabelle finden Sie weitere Informationen zu diesen Funktionen.

![](assets/faq.png)

>[!NOTE]
>
>Die [!DNL Places]-Integration umfasst Ortsereignisse als Auslöser für In-App-Nachrichten (gilt nicht für Push-Benachrichtigungen), wodurch Profile mit [!DNL Places]-Daten und der Unterstützung lokaler Benachrichtigungen angereichert werden. Weitere Informationen finden Sie auf dieser [Seite](../../channels/using/preparing-and-sending-an-in-app-message.md). Die eingeschränkte <br>[!DNL Places]-Integration umfasst die Anreicherung von Profilen mit [!DNL Places]-Daten.

## Welchen Anwendungsfall ermöglicht die Adobe Experience Platform SDK-Integration in Adobe Campaign Standard? {#aep-use-cases}

Die folgenden Anwendungsfälle werden unterstützt:

* **[!UICONTROL Mobiles Profil]** in Campaign erhalten (durch ECID auf der Registerkarte **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL Mobile App (AEP SDK)]** > **[!UICONTROL Abonnenten der Mobile App]** gekennzeichnet)
* **[!UICONTROL Ein mobiles Profil]** in Adobe Campaign anreichern (**[!UICONTROL benutzerdefinierte Ressourcenerweiterung]** der appSubscriberRcp-Tabelle erforderlich)
* Push-Token zum Senden von Push-Nachrichten erhalten (Benutzer muss sich für den Empfang von Push-Nachrichten anmelden)
* Push- und In-App-Nachrichten senden
* Interaktion des Benutzers mit Push- und In-App-Nachrichten tracken und entsprechende Berichte bereitstellen

## Was muss ich tun, um ein mobiles Profil in Campaign zu erhalten? {#mobile-profile-campaign}

Gehen Sie dazu wie folgt vor:

1. Konfigurieren Sie eine **[!UICONTROL mobile Eigenschaft]** in [!DNL Launch].
1. Installieren Sie die Adobe Campaign Standard-Erweiterung. Beachten Sie, dass die Adobe Campaign Standard-Erweiterung auch die **[!UICONTROL Mobile Core]**-, **[!UICONTROL Profil]**- und **[!UICONTROL Lifecycle]**-Erweiterungen erfordert, die standardmäßig in [!DNL Launch] installiert sind.
   * Benutzer sollten den Sitzungs-Timeout in der **[!UICONTROL Mobile Core]**-Erweiterung konfigurieren, was sich auf die Häufigkeit der Lebenszyklusereignisse auswirkt.
   * Sobald die Erweiterung konfiguriert ist, sollten Benutzer mithilfe von Cocoapods für iOS und Gradle für Android entsprechende Abhängigkeiten in der Mobile App hinzufügen. Folgen Sie den Anweisungen [hier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard).
   * Verwenden Sie immer die neuesten Versionen der Bibliotheken.
   * Registrieren Sie die **[!UICONTROL Campaign]**-, **[!UICONTROL UserProfile]**-, **[!UICONTROL Identity]**-, **[!UICONTROL Lifecycle]**- und **[!UICONTROL Signal]**-Erweiterungen in der Mobile App. Folgen Sie den Anweisungen [hier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard#register-the-campaign-standard-extension-with-mobile-core).
   * Nachdem die Erweiterungen registriert sind, starten Sie ACPCore. Stellen Sie für Android sicher, dass Sie setApplication mit onCreate () festlegen. Befolgen Sie der Anleitung zur mobilen Installation für Ihre Eigenschaft für Mobilgeräte in Launch.
   * Die folgenden SDK-APIs sind ebenfalls erforderlich. Implementieren Sie die „Lifecycle Start“- und „Lifecycle Pause“-APIs, wie [hier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle/lifecycle-extension-in-android) für Android und hier für iOS beschrieben.
1. Konfigurieren Sie eine **[!UICONTROL Mobile Property]** in Adobe Campaign Standard. Folgen Sie dem Verfahren [hier](../../administration/using/configuring-a-mobile-application.md#channel-specific-config).

## Was muss ich tun, um ein mobiles Profil in Campaign anzureichern? {#enrich-mobile-profile}

Sie müssen ein CollectPII-Postback konfigurieren (siehe diese [Seite](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#PIIpostback)) und die CollectPII-API vom SDK implementieren (siehe diese [Seite](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#collect-pii)).

## Wie oft sollte ein CollectPII-Aufruf ausgelöst werden? {#collect-pii}

Das Ziel des CollectPII-Aufrufs ist es, das mobile Profil in Campaign anzureichern. Es sollte ausgelöst werden, wenn neue aussagekräftige Informationen vorliegen, die Kunden dem Profil je nach Anwendungsfall und Geschäftsanforderungen hinzufügen möchten.

## Können CollectPII-Aufrufe als Reaktion auf mehrere Trigger-Ereignisse ausgelöst werden? {#collect-pii-calls}

Ja. Je nach Ihren geschäftlichen Anforderungen können Sie CollectPII-Aufrufe als Reaktion auf die Anmeldung des Benutzers in der App, einen Kauf, ein Lebenszyklusereignis oder das Betreten des Benutzers eines Geofence usw. auslösen. Zusammenfassend ist dies eine Benutzerinteraktion mit der App, die Informationen generiert, die Sie für die Anreicherung von Profilen verwenden möchten.

## Kann ich als Reaktion auf alle mobilen Ereignisse CollectPII-Aufrufe auslösen? {#collect-pii-events}

Häufigkeit und Design von CollectPII-Aufrufen sollten von den Geschäftsanforderungen abhängen und nicht blind ausgelöst werden, da dies die DB zusätzlich belastet.

### Wenn ich versuche, auf Adobe Experience Platform-Apps in Campaign oder Launch zuzugreifen, wird manchmal ein Fehler angezeigt, dass die Eigenschaft nicht verfügbar ist. {#aep-error}

Das ist ein bekanntes Problem und tritt aufgrund des Ablaufs des Tokens auf. In diesem Fall sollten Sie sich ab- und wieder anmelden.

## Was wären nützliche Empfehlungen für Ressourcen, um mehr über das Adobe Experience Platform SDK (früher bekannt als SDK V5) zu erfahren?{#resource-aep}

Sehen Sie sich die folgenden Ressourcen an:

* [Dokumentation](https://aep-sdks.gitbook.io/docs/) zum Experience Platform SDK
* [Dokumentation](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property) zu den ersten Schritten mit Launch und dem Experience Platform SDK
* [Dokumentation](https://aep-sdks.gitbook.io/docs/resources/upgrading-to-aep) zur Aktualisierung auf das Experience Platform SDK
* [Dokumentation](https://github.com/Adobe-Marketing-Cloud/acp-sdks/) zum Experience Platform SDK in Github

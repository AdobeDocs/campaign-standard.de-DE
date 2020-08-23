---
title: Häufig gestellte Fragen zur Adobe Experience Platform SDK und Adobe Campaign-Integration
description: Häufig gestellte Fragen zur Adobe Experience Platform SDK und Adobe Campaign-Integration
page-status-flag: never-activated
uuid: 867b1c4b-4c79-4c52-9d0a-ef71993e50a2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 406c955a-b2d2-4099-9918-95f5fa966067
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 762700893c913d9aea884d00438c84b39a800188
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 4%

---


# Häufig gestellte Fragen zur Integration des Experience Platform SDK {#aep-faq}

Um Push-Benachrichtigungen und In-App-Nachrichten mit Experience Platform SDK zu senden, muss eine Mobilanwendung im Adobe Experience Platform SDK eingerichtet und in Adobe Campaign konfiguriert werden.

Im folgenden Abschnitt werden allgemeine Fragen zu dieser Synchronisierung Liste.

Weitere Informationen zu Push oder In-App finden Sie in den folgenden häufig gestellten Fragen:

* [Häufig gestellte Fragen zur Push-Benachrichtigung](../../channels/using/about-push-notifications.md#push-faq)
* [Häufig gestellte Fragen zur In-App](../../channels/using/about-push-notifications.md#in-app-faq)
* [Häufig gestellte Fragen zur Synchronisierung mit dem technischen Arbeitsablauf beim Start](../../administration/using/syncwithlaunch-faq.md)

## Nützliche Ressourcen vor dem Start {#resource-mobile-property}

Weitere Informationen zur Adobe Experience Platform SDK- und Campaign Standard-Integration finden Sie in den nachfolgend aufgeführten Ressourcen:

* Video [über Start/Mobile-Übersicht](https://www.adobe.com/experience-platform/launch.html#acpl-mobile-video)
* Handbuch &quot; [Starts/Handys und Tricks&quot;](https://www.adobe.com/content/dam/www/us/en/experience-platform/launch-tag-manager/pdfs/adobe-cloud-platform-launch-tips-and-tricks-sheet.pdf)

## Ist die Adobe Experience Platform SDK-Integration für Adobe Campaign Standard und Adobe Campaign Classic verfügbar? {#aep-validity}

Ja, die [!DNL Adobe Experience Platform SDK] Integration ist für Adobe Campaign Standard und Adobe Campaign Classic verfügbar. Sie müssen die entsprechende **[!UICONTROL Erweiterung]** über installieren, [!DNL Adobe Launch] um die Integration zu aktivieren.

Weitere Informationen dazu finden Sie auf dieser [Seite](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaignclassic) zum Campaign Classic und auf dieser [Seite](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) zum Campaign Standard.

## Welche Funktionen erleichtert die Adobe Experience Platform SDK-Integration in Adobe Campaign? {#aep-capabilities}

In der folgenden Tabelle finden Sie weitere Informationen zu diesen Funktionen.

![](assets/faq.png)

>[!NOTE]
>
>[!DNL Places] Die Integration umfasst Orte, an denen Ereignis als Auslöser für In-App-Nachrichten (Nicht-App-Nachrichten für Push-Benachrichtigungen) fungieren, wodurch Profil mit Unterstützung für [!DNL Places] Daten und lokale Benachrichtigungen erweitert werden. Weitere Informationen finden Sie auf dieser [Seite](../../channels/using/preparing-and-sending-an-in-app-message.md) . <br>[!DNL Places] Die eingeschränkte Integration umfasst die Anreicherung von Profilen mit [!DNL Places] Daten.

## Welchen Anwendungsfall erleichtert die Adobe Experience Platform SDK-Integration in Adobe Campaign Standard? {#aep-use-cases}

Die folgenden Anwendungsfälle werden unterstützt:

* Erwerben eines **[!UICONTROL mobilen Profils]** in Kampagne (durch ECID gekennzeichnet in **[!UICONTROL Administration]** > **[!UICONTROL Kanal]** > **[!UICONTROL Mobile App (AEP SDK)]** > Registerkarte &quot;Abonnenten **[!UICONTROL von]** Mobilanwendungen&quot;)
* Anreichern eines **[!UICONTROL Mobile-Profils]** in Adobe Campaign ( **[!UICONTROL benutzerdefinierte Ressourcenerweiterung]** der appSubscriberRcp-Tabelle erforderlich)
* Push-Token zum Senden von Push-Nachrichten erwerben (Push-Benachrichtigungen müssen vom Benutzer aktiviert werden, um Push-Nachrichten zu empfangen)
* Push- und In-App-Nachrichten senden
* Verfolgen Sie die Interaktion des Benutzers mit Push- und In-App-Nachrichten und stellen Sie Berichte darüber bereit.

## Was muss ich tun, um ein mobiles Profil in der Kampagne zu erwerben? {#mobile-profile-campaign}

Gehen Sie dazu wie folgt vor:

1. Konfigurieren Sie eine **[!UICONTROL Mobile-Eigenschaft]** in [!DNL Launch].
1. Installieren Sie die Adobe Campaign Standard-Erweiterung. Beachten Sie, dass die Adobe Campaign Standard-Erweiterung auch **[!UICONTROL Mobile Core]**-, **[!UICONTROL Profil]** - und **[!UICONTROL Lebenszykluserweiterungen]** erfordert, die standardmäßig in installiert sind [!DNL Launch].
   * Die Benutzer sollten den Sitzungs-Timeout in der **[!UICONTROL Mobile Core]** Extension konfigurieren, was sich auf die Häufigkeit von LebenszyklusEreignissen auswirkt.
   * Nachdem die Erweiterung konfiguriert wurde, sollten Benutzer der Mobile App entsprechende Abhängigkeiten mit Cocoapods für iOS und Gradle für Android hinzufügen. Folgen Sie den Anweisungen [hier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard).
   * Nehmen Sie immer die neuesten Versionen der Bibliotheken.
   * Registrieren Sie in der Mobile App **[!UICONTROL Kampagne]**, **[!UICONTROL UserProfile]**, **[!UICONTROL Identity]**, **[!UICONTROL Lifecycle]** und **[!UICONTROL Signal]** Extensions. Folgen Sie den Anweisungen [hier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard#register-the-campaign-standard-extension-with-mobile-core).
   * Sobald Erweiterungen registriert sind, Beginn ACPCore. Achten Sie bei Android darauf, onCreate() auf &quot;Application&quot;festzulegen. Befolgen Sie die genauen Anweisungen, die in den Anweisungen zur Mobile-Installation für Ihre Mobile-Eigenschaft beim Start bereitgestellt werden.
   * Die folgenden SDK-APIs sind ebenfalls erforderlich. Implementieren Sie die APIs für den Lebenszyklus-Beginn und die Pause-APIs, wie [hier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle/lifecycle-extension-in-android) für Android und hier für iOS beschrieben.
1. Konfigurieren Sie eine **[!UICONTROL Mobile-Eigenschaft]** in Adobe Campaign Standard. Folgen Sie dem Verfahren [hier](../../administration/using/configuring-a-mobile-application.md#channel-specific-config).

## Was muss ich tun, um ein mobiles Profil in der Kampagne zu bereichern? {#enrich-mobile-profile}

Sie müssen einen CollectPII-Postback konfigurieren (siehe diese [Seite](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#PIIpostback)) und die CollectPII-API aus SDK implementieren (siehe diese [Seite](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#collect-pii)).

## Wie oft sollte ein CollectPII-Aufruf ausgelöst werden? {#collect-pii}

Das Ziel des CollectPII-Aufrufs ist es, das mobile Profil in der Kampagne zu bereichern. Es sollte ausgelöst werden, wenn neue aussagekräftige Informationen vorliegen, die Kunden dem Profil je nach Anwendungsfall und Geschäftsanforderungen hinzufügen möchten.

## Können CollectPII-Aufrufe als Reaktion auf mehrere Auslöser-Ereignis ausgelöst werden? {#collect-pii-calls}

Ja. Je nach Bedarf Ihres Unternehmens können Sie CollectPII-Aufrufe auslösen, wenn Sie sich bei der App anmelden, etwas erwerben oder ein Lebenszyklusprodukt erwerben oder einen Benutzer in eine Geometrie eingeben usw. Zusammenfassend ist dies eine Benutzerinteraktion mit der App, die Informationen generiert, die Sie für die Anreicherung von Profilen verwenden möchten.

## Kann ich als Antwort auf alle mobilen Ereignis CollectPII-Anrufe auslösen? {#collect-pii-events}

Häufigkeit und Design von CollectPII-Aufrufen sollten von geschäftlichen Anforderungen bestimmt werden und sollten nicht blindlings ausgelöst werden, da sie zusätzliche Belastungen für die DB verursachen.

### Wenn ich versuche, auf Adobe Experience Platform-Apps in Kampagne oder Launch zuzugreifen, wird manchmal ein Fehler wegen fehlender Eigenschaft angezeigt. {#aep-error}

Dies ist ein bekanntes Problem, das aufgrund des Ablaufs von Token auftritt. Sie sollten sich ab- und einloggen.

## Was wären nützliche Empfehlungen für Ressourcen, um mehr über Adobe Experience Platform SDK (früher SDK V5) zu erfahren?{#resource-aep}

Sehen Sie sich die folgenden Ressourcen an:

* Experience Platform SDK- [Dokumentation](https://aep-sdks.gitbook.io/docs/)
* Erste Schritte mit der [Dokumentation zum Start- und Experience Platform-SDK](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* Aktualisierung der Experience Platform SDK- [Dokumentation](https://aep-sdks.gitbook.io/docs/resources/upgrading-to-aep)
* Github-Experience Platform-SDK- [Dokumentation](https://github.com/Adobe-Marketing-Cloud/acp-sdks/)

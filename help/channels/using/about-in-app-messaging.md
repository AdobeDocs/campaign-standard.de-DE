---
title: Über In-App-Messaging
seo-title: Über In-App-Messaging
description: Über In-App-Messaging
seo-description: Mit In-App-Messaging können Sie Nachrichten oder Warnhinweise innerhalb einer Mobile App anzeigen.
page-status-flag: never-activated
uuid: 6784cdfc-6db9-41dd-9fbb-2e756a5bcb5f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: in-app-messaging
discoiquuid: a4168cfb-22bf-4ab3-b9d8-6e76e1bdc055
context-tags: delivery,triggers,back
internal: n
snippet: y
translation-type: ht
source-git-commit: 74f037ba618639ab61edfb8311adeb44a7a99ebd

---


# Über In-App-Messaging{#about-in-app-messaging}

In-App-Messaging ist ein Messaging-Kanal, mit dem Sie in einer App eine Nachricht einblenden können, wenn ein Benutzer diese gerade verwendet. Dieser Nachrichtentyp ist eine Ergänzung zu Push-Benachrichtigungen, mit denen Nachrichten direkt an die Benachrichtigungszentrale des Telefons des Benutzers gesendet werden. Weiterführende Informationen zu Push-Benachrichtigungen erhalten Sie in [diesem Abschnitt](../../channels/using/about-push-notifications.md).

Dieser Kanal erfordert die Integration von Mobile Apps mit dem Adobe Experience Platform SDK. Diese Apps müssen in Adobe Experience Platform Launch aktiviert werden, damit sie in Adobe Campaign für In-App-Sendungen verfügbar sind.

![](assets/launch_campaign.png)

Um In-App-Nachrichten mithilfe des Experience Platform SDK über Mobile Apps senden zu können, müssen folgende Voraussetzungen gegeben sein:

1. Sie benötigen in Adobe Campaign Zugriff auf den **[!UICONTROL In-App]**-Kanal. Wenn Sie keinen Zugriff auf diesen Kanal haben, kontaktieren Sie das für Ihr Konto zuständige Team.
1. Definieren Sie in Experience Platform Launch Ihre Mobile App durch die Erstellung einer Mobile-Eigenschaft (Mobile Property) und statten Sie Ihre Mobile App mit dem Experience Platform SDK aus.

   Weiterführende Informationen dazu finden Sie in der Adobe Launch-Dokumentation im Abschnitt [Eine Mobile Property einrichten](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property).

1. Installieren Sie für Ihre Mobile App in Experience Platform Launch die **[!UICONTROL Adobe Campaign Standard]**-Erweiterung:

   Weiterführende Informationen zu Erweiterungen finden Sie im Adobe Experience Platform Launch-Handbuch im Abschnitt zur [Konfiguration der Campaign Standard-Erweiterung in Experience Platform Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard).

1. Weiterführende Informationen zur Konfiguration von Regeln und Datenelementen für Ihre Anwendung in Adobe Experience Platform Launch finden Sie im Abschnitt [Anwendung in Experience Platform Launch konfigurieren](https://helpx.adobe.com/de/campaign/kb/config-app-in-launch.html#Step1Createdataelements).

1. Konfigurieren Sie Ihre Experience Platform Launch-Anwendung in Adobe Campaign Standard. Informationen dazu finden Sie im Abschnitt [Experience Platform Launch-App in Adobe Campaign einrichten](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html#SettingupyourAdobeLaunchapplicationinAdobeCampaign).

Weiterführende Informationen zur Konfiguration von Experience Platform SDKs finden Sie auf dieser [Seite](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html).

**Verwandte Inhalte:**

* [In-App-Nachricht vorbereiten und senden](../../channels/using/preparing-and-sending-an-in-app-message.md)
* [In-App-Nachricht anpassen](../../channels/using/customizing-an-in-app-message.md)
* [Nachricht vom Typ "Lokale Benachrichtigung" anpassen](../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type)
* [In-App-Nachricht in einem Workflow senden](../../automating/using/in-app-delivery.md)
* [FAQ zu Push-Benachrichtigungen und In-App-Nachrichten](https://helpx.adobe.com/de/campaign/kb/push_inapp_faq.html)
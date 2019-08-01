---
title: Über In-App-Messaging
seo-title: Über In-App-Messaging
description: Über In-App-Messaging
seo-description: Mit In-App-Messaging können Sie Nachrichten oder Warnhinweise innerhalb einer Mobile App anzeigen.
page-status-flag: nie aktiviert
uuid: 6784 cdfc -6 db 9-41 dd -9 fbb -2 e 756 a 5 bcb 5 f
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Kanäle
content-type: Referenz
topic-tags: In-App-Nachrichten
discoiquuid: a 4168 cfb -22 bf -4 ab 3-b 9 d 8-6 e 76 e 1 bdc 55
context-tags: Bereitstellung, Auslöser, zurück
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 74f037ba618639ab61edfb8311adeb44a7a99ebd

---


# Über In-App-Messaging{#about-in-app-messaging}

In-App-Messaging ist ein Messaging-Kanal, mit dem Sie in einer App eine Nachricht einblenden können, wenn ein Benutzer diese gerade verwendet. Dieser Nachrichtentyp ist eine Ergänzung zu Push-Benachrichtigungen, mit denen Nachrichten direkt an die Benachrichtigungszentrale des Telefons des Benutzers gesendet werden. Weiterführende Informationen zu Push-Benachrichtigungen erhalten Sie in [diesem Abschnitt](../../channels/using/about-push-notifications.md).

Dieser Kanal erfordert die Integration von Mobile Apps mit dem Adobe Experience Platform SDK. Diese Apps müssen in Adobe Experience Platform Launch aktiviert werden, bevor sie in Adobe Campaign für In-App-Lieferungen verfügbar sind.

![](assets/launch_campaign.png)

Um In-App-Nachrichten mithilfe des Experience Platform SDK über Mobile Apps senden zu können, müssen folgende Voraussetzungen gegeben sein:

1. Sie benötigen in Adobe Campaign Zugriff auf den **[!UICONTROL In-App]-Kanal.** Wenn Sie keinen Zugriff auf diesen Kanal haben, kontaktieren Sie das für Ihr Konto zuständige Team.
1. Erstellen Sie im Experience Platform Launch die Mobilanwendung, indem Sie eine Mobilanwendung erstellen und die mobile App mit Experience Platform SDK instrumentieren.

   Weiterführende Informationen dazu finden Sie in der Adobe Launch-Dokumentation im Abschnitt [Eine Mobile Property einrichten](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property).

1. In Experience Platform Launch, install the **[!UICONTROL Adobe Campaign Standard]** extension for your mobile application in Experience Platform Launch:

   For more on extensions, refer to the [Configure Campaign Standard Extension in Experience Platform Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) in Experience Platform Launch documentation.

1. In Experience Platform Launch, configure rules and data elements for your application, see [Configuring your application in Experience Platform Launch](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#Step1Createdataelements)

1. Configure your Experience Platform Launch application in Adobe Campaign Standard, see [Setting up your Experience Platform Launch application in Adobe Campaign](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#SettingupyourAdobeLaunchapplicationinAdobeCampaign) .

Weiterführende Informationen zur Konfiguration von Experience Platform SDKs finden Sie auf dieser [Seite](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

**Verwandte Inhalte:**

* [In-App-Nachricht vorbereiten und senden](../../channels/using/preparing-and-sending-an-in-app-message.md)
* [In-App-Nachricht anpassen](../../channels/using/customizing-an-in-app-message.md)
* [Nachricht vom Typ "Lokale Benachrichtigung" anpassen](../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type)
* [In-App-Nachricht in einem Workflow senden](../../automating/using/in-app-delivery.md)
* [Push- und In-App-häufig gestellte Fragen](https://helpx.adobe.com/campaign/kb/push_inapp_faq.html)
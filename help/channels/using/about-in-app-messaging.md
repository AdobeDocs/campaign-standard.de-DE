---
title: Über In-App-Messaging
description: Mit In-App-Messaging können Sie Nachrichten oder Warnhinweise innerhalb einer Mobile App anzeigen.
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
source-git-commit: 501ba6f97a86076116d4d84f43df674536e12f6a

---


# Über In-App-Messaging{#about-in-app-messaging}

In-App-Messaging ist ein Messaging-Kanal, mit dem Sie in einer App eine Nachricht einblenden können, wenn ein Benutzer diese gerade verwendet. Dieser Nachrichtentyp ist eine Ergänzung zu Push-Benachrichtigungen, mit denen Nachrichten direkt an die Benachrichtigungszentrale des Telefons des Benutzers gesendet werden. Weiterführende Informationen zu Push-Benachrichtigungen erhalten Sie in [diesem Abschnitt](../../channels/using/about-push-notifications.md).

Dieser Kanal erfordert die Integration von Mobile Apps mit dem Adobe Experience Platform SDK. Diese Apps müssen in Adobe Experience Platform Launch aktiviert werden, damit sie in Adobe Campaign für In-App-Sendungen verfügbar sind.

![](assets/launch_campaign.png)

Um In-App-Nachrichten mithilfe des Experience Platform SDK über Mobile Apps senden zu können, müssen folgende Voraussetzungen gegeben sein:

1. Sie benötigen in Adobe Campaign Zugriff auf den **[!UICONTROL In-App]**-Kanal. Wenn Sie keinen Zugriff auf diesen Kanal haben, kontaktieren Sie das für Ihr Konto zuständige Team.

1. Anwendungsfälle für Mobilgeräte, die in Adobe Campaign Standard in Kombination mit einer Experience Cloud SDK-Applikation unterstützt werden, erfordern eine in Adobe Experience Platform Launch erstellte und in Adobe Campaign Standard konfigurierte App. Eine Schritt-für-Schritt-Anleitung hierzu finden Sie auf dieser [Seite](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html).

1. Nach der Konfiguration können Sie Ihre In-App-Nachricht vorbereiten. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../channels/using/preparing-and-sending-an-in-app-message.md#preparing-your-in-app-message).

1. Im Anschluss daran bestimmen Sie noch, ob Sie eine [In-App-Nachricht](../../channels/using/customizing-an-in-app-message.md) versenden oder eine [Nachricht vom Typ &quot;Lokale Benachrichtigung&quot; anpassen](../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type) möchten.

1. Ihre Nachricht ist jetzt bereit für den Versand. Weiterführende Informationen finden Sie auf dieser [Seite](../../channels/using/preparing-and-sending-an-in-app-message.md#sending-your-in-app-message).

**Verwandte Inhalte:**

* [In-App-Bericht](../../reporting/using/in-app-report.md)
* [Häufig gestellte Fragen zu Push- und In-App-Nachrichten](https://helpx.adobe.com/de/campaign/kb/push_inapp_faq.html)
* [Unterstützte Anwendungsfälle für Mobilgeräte in Adobe Campaign Standard](https://helpx.adobe.com/de/campaign/kb/configure-launch-rules-acs-use-cases.html)
* [Handbuch zu Campaign Standard Mobile](https://helpx.adobe.com/de/campaign/kb/acs-mobile.html)

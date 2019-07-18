---
title: Über Push-Benachrichtigungen
seo-title: Über Push-Benachrichtigungen
description: Über Push-Benachrichtigungen
seo-description: Hier erhalten Sie die wichtigsten Informationen zum Push-Benachrichtigungskanal in Adobe Campaign.
page-status-flag: nie aktiviert
uuid: 961 aaeb 5-6948-4 fd 2-b 8 d 7-de 4510 c 10566
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Kanäle
content-type: Referenz
topic-tags: push-notifications
discoiquuid: 23 b 4212 e-e 878-4922-be 20-50 fb 7 fa 88 ae 8
context-tags: Mobileapp, overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 80e65c3fedc5452105c296144a683948daa69150

---


# Über Push-Benachrichtigungen{#about-push-notifications}

>[!CAUTION]
>
>Die Implementierung der Push-Benachrichtigung muss von Experten durchgeführt werden. Wenn Sie Hilfe brauchen, kontaktieren Sie bitte Ihren Adobe-Kundenbetreuer oder Professional Services-Partner. Push-Benachrichtigungen sind eine optionale Funktion. Bitte prüfen Sie Ihren Lizenzvertrag und kontaktieren Sie den Ansprechpartner für Ihr Konto, um diese Funktion zu aktivieren.

Sie können mit Adobe Campaign personalisierte und zielgruppenspezifische Push-Benachrichtigungen an iOS- und Android-Mobilgeräte versenden.

Diese Nachrichten werden auf Mobile Apps empfangen, die in Adobe Campaign unter Verwendung des Experience Cloud Mobile SDK V4 oder Experience Platform SDK eingerichtet werden. Weiterführende Informationen dazu finden Sie unter [Eine Mobile App mit SDK V4 konfigurieren](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html) und [Eine Mobile App mit Adobe Experience Platform SDKs konfigurieren](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

In Adobe Campaign sind Attribute zu mobilen Profilen, die von Mobilgeräten gesendet werden, in der Ressource **[!UICONTROL App-Abonnements (appSubscriptionRcp)]** gespeichert. Dort können die Daten definiert werden, die über die Abonnenten Ihrer Apps gesammelt werden sollen.

Diese Ressource muss erweitert werden, damit die gewünschten, vom Mobilgerät an Adobe Campaign gesendeten Daten gesammelt werden. Eine detaillierte Anleitung dazu finden Sie auf dieser [Seite](../../developing/using/extending-the-subscriptions-to-an-application-resource.md).

In Adobe Campaign sind zwei Arten von Push-Benachrichtigungen verfügbar:

* **[!UICONTROL Mit Benachrichtigungen vom Typ Warnung/Nachricht und Badge]** können Sie standardmäßige textbasierte Nachrichten mit zusätzlichem Inhalt versenden (Ton, Badge, Deeplink etc.), die Sie im Abschnitt **[!UICONTROL Erweiterte Optionen]definieren können.**

   Diese Benachrichtigungstyp ermöglicht es Ihnen, einen Titel und eine Nachricht hinzuzufügen, in denen Sie Personalisierungsfelder verwenden können. Zum Personalisieren der Nachricht muss die Vorlage **[!UICONTROL Push-Benachrichtigungs-Versand (bezogen auf Profile)]ausgewählt sein.**

* **[!UICONTROL Benachrichtigungen vom Typ Stilles Pushen]** werden verwendet, um die Anwendung still zu informieren, ohne dass der Benutzer eine Nachricht oder einen Inhalt erhält. Ein typisches Anwendungsbeispiel für diese Art von Nachricht wäre, die Anwendung darauf hinzuweisen, dass auf dem Server Inhalt zum Herunterladen bereitsteht.

Mithilfe bestimmter Konfigurationen kann das Verhalten von Benachrichtigungen gesteuert werden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../channels/using/customizing-a-push-notification.md).

Erfahrene Benutzer, die diese Konfigurationen definieren möchten, finden weiterführende Informationen in den [Technotes](https://helpx.adobe.com/campaign/kb/acs-article-list.html) zu Mobile Apps.

>[!NOTE]
>
>Datenschutzgesetze sind von Land zu Land unterschiedlich. In manchen Ländern ist es vorgeschrieben, die Benutzer Ihrer Apps über die Art der erhobenen Daten zu unterrichten. Erkundigen Sie sich bitte über die in Ihrem Land für Mobile Apps gültigen Gesetze. Stellen Sie sicher, dass die an Mobile Apps gesendeten Push-Benachrichtigungen den von Apple (Apple Push Notification Service) und Google (Google Cloud Messaging oder Firebase Cloud Messaging) vorgegebenen Voraussetzungen und Bedingungen entsprechen.

**Verwandte Inhalte:**

* [Push-Benachrichtigung vorbereiten und senden](../../channels/using/preparing-and-sending-a-push-notification.md)
* [Mehrsprachige Push-Benachrichtigungen erstellen](../../channels/using/creating-a-multilingual-push-notification.md)
* [Push-Benachrichtigungen in einem Workflow versenden](../../automating/using/push-notification-delivery.md)
* [Push- und In-App-häufig gestellte Fragen](https://helpx.adobe.com/campaign/kb/push_inapp_faq.html)

## Voraussetzungen {#prerequisites}

>[!NOTE]
>Um die Funktion für Push-Benachrichtigungen aus Kampagne nutzen zu können, müssen Sie ein gültiges Push-Zertifikat im PEM-Format ohne Kennwörter bereitstellen.
Wenn Sie über ein gültiges p 12-Zertifikat verfügen, können Sie es mithilfe von Online-Ressourcen einfach in eine. pem-Datei konvertieren.

Um mit dem Versand von Push-Benachrichtigungen zu beginnen, müssen Sie zuerst Ihre Mobile App mithilfe von SDK V4 konfigurieren: Sie können Ihre Mobile App mithilfe von Experience Platform SDKs konfigurieren. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

Vor dem Versand Ihrer Push-Benachrichtigungen sollten Sie auf Folgendes achten:

1. Stellen Sie sicher, dass Sie auf den **[!UICONTROL Mobile App]-Kanal in Adobe Campaign zugreifen können.**
1. Konfigurieren Sie Ihre Mobile App:

   * Adobe Campaign
   * in der Adobe-Mobile-Services-Benutzeroberfläche

1. Richten Sie die Mobile App ein:

   * Verpacken Sie die von der Adobe-Mobile-Services-Benutzeroberfläche heruntergeladene Konfigurationsdatei mit der Mobile App.
   * Integrieren Sie das Experience Cloud Mobile SDK in Ihre Mobile App.

1. Definieren Sie die Daten, die Sie über die Abonnenten Ihrer App abrufen möchten. Die Abonnenten der Mobile App, deren Profil in der Datenbank von Adobe Campaign gespeichert ist, werden entsprechend den von Ihnen definierten Kriterien abgeglichen.

Nach der Konfiguration Ihrer Mobile App können Sie damit beginnen, Ihre In-App-Nachrichten vorzubereiten und zu versenden. Weiterführende Informationen dazu finden Sie im Abschnitt [Push-Benachrichtigung vorbereiten und senden](../../channels/using/preparing-and-sending-a-push-notification.md).

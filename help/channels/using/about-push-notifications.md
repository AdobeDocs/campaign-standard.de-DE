---
title: Über Push-Benachrichtigungen
description: Hier erhalten Sie die wichtigsten Informationen zum Push-Benachrichtigungskanal in Adobe Campaign.
page-status-flag: never-activated
uuid: 961aaeb5-6948-4fd2-b8d7-de4510c10566
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
discoiquuid: 23b4212e-e878-4922-be20-50fb7fa88ae8
context-tags: mobileApp,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

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

* **[!UICONTROL Mit Benachrichtigungen vom Typ Warnung/Nachricht und Badge]** können Sie standardmäßige textbasierte Nachrichten mit zusätzlichem Inhalt versenden (Ton, Badge, Deeplink etc.), die Sie im Abschnitt **[!UICONTROL Erweiterte Optionen]** definieren können.

   Diese Benachrichtigungstyp ermöglicht es Ihnen, einen Titel und eine Nachricht hinzuzufügen, in denen Sie Personalisierungsfelder verwenden können. Zum Personalisieren der Nachricht muss die Vorlage **[!UICONTROL Push-Benachrichtigungs-Versand (bezogen auf Profile)]** ausgewählt sein.

* **[!UICONTROL Benachrichtigungen vom Typ Stilles Pushen]** werden verwendet, um die Anwendung still zu informieren, ohne dass der Benutzer eine Nachricht oder einen Inhalt erhält. Ein typisches Anwendungsbeispiel für diese Art von Nachricht wäre, die Anwendung darauf hinzuweisen, dass auf dem Server Inhalt zum Herunterladen bereitsteht.

Mithilfe bestimmter Konfigurationen kann das Verhalten von Benachrichtigungen gesteuert werden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../channels/using/customizing-a-push-notification.md).

Erfahrene Benutzer, die diese Konfigurationen definieren möchten, finden weiterführende Informationen in den [Technotes](https://helpx.adobe.com/campaign/kb/acs-article-list.html) zu Mobile Apps.

>[!NOTE]
>
>Datenschutzgesetze sind von Land zu Land unterschiedlich. In manchen Ländern ist es vorgeschrieben, die Benutzer Ihrer Apps über die Art der erhobenen Daten zu unterrichten. Erkundigen Sie sich bitte über die in Ihrem Land für Mobile Apps gültigen Gesetze. Stellen Sie sicher, dass die an Mobile Apps gesendeten Push-Benachrichtigungen den von Apple (Apple Push Notification Service) und Google (Google Cloud Messaging oder Firebase Cloud Messaging) vorgegebenen Voraussetzungen und Bedingungen entsprechen.

**Verwandte Inhalte:**

* [Push-Benachrichtigung vorbereiten und senden](../../channels/using/preparing-and-sending-a-push-notification.md)
* [Mehrsprachige Push-Benachrichtigungen erstellen](../../channels/using/creating-a-multilingual-push-notification.md)
* [Bericht zu Push-Benachrichtigungen](../../reporting/using/push-notification-report.md)
* [Häufig gestellte Fragen zu Push und In-App](https://helpx.adobe.com/campaign/kb/push_inapp_faq.html)

## Voraussetzungen {#prerequisites}

>[!NOTE]
>Um die Funktion für Push-Benachrichtigungen in Campaign zu nutzen, benötigen Sie ein gültiges Push-Zertifikat im PEM-Format ohne Passwörter.
Wenn Sie über ein gültiges p12-Zertifikat verfügen, können Sie es mithilfe von Online-Ressourcen einfach in eine PEM-Datei konvertieren.

Um mit dem Versand von Push-Benachrichtigungen zu beginnen, müssen Sie zuerst Ihre Mobile App mithilfe von SDK V4 konfigurieren: Sie können Ihre Mobile App mithilfe von Experience Platform SDKs konfigurieren. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html).

Vor dem Versand Ihrer Push-Benachrichtigungen sollten Sie auf Folgendes achten:

1. Stellen Sie sicher, dass Sie auf den **[!UICONTROL Mobile App]**-Kanal in Adobe Campaign zugreifen können.
1. Konfigurieren Sie Ihre Mobile App:

   * Adobe Campaign
   * in der Adobe-Mobile-Services-Benutzeroberfläche

1. Richten Sie die Mobile App ein:

   * Verpacken Sie die von der Adobe-Mobile-Services-Benutzeroberfläche heruntergeladene Konfigurationsdatei mit der Mobile App.
   * Integrieren Sie das Experience Cloud Mobile SDK in Ihre Mobile App.

1. Definieren Sie die Daten, die Sie über die Abonnenten Ihrer App abrufen möchten. Die Abonnenten der Mobile App, deren Profil in der Datenbank von Adobe Campaign gespeichert ist, werden entsprechend den von Ihnen definierten Kriterien abgeglichen.

Nach der Konfiguration Ihrer Mobile App können Sie damit beginnen, Ihre In-App-Nachrichten vorzubereiten und zu versenden. Weiterführende Informationen dazu finden Sie im Abschnitt [Push-Benachrichtigung vorbereiten und senden](../../channels/using/preparing-and-sending-a-push-notification.md).

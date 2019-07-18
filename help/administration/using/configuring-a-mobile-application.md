---
title: Mobile App konfigurieren
seo-title: Mobile App konfigurieren
description: Mobile App konfigurieren
seo-description: Hier erfahren Sie, wie Adobe Campaign konfiguriert werden muss, damit Push-Benachrichtigungen oder In-App-Nachrichten unter Verwendung von SDK V4 oder Experience Platform SDK gesendet werden können.
page-status-flag: nie aktiviert
uuid: 63 e 1476 a -7875-4 f 48-ba 9 e -97 f 1 a 0007 e 42
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Administration
content-type: Referenz
topic-tags: configuring-channels
discoiquuid: 2 a 14500 f -5 ede -4131-8 b 1 a-b 7 fd 65 b 7 e 3 aa
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4d148014d1b90712e78b8af17d7ddee2659329ed

---


# Mobile App konfigurieren{#configuring-a-mobile-application}

Push-Benachrichtigungen oder In-App-Nachrichten werden bei mobilen Anwendungen empfangen, die je nach dem zu verwendenden Kanal zuerst in Adobe Mobile Services konfiguriert werden müssen.

* Um In-App-Nachrichten und Push-Benachrichtigungen zu senden, müssen Ihre mobilen Anwendungen in Adobe Campaign eingerichtet werden, indem Sie Adobe Experience Platform sdks nutzen. See [Using Adobe Experience Platform SDK](#using-adobe-experience-platform-sdk).

* Um nur Push-Benachrichtigungen zu senden, können Sie die Integration zwischen Adobe Campaign und Adobe Mobile Service mithilfe von SDK V 4 konfigurieren. See [Using SDK V4](#using-sdk-v4).

After your mobile applications are set up in Adobe Campaign by leveraging the Experience Cloud Mobile SDK V4 or Experience Platform SDK, they need to be configured by an administrator under the [!UICONTROL Administration] &gt; [!UICONTROL Channels] &gt; [!UICONTROL Mobile app] menu.

>[!CAUTION]
>
>Push-Benachrichtigungen und In-App-Implementierungen müssen von Expertenbenutzern durchgeführt werden. Wenn Sie Hilfe brauchen, kontaktieren Sie bitte Ihren Adobe-Kundenbetreuer oder Professional Services-Partner.

## Adobe Experience Platform SDK verwenden {#using-adobe-experience-platform-sdk}

Um Push-Benachrichtigungen und In-App-Nachrichten mit Experience Platform SDK-Anwendungen zu senden, muss eine Mobilanwendung in Adobe Experience Platform Experience Platform Experience Platform Starten und konfiguriert in Adobe Campaign eingerichtet werden. Eine detaillierte Anleitung zur Konfiguration einer Mobile App mithilfe des Experience Platform SDK finden Sie auf dieser [Seite](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html).

Führen Sie zur Konfiguration die folgenden Schritte aus:

1. Stellen Sie sicher, dass Sie Zugriff auf die folgenden **[!UICONTROL Mobile]-Kanäle haben: Push-Benachrichtigung und In-App-Nachricht in Adobe Campaign.** Falls nicht, wenden Sie sich an Ihr Konto.

   ![](assets/launch_1.png)

1. Erstellen Sie die Mobilanwendung im Experience Platform Launch, indem Sie eine Eigenschaft des Mobile-Typs erstellen. For more info, refer to the [Experience Platform Launch](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-new-mobile-property) documentation.
1. Install the **[!UICONTROL Adobe Campaign (Beta)]** extension for your mobile application in Experience Platform Launch:

   For more information on extensions, refer to the [Experience Platform Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard-beta) documentation.

1. Konfigurieren Sie in Adobe Launch Regeln für Ihre Anwendung. Informationen dazu finden Sie im Abschnitt [Anwendung in Adobe Launch konfigurieren](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#ConfiguringyourapplicationinLaunch).
1. Konfigurieren Sie Ihre Adobe-Launch-Anwendung in Adobe Campaign Standard. Informationen dazu finden Sie im Abschnitt [Adobe-Launch-App in Adobe Campaign einrichten](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#SettingupyourAdobeLaunchapplicationinAdobeCampaign).
1. Fügen Sie zu Ihrer Mobile App eine kanalspezifische Konfiguration hinzu. Informationen dazu finden Sie im Abschnitt [Kanalspezifische Anwendungskonfiguration in Adobe Campaign](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#ChannelspecificapplicationconfigurationinAdobeCampaign).

   ![](assets/launch_2.png)

## SDK V4 verwenden {#using-sdk-v4}

Im Gegensatz zu In-App-Nachrichten werden Push-Benachrichtigungen von SDK V4 und Adobe Experience Platform SDKs unterstützt. Eine detaillierte Anleitung zur Verwendung von Push-Benachrichtigungen mit einer Mobile App finden Sie auf dieser [Seite](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html).

Mobile Apps, über die Push-Benachrichtigungen empfangen werden, müssen von einem Administrator in der Adobe-Campaign-Benutzeroberfläche konfiguriert werden. Durch die Konfiguration von sowohl Adobe Campaign als auch Adobe Mobile Services können Sie die Daten Ihrer Mobile Apps für Ihre Kampagnen verwenden.

Für den Versand von Push-Benachrichtigungen müssen folgende Voraussetzungen gegeben sein:

1. Stellen Sie sicher, dass Sie auf den **[!UICONTROL Mobile App]-Kanal in Adobe Campaign zugreifen können.**
1. Konfigurieren Sie Ihre Mobile App:

   * [Adobe Campaign](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html#SettingupamobileapplicationinAdobeCampaign).
   * [Adobe Mobile Services](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html#ConfiguringamobileapplicationinAdobeMobileServices).

1. Richten Sie die Mobile App ein:

   * Verpacken Sie die von der Adobe-Mobile-Services-Benutzeroberfläche heruntergeladene Konfigurationsdatei mit der Mobile App.
   * Integrieren Sie das Experience Cloud Mobile SDK in Ihre Mobile App.

1. Definieren Sie die Daten, die Sie über die Abonnenten Ihrer App abrufen möchten. Die Abonnenten der Mobile App, deren Profil in der Datenbank von Adobe Campaign gespeichert ist, werden entsprechend den von Ihnen definierten Kriterien abgeglichen.

   Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html#Collectingsubscribersdatafromamobileapplication) .

1. Stellen Sie sicher, dass die Einrichtung erfolgreich abgeschlossen wurde. Starten Sie zu diesem Zweck Ihre Mobile App auf Ihrem Gerät und melden Sie sich an. Aktivieren Sie dabei den Empfang von Benachrichtigungen.
1. Then, in Adobe Campaign's advanced menu, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Mobile app]**.
1. Wählen Sie Ihre Mobile App aus der Liste aus, um ihre Eigenschaften anzuzeigen. Ihre Abonnementinformationen werden unter der Liste der Abonnenten aufgeführt.

   ![](assets/push_notif_mobile_app.png)

1. Um die Mobile Apps zu prüfen, für die sich ein Profil angemeldet hat, wählen Sie im Menü **[!UICONTROL Profile &amp; Audiences &gt; Profile]** ein Profil aus und verwenden Sie rechts die Schaltfläche **Profileigenschaften bearbeiten.** Die Mobile Apps werden im Tab **[!UICONTROL Mobile-App-Anmeldungen]aufgeführt.**

   ![](assets/push_notif_subscriptions.png)

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
source-git-commit: 8111dfd2fd3cf254f73d0b01917d606b0a70aa84

---


# Über Push-Benachrichtigungen{#about-push-notifications}

>[!CAUTION]
>
>Die Implementierung der Push-Benachrichtigung muss von Experten durchgeführt werden. Wenn Sie Hilfe brauchen, kontaktieren Sie bitte Ihren Adobe-Kundenbetreuer oder Professional Services-Partner. Push-Benachrichtigungen sind eine optionale Funktion. Bitte prüfen Sie Ihren Lizenzvertrag und kontaktieren Sie den Ansprechpartner für Ihr Konto, um diese Funktion zu aktivieren.

Sie können mit Adobe Campaign personalisierte und zielgruppenspezifische Push-Benachrichtigungen an iOS- und Android-Mobilgeräte versenden.

Diese Meldungen werden in Mobilanwendungen empfangen, die Sie in Adobe Campaign mithilfe des Experience Platform SDK eingerichtet haben. For more information on this, refer to [Configuring a mobile application using Adobe Experience Platform SDKs](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html).

In Adobe Campaign, mobile profile attributes data sent from mobile device are stored in **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** resource which allows you to define the data that you want to collect from your applications&#39; subscribers.

Diese Ressource muss erweitert werden, damit die gewünschten, vom Mobilgerät an Adobe Campaign gesendeten Daten gesammelt werden. Eine detaillierte Anleitung dazu finden Sie auf dieser [Seite](../../developing/using/extending-the-subscriptions-to-an-application-resource.md).

In Adobe Campaign sind zwei Arten von Push-Benachrichtigungen verfügbar:

* **[!UICONTROL Alert/Message/Badge]** Mit Typbenachrichtigungen können Sie textbasierte Standardmeldungen mit zusätzlichen Inhalten (Ton, Abzeichen, DeepLink usw.) senden. , die Sie im **[!UICONTROL Advanced options]** Abschnitt definieren können.

   Diese Benachrichtigungstypen ermöglichen es Ihnen, einen Titel und eine Nachricht hinzuzufügen, in denen Sie Personalisierungsfelder verwenden können. To be able to personalize your message, make sure you select the **[!UICONTROL Send push on profiles]** template.

* **[!UICONTROL Silent push]** Mit Typbenachrichtigungen wird die Anwendung ohne Meldung oder Inhalt für den Endbenutzer automatisch benachrichtigt. Ein typisches Anwendungsbeispiel für diese Art von Nachricht wäre, die Anwendung darauf hinzuweisen, dass auf dem Server Inhalt zum Herunterladen bereitsteht.

Mithilfe bestimmter Konfigurationen kann das Verhalten von Benachrichtigungen gesteuert werden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../channels/using/customizing-a-push-notification.md).

Erfahrene Benutzer, die diese Konfigurationen definieren möchten, finden weiterführende Informationen in den [Technotes](https://helpx.adobe.com/de/campaign/kb/acs-article-list.html) zu Mobile Apps.

>[!NOTE]
>
>Datenschutzgesetze sind von Land zu Land unterschiedlich. In manchen Ländern ist es vorgeschrieben, die Benutzer Ihrer Apps über die Art der erhobenen Daten zu unterrichten. Erkundigen Sie sich bitte über die in Ihrem Land für Mobile Apps gültigen Gesetze. Stellen Sie sicher, dass die an Mobile Apps gesendeten Push-Benachrichtigungen den von Apple (Apple Push Notification Service) und Google (Google Cloud Messaging oder Firebase Cloud Messaging) vorgegebenen Voraussetzungen und Bedingungen entsprechen.

**Verwandte Inhalte:**

* [Push-Benachrichtigung vorbereiten und senden](../../channels/using/preparing-and-sending-a-push-notification.md)
* [Mehrsprachige Push-Benachrichtigungen erstellen](../../channels/using/creating-a-multilingual-push-notification.md)
* [Bericht zu Push-Benachrichtigungen](../../reporting/using/push-notification-report.md)
* [Handbuch zu Campaign Standard Mobile](https://helpx.adobe.com/de/campaign/kb/acs-mobile.html)

## Voraussetzungen {#prerequisites}

>[!NOTE]
>Um die Funktion für Push-Benachrichtigungen in Campaign zu nutzen, benötigen Sie ein gültiges Push-Zertifikat im PEM-Format ohne Passwörter. Wenn Sie über ein gültiges p12-Zertifikat verfügen, können Sie es mithilfe von Online-Ressourcen einfach in eine PEM-Datei konvertieren.

Vor dem Versand Ihrer Push-Benachrichtigungen sollten Sie auf Folgendes achten:

1. Sie benötigen in Adobe Campaign Zugriff auf den **[!UICONTROL Push notification]**-Kanal. Wenn Sie keinen Zugriff auf diesen Kanal haben, kontaktieren Sie das für Ihr Konto zuständige Team.

1. Vergewissern Sie sich, dass Ihr Benutzer über die erforderlichen Berechtigungen in Adobe Campaign Standard und Experience Platform Launch verfügt.

1. Erstellen Sie in Experience Platform Launch eine mobile Eigenschaft. Weitere Informationen finden Sie unter [Einrichten einer mobilen Eigenschaft](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property).

1. Installieren Sie die **[!UICONTROL Adobe Campaign Standard]** Erweiterung in Experience Platform Launch.

1. Konfigurieren Sie in Adobe Campaign Standard die mobile Eigenschaft, die Sie in Experience Platform Launch erstellt haben. Weitere Informationen finden Sie unter [Einrichten der Experience Platform Launch-Anwendung in Adobe Campaign](https://helpx.adobe.com/campaign/kb/configuring-app-sdk.html#SettingupyourAdobeExperiencePlatformLaunchapplicationinAdobeCampaign).

1. Hinzufügen Sie die Kanal-spezifische Konfiguration für Ihre Mobilanwendung einrichten. Weitere Informationen finden Sie unter Anwendungskonfiguration für [Kanal in Adobe Campaign](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html#ChannelspecificapplicationconfigurationinAdobeCampaign).

1. Informationen zur Unterstützung von Fallimplementierungen für Mobilgeräte finden Sie in den ausführlichen Anweisungen zu Erweiterungen, Experience Platform Launch-Regeln und der SDK-Implementierung in [Mobile-Anwendungsfällen, die in Adobe Campaign Standard mithilfe der Adobe Experience Platform SDKs](https://helpx.adobe.com/de/campaign/kb/configure-launch-rules-acs-use-cases.html)unterstützt werden.
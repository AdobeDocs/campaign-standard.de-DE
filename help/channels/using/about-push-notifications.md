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
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '1301'
ht-degree: 100%

---


# Über Push-Benachrichtigungen{#about-push-notifications}

>[!CAUTION]
>
>Die Implementierung der Push-Benachrichtigung muss von Experten durchgeführt werden. Wenn Sie Hilfe brauchen, kontaktieren Sie bitte Ihren Adobe-Kundenbetreuer oder Professional Services-Partner. Push-Benachrichtigungen sind eine optionale Funktion. Bitte prüfen Sie Ihren Lizenzvertrag und kontaktieren Sie den Ansprechpartner für Ihr Konto, um diese Funktion zu aktivieren.

Sie können mit Adobe Campaign personalisierte und zielgruppenspezifische Push-Benachrichtigungen an iOS- und Android-Mobilgeräte versenden.

Diese Nachrichten werden in Mobile Apps empfangen, die in Adobe Campaign unter Verwendung des Experience Platform SDK eingerichtet wurden. Weiterführende Informationen dazu finden Sie im Abschnitt [Konfiguration einer Mobile App mithilfe von Experience Platform SDKs](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html).

In Adobe Campaign sind Attribute zu mobilen Profilen, die von Mobilgeräten gesendet werden, in der Ressource **[!UICONTROL App-Abonnements (appSubscriptionRcp)]** gespeichert. Dort können die Daten definiert werden, die über die Abonnenten Ihrer Apps gesammelt werden sollen.

Diese Ressource muss erweitert werden, damit die gewünschten, vom Mobilgerät an Adobe Campaign gesendeten Daten gesammelt werden. Eine detaillierte Anleitung dazu finden Sie auf dieser [Seite](../../developing/using/extending-the-subscriptions-to-an-application-resource.md).

In Adobe Campaign sind zwei Arten von Push-Benachrichtigungen verfügbar:

* Mit Benachrichtigungen vom Typ **[!UICONTROL Warnung/Nachricht/Badge]** können Sie standardmäßige textbasierte Nachrichten mit zusätzlichem Inhalt versenden (Ton, Badge, Deeplink usw.), die Sie im Abschnitt **[!UICONTROL Erweiterte Optionen]** definieren können.

   Diese Benachrichtigungstypen ermöglichen es Ihnen, einen Titel und eine Nachricht hinzuzufügen, in denen Sie Personalisierungsfelder verwenden können. Zum Personalisieren der Nachricht muss die Vorlage **[!UICONTROL Push-Benachrichtigung für Profile senden]** ausgewählt sein.

* Benachrichtigungen vom Typ **[!UICONTROL Stilles Pushen]** werden verwendet, um die Anwendung still zu informieren, ohne dass der Benutzer eine Nachricht oder einen Inhalt erhält. Ein typisches Anwendungsbeispiel für diese Art von Nachricht wäre, die Anwendung darauf hinzuweisen, dass auf dem Server Inhalt zum Herunterladen bereitsteht.

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
>Um die Funktion für Push-Benachrichtigungen in Campaign zu nutzen, benötigen Sie ein gültiges Push-Zertifikat im PEM-Format ohne Passwörter. 
>
>Wenn Sie über ein gültiges p12-Zertifikat verfügen, können Sie es mithilfe von Online-Ressourcen einfach in eine PEM-Datei konvertieren.

Vor dem Versand Ihrer Push-Benachrichtigungen sollten Sie auf Folgendes achten:

1. Sie benötigen in Adobe Campaign Zugriff auf den Kanal **[!UICONTROL Push-Benachrichtigungen]**. Wenn Sie keinen Zugriff auf diesen Kanal haben, kontaktieren Sie das für Ihr Konto zuständige Team.

1. Vergewissern Sie sich, dass Ihr Anwender über die erforderlichen Berechtigungen in Adobe Campaign Standard und Experience Platform Launch verfügt.

1. Erstellen Sie in Experience Platform Launch eine Eigenschaft für Mobilgeräte. Weiterführende Informationen finden Sie unter [Eigenschaft für Mobilgeräte einrichten](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property).

1. Installieren Sie in Experience Platform Launch die **[!UICONTROL Adobe Campaign Standard]**-Erweiterung.

1. Konfigurieren Sie in Adobe Campaign Standard die Eigenschaft für Mobilgeräte, die Sie in Experience Platform Launch erstellt haben. Weiterführende Informationen finden Sie unter [Einrichten der Experience Platform Launch-App in Adobe Campaign](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html#SettingupyourAdobeExperiencePlatformLaunchapplicationinAdobeCampaign).

1. Fügen Sie die kanalspezifische Konfiguration für Ihre Mobile App-Einrichtung hinzu. Weiterführende Informationen finden Sie unter [Kanalspezifische Anwendungskonfiguration in Adobe Campaign](../../administration/using/configuring-a-mobile-application.md#channel-specific-config).

1. Informationen zu Fallimplementierungen für Mobilgeräte finden Sie in den ausführlichen Anweisungen zu Erweiterungen, Experience Platform Launch-Regeln und der SDK-Implementierung in [Mobile Anwendungsfällen, die in Adobe Campaign Standard mit den Adobe Experience Platform SDKs unterstützt werden](https://helpx.adobe.com/de/campaign/kb/configure-launch-rules-acs-use-cases.html).

## Häufig gestellte Fragen zu Push-Benachrichtigungen {#push-faq}

### Welche Ressourcen wären empfehlenswert, um mehr über den Push-Kanal zu erfahren? {#resource-push}

Sehen Sie sich die folgenden Ressourcen an:

* [Video-Tutorials](https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/communication-channels/mobile/push/creating-a-push-notification.html)
* [Produktdokumentation](../../channels/using/about-push-notifications.md)
* Konfigurieren mithilfe der AEP-SDK-[Dokumentation](../../administration/using/configuring-a-mobile-application.md)
* [Community-Seite](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-standard/ct-p/adobe-campaign-standard-community)

### Was muss ich tun, um in Campaign ein Push-Token zu erwerben? {#push-token-acquisition}

Stellen Sie sicher, dass das Bereitstellungs-Team die Bereitstellung des Push-Kanals in Adobe Campaign Standard abgeschlossen hat. Implementieren Sie die setPushIdentifier-API aus dem SDK. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard#set-up-push-messaging).

### Was benötige ich noch, um eine Push-Benachrichtigung zu senden, sobald ich das Push-Token und ECID in Campaign habe? {#sending-push}

Kunden müssen ein gültiges Push-Zertifikat im .pem-Format bereitstellen, um eine Push-Benachrichtigung zu senden. Für dieses Zertifikat ist kein Kennwort erforderlich.

### Was ist, wenn ich ein .p12-Zertifikat anstelle des .pem-Zertifikats habe? {#certificates}

Sie können ein .p12-Zertifikat in ein .pem-Zertifikat konvertieren, indem Sie den folgenden Befehl im Gerät ausführen. Es stehen auch verschiedene Online-Ressourcen für Konvertierungsanweisungen zur Verfügung.

```
openssl pkcs12 -in pushcert.p12 -out pushcert.pem -nodes -clcerts
```

### Woher weiß ich, ob das Hochladen des Zertifikats erfolgreich war? {#certificate-upload}

Die folgende Meldung wird angezeigt.

![](assets/faq_2.png)

### Kann ich gleichzeitig Produktions- und Sandbox-Zertifikate für die iOS-App hochladen (nicht zutreffend für Android)? {#prod-sandbox-certificate}

Nein, Apps funktionieren entweder im Sandbox- oder im Produktionsmodus und können nicht mehr in den anderen Modus (d. h. Sandbox- in Produktions-App) geändert werden, sobald sie eingerichtet wurden. Es wird empfohlen, dass Sie Ihre App zuerst im Sandbox-Modus testen und dann in den Produktionsmodus überleiten.

Um in den Produktionsmodus zu wechseln, müssen Sie eine weitere App erstellen. Achten Sie außerdem darauf, das Kontrollkästchen „Sandbox“ nicht zu aktivieren und ein Produktionszertifikat hochzuladen.

### Kann ich gleichzeitig iOS- und Android-Anmeldedaten hochladen? {#ios-android-credentials}

Ja, Campaign unterstützt beide Plattformen zugleich und ermöglicht das Hochladen von Anmeldedaten für beide Plattformen.

### Ich habe Push-Zertifikate erfolgreich hochgeladen, aber es werden keine Push-Nachrichten gesendet. {#push-certificates-upload}

Stellen Sie sicher, dass Ihre Push-Zertifikate gültig sind, indem Sie sie [hier](https://pushtry.com/) testen.

### Ich kann Push-Benachrichtigungen erfolgreich von pushtry.com senden, aber nicht über Campaign. {#push-not-sending}

Vergewissern Sie sich, dass Sie die [hier](../../administration/using/push-payload.md) angegebenen Push-Payload-Anweisungen befolgen.

Beachten Sie, dass Campaign für Android nur Daten-Payloads unterstützt, keine Benachrichtigungs-Payloads.

### Ich habe eine App im Abschnitt „Administration“ von Adobe Campaign Standard konfiguriert, aber die App ist nicht in den Versandeigenschaften verfügbar. {#mobile-app-unavailable}

Für eine App muss ein gültiges Push-Zertifikat hochgeladen werden, bevor sie in den Versandeigenschaften verfügbar gemacht werden kann.

### Ich habe alle Anweisungen auf dieser Seite ausprobiert und kann trotzdem keine Push-Benachrichtigungen von Campaign aus senden. {#push-troubleshoot}

Bitte eröffnen Sie ein Ticket für die Kundenunterstützung.

### Push-Benachrichtigungen werden von Campaign zugestellt, aber die Mediendatei wird nicht angezeigt.{#media-file-unavailable}

App-Entwickler müssen die Unterstützung für Mediendateien in der App bearbeiten. Manchmal verhindert auch die Netzwerkbandbreite das Rendering einer Mediendatei. Weitere Hinweise finden Sie auf dieser [Seite](../../administration/using/image-push-notification.md).

### Was muss ich tun, um Push-Berichte in Campaign zu aktivieren? {#push-reporting-enable}

Gehen Sie wie folgt vor:

* Konfigurieren Sie ein Postback für das Push-Tracking. Anweisungen dazu finden Sie [hier](../../administration/using/configuring-a-mobile-application.md).
* Implementieren Sie die trackAction-API vom Mobile Core. Weitere Informationen finden Sie auf dieser [Seite.](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference)

Detailliertere Anweisungen finden Sie auf dieser [Seite](../../administration/using/push-tracking.md).

### Welche Berichte stehen für den Push-Kanal zur Verfügung? {#push-report-available}

In Adobe Campaign steht für den Push-Kanal ein vordefinierter Bericht zur Verfügung. In dieser [Dokumentation](../../reporting/using/push-notification-report.md) finden Sie weitere Informationen.

Auf dieser [Seite](../../reporting/using/indicator-calculation.md#push-notification-delivery) erfahren Sie, wie die einzelnen Push-Metriken berechnet werden.

### Werden Deep-Links in Push- und In-App-Nachrichten unterstützt? {#deeplink-push}

Ja, Deep-Links werden in Push-Nachrichten unterstützt. Deep-Links sollten Folgendes enthalten:

* Sprache, die besagt, dass das Versand-Tracking deaktiviert werden muss, damit die Deep-Links funktionieren.
* Appsflyer mit Branch als Partner, die das Deeplink-Tracking durchführen können. Weitere Informationen zur Integration von Branch und Adobe Campaign Standard finden Sie auf dieser [Seite](Https://help.branch.io/using-branch/docs/adobe-campaign-standard-1).

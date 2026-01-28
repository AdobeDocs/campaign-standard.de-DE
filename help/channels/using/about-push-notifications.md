---
title: Über Push-Benachrichtigungen
description: Hier erhalten Sie die wichtigsten Informationen zum Push-Benachrichtigungskanal in Adobe Campaign.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
feature: Push
role: User
level: Intermediate
exl-id: e61daed6-a0ec-49d8-b1ad-77590fafb496
source-git-commit: 597ece8d833a216f0540f801461b08fdc9865024
workflow-type: ht
source-wordcount: '1227'
ht-degree: 100%

---

# Über Push-Benachrichtigungen{#about-push-notifications}

>[!CAUTION]
>
>Die Implementierung der Push-Benachrichtigung muss von Experten durchgeführt werden. Wenn Sie Hilfe brauchen, kontaktieren Sie bitte Ihren Adobe-Kundenbetreuer oder Professional Services-Partner. Push-Benachrichtigungen sind eine optionale Funktion. Bitte prüfen Sie Ihren Lizenzvertrag und kontaktieren Sie den Ansprechpartner für Ihr Konto, um diese Funktion zu aktivieren.

Sie können mit Adobe Campaign personalisierte und zielgruppenspezifische Push-Benachrichtigungen an iOS- und Android-Mobilgeräte versenden.

Diese Nachrichten werden in Mobile Apps empfangen, die in Adobe Campaign unter Verwendung des Experience Platform SDK eingerichtet wurden. Weiterführende Informationen dazu finden Sie im Abschnitt [Konfiguration einer Mobile App mithilfe von Experience Platform SDKs](../../administration/using/configuring-a-mobile-application.md).

In Adobe Campaign sind Attribute zu mobilen Profilen, die von Mobilgeräten gesendet werden, in der Ressource **[!UICONTROL App-Abonnements (appSubscriptionRcp)]** gespeichert. Dort können die Daten definiert werden, die über die Abonnenten Ihrer Apps gesammelt werden sollen.

Diese Ressource muss erweitert werden, damit die gewünschten, vom Mobilgerät an Adobe Campaign gesendeten Daten gesammelt werden. Eine detaillierte Anleitung dazu finden Sie auf dieser [Seite](../../developing/using/extending-the-subscriptions-to-an-application-resource.md).

In Adobe Campaign sind zwei Arten von Push-Benachrichtigungen verfügbar:

* Mit Benachrichtigungen vom Typ **[!UICONTROL Warnung/Nachricht/Badge]** können Sie standardmäßige textbasierte Nachrichten mit zusätzlichem Inhalt versenden (Ton, Badge, Deeplink usw.), die Sie im Abschnitt **[!UICONTROL Erweiterte Optionen]** definieren können.

  Diese Benachrichtigungstypen ermöglichen es Ihnen, einen Titel und eine Nachricht hinzuzufügen, in denen Sie Personalisierungsfelder verwenden können. Zum Personalisieren der Nachricht muss die Vorlage **[!UICONTROL Push-Benachrichtigung für Profile senden]** ausgewählt sein.

* Benachrichtigungen vom Typ **[!UICONTROL Stilles Pushen]** werden verwendet, um die Anwendung still zu informieren, ohne dass der Benutzer eine Nachricht oder einen Inhalt erhält. Ein typisches Anwendungsbeispiel für diese Art von Nachricht wäre, die Anwendung darauf hinzuweisen, dass auf dem Server Inhalt zum Herunterladen bereitsteht.

Mithilfe bestimmter Konfigurationen kann das Verhalten von Benachrichtigungen gesteuert werden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../channels/using/customizing-a-push-notification.md).

>[!NOTE]
>
>Datenschutzgesetze sind von Land zu Land unterschiedlich. In manchen Ländern ist es vorgeschrieben, die Benutzer Ihrer Apps über die Art der erhobenen Daten zu unterrichten. Erkundigen Sie sich bitte über die in Ihrem Land für Mobile Apps gültigen Gesetze. Stellen Sie sicher, dass die an Mobile Apps gesendeten Push-Benachrichtigungen den von Apple (Apple Push Notification Service) und Google (Google Cloud Messaging oder Firebase Cloud Messaging) vorgegebenen Voraussetzungen und Bedingungen entsprechen.

**Verwandte Inhalte:**

* [Push-Benachrichtigung vorbereiten und senden](../../channels/using/preparing-and-sending-a-push-notification.md)
* [Mehrsprachige Push-Benachrichtigungen erstellen](../../channels/using/creating-a-multilingual-push-notification.md)
* [Bericht zu Push-Benachrichtigungen](../../reporting/using/push-notification-report.md)
* [Handbuch zu Campaign Standard Mobile](../../channels/using/get-started-communication-channels.md)

## Voraussetzungen {#prerequisites}

>[!NOTE]
>Um die Funktion für Push-Benachrichtigungen in Campaign zu nutzen, benötigen Sie ein gültiges Push-Zertifikat im PEM-Format ohne Passwörter. 
>
>Wenn Sie über ein gültiges p12-Zertifikat verfügen, können Sie es mithilfe von Online-Ressourcen einfach in eine PEM-Datei konvertieren.

Vor dem Versand Ihrer Push-Benachrichtigungen sollten Sie auf Folgendes achten:

1. Sie benötigen in Adobe Campaign Zugriff auf den Kanal **[!UICONTROL Push-Benachrichtigungen]**. Wenn Sie keinen Zugriff auf diesen Kanal haben, kontaktieren Sie das für Ihr Konto zuständige Team.

1. Prüfen Sie, ob Ihr Anwender über die erforderlichen Berechtigungen in Adobe Campaign Standard und Tags in Adobe Experience Platform verfügt.

1. Erstellen Sie in der Datenerfassungs-UI eine Eigenschaft für Mobilgeräte. Weiterführende Informationen finden Sie unter [Eigenschaft für Mobilgeräte einrichten](https://developer.adobe.com/client-sdks/documentation/getting-started/create-a-mobile-property/).

1. Installieren Sie in der Datenerfassungs-UI die Erweiterung **[!UICONTROL Adobe Campaign Standard]**.

1. Konfigurieren Sie in Adobe Campaign Standard die Eigenschaft für Mobilgeräte, die Sie in der Datenerfassungs-UI erstellt haben. Weiterführende Informationen finden Sie unter [Einrichten der Tag-App in Adobe Campaign](../../administration/using/configuring-a-mobile-application.md#set-up-campaign).

1. Fügen Sie die kanalspezifische Konfiguration für Ihre Mobile App-Einrichtung hinzu. Weiterführende Informationen finden Sie unter [Kanalspezifische Anwendungskonfiguration in Adobe Campaign](../../administration/using/configuring-a-mobile-application.md#channel-specific-config).

1. Informationen zu Fallimplementierungen für Mobilgeräte finden Sie in den ausführlichen Anweisungen zu Erweiterungen, Tag-Regeln und der SDK-Implementierung in [Mobile Anwendungsfälle, die in Adobe Campaign Standard mit den Adobe Experience Platform SDKs unterstützt werden](../../administration/using/configuring-rules-launch.md).

## Häufig gestellte Fragen zu Push-Benachrichtigungen {#push-faq}

### Welche Ressourcen wären empfehlenswert, um mehr über den Push-Kanal zu erfahren? {#resource-push}

Sehen Sie sich die folgenden Ressourcen an:

* [Video-Tutorials](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/mobile/push/creating-a-push-notification.html?lang=de)
* [Produktdokumentation](../../channels/using/about-push-notifications.md)
* Konfigurieren mithilfe der AEP-SDK-[Dokumentation](../../administration/using/configuring-a-mobile-application.md)
* [Community-Seite](https://experienceleaguecommunities.adobe.com/t5/adobe-campaign-standard/ct-p/adobe-campaign-standard-community)

### Was muss ich tun, um in Campaign ein Push-Token zu erwerben? {#push-token-acquisition}

Stellen Sie sicher, dass das Bereitstellungs-Team die Bereitstellung des Push-Kanals in Adobe Campaign Standard abgeschlossen hat. Implementieren Sie die setPushIdentifier-API aus dem SDK. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/#set-up-push-messaging).

### Was benötige ich noch, um eine Push-Benachrichtigung zu senden, sobald ich das Push-Token und die ECID in Campaign habe? {#sending-push}

Kunden müssen ein gültiges Push-Zertifikat im .pem-Format bereitstellen, um eine Push-Benachrichtigung zu senden. Für dieses Zertifikat ist kein Kennwort erforderlich.

### Was ist, wenn ich ein .p12-Zertifikat anstelle des .pem-Zertifikats habe? {#certificates}

Sie können ein .p12-Zertifikat in ein .pem-Zertifikat konvertieren, indem Sie den folgenden Befehl im Gerät ausführen. Es stehen auch verschiedene Online-Ressourcen für Konvertierungsanweisungen zur Verfügung.

```
openssl pkcs12 -in pushcert.p12 -out pushcert.pem -nodes -clcerts
```

### Woher weiß ich, ob das Hochladen des Zertifikats erfolgreich war? {#certificate-upload}

Die folgende Meldung wird angezeigt.

![](assets/faq_2.png)

### Kann ich gleichzeitig Produktions- und Sandbox-Zertifikate für die iOS-Mobile-App hochladen (nicht zutreffend für Android)? {#prod-sandbox-certificate}

Nein, Apps funktionieren entweder im Sandbox- oder im Produktionsmodus und können nicht mehr in den anderen Modus (d. h. Sandbox- in Produktions-App) geändert werden, sobald sie eingerichtet wurden. Es wird empfohlen, dass Sie Ihre App zuerst im Sandbox-Modus testen und dann in den Produktionsmodus überleiten.

Um in den Produktionsmodus zu wechseln, müssen Sie eine weitere App erstellen. Achten Sie außerdem darauf, das Kontrollkästchen „Sandbox“ nicht zu aktivieren und ein Produktionszertifikat hochzuladen.

### Kann ich gleichzeitig iOS- und Android-Anmeldedaten hochladen? {#ios-android-credentials}

Ja, Campaign unterstützt beide Plattformen zugleich und ermöglicht das Hochladen von Anmeldedaten für beide Plattformen.

### Ich habe Push-Zertifikate erfolgreich hochgeladen, aber es werden keine Push-Nachrichten gesendet. {#push-certificates-upload}

Stellen Sie sicher, dass Ihre Push-Zertifikate gültig sind, indem Sie sie [hier](https://pushtry.com/) testen.

### Ich kann Push-Benachrichtigungen erfolgreich von pushtry.com senden, aber nicht über Campaign. {#push-not-sending}

Vergewissern Sie sich, dass Sie die [hier](../../administration/using/push-payload.md) angegebenen Push-Payload-Anweisungen befolgen.

Beachten Sie, dass Campaign für Android nur Daten-Payloads unterstützt, keine Benachrichtigungs-Payloads.

### Ich habe im Abschnitt &quot;Administration&quot; von Adobe Campaign Standard eine Mobile App konfiguriert, aber sie ist nicht in den Versandeigenschaften verfügbar. {#mobile-app-unavailable}

Für eine Mobile App muss ein gültiges Push-Zertifikat hochgeladen werden, bevor sie in den Versandeigenschaften verfügbar gemacht werden kann.

### Ich habe alle Anweisungen auf dieser Seite ausprobiert und kann in Campaign trotzdem keine Push-Benachrichtigungen senden. {#push-troubleshoot}

Bitte reichen Sie ein Ticket für die Kundenunterstützung ein.

### Push-Benachrichtigungen werden von Campaign zugestellt, aber die Mediendatei wird nicht angezeigt.{#media-file-unavailable}

App-Entwickler müssen die Unterstützung für Mediendateien in der App bearbeiten. Manchmal verhindert auch die Netzwerkbandbreite das Rendering einer Mediendatei. Weitere Hinweise finden Sie auf dieser [Seite](../../administration/using/image-push-notification.md).

### Was muss ich tun, um Push-Berichte in Campaign zu aktivieren? {#push-reporting-enable}

Gehen Sie wie folgt vor:

* Konfigurieren Sie ein Postback für das Push-Tracking. Anweisungen dazu finden Sie [hier](../../administration/using/configuring-a-mobile-application.md).
* Implementieren Sie die trackAction-API vom Mobile Core. Weitere Informationen finden Sie auf dieser [Seite.](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/)

Detailliertere Anweisungen finden Sie auf dieser [Seite](../../administration/using/push-tracking.md).

### Welche Berichte stehen für den Push-Kanal zur Verfügung? {#push-report-available}

In Adobe Campaign steht für den Push-Kanal ein vordefinierter Bericht zur Verfügung. In dieser [Dokumentation](../../reporting/using/push-notification-report.md) finden Sie weitere Informationen.

Auf dieser [Seite](../../reporting/using/indicator-calculation.md#push-notification-delivery) erfahren Sie, wie die einzelnen Push-Metriken berechnet werden.

### Werden Deeplinks in Push- und In-App-Nachrichten unterstützt? {#deeplink-push}

Ja, Deeplinks werden in Push-Nachrichten unterstützt. Deeplinks sollten Folgendes enthalten:

* Sprache, die besagt, dass das Versand-Tracking deaktiviert werden muss, damit die Deeplinks funktionieren.
* Appsflyer mit Branch als Partner, die das Deeplink-Tracking durchführen können. Weitere Informationen zur Integration von Branch und Adobe Campaign Standard finden Sie auf dieser [Seite](https://help.branch.io/using-branch/docs/adobe-campaign-standard-1).

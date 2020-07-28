---
title: Bild aus einer Push-Benachrichtigung von Adobe Campaign Standard anzeigen
description: Hier erfahren Sie, wie Sie ein Bild aus einer Adobe Campaign-Push-Benachrichtigung auf einem iOS-Gerät anzeigen.
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
source-git-commit: cf43edcacbab9f1f33ce29e23c0957d8bfa64e7d
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 85%

---


# Bilder und Videos unter iOS hinzufügen {#image-push}

>[!NOTE]
>
>Dieses Dokument gilt nur für iOS-Geräte.

In diesem Dokument erfahren Sie, wie Sie ein Bild aus einer iOS-Push-Benachrichtigung eines Adobe Campaign Standards anzeigen.

## Schritt 1: Push-Benachrichtigung einrichten {#set-up-push}

Push-Benachrichtigungen werden von Experience Platform SDKs unterstützt.

Mobile Apps, über die Push-Benachrichtigungen empfangen werden, müssen von einem Administrator in der Adobe-Campaign-Benutzeroberfläche konfiguriert werden.

Durch die Konfiguration von sowohl Adobe Campaign als auch Adobe Mobile Services können Sie die Daten Ihrer Mobile Apps für Ihre Kampagnen verwenden. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html).

Um Push-Benachrichtigungen mithilfe einer Experience Cloud SDK-Anwendung zu senden, muss in Adobe Experience Platform Launch eine Mobile App eingerichtet und in Adobe Campaign konfiguriert werden. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html#ChannelspecificapplicationconfigurationinAdobeCampaign).

## Schritt 2: Push-Benachrichtigung im Adobe Campaign anpassen {#customize-push}

In Adobe Campaign stehen Ihnen zur Anpassung von Push-Benachrichtigungen bei deren Erstellung eine Reihe erweiterter Optionen zur Verfügung.

1. Push-Benachrichtigung erstellen. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../channels/using/preparing-and-sending-a-push-notification.md).

1. From your push notification content page, access the **[!UICONTROL Advanced options]** section.

1. Enter the URL of your file in the **[!UICONTROL Rich media content URL]** field.
Unter iOS 10 oder höher können Sie Bild-, GIF-, Audio- und Videodateien einfügen.

   ![](assets/push_notif_advanced_6.png)

1. Erstellen Sie eine Vorschau Ihrer Push-Benachrichtigung und speichern Sie sie.

## Schritt 3: Mobile-App-Code anpassen {#mobile-app-code}

Nachdem Sie Ihre Push-Benachrichtigung in Adobe Campaign angepasst haben, müssen Sie Ihre Mobile App so konfigurieren, dass das Bild auf Geräten angezeigt wird.

>[!NOTE]
>
>Wenn Ihre App in Objective-C geschrieben ist, lesen Sie die folgende [Dokumentation](https://docs.adobe.com/content/help/de-DE/mobile-services/ios/messaging-ios/push-messaging/c-set-up-rich-push-notif-ios.html).

If your app is in [!DNL Swift], follow the steps below:

1. Open your [!DNL Xcode] project.

1. In your [!DNL Xcode] project, select **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL Target]**.

1. Select **[!UICONTROL Notification Service Extension]**.

   ![](assets/push_notif_advanced_12.png)

1. Überprüfen Sie, ob die **NotificationService.swift**-Dateiklasse erstellt wurde.

1. Bearbeiten Sie diese Klasse und ersetzen Sie den Standardinhalt durch Folgendes.
Dadurch kann die App den eingehenden Parameter mit der Bild-URL verarbeiten, analysieren, lokal kopieren und dann über die Push-Benachrichtigung anzeigen.

   ```
   import UserNotifications
   
   class NotificationService: UNNotificationServiceExtension {
   
   var contentHandler: ((UNNotificationContent) -> Void)?
   var bestAttemptContent: UNMutableNotificationContent?
   
   override func didReceive(_ request: UNNotificationRequest, withContentHandler contentHandler: @escaping (UNNotificationContent) -> Void) {
       self.contentHandler = contentHandler
       bestAttemptContent = (request.content.mutableCopy() as? UNMutableNotificationContent)
   
       if let bestAttemptContent = bestAttemptContent {
           var urlString:String? = nil
           if let urlImageString = request.content.userInfo["media-attachment-url"] as? String {
               urlString = urlImageString
           }
   
           if urlString != nil, let fileUrl = URL(string: urlString!) {
               print("fileUrl: \(fileUrl)")
   
               // Download the attachment
               URLSession.shared.downloadTask(with: fileUrl) { (location, response, error) in
                   if let location = location {
                       // Move temporary file to remove .tmp extension
                       if (error == nil) {
                           let tmpDirectory = NSTemporaryDirectory()
                           let tmpFile = "file://".appending(tmpDirectory).appending(fileUrl.lastPathComponent)
                           let tmpUrl = URL(string: tmpFile)!
                           try! FileManager.default.moveItem(at: location, to: tmpUrl)
   
                           // Add the attachment to the notification content
                           if let attachment = try? UNNotificationAttachment(identifier: fileUrl.lastPathComponent, url: tmpUrl) {
                               bestAttemptContent.attachments = [attachment]
                               }
                       }
                       if(error != nil) {
                           print("Failed to download attachment: \(error.debugDescription)")
                       }
                   }
                   // Serve the notification content
                   contentHandler(bestAttemptContent)
               }.resume()
           }
       }
   }
   
   override func serviceExtensionTimeWillExpire() {
       // Called just before the extension will be terminated by the system.
       // Use this as an opportunity to deliver your "best attempt" at modified content, otherwise the original push payload will be used.
       if let contentHandler = contentHandler, let bestAttemptContent = bestAttemptContent {
           contentHandler(bestAttemptContent)
       }
   }
   
   }
   ```

Das Mobilgerät sollte die folgende Payload erhalten, während die Benachrichtigung gesendet wird.

Die Bild-URL ist dem Schlüssel &quot;media-attachment-url&quot; zugeordnet. Dies ist das Schlüssel/Wert-Paar, das Sie aus der Perspektive des Anwendungs-Codes handhaben müssen, um das Bild herunterzuladen und anzuzeigen.

```
userInfo: [AnyHashable("media-attachment-url"): https://pbs.twimg.com/profile_images/876737835314950144/zPTs9b7o.jpg, AnyHashable("_dId"): 1de3ef93, AnyHashable("_mId"): h280a5, AnyHashable("aps"): {
 
    alert =     {
 
        body = "Message Body here";
 
        title = "This a push from Campaign";
 
    };
 
    badge = 1;
 
    "mutable-content" = 1;
 
}]
```

## Schritt 4: Versand der Push-Benachrichtigung testen {#test-send-push}

Sie können jetzt testen, wie Ihre App und der in Schritt 2 erstellte Versand funktionieren. Weiterführende Informationen zum Vorbereiten und Senden Ihrer Push-Benachrichtigung finden Sie auf dieser [Seite](../../channels/using/preparing-and-sending-a-push-notification.md).

![](assets/push_notif_advanced_34.png)


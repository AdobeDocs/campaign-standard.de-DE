---
solution: Campaign Standard
product: campaign
title: Implementieren von Push-Tracking
description: Mit diesem Dokument können Sie sicherstellen, dass das Tracking von Push-Benachrichtigungen unter iOS und Android richtig implementiert wurde.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
feature: Instanzeinstellungen
role: Administrator
level: Erfahren
translation-type: tm+mt
source-git-commit: a7a1aa2841410674597264927325c073fef4ce26
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 74%

---


# Implementieren des lokalen Tracking {#local-tracking}

## Über das lokale Tracking {#about-local-tracking}

Auf dieser Seite erfahren Sie, wie Sie sicherstellen, dass das lokale Benachrichtigungs-Tracking korrekt implementiert wurde. Beachten Sie, dass dies voraussetzt, dass die lokale Benachrichtigung bereits konfiguriert wurde.

Das Tracking lokaler Benachrichtigungen kann in drei Typen unterteilt werden:

* **Lokale Impressionen**: Wenn eine lokale Benachrichtigung an das Gerät gesendet wurde und im Benachrichtigungs-Center vorhanden ist, aber noch keine Aktivität stattgefunden hat. In den meisten Fällen sollte die Zahl der Impressionen ähnlich oder gar identisch mit der gesendeten Zahl sein. Dadurch wird sichergestellt, dass das Gerät die Nachricht erhalten hat und diese Informationen an den Server zurückgibt.

* **Lokaler Klick** : Wenn eine lokale Benachrichtigung an das Gerät gesendet wurde und der Benutzer auf die Benachrichtigung geklickt hat. Der Anwender wollte die Benachrichtigung entweder ansehen oder verwerfen. Wenn er sie angesehen hat, wird sie beim lokalen Öffnungs-Tracking berücksichtigt.

* **Lokale Öffnung**: Wenn eine lokale Benachrichtigung an das Gerät gesendet wurde und der Anwender auf die Benachrichtigung geklickt hat, wodurch die App geöffnet wurde. Dies ist ähnlich der lokalen Klick-Kategorie mit dem Unterschied, dass keine lokale Öffnung ausgelöst wird, wenn die Benachrichtigung verworfen wird.

Um das Tracking für Adobe Campaign Standard zu implementieren, muss die Mobile App das Mobile SDK in die App integrieren. Diese SDKs sind in [!DNL Adobe Mobile Services] verfügbar.

Zum Senden von Tracking-Daten müssen drei Variablen gesendet werden. Zwei davon gehören zu den von Adobe Campaign empfangenen Daten und die dritte ist eine Aktionsvariable, die bestimmt, ob es sich um eine Impression, einen Klick oder eine Öffnung handelt.

| Variable | Wert |
| :-: | :-: |
| deliveryId | `deliveryId` aus eingehenden Daten (ähnlich wie bei der Push-Verfolgung, bei der  `_dld` die Daten verwendet werden) |
| broadlogId | `broadlogId` aus eingehenden Daten (ähnlich wie bei der Push-Verfolgung, bei der  `_mld` die Daten verwendet werden) |
| Aktion | &quot;1&quot; für Öffnung, &quot;2&quot; für Klick und &quot;7&quot; für Impression |

## Implementieren der lokalen Impressionsverfolgung {#implement-local-impression-tracking}

Das Adobe Experience Platform Mobile SDK sendet automatisch das Impressions-Ereignis für Android und iOS ohne zusätzliche Konfiguration.

## Implementieren der Klick-Verfolgung {#implementing-click-tracking}

Zur Klick-Verfolgung müssen Sie den Wert &quot;2&quot;für Aktion senden, wenn Sie die Funktionen `collectMessageInfo()` oder `trackAction()` aufrufen.

### Für Android {#implement-click-tracking-android}

Beim Klick-Tracking müssen zwei Szenarien behandelt werden:

* Der Anwender sieht die Benachrichtigung, löscht sie jedoch.

   Um Klick im Fall eines Kündigungsszenarios zu verfolgen, fügen Sie den Broadcast-Empfänger `NotificationDismissalHandler` in der AndroidManifest-Datei Ihres Anwendungsmoduls hinzu.

   ```
   <receiver
   android:name="com.adobe.marketing.mobile.NotificationDismissalHandler">
   </receiver>
   ```

* Der Benutzer sieht die Benachrichtigung und klickt darauf. Dies führt zum Öffnungs-Tracking.

   Dieses Szenario sollte einen Klick und einen offenen Klick erzeugen. Die Verfolgung dieses Klicks ist Teil der Implementierung, die zur Verfolgung des offenen Bereichs erforderlich ist. Siehe [Implementieren der offenen Verfolgung](#implement-open-tracking).

### Für iOS {#implement-click-tracking-ios}

Um die Klick-Tracking-Informationen zu senden, müssen Sie Folgendes hinzufügen:

```
class NotificationDelegate: NSObject, UNUserNotificationCenterDelegate {

   func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
        let userInfo = response.notification.request.content.userInfo
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            print("Dismiss Action")
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
                
                //If you are using ACPCore v2.3.0 or later, use the next line.
                
                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                
                //Else comment out the above line and uncomment the line below
                
                // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            
            ////MORE CODE
        }
        completionHandler()
    }
}
```

## Implementieren der offenen Verfolgung {#implement-open-tracking}

Sie müssen &quot;1&quot; und &quot;2&quot; senden, da der Benutzer zum Öffnen der App zunächst auf die Benachrichtigung klicken muss. Wenn die App nicht über eine lokale Benachrichtigung gestartet/geöffnet wird, treten keine Tracking-Ereignisse auf.

### Für Android {#implement-open-tracking-android}

Um das Öffnen verfolgen zu können, müssen Sie einen Intent erstellen. Intent-Objekte ermöglichen es dem Android-OS, Ihre Methode aufzurufen, wenn bestimmte Aktionen ausgeführt werden. In diesem Fall ist dies das Klicken der Benachrichtigung, um die App zu öffnen.

Dieser Code basiert auf der Implementierung des Klick-Impression-Tracking. Mit festgelegtem Intent müssen Sie jetzt Tracking-Daten zurück an Adobe Campaign senden. In diesem Fall wird Android View ([!DNL Activity]), das die Benachrichtigung ausgelöst hat, aufgrund des Klicks des Benutzers geöffnet oder in den Vordergrund gestellt. Das Intent-Objekt in [!DNL Activity] enthält die Benachrichtigungsdaten, die zum Verfolgen von Öffnungen verwendet werden können.

MainActivity.java (erweitert [!DNL Activity])

```
@Override
protected void onResume() {
    super.onResume();
    handleTracking();
}
 
 
private void handleTracking() {

    //Check to see if this view was opened based on a notification

    Intent intent = getIntent();
    Bundle data = intent.getExtras();
 
    if (data != null) {

        //Opened based on the notification, you need to get the tracking that was passed on.

        Map<String, String> notificationData = (Map<String, Object>)data.getSerializableExtra("NOTIFICATION_USER_INFO");
        String deliveryId = (String)notificationData.get("deliveryId");
        String messageId = (String)notificationData.get("broadlogId");

        if (deliveryId != null && messageId != null) {
            HashMap<String, String> contextData = new HashMap<>();
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
 
            //Send click tracking since the user did click on the notification

            contextData.put("action", "2");

            //If you are using ACPCore v1.4.0 or later, use the next line.
    
            MobileCore.collectMessageInfo(contextData);

            //Else comment out the above line and uncomment the line below

            // MobileCore.trackAction("tracking", contextData);
 
            //Send open tracking since the user opened the app

            contextData.put("action", "1");

            //If you are using  ACPCore v1.4.0 or later, use the next line.

            MobileCore.collectMessageInfo(contextData);

            //Else comment out the above line and uncomment the line below

            // MobileCore.trackAction("tracking", contextData);
        }
    }
}
```

### Für iOS {#implement-open-tracking-ios}

```
import os.log
import Foundation
import UserNotifications
import UserNotificationsUI
import ACPCore
 
class NotificationDelegate: NSObject, UNUserNotificationCenterDelegate {
 
    //Called when user clicks the local notification or also called from willPresent()

    func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
 
        let userInfo = response.notification.request.content.userInfo
        os_log("App push data %{public}@, in userNotificationCenter:didReceive()", type: .debug, userInfo)
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:

            //This is to handle the Dismiss action

            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {

                //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])

                //Else comment out the above line and uncomment the line below

                // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            //This is to handle the tracking when the app opens
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {

               //If you are using ACPCore v2.3.0 or later, use the next line.

               ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
               ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])

               //Else comment out the above line and uncomment the line below

               // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
               // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
            }
        }
        completionHandler()
    }
}
```

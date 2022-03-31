---
title: Implementieren von lokalem Tracking
description: Erfahren Sie, wie Sie sicherstellen können, dass das Tracking von Push-Benachrichtigungen unter iOS und Android richtig implementiert wurde
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
exl-id: b983d0a3-c345-44d4-bc82-202bf6ed26ab
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: ht
source-wordcount: '568'
ht-degree: 100%

---

# Implementieren von lokalem Tracking {#local-tracking}

## Über das lokale Tracking {#about-local-tracking}

Auf dieser Seite erfahren Sie, wie Sie sicherstellen, dass das lokale Benachrichtigungs-Tracking korrekt implementiert wurde. Beachten Sie, dass dies voraussetzt, dass die lokale Benachrichtigung bereits konfiguriert wurde.

Das Tracking lokaler Benachrichtigungen kann in drei Typen unterteilt werden:

* **Lokale Impressionen**: Wenn eine lokale Benachrichtigung an das Gerät gesendet wurde und im Benachrichtigungs-Center vorhanden ist, aber noch keine Aktivität stattgefunden hat. In den meisten Fällen sollte die Zahl der Impressionen ähnlich oder gar identisch mit der gesendeten Zahl sein. Dadurch wird sichergestellt, dass das Gerät die Nachricht erhalten hat und diese Informationen an den Server zurückgibt.

* **Lokaler Klick**: Wenn eine lokale Benachrichtigung an das Gerät gesendet wurde und der Anwender auf diese Benachrichtigung geklickt hat. Der Anwender wollte die Benachrichtigung entweder ansehen oder verwerfen. Wenn er sie angesehen hat, wird sie beim lokalen Öffnungs-Tracking berücksichtigt.

* **Lokale Öffnung**: Wenn eine lokale Benachrichtigung an das Gerät gesendet wurde und der Anwender auf die Benachrichtigung geklickt hat, wodurch die App geöffnet wurde. Dies ist ähnlich der lokalen Klick-Kategorie mit dem Unterschied, dass keine lokale Öffnung ausgelöst wird, wenn die Benachrichtigung verworfen wird.

Um das Tracking für Adobe Campaign Standard zu implementieren, muss die Mobile App das Mobile SDK in die App integrieren. Diese SDKs sind in [!DNL Adobe Mobile Services] verfügbar.

Zum Senden von Tracking-Daten müssen drei Variablen gesendet werden. Zwei davon gehören zu den von Adobe Campaign empfangenen Daten und die dritte ist eine Aktionsvariable, die bestimmt, ob es sich um eine Impression, einen Klick oder eine Öffnung handelt.

| Variable | Wert |
| :-: | :-: |
| deliveryId | `deliveryId` aus den eingehenden Daten (ähnlich einem Push-Tracking, bei dem `_dld` verwendet wird) |
| broadlogId | `broadlogId` aus den eingehenden Daten (ähnlich einem Push-Tracking, bei dem `_mld` verwendet wird) |
| Aktion | &quot;1&quot; für Öffnung, &quot;2&quot; für Klick und &quot;7&quot; für Impression |

## Implementieren des lokalen Impression-Tracking {#implement-local-impression-tracking}

Das Adobe Experience Platform Mobile SDK sendet automatisch das Impression-Ereignis sowohl für Android als auch für iOS ohne zusätzliche Konfiguration.

## Implementieren des Klick-Tracking {#implementing-click-tracking}

Für das Klick-Tracking muss für die Aktion der Wert &quot;2&quot; gesendet werden, wenn die Funktion `collectMessageInfo()` oder `trackAction()` aufgerufen wird.

### Für Android {#implement-click-tracking-android}

Um Klicks zu verfolgen, müssen zwei Szenarien implementiert werden:

* Der Anwender sieht die Benachrichtigung, löscht sie jedoch.

   Um die Klicks für Abweisungsszenarien zu verfolgen, fügen Sie den Broadcast-Empfänger `NotificationDismissalHandler` in der AndroidManifest-Datei Ihres Anwendungsmoduls hinzu.

   ```
   <receiver
   android:name="com.adobe.marketing.mobile.NotificationDismissalHandler">
   </receiver>
   ```

* Der Benutzer sieht die Benachrichtigung und klickt darauf. Dies führt zu einem Öffnungs-Tracking.

   Dieses Szenario sollte einen Klick und eine Öffnung erzeugen. Das Tracking dieses Klicks ist Teil der Implementierung, die zum Tracking von Öffnungen erforderlich ist. Siehe [Implementieren des Öffnungs-Trackings](#implement-open-tracking).

### Für iOS {#implement-click-tracking-ios}

Um die Informationen zum Klick-Tracking zu senden, müssen Sie Folgendes hinzufügen:

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

## Implementieren des Öffnungs-Trackings {#implement-open-tracking}

Sie müssen &quot;1&quot; und &quot;2&quot; senden, da der Benutzer zum Öffnen der Anwendung zunächst auf die Benachrichtigung klicken muss. Wenn die Anwendung nicht über eine lokale Benachrichtigung gestartet/geöffnet wird, treten keine Tracking-Ereignisse auf.

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

        //Opened based on the notification, you must get the tracking that was passed on.

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

---
title: Implementieren von Push-Tracking
description: Erfahren Sie, wie Sie sicherstellen können, dass das Tracking von Push-Benachrichtigungen unter iOS und Android richtig implementiert wurde
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 950d24e2-358f-44f8-98ea-643be61d4573
source-git-commit: acbe5f1990738f586e4310d13f0e19baab11d771
workflow-type: tm+mt
source-wordcount: '984'
ht-degree: 100%

---

# Implementieren von Push-Tracking {#push-tracking}

## Informationen zu Push-Tracking {#about-push-tracking}

Damit die Push-Benachrichtigung vollständig eingerichtet ist, müssen Sie darauf achten, dass das Tracking korrekt implementiert wurde, da nicht bei jeder Push-Benachrichtigung das Tracking aktiviert ist. Zu diesem Zweck müssen Entwickler feststellen, bei welchen Sendungen das Tracking aktiviert ist. Adobe Campaign Standard sendet ein Flag mit dem Namen `_acsDeliveryTracking` mit den zwei Werten: **on** oder **off**. Der App-Entwickler sollte eine Tracking-Anfrage nur für Sendungen senden, deren Variable aktiviert ist (**on**).

>[!IMPORTANT]
>
>Diese Variable ist nicht verfügbar für Sendungen, die vor Version 21.1 eingerichtet wurden, oder für Sendungen, die benutzerdefinierte Vorlagen verwenden.

Das Push-Tracking ist in drei Typen unterteilt:

* **Push-Impressionen**: Wenn eine Push-Benachrichtigung an das Gerät gesendet wurde und im Benachrichtigungs-Center sitzt, aber noch nicht angefasst wurde.  Dies gilt als Impression.  In den meisten Fällen sollte die Zahl der Impressionen ähnlich oder gar identisch mit der gesendeten Zahl sein. Dadurch wird sichergestellt, dass das Gerät die Nachricht erhalten und diese Informationen an den Server zurückgegeben hat.

* **Push-Klick**: Wenn eine Push-Benachrichtigung an das Gerät gesendet wurde und der Anwender auf das Gerät geklickt hat.  Der Anwender wollte die Benachrichtigung entweder ansehen oder verwerfen. Wenn er sie angesehen hat, wird sie beim Push-Öffnungs-Tracking berücksichtigt.

* **Push-Öffnung**: Wenn eine Push-Benachrichtigung an das Gerät gesendet wurde und der Anwender auf die Benachrichtigung geklickt hat, wodurch die App geöffnet wurde.  Dies ist ähnlich der Push-Klick-Kategorie mit dem Unterschied, dass keine Push-Öffnung ausgelöst wird, wenn die Benachrichtigung verworfen wird.

Um das Tracking für Campaign Standard zu implementieren, muss die Mobile App die Adobe Experience Platform-SDKs enthalten. Diese SDKs sind im Abschnitt [Dokumentation zu Adobe Experience Platform-SDKs](https://github.com/Adobe-Marketing-Cloud/acp-sdks) verfügbar.

Zum Senden von Tracking-Daten müssen drei Variablen gesendet werden. Zwei davon gehören zu den von Campaign Standard empfangenen Daten, eine ist eine Aktionsvariable, die bestimmt, ob es sich um eine **Impression**, einen **Klick** oder eine **Öffnung** handelt.

| Variable | Wert |
|:-:|:-:|
| broadlogId | _mId aus Daten |
| deliveryId | _dId aus Daten |
| Aktion | &quot;1&quot; für Öffnung, &quot;2&quot; für Klick und &quot;7&quot; für Impression |

## Implementierung für Android {#implementation-android}

### Implementieren des Push-Impression-Tracking {#push-impression-tracking-android}

Für das Impression-Tracking müssen Sie bei einer Aktion den Wert &quot;7&quot; senden, wenn die Funktionen `collectMessageInfo()` oder `trackAction()` aufgerufen werden.

Weitere Informationen zu Sendungen, die vor Version 21.1 erstellt wurden, oder Sendungen mit benutzerdefinierter Vorlage finden Sie in diesem [Abschnitt](../../administration/using/push-tracking.md#about-push-tracking).

```
@Override
public void onMessageReceived(RemoteMessage remoteMessage) {
....{Handle push messages}....
  if (data.size() > 0) {
    String deliveryId = data.get("_dId");
    String messageId = data.get("_mId");
    String acsDeliveryTracking = data.get("_acsDeliveryTracking");
 
    /*
    This is to handle deliveries created before 21.1 release or deliveries with custom template
    where acsDeliveryTracking is not available.
    */
    if( acsDeliveryTracking == null ) {
        acsDeliveryTracking = "on";
    }
 
    HashMap<String, String> contextData = new HashMap<>();
    if( deliveryId != null && messageId != null && acsDeliveryTracking.equals("on")) {
      contextData.put("deliveryId", deliveryId);
      contextData.put("broadlogId", messageId);
      contextData.put("action", "7");

    //If you are using ACPCore v1.4.0 or later, use the next line.
      
      MobileCore.collectMessageInfo(contextData);
      
    //Else comment out the above line and uncomment the line below
        
    //MobileCore.trackAction("tracking", contextData) ;
    }
  }
}
```

### Implementieren des Klick-Tracking {#push-click-tracking-android}

Für das Klick-Tracking muss bei einer Aktion der Wert &quot;2&quot; gesendet werden, wenn die Funktionen `collectMessageInfo()` oder `trackAction()` aufgerufen werden.
Beim Klick-Tracking müssen zwei Szenarien behandelt werden:

* Der Anwender sieht die Benachrichtigung, löscht sie jedoch.
* Der Anwender sieht die Benachrichtigung und klickt darauf, sodass nun das Öffnungs-Tracking erfolgt.

Dazu müssen Sie zwei Intents verwenden: eine zum Klicken auf die Benachrichtigung und eine andere zum Verwerfen der Benachrichtigung.

Weitere Informationen zu Sendungen, die vor Version 21.1 erstellt wurden, oder Sendungen mit benutzerdefinierter Vorlage finden Sie in diesem [Abschnitt](../../administration/using/push-tracking.md#about-push-tracking).

**[!UICONTROL MyFirebaseMessagingService.java]**

```
private void sendNotification(Map<String, String> data) {
    Intent openIntent = new Intent(this, CollectPIIActivity.class);
    Intent dismissIntent = new Intent(this, NotificationDismissedReceiver.class);
    openIntent.addFlags(Intent.FLAG_ACTIVITY_CLEAR_TOP);
  
    //put the data map into the intent to track clickthroughs
    Bundle pushData = new Bundle();
    Set<String> keySet = data.keySet();
    for (String key : keySet) {
        pushData.putString(key, data.get(key));
    }
    openIntent.putExtras(pushData);
    dissmissIntent.putExtras(pushData);
  
  
    PendingIntent pendingIntent = PendingIntent.getActivity(this, 0, openIntent,
        PendingIntent.FLAG_UPDATE_CURRENT);
    PendingIntent onDismissPendingIntent = PendingIntent.getBroadcast(this.getApplicationContext(), 0, dismissIntent, 0);
  
    //<BUILD NOTIFICATION using notification builder>
    //Add both Intents to the notification
    notificationBuilder.setContentIntent(pendingIntent);
    notificationBuilder.setDeleteIntent(onDismissPendingIntent);
}
```

Damit der **[!UICONTROL BroadcastReceiver]** funktioniert, müssen Sie ihn bei **[!UICONTROL AndroidManifest.xml]** registrieren.

```
<manifest>
    <application>
        <receiver android:name=".NotificationDismissedReceiver">
        </receiver>
    </application>
</manifest>
```

NotificationDismessedReceiver.java

```
public class NotificationDismissedReceiver extends BroadcastReceiver {
    private static final String TAG = NotificationDismissedReceiver.class.getSimpleName();
    @Override
    public void onReceive(Context context, Intent intent) {
        Bundle data = intent.getExtras();
        String deliveryId = data.getString("_dId");
        String messageId = data.getString("_mId");
        String acsDeliveryTracking = data.get("_acsDeliveryTracking");
         
        /*
        This is to handle deliveries created before 21.1 release or deliveries with custom template
        where acsDeliveryTracking is not available.
        */
        if( acsDeliveryTracking == null ) {
            acsDeliveryTracking = "on";
        }
 
        HashMap<String, Object> contextData = new HashMap<>();
 
        //We only send the click tracking since the user dismissed the notification
        if (deliveryId != null && messageId != null && acsDeliveryTracking.equals("on")) {
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
            contextData.put("action", "2");
            
        //If you are using ACPCore v1.4.0 or later, use the next line.
        
            MobileCore.collectMessageInfo(contextData);
            
        //Else comment out the above line and uncomment the line below
        
            //MobileCore.trackAction("tracking", contextData);
        }
    }
}
```

### Implementieren des Öffnungs-Tracking {#push-open-tracking-android}

Sie müssen &quot;1&quot; und &quot;2&quot; senden, da der Anwender zum Öffnen der App zunächst auf die Benachrichtigung klicken muss. Wenn die App nicht über eine Push-Benachrichtigung gestartet/geöffnet wird, treten keine Tracking-Ereignisse auf.

Um das Öffnen verfolgen zu können, müssen Sie einen Intent erstellen. Intent-Objekte ermöglichen es dem Android-OS, Ihre Methode aufzurufen, wenn bestimmte Aktionen ausgeführt werden. In diesem Fall ist es das Klicken auf die Benachrichtigung, um die App zu öffnen.

Dieser Code basiert auf der Implementierung des Klick-Impression-Tracking. Mit festgelegtem **[!UICONTROL Intent]** müssen Sie jetzt Tracking-Daten zurück an Adobe Campaign Standard senden. In diesem Fall müssen Sie den **[!UICONTROL Öffnungs-Intent]** so definieren, dass eine bestimmte Ansicht in Ihrer App geöffnet wird. Dadurch wird die onResume-Methode mit den Benachrichtigungsdaten im **[!UICONTROL Intent-Objekt]** aufgerufen.

Weitere Informationen zu Sendungen, die vor Version 21.1 erstellt wurden, oder Sendungen mit benutzerdefinierter Vorlage finden Sie in diesem [Abschnitt](../../administration/using/push-tracking.md#about-push-tracking).

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
        //This was opened based on the notification, you need to get the tracking that was passed on.
        String deliveryId = data.getString("_dId");
        String messageId = data.getString("_mId");
        String acsDeliveryTracking = data.get("_acsDeliveryTracking");
        /*
        This is to handle deliveries created before 21.1 release or deliveries with custom template
        where acsDeliveryTracking is not available.
        */
        if( acsDeliveryTracking == null) {
            acsDeliveryTracking = "on";
        }
 
        HashMap<String, String> contextData = new HashMap<>();
 
        if (deliveryId != null && messageId != null && acsDeliveryTracking.equals("on")) {
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
            contextData.put("action", "2");
            
            //Send Click Tracking since the user did click on the notification
              
                //If you are using ACPCore v1.4.0 or later, use the next line.

                MobileCore.collectMessageInfo(contextData);
                  
                //Else comment out the above line and uncomment the line below
        
                //MobileCore.trackAction("tracking", contextData);
 
                //Send Open Tracking since the user opened the app
            
                contextData.put("action", "1");
                
                //If you are using ACPCore v1.4.0 or later, use the next line.

                MobileCore.collectMessageInfo(contextData);
                //Else comment out the above line and uncomment the line below
        
                //MobileCore.trackAction("tracking", contextData);
        }
    }
}
```

## Implementierung für iOS {#implementation-iOS}

### Implementieren des Push-Impression-Tracking {#push-impression-tracking-iOS}

Für das Impression-Tracking müssen Sie bei einer Aktion den Wert &quot;7&quot; senden, wenn die Funktionen `collectMessageInfo()` oder `trackAction()` aufgerufen werden.

Um zu verstehen, wie iOS-Benachrichtigungen funktionieren, müssen die drei Status einer App beschrieben werden:

* **Vordergrund**: Wenn die App aktuell aktiv ist und sich derzeit auf dem Bildschirm befindet (im Vordergrund).
* **Hintergrund**: Wenn die App sich nicht auf dem Bildschirm befindet, der Prozess jedoch nicht geschlossen ist. Wenn Sie auf die Schaltfläche &quot;Startseite&quot; doppelklicken, werden in der Regel alle im Hintergrund befindlichen Apps angezeigt.
* **Aus/geschlossen**: Eine App, deren Prozess beendet wurde.

Damit das **[!UICONTROL Impression]**-Tracking auch dann funktioniert, wenn das Programm im Hintergrund läuft, müssen wir **[!UICONTROL Content-Available]** senden, um dem Programm mitzuteilen, dass ein Tracking durchgeführt werden soll.

>[!CAUTION]
>
> Wenn ein Programm geschlossen ist, ruft Apple das Programm erst nach dessen Neustart auf. Das bedeutet, dass Sie nicht erfahren, wenn die Benachrichtigung unter iOS empfangen wird. </br> Aus diesem Grund ist das Impression-Tracking unter iOS möglicherweise nicht präzise und sollte daher nicht als zuverlässig betrachtet werden.

Weitere Informationen zu Sendungen, die vor Version 21.1 erstellt wurden, oder Sendungen mit benutzerdefinierter Vorlage finden Sie in diesem [Abschnitt](../../administration/using/push-tracking.md#about-push-tracking).

Der folgende Code richtet sich an die App im Hintergrund:

```
// In didReceiveRemoteNotification event handler in AppDelegate.m
 
//In order to handle push notification when only in background with content-available: 1
func application(_ application: UIApplication, didReceiveRemoteNotification userInfo: [AnyHashable : Any], fetchCompletionHandler completionHandler: @escaping (UIBackgroundFetchResult) -> Void) {
 
        //Check if the app is not in the foreground right now
        if(UIApplication.shared.applicationState != .active) {
            let deliveryId = userInfo["_dId"] as? String
            let broadlogId = userInfo["_mId"] as? String
            let acsDeliveryTracking = userInfo["_acsDeliveryTracking"] as? String
            /*
            This is to handle deliveries created before 21.1 release or deliveries with custom template where acsDeliveryTracking is not available.
            */
            if( acsDeliveryTracking == nil ) {
                acsDeliveryTracking = "on";
            }
            if (deliveryId != nil && broadlogId != nil && acsDeliveryTracking?.caseInsensitiveCompare("on") == ComparisonResult.orderedSame) {

            //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"7"])
                
            //Else comment out the above line and uncomment the line below
        
                //ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"7"])
            }
        }
        completionHandler(UIBackgroundFetchResult.noData)
    }
```

Der folgende Code richtet sich an die App im Vordergrund:

```
// This will get called when the app is in the foreground
 
func userNotificationCenter(_ center: UNUserNotificationCenter, willPresent notification: UNNotification, withCompletionHandler completionHandler: @escaping (UNNotificationPresentationOptions) -> Void) {
 
 
        let userInfo = notification.request.content.userInfo
        let deliveryId = userInfo["_dId"] as? String
        let broadlogId = userInfo["_mId"] as? String
        let acsDeliveryTracking = userInfo["_acsDeliveryTracking"] as? String
        /*
        This is to handle deliveries created before 21.1 release or deliveries with custom template where acsDeliveryTracking is not available.
        */
        if( acsDeliveryTracking == nil ) {
            acsDeliveryTracking = "on";
        }
        if (deliveryId != nil && broadlogId != nil && acsDeliveryTracking?.caseInsensitiveCompare("on") == ComparisonResult.orderedSame) {

            //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"7"])
                
            //Else comment out the above line and uncomment the line below
        
                //ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"7"])        
            }
        completionHandler([.alert,.sound])
    }
```

### Implementieren des Klick-Tracking {#push-click-tracking-iOS}

Für das Klick-Tracking muss bei einer Aktion der Wert &quot;2&quot; gesendet werden, wenn die Funktionen `collectMessageInfo()` oder `trackAction()` aufgerufen werden.
Weitere Informationen zu Sendungen, die vor Version 21.1 erstellt wurden, oder Sendungen mit benutzerdefinierter Vorlage finden Sie in diesem [Abschnitt](../../administration/using/push-tracking.md#about-push-tracking).

```
// AppDelegate.swift
...
import os.log
import UserNotifications
...
  
func registerForPushNotifications() {
        let center = UNUserNotificationCenter.current()
        center.delegate = notificationDelegate
        //Here we are creating a new Category that allows us to handle Dismiss Actions
        let defaultCategory = UNNotificationCategory(identifier: "DEFAULT", actions: [], intentIdentifiers: [], options: .customDismissAction)
        //Add it to our array of Category, in this case we only have one
        center.setNotificationCategories([defaultCategory])
        center.requestAuthorization(options: [.alert, .sound, .badge]) {
            (granted, error) in
            os_log("Permission granted: %{public}@", type:. debug, granted.description)
            if error != nil {
                return
            }
            if granted {
                os_log("Notifications allowed", type: .debug)
            }
            else {
                os_log("Notifications denied", type: .debug)
            }
  
            // 2. Attempt registration for remote notifications on the main thread
            DispatchQueue.main.async {
                UIApplication.shared.registerForRemoteNotifications()
            }
        }
    }
```

Wenn Sie jetzt Push-Benachrichtigungen senden, müssen Sie eine Kategorie hinzufügen. In diesem Fall wurde sie &quot;STANDARD&quot; genannt.

![](assets/tracking_push.png)

Um dann das **[!UICONTROL Verwerfen]** zu handhaben und Tracking-Daten zu senden, müssen Sie Folgendes hinzufügen:

```
func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
        let userInfo = response.notification.request.content.userInfo
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            print("Dismiss Action")
            let deliveryId = userInfo["_dId"] as? String
            let broadlogId = userInfo["_mId"] as? String
            let acsDeliveryTracking = userInfo["_acsDeliveryTracking"] as? String
            /*
            This is to handle deliveries created before 21.1 release or deliveries with custom template where acsDeliveryTracking is not available.
            */
            if( acsDeliveryTracking == nil ) {
                acsDeliveryTracking = "on";
            }
            if (deliveryId != nil && broadlogId != nil && acsDeliveryTracking?.caseInsensitiveCompare("on") == ComparisonResult.orderedSame) {

            //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                
            //Else comment out the above line and uncomment the line below
        
                //ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])   
            }
        default:
            ////MORE CODE
        }
        completionHandler()
    }
```

### Implementieren des Öffnungs-Tracking {#push-open-tracking-iOS}

Sie müssen &quot;1&quot; und &quot;2&quot; senden, da der Anwender zum Öffnen der App zunächst auf die Benachrichtigung klicken muss. Wenn die App nicht über eine Push-Benachrichtigung gestartet/geöffnet wird, treten keine Tracking-Ereignisse auf.

Weitere Informationen zu Sendungen, die vor Version 21.1 erstellt wurden, oder Sendungen mit benutzerdefinierter Vorlage finden Sie in diesem [Abschnitt](../../administration/using/push-tracking.md#about-push-tracking).

```
import Foundation
import UserNotifications
import UserNotificationsUI
 
class NotificationDelegate: NSObject, UNUserNotificationCenterDelegate {
 
    // Called when user clicks the push notification or also called from willPresent()
    func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
 
        let userInfo = response.notification.request.content.userInfo
        os_log("App push data %{public}@, in userNotificationCenter:didReceive()", type: .debug, userInfo)
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            //This is to handle the Dismiss Action
            let deliveryId = userInfo["_dId"] as? String
            let broadlogId = userInfo["_mId"] as? String
            let acsDeliveryTracking = userInfo["_acsDeliveryTracking"] as? String
            /*
            This is to handle deliveries created before 21.1 release or deliveries with custom template where acsDeliveryTracking is not available.
            */
            if( acsDeliveryTracking == nil ) {
                acsDeliveryTracking = "on";
            }
            if (deliveryId != nil && broadlogId != nil && acsDeliveryTracking?.caseInsensitiveCompare("on") == ComparisonResult.orderedSame) {

            //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                
            //Else comment out the above line and uncomment the line below
        
                //ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])

            }
        default:
            //This is to handle the tracking when the app opens
            let deliveryId = userInfo["_dId"] as? String
            let broadlogId = userInfo["_mId"] as? String
            let acsDeliveryTracking = userInfo["_acsDeliveryTracking"] as? String
            /*
            This is to handle deliveries created before 21.1 release or deliveries with custom template where acsDeliveryTracking is not available.
            */
            if( acsDeliveryTracking == nil ) {
                acsDeliveryTracking = "on";
            }
            if (deliveryId != nil && broadlogId != nil && acsDeliveryTracking?.caseInsensitiveCompare("on") == ComparisonResult.orderedSame) {
            //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                
            //Else comment out the above line and uncomment the line below
        
                //ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])                
                
            //If you are using ACPCore v2.3.0 or later, use the next line.

                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
                
            //Else comment out the above line and uncomment the line below
        
                //ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
                
            }
        }
        completionHandler()
    }
}
```

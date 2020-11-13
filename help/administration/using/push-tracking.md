---
title: Implementieren von Push-Tracking
description: Mit diesem Dokument können Sie sicherstellen, dass das Tracking von Push-Benachrichtigungen unter iOS und Android richtig implementiert wurde.
page-status-flag: never-activated
uuid: 961aaeb5-6948-4fd2-b8d7-de4510c10566
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
discoiquuid: 23b4212e-e878-4922-be20-50fb7fa88ae8
context-tags: mobileApp,overview
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '834'
ht-degree: 100%

---


# Implementieren von Push-Tracking {#push-tracking}

## Informationen zu Push-Tracking {#about-push-tracking}

Um sicherzustellen, dass die Push-Benachrichtigung vollständig entwickelt wurde, müssen Sie dafür sorgen, dass der Tracking-Anteil richtig implementiert wurde.
Dies setzt voraus, dass Sie die ersten Teile der Implementierung von Push-Benachrichtigungen bereits implementiert haben:

* Registrieren des App-Anwenders
* Verarbeiten einer Push-Benachrichtigung

Das Push-Tracking ist in drei Typen unterteilt:

* **Push-Impressionen**: Wenn eine Push-Benachrichtigung an das Gerät gesendet wurde und im Benachrichtigungs-Center sitzt, aber noch nicht angefasst wurde.  Dies gilt als Impression.  In den meisten Fällen sollte die Zahl der Impressionen ähnlich oder gar identisch mit der gesendeten Zahl sein. Dadurch wird sichergestellt, dass das Gerät die Nachricht erhalten und diese Informationen an den Server zurückgegeben hat.

* **Push-Klick**: Wenn eine Push-Benachrichtigung an das Gerät gesendet wurde und der Anwender auf das Gerät geklickt hat.  Der Anwender wollte die Benachrichtigung entweder ansehen oder verwerfen. Wenn er sie angesehen hat, wird sie beim Push-Öffnungs-Tracking berücksichtigt.

* **Push-Öffnung**: Wenn eine Push-Benachrichtigung an das Gerät gesendet wurde und der Anwender auf die Benachrichtigung geklickt hat, wodurch die App geöffnet wurde.  Dies ist ähnlich der Push-Klick-Kategorie mit dem Unterschied, dass keine Push-Öffnung ausgelöst wird, wenn die Benachrichtigung verworfen wird.

Um das Tracking für Campaign Standard zu implementieren, muss die Mobile App &quot;Mobile SDK&quot; enthalten. Diese SDKs sind über Adobe Mobile Services verfügbar. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../administration/using/configuring-a-mobile-application.md).

Zum Senden von Tracking-Daten müssen drei Variablen gesendet werden. Zwei davon gehören zu den von Campaign Standard empfangenen Daten, eine ist eine Aktionsvariable, die bestimmt, ob es sich um eine **Impression**, einen **Klick** oder eine **Öffnung** handelt.

| Variable | Wert |
|:-:|:-:|
| broadlogId | _mId aus Daten |
| deliveryId | _dId aus Daten |
| Aktion | 1 für &quot;Öffnung&quot;, 2 für &quot;Klick&quot; und 7 für &quot;Impression&quot; |

## Implementierung für Android {#implementation-android}

### Implementieren des Push-Impression-Tracking {#push-impression-tracking-android}

Für das Impression-Tracking müssen Sie bei einer Aktion den Wert &quot;7&quot; senden, wenn die Funktion **[!UICONTROL trackAction()]** aufgerufen wird.

```
@Override
public void onMessageReceived(RemoteMessage remoteMessage) {
....{Handle push messages}....
  if (data.size() > 0) {
    String deliveryId = data.get("_dId");
    String messageId = data.get("_mId");
    HashMap<String, String> contextData = new HashMap<>();
    if (deliveryId != null && messageId != null) {
                contextData.put("deliveryId", deliveryId);
                contextData.put("broadlogId", messageId);
                contextData.put("action", "7");
                MobileCore.trackAction("tracking", contextData);
    }
  }
}
```

### Implementieren des Klick-Tracking {#push-click-tracking-android}

Für das Klick-Tracking müssen Sie bei einer Aktion den Wert &quot;2&quot; senden, wenn die Funktion **[!UICONTROL trackAction()]** aufgerufen wird.

Beim Klick-Tracking müssen zwei Szenarien behandelt werden:

* Der Anwender sieht die Benachrichtigung, löscht sie jedoch.
* Der Anwender sieht die Benachrichtigung und klickt darauf, sodass nun das Öffnungs-Tracking erfolgt.

Dazu müssen Sie zwei Intents verwenden: eine zum Klicken auf die Benachrichtigung und eine andere zum Verwerfen der Benachrichtigung.

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
  
        HashMap<String, Object> contextData = new HashMap<>();
  
        //We only send the click tracking since the user dismissed the notification
        if (deliveryId != null && messageId != null) {
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
            contextData.put("action", "1");
            MobileCore.trackAction("tracking", contextData);
        }
    }
}
```

### Implementieren des Öffnungs-Tracking {#push-open-tracking-android}

Sie müssen &quot;1&quot; und &quot;2&quot; senden, da der Anwender zum Öffnen der App zunächst auf die Benachrichtigung klicken muss. Wenn die App nicht über eine Push-Benachrichtigung gestartet/geöffnet wird, treten keine Tracking-Ereignisse auf.

Um das Öffnen verfolgen zu können, müssen Sie einen Intent erstellen. Intent-Objekte ermöglichen es dem Android-OS, Ihre Methode aufzurufen, wenn bestimmte Aktionen ausgeführt werden. In diesem Fall ist es das Klicken auf die Benachrichtigung, um die App zu öffnen.

Dieser Code basiert auf der Implementierung des Klick-Impression-Tracking. Mit festgelegtem **[!UICONTROL Intent]** müssen Sie jetzt Tracking-Daten zurück an Adobe Campaign Standard senden. In diesem Fall müssen Sie den **[!UICONTROL Öffnungs-Intent]** so definieren, dass eine bestimmte Ansicht in Ihrer App geöffnet wird. Dadurch wird die onResume-Methode mit den Benachrichtigungsdaten im **[!UICONTROL Intent-Objekt]** aufgerufen.

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
        //Looks it was opened based on the notification, lets get the tracking we passed on.
        String deliveryId = data.getString("_dId");
        String messageId = data.getString("_mId");
  
        HashMap<String, Object> contextData = new HashMap<>();
  
        if (deliveryId != null && messageId != null) {
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
  
            //Send Click Tracking since the user did click on the notification
            contextData.put("action", "2");
            MobileCore.trackAction("tracking", contextData);
  
            //Send Open Tracking since the user opened the app
            contextData.put("action", "1");
            MobileCore.trackAction("tracking", contextData);
        }
    }
}
```

## Implementierung für iOS {#implementation-iOS}

### Implementieren des Push-Impression-Tracking {#push-impression-tracking-iOS}

Für das Impression-Tracking müssen Sie bei einer Aktion den Wert &quot;7&quot; senden, wenn die Funktion **[!UICONTROL trackAction()]** aufgerufen wird.

Um zu verstehen, wie iOS-Benachrichtigungen funktionieren, müssen die drei Status einer App beschrieben werden:

* **Vordergrund**: Wenn die App aktuell aktiv ist und sich derzeit auf dem Bildschirm befindet (im Vordergrund).
* **Hintergrund**: Wenn die App sich nicht auf dem Bildschirm befindet, der Prozess jedoch nicht geschlossen ist. Wenn Sie auf die Schaltfläche &quot;Startseite&quot; doppelklicken, werden in der Regel alle im Hintergrund befindlichen Apps angezeigt.
* **Aus/geschlossen**: Eine App, deren Prozess beendet wurde.

Wenn eine App geschlossen ist, ruft Apple die App erst nach ihrem Neustart auf. Das bedeutet, dass Sie nicht erfahren können, wann die Benachrichtigung unter iOS empfangen wurde.

Damit das **[!UICONTROL Impression]**-Tracking auch dann funktioniert, wenn sich die App im Hintergrund befindet, müssen wir **[!UICONTROL Content-Available]** senden, um der App mitzuteilen, dass ein Tracking durchgeführt werden soll.

>[!CAUTION]
>
>Das Impression-Tracking in iOS ist nicht präzise und sollte nicht als zuverlässig betrachtet werden.

Der folgende Code richtet sich an die App im Hintergrund:

```
// In didReceiveRemoteNotification event handler in AppDelegate.m
  
//In order to handle push notification when only in background with content-available: 1
func application(_ application: UIApplication, didReceiveRemoteNotification userInfo: [AnyHashable : Any], fetchCompletionHandler completionHandler: @escaping (UIBackgroundFetchResult) -> Void) {
  
        //Check if the app is not in the foreground right now
        if(UIApplication.shared.applicationState != .active) {
            let deliveryId = userInfo["_dId"] as? String
            let broadlogId = userInfo["_mId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
               ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"7"])
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
        if (deliveryId != nil && broadlogId != nil) {
             ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"7"])
        }
        completionHandler([.alert,.sound])
    }
```

### Implementieren des Klick-Tracking {#push-click-tracking-iOS}

Für das Klick-Tracking müssen Sie bei einer Aktion den Wert &quot;2&quot; senden, wenn die Funktion **[!UICONTROL trackAction()]** aufgerufen wird.

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
            if (deliveryId != nil && broadlogId != nil) {
                ADBMobile.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            ////MORE CODE
        }
        completionHandler()
    }
```

### Implementieren des Öffnungs-Tracking {#push-open-tracking-iOS}

Sie müssen &quot;1&quot; und &quot;2&quot; senden, da der Anwender zum Öffnen der App zunächst auf die Benachrichtigung klicken muss. Wenn die App nicht über eine Push-Benachrichtigung gestartet/geöffnet wird, treten keine Tracking-Ereignisse auf.

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
            if (deliveryId != nil && broadlogId != nil) {
                ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            //This is to handle the tracking when the app opens
            let deliveryId = userInfo["_dId"] as? String
            let broadlogId = userInfo["_mId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
                ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
            }
        }
        completionHandler()
    }
}
```

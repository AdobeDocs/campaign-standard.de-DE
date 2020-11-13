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
source-wordcount: '726'
ht-degree: 100%

---


# Implementieren des lokalen Tracking {#local-tracking}

## Über das lokale Tracking {#about-local-tracking}

Auf dieser Seite erfahren Sie, wie Sie sicherstellen, dass das lokale Benachrichtigungs-Tracking korrekt implementiert wurde. Beachten Sie, dass dies voraussetzt, dass die lokale Benachrichtigung bereits konfiguriert wurde.

Das Tracking lokaler Benachrichtigungen kann in drei Typen unterteilt werden:

* **Lokale Impressionen**: Wenn eine lokale Benachrichtigung an das Gerät gesendet wurde und im Benachrichtigungs-Center vorhanden ist, aber noch keine Aktivität stattgefunden hat. In den meisten Fällen sollte die Zahl der Impressionen ähnlich oder gar identisch mit der gesendeten Zahl sein. Dadurch wird sichergestellt, dass das Gerät die Nachricht erhalten hat und diese Informationen an den Server zurückgibt.

* **Lokaler Klick**: Wenn eine lokale Benachrichtigung an das Gerät gesendet wurde und der Anwender auf das Gerät geklickt hat. Der Anwender wollte die Benachrichtigung entweder ansehen oder verwerfen. Wenn er sie angesehen hat, wird sie beim lokalen Öffnungs-Tracking berücksichtigt.

* **Lokale Öffnung**: Wenn eine lokale Benachrichtigung an das Gerät gesendet wurde und der Anwender auf die Benachrichtigung geklickt hat, wodurch die App geöffnet wurde. Dies ist ähnlich der lokalen Klick-Kategorie mit dem Unterschied, dass keine lokale Öffnung ausgelöst wird, wenn die Benachrichtigung verworfen wird.

Um das Tracking für Adobe Campaign Standard zu implementieren, muss die Mobile App das Mobile SDK in die App integrieren. Diese SDKs sind in [!DNL Adobe Mobile Services] verfügbar.

Zum Senden von Tracking-Daten müssen drei Variablen gesendet werden. Zwei davon gehören zu den von Adobe Campaign empfangenen Daten und die dritte ist eine Aktionsvariable, die bestimmt, ob es sich um eine Impression, einen Klick oder eine Öffnung handelt.

| Variable | Wert |
| :-: | :-: |
| deliveryId | &quot;deliveryId&quot; aus den eingehenden Daten (ähnlich dem Push-Tracking, wobei &quot;_dld&quot; verwendet wird) |
| broadlogId | &quot;broadlogId&quot; aus den eingehenden Daten (ähnlich dem Push-Tracking, wobei &quot;_mld&quot; verwendet wird) |
| Aktion | &quot;1&quot; für Öffnung, &quot;2&quot; für Klick und &quot;7&quot; für Impression |

## Implementieren des lokalen Impression-Tracking {#implement-local-impression-tracking}

Für das Impression-Tracking müssen Sie bei einer Aktion den Wert &quot;7&quot; senden, wenn die Funktion collectMessageInfo() oder trackAction() aufgerufen wird.

### Für Android {#implement-local-impression-tracking-android}

Das Adobe Experience Platform Mobile SDK startet beim Auslösen das Impression-Tracking für lokale Benachrichtigungen.

### Für iOS {#implement-local-impression-tracking-ios}

Um zu erklären, wie das Impression Tracking implementiert wird, müssen wir die drei Zustände einer App verstehen:

* **Vordergrund**: Wenn die App aktuell aktiv ist und sich auf dem Bildschirm im Vordergrund befindet.

* **Hintergrund**: Wenn die App sich nicht auf dem Bildschirm befindet, der Prozess jedoch nicht geschlossen ist. Wenn Sie auf die Schaltfläche &quot;Startseite&quot; doppelklicken, werden in der Regel alle im Hintergrund befindlichen Apps angezeigt.

* **Aus/geschlossen**: Wenn der App-Prozess beendet wurde. Wenn eine App geschlossen ist, ruft Apple die App erst nach ihrem Neustart auf. Dies bedeutet, dass Sie nie wirklich wissen können, wann die Benachrichtigung unter iOS empfangen wurde.

Damit das Impression-Tracking auch dann funktioniert, wenn sich die App im Hintergrund befindet, müssen wir &quot;Content-Available&quot; senden, um der App mitzuteilen, dass Tracking durchgeführt werden soll.

Das Adobe Experience Platform Mobile SDK startet beim Auslösen das Impression-Tracking für lokale Benachrichtigungen.

>[!CAUTION]
>
>Das Impression-Tracking in iOS ist nicht präzise und sollte nicht als zuverlässig betrachtet werden.

## Implementieren von Klick-Tracking {#implementing-click-tracking}

Für das Klick-Tracking müssen Sie bei einer Aktion den Wert &quot;2&quot; senden, wenn die Funktion collectMessageInfo() oder trackAction() aufgerufen wird.

### Für Android {#implement-click-tracking-android}

Beim Klick-Tracking müssen zwei Szenarien behandelt werden:

* Der Anwender sieht die Benachrichtigung, löscht sie jedoch.

* Der Benutzer sieht die Benachrichtigung und klickt darauf. Dies führt zum Öffnungs-Tracking.

Das erste Klickszenario wird vom Adobe Experience Platform Mobile SDK verfolgt.

### Für iOS {#implement-click-tracking-ios}

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

Um dann das Verwerfen zu handhaben und Tracking-Daten zu senden, müssen Sie Folgendes hinzufügen:

```
func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
        let userInfo = response.notification.request.content.userInfo
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            print("Dismiss Action")
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
                // If you're using  ACPCore v2.3.0 or later, use the line below.
                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
                // Else comment out the above line and uncomment the line below
                // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            ////MORE CODE
        }
        completionHandler()
    }
```

## Implementieren von Öffnungs-Tracking {#implement-open-tracking}

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
        //Looks it was opened based on the notification, lets get the tracking we passed on.
        Map<String, String> notificationData = (Map<String, Object>)data.getSerializableExtra("NOTIFICATION_USER_INFO");
        String deliveryId = (String)notificationData.get("deliveryId");
        String messageId = (String)notificationData.get("broadlogId");
  
  
  
        if (deliveryId != null && messageId != null) {
            HashMap<String, String> contextData = new HashMap<>();
            contextData.put("deliveryId", deliveryId);
            contextData.put("broadlogId", messageId);
  
            //Send Click Tracking since the user did click on the notification
            contextData.put("action", "2");
            // If you're using  ACPCore v1.4.0 or later, use the next line.
            MobileCore.collectMessageInfo(contextData);
            // Else comment out the above line and uncomment the line below
            // MobileCore.trackAction("tracking", contextData);
  
            //Send Open Tracking since the user opened the app
            contextData.put("action", "1");
            // If you're using  ACPCore v1.4.0 or later, use the next line.
            MobileCore.collectMessageInfo(contextData);
            // Else comment out the above line and uncomment the line below
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
  
    // Called when user clicks the local notification or also called from willPresent()
    func userNotificationCenter(_ center: UNUserNotificationCenter, didReceive response: UNNotificationResponse, withCompletionHandler completionHandler: @escaping () -> Void) {
  
        let userInfo = response.notification.request.content.userInfo
        os_log("App push data %{public}@, in userNotificationCenter:didReceive()", type: .debug, userInfo)
        switch response.actionIdentifier {
        case UNNotificationDismissActionIdentifier:
            //This is to handle the Dismiss Action
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
            // If you're using  ACPCore v2.3.0 or later, use the line below.
                ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            // Else comment out the above line and uncomment the line below
            // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
            }
        default:
            //This is to handle the tracking when the app opens
            let deliveryId = userInfo["deliveryId"] as? String
            let broadlogId = userInfo["broadlogId"] as? String
            if (deliveryId != nil && broadlogId != nil) {
               // If you're using  ACPCore v2.3.0 or later, use the line below.
               ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
               ACPCore.collectMessageInfo(["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
               // Else comment out the above line and uncomment the line below
               // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
               // ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"1"])
            }
        }
        completionHandler()
    }
}
```

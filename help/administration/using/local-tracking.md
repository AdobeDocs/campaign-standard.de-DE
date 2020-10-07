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
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '726'
ht-degree: 9%

---


# Implementieren der lokalen Verfolgung {#local-tracking}

## Informationen zur lokalen Verfolgung {#about-local-tracking}

Auf dieser Seite erfahren Sie, wie Sie sicherstellen können, dass die lokale Benachrichtigungsverfolgung korrekt implementiert wurde. Beachten Sie, dass dies bedeutet, dass die lokale Benachrichtigung bereits konfiguriert wurde.

Die Verfolgung lokaler Benachrichtigungen kann in drei Typen unterteilt werden:

* **Lokale Impressionen** : Wenn eine lokale Benachrichtigung an das Gerät gesendet wurde und im Benachrichtigungszentrum sitzt, aber überhaupt nicht berührt wurde. In den meisten Fällen sollte die Anzahl der Impressionen ähnlich sein, wenn nicht mit der der gelieferten Nummer identisch sein. Es stellt sicher, dass das Gerät die Meldung erhalten hat und diese Informationen an den Server zurückübergibt.

* **Lokaler Klick** : Wenn eine lokale Benachrichtigung an das Gerät gesendet wurde und der Benutzer auf das Gerät geklickt hat. Der Benutzer wollte entweder die Benachrichtigung (die wiederum zur lokalen offenen Verfolgung wechselt) Ansicht oder die Benachrichtigung schließen.

* **Lokal geöffnet** : Wenn eine lokale Benachrichtigung an das Gerät gesendet wurde und der Benutzer auf die Benachrichtigung geklickt hat, die die Anwendung geöffnet hat. Dies ähnelt dem lokalen Klick, es sei denn, ein lokaler Aufruf wird nicht ausgelöst, wenn die Benachrichtigung abgelehnt wurde.

Um die Verfolgung für Adobe Campaign Standard zu implementieren, muss die Mobilanwendung das Mobile SDK in die Anwendung einschließen. Diese SDKs sind in verfügbar [!DNL Adobe Mobile Services].

Zum Senden von Verfolgungsinformationen müssen drei Variablen gesendet werden: Zwei davon sind Teil der von Adobe Campaign erhaltenen Daten und die andere ist eine Aktionsvariable, die vorgibt, ob es sich um eine Impression, ein Klick oder ein Öffnen handelt.

| Variable | Wert |
| :-: | :-: |
| deliveryId | &quot;deliveryId&quot;aus eingehenden Daten (ähnlich wie bei der Push-Verfolgung, bei der &quot;_dld&quot;verwendet wird) |
| broadlogId | &quot;breitlogId&quot;aus eingehenden Daten (ähnlich wie bei der Push-Verfolgung, bei der &quot;_mld&quot;verwendet wird) |
| Aktion | &quot;1&quot;für &quot;Öffnen&quot;, &quot;2&quot;für &quot;Klicken&quot;und &quot;7&quot;für &quot;Impression&quot; |

## Implementieren der lokalen Impressionsverfolgung {#implement-local-impression-tracking}

Zur Impressionsverfolgung müssen Sie den Wert &quot;7&quot;für die Aktion senden, wenn Sie die Funktionen &quot;collectionMessageInfo()&quot;oder &quot;trackAction()&quot;aufrufen.

### Für Android {#implement-local-impression-tracking-android}

Das Adobe Experience Platform Mobile SDK Beginn die Impressionsverfolgung für lokale Benachrichtigungen, wenn diese ausgelöst werden.

### Für iOS {#implement-local-impression-tracking-ios}

Um zu erklären, wie die Impressionsverfolgung implementiert wird, müssen wir die drei Zustände einer Anwendung verstehen:

* **Vordergrund**: wenn die Anwendung aktuell aktiv ist und sich auf dem Bildschirm im Vordergrund befindet.

* **Hintergrund**: wenn die Anwendung nicht auf dem Bildschirm angezeigt wird, der Prozess aber auch nicht geschlossen wird. Wenn Sie mit der Dublette auf die Schaltfläche &quot;Startseite&quot;klicken, werden in der Regel alle Anwendungen im Hintergrund angezeigt.

* **Aus/geschlossen**: wenn der Antragsprozess beendet wurde. Wenn eine Anwendung geschlossen wird, ruft Apple sie erst nach dem Neustart der Anwendung auf. Das bedeutet, dass Sie nie wirklich wissen können, wann die Benachrichtigung unter iOS erhalten wurde.

Damit die Impressionsverfolgung während der Ausführung der Anwendung im Hintergrund weiterhin funktioniert, müssen wir &quot;Content-Available&quot;senden, um der Anwendung mitzuteilen, dass die Verfolgung durchgeführt werden muss.

Das Adobe Experience Platform Mobile SDK Beginn die Impressionsverfolgung für lokale Benachrichtigungen, wenn diese ausgelöst werden.

>[!CAUTION]
>
>Die iOS-Impressionsverfolgung ist nicht korrekt und sollte nicht zuverlässig überprüft werden.

## Implementierung der Klick-Verfolgung {#implementing-click-tracking}

Zur Klick-Verfolgung müssen Sie den Wert &quot;2&quot;für die Aktion senden, wenn Sie die Funktionen &quot;collectionMessageInfo()&quot;oder &quot;trackAction()&quot;aufrufen.

### Für Android {#implement-click-tracking-android}

Beim Klick-Tracking müssen zwei Szenarien behandelt werden:

* Der Anwender sieht die Benachrichtigung, löscht sie jedoch.

* Der Benutzer sieht die Benachrichtigung und klickt darauf. Dies wird zu einer offenen Verfolgung.

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

Um dann den Ausschluss zu bearbeiten und eine Verfolgungsinformationen zu senden, müssen Sie Folgendes hinzufügen:

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

## Implementierung der offenen Verfolgung {#implement-open-tracking}

Sie müssen &quot;1&quot;und &quot;2&quot;senden, da der Benutzer auf die Benachrichtigung klicken muss, um die Anwendung zu öffnen. Wenn die Anwendung nicht über eine lokale Benachrichtigung gestartet/geöffnet wird, treten keine Ereignis zur Verfolgung auf.

### Für Android {#implement-open-tracking-android}

Um offen nachzuverfolgen, müssen wir Absichten schaffen. Zielobjekte ermöglichen es Android OS, Ihre Methode aufzurufen, wenn bestimmte Aktionen durchgeführt werden. In diesem Fall klicken Sie auf die Benachrichtigung, um die App zu öffnen.

Dieser Code basiert auf der Implementierung des Klick-Impression-Tracking. Mit der Einstellung &quot;Absicht&quot;müssen Sie jetzt Verfolgungsinformationen zurück an Adobe Campaign senden. In diesem Fall wird die Android-Ansicht([!DNL Activity]), die die Benachrichtigung auslöste, durch das Klicken auf den Benutzer geöffnet oder in den Vordergrund gestellt. Das intent-Objekt in [!DNL Activity] enthält die Benachrichtigungsdaten, die zur Verfolgung von &quot;open&quot;verwendet werden können.

MainActivity.java (extension [!DNL Activity])

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

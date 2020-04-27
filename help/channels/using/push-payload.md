---
title: Understanding Campaign Standard Push Notifications Payload Structure
description: Dieses Dokument soll die Struktur der Nutzlast beschreiben, die in mobilen Anwendungen empfangen wird.
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
source-git-commit: 302159577f5a7d917ba253994ff23c4980d518e5

---


# Understanding Campaign Standard Push Notifications Payload Structure {#push-payload}

Mit Adobe Campaign können Sie personalisierte und segmentierte Push-Benachrichtigungen auf iOS- und Android-Mobilgeräten an mobile Anwendungen (mobile App) senden.

Jede Push-Benachrichtigung, die auf einer mobilen App empfangen wird, enthält einige Informationen, die von der App verwendet werden, um die Push-Benachrichtigung anzuzeigen, wenn eine Push-Benachrichtigung gesendet wird, und wahrscheinlich auch einige weitere Berechnungen durchführen, insbesondere wenn eine Push-Benachrichtigung gesendet wird.

Diese Informationen werden vom Code der mobilen App in einem Ereignis-Handler empfangen, der angibt, dass eine Push-Benachrichtigung empfangen wurde. Wenn Sie Push-Benachrichtigungen von Adobe Campaign Standard senden, enthalten die in der mobilen App erhaltenen Informationen möglicherweise auch Campaign Standard-spezifische Informationen, die verwendet werden können, um einige von Campaign Standard bereitgestellte Funktionen zu nutzen. Darüber hinaus kann die Nutzlast benutzerdefinierte Daten enthalten, die von der mobilen App genutzt werden können.

Dieses Dokument beschreibt die Struktur der Nutzlast, die in einer mobilen App empfangen wird, wenn eine Push-Benachrichtigung erfolgreich von Adobe Campaign Standard an eine App gesendet wurde.

>[!NOTE]
>
>Die Payload-Struktur hängt vom Typ der mobilen App ab (d. h. iOS-App, FCM-fähige Android-App).

## Push-Nutzdatenstruktur {#push-payload-structure}

In diesem Abschnitt wird die Struktur einer Beispielnutzlast für verschiedene mobile Plattformen beschrieben und die darin enthaltenen Hauptattribute beschrieben. Dies ist die Struktur der Nutzlast, die im Mobilanwendungscode im Ereignis-Handler empfangen wird und angibt, dass eine Push-Benachrichtigung empfangen wurde.

Die Nutzlastattribute und ihre Werte variieren je nach den Konfigurationen in den erweiterten Optionen für Push-Benachrichtigungen. Dieser Abschnitt enthält auch eine Zuordnung zwischen diesen Konfigurationen in der Benutzeroberfläche des Campaign Standards und den Attributen in der Nutzlast, um zu klären, wie sich die Nutzlast bei der Konfiguration einer Option in Campaign Standard ändert.

### Für iOS Mobile App {#payload-structure-ios}

**Beispiel-Nutzlast, die von Adobe Campaign an die iOS-App gesendet wird:**

```
{

    "aps":{

            "alert":{

                    "body":"This is the content of my push notification",

                    "title":"Push Notification Title"

            },

            "content-available":1,

            "category":"NEW_MESSAGE_CATEGORY",

            "badge":2,

            "mutable-content":1,

            "sound":"default"

        },

    "custom_field1":"custom_value1",

    "custom_field2":"custom_value2",

    "media-attachment-url":"https://2.img-dpreview.com/files/p/articles/9440145363/Creative_Cloud.jpeg",

    "uri":"https://mydeeplinkurl.com",

    "_dId":"56c4",

    "_mId":"h138a"} 
```

**JSON-Beispielnutzlast zur Verwendung mit[iOS APNS Tester](https://pushtry.com/)**

```
{

  "aps": {

    "alert": {

      "title": "Push Notification Title",

      "body": "body of push"

    },

    "badge": 33,

    "sound": "default"

  },

  "custom_field1": "custom_value1",

  "uri": "https://mydeeplinkurl.com"

}
```

Der wichtigste Abschnitt der Nutzlast ist das App-Wörterbuch, das von Apple definierte Schlüssel enthält und bestimmt, wie das System, das die Benachrichtigung erhält, den Benutzer warnt, wenn überhaupt. Dieser Abschnitt enthält vordefinierte Schlüssel, mit denen die mobile App das Verhalten der Push-Benachrichtigung formuliert.

Ausführliche Informationen zu den Attributen in Apple finden Sie in den Apple-Entwicklerdocs: Erstellen der [Fernbenachrichtigungsnutzlast](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html#//apple_ref/doc/uid/TP40008194-CH10-SW1).

### Für Android-App {#payload-structure-android}

**Beispiel-Nutzdatenversand von Adobe Campaign an die Android-App**

```
{

  "collapseKey": "1476005",

  "priority": "high",

  "data": {

    "_dId": "d57fd6",

    "_mId": "h1685a5",

    "body": "adobe body 123",

    "category": "adobe category 123",

    "custom key 1": "value 1",

    "custom key 2": "test value 2",

    "custom key 3": "foo bar android",

    "media-attachment-url": "http://adobegiphy.com?test=123",

    "sound": "http://testcampaign.instance.com/r/?id=s1685a5,d57fd6,d57ff5",

    "title": "adobe title 123",

    "uri": "http://testcampaign.instance.com/r/?id=d1685a5,d57fd6,d57ff6",

    "badge": 1817

  }

}
```

**JSON-Beispiel-Nutzlast zur Verwendung des[Google FCM-Tester](https://pushtry.com/)**

```
{

  "to": "<==========ENTER your device token==============>",

  "collapseKey": "1476005",

  "priority": "high",

  "data": {

    "_dId": "d57fd6",

    "_mId": "h1685a5",

    "title": "adobe title 123",

    "body": "adobe body 123",

    "category": "adobe category 123",

    "custom key 1": "value 1",

    "custom key 2": "test value 2",

    "custom key 3": "foo bar android",

    "media-attachment-url": "http://adobegiphy.com?test=123",

    "sound": "http://testcampaign.instance.com/r/?id=s1685a5,d57fd6,d57ff5",

    "uri": "http://testcampaign.instance.com/r/?id=d1685a5,d57fd6,d57ff6",

    "badge": 1817

  }

}
```

Die Payload enthält eine Datenmeldung, die den gesamten Inhalt des Push-Benachrichtigungs-Versands einschließlich der benutzerdefinierten Schlüssel/Wert-Paare enthält. Die Client-App muss die Nachricht bearbeiten, um bei Bedarf Push-Benachrichtigungen zu erstellen und anzuzeigen, oder um eine andere Geschäftslogik hinzuzufügen.

Informationen zu Aspekten einer android-Nutzlast finden Sie unter [Messaging Concepts and Options (fcm)](https://firebase.google.com/docs/cloud-messaging/concept-options).

>[!NOTE]
>
>Ab Januar 2018 wurde die Unterstützung für Benachrichtigungen in Android-Nutzdaten entfernt, damit die App nachwächst und die Kontrolle an die mobile App weitergegeben werden kann, ohne dass der Benutzer mit der App interagieren muss.

### Zuordnung zwischen Campaign Standard-Konfigurationen und Nutzlastattributen {#mapping-payload}

| Konfiguration der Kampagne | Impact Attribute in iOS | Impact Attribute in Android | Description |
|:-:|:-:|:-:|:-:|
| Nachrichtentitel <br>Nachrichtentext | alert → title <br> alert → body | title <br>body | Diese Daten enthalten Details zur Warnmeldung.<br>Die Titel- und Textschlüssel geben den Inhalt der Warnung an. |
| Ton abspielen | sound | sound | Ein benutzerdefinierter Sound, der mit dem Warnhinweis wiedergegeben wird. |
| Badge-Wert | badge | badge | Ein ganzzahliger Wert, mit dem das Symbol der App gekennzeichnet wird. |
| Deeplink hinzufügen  | uri | NA | Mit einem Deeplink gelangen Benutzer direkt zu Inhalten, die in der Anwendung enthalten sind (anstatt eine Webseite zu öffnen). |
| Kategorie | category | category | So zeigen Sie benutzerdefinierte Aktionen mit einer Remote-Benachrichtigung an. <br>Mit der Kategorie-Taste kann das System die Aktionen für diese Kategorie als Schaltflächen in der Warnungs-Oberfläche anzeigen. |
| Benutzerdefinierte Felder | custom_field1, custom_field2 ... | custom_field1, custom_field2 ... | Alle benutzerspezifischen Daten, die Sie an Ihre App senden möchten. |
| URL des Rich-Media-Inhalts (Bild-, GIF-, Audio- und Videodateien)<br>(nur für iOS 10 oder höher) | media-attachment-url | NA | URL Ihrer Mediendateien, um Rich-Content zu Ihrer Benachrichtigung hinzuzufügen. <br>Wenn Sie einen Wert für diese URL angeben, wird das Flag für veränderliche Inhalte automatisch an die Nutzlast gesendet. <br> (Nur für iOS 10 oder höher) |
| Veränderliche Inhalte <br> (nur für iOS 10 oder höher) | mutable-content | NA | Die Benachrichtigungsdiensterweiterung in Ihrer App &quot;erfasst&quot;alle Remote-Benachrichtigungen mit dem Schlüssel für veränderliche Inhalte und ermöglicht Ihnen die Verarbeitung/Bearbeitung des Inhalts der Anforderungs-Nutzlast, die dann zum Anpassen der Benachrichtigung verwendet werden kann. Anwendungsfälle dieser Funktion sind das Herunterladen und Anzeigen mehrerer Medien und das Entschlüsseln aller in der Push-Nutzlast vorhandenen verschlüsselten Daten. Weitere Informationen finden Sie unter [Ändern der Nutzlast einer Remote-Benachrichtigung](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html). <br>(Nur für iOS 10 oder höher) |
| Inhalt verfügbar | content-available | NA | Wenn Sie diese Option auswählen, wird das Aufwachen einer iOS-App aktiviert, während sie sich im Hintergrund bzw. im Aussetzzustand befindet. Das Aufwachen bedeutet, dass die App im Hintergrund ausgeführt wird und der für den Empfang der Push-Benachrichtigungs-Datennutzlast zuständige Ereignis-Handler ein Steuerelement erhält und die Daten für jede Berechnung verwenden kann, einschließlich, aber nicht darauf beschränkt, benutzerdefinierte Push-Benachrichtigungen zu erstellen und dasselbe anzuzeigen. Weitere Informationen finden Sie unter [Wake up App with Notification Versand](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| URL des Rich-Media-Inhalts (Bilddateien)<br>(nur für Android verfügbar) | NA | media-attachment-url | URL der Bilddateien, um der Benachrichtigung Rich-Content hinzuzufügen. |
| NA | _mId<br>_dId | _mId <br>_dId | Werte von &quot;extenlogId&quot;und &quot;deliveryId&quot;.<br>Diese Attribute sind erforderlich, wenn Ihre App einen Tracking-Postback aufrufen möchte, der verfolgt werden soll, wenn auf die Push-Benachrichtigung geklickt/geöffnet wurde. Diese Informationen werden intern vom App-Server ohne Benutzereingriff berechnet und gesendet.<br>Informationen zu Postbacks finden Sie auf dieser [Seite](https://helpx.adobe.com/campaign/kb/config-app-in-launch.html#PIIpostback). |

### So rufen Sie Nutzlastinformationen im Code einer mobilen App ab {#payload-information}

Die Nutzlastinformationen, die vom App-Server gesendet werden, werden vom mobilen App-Code in einem Ereignis-Handler empfangen, der angibt, dass eine Push-Benachrichtigung empfangen wurde. Dieses Ereignis variiert je nach verwendeter Mobilplattform und je nachdem, ob die App im Vordergrund oder Hintergrund ausgeführt wird. Die folgende Dokumentation hilft Ihnen dabei, den Ereignis-Handler zu identifizieren, den Sie je nach Anwendungsfall bearbeiten möchten.

* iOS-Anwendungen: Abschnitt **Umgang mit Remote-Benachrichtigungen** in [Remote-Benachrichtigungen](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/HandlingRemoteNotifications.html).
* Android-Anwendungen: Nachrichten [in einer Android-Client-App empfangen](https://firebase.google.com/docs/cloud-messaging/android/receive)

**Beispiel für eine mobile iOS-App**

```
 - (void)application:(UIApplication *)application

didReceiveRemoteNotification:(NSDictionary *)userInfo {

    

    NSDictionary *apsDict = [userInfo objectForKey:@"aps"];

    NSDictionary *alertDict = [apsDict objectForKey:@"alert"];

    NSString *title = [alertDict objectForKey:@"title"];

    NSString *body = [alertDict objectForKey:@"body"];

    NSString *category = [apsDict objectForKey:@"category"];

    NSString *deliveryId = userInfo[@"_dId"];

    NSString *broadlogId = userInfo[@"_mId"];

    NSString *mediaAttachmentURL = userInfo[@"media-attachment-url"];

    NSString *deeplinkURL = userInfo[@"uri"];

    NSString *customValue1 = userInfo[@"custom_field1"];   

}
```

**Beispiel für die Android Mobile FCM-App**

```
public void onMessageReceived(RemoteMessage message) {

    Map<String, String> dataMap = message.getData();

     

    String title = dataMap.get("title");

    String body = dataMap.get("body");

    String category = dataMap.get("category");

    String deliveryId = dataMap.get("_dId");

    String broadlogId = dataMap.get("_mId");

    String mediaAttachmentURL = dataMap.get("media-attachment-url");

    String deeplinkURL = dataMap.get("uri");

    String customValue1 = dataMap.get("custom_field1");

}
```

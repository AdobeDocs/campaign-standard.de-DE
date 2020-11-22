---
solution: Campaign Standard
product: campaign
title: Die Struktur der Payload von Push-Benachrichtigungen in Campaign Standard
description: In diesem Dokument wird die Struktur der in Mobile Apps empfangenen Payload beschrieben.
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1148'
ht-degree: 100%

---


# Payload-Struktur der Push-Nachrichten verstehen {#push-payload}

Mit Adobe Campaign können Sie personalisierte und segmentierte Push-Benachrichtigungen auf iOS- und Android-Mobilgeräten an mobile Anwendungen (Mobile Apps) senden.

Jede Push-Benachrichtigung, die auf einer Mobile App empfangen wird, enthält Daten, die von der App verwendet werden, um die Push-Benachrichtigung anzuzeigen, wenn sie als Warnhinweis gesendet wird. Außerdem werden die Daten häufig zur Durchführung weiterer Berechnungen genutzt, insbesondere beim Versand einer stillen Push-Benachrichtigung.

Diese Daten werden vom Code der Mobile App in einem Event-Handler empfangen, der mitteilt, dass eine Push-Benachrichtigung empfangen wurde. Wenn Sie Push-Benachrichtigungen von Adobe Campaign Standard aus senden, enthalten die in der Mobile App empfangenen Daten möglicherweise auch Campaign Standard-spezifische Daten, die dazu dienen können, bestimmte von Campaign Standard bereitgestellte Funktionen zu nutzen. Darüber hinaus kann die Payload benutzerdefinierte Daten beinhalten, die von der Mobile App verwendet werden können.

In diesem Dokument wird die Struktur der Payload beschrieben, die in einer Mobile App empfangen wird, wenn Adobe Campaign Standard erfolgreich eine Push-Benachrichtigung an diese App sendet.

>[!NOTE]
>
>Die Struktur der Payload hängt von der Art der Mobile App ab (d. h. iOS-App, FCM-fähige Android-App).

## Payload-Struktur bei Push-Benachrichtigungen {#push-payload-structure}

In diesem Abschnitt wird die Struktur einer Beispiel-Payload für verschiedene mobile Plattformen und die darin enthaltenen Hauptattribute beschrieben. Dies ist die Struktur der Payload, die im Mobile-App-Code im Event-Handler empfangen wird und mitteilt, dass eine Push-Benachrichtigung empfangen wurde.

Die Payload-Attribute und ihre Werte variieren je nach der Konfiguration in den erweiterten Optionen für Push-Benachrichtigungen. Dieser Abschnitt enthält auch ein Mapping zwischen diesen Konfigurationen in der Benutzeroberfläche von Campaign Standard und den Attributen in der Payload, um zu veranschaulichen, wie sich die Payload bei der Konfiguration einer Option in Campaign Standard verändert.

### Für iOS-Mobile Apps {#payload-structure-ios}

**Beispiel-Payload, die von Adobe Campaign an eine iOS-App gesendet wird:**

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

**JSON-Beispiel-Payload zur Verwendung mit [iOS APNS-Tester](https://pushtry.com/)**

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

Der wichtigste Bereich der Payload ist das aps-Wörterbuch, das von Apple definierte Schlüssel enthält und bestimmt, wie das System, das die Benachrichtigung erhält, den Benutzer warnen soll (wenn überhaupt). Dieser Abschnitt enthält vordefinierte Schlüssel, mit denen die Mobile App das Verhalten der Push-Benachrichtigung formuliert.

Ausführliche Informationen zu den Attributen in aps finden Sie in der Apple-Entwicklerdokumentation: [Creating the Remote Notification Payload](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html#//apple_ref/doc/uid/TP40008194-CH10-SW1).

### Für Android-Apps {#payload-structure-android}

**Beispiel-Payload, gesendet von Adobe Campaign an Android-App**

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

**JSON-Beispiel-Payload zur Verwendung mit [Google FCM-Tester](https://pushtry.com/)**

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

Die Payload enthält eine Datennachricht, die alle Inhalte aus dem Push-Benachrichtigungsversand einschließlich der benutzerdefinierten Schlüssel/Wert-Paare umfasst. Die Client-App muss die Nachricht handhaben, um bei Bedarf Push-Benachrichtigungen zu erstellen und anzuzeigen oder um eine andere Business-Logik hinzuzufügen.

Informationen zu Aspekten einer Android-Payload finden Sie unter [Messaging Concepts and Options (fcm)](https://firebase.google.com/docs/cloud-messaging/concept-options).

>[!NOTE]
>
>Im Januar 2018 wurde die Unterstützung für Benachrichtigungen in Android-Payloads entfernt, damit die App aufgeweckt und die Kontrolle an die Mobile App weitergegeben werden kann, ohne dass der Benutzer mit der App interagieren muss.

### Mapping zwischen Campaign Standard-Konfigurationen und Payload-Attributen {#mapping-payload}

| Campaign-Konfiguration | Betroffene Attribute in iOS | Betroffene Attribute in Android | Beschreibung |
|:-:|:-:|:-:|:-:|
| Nachrichtentitel <br>Nachrichtentext | alert → title <br> alert → body | title <br>body | Diese Daten enthalten Details zur Warnmeldung.<br>Die Titel- und Textschlüssel geben den Inhalt der Warnung wieder. |
| Ton abspielen | sound | sound | Ein benutzerdefinierter Ton, der mit der Warnung wiedergegeben wird. |
| Badge-Wert | badge | badge | Ein ganzzahliger Wert, der als Badge für das Symbol der App verwendet wird. |
| Deeplink hinzufügen  | uri | Nicht zutreffend | Mit einem Deeplink gelangen Benutzer direkt zu Inhalten, die in der Anwendung enthalten sind (anstatt eine Webseite zu öffnen). |
| Kategorie | category | category | So zeigen Sie benutzerdefinierte Aktionen mit einer Remote-Benachrichtigung an. <br>Mit der Kategorietaste kann das System die Aktionen für diese Kategorie als Schaltflächen in der Warnoberfläche anzeigen. |
| Benutzerdefinierte Felder | custom_field1, custom_field2 ... | custom_field1, custom_field2 ... | Alle benutzerdefinierten Daten, die Sie an Ihre App senden möchten. |
| URL für Rich-Media-Daten (Bild-, GIF-, Audio- und Videodateien)<br>(nur bei iOS 10 oder höher) | media-attachment-url | Nicht zutreffend | URL Ihrer Mediendateien, um Ihrer Benachrichtigung Rich-Inhalte hinzuzufügen. <br>Wenn Sie einen Wert für diese URL angeben, wird das Flag für veränderliche Inhalte (mutable-content) automatisch in die Payload gesendet. <br> (nur bei iOS 10 oder höher) |
| Veränderliche Inhalte <br> (nur bei iOS 10 oder höher) | mutable-content | Nicht zutreffend | Die Notification Service-Erweiterung in Ihrer App &quot;erfasst&quot; alle Remote-Benachrichtigungen mit dem Schlüssel &quot;mutable-content&quot; und ermöglicht Ihnen die Verarbeitung/Bearbeitung des Inhalts der Anfrage-Payload, der dann zum Anpassen der Benachrichtigung verwendet werden kann. Anwendungsbeispiele für diese Funktion sind das Herunterladen und Anzeigen mehrerer Medien, wobei alle in der Push-Payload vorhandenen verschlüsselten Daten entschlüsselt werden. Weiterführende Informationen finden Sie unter [Payload einer Remote-Benachrichtigung ändern](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html). <br>(nur bei iOS 10 oder höher) |
| Inhalt verfügbar | content-available | Nicht zutreffend | Wenn Sie diese Option auswählen, wird das Aufwecken einer iOS-App aktiviert, die sie sich im Hintergrund bzw. ausgesetzten Zustand befindet. Aufwecken bedeutet, dass die App im Hintergrund ausgeführt wird und der für den Empfang der Daten-Payload der Push-Benachrichtigung zuständige Event-Handler die Kontrolle erhält und die Daten für beliebige Berechnungen verwenden kann, zum Beispiel zum Erstellen und Anzeigen benutzerdefinierter Push-Benachrichtigungen. Weiterführende Informationen finden Sie unter [App bei Benachrichtigungsversand wecken](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| URL der Rich-Media-Inhalte (Grafikdateien)<br>(nur bei Android verfügbar) | Nicht zutreffend | media-attachment-url | URL der Grafikdateien, um der Benachrichtigung Rich-Inhalte hinzuzufügen. |
| Nicht zutreffend | _mId<br>_dId | _mId <br>_dId | Werte von &quot;broadlogId&quot; und &quot;deliveryId&quot;.<br>Diese Attribute sind erforderlich, wenn Ihre App einen Tracking-Postback aufrufen möchte, um zu verfolgen, wann die Push-Benachrichtigung angeklickt/geöffnet wurde. Diese Daten werden vom App-Server ohne Benutzereingriff intern berechnet und gesendet.<br>Informationen zu Postbacks finden Sie auf dieser [Seite](https://helpx.adobe.com/de/campaign/kb/config-app-in-launch.html#PIIpostback). |

### So rufen Sie Payload-Daten in Mobile-App-Code ab {#payload-information}

Die Payload-Daten, die vom App-Server gesendet werden, werden vom Mobile-App-Code in einem Event-Handler empfangen, der mitteilt, dass eine Push-Benachrichtigung empfangen wurde. Dieses Ereignis variiert je nach verwendeter mobiler Plattform und je nachdem, ob die App im Vordergrund oder Hintergrund ausgeführt wird. Die folgende Dokumentation hilft Ihnen dabei, den Event-Handler zu ermitteln, den Sie je nach Anwendungsfall benötigen.

* iOS-Apps: Abschnitt **Umgang mit Remote-Benachrichtigungen** in [Remote-Benachrichtigungen](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/HandlingRemoteNotifications.html).
* Android-Apps: [Empfangen von Nachrichten in einer Android-Client-App](https://firebase.google.com/docs/cloud-messaging/android/receive)

**Beispiel für eine iOS-Mobile-App**

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

**Beispiel für eine Android-Mobile-FCM-App**

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

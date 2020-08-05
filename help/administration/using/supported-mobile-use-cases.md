---
title: Anwendungsfälle für Mobilgeräte, die in Adobe Campaign Standard mit den Adobe Experience Platform SDKs unterstützt werden
description: Dieses Dokument enthält Informationen zur Unterstützung von Anwendungsfällen für Mobilgeräte.
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
source-git-commit: 5e1a0bea0a0b43b20830ffdb58c0b53d1ff1e36a
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 1%

---


# Unterstützte Anwendungsfälle für Mobilgeräte in Adobe Campaign Standard {#mobile-use-cases}

Auf dieser Seite finden Sie die Liste aller Mobilgeräte-Nutzungsszenarien, die bei der [!DNL Adobe Campaign Standard] Verwendung des [!DNL Adobe Experience Platform SDKs]. Beachten Sie, dass bei der Unterstützung dieser Anwendungsfälle die Installation und Konfiguration der Variablen [!DNL Adobe Experience Platform SDKs], [!DNL Adobe Experience Platform Launch]und [!DNL Adobe Campaign Standard]erforderlich ist. Weiterführende Informationen dazu finden Sie auf dieser [Seite](../../administration/using/configuring-a-mobile-application.md).

Adobe Campaign Standard unterstützt die folgenden Anwendungsfälle:

* [Mobiles Profil in Campaign Standard registrieren](../../administration/using/supported-mobile-use-cases.md#register-mobile-profile)
* [Push-Token an Campaign Standard senden](../../administration/using/supported-mobile-use-cases.md#send-push-token)
* [Mobiles Profil mit benutzerspezifischen Daten aus Ihrer Anwendung aufwerten](../../administration/using/supported-mobile-use-cases.md#enrich-mobile-profile-custom)
* [Aufwerten eines mobilen Profils mit Lebenszyklusdaten aus Ihrer Anwendung](../../administration/using/supported-mobile-use-cases.md#enrich-mobile-profile-lifecycle)
* [Benutzerinteraktion mit Push-Benachrichtigungen verfolgen](../../administration/using/supported-mobile-use-cases.md#track-user-push)
* [Implementieren eines benutzerdefinierten Ereignisses in Ihrer mobilen App, um In-App-Nachrichten auszulösen](../../administration/using/supported-mobile-use-cases.md#custom-event-inapp)
* [Verknüpfungsfelder für zusätzliche Authentifizierung für die Profil-Vorlage festlegen, die auf In-App-Nachrichten basiert](../../administration/using/supported-mobile-use-cases.md#linkage-fields-inapp)

Zum Konfigurieren dieser Anwendungsfälle benötigen Sie die folgenden Erweiterungen aus [!DNL Experience Platform Launch]:

* **[!DNL Adobe Campaign Standard]** <br>Informationen zum Installieren und Konfigurieren der Campaign Standard-Erweiterung finden Sie unter Campaign Standard-Erweiterung [konfigurieren in Experience Platform Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard#configure-the-campaign-standard-extension-in-experience-platform-launch).
* **[!DNL Mobile Core]**, der automatisch installiert wird. <br>Weitere Informationen zur Mobile Core Extension finden Sie unter [Mobile Core](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core).
* **[!DNL Profile]**, der automatisch installiert wird. <br>Weitere Informationen zur Profil-Erweiterung finden Sie unter [Profil](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/profile).

## Mobiles Profil in Campaign Standard registrieren {#register-mobile-profile}

### Mit iOS {#register-mobile-profile-ios}

Unter iOS sind folgende [!DNL Experience Platform APIs] erforderlich:

* **[!UICONTROL Lebenszyklus-Beginn]**, wenn die App gestartet wird und sich die App im Vordergrund befindet.
* **[!UICONTROL Lebenszykluspause]**, wenn sich die App im Hintergrund befindet.

Weitere Informationen finden Sie unter [Lebenszykluserweiterung unter iOS](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle/lifecycle-extension-in-ios).

Hier finden Sie eine Beispielimplementierung dieses Anwendungsfalls mit iOS:

```
 func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
  
  
 ACPCore.setLogLevel(.debug)
 appId = SettingsBundle.getLaunchAppId()
   
 //===== START Set up Adobe SDK =====
 ACPCore.configure(withAppId: appId)
   
 ACPCampaign.registerExtension()
 ACPIdentity.registerExtension()
 ACPLifecycle.registerExtension()
 ACPUserProfile.registerExtension()
 ACPSignal.registerExtension()
 ACPCore.start()
 ACPCore.lifecycleStart(nil)
   
 return true
 }
  
func applicationDidEnterBackground(_ application: UIApplication) {
 ACPCore.lifecyclePause()
 }
   
 func applicationDidBecomeActive(_ application: UIApplication) {
 // Workaround until jira AMSDK-7411 is fixed.
 sleep(2)
 ACPCore.lifecycleStart(nil)
 }
```

### Mit Android {#register-mobile-profile-android}

In Android [!DNL Experience Platform APIs] sind folgende Schritte erforderlich:

* **[!UICONTROL OnResume]**
* **[!UICONTROL OnPause]**

Weitere Informationen finden Sie unter [Lebenszykluserweiterung in Android](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle/lifecycle-extension-in-android).

Hier finden Sie eine Beispielimplementierung für diesen Anwendungsfall mit Android:

```
@Override
  
public void onResume() {
 super.onResume();
 MobileCore.setApplication(getApplication());
 MobileCore.lifecycleStart(null);
 handleOpenTracking();
 }
  
 @Override
 public void onPause() {
 super.onPause();
 MobileCore.lifecyclePause();
 }
```

## Senden eines Push-Tokens an Adobe Campaign Standard {#send-push-token}

### Mit iOS {#send-push-token-ios}

Unter iOS ist Folgendes [!DNL Experience Platform SDK] erforderlich:

* **[!UICONTROL setPushIdentifier]** <br>Weitere Informationen finden Sie unter [setPushIdentifier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#setpushidentifier).

Hier finden Sie die Beispielimplementierung für diesen Anwendungsfall mit iOS:

```
func application(_ application: UIApplication, didRegisterForRemoteNotificationsWithDeviceToken deviceToken: Data) {
  
 // Register Device Token
 ACPCore.setPushIdentifier(deviceToken)
```

### Mit Android {#send-push-token-android}

In Android [!DNL Experience Platform SDK] ist Folgendes erforderlich:

* **[!UICONTROL setPushIdentifier]** <br>Weitere Informationen finden Sie unter [setPushIdentifier](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#setpushidentifier).

Hier finden Sie eine Beispielimplementierung für diesen Anwendungsfall mit Android:

```
@Override
public void onNewToken(String token) {
    Log.d(TAG, "Refreshed token: " + token);
    MobileCore.setPushIdentifier(token);
}
```

## Mobiles Profil mit benutzerspezifischen Daten aus Ihrer Anwendung aufwerten {#enrich-mobile-profile-custom}

Damit dieser Anwendungsfall funktioniert, müssen Sie Regeln für PII-Postbacks erstellen. Weitere Informationen finden Sie unter [PII-Postbacks](../../administration/using/configuring-rules-launch.md#pii-postback).

### Mit iOS {#enrich-mobile-profile-custom-ios}

Unter iOS ist Folgendes [!DNL Experience Platform API] erforderlich:

* collectionPII <br> Weitere Informationen finden Sie unter collectionPII.

Hier finden Sie eine Beispielimplementierung dieses Anwendungsfalls mit iOS:

```
ACPCore.collectPii(["email":email, "firstName":firstName, "lastName":lastName])
```

### Mit Android {#enrich-mobile-profile-custom-android}

In Android [!DNL Experience Platform API] ist Folgendes erforderlich:

* collectionPII <br> Weitere Informationen finden Sie unter collectionPII.

Hier finden Sie eine Beispielimplementierung für diesen Anwendungsfall mit Android:

```
HashMap<String, String> data = new HashMap<>();
data.put("firstName", firstNameText);
data.put("lastName", lastNameText);
data.put("email", emailText);
MobileCore.collectPii(data);
```

## Aufwerten eines mobilen Profils mit Lebenszyklusdaten aus Ihrer Anwendung {#enrich-mobile-profile-lifecycle}

Damit dieser Anwendungsfall funktioniert, müssen Sie Regeln für PII-Postbacks erstellen. Weitere Informationen finden Sie unter [PII-Postbacks](../../administration/using/configuring-rules-launch.md#pii-postback).

>[!NOTE]
>
>Adobe Campaign unterscheidet nicht zwischen benutzerspezifischen Daten oder Lebenszyklusdaten und der mobilen App. Beide Datentypen können als Reaktion auf ein Ereignis in der mobilen App mit einer &quot;collectionPii&quot;-Postback-Regel an den Server gesendet werden.

### Mit iOS {#enrich-mobile-profile-lifecycle-ios}

Unter iOS sind folgende [!DNL Experience Platform APIs] erforderlich:

* **[!UICONTROL Lebenszyklus-Beginn]**, wenn die App gestartet wird und sich die App im Vordergrund befindet.
* **[!UICONTROL Lebenszykluspause]**, wenn sich die App im Hintergrund befindet.

Weitere Informationen finden Sie unter [Lebenszykluserweiterung unter iOS](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle/lifecycle-extension-in-ios).

Hier finden Sie eine Beispielimplementierung dieses Anwendungsfalls mit iOS:

```
func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?) -> Bool {
  
  
 ACPCore.setLogLevel(.debug)
 appId = SettingsBundle.getLaunchAppId()
   
 //===== START Set up Adobe SDK =====
 ACPCore.configure(withAppId: appId)
   
 ACPCampaign.registerExtension()
 ACPIdentity.registerExtension()
 ACPLifecycle.registerExtension()
 ACPUserProfile.registerExtension()
 ACPSignal.registerExtension()
 ACPCore.start()
 ACPCore.lifecycleStart(nil)
   
 return true
 }
  
func applicationDidEnterBackground(_ application: UIApplication) {
 ACPCore.lifecyclePause()
 }
   
 func applicationDidBecomeActive(_ application: UIApplication) {
 // Workaround until jira AMSDK-7411 is fixed.
 sleep(2)
 ACPCore.lifecycleStart(nil)
 }
```

### Mit Android {#enrich-mobile-profile-lifecycle-android}

In Android [!DNL Experience Platform APIs] sind folgende Schritte erforderlich:

* **[!UICONTROL OnResume]**
* **[!UICONTROL OnPause]**

Weitere Informationen finden Sie unter [Lebenszykluserweiterung in Android](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle/lifecycle-extension-in-android).

Hier finden Sie eine Beispielimplementierung für diesen Anwendungsfall mit Android:

```
@Override
  
public void onResume() {
 super.onResume();
 MobileCore.setApplication(getApplication());
 MobileCore.lifecycleStart(null);
 handleOpenTracking();
 }
  
 @Override
 public void onPause() {
 super.onPause();
 MobileCore.lifecyclePause();
 }
```

## Benutzerinteraktion mit Push-Benachrichtigungen verfolgen {#track-user-push}

Sie müssen Regeln für die Nachverfolgung von Postback-Benachrichtigungen erstellen. Weitere Informationen finden Sie unter Nachverfolgung von [Push-Benachrichtigungen](../../administration/using/configuring-rules-launch.md#push-tracking-postback).

### Mit iOS {#track-user-push-ios}

Unter iOS ist Folgendes [!DNL Experience Platform SDK] erforderlich:

* **[!UICONTROL trackAction]**. Weitere Informationen finden Sie unter [Verfolgen von App-Aktionen](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

Hier finden Sie eine Beispielimplementierung dieses Anwendungsfalls mit iOS:

```
let deliveryId = userInfo["_dId"] as? String
let broadlogId = userInfo["_mId"] as? String
if (deliveryId != nil && broadlogId != nil) {
    ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
}
```

### Mit Android {#track-user-push-android}

In Android [!DNL Experience Platform SDK] ist Folgendes erforderlich:

* **[!UICONTROL trackAction]** Weitere Informationen finden Sie unter [Verfolgung von App-Aktionen](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

Hier finden Sie eine Beispielimplementierung für diesen Anwendungsfall mit Android:

```
contextData.put("deliveryId", deliveryId);
contextData.put("broadlogId", messageId);
contextData.put("action", "2");
MobileCore.trackAction("tracking", contextData);
```

## Implementieren eines benutzerdefinierten Ereignisses in Ihrer Anwendung, um In-App-Nachrichten auszulösen {#custom-event-inapp}

### Mit iOS {#custom-event-inapp-ios}

Unter iOS ist Folgendes [!DNL Experience Platform SDK] erforderlich:

* **[!UICONTROL trackAction]**. Weitere Informationen finden Sie unter [Verfolgen von App-Aktionen](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

Hier finden Sie eine Beispielimplementierung dieses Anwendungsfalls mit iOS:

```
ACPCore.trackAction(mobileEventName, data: [:] )
```

### Mit Android {#custom-event-inapp-android}

In Android [!DNL Experience Platform SDK] ist Folgendes erforderlich:

* **[!UICONTROL trackAction]** Weitere Informationen finden Sie unter [Verfolgung von App-Aktionen](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

Hier finden Sie eine Beispielimplementierung für diesen Anwendungsfall mit Android:

```
MobileCore.trackAction(mobileEventText, new HashMap<String,String>());
```

## Verknüpfungsfelder für zusätzliche Authentifizierung festlegen {#linkage-fields-inapp}

### Mit iOS {#linkage-fields-inapp-ios}

Um Verknüpfungsfelder für die zusätzliche Authentifizierung für die Profil-Vorlage festzulegen, die auf In-App-Nachrichten in iOS basiert, [!DNL Experience Platform SDK] müssen Sie Folgendes festlegen:

* Verknüpfungsfelder festlegen <br>Weitere Informationen finden Sie unter [Festlegen von Verknüpfungsfeldern](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#set-linkage-fields).
* Verknüpfungsfelder zurücksetzen <br>Weitere Informationen finden Sie unter Verknüpfungsfelder [zurücksetzen](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#reset-linkage-fields).

Im Folgenden finden Sie Beispiele für Implementierungen dieses Anwendungsfalls mit iOS.

So legen Sie Verknüpfungsfelder fest:

```
var linkageFields = [String: String]()
linkageFields["cusEmail"] = "john.doe@email.com"
ACPCampaign.setLinkageFields(linkageFields)
```

So setzen Sie Verknüpfungsfelder zurück:

```
ACPCampaign.resetLinkageFields(linkageFields)
```

### Mit Android {#linkage-fields-inapp-android}

Zum Festlegen von Verknüpfungsfeldern für die zusätzliche Authentifizierung für die Profil-Vorlage, die auf In-App-Nachrichten in Android basiert, ist das folgende Experience Platform-SDK erforderlich:

* Verknüpfungsfelder festlegen <br>Weitere Informationen finden Sie unter [Festlegen von Verknüpfungsfeldern](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#set-linkage-fields).
* Verknüpfungsfelder zurücksetzen <br>Weitere Informationen finden Sie unter Verknüpfungsfelder [zurücksetzen](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference#reset-linkage-fields).

Im Folgenden finden Sie Beispiele für Implementierungen dieses Anwendungsfalls mit Android.

So legen Sie Verknüpfungsfelder fest:

```
HashMap<String, String> linkageFields = new HashMap<String, String>();
linkageFields.put("cusEmail", "john.doe@email.com");
Campaign.setLinkageFields(linkageFields);
```

So setzen Sie Verknüpfungsfelder zurück:

```
Campaign.resetLinkageFields()
```

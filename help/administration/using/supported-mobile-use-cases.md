---
title: Anwendungsfälle für Smartphones und Tablets, die in Adobe Campaign Standard mit den Adobe Experience Platform SDKs unterstützt werden
description: Erfahren Sie, wie Sie Anwendungsfälle für Mobilgeräte unterstützen
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 3cd8d756-a271-4e53-8ed0-984ce20298bc
source-git-commit: 597ece8d833a216f0540f801461b08fdc9865024
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 88%

---

# Unterstützte Anwendungsfälle für Smartphones und Tablets in Adobe Campaign Standard {#mobile-use-cases}

Auf dieser Seite finden Sie die Liste aller Anwendungsfälle für Smartphones und Tablets, die in [!DNL Adobe Campaign Standard] unter Verwendung von [!DNL Adobe Experience Platform SDKs] unterstützt werden. Beachten Sie, dass zur Unterstützung dieser Anwendungsfälle die Installation und Konfiguration von [!DNL Adobe Experience Platform SDKs], [!DNL tags in Adobe Experience Platform] und [!DNL Adobe Campaign Standard]erforderlich sind. Weiterführende Informationen dazu finden Sie auf dieser [Seite](../../administration/using/configuring-a-mobile-application.md).

Adobe Campaign Standard unterstützt die folgenden Anwendungsfälle:

* [Mobiles Profil in Campaign Standard registrieren](../../administration/using/supported-mobile-use-cases.md#register-mobile-profile)
* [Push-Token an Campaign Standard senden](../../administration/using/supported-mobile-use-cases.md#send-push-token)
* [Mobiles Profil mit benutzerspezifischen Daten aus Ihrer Mobile App anreichern](../../administration/using/supported-mobile-use-cases.md#enrich-mobile-profile-custom)
* [Mobiles Profil mit Lebenszyklusdaten aus Ihrer Mobile App anreichern](../../administration/using/supported-mobile-use-cases.md#enrich-mobile-profile-lifecycle)
* [Benutzerinteraktion mit Push-Benachrichtigungen tracken](../../administration/using/supported-mobile-use-cases.md#track-user-push)
* [Benutzerdefiniertes Ereignis in Ihrer Mobile App implementieren, um In-App-Nachrichten auszulösen](../../administration/using/supported-mobile-use-cases.md#custom-event-inapp)
* [Verknüpfungsfelder für zusätzliche Authentifizierung für die Profilvorlage festlegen, die auf In-App-Nachrichten basiert](../../administration/using/supported-mobile-use-cases.md#linkage-fields-inapp)

Zum Konfigurieren dieser Anwendungsfälle benötigen Sie die folgenden Erweiterungen:

* **[!DNL Adobe Campaign Standard]** <br>Informationen zum Installieren und Konfigurieren der Campaign Standard-Erweiterung finden Sie unter [Campaign Standard-Erweiterung in der Datenerfassungs-UI konfigurieren](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/#configure-the-campaign-standard-extension).
* **[!DNL Mobile Core]** (wird automatisch installiert). <br>Weitere Informationen zur Mobile Core-Erweiterung finden Sie unter [Mobile Core](https://developer.adobe.com/client-sdks/documentation/mobile-core/).
* **[!DNL Profile]** (wird automatisch installiert). <br>Weitere Informationen zur Profil-Erweiterung finden Sie unter [Profil](https://developer.adobe.com/client-sdks/documentation/profile/).

## Mobiles Profil in Campaign Standard registrieren {#register-mobile-profile}

### Mit iOS {#register-mobile-profile-ios}

Unter iOS sind folgende [!DNL Experience Platform APIs] erforderlich:

* **[!UICONTROL Lifecycle Start]**, wenn die Mobile App gestartet wird und sie sich im Vordergrund befindet.
* **[!UICONTROL Lifecycle Pause]**, wenn sich die Mobile App im Hintergrund befindet.

Weitere Informationen finden Sie unter [Lifecycle-Erweiterung unter iOS](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/ios/).

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

Unter Android sind folgende [!DNL Experience Platform APIs] erforderlich:

* **[!UICONTROL OnResume]**
* **[!UICONTROL OnPause]**

Weitere Informationen finden Sie unter [Lifecycle-Erweiterung unter Android](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/android/).

Hier finden Sie eine Beispielimplementierung dieses Anwendungsfalls mit Android:

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

## Push-Token an Adobe Campaign Standard senden {#send-push-token}

### Mit iOS {#send-push-token-ios}

Unter iOS ist folgendes [!DNL Experience Platform SDK] erforderlich:

* **[!UICONTROL setPushIdentifier]** <br>Weitere Informationen finden Sie unter [setPushIdentifier](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/).

Hier finden Sie die Beispielimplementierung dieses Anwendungsfalls mit iOS:

```
func application(_ application: UIApplication, didRegisterForRemoteNotificationsWithDeviceToken deviceToken: Data) {
  
 // Register Device Token
 ACPCore.setPushIdentifier(deviceToken)
```

### Mit Android {#send-push-token-android}

Unter Android ist folgendes [!DNL Experience Platform SDK] erforderlich:

* **[!UICONTROL setPushIdentifier]** <br>Weitere Informationen finden Sie unter [setPushIdentifier](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/).

Hier finden Sie die Beispielimplementierung dieses Anwendungsfalls mit Android:

```
@Override
public void onNewToken(String token) {
    Log.d(TAG, "Refreshed token: " + token);
    MobileCore.setPushIdentifier(token);
}
```

## Mobiles Profil mit benutzerspezifischen Daten aus Ihrer Mobile App anreichern {#enrich-mobile-profile-custom}

Damit dieser Anwendungsfall funktioniert, müssen Sie Regeln für PII-Postbacks erstellen. Weitere Informationen finden Sie unter [PII-Postbacks](../../administration/using/configuring-rules-launch.md#pii-postback).

### Mit iOS {#enrich-mobile-profile-custom-ios}

Unter iOS ist folgendes [!DNL Experience Platform API] erforderlich:

* collectPII <br> Weitere Informationen finden Sie unter „collectPII“.

Hier finden Sie eine Beispielimplementierung dieses Anwendungsfalls mit iOS:

```
ACPCore.collectPii(["pushPlatform":"apns", "email":email, "firstName":firstName, "lastName":lastName])
```

### Mit Android {#enrich-mobile-profile-custom-android}

Unter Android ist folgendes [!DNL Experience Platform API] erforderlich:

* collectPII <br> Weitere Informationen finden Sie unter „collectPII“.

Hier finden Sie eine Beispielimplementierung dieses Anwendungsfalls mit Android:

```
HashMap<String, String> data = new HashMap<>();
data.put("pushPlatform", "gcm");
data.put("firstName", firstNameText); 
data.put("lastName", lastNameText); 
data.put("email", emailText); 
MobileCore.collectPii(data);
```

## Mobiles Profil mit Lebenszyklusdaten aus Ihrer Mobile App anreichern {#enrich-mobile-profile-lifecycle}

Damit dieser Anwendungsfall funktioniert, müssen Sie Regeln für PII-Postbacks erstellen. Weitere Informationen finden Sie unter [PII-Postbacks](../../administration/using/configuring-rules-launch.md#pii-postback).

>[!NOTE]
>
>Adobe Campaign unterscheidet nicht zwischen benutzerspezifischen Daten und Lebenszyklusdaten aus der Mobile App. Beide Datentypen können mithilfe einer collectPii-Postback-Regel als Reaktion auf ein Ereignis in der Mobile App an den Server gesendet werden.

### Mit iOS {#enrich-mobile-profile-lifecycle-ios}

Unter iOS sind folgende [!DNL Experience Platform APIs] erforderlich:

* **[!UICONTROL Lifecycle Start]**, wenn die Mobile App gestartet wird und sie sich im Vordergrund befindet.
* **[!UICONTROL Lifecycle Pause]**, wenn sich die Mobile App im Hintergrund befindet.

Weitere Informationen finden Sie unter [Lifecycle-Erweiterung unter iOS](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/ios/).

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

Unter Android sind folgende [!DNL Experience Platform APIs] erforderlich:

* **[!UICONTROL OnResume]**
* **[!UICONTROL OnPause]**

Weitere Informationen finden Sie unter [Lifecycle-Erweiterung unter Android](https://developer.adobe.com/client-sdks/documentation/mobile-core/lifecycle/android/).

Hier finden Sie eine Beispielimplementierung dieses Anwendungsfalls mit Android:

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

## Benutzerinteraktion mit Push-Benachrichtigungen tracken {#track-user-push}

Sie müssen Regeln für das Tracking-Postback von Push-Benachrichtigungen erstellen. Weitere Informationen finden Sie unter [Tracking-Postback von Push-Benachrichtigungen](../../administration/using/configuring-rules-launch.md#push-tracking-postback).

### Mit iOS {#track-user-push-ios}

Unter iOS ist folgendes [!DNL Experience Platform SDK] erforderlich:

* **[!UICONTROL trackAction]**. Weitere Informationen finden Sie unter [App-Aktionen tracken](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction).

Hier finden Sie eine Beispielimplementierung dieses Anwendungsfalls mit iOS:

```
let deliveryId = userInfo["_dId"] as? String
let broadlogId = userInfo["_mId"] as? String
if (deliveryId != nil && broadlogId != nil) {
    ACPCore.trackAction("tracking", data: ["deliveryId": deliveryId!, "broadlogId": broadlogId!, "action":"2"])
}
```

### Mit Android {#track-user-push-android}

Unter Android ist folgendes [!DNL Experience Platform SDK] erforderlich:

* **[!UICONTROL trackAction]**
Weitere Informationen finden Sie unter [App-Aktionen tracken](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction).

Hier finden Sie eine Beispielimplementierung dieses Anwendungsfalls mit Android:

```
contextData.put("deliveryId", deliveryId);
contextData.put("broadlogId", messageId);
contextData.put("action", "2");
MobileCore.trackAction("tracking", contextData);
```

## Benutzerdefiniertes Ereignis in Ihrer Mobile App implementieren, um In-App-Nachrichten auszulösen {#custom-event-inapp}

### Mit iOS {#custom-event-inapp-ios}

Unter iOS ist folgendes [!DNL Experience Platform SDK] erforderlich:

* **[!UICONTROL trackAction]**. Weitere Informationen finden Sie unter [App-Aktionen tracken](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction).

Hier finden Sie eine Beispielimplementierung dieses Anwendungsfalls mit iOS:

```
ACPCore.trackAction(mobileEventName, data: [:] )
```

### Mit Android {#custom-event-inapp-android}

Unter Android ist folgendes [!DNL Experience Platform SDK] erforderlich:

* **[!UICONTROL trackAction]**
Weitere Informationen finden Sie unter [App-Aktionen tracken](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction).

Hier finden Sie eine Beispielimplementierung dieses Anwendungsfalls mit Android:

```
MobileCore.trackAction(mobileEventText, new HashMap<String,String>());
```

## Verknüpfungsfelder für zusätzliche Authentifizierung festlegen {#linkage-fields-inapp}

### Mit iOS {#linkage-fields-inapp-ios}

Um Verknüpfungsfelder für die zusätzliche Authentifizierung für die Profilvorlage festzulegen, die auf In-App-Nachrichten in iOS basiert, ist folgendes [!DNL Experience Platform SDK] erforderlich:

* Verknüpfungsfelder festlegen <br>Weitere Informationen finden Sie unter [Verknüpfungsfelder festlegen](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/#setlinkagefields).
* Verknüpfungsfelder zurücksetzen <br>Weitere Informationen finden Sie unter [Verknüpfungsfelder zurücksetzen](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/#setlinkagefields).

Hier finden Sie Beispielimplementierungen dieses Anwendungsfalls mit iOS:

Festlegen von Verknüpfungsfeldern:

```
var linkageFields = [String: String]()
linkageFields["cusEmail"] = "john.doe@email.com"
ACPCampaign.setLinkageFields(linkageFields)
```

Zurücksetzen von Verknüpfungsfeldern:

```
ACPCampaign.resetLinkageFields(linkageFields)
```

### Mit Android {#linkage-fields-inapp-android}

Um Verknüpfungsfelder für die zusätzliche Authentifizierung für die Profilvorlage festzulegen, die auf In-App-Nachrichten in Android basiert, ist folgendes Experience Platform SDK erforderlich:

* Verknüpfungsfelder festlegen <br>Weitere Informationen finden Sie unter [Verknüpfungsfelder festlegen](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/#setlinkagefields).
* Verknüpfungsfelder zurücksetzen <br>Weitere Informationen finden Sie unter [Verknüpfungsfelder zurücksetzen](https://developer.adobe.com/client-sdks/documentation/adobe-campaign-standard/api-reference/#resetlinkagefields).

Hier finden Sie Beispielimplementierungen dieses Anwendungsfalls mit Android:

Festlegen von Verknüpfungsfeldern:

```
HashMap<String, String> linkageFields = new HashMap<String, String>();
linkageFields.put("cusEmail", "john.doe@email.com");
Campaign.setLinkageFields(linkageFields);
```

Zurücksetzen von Verknüpfungsfeldern:

```
Campaign.resetLinkageFields()
```

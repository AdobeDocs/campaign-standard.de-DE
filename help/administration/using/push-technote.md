---
title: Künftige Änderungen am Push-Benachrichtigungskanal
description: Künftige Änderungen am Push-Benachrichtigungskanal
audience: channels
feature: Push
role: Admin
level: Experienced
exl-id: e273b443-7c43-482b-8f86-60ada4b57cbf
source-git-commit: 2d3210f681bef0f94b7f22f43906ac62b29541f2
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 37%

---

# Änderungen am Push-Benachrichtigungskanal {#push-upgrade}

Sie können Campaign verwenden, um Push-Benachrichtigungen an Android- und iOS-Geräte zu senden. Dazu benötigt Campaign bestimmte Abonnementdienste. Einige wichtige Änderungen am Android Firebase Cloud Messaging(FCM)-Dienst werden 2024 veröffentlicht und können sich auf Ihre Implementierung von Adobe Campaign auswirken. Ihre Konfiguration der Anmeldedienste für Android-Push-Nachrichten muss möglicherweise aktualisiert werden, um diese Änderung zu unterstützen.

Darüber hinaus empfiehlt Adobe dringend, zur Token-basierten anstatt einer zertifikatbasierten Verbindung zu APNs zu migrieren, weil sie sicherer und skalierbarer ist.

Um einen unterbrechungsfreien Dienst sicherzustellen, müssen Sie Ihre bei Adobe Campaign registrierten Mobile Apps aktualisieren, um die neuesten Authentifizierungsmechanismen für FCM (Android) und APNs (iOS) zu implementieren.


[Erfahren Sie mehr über die Konfiguration Ihrer Mobile-App-Zertifikate in Adobe Campaign Standard](configuring-a-mobile-application.md#channel-specific-config)


## Google Android Firebase Cloud Messaging (FCM)-Dienst {#fcm-push-upgrade}

### Was hat sich verändert? {#fcm-changes}

Im Rahmen der kontinuierlichen Bemühungen von Google, seine Dienste zu verbessern, werden die veralteten FCM-APIs am **20. Juni 2024** eingestellt. Weitere Informationen zum HTTP-Protokoll von Firebase Cloud Messaging finden Sie in der [Google Firebase-Dokumentation](https://firebase.google.com/docs/cloud-messaging/http-server-ref){target="_blank"}.

Ab Version 24.2 unterstützt Adobe Campaign Standard die HTTP v1-APIs zum Senden von Android-Push-Benachrichtigungen.

### Sind Sie betroffen? {#fcm-impact}

Wenn Sie Adobe Campaign Standard bereits zum Senden von Push-Benachrichtigungen verwenden, muss Ihre Implementierung aktualisiert werden.

Der Übergang zu den neuesten APIs ist obligatorisch, um eine Dienstverzerrung zu vermeiden.

<!--To check if you are impacted, you can filter your **Services and Subscriptions** as per the filter below

* If any of your active push notification service uses the **HTTP (legacy)** API, your setup will be directly impacted by this change. You must review your current configurations and move to the newer APIs as described below.

* If your setup exclusively uses the **HTTP v1** API for Android push notifications, then you are already in compliance and no further action will be required on your part.-->

### Wie erfolgt die Aktualisierung? {#fcm-transition-procedure}

#### Voraussetzungen {#fcm-transition-prerequisites}

* Die Unterstützung **HTTP v1-APs** -Modus wurde in Version 24.1 hinzugefügt. Wenn Ihre Umgebung auf einer älteren Version ausgeführt wird, besteht eine Voraussetzung für diese Änderung darin, Ihre Umgebung auf die [neueste Version von Campaign Standard](../../rn/using/release-notes.md).

* Die JSON-Datei des Kontos des Firebase Admin SDK-Dienstes ist erforderlich, damit die Mobile App auf HTTP v1 verschoben wird. In der [Dokumentation zu Google Firebase](https://firebase.google.com/docs/admin/setup#initialize-sdk){target="_blank"} erfahren Sie, wie Sie diese Datei erhalten.

* Wenn Sie noch diese ältere Version des SDK verwenden, müssen Sie Ihre Implementierung mit dem Adobe Experience Platform SDK aktualisieren. Erfahren Sie, wie Sie zu Adobe Experience Platform SDK migrieren können in [diesem Artikel](sdkv4-migration.md).

* Vergewissern Sie sich, dass die **Konfiguration der Mobile App** -Berechtigung in Adobe Experience Platform Data Collection Mobile , bevor Sie die folgenden Schritte ausführen. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-platform/collection/permissions.html?lang=en#adobe-experience-platform-data-collection-permissions){target="_blank"}.


#### Migrationsverfahren {#fcm-transition-steps}

Befolgen Sie die folgenden Schritte, um Ihre Umgebung zu HTTP v1 zu migrieren:

1. Navigieren Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL Mobile App (AEP SDK)]**.

   ![](assets/push_technote_1.png)

1. Wählen Sie die spezifische Mobile App aus, für die das Zertifikat aktualisiert werden muss.

1. Überprüfen Sie die **[!UICONTROL App-Anmeldeinformationen aktualisieren]** aktivieren.

   ![](assets/push_technote_5.png)

1. Geben Sie die App-ID (den Android-Paketnamen) aus dem `build.gradle` -Datei. Beispiel: `com.android.test.testApp`. Stellen Sie sicher, dass Sie verschiedene IDs für Staging- und Produktionsumgebungen verwenden.

1. Laden Sie die JSON-Schlüsseldatei mit dem privaten Android-Schlüssel hoch.

   ![](assets/push_technote_3.png)

1. Klicken Sie auf die Schaltfläche **Speichern**.

>[!NOTE]
>
>Sobald diese Änderungen angewendet wurden, verwenden alle neuen Push-Benachrichtigungsversand an Android-Geräte die HTTP v1-API. Für bestehende Push-Sendungen, die gerade erneut versucht werden, gestartet sind oder verwendet werden, wird weiterhin die (veraltete) HTTP-API verwendet.


## Apple iOS-Push-Benachrichtigungsdienst (APNs) {#apns-push-upgrade}

### Was hat sich verändert? {#ios-changes}

Wie von Apple empfohlen, sollten Sie Ihre Kommunikation mit dem Apple-Push-Benachrichtigungsdienst (APNs) mithilfe von Stateless-Authentifizierungs-Token sichern.

Token-basierte Authentifizierung bietet eine Möglichkeit der Stateless-Kommunikation mit dem APNs. Stateless-Kommunikation ist schneller als zertifikatbasierte Kommunikation, da hier der APNs nicht das Zertifikat oder andere Informationen zu Ihrem Anbieter-Server nachschlagen muss. Die Verwendung der Token-basierten Authentifizierung bietet noch weitere Vorteile:

* Sie können dasselbe Token von mehreren Anbieter-Servern verwenden.

* Mit einem einzelnen Token können Sie Benachrichtigungen für alle Apps Ihres Unternehmens verteilen.

Erfahren Sie mehr über Token-basierte Verbindungen zum APNs im [Apple-Entwickler-Handbuch](https://developer.apple.com/documentation/usernotifications/establishing-a-token-based-connection-to-apns){target="_blank"}.

Adobe Campaign Standard unterstützt sowohl Token-basierte als auch zertifikatbasierte Verbindungen. Wenn Ihre Implementierung auf einer zertifikatbasierten Verbindung basiert, empfiehlt Adobe dringend, sie durch eine Token-basierte Verbindung zu ersetzen.

### Sind Sie betroffen? {#ios-impact}

Wenn Ihre aktuelle Implementierung für die Verbindung mit dem APNs auf zertifikatbasierten Anfragen basiert, sind Sie betroffen. Die Migration zu einer Token-basierten Verbindung wird empfohlen.

<!--To check if you are impacted, you can filter your **Services and Subscriptions** as per the filter below:

![](assets/filter-services-ios.png)


* If any of your active push notification service uses the **Certificate-based authentication** mode (.p12), your current implementations should be reviewed and moved to a **Token-based authentication** mode (.p8) as described below.

* If your setup exclusively uses the **Token-based authentication** mode for iOS push notifications, then your implementation is already up-to-date and no further action will be required on your part.-->

### Wie erfolgt die Aktualisierung? {#ios-transition-procedure}

#### Voraussetzungen {#ios-transition-prerequisites}

* Die Unterstützung **Token-basierte Authentifizierung** -Modus wurde in Version 24.1 hinzugefügt. Wenn Ihre Umgebung auf einer älteren Version ausgeführt wird, besteht eine Voraussetzung für diese Änderung darin, Ihre Umgebung auf die [neueste Version von Campaign Standard](../../rn/using/release-notes.md).

* Sie benötigen einen Signierschlüssel für die APNs-Authentifizierungs-Token, um die Token zu erzeugen, die Ihr Server verwendet. Sie fordern diesen Schlüssel über Ihr Apple-Entwicklerkonto an, wie im [Apple-Entwickler-Handbuch](https://developer.apple.com/documentation/usernotifications/establishing-a-token-based-connection-to-apns){target="_blank"} beschrieben.


#### Migrationsverfahren {#ios-transition-steps}

Gehen Sie wie folgt vor, um Ihre mobilen iOS-Apps zum Token-basierten Authentifizierungsmodus zu migrieren:

1. Navigieren Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL Mobile App (AEP SDK)]**.

   ![](assets/push_technote_1.png)

1. Wählen Sie die spezifische Mobile App aus, für die das Zertifikat aktualisiert werden muss.

1. Überprüfen Sie die **[!UICONTROL App-Anmeldeinformationen aktualisieren]** aktivieren.

   ![](assets/push_technote_2.png)

1. Stellen Sie die **App-ID** (iOS Bundle ID). Sie finden die iOS Bundle-ID (App-ID) im primären Ziel Ihrer App in Xcode.

1. Hochladen Ihrer **iOS p8-Zertifikatdatei**.

1. Füllen Sie die APNs-Verbindungseinstellungen aus. **[!UICONTROL Schlüssel-ID]** und **[!UICONTROL iOS-Team-ID]**.

   ![](assets/push_technote_4.png)

1. Klicken Sie auf **[!UICONTROL Speichern]**.

Ihre iOS-Anwendung wird jetzt zum Token-basierten Authentifizierungsmodus migriert.

## Häufig gestellte Fragen{#push-upgrade-faq}

++ + Kann dieselbe AppID in der Staging- und Produktionsinstanz beibehalten werden?

Bei mobilen iOS-Anwendungen können Sie dieselbe App-ID, d. h. Ihre iOS-App-Bundle-ID, sowohl für Staging- als auch für Produktionsumgebungen verwenden. Unter Android sollte die App-ID jedoch für jede Umgebung eindeutig sein. Daher wird vorgeschlagen, &quot;stage&quot;an die in der Staging-Umgebung erstellte App-ID anzuhängen.

+++


+++ Können wir nur die Android-App migrieren?

Nein, sowohl Android- als auch iOS-Apps müssen entsprechend den oben beschriebenen Schritten migriert werden.

+++

+++ Welche Art von Überprüfung müssen wir nach der Migration durchführen?

Wir empfehlen, alle Ihre Push-bezogenen Anwendungsfälle funktionell zu validieren.

+++

+++Was tun, wenn beim Speichern der App der Fehler &quot;Nicht autorisiert&quot;angezeigt wird?

Dies scheint ein Berechtigungsproblem im Zusammenhang mit der Adobe Experience Platform-Datenerfassung zu sein. Um dies zu beheben, müssen Sie Berechtigungen für &quot;Mobile&quot;und &quot;Mobile App Configuration&quot;in der Adobe Admin Console hinzufügen, wie im Abschnitt &quot;Voraussetzungen&quot;dieses Artikels beschrieben.

+++

+++ Sind Änderungen im Code der mobilen App erforderlich?

Nein, es sind nur konfigurationsbezogene Änderungen in Firebase und dem App-Entwicklerkonto erforderlich. Änderungen in der mobilen Kundenanwendung sind nicht erforderlich.

+++

+++ Müssen wir das iOS-Zertifikat jedes Jahr aktualisieren?

Nein, nach dieser Migration muss das iOS-Zertifikat nicht jedes Jahr aktualisiert werden.

+++

+++ Was passiert, wenn diese Migration nicht durchgeführt wird?

Die Android-Push-Nachrichten schlagen nach dem 20. Juni 2024 gemäß der Benachrichtigung von Google fehl. [Weitere Informationen](https://firebase.google.com/docs/cloud-messaging/migrate-v1){target="_blank"}.

+++

++ Können Kunden nach Abschluss der FCMv1-Migration zu FCM zurückkehren?

Ja, Kunden können bis zum 20. Juni 2024 zurück zu FCM migrieren. Nach diesem Datum ist die Migrationsoption nicht mehr verfügbar.

+++

+++ Wird die Migration der HTTP v1-API von der mobilen SDK V4-App unterstützt?

Nein, Kunden müssen zunächst ihre mobile App zum V5-SDK migrieren und dann mit der oben genannten Migration fortfahren. Sie müssen dies vorrangig tun, da ihr Push-Dienst gemäß der Benachrichtigung von Google ab Juni 2024 fehlschlagen wird.

+++

++ Hat die Änderung auf der Staging-Instanz Auswirkungen auf die Produktionsinstanz?

Nein, Änderungen an der mobilen Staging-App haben keine Auswirkungen auf die Produktionsinstanz.

+++
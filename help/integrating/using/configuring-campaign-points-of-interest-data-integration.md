---
title: Integration von Campaign-POI-Daten konfigurieren
seo-title: Integration von Campaign-POI-Daten konfigurieren
description: Integration von Campaign-POI-Daten konfigurieren
seo-description: Hier erfahren Sie, wie Sie die POI-Daten-Funktion in Adobe Campaign konfigurieren, um Ihren Abonnenten je nach ihrem Standort personalisierte Nachrichten zu senden.
page-status-flag: nie aktiviert
uuid: 0689 a 06 c-cc 1 a -442 f -95 b 8-a 07 fcec 85 d 79
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird integriert
content-type: Referenz
topic-tags: working-with-campaign-and-analytics-for-mobile
discoiquuid: a 967 c 6 cc-c 53 b -41 b 4-866 b -90860 d 78 f 463
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6df0e764750a31f29d6fe3ec4d92e19b3f07f728

---


# Integration von Campaign-POI-Daten konfigurieren{#configuring-campaign-points-of-interest-data-integration}

Mobile Apps, mit denen Standortdaten erfasst werden, müssen von einem **Administrator** in der Adobe-Campaign-Benutzeroberfläche konfiguriert werden.

Um die POI-Funktion verwenden zu können, gehen Sie folgendermaßen vor:

1. Zunächst benötigen Sie Zugriff auf Adobe Analytics for Mobile. Wenn Sie weitere Informationen benötigen, überprüfen Sie Ihr Lizenzabkommen oder kontaktieren Sie Ihren Adobe-Kundenbetreuer.
1. Richten Sie in Adobe Campaign Ihre Mobile App ein. Siehe [Mobile App in Campaign einrichten](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#setting-up-a-mobile-app-in-campaign).
1. Richten Sie in der Benutzeroberfläche von Adobe Mobile Services Ihre Mobile App ein. Damit können Sie sicherstellen, dass die von Adobe Mobile Services erfassten Daten an Adobe Campaign gesendet werden. Siehe [Mobile App in Adobe Mobile Services konfigurieren](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#configuring-a-mobile-app-in-adobe-mobile-services).
1. Richten Sie die Mobile App ein:

   * Verpacken Sie die von der Adobe-Mobile-Services-Benutzeroberfläche heruntergeladene Konfigurationsdatei mit der Mobile App.
   * Integrieren Sie das Experience Cloud Mobile SDK in Ihre Mobile App. Siehe [SDK in Mobile Apps integrieren](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#integrating-the-sdk-into-a-mobile-application).

1. Definieren Sie POI in der Adobe-Mobile-Services-Benutzeroberfläche. Siehe [POI in Adobe Mobile Services definieren](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#defining-points-of-interest-in-adobe-mobile-services).
1. Definieren Sie die Daten, die Sie von den Abonnenten Ihrer Mobile App erfassen möchten. Siehe [POI-Daten von Abonnenten erfassen](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#collecting-subscribers--points-of-interest-data).
1. Stellen Sie sicher, dass Sie auf die Mobile App und die erfassten Standortdaten in Adobe Campaign Zugriff haben. Siehe [Auf Mobile Apps zugreifen, mit denen Standortdaten erfasst werden](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#accessing-mobile-apps-used-to-collect-location-data) und [Erfasste Standortdaten abrufen](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#accessing-collected-location-data).

## Mobile App in Campaign einrichten {#setting-up-a-mobile-app-in-campaign}

Um POI-Daten mit Adobe Campaign erfassen zu können, müssen Sie die Mobile App konfigurieren, von der Adobe Campaign Daten erhält.

1. Click the **[!UICONTROL Adobe Campaign]** logo, in the top left corner, then select **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Mobile app]**.
1. Verwenden Sie die Schaltfläche **[!UICONTROL Erstellen], um eine App einzurichten.**
1. Füllen Sie das Feld **[!UICONTROL App-Name]** aus und klicken Sie auf **[!UICONTROL Erstellen]**.

   Füllen Sie nicht den Bereich **[!UICONTROL Gerätespezifische Parameter]aus.** Dies gilt nur für das Konfigurieren von Anwendungen, die Push-Benachrichtigungen empfangen.

In the **[!UICONTROL Mobile application properties]** section, two URLs are listed: **[!UICONTROL Collect PII endpoint]** and **[!UICONTROL Location Services endpoint]**. Diese werden in der Adobe-Mobile-Services-Benutzeroberfläche verwendet. Siehe [Mobile App in Adobe Mobile Services konfigurieren](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#configuring-a-mobile-app-in-adobe-mobile-services).

* Über die URL für den **[!UICONTROL PII-Abruf-Endpoint]ruft die Mobile App bei ihrem Start die Experience Cloud-Kennung und den Anmeldetoken des jeweiligen Benutzers ab.** Wenn sich ein Benutzer bei der App mit seinen Zugangsdaten, wie E-Mail, Vorname, Nachname etc., anmeldet, werden auch diese Daten erfasst und verwendet, um den Anmeldetoken des Benutzers mit einem Adobe-Campaign-Profil abzugleichen.
* Mit der URL **[!UICONTROL Ort versorgt Endpunkt]werden Standortdaten wie der Längen- und Breitengrad und die Entfernung des Benutzers von einem POI (Point of Interest) erfasst.**

Sie können diese Werte jetzt in Adobe Mobile Services verwenden, um die Konfiguration wie im Abschnitt [Mobile App in Adobe Mobile Services konfigurieren](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#configuring-a-mobile-app-in-adobe-mobile-services) beschrieben abzuschließen.

![](assets/poi_mobile_app_properties.png)

## Mobile App in Adobe Mobile Services konfigurieren {#configuring-a-mobile-app-in-adobe-mobile-services}

Um die von Adobe Mobile Services erfassten Daten an Adobe Campaign zu senden, müssen Sie in der Mobile-Services-Benutzeroberfläche Postbacks konfigurieren.

Des Weiteren benötigen Sie spezielle Informationen, die Sie in den in Adobe Campaign eingerichteten Parametern der Mobile App finden (siehe [Mobile App in Campaign einrichten](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#setting-up-a-mobile-app-in-campaign)):

* **[!UICONTROL Kennung der IMS-Organisation]**
* **[!UICONTROL PII-Abruf-Endpoint]**
* **[!UICONTROL Ortungsdienst-Endpunkt]**

Um die folgende Konfiguration durchzuführen, benötigen Sie Zugriff auf Adobe Analytics. Wenn Sie kein Benutzer von Adobe Analytics sind, kontaktieren Sie Ihren Adobe-Campaign-Administrator.

1. Melden Sie sich bei [mobilemarketing.adobe.com](http://mobilemarketing.adobe.com/) an.
1. Erstellen Sie eine Mobile-App oder wählen Sie eine bestehende aus.
1. Gehen Sie zur Seite **[!UICONTROL App-Einstellungen verwalten].**
1. In the **Visitor ID Service ** section, check **Enable** and select your organization from the drop-down list. Wählen Sie **Speichern** aus.

   >[!CAUTION]
   >
   >Dieses Unternehmen muss mit dem in der Adobe-Campaign-Instanz verwendeten übereinstimmen.

1. Klicken Sie auf **[!UICONTROL Postbacks verwalten]**.
1. Erstellen Sie ein Postback.

   * Select **[!UICONTROL PII]** as the **[!UICONTROL Postback Type]**.
   * Kopieren Sie in das Feld **[!UICONTROL URL]** den Servernamen gefolgt von der URL **PII-Abruf-Endpoint]von der in der Adobe-Campaign-Benutzeroberfläche konfigurierten Mobile App.[!UICONTROL ** Siehe [Mobile App in Campaign einrichten](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#setting-up-a-mobile-app-in-campaign).
   * Füllen Sie das Feld **[!UICONTROL Post-Körper]folgendermaßen aus:**

      Für iOS:

      ```
      {
      "userKey": "{userKey}",
      "pushPlatform":"apns",
      "marketingCloudId":"{%mcid%}",
      "cusEmail":"{email}",
      "cusFirstName":"{firstName}",
      "cusLastName":"{lastName}"
      }
      ```

      Für Android:

      ```
      {
      "userKey": "{userKey}",
      "pushPlatform":"gcm",
      "marketingCloudId":"{%mcid%}",
      "cusEmail":"{email}",
      "cusFirstName":"{firstName}",
      "cusLastName":"{lastName}"
      }
      ```

   * Wählen Sie für **Inhaltstyp** die Option **[!UICONTROL application/json]**.
   * Wählen Sie unter **Welche Daten-Tags lösen den Postback aus?** ein beliebiges Ereignis, normalerweise **[!UICONTROL Gestartet]** und **[!UICONTROL Ist vorhanden]**.
   * Klicken Sie auf **[!UICONTROL Speichern und aktivieren]**.

1. Erstellen Sie ein zweites Postback.

   * Select **[!UICONTROL Postback]** as the **[!UICONTROL Postback Type]**.
   * Kopieren Sie in das Feld **[!UICONTROL URL]** den Servernamen gefolgt von der URL **Ort versorgt Endpunkt]von der in der Adobe-Campaign-Benutzeroberfläche konfigurierten Mobile App.[!UICONTROL ** Siehe [Mobile App in Campaign einrichten](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md#setting-up-a-mobile-app-in-campaign).
   * Füllen Sie das Feld **[!UICONTROL Post-Körper]folgendermaßen aus:**

      ```
      {
      "locationData":{
      "distances":"{a.loc.dist}",
      "poiLabel":"{a.loc.poi}",
      "latitude.a":"{a.loc.lat.a}",
      "latitude.b":"{a.loc.lat.b}",
      "latitude.c":"{a.loc.lat.c}",
      "longitude.a":"{a.loc.lon.a}",
      "longitude.b":"{a.loc.lon.b}",
      "longitude.c":"{a.loc.lon.c}",
      "appId":"{a.appid}",
      "marketingCloudId":"{mid}"
      }
      }
      ```

   * Wählen Sie für **Inhaltstyp** die Option **[!UICONTROL application/json]**.
   * Wählen Sie unter **Welche Daten-Tags lösen den Postback aus?** die Option **[!UICONTROL campaign.test]** und **[!UICONTROL Ist vorhanden]**.
   * Klicken Sie auf **[!UICONTROL Speichern und aktivieren]**.

>[!NOTE]
>
>Weitere Informationen zur Konfiguration von Postbacks finden Sie im [Adobe-Mobile-Services-Handbuch](https://marketing.adobe.com/resources/help/en_US/mobile/signals_.html).

## SDK in Mobile Apps integrieren {#integrating-the-sdk-into-a-mobile-application}

Mit dem Mobile-Core-Service-SDK (Software Developer Kit) kann eine Mobile App in Adobe Campaign integriert werden.

Dieser Schritt wird auf dieser [Seite](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html) beschrieben.

## POI in Adobe Mobile Services definieren {#defining-points-of-interest-in-adobe-mobile-services}

So definieren Sie POI zum Erfassen von Standortdaten:

1. Gehen Sie zur Adobe-Mobile-Services-Benutzeroberfläche.
1. Fügen Sie Ihre Anwendung hinzu.

   Weitere Informationen zur Verwaltung von Anwendungen in Mobile Services finden Sie im [Adobe-Mobile-Services-Handbuch](https://marketing.adobe.com/resources/help/en_US/mobile/t_new_app.html).

1. Definieren Sie die POI.

   Weitere Informationen zur Verwaltung von POI finden Sie im [Adobe Mobile Services-Handbuch](https://marketing.adobe.com/resources/help/en_US/mobile/t_manage_points.html).

## POI-Daten von Abonnenten erfassen {#collecting-subscribers--points-of-interest-data}

Eine spezielle benutzerdefinierte Ressource ermöglicht es Ihnen, die Daten zu definieren, die Sie in Bezug auf die Abonnenten Ihrer App abrufen möchten.

Dieser Schritt wird auf der Seite [Eine Mobile App mit SDK V4 konfigurieren](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html) beschrieben.

## Auf Mobile Apps zugreifen, mit denen Standortdaten erfasst werden {#accessing-mobile-apps-used-to-collect-location-data}

Um die in Adobe Campaign erfolgreich erstellten Anwendungen zu öffnen, gehen Sie folgendermaßen vor:

1. Wählen Sie oben links das **[!UICONTROL Adobe-Campaign]-Logo aus.**
1. Select **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Mobile app]**.
1. Wählen Sie eine Mobile App aus der Liste aus, um ihre Eigenschaften anzuzeigen.

   ![](assets/poi_mobile_app_subscribers.png)

Auch eine Liste mit den Abonnenten der Anwendung wird angezeigt. Die Abonnenten sind alle Benutzer, die die Anwendung auf ihrem Mobilgerät installiert haben. Die Profile in der Adobe-Campaign-Datenbank werden mit einem Anmeldetoken identifiziert.

## Erfasste Standortdaten abrufen {#accessing-collected-location-data}

Nach dem Einrichten werden die erfassten POI-Daten im Tab **[!UICONTROL Orte]eines jeden Profils aufgeführt.** So greifen Sie auf die Liste zu:

1. Wählen Sie ein Profil aus.
1. Wählen Sie rechts die Schaltfläche **[!UICONTROL Profileigenschaften bearbeiten]aus.**
1. Wählen Sie den Tab **[!UICONTROL Orte]aus.**

   ![](assets/poi_profile_places.png)

Die erfassten POI-Daten für das aktuelle Profil werden angezeigt. Standortdaten werden sechs Monate lang in der Datenbank von Adobe Campaign gespeichert.

Weitere Informationen zum Öffnen und Bearbeiten von Profilen finden Sie unter [Profile](../../audiences/using/about-profiles.md).

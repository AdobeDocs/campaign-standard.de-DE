---
title: Konfigurieren von Adobe Experience Platform Launch-Regeln zur Unterstützung von Adobe Campaign Standard-Anwendungsfällen
description: Konfigurieren von Adobe Experience Platform Launch-Regeln zur Unterstützung von Adobe Campaign Standard-Anwendungsfällen
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
source-git-commit: 2b8a25a90ea253666fb71c3f7aaf830d736e6c5b
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 9%

---


# Konfigurieren von Startregeln zur Unterstützung von Adobe Campaign Standard-Anwendungsfällen {#configuring-rules-launch}

In [!DNL Adobe Experience Platform Launch], you need to create data elements and rules to send PII and other data from mobile applications to [!DNL Adobe Campaign Standard].

Um sicherzustellen, dass alle Konfigurationsänderungen wirksam [!DNL Adobe Experience Platform Launch] werden, müssen Sie diese Änderungen veröffentlichen. Weitere Informationen finden Sie unter [Veröffentlichen](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration).

Gehen Sie wie [!DNL Experience Platform Launch]folgt vor, um Regeln zu erstellen:

1. [Datenelemente erstellen](../../administration/using/configuring-rules-launch.md#create-data-elements)
2. [Erstellen von Regeln](../../administration/using/configuring-rules-launch.md#create-data-elements) für Anwendungsfälle, die Sie unterstützen möchten:
   * [PII-Postback](../../administration/using/configuring-rules-launch.md#pii-postback)
   * [In-App-Tracking-Postback](../../administration/using/configuring-rules-launch.md#inapp-tracking-postback)
   * [Nachverfolgung von Push-Benachrichtigungen](../../administration/using/configuring-rules-launch.md#push-tracking-postback)
   * [Standort-Postback](../../administration/using/configuring-rules-launch.md#location-postback)

## Datenelemente erstellen {#create-data-elements}

Im Folgenden finden Sie die Datenelemente, die wir Ihnen empfehlen, in zu erstellen [!DNL Experience Platform Launch].
Sie können weitere Datenelemente entsprechend Ihren Anforderungen erstellen.

* **[!UICONTROL Experience-Cloud-ID]**
* **[!UICONTROL Schlüssel]**
* **[!UICONTROL Kampagne-Server]**

So erstellen Sie diese Datenelemente:

1. Klicken Sie [!DNL Experience Platform Launch]im Dashboard Ihrer mobilen Anwendung auf die Registerkarte **[!UICONTROL Datenelemente]** .

1. Klicken Sie zum Erstellen des **[!UICONTROL Experience Cloud-ID]** -Datenelements auf Neues Datenelement **[!UICONTROL erstellen]**.

1. In the **[!UICONTROL Name]** field, for example, type in **mcid**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Extension]** die Option **[!UICONTROL Mobile Core]** aus. Dann **[!UICONTROL Experience Cloud-ID]** in der Dropdown-Liste **[!UICONTROL Datenelementtyp]** .

   ![](assets/rules_1.png)

1. Klicken Sie zum Erstellen des Pkey-Datenelements auf **[!UICONTROL Hinzufügen Datenelement]**.

1. Geben Sie im Feld **[!UICONTROL Name]** beispielsweise **pkey** ein.

1. From the **[!UICONTROL Extension]** drop-down, select **[!UICONTROL Adobe Campaign Standard]**. Drücken Sie dann **[!UICONTROL die]** Taste in der Dropdown-Liste **[!UICONTROL Datenelementtyp]** .

1. Klicken Sie zum Erstellen des Datenelements &quot;Kampagne-Server&quot;auf **[!UICONTROL Hinzufügen Datenelement]**.

1. Geben Sie im Feld **[!UICONTROL Name]** einen Namen ein, z. B. **camp-server**.

1. From the **[!UICONTROL Extension]** drop-down, select **[!UICONTROL Adobe Campaign Standard]**. Dann **[!UICONTROL Kampagne Server]** in der Dropdown-Liste **[!UICONTROL Data element]** type.

## Erstellen von Regeln {#creating-rules}

Sie müssen Regeln für Folgendes erstellen:

* [PII-Postback](../../administration/using/configuring-rules-launch.md#pii-postback)
* [In-App-Tracking-Postback](../../administration/using/configuring-rules-launch.md#inapp-tracking-postback)
* [Nachverfolgung von Push-Benachrichtigungen](../../administration/using/configuring-rules-launch.md#push-tracking-postback)
* [Standort-Postback](../../administration/using/configuring-rules-launch.md#location-postback)

### PII-Postback {#pii-postback}

>[!NOTE]
>
>Um PII-Informationen von einer mobilen App an Adobe Campaign zu senden, müssen Sie eine SDK-API implementieren. Weitere Informationen finden Sie unter [CollectPII](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#collect-pii).

Um PII-Daten an [!DNL Adobe Campaign Standard]zu senden, erstellen Sie eine Regel in [!DNL Experience Platform Launch]:

1. Klicken Sie [!DNL Experience Platform Launch]im Dashboard der Mobilanwendung auf die Registerkarte **[!UICONTROL Regeln]** und dann auf Neue Regel **[!UICONTROL erstellen]**.

1. Geben Sie einen Namen ein, z. B. **Mobile Core - Collect PII**.

1. Klicken Sie im Abschnitt **[!UICONTROL Ereignisse]** auf **[!UICONTROL Hinzufügen]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Extension]** die Option **[!UICONTROL Mobile Core]** aus. Dann **[!UICONTROL Collect PII]** in der Dropdownliste **[!UICONTROL Ereignistyp]** .

1. Klicken Sie auf Änderungen **[!UICONTROL beibehalten]**.

1. Klicken Sie im Abschnitt **[!UICONTROL Aktionen]** auf **[!UICONTROL Hinzufügen]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Extension]** die Option **[!UICONTROL Mobile Core]** aus. Dann **[!UICONTROL senden Sie PII]** in der Dropdownliste **[!UICONTROL Aktionstyp]** .

1. Geben Sie in die **[!UICONTROL URL]** die folgende URL ein:

   ```
   https://{%%camp-server%%}/rest/head/mobileAppV5/{%%pkey%%}/subscriptions/{%%mcid%%}
   ```

1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL HinzufügenBeitragstext]** .

1. Geben Sie in **[!UICONTROL Post Body]** Folgendes ein:

   ```
   {
   "marketingCloudId":
   "{%%mcid%%}",
   "cusEmail":
   "{%contextdata.email%}",
   "cusFirstName":
   "{%contextdata.firstName%}",
   "cusLastName":
   "{%contextdata.lastName%}" }
   ```

   Mit der marketingCloudId können Sie Ihre App-Abonnenten mit den Empfängern in der Datenbank abgleichen, was erforderlich ist. Sie können weitere Schlüssel/Wert-Paare entsprechend Ihren geschäftlichen Anforderungen angeben. Im obigen Beispiel werden E-Mail, Vorname und Nachname von der App weitergeleitet.

   Die Schlüssel (z. B. cusEmail, cusFirstName und cusLastName) sollten mit den field-IDs übereinstimmen, die in Ihrer benutzerdefinierten Ressource in der Adobe Campaign Standard-Instanz definiert sind. Die Wertevariablen (z. B. email, firstName und LastName) sollten mit den Schlüsseln in den JSON-Daten übereinstimmen, die von der mobilen App gesendet werden, während die AMS collectionPII-API aus dem App-Code aufgerufen wird.

   Sie können auch Lebenszyklusdaten im PII-Postback sammeln oder in einem anderen Postback weitergeben, je nachdem, welches Ereignis ausgelöst wird. Hier ist ein Beispiel für die JSON-Datei zu Lebenszyklusdaten:

       &quot;
 {     
 &quot;marketingCloudId&quot;:&quot;{%%mcid%%}&quot;,     
     &quot;cusDayslastlaunch&quot;: &quot;{%%DaysSinceLastUse%}&quot;,
     &quot;cusDaysfirstlaunch&quot;: &quot;{%%DaysSinceFirstUse%}&quot;,
     &quot;cusLaunches&quot;: &quot;{%%Launches%}&quot;
     }
     &quot;
   
   Die Datenelemente, die in definiert sind, [!DNL Experience Platform Launch] sollten in Prozentzahlen zur Dublette eingeschlossen werden, z. B. %%mcid%%, und Kontextvariablen der App sollten in einzelnen Prozentwerten eingeschlossen werden, z. B. %contextdata.email%.

1. Geben Sie unter **[!UICONTROL Content-Typ]** den Wert **application/json** ein.

1. Wählen Sie in **[!UICONTROL Timeout]** 0.

   ![](assets/rules_2.png)

Ihre Benutzerdaten sind nun konfiguriert und können an Campaign gesendet werden.

### In-App-Tracking-Postback {#inapp-tracking-postback}

Um Verfolgungsdaten zum Berichte [!DNL Adobe Campaign Standard] darüber zu senden, wie Ihre Benutzer mit In-App-Nachrichten in Ihrer mobilen Anwendung interagieren, erstellen Sie die folgende Regel in [!DNL Experience Platform Launch]:

1. Wählen Sie [!DNL Experience Platform Launch]im Dashboard der Mobilanwendung die Registerkarte **[!UICONTROL Regeln]** und klicken Sie auf **[!UICONTROL Hinzufügen Regel]**.

1. Geben Sie einen Namen ein, z. B. **Adobe Campaign - In-App-Klick-Tracking**.

1. Klicken Sie im Abschnitt **[!UICONTROL Ereignisse]** auf **[!UICONTROL Hinzufügen]**.

1. From the **[!UICONTROL Extension]** drop-down, select **[!UICONTROL Adobe Campaign Standard]**. Anschließend können Sie die **[!UICONTROL In-App-Klick-Verfolgung]** in der Dropdown-Liste &quot; **[!UICONTROL Ereignistyp]** &quot;durchführen.

1. Klicken Sie auf Änderungen **[!UICONTROL beibehalten]**.

1. Klicken Sie im Abschnitt **[!UICONTROL Aktionen]** auf **[!UICONTROL Hinzufügen]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Extension]** die Option **[!UICONTROL Mobile Core]** aus. Dann **[!UICONTROL Senden Sie Postback]** in der Dropdownliste **[!UICONTROL Ereignistyp]** .

1. Geben Sie in die **[!UICONTROL URL]** die folgende URL ein:

   ```
   https://{%%camp-server%%}/r/?id={%id%}&mcid={%%mcid%%}
   ```

1. Aktivieren Sie das Kontrollkästchen &quot; **[!UICONTROL HinzufügenPost Body]** &quot;.

1. Geben Sie in **[!UICONTROL Post Body]****{}** ein.

1. Geben Sie unter **[!UICONTROL Content-Typ]** den Wert **application/json** ein.

1. Wählen Sie in **[!UICONTROL Timeout]** 0.

   ![](assets/rules_3.png)

### Nachverfolgung von Push-Benachrichtigungen {#push-tracking-postback}

To send tracking data to [!DNL Adobe Campaign Standard], which helps track your Push notification deliveries and your users’ interaction with your mobile application, you need to create a rule in [!DNL Experience Platform Launch].

Weitere Informationen zur Push-Verfolgung finden Sie unter [Push-Verfolgung](../../administration/using/push-tracking.md).

Verwenden Sie zur Verfolgung von App-Aktionen die trackAction-API. Weitere Informationen finden Sie unter [Verfolgen von App-Aktionen](https://app.gitbook.com/@aep-sdks/s/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

1. Klicken Sie [!DNL Experience Platform Launch]im Dashboard der Mobilanwendung auf die Registerkarte **[!UICONTROL Regeln]** und dann auf **[!UICONTROL Hinzufügen Regel]**.

1. Geben Sie einen Namen ein, z. B. **Adobe Campaign - Push-Klick-Verfolgung**.

1. Klicken Sie im Abschnitt **[!UICONTROL Ereignisse]** auf **[!UICONTROL Hinzufügen]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Extension]** die Option **[!UICONTROL Mobile Core]** aus. Dann **[!UICONTROL Aktion]** verfolgen in der Dropdown-Liste **[!UICONTROL Ereignistyp]** .

1. Wählen Sie in der Dropdownliste **[!UICONTROL Aktion]** die Option **[!UICONTROL Aktion]**, wählen Sie **[!UICONTROL gleich]** und geben Sie **tracking** ein.

1. Klicken Sie auf Änderungen **[!UICONTROL beibehalten]**. Klicken Sie anschließend im Abschnitt **[!UICONTROL Aktionen]** auf **[!UICONTROL Hinzufügen]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Extension]** die Option **[!UICONTROL Mobile Core]** aus. Dann **[!UICONTROL Senden Sie Postback]** in der Dropdownliste **[!UICONTROL Aktionstyp]** .

1. Geben Sie in die **[!UICONTROL URL]** die folgende URL ein:

   ```
   https://{%%camp-server%%}/r/?id={%contextdata.broadlogId%},{%contextdata.deliveryId%},{%contextdata.action%}&mcId={%%mcid%%}
   ```

1. Aktivieren Sie das Kontrollkästchen &quot; **[!UICONTROL HinzufügenPost Body]** &quot;.

1. Hinzufügen Sie Ihren Beitragstext, z. B. { }.

1. Geben Sie unter **[!UICONTROL Content-Typ]** den Wert **application/json** ein.

1. Wählen Sie in **[!UICONTROL Timeout]** 0.

### Standort-Postback {#location-postback}

1. Klicken Sie [!DNL Experience Platform Launch]im Dashboard der Mobilanwendung auf die Registerkarte **[!UICONTROL Regeln]** und dann auf **[!UICONTROL Hinzufügen Regel]**.

1. Geben Sie einen Namen ein, z. B. **Location Postback**.

1. Klicken Sie im Abschnitt **[!UICONTROL Ereignisse]** auf **[!UICONTROL Hinzufügen]**.

1. Erstellen Sie ein Ereignis, z. B. &quot;POI eingeben&quot;oder &quot;POI beenden&quot;. Wählen Sie aus der Dropdownliste **[!UICONTROL Erweiterung]** die Option **Orte - Beta**. Geben Sie dann **POI** oder **Ausstiegspunkt** in der Dropdownliste **[!UICONTROL Ereignistyp]** ein.

1. Geben Sie einen Namen ein, z. B. **Orte - Beta - Geben Sie POI** ein oder **Ausstiegspunkt**.

1. Klicken Sie im Abschnitt **[!UICONTROL Aktionen]** auf **[!UICONTROL Hinzufügen]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Extension]** die Option **[!UICONTROL Mobile Core]** aus. Dann **[!UICONTROL Senden Sie Postback]** aus der Dropdownliste **[!UICONTROL Aktionstyp]** .

1. Geben Sie einen Namen ein, z. B. &quot; **Mobile Core - Location Postback** senden&quot;.

1. Geben Sie in die **[!UICONTROL URL]** die folgende URL ein:

   ```
   https://{%%camp-server%%}/rest/head/mobileAppV5/{%%pkey%%}/locations/
   ```

1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL HinzufügenBeitragstext]** und fügen Sie Ihren Beitragstext hinzu, z. B.:

   ```
   {
   "locationData": {
       "distances": "{%%Distance%%}",
       "poiLabel": "{%%POILabel%%}",
       "latitude": "{%%Latitude%%}",
       "longitude": "{%%Longitude%%}",
       "appId": "{%%AppId%%}",
       "marketingCloudId": "{%%ECID%%}"
   }
   }
   ```

   >[!NOTE]
   >
   >Im obigen Beispiel müssen die Datenelemente auf der rechten Seite konfiguriert werden, [!DNL Experience Platform Launch] indem die Schritte unter [Erstellen von Datenelementen](../../administration/using/configuring-rules-launch.md#create-data-elements)genutzt werden. Die Datenelemente auf der linken Seite werden in unterstützt [!DNL Adobe Campaign Standard] und benötigen keine Konfiguration. Wenn Sie zusätzliche Daten benötigen, müssen Sie benutzerdefinierte Ressourcenerweiterungen in durchführen [!DNL Adobe Campaign Standard].

1. Geben Sie unter **[!UICONTROL Content-Typ]** den Wert **application/json** ein.

1. Wählen Sie in **[!UICONTROL Timeout]** 5.

   ![](assets/rules_4.png)

---
title: Konfigurieren von Tag-Regeln zur Unterstützung von Adobe Campaign Standard-Anwendungsfällen
description: Erfahren Sie, wie sich Tag-Regeln zur Unterstützung von Adobe Campaign Standard-Anwendungsfällen konfigurieren lassen
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
feature: Instance Settings
role: Admin
level: Experienced
exl-id: b5f4f612-ea23-4007-b427-069777ecdd58
source-git-commit: 7767b39a48502f97e2b3af9d21a3f49b9283ab2e
workflow-type: ht
source-wordcount: '1169'
ht-degree: 100%

---

# Konfigurieren von Tag-Regeln zur Unterstützung von Adobe Campaign Standard-Anwendungsfällen {#configuring-rules-launch}

Erstellen Sie in der Datenerfassungs-UI Datenelemente und Regeln, damit personenbezogene Daten und andere Informationen von Mobile Apps an [!DNL Adobe Campaign Standard] gesendet werden können.

Damit alle Konfigurationsänderungen in der Datenerfassungs-UI in Kraft treten können, müssen Sie diese Änderungen veröffentlichen. Weitere Informationen finden Sie unter [Veröffentlichen](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration).

Gehen Sie wie folgt vor, um Regeln in der Datenerfassungs-UI zu erstellen:

1. [Datenelemente erstellen](../../administration/using/configuring-rules-launch.md#create-data-elements)
2. [Regeln für Anwendungsfälle erstellen](../../administration/using/configuring-rules-launch.md#create-data-elements), die Sie unterstützen möchten:
   * [Postback für personenbezogene Daten](../../administration/using/configuring-rules-launch.md#pii-postback)
   * [In-App-Tracking-Postback](../../administration/using/configuring-rules-launch.md#inapp-tracking-postback)
   * [Tracking-Postback für Push-Benachrichtigungen](../../administration/using/configuring-rules-launch.md#push-tracking-postback)
   * [Standort-Postback](../../administration/using/configuring-rules-launch.md#location-postback)

## Datenelemente erstellen {#create-data-elements}

Im Folgenden finden Sie die Datenelemente, die Sie in der Datenerfassungs-UI erstellen sollten.
Je nach Bedarf können Sie zusätzliche Datenelemente erstellen.

* **[!UICONTROL Experience-Cloud-ID]**
* **[!UICONTROL Pkey]**
* **[!UICONTROL Campaign-Server]**

So erstellen Sie diese Datenelemente:

1. Klicken Sie in der Datenerfassungs-UI über Ihr Mobile-App-Dashboard auf die Registerkarte **[!UICONTROL Datenelemente]**.

1. Um das Datenelement **[!UICONTROL Experience-Cloud-ID]** zu erstellen, klicken Sie auf **[!UICONTROL Neues Datenelement erstellen]**.

1. Geben Sie im Feld **[!UICONTROL Name]** beispielsweise **mcid** ein.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Erweiterung]** die Option **[!UICONTROL Mobile Core]** aus. Wählen Sie anschließend **[!UICONTROL Experience-Cloud-ID]** aus der Dropdown-Liste **[!UICONTROL Datenelement]** aus.

   ![](assets/do-not-localize/rules_1.png)

1. Klicken Sie auf **[!UICONTROL Datenelement hinzufügen]**, um das Datenelement „Pkey“ zu erstellen.

1. Geben Sie im Feld **[!UICONTROL Name]** beispielsweise **pkey** ein.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Erweiterung]** die Option **[!UICONTROL Adobe Campaign Standard]** aus. Wählen Sie anschließend **[!UICONTROL pkey]** aus der Dropdown-Liste **[!UICONTROL Datenelement]** aus.

1. Klicken Sie auf **[!UICONTROL Datenelement hinzufügen]**, um das Datenelement „Campaign Server“ zu erstellen.

1. Geben Sie im Feld **[!UICONTROL Name]** einen Namen ein, beispielsweise **camp-server**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Erweiterung]** die Option **[!UICONTROL Adobe Campaign Standard]** aus. Wählen Sie anschließend **[!UICONTROL Campaign Server]** aus der Dropdown-Liste **[!UICONTROL Datenelement]** aus.

## Regeln erstellen {#creating-rules}

Sie müssen Regeln für Folgendes erstellen:

* [Postback für personenbezogene Daten](../../administration/using/configuring-rules-launch.md#pii-postback)
* [In-App-Tracking-Postback](../../administration/using/configuring-rules-launch.md#inapp-tracking-postback)
* [Tracking-Postback für Push-Benachrichtigungen](../../administration/using/configuring-rules-launch.md#push-tracking-postback)
* [Standort-Postback](../../administration/using/configuring-rules-launch.md#location-postback)

### Postback für personenbezogene Daten {#pii-postback}

>[!NOTE]
>
>Um personenbezogene Informationen von einer Mobile App an Adobe Campaign zu senden, müssen Sie eine SDK-API implementieren. Weitere Informationen finden Sie unter [CollectPII](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#collect-pii).

Zum Senden von personenbezogenen Daten an [!DNL Adobe Campaign Standard] erstellen Sie eine Regel in der Datenerfassungs-UI:

1. Klicken Sie in der Datenerfassungs-UI im Dashboard Ihrer Mobile App auf die Registerkarte **[!UICONTROL Regeln]** und anschließend auf **[!UICONTROL Neue Regel erstellen]**.

1. Geben Sie einen Namen ein, beispielsweise **Mobile Core – Collect PII**.

1. Klicken Sie im Bereich **[!UICONTROL Ereignisse]** auf **[!UICONTROL Hinzufügen]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Erweiterung]** die Option **[!UICONTROL Mobile Core]** aus. Wählen Sie anschließend **[!UICONTROL PII abrufen]** aus der Dropdown-Liste **[!UICONTROL Ereignistyp]** aus.

1. Klicken Sie auf **[!UICONTROL Änderungen beibehalten]**.

1. Klicken Sie im Bereich **[!UICONTROL Aktionen]** auf **[!UICONTROL Hinzufügen]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Erweiterung]** die Option **[!UICONTROL Mobile Core]** aus. Wählen Sie anschließend **[!UICONTROL PII senden]** aus der Dropdown-Liste **[!UICONTROL Aktionstyp]** aus.

1. Geben Sie die folgende URL in **[!UICONTROL URL]** ein:

   ```
   https://{%%camp-server%%}/rest/head/mobileAppV5/{%%pkey%%}/subscriptions/{%%mcid%%}
   ```

1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL POST-Hauptteil hinzufügen]**.

1. Geben Sie Folgendes in **[!UICONTROL POST-Hauptteil]** ein:

   ```
   {
   "marketingCloudId":
   "{%%mcid%%}",
   "pushPlatform":
   "{%contextdata.pushPlatform%}",
   "cusEmail":
   "{%contextdata.email%}",
   "cusFirstName":
   "{%contextdata.firstName%}",
   "cusLastName":
   "{%contextdata.lastName%}" }
   ```

   Die ID für Marketing Cloud ermöglicht Ihnen den Abgleich Ihrer App-Abonnenten mit den Empfängern in der Datenbank und ist daher erforderlich. Sie können je nach Ihren Geschäftsanforderungen weitere Schlüssel-Werte-Paare angeben. Im obigen Beispiel werden E-Mail, Vorname und Nachname von der App übergeben.

   Die Schlüssel (z. B. cusEmail, cusFirstName und cusLastName) sollten mit den Feld-IDs übereinstimmen, die in Ihrer benutzerdefinierten Ressource in der Adobe Campaign Standard-Instanz definiert sind. Die Wertvariablen (z. B. E-Mail, Vorname und Nachname) sollten mit den Schlüsseln in den JSON-Daten übereinstimmen, die von der mobilen App gesendet werden, während die collectPII-API von AMS aus dem App-Code aufgerufen wird.

   Sie können auch abhängig von Ihren Ereignisauslösern Lebenszyklusdaten im Collect PII-Postback oder einem anderen Postback übergeben. Hier ist ein Beispiel für die Lebenszyklusdaten-JSON:

   ```
   {
   "marketingCloudId":"{%%mcid%%}",
   "pushPlatform":"{%contextdata.pushPlatform%}",
   "cusDayslastlaunch": "{%%DaysSinceLastUse%%}", 
   "cusDaysfirstlaunch": "{%%DaysSinceFirstUse%%}", 
   "cusLaunches": "{%%Launches%%}"
   }
   ```

   Die Datenelemente, die in der Datenerfassungs-UI definiert sind, sollten in doppelte Prozentzeichen (z. B. `%%mcid%%`) und die Kontextvariablen der Mobile App in einfache Prozentzeichen (z. B. %contextdata.email%) eingeschlossen werden.

1. Geben Sie unter **[!UICONTROL Content-Typ]** den Wert **application/json** ein.

1. Wählen Sie „0“ als **[!UICONTROL Zeitüberschreitung]** aus.

   ![](assets/do-not-localize/rules_2.png)

Ihre Benutzerdaten sind nun konfiguriert und können an Campaign gesendet werden.

### In-App-Tracking-Postback {#inapp-tracking-postback}

>[!NOTE]
>
>Wenn Sie Android ACPCore v1.4.0 oder höher bzw. iOS ACPCore v2.3.0 oder höher verwenden, ist die Konfiguration von Tracking-Postbacks nicht erforderlich.

Um Tracking-Daten zum Reporting über die Interaktion Ihrer Benutzer mit In-App-Nachrichten in der Mobile App an [!DNL Adobe Campaign Standard] zu senden, erstellen Sie die folgende Regel in der Datenerfassungs-UI:

1. Wählen Sie in der Datenerfassungs-UI über das Dashboard Ihrer Mobile App die Registerkarte **[!UICONTROL Regeln]** und klicken Sie auf **[!UICONTROL Regel hinzufügen]**.

1. Geben Sie einen Namen ein, beispielsweise **Adobe Campaign - In-App Klick-Tracking**.

1. Klicken Sie im Bereich **[!UICONTROL Ereignisse]** auf **[!UICONTROL Hinzufügen]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Erweiterung]** die Option **[!UICONTROL Adobe Campaign Standard]** aus. Wählen Sie anschließend **[!UICONTROL In-App Klick-Tracking]** aus der Dropdown-Liste **[!UICONTROL Ereignistyp]** aus.

1. Klicken Sie auf **[!UICONTROL Änderungen beibehalten]**.

1. Klicken Sie im Bereich **[!UICONTROL Aktionen]** auf **[!UICONTROL Hinzufügen]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Erweiterung]** die Option **[!UICONTROL Mobile Core]** aus. Wählen Sie anschließend **[!UICONTROL Postback senden]** aus der Dropdown-Liste **[!UICONTROL Ereignistyp]** aus.

1. Geben Sie die folgende URL in **[!UICONTROL URL]** ein:

   ```
   https://{%%camp-server%%}/r/?id={%id%}&mcid={%%mcid%%}
   ```

1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL POST-Hauptteil hinzufügen]**.

1. Geben Sie in **[!UICONTROL POST-Hauptteil]** **{}** ein.

1. Geben Sie unter **[!UICONTROL Content-Typ]** den Wert **application/json** ein.

1. Wählen Sie „0“ als **[!UICONTROL Zeitüberschreitung]** aus.

   ![](assets/do-not-localize/rules_3.png)

### Tracking-Postback für Push-Benachrichtigungen {#push-tracking-postback}

>[!NOTE]
>
>Wenn Sie Android ACPCore v1.4.0 oder höher bzw. iOS ACPCore v2.3.0 oder höher verwenden, ist die Konfiguration von Tracking-Postbacks nicht erforderlich.

Um Tracking-Daten an [!DNL Adobe Campaign Standard] zu senden, damit Ihre Push-Benachrichtigung und die Benutzerinteraktionen mit Ihrer Mobile App getrackt werden können, müssen Sie eine Regel in der Datenerfassungs-UI erstellen.

Weitere Informationen zum Push-Tracking finden Sie im Abschnitt [Push-Tracking](../../administration/using/push-tracking.md).

Verwenden Sie die trackAction-API, um App-Aktionen zu tracken. Weitere Informationen finden Sie unter [App-Aktionen tracken](https://app.gitbook.com/@aep-sdks/s/docs/using-mobile-extensions/mobile-core/mobile-core-api-reference#track-app-actions).

1. Klicken Sie in der Datenerfassungs-UI über das Dashboard Ihrer Mobile App auf die Registerkarte **[!UICONTROL Regeln]** und anschließend auf **[!UICONTROL Neue Regel hinzufügen]**.

1. Geben Sie einen Namen ein, beispielsweise **Adobe Campaign - push click tracking**.

1. Klicken Sie im Bereich **[!UICONTROL Ereignisse]** auf **[!UICONTROL Hinzufügen]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Erweiterung]** die Option **[!UICONTROL Mobile Core]** aus. Wählen Sie anschließend **[!UICONTROL Aktion tracken]** aus der Dropdown-Liste **[!UICONTROL Ereignistyp]** aus.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Aktion]** die Option **[!UICONTROL Aktion]** aus. Wählen Sie **[!UICONTROL ist gleich]** aus und geben Sie **Tracking** ein.

1. Klicken Sie auf **[!UICONTROL Änderungen beibehalten]**. Klicken Sie anschließend im Bereich **[!UICONTROL Aktionen]** auf **[!UICONTROL Hinzufügen]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Erweiterung]** die Option **[!UICONTROL Mobile Core]** aus. Wählen Sie anschließend **[!UICONTROL Postback senden]** aus der Dropdown-Liste **[!UICONTROL Aktionstyp]** aus.

1. Geben Sie die folgende URL in **[!UICONTROL URL]** ein:

   ```
   https://{%%camp-server%%}/r/?id={%contextdata.broadlogId%},{%contextdata.deliveryId%},{%contextdata.action%}&mcId={%%mcid%%}
   ```

1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL POST-Hauptteil hinzufügen]**.

1. Geben Sie Ihren POST-Hauptteil ein, beispielsweise „{ }“.

1. Geben Sie unter **[!UICONTROL Content-Typ]** den Wert **application/json** ein.

1. Wählen Sie „0“ als **[!UICONTROL Zeitüberschreitung]** aus.

### Standort-Postback {#location-postback}

1. Klicken Sie in der Datenerfassungs-UI über das Dashboard Ihrer Mobile App auf die Registerkarte **[!UICONTROL Regeln]** und anschließend auf **[!UICONTROL Neue Regel hinzufügen]**.

1. Geben Sie einen Namen ein, beispielsweise **Standort-Postback**.

1. Klicken Sie im Bereich **[!UICONTROL Ereignisse]** auf **[!UICONTROL Hinzufügen]**.

1. Erstellen Sie ein Ereignis, beispielsweise „Enter POI“ oder „Exit POI“. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Erweiterung]** die Option **Places – Betaversion** aus. Wählen Sie anschließend **Enter POI** oder **Exit POI** aus der Dropdown-Liste **[!UICONTROL Ereignistyp]** aus.

1. Geben Sie einen Namen ein, beispielsweise **Places - Betaversion - Enter POI** oder **Exit POI**.

1. Klicken Sie im Bereich **[!UICONTROL Aktionen]** auf **[!UICONTROL Hinzufügen]**.

1. Wählen Sie aus der Dropdown-Liste **[!UICONTROL Erweiterung]** die Option **[!UICONTROL Mobile Core]** aus. Wählen Sie anschließend **[!UICONTROL Postback senden]** aus der Dropdown-Liste **[!UICONTROL Aktionstyp]** aus.

1. Geben Sie einen Namen ein, beispielsweise **Mobile Core - Send Location Postback**.

1. Geben Sie die folgende URL in **[!UICONTROL URL]** ein:

   ```
   https://{%%camp-server%%}/rest/head/mobileAppV5/{%%pkey%%}/locations/
   ```

1. Aktivieren Sie das Kontrollkästchen **[!UICONTROL POST-Hauptteil hinzufügen]** und geben Sie Ihren POST-Hauptteil ein, beispielsweise:

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
   >Im obigen Beispiel müssen die Datenelemente auf der rechten Seite in der Datenerfassungs-UI konfiguriert werden. Nutzen Sie dazu die Schritte unter [Erstellen von Datenelementen](../../administration/using/configuring-rules-launch.md#create-data-elements). Die Datenelemente auf der linken Seite werden in [!DNL Adobe Campaign Standard] unterstützt und müssen nicht konfiguriert werden. Wenn Sie zusätzliche Daten benötigen, müssen Sie in [!DNL Adobe Campaign Standard] benutzerdefinierte Ressourcenerweiterungen ausführen.

1. Geben Sie unter **[!UICONTROL Content-Typ]** den Wert **application/json** ein.

1. Wählen Sie „5“ als **[!UICONTROL Zeitüberschreitung]** aus.

   ![](assets/do-not-localize/rules_4.png)

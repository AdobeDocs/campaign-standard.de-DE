---
title: Transaktionsnachrichten konfigurieren
description: Hier erfahren Sie, wie Transaktionsnachrichten konfiguriert werden.
page-status-flag: never-activated
uuid: 4caeadbe-f4a7-43ce-986d-e99fa9ca0d0d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 3f968556-e774-43dc-a0b8-7188d7665fbc
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 34f4bbf7b7913cfb1833379c963b590961f7de73

---


# Transaktionsnachrichten konfigurieren{#configuring-transactional-messaging}

Um eine Transaktionsnachricht mit Adobe Campaign zu senden, müssen Sie zunächst die Struktur der Ereignisdaten definieren.

Die Ereigniskonfiguration muss von einem **Administrator** durch Ausführung der folgenden Schritte vorgenommen werden:

Je nach dem Typ der zu sendenden Transaktionsnachricht kann die Konfiguration unterschiedlich sein. Lesen Sie diesbezüglich auch den Abschnitt [Konfigurationen für Transaktionsereignisse](#transactional-event-specific-configurations).

Nach der Publikation des Ereignisses wird die entsprechende Transaktionsnachricht automatisch erstellt. Weiterführende Informationen zum Thema Transaktionsnachrichten finden Sie auf [dieser Seite](../../channels/using/about-transactional-messaging.md).

## Ereignis erstellen   {#creating-an-event}

Erstellen Sie das Ereignis zunächst entsprechend Ihren Anforderungen.

1. Klicken Sie auf das **[!UICONTROL Adobe Campaign]** Logo in der oberen linken Ecke und wählen Sie dann **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Event configuration]**.
1. Click the **[!UICONTROL Create]** button.
1. Give a **[!UICONTROL Label]** and an **[!UICONTROL ID]** to the event. Das Feld **[!UICONTROL ID]** ist ein Pflichtfeld und sollte mit dem Präfix &quot;EVT&quot; beginnen. If you do not use this prefix, it is automatically added once you click **[!UICONTROL Create]**.

   ![](assets/message-center_1.png)

   >[!IMPORTANT]
   >
   >Die Kennung einschließlich des EVT-Präfixes darf maximal 64 Zeichen lang sein.

1. Select the channel that will be used to send your transactional messages **[!UICONTROL Email]**, **[!UICONTROL Mobile (SMS)]** or **[!UICONTROL Mobile application]** (push notification).

   >[!NOTE]
   >
   >Für jede Ereigniskonfiguration kann jeweils nur ein Kanal verwendet werden. Nach der Erstellung des Ereignisses lässt sich der Kanal nicht mehr ändern.

1. Select the targeting dimension corresponding to the desired event configuration and click **[!UICONTROL Create]**.

   Bei ereignisbasierten Transaktionsnachrichten werden die im Ereignis selbst vorhandenen Daten verwendet, während bei profilbasierten Transaktionsnachrichten die in der Adobe-Campaign-Datenbank verfügbaren Daten verwendet werden. Lesen Sie diesbezüglich auch den Abschnitt [Konfigurationen für Transaktionsereignisse](#transactional-event-specific-configurations).

## Ereignisattribute definieren   {#defining-the-event-attributes}

In the **[!UICONTROL Fields]** section, define the attributes that will be integrated into the event content and will then be able to be used to personalize the transactional message.

Alle das Hinzufügen oder Ändern von Feldern betreffenden Schritte folgen dem gleichen Prinzip wie für [benutzerdefinierte Ressourcen](../../developing/using/configuring-the-resource-s-data-structure.md#adding-fields-to-a-resource).

![](assets/message-center_2.png)

>[!NOTE]
>
>Wenn Sie eine mehrsprachige Transaktionsnachricht erstellen möchten, definieren Sie ein zusätzliches Ereignisattribut mit der ID **[!UICONTROL AC_language]**. Dies gilt nur für Transaktionsnachrichten. Nach der Publikation des Ereignisses sind die Schritte zur Bearbeitung des Inhalts einer mehrsprachigen Transaktionsnachricht dieselben wie für eine mehrsprachige Standard-E-Mail. Siehe [Mehrsprachige E-Mail erstellen](../../channels/using/creating-a-multilingual-email.md).

## Datenkollektionen definieren   {#defining-data-collections}

Sie können zum Ereignisinhalt eine Kollektion von Elementen hinzufügen, wobei jedes Element mehrere Attribute enthält.

Diese Kollektion kann in Transaktions-E-Mails verwendet werden, um Produktlisten zum Nachrichteninhalt hinzuzufügen, wie z. B. eine Liste mit Produkten einschließlich Preis, Referenznummer, Menge etc. für jedes Produkt auf der Liste.

1. Klicken Sie im **[!UICONTROL Collections]** Abschnitt auf die **[!UICONTROL Create element]** Schaltfläche.

   ![](assets/message-center_collection_create.png)

1. Fügen Sie Ihrer Kollektion einen Titel und eine Kennung hinzu.
1. Fügen Sie alle Felder hinzu, die Sie für jedes Produkt der Liste in der Transaktionsnachricht anzeigen möchten.

   Für dieses Beispiel haben wir folgende Felder hinzugefügt:

   ![](assets/message-center_collection_fields.png)

Nach der Publikation des Ereignisses sowie der Nachricht lässt sich diese Kollektion in den Transaktionsnachrichten verwenden.

Dies ist die API-Vorschau für dieses Beispiel:

![](assets/message-center_collection_api-preview.png)

**Verwandte Themen:**

* [Vorschau erstellen und Ereignis publizieren](#previewing-and-publishing-the-event)
* [Produktlisten in Transaktionsnachrichten verwenden](../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message)

## Inhalt der Transaktionsnachricht anreichern {#enriching-the-transactional-message-content}

Durch die Anreicherung der Transaktionsnachrichten mit Informationen aus der Adobe-Campaign-Datenbank können Nachrichten personalisiert werden. Ausgehend vom Nachnamen oder der CRM-ID all Ihrer Empfänger können Sie beispielsweise Daten wie deren jeweilige Adresse oder das Geburtsdatum oder jedes beliebige in der Profiltabelle hinzugefügte benutzerdefinierte Feld abrufen, um die den Empfängern gesendeten Informationen zu personalisieren.

It is possible to enrich the transactional message content with information from extended **[!UICONTROL Profile]** or **[!UICONTROL Service]** resources.

Diese Informationen können auch in neuen Ressourcen gespeichert werden. In that case, the resource must be linked to the **[!UICONTROL Profile]** or **[!UICONTROL Service]** resources either directly, or via another table. For example, in the configuration below, it is possible to enrich the transactional message content with information from the **[!UICONTROL Product]** resource like the product category or ID, if the **[!UICONTROL Product]** resource is linked to the **[!UICONTROL Profile]** resource.

![](assets/message-center_usecaseschema.png)

Weiterführende Informationen zur Erstellung und Publikation von Ressourcen finden Sie auf [dieser Seite](../../developing/using/key-steps-to-add-a-resource.md).

1. Klicken Sie im **[!UICONTROL Enrichment]** Abschnitt auf die **[!UICONTROL Create element]** Schaltfläche.

   ![](assets/message-center_addenrichment.png)

1. Wählen Sie die Ressource aus, mit der Sie Ihre Nachricht verknüpfen möchten. In this case, choose the **[!UICONTROL Profile]** resource.

   ![](assets/message-center_new-enrichment.png)

1. Use the **[!UICONTROL Create element]** button to link a field from the selected resource to one of the fields you previously added to the event (see [Defining the event attributes](#defining-the-event-attributes)).

   ![](assets/message-center_enrichment-join.png)

1. In this example, we reconcile the **[!UICONTROL Last name]** and the **[!UICONTROL First name]** fields with the corresponding fields in the **[!UICONTROL Profile]** resource.

   ![](assets/message-center_enrichment-join-fields.png)

   You can also enrich the transactional message content using the **[!UICONTROL Service]** resource. For more on services, see this [section](../../audiences/using/creating-a-service.md).

1. Wenn Sie ein Profil-basiertes Ereignis erstellen oder bearbeiten, wählen Sie im **[!UICONTROL Targeting enrichment]** Abschnitt die Anreicherung aus, die während der Ausführung des Versands als Zielgruppe der Nachricht verwendet wird.

   ![](assets/message-center_marketing_targeting_enrichment.png)

   >[!NOTE]
   >
   >Die Auswahl einer Targeting-Anreicherung basierend auf der **[!UICONTROL Profile]** Ressource ist für Profil-basierte Ereignis obligatorisch.

Sobald das Ereignis und die Nachricht veröffentlicht wurden, können Sie über diesen Link den Inhalt der Transaktionsnachricht bereichern.

**Verwandte Themen:**

* [Vorschau erstellen und Ereignis publizieren](#previewing-and-publishing-the-event).
* [Transaktionsnachricht personalisieren](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message).

## Vorschau erstellen und Ereignis publizieren {#previewing-and-publishing-the-event}

Bevor Sie das Ereignis verwenden können, müssen Sie eine Vorschau erstellen und es publizieren.

1. Click the **[!UICONTROL API preview]** button to see a simulation of the REST API that will be used by your website developer before it is published. Nach der Publikation des Ereignisses dient diese Schaltfläche des Weiteren dazu, eine Vorschau der in Produktion befindlichen API anzuzeigen. Siehe [Aktivierung des Ereignisses in eine Website integrieren](#integrating-the-triggering-of-the-event-in-a-website).

   ![](assets/message-center_api_preview.png)

   >[!NOTE]
   >
   >Die REST-API variiert je nach ausgewähltem Kanal und nach ausgewählter Zielgruppendimension. Weiterführende Informationen zu den unterschiedlichen Konfigurationen finden Sie unter [Konfigurationen für Transaktionsereignisse](#transactional-event-specific-configurations).

1. Click **[!UICONTROL Publish]** to start publication.

   ![](assets/message-center_pub.png)

1. Die Veröffentlichungsprotokolle können auf der entsprechenden Registerkarte Ansicht werden.

   ![](assets/message-center_logs.png)

   >[!IMPORTANT]
   >
   >Each time you modify the event, you must click **[!UICONTROL Publish]** again to generate the updated REST API that will be used by your website developer.

   Mit Ausführung der Publikation wird automatisch eine dem neuen Ereignis entsprechende Transaktionsnachricht erzeugt.

1. Sie können direkt über den Link auf der linken Seite auf diese Transaktionsnachricht zugreifen.

   ![](assets/message-center_messagegeneration.png)

In order for the event to trigger sending a transactional message, you must modify and publish the message that was just created. See [Event transactional messages](../../channels/using/event-transactional-messages.md).

Außerdem muss die Auslösung dieses Ereignisses in Ihre Webseite integriert werden. Siehe [Aktivierung des Ereignisses in eine Website integrieren](#integrating-the-triggering-of-the-event-in-a-website).

Sobald Adobe Campaign-Beginn Ereignis im Zusammenhang mit dieser Ereignis-Konfiguration erhalten, können Sie über den **[!UICONTROL Latest transactional events]** Link unter dem **[!UICONTROL History]** Abschnitt auf die neuesten Ereignis zugreifen, die von Ihrem Drittanbieterdienst gesendet und von Adobe Campaign verarbeitet werden.

![](assets/message-center_latest-events.png)

Die Ereignis (im JSON-Format) werden von der letzten bis zur ältesten aufgelistet. Mit dieser Liste können Sie Daten wie den Inhalt oder den Status eines Ereignisses zu Kontroll- und Debugging-Zwecken überprüfen.

### Ereignis depublizieren   {#unpublishing-an-event}

The **[!UICONTROL Unpublish]** button lets you cancel the publication of the event, which deletes from the REST API the resource corresponding to the event that you previously created. Selbst wenn das Ereignis auf Ihrer Webseite ausgelöst wird, werden die entsprechenden Nachrichten nun nicht mehr gesendet und auch nicht in der Datenbank gespeichert.

![](assets/message-center_unpublish.png)

>[!NOTE]
>
>Sollten Sie die entsprechende Transaktionsnachricht bereits publiziert haben, wird die Transaktionsnachrichtenpublikation ebenfalls abgebrochen. Siehe [Transaktionsnachricht depublizieren](../../channels/using/event-transactional-messages.md#unpublishing-a-transactional-message).

Click the **[!UICONTROL Publish]** button to generate a new REST API.

### Löschen eines Ereignisses {#deleting-an-event}

Wenn die Veröffentlichung eines Ereignisses rückgängig gemacht wurde oder ein Ereignis noch nicht veröffentlicht wurde, können Sie es aus der Liste zur Ereignis-Konfiguration löschen. Gehen Sie dazu wie folgt vor:

1. Klicken Sie auf das **[!UICONTROL Adobe Campaign]** Logo in der oberen linken Ecke und wählen Sie dann **[!UICONTROL Marketing plans]** > **[!UICONTROL Transactional messages]** > **[!UICONTROL Event configuration]**.
1. Bewegen Sie den Mauszeiger über die gewünschte Ereignis-Konfiguration und wählen Sie die **[!UICONTROL Delete element]** Schaltfläche aus.

   ![](assets/message-center_delete-button.png)

   >[!NOTE]
   >
   >Vergewissern Sie sich, dass die Konfiguration des Ereignisses den **[!UICONTROL Draft]** Status hat, andernfalls können Sie sie nicht löschen. Der **[!UICONTROL Draft]** Status gilt für ein Ereignis, das noch nicht veröffentlicht wurde oder dessen Veröffentlichung [rückgängig gemacht](#unpublishing-an-event)wurde.

1. Click the **[!UICONTROL Confirm]** button.

   ![](assets/message-center_delete-confirm.png)

>[!IMPORTANT]
>
>Wenn Sie eine bereits veröffentlichte und verwendete Ereignis-Konfiguration löschen, werden auch die entsprechende(n) Transaktionsnachricht(n) sowie deren Senden und Trackinglogs gelöscht.

## Aktivierung des Ereignisses in eine Website integrieren {#integrating-the-triggering-of-the-event-in-a-website}

Nach der Erstellung des gewünschten Ereignisses muss die Auslösung dieses Ereignisses in Ihre Webseite integriert werden.

In dem in Abschnitt [Funktionsweise von Transaktionsnachrichten](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) beschriebenen Beispiel wird ein Ereignis vom Typ &quot;Stehen gelassener Warenkorb&quot; ausgelöst, wenn ein Besucher Ihre Webseite verlassen hat, ohne den Kauf der Artikel in seinem Warenkorb abzuschließen. Zu diesem Zweck muss der Web-Entwickler Ihrer Seite die Adobe Campaign Standard REST-API verwenden.

Weiterführende Informationen dazu finden Sie im Abschnitt [REST-API-Dokumentation](../../api/using/managing-transactional-messages.md) .

## Konfigurationen für Transaktionsereignisse {#transactional-event-specific-configurations}

Die Konfiguration von Transaktionsereignissen variiert je nach dem Typ der zu sendenden Transaktionsnachricht (Ereignis oder Profil) und dem verwendeten Kanal.

In den folgenden Abschnitten wird beschrieben, welche Konfiguration für die jeweilige Transaktionsnachricht festgelegt werden sollte. Weiterführende Informationen zu den allgemeinen Schritten bei der Konfiguration eines Ereignisses finden Sie im Abschnitt   [Ereignis erstellen](#creating-an-event).

### Ereignisbasierte Transaktionsnachrichten {#event-based-transactional-messages}

Um eine ereignisbasierte Transaktionsnachricht zu senden, erstellen und konfigurieren Sie zunächst ein Ereignis, bei dem die im Ereignis selbst enthaltenen Daten zur Zielgruppenbestimmung verwendet werden.
Weiterführende Informationen finden Sie unter [Interaktionen fördern mit Transaktionsnachrichten](https://helpx.adobe.com/campaign/kb/simplify-campaign-management.html#Managedatatofuelengagingexperiences).

1. When creating the event configuration, select the **[!UICONTROL Real-time event]** targeting dimension (see [Creating an event](#creating-an-event)).
1. Fügen Sie zum Ereignis Felder hinzu, damit Sie die Transaktionsnachricht personalisieren können (siehe [Ereignisattribute definieren](#defining-the-event-attributes)).
1. Reichern Sie den Inhalt der Transaktionsnachricht an, wenn Sie Zusatzinformationen aus der Adobe-Campaign-Datenbank verwenden möchten (siehe [Inhalt der Transaktionsnachricht anreichern](#enriching-the-transactional-message-content)).

   >[!NOTE]
   >
   >Beim ereignisbasierten Transaktionsnachrichtenversand sollen ausschließlich die Daten verwendet werden, die im gesendeten Ereignis der Personalisierung von Empfängern und Nachrichteninhalten dienen. Der Inhalt Ihrer Transaktionsnachricht lässt sich jedoch durch die Verwendung von in der Adobe-Campaign-Datenbank enthaltenen Informationen anreichern.

1. Erstellen Sie eine Vorschau und publizieren Sie das Ereignis (siehe [Vorschau erstellen und Ereignis publizieren](#previewing-and-publishing-the-event)).

   Bei der Vorschau des Ereignisses enthält die REST-API ein Attribut, mit dem entsprechend dem ausgewählten Kanal die E-Mail-Adresse oder das Mobiltelefon spezifiziert wird.

   Mit Ausführung der Publikation wird automatisch eine dem neuen Ereignis entsprechende Transaktionsnachricht erzeugt. Damit das entsprechende Ereignis den Versand der Transaktionsnachricht auslösen kann, muss die Transaktionsnachricht angepasst und publiziert werden; siehe [Ereignis-Transaktionsnachrichten](../../channels/using/event-transactional-messages.md).

1. Integrieren Sie das Ereignis in Ihre Website (siehe [Aktivierung des Ereignisses in eine Website integrieren](#integrating-the-triggering-of-the-event-in-a-website)).

### Profilbasierte Transaktionsnachrichten   {#profile-based-transactional-messages}

Um eine profilbasierte Transaktionsnachricht zu senden, erstellen und konfigurieren Sie zunächst ein Ereignis, bei dem die in der Adobe-Campaign-Datenbank enthaltenen Daten zur Zielgruppenbestimmung verwendet werden.

1. When creating the event configuration, select the **[!UICONTROL Profile event]** targeting dimension (see [Creating an event](#creating-an-event)).
1. Fügen Sie zum Ereignis Felder hinzu, damit Sie die Transaktionsnachricht personalisieren können (siehe [Ereignisattribute definieren](#defining-the-event-attributes)). Für eine Anreicherung müssen Sie mindestens ein Feld hinzufügen. Sie müssen keine anderen Felder wie **Vorname** und **Nachname** erstellen, da Sie Personalisierungsfelder aus der Adobe-Campaign-Datenbank verwenden können.
1. Create an enrichment in order to link the event to the **[!UICONTROL Profile]** resource (see [Enriching the transactional message content](#enriching-the-transactional-message-content)). Creating an enrichment is mandatory when using a **[!UICONTROL Profile]** targeting dimension.
1. Erstellen Sie eine Vorschau und publizieren Sie das Ereignis (siehe [Vorschau erstellen und Ereignis publizieren](#previewing-and-publishing-the-event)).

   When previewing the event, the REST API does not contain an attribute specifying the email address or the mobile phone as it will be retrieved from the **[!UICONTROL Profile]** resource.

   Mit Ausführung der Publikation wird automatisch eine dem neuen Ereignis entsprechende Transaktionsnachricht erzeugt. Damit das entsprechende Ereignis den Versand der Transaktionsnachricht auslösen kann, muss die soeben erstellte Nachricht angepasst und publiziert werden; siehe [Profil-Transaktionsnachricht senden](../../channels/using/profile-transactional-messages.md#sending-a-profile-transactional-message).

1. Integrieren Sie das Ereignis in Ihre Website (siehe [Aktivierung des Ereignisses in eine Website integrieren](#integrating-the-triggering-of-the-event-in-a-website)).

### Ereignisbasierte Transaktions-Push-Benachrichtigungen   {#event-based-transactional-push-notifications}

Für den Versand von Transaktions-Push-Benachrichtigungen müssen Sie Adobe Campaign entsprechend konfigurieren. Siehe [Konfiguration von Push-Benachrichtigungen](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html).

Um eine anonyme Transaktions-Push-Benachrichtigung an alle Benutzer zu senden, die sich für den Empfang von Benachrichtigungen von Ihrer Mobile App angemeldet haben, erstellen und konfigurieren Sie zunächst ein Ereignis, bei dem die im Ereignis selbst enthaltenen Daten zur Zielgruppenbestimmung verwendet werden. Die entsprechenden Schritte finden Sie unten.

Das Ereignis muss diese drei Elemente enthalten:

* Einen **Anmeldetoken** als Nutzerkennung für eine Mobile App und ein Gerät. Möglicherweise entspricht es keinem Profil in der Adobe-Campaign-Datenbank.
* Einen **Mobile-App-Namen** (einen für alle Geräte – Android und iOS). Dies ist die Kennung der in Adobe Campaign konfigurierten Mobile App, die für den Empfang von Push-Benachrichtigungen auf den Geräten des Benutzers verwendet wird. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://helpx.adobe.com/campaign/kb/configuring-app-sdkv4.html)
* Eine **Push-Plattform** (&quot;gcm&quot; für Android oder &quot;apns&quot; für iOS).

1. When creating the event configuration, select the **[!UICONTROL Mobile application]** channel and the **[!UICONTROL Real-time event]** targeting dimension (see [Creating an event](#creating-an-event)).
1. Fügen Sie zum Ereignis Felder hinzu, damit Sie die Transaktionsnachricht personalisieren können (siehe [Ereignisattribute definieren](#defining-the-event-attributes)).
1. Reichern Sie den Inhalt der Transaktionsnachricht an, wenn Sie Zusatzinformationen aus der Adobe-Campaign-Datenbank verwenden möchten (siehe [Inhalt der Transaktionsnachricht anreichern](#enriching-the-transactional-message-content)).

   >[!NOTE]
   >
   >Beim ereignisbasierten Transaktionsnachrichtenversand sollen ausschließlich die Daten verwendet werden, die im gesendeten Ereignis der Personalisierung von Empfängern und Nachrichteninhalten dienen. Der Inhalt Ihrer Transaktionsnachricht lässt sich jedoch durch die Verwendung von in der Adobe-Campaign-Datenbank enthaltenen Informationen anreichern.

1. Erstellen Sie eine Vorschau und publizieren Sie das Ereignis (siehe [Vorschau erstellen und Ereignis publizieren](#previewing-and-publishing-the-event)).

   Bei der Vorschau des Ereignisses enthält die REST-API die Attribute &quot;registrationToken&quot;, &quot;application&quot; und &quot;pushPlatform&quot;, die für die Zielgruppenbestimmung des Versands verwendet werden.

   ![](assets/message-center_push_api.png)

   Mit Ausführung der Publikation wird automatisch eine dem neuen Ereignis entsprechende Transaktions-Push-Benachrichtigung erzeugt. Um die soeben erstellte Nachricht anzupassen und zu publizieren, siehe [Transaktions-Push-Benachrichtigungen senden, bei denen die Zielgruppenbestimmung durch ein Ereignis erfolgt](../../channels/using/transactional-push-notifications.md#transactional-push-notifications-targeting-an-event).

1. Integrieren Sie das Ereignis in Ihre Website (siehe [Aktivierung des Ereignisses in eine Website integrieren](#integrating-the-triggering-of-the-event-in-a-website)).

### Profilbasierte Transaktions-Push-Benachrichtigungen   {#profile-based-transactional-push-notifications}

Um eine Transaktions-Push-Benachrichtigung an die Adobe-Campaign-Profile zu senden, die sich für Ihre Mobile App angemeldet haben, müssen Sie zunächst ein Ereignis erstellen und konfigurieren, bei dem die in der Adobe-Campaign-Datenbank enthaltenen Daten zur Zielgruppenbestimmung verwendet werden.

1. When creating the event configuration, select the **[!UICONTROL Mobile application]** channel and the **[!UICONTROL Profile]** targeting dimension (see [Creating an event](#creating-an-event)).

   Standardmäßig wird die Transaktions-Push-Benachrichtigung an alle Mobile Apps gesendet, für die sich der Empfänger angemeldet hat. Um die Push-Benachrichtigung an eine bestimmte Mobile App zu senden, wählen Sie sie in der Liste aus. Die anderen Mobile Apps werden zwar bei der Zielgruppenbestimmung der Nachricht berücksichtigt, aber vom Versand ausgeschlossen.

   ![](assets/message-center_push_appfilter.png)

1. Fügen Sie zum Ereignis Felder hinzu, wenn Sie die Transaktionsnachricht personalisieren möchten (siehe [Ereignisattribute definieren](#defining-the-event-attributes)).

   >[!NOTE]
   >
   >Für eine Anreicherung müssen Sie mindestens ein Feld hinzufügen. Sie müssen keine anderen Felder wie **Vorname** und **Nachname** erstellen, da Sie Personalisierungsfelder aus der Adobe-Campaign-Datenbank verwenden können.

1. Create an enrichment in order to link the event to the **[!UICONTROL Profile]** resource (see [Enriching the transactional message content](#enriching-the-transactional-message-content)). Creating an enrichment is mandatory when using a **[!UICONTROL Profile]** targeting dimension.
1. Erstellen Sie eine Vorschau und publizieren Sie das Ereignis (siehe [Vorschau erstellen und Ereignis publizieren](#previewing-and-publishing-the-event)).

   When previewing the event, the REST API does not contain an attribute specifying the registration token, the application name and the push platform as they will be retrieved from the **[!UICONTROL Profile]** resource.

   Mit Ausführung der Publikation wird automatisch eine dem neuen Ereignis entsprechende Transaktions-Push-Benachrichtigung erzeugt. Um die soeben erstellte Nachricht anzupassen und zu publizieren, siehe [Transaktions-Push-Benachrichtigungen senden, bei denen die Zielgruppenbestimmung durch ein Profil erfolgt](../../channels/using/transactional-push-notifications.md#transactional-push-notifications-targeting-a-profile).

1. Integrieren Sie das Ereignis in Ihre Website (siehe [Aktivierung des Ereignisses in eine Website integrieren](#integrating-the-triggering-of-the-event-in-a-website)).

### Ereignis konfigurieren, um eine Folgenachricht zu senden   {#configuring-an-event-to-send-a-follow-up-message}

Eine Folgenachricht ist eine vordefinierte Marketing-Versandvorlage, die in einem Workflow verwendet werden kann, um Nachrichten an die Empfänger einer bestimmten Transaktionsnachricht zu senden. Lesen Sie diesbezüglich auch den Abschnitt [Folgenachrichten](../../channels/using/follow-up-messages.md).

1. Verwenden Sie dieselbe Ereigniskonfiguration wie für den Versand einer Ereignis-Transaktionsnachricht. Siehe [Ereignisbasierte Transaktionsnachrichten](#event-based-transactional-messages).
1. Markieren Sie beim Konfigurieren des Ereignisses das **[!UICONTROL Create follow-up delivery template for this event]** Kästchen, bevor Sie das Ereignis veröffentlichen.

   ![](assets/message-center_follow-up-checkbox.png)

1. Erstellen Sie eine Vorschau und publizieren Sie das Ereignis (siehe [Vorschau erstellen und Ereignis publizieren](#previewing-and-publishing-the-event)).

   Mit Ausführung der Publikation werden automatisch eine dem neuen Ereignis entsprechende Transaktionsnachricht und eine Folgenachricht aus einer Versandvorlage erzeugt. Lesen Sie zur Verwendung von Folgenachrichten auch den Abschnitt [Folgenachrichten senden](../../channels/using/follow-up-messages.md#sending-a-follow-up-message).

## Anwendungsbeispiel: Konfiguration eines Ereignisses zum Senden einer Transaktionsnachricht   {#use-case--configuring-an-event-to-send-a-transactional-message}

In diesem Beispiel möchten wir ein Ereignis konfigurieren, um nach jedem Kauf auf unserer Website eine Bestätigungsnachricht mit folgenden Merkmalen zu senden:

As we want to identify our client via his CRM ID, first make sure that the **[!UICONTROL Profile]** resource has been extended with this new field.

In the same way, a custom resource corresponding to purchases must have been created and published, and must be linked to the **[!UICONTROL Profile]** resource. Auf diese Weise werden Sie in der Lage sein, Informationen aus dieser Ressource zur Anreicherung des Nachrichteninhalts abzurufen.

Weiterführende Informationen zur Erstellung und Publikation von Ressourcen finden Sie auf [dieser Seite](../../developing/using/key-steps-to-add-a-resource.md).

1. Create a new event using the **[!UICONTROL Email]** channel and the **[!UICONTROL Profile]** targeting dimension (see [Creating an event](#creating-an-event)).
1. Definieren Sie die Attribute, die zur Personalisierung der Transaktionsnachricht verfügbar sein sollen. Fügen Sie in unserem Fall die Felder &quot;CRM ID&quot; und &quot;Produktkennung&quot; hinzu (siehe [Ereignisattribute definieren](#defining-the-event-attributes)).

   ![](assets/message-center_usecase1.png)

1. To enrich the message content with information regarding the client&#39;s previous purchases, create an enrichment targeting the **[!UICONTROL Purchase]** resource (see [Enriching the transactional message content](#enriching-the-transactional-message-content)).

   ![](assets/message-center_usecase2.png)

1. Create a join condition between the &quot;Product identifier&quot; field that was previously added to the message, and the corresponding field from the **[!UICONTROL Purchase]** resource.

   ![](assets/message-center_usecase3.png)

1. Erstellen Sie eine Vorschau und publizieren Sie das Ereignis (siehe [Vorschau erstellen und Ereignis publizieren](#previewing-and-publishing-the-event)).
1. Integrieren Sie das Ereignis in Ihre Website (siehe [Aktivierung des Ereignisses in eine Website integrieren](#integrating-the-triggering-of-the-event-in-a-website)).


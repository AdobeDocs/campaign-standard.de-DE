---
solution: Campaign Standard
product: campaign
title: Push-Benachrichtigungen für Transaktionen
description: Hier erfahren Sie, wie Sie eine Transaktions-Push-Benachrichtigungen erstellen und publizieren.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
translation-type: tm+mt
source-git-commit: 9ad23468d3d1cf386d9558e6cd2344ea2316fc82
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 63%

---


# Push-Benachrichtigungen für Transaktionen{#transactional-push-notifications}

Sie können mit Adobe Campaign Transaktions-Push-Benachrichtigungen an iOS- und Android-Mobilgeräte versenden. Diese Nachrichten werden auf Mobile Apps empfangen, die in Adobe Campaign unter Verwendung des Experience Cloud Mobile SDK eingerichtet werden.

>[!NOTE]
>
>Der Push-Kanal ist optional. Prüfen Sie diesbezüglich Ihren Lizenzvertrag. Weitere Informationen zu Standard-Push-Benachrichtigungen finden Sie unter [Push-Benachrichtigungen](../../channels/using/about-push-notifications.md).

Für den Versand von Transaktions-Push-Benachrichtigungen müssen Sie Adobe Campaign entsprechend konfigurieren. Siehe [Mobilanwendung konfigurieren](../../administration/using/configuring-a-mobile-application.md).

Sie können zwei Arten von Transaktions-Push-Benachrichtigungen versenden:

* [Transaktions-Push-Benachrichtigungen, bei denen die Zielgruppenbestimmung durch ein Ereignis erfolgt](#transactional-push-notifications-targeting-an-event)
* [Transaktions-Push-Benachrichtigungen, bei denen die Zielgruppenbestimmung durch Profile in der Adobe-Campaign-Datenbank erfolgt](#transactional-push-notifications-targeting-a-profile)

>[!NOTE]
>
>Sie können nur dann auf Transaktionsnachrichten zugreifen, wenn Sie der Sicherheitsgruppe **[!UICONTROL Administratoren (alle Einheiten)]** angehören. Weitere Informationen finden Sie unter [Benutzerverwaltung](../../administration/using/users-management.md#functional-administrators).

## Transaktions-Push-Benachrichtigungen, bei denen die Zielgruppenbestimmung durch ein Ereignis erfolgt {#transactional-push-notifications-targeting-an-event}

Sie können Adobe Campaign verwenden, um **anonyme transaktionale Push-Benachrichtigungen an alle Benutzer zu senden, die sich für den Empfang von Benachrichtigungen von Ihrer Mobilanwendung entschieden haben.**

In diesem Fall werden nur **die im Ereignis selbst enthaltenen Daten verwendet, um die Zielgruppe des Versands** zu definieren. Daten aus der integrierten Profildatenbank von Adobe Campaign werden nicht genutzt.

### Konfigurieren einer Ereignis-basierten transaktionalen Push-Benachrichtigung {#configuring-event-based-transactional-push-notification}

Um eine transaktionale Push-Benachrichtigung an alle Benutzer zu senden, die sich für den Empfang von Benachrichtigungen von Ihrer Mobilanwendung entschieden haben, müssen Sie zunächst ein Ereignis erstellen und konfigurieren, das auf die im Ereignis enthaltenen Daten abzielt.

>[!NOTE]
>
>Sie können den Inhalt einer Ereignis-basierten transaktionalen Push-Benachrichtigung weiterhin mit [Ereignis-Attributen](../../channels/using/configuring-transactional-event.md#defining-the-event-attributes) (Daten aus dem Ereignis) und [Ereignis-Anreicherung](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content) (Daten aus der Kampagne) personalisieren. Siehe [das Beispiel unten](#sending-event-based-transactional-push-notification).

Das Ereignis muss diese drei Elemente enthalten:

* Einen **Anmeldetoken** als Nutzerkennung für eine Mobile App und ein Gerät. Möglicherweise entspricht es keinem Profil in der Adobe-Campaign-Datenbank.
* Einen **Mobile-App-Namen** (einen für alle Geräte – Android und iOS). Dies ist die Kennung der in Adobe Campaign konfigurierten Mobile App, die für den Empfang von Push-Benachrichtigungen auf den Geräten des Benutzers verwendet wird. Weitere Informationen finden Sie unter [Mobilanwendung konfigurieren](../../administration/using/configuring-a-mobile-application.md).
* Eine **Push-Plattform** (&quot;gcm&quot; für Android oder &quot;apns&quot; für iOS).

Gehen Sie wie folgt vor, um das Ereignis zu konfigurieren:

1. Wählen Sie bei der Erstellung der Ereigniskonfiguration den Kanal **[!UICONTROL Mobile App]** und die Zielgruppendimension **[!UICONTROL Echtzeit-Ereignis]** (siehe [Ereignis erstellen](../../channels/using/configuring-transactional-event.md#creating-an-event)).
1. hinzufügen Felder im Ereignis. Auf diese Weise können Sie die Transaktionsnachricht personalisieren (siehe [Definieren der Ereignis-Attribute](../../channels/using/configuring-transactional-event.md#defining-the-event-attributes)). Definieren Sie in diesem Beispiel die Felder &quot;gateNumber&quot;, &quot;lastname&quot;und &quot;firstname&quot;.
1. Richten Sie den Inhalt der Transaktionsnachricht ein, wenn Sie zusätzliche Informationen aus der Adobe Campaign-Datenbank verwenden möchten (siehe [Anreichern des Ereignisses](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content)).

   >[!NOTE]
   >
   >Beim ereignisbasierten Transaktionsnachrichtenversand sollen ausschließlich die Daten verwendet werden, die im gesendeten Ereignis der Personalisierung von Empfängern und Nachrichteninhalten dienen. Der Inhalt Ihrer Transaktionsnachricht lässt sich jedoch durch die Verwendung von in der Adobe-Campaign-Datenbank enthaltenen Informationen anreichern.

1. [Vorschau und Veröffentlichung des Ereignisses](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event).

   Bei der Vorschau des Ereignisses enthält die REST-API die Attribute &quot;registrationToken&quot;, &quot;application&quot; und &quot;pushPlatform&quot;, die für die Zielgruppenbestimmung des Versands verwendet werden.

   ![](assets/message-center_push_api.png)

   Mit Ausführung der Publikation wird automatisch eine dem neuen Ereignis entsprechende Transaktions-Push-Benachrichtigung erzeugt. Sie können jetzt die soeben erstellte Meldung ändern und veröffentlichen (siehe [diesen Abschnitt](#sending-event-based-transactional-push-notification)).

1. Integrieren Sie das Ereignis in Ihre Website (siehe Integrate Ereignis Trigging(../../channels/using/getting-started-with-transactional-msg.md#integrate-Ereignis-trigger)).

### Senden einer Ereignis-basierten transaktionalen Push-Benachrichtigung {#sending-event-based-transactional-push-notification}

Beispiel: Eine Fluglinie möchte ihre Mobile-App-Nutzer auffordern, sich zum Boarding zum entsprechenden Flugsteig zu begeben.

Das Unternehmen sendet eine einzige Transaktions-Push-Benachrichtigung pro Benutzer (durch einen Anmeldetoken registriert) mit einer einzigen Mobile App über ein einziges Gerät.

1. Rufen Sie die erstellte Transaktionsnachricht auf, um sie zu bearbeiten. Siehe [Zugriff auf Transaktionsnachrichten](../../channels/using/editing-transactional-message.md#accessing-transactional-messages).

   ![](assets/message-center_push_message.png)

1. Öffnen Sie nun mithilfe der gleichnamigen Kachel den **[!UICONTROL Inhalt]** der Nachricht, um den Titel und den Hauptteil anzupassen.

1. Sie können Personalisierungsfelder einfügen, um Elemente hinzuzufügen, die Sie beim Erstellen Ihres Ereignisses definiert haben (siehe [Definieren der Ereignis-Attribute](../../channels/using/configuring-transactional-event.md#defining-the-event-attributes)).

   ![](assets/message-center_push_content.png)

   Wählen Sie dazu das Stiftsymbol neben einem Objekt und **[!UICONTROL Personalisierungsfeld einfügen]** aus und danach **[!UICONTROL Kontext]** > **[!UICONTROL Echtzeit-Ereignis]** > **[!UICONTROL Ereigniskontext]**.

   ![](assets/message-center_push_personalization.png)

   Weitere Informationen zum Bearbeiten von Inhalten für Push-Benachrichtigungen finden Sie unter [Vorbereiten und Senden einer Push-Benachrichtigung](../../channels/using/preparing-and-sending-a-push-notification.md).

1. Sie können den Inhalt der Transaktionsnachricht auch anreichern, wenn Sie zusätzliche Informationen aus der Adobe Campaign-Datenbank verwenden möchten (siehe [Anreichern des Ereignisses](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content)).

1. Speichern Sie Ihre Änderungen und publizieren Sie die Nachricht. Siehe [Transaktionsnachricht publizieren](../../channels/using/publishing-transactional-message.md#publishing-a-transactional-message).

1. Senden Sie unter Verwendung einer Mobile App (WeFlight) unter Android (gcm) mithilfe der Adobe-Campaign-Standard-REST-API an einen Anmeldetoken (ABCDEF123456789) ein Ereignis, das die Boarding-Daten enthält:

   ```
   {
     "registrationToken":"ABCDEF123456789",
     "application":"WeFlight",
     "pushPlatform":"gcm",
     "ctx":
     {
       "gateNumber":"Gate B18",
       "lastname":"Green",
       "firstname":"Jane"
     }
   }
   ```

   Weitere Informationen zum Integrieren der Auslösung eines Ereignisses in ein externes System finden Sie unter Integrate Ereignis Trigging(../../channels/using/getting-started-with-transactional-msg.md#integrate-Ereignis-trigger).

Wenn der Anmeldetoken existiert, erhält der entsprechende Benutzer eine Transaktions-Push-Benachrichtigung mit folgendem Inhalt:

*&quot;Hallo, Jane Green, das Boarding hat soeben begonnen! Bitte gehen Sie zu Flugsteig B18.&quot;*

## Transaktions-Push-Benachrichtigung, bei der die Zielgruppenbestimmung durch ein Profil erfolgt    {#transactional-push-notifications-targeting-a-profile}

Sie können eine transaktionale Push-Benachrichtigung **an die Adobe Campaign-Profil senden, die Ihre Mobilanwendung abonniert haben**. Dieser Versand kann [Personalisierungsfelder](../../designing/using/personalization.md#inserting-a-personalization-field) enthalten, z. B. den Vornamen des Empfängers, der direkt aus der Adobe Campaign-Datenbank abgerufen wird.

In diesem Fall muss das Ereignis einige Felder **enthalten, die eine Absöhnung mit einem Profil aus der Adobe Campaign-Datenbank** ermöglichen.

Bei der Zielgruppenbestimmung durch Profile wird pro Mobile App und Gerät eine einzige Transaktions-Push-Benachrichtigung versendet. Wenn sich beispielsweise ein Adobe-Campaign-Benutzer für zwei Anwendungen angemeldet hat, erhält er zwei Benachrichtigungen. Wenn sich ein Benutzer für dieselbe Anwendung mit zwei unterschiedlichen Geräten angemeldet hat, erhält er auf jedes Gerät eine Benachrichtigung.

Die Mobile Apps, für die sich ein Profil angemeldet hat, werden auf der Registerkarte **[!UICONTROL Mobile-App-Abonnements]** dieses Profils aufgelistet. Um diese Registerkarte zu öffnen, wählen Sie ein Profil und danach rechts die Schaltfläche **[!UICONTROL Profileigenschaften bearbeiten]** aus.

![](assets/push_notif_subscriptions.png)

Weitere Informationen zum Zugriff auf und Bearbeiten von Profilen finden Sie unter [Profil](../../audiences/using/about-profiles.md).

### Konfigurieren einer Profil-basierten transaktionalen Push-Benachrichtigung {#configuring-profile-based-transactional-push-notification}

Um eine Transaktions-Push-Benachrichtigung an die Adobe-Campaign-Profile zu senden, die sich für Ihre Mobile App angemeldet haben, müssen Sie zunächst ein Ereignis erstellen und konfigurieren, bei dem die in der Adobe-Campaign-Datenbank enthaltenen Daten zur Zielgruppenbestimmung verwendet werden.

1. Wählen Sie bei der Erstellung der Ereigniskonfiguration den Kanal **[!UICONTROL Mobile App]** und die Zielgruppendimension **[!UICONTROL Profil]** (siehe [Ereignis erstellen](../../channels/using/configuring-transactional-event.md#creating-an-event)).

   Standardmäßig wird die Transaktions-Push-Benachrichtigung an alle Mobile Apps gesendet, für die sich der Empfänger angemeldet hat. Um die Push-Benachrichtigung an eine bestimmte Mobile App zu senden, wählen Sie sie in der Liste aus. Die anderen Mobile Apps werden zwar bei der Zielgruppenbestimmung der Nachricht berücksichtigt, aber vom Versand ausgeschlossen.

   ![](assets/message-center_push_appfilter.png)

1. Fügen Sie zum Ereignis Felder hinzu, wenn Sie die Transaktionsnachricht personalisieren möchten (siehe [Ereignisattribute definieren](../../channels/using/configuring-transactional-event.md#defining-the-event-attributes)).

   >[!NOTE]
   >
   >Für eine Anreicherung müssen Sie mindestens ein Feld hinzufügen. Sie müssen keine anderen Felder wie **Vorname** und **Nachname** erstellen, da Sie Personalisierungsfelder aus der Adobe-Campaign-Datenbank verwenden können.

1. Erstellen Sie eine Anreicherung, um das Ereignis mit der Ressource **[!UICONTROL Profil]** zu verknüpfen (siehe [Anreichern des Ereignisses](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content)). Wenn die Zielgruppendimension **[!UICONTROL Profil]** verwendet wird, ist die Erstellung einer Anreicherung zwingend erforderlich.
1. [Vorschau und Veröffentlichung des Ereignisses](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event).

   Bei der Vorschau des Ereignisses enthält die REST-API kein Attribut, das das Anmeldetoken, den App-Namen und die Push-Plattform spezifiziert, da diese Informationen aus der Ressource **[!UICONTROL Profil]** entnommen werden.

   Mit Ausführung der Publikation wird automatisch eine dem neuen Ereignis entsprechende Transaktions-Push-Benachrichtigung erzeugt. Sie können jetzt die soeben erstellte Meldung ändern und veröffentlichen (siehe [diesen Abschnitt](#sending-profile-based-transactional-push-notification)).

1. Integrieren Sie das Ereignis in Ihre Website (siehe Integrate Ereignis Trigging(../../channels/using/getting-started-with-transactional-msg.md#integrate-Ereignis-trigger)).

### Senden einer Profil-basierten transaktionalen Push-Benachrichtigung {#sending-profile-based-transactional-push-notification}

Beispiel: Eine Fluglinie möchte allen Adobe-Campaign-Benutzern, die sich für ihre Mobile App angemeldet haben, eine letzte Aufforderung zum Boarding senden.

1. Rufen Sie die erstellte Transaktionsnachricht auf, um sie zu bearbeiten. Siehe [Zugriff auf Transaktionsnachrichten](../../channels/using/editing-transactional-message.md#accessing-transactional-messages).

1. Öffnen Sie nun mithilfe der gleichnamigen Kachel den **[!UICONTROL Inhalt]** der Nachricht, um den Titel und den Hauptteil anzupassen.

   Im Gegensatz zu auf Echtzeit-Ereignissen basierenden Konfigurationen haben Sie direkten Zugriff auf alle Profilinformationen, um die Nachricht zu personalisieren. Siehe [Personalisierungsfelder einfügen](../../designing/using/personalization.md#inserting-a-personalization-field).

   Weitere Informationen zum Bearbeiten von Inhalten für Push-Benachrichtigungen finden Sie unter [Vorbereiten und Senden einer Push-Benachrichtigung](../../channels/using/preparing-and-sending-a-push-notification.md).

1. Speichern Sie Ihre Änderungen und publizieren Sie die Nachricht. Siehe [Transaktionsnachricht publizieren](../../channels/using/publishing-transactional-message.md#publishing-a-transactional-message).
1. Senden Sie unter Verwendung der Adobe-Campaign-Standard-REST-API ein Ereignis an ein Profil:

   ```
   {
     "ctx":
     {
       "email":"janegreen@email.com",
       "gateNumber":"D16",
     }
   }
   ```

Weitere Informationen zum Integrieren der Auslösung eines Ereignisses in ein externes System finden Sie unter Integrate Ereignis Trigging(../../channels/using/getting-started-with-transactional-msg.md#integrate-Ereignis-trigger).

Der entsprechende Benutzer erhält eine transaktionale Push-Benachrichtigung einschließlich aller Personalisierungselemente, die aus der Adobe Campaign-Datenbank abgerufen werden.

>[!NOTE]
>
>Es gibt keine Felder für Anmeldetoken, Anwendung und Push-Plattform. In diesem Beispiel erfolgt die Abstimmung über das E-Mail-Feld.

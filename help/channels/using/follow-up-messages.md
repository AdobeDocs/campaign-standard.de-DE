---
solution: Campaign Standard
product: campaign
title: Folgenachrichten
description: Hier erfahren Sie, wie Sie eine Folgenachricht erstellen und publizieren.
audience: channels
content-type: reference
topic-tags: transactional-messaging
translation-type: tm+mt
source-git-commit: fc755f3176622e1faf08ccfa4236e016110f9a68
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 74%

---


# Folgenachrichten {#follow-up-messages}

Eine Follow-up-Meldung ist eine vordefinierte Marketing-Versandvorlage, die in einem Workflow verwendet werden kann, um eine andere Kommunikation an die Empfänger einer bestimmten Transaktionsnachricht zu senden.

Greifen wir hierfür das im Abschnitt [Funktionsweise von Transaktionsnachrichten](../../channels/using/getting-started-with-transactional-msg.md#transactional-messaging-operating-principle) beschriebene Beispiel wieder auf: eine E-Mail-Benachrichtigung, die an Besucher Ihrer Webseite gesendet wird, die Artikel in ihrem Warenkorb hinzugefügt, aber die Webseite verlassen haben, ohne den Kauf abzuschließen.

Sie möchten eine freundliche Erinnerung an alle Kunden senden, die die Benachrichtigung zum Warenkorbabbruch erhalten haben, diese aber nach drei Tagen nicht geöffnet haben. Sie erhalten eine Anschlussnachricht, die auf denselben Daten basiert, die in der ersten gesendeten E-Mail verwendet wurden.

## Ereignis konfigurieren, um eine Folgenachricht zu senden        {#configuring-an-event-to-send-a-follow-up-message}

Um eine Folgemaßnahme zu senden, müssen Sie zunächst das Ereignis entsprechend der bereits erhaltenen Transaktionsnachricht konfigurieren.

1. Verwenden Sie dieselbe Ereigniskonfiguration wie für den Versand einer Ereignis-Transaktionsnachricht. Siehe [Konfigurieren eines transaktionalen Ereignisses](../../channels/using/configuring-transactional-event.md).
1. Aktivieren Sie bei der Konfiguration Ihres Ereignisses und vor seiner Publikation die Option **[!UICONTROL Folgenachrichten-Vorlage für dieses Ereignis erstellen]**.

   ![](assets/message-center_follow-up-checkbox.png)

1. [Vorschau und Veröffentlichung des Ereignisses](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event).

Mit Ausführung der Publikation werden automatisch eine dem neuen Ereignis entsprechende Transaktionsnachricht und eine Folgenachricht aus einer Versandvorlage erzeugt. Die Schritte zum Senden der Follow-up-Meldung sind in [diesem Abschnitt](#sending-a-follow-up-message) beschrieben.

## Zugriff auf die Folgenachrichten      {#accessing-the-follow-up-messages}

Zur Verwaltung eines Ereignisses innerhalb eines Workflows ist eine Versandvorlage notwendig. Allerdings kann die bei der Publikation des Ereignisses erstellte [Transaktionsnachricht](../../channels/using/editing-transactional-message.md) nicht als Vorlage verwendet werden. Hierfür müssen Sie eine spezifische Versandvorlage für Folgenachrichten erstellen, die diesen Ereignistyp und die Verwendung als Vorlage in Workflows unterstützt.

So greifen Sie auf diese Vorlage zu:

1. Wählen Sie oben links das **[!UICONTROL Adobe Campaign]**-Logo aus.
1. Wählen Sie dann **[!UICONTROL Ressourcen]** > **[!UICONTROL Vorlagen]** > **[!UICONTROL Versandvorlagen]**.
1. Aktivieren Sie im linken Bereich die Option **[!UICONTROL Folgenachrichten]**.

   ![](assets/message-center_follow-up-search.png)

Nur die Folgenachrichten werden angezeigt.

>[!NOTE]
>
>Sie können nur dann auf Transaktionsnachrichten zugreifen, wenn Sie der Sicherheitsgruppe **[!UICONTROL Administratoren (alle Einheiten)]** angehören.

## Folgenachrichten senden {#sending-a-follow-up-message}

Nachdem Sie die Folgenachrichten-Versandvorlage erstellt haben, können Sie sie in einem Workflow zum Versenden einer Folgenachricht verwenden.

(Sie müssen einen Arbeitsablauf einrichten, der auf das Ereignis ausgerichtet ist, das der bereits empfangenen Transaktionsnachricht entspricht.)

1. Gehen Sie in die Liste der Marketingaktivitäten und erstellen Sie einen neuen Workflow.

   Siehe [Erstellen eines Workflows](../../automating/using/building-a-workflow.md#creating-a-workflow).

1. Ziehen Sie eine **[!UICONTROL Planung]** in den Workflow und öffnen Sie sie. Wählen Sie für die Ausführungshäufigkeit einmal pro Tag aus.

   Weiterführende Informationen zur Aktivität &quot;Planung&quot; finden Sie im Abschnitt [Planung](../../automating/using/scheduler.md).

1. Ziehen Sie eine **[!UICONTROL Abfrage]** in den Workflow-Arbeitsbereich und öffnen Sie sie.

   Weiterführende Informationen zur Abfrage-Aktivität finden Sie im Abschnitt [Abfrage](../../automating/using/query.md).

1. Damit sich Ihre Abfrage auf eine andere als die Profil-Ressource bezieht, gehen Sie in den **[!UICONTROL Eigenschaften]**-Tab der Aktivität und wählen Sie die entsprechende **[!UICONTROL Ressource]** aus der Dropdown-Liste aus.

   ![](assets/message-center_follow-up-query-properties.png)

   >[!NOTE]
   >
   >Die Standardkonfiguration der Aktivität sieht die Suche nach Profilen vor.

1. Wählen Sie das Ereignis aus, auf das Ihr Workflow abzielen soll, sodass Sie ausschließlich auf zu diesem Ereignis gehörende Daten zugreifen.

   ![](assets/message-center_follow-up-query-resource.png)

1. Wechseln Sie zur Registerkarte **[!UICONTROL Zielgruppe]** der Aktivität und ziehen Sie das Element **[!UICONTROL Versandlogs (Protokolle)]** aus der Palette in den Arbeitsbereich.

   ![](assets/message-center_follow-up-delivery-logs.png)

   Wählen Sie **[!UICONTROL Vorhanden]** aus, um alle Kunden, die die E-Mail erhalten haben, Zielgruppe.

   ![](assets/message-center_follow-up-delivery-logs-exists.png)

1. Verschieben Sie das Element **[!UICONTROL Trackinglogs (tracking)]** aus der Palette in den Arbeitsbereich und wählen Sie **[!UICONTROL Ist nicht vorhanden]**, um alle Kunden, die die E-Mail nicht geöffnet haben, Zielgruppe.

   ![](assets/message-center_follow-up-delivery-and-tracking-logs.png)

1. Ziehen Sie das Ereignis, für das Sie eine Zielgruppe bestimmen (in diesem Beispiel **Stehen gelassener Warenkorb**), von der Palette in den Arbeitsbereich. Definieren Sie dann eine Regel, um alle Nachrichten einzuschließen, die vor drei Tagen gesendet wurden.

   ![](assets/message-center_follow-up-created.png)

   Dadurch sind alle Empfänger in der Zielgruppe enthalten, die die Transaktionsnachricht drei Tage vor der Ausführung des Workflows erhalten und noch nicht geöffnet haben.

   Speichern Sie die Abfrage mithilfe der Schaltfläche **[!UICONTROL Bestätigen]**.

1. Ziehen Sie einen **E-Mail-Versand** in den Workflow-Arbeitsbereich.

   Weiterführende Informationen zu dieser Aktivität finden Sie im Abschnitt [E-Mail-Versand](../../automating/using/email-delivery.md).

   ![](assets/message-center_follow-up-workflow.png)

   Sie können auch einen [SMS-Versand](../../automating/using/sms-delivery.md) oder einen [Push-Benachrichtigungs-Versand](../../automating/using/push-notification-delivery.md)-Aktivität verwenden. Stellen Sie in diesem Fall sicher, dass Sie, während Sie Ihre Ereigniskonfiguration vornehmen, den Kanal **[!UICONTROL Mobiltelefon (SMS)]** oder **[!UICONTROL Mobile App]** auswählen. Siehe [Ereignis erstellen](../../channels/using/configuring-transactional-event.md#creating-an-event).

1. Öffnen Sie die Aktivität **E-Mail-Versand.** Aktivieren Sie im Erstellungsassistenten die Option **[!UICONTROL Folgenachrichten]** und wählen Sie die Folgenachrichten-Versandvorlage aus, die nach dem Publizieren des Ereignisses erstellt wurde.

   ![](assets/message-center_follow-up-template.png)

1. Sie können den Inhalt Ihres Ereignisses im Inhalt der Folgenachricht übernehmen, indem Sie Personalisierungsfelder hinzufügen.

   ![](assets/message-center_follow-up-content.png)

1. Die von Ihnen bei der Erstellung des Ereignisses definierten Felder finden Sie durch die Auswahl von **[!UICONTROL Kontext]** > **[!UICONTROL Echtzeit-Ereignis]** > **[!UICONTROL Ereigniskontext]**. Siehe [Transaktionsnachricht personalisieren](../../channels/using/editing-transactional-message.md#personalizing-a-transactional-message).

   ![](assets/message-center_follow-up-personalization.png)

   Das bedeutet, dass Sie denselben Inhalt, der beim ersten Versand des Ereignisses benutzt wurde, einschließlich angereicherter Daten für die Erstellung einer höflichen personalisierten Erinnerung verwenden können.

1. Speichern Sie die Aktivität und starten Sie den Workflow.

Nach dem Start des Workflows erhalten alle Kunden, die drei Tage zuvor Ihre Benachrichtigung über den stehen gelassenen Warenkorb empfangen, aber nicht geöffnet haben, eine auf denselben Daten basierende Folgenachricht.

>[!NOTE]
>
>Wenn Sie die Zielgruppendimension **[!UICONTROL Profil]** bei der Erstellung der Ereigniskonfiguration ausgewählt haben, nutzt die Folgenachricht zudem die Marketing-Datenbank von Adobe Campaign. Siehe [Profil-Transaktionsnachrichten](../../channels/using/editing-transactional-message.md#profile-transactional-message-specificities).

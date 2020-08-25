---
title: Folgenachrichten
description: Hier erfahren Sie, wie Sie eine Folgenachricht erstellen und publizieren.
page-status-flag: never-activated
uuid: d2a17da2-e935-420a-8531-78ed6a1fe68b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: transactional-messaging
discoiquuid: 9615e369-754f-4f6a-a1b1-14462f946666
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1efcd646f4af86175b3b09b53185c792cb4cf7dd
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 100%

---


# Folgenachrichten{#follow-up-messages}

Sie haben die Möglichkeit, Folgenachrichten an Kunden zu senden, die zuvor eine spezifische Transaktionsnachricht erhalten haben. Hierzu müssen Sie einen auf das entsprechende Ereignis abzielenden Workflow erstellen.

Greifen wir hierfür das im Abschnitt [Funktionsweise von Transaktionsnachrichten](../../channels/using/getting-started-with-transactional-msg.md#transactional-messaging-operating-principle) beschriebene Beispiel wieder auf: eine E-Mail-Benachrichtigung, die an Besucher Ihrer Webseite gesendet wird, die Artikel in ihrem Warenkorb hinzugefügt, aber die Webseite verlassen haben, ohne den Kauf abzuschließen.

Sie möchten eine höfliche Erinnerung an alle Kunden senden, die vor drei Tagen die Benachrichtigung über einen stehen gelassenen Warenkorb erhalten, aber nicht geöffnet haben.

Jeder betroffene Kunde erhält eine Folgenachricht, die auf den gleichen Daten basiert, die schon in der ersten gesendeten E-Mail verwendet wurden.

## Zugriff auf die Folgenachrichten  {#accessing-the-follow-up-messages}

Nach der Erstellung und Publikation des gewünschten Ereignisses (im vorliegenden [Beispiel](../../channels/using/getting-started-with-transactional-msg.md#transactional-messaging-operating-principle) &quot;Stehen gelassener Warenkorb&quot;) werden die entsprechende Transaktionsnachricht und Folgenachricht automatisch erstellt.

Die Konfigurationsschritte finden Sie im Abschnitt [Ereignis konfigurieren, um eine Profil-Transaktionsnachricht zu senden](../../administration/using/configuring-transactional-messaging.md#configuring-an-event-to-send-a-follow-up-message).

Zur Verwaltung eines Ereignisses innerhalb eines Workflows ist eine Versandvorlage notwendig. Allerdings kann die bei der Publikation des Ereignisses erstellte [Transaktionsnachricht](../../channels/using/event-transactional-messages.md) nicht als Vorlage verwendet werden. Hierfür müssen Sie eine spezifische Versandvorlage für Folgenachrichten erstellen, die diesen Ereignistyp und die Verwendung als Vorlage in Workflows unterstützt.

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

1. Gehen Sie in die Liste der Marketingaktivitäten und erstellen Sie einen neuen Workflow.

   Lesen Sie diesbezüglich auch den Abschnitt [Workflows erstellen](../../automating/using/building-a-workflow.md#creating-a-workflow).

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

1. Navigieren Sie zum Tab **[!UICONTROL Zielgruppe]** der Aktivität und ziehen Sie das Element **[!UICONTROL Versandlogs (logs)]** aus der Palette in den Arbeitsbereich.

   ![](assets/message-center_follow-up-delivery-logs.png)

   Wählen Sie **[!UICONTROL Existiert]** aus, um alle Kunden in Ihre Zielgruppe miteinzubeziehen, die die E-Mail erhalten haben.

   ![](assets/message-center_follow-up-delivery-logs-exists.png)

1. Ziehen Sie das Element **[!UICONTROL Trackinglogs (Tracking)]** aus der Palette in den Arbeitsbereich und wählen Sie **[!UICONTROL Existiert nicht]** aus, um alle Kunden in Ihre Zielgruppe miteinzubeziehen, die die E-Mail nicht geöffnet haben.

   ![](assets/message-center_follow-up-delivery-and-tracking-logs.png)

1. Ziehen Sie das Ereignis, für das Sie eine Zielgruppe bestimmen (in diesem Beispiel **Stehen gelassener Warenkorb**), von der Palette in den Arbeitsbereich. Definieren Sie dann eine Regel, um alle Nachrichten einzuschließen, die vor drei Tagen gesendet wurden.

   ![](assets/message-center_follow-up-created.png)

   Dadurch sind alle Empfänger in der Zielgruppe enthalten, die die Transaktionsnachricht drei Tage vor der Ausführung des Workflows erhalten und noch nicht geöffnet haben.

   Speichern Sie die Abfrage mithilfe der Schaltfläche **[!UICONTROL Bestätigen]**.

1. Ziehen Sie einen **E-Mail-Versand** in den Workflow-Arbeitsbereich.

   Weiterführende Informationen zu dieser Aktivität finden Sie im Abschnitt [E-Mail-Versand](../../automating/using/email-delivery.md).

   ![](assets/message-center_follow-up-workflow.png)

   Sie können alternativ auch einen [SMS-Versand](../../automating/using/sms-delivery.md) oder die Aktivität [Mobile-App-Versand](../../automating/using/push-notification-delivery.md) verwenden. Stellen Sie in diesem Fall sicher, dass Sie, während Sie Ihre Ereigniskonfiguration vornehmen, den Kanal **[!UICONTROL Mobiltelefon (SMS)]** oder **[!UICONTROL Mobile App]** auswählen. Siehe [Ereignis erstellen](../../administration/using/configuring-transactional-messaging.md#creating-an-event).

1. Öffnen Sie die Aktivität **E-Mail-Versand.** Aktivieren Sie im Erstellungsassistenten die Option **[!UICONTROL Folgenachrichten]** und wählen Sie die Folgenachrichten-Versandvorlage aus, die nach dem Publizieren des Ereignisses erstellt wurde.

   ![](assets/message-center_follow-up-template.png)

1. Sie können den Inhalt Ihres Ereignisses im Inhalt der Folgenachricht übernehmen, indem Sie Personalisierungsfelder hinzufügen.

   ![](assets/message-center_follow-up-content.png)

1. Die von Ihnen bei der Erstellung des Ereignisses definierten Felder finden Sie durch die Auswahl von **[!UICONTROL Kontext]** > **[!UICONTROL Echtzeit-Ereignis]** > **[!UICONTROL Ereigniskontext]**. Siehe [Transaktionsnachricht personalisieren](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message).

   ![](assets/message-center_follow-up-personalization.png)

   Das bedeutet, dass Sie denselben Inhalt, der beim ersten Versand des Ereignisses benutzt wurde, einschließlich angereicherter Daten für die Erstellung einer höflichen personalisierten Erinnerung verwenden können.

1. Speichern Sie die Aktivität und starten Sie den Workflow.

Nach dem Start des Workflows erhalten alle Kunden, die drei Tage zuvor Ihre Benachrichtigung über den stehen gelassenen Warenkorb empfangen, aber nicht geöffnet haben, eine auf denselben Daten basierende Folgenachricht.

>[!NOTE]
>
>Wenn Sie die Zielgruppendimension **[!UICONTROL Profil]** bei der Erstellung der Ereigniskonfiguration ausgewählt haben, nutzt die Folgenachricht zudem die Marketing-Datenbank von Adobe Campaign. Siehe [Profil-Transaktionsnachrichten](../../channels/using/profile-transactional-messages.md).


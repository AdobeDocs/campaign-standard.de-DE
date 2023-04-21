---
title: Transaktionsereignis veröffentlichen
description: Erfahren Sie, wie Sie die Konfiguration von Transaktionsereignissen in der Vorschau anzeigen, veröffentlichen, deren Veröffentlichung aufheben und sie löschen.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
feature: Transactional Messaging
role: User
level: Intermediate
exl-id: 6bcd8dcd-d710-4ca3-937d-bf4339f36069
source-git-commit: ee7539914aba9df9e7d46144e437c477a7e52168
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 100%

---

# Transaktionsereignis veröffentlichen {#publishing-transactional-event}

Sobald die [Konfiguration](../../channels/using/configuring-transactional-event.md) abgeschlossen ist, kann das Ereignis veröffentlicht werden. Die Schritte zum Erstellen einer Vorschau, zum Veröffentlichen, zum Aufheben der Veröffentlichung und zum Löschen eines Ereignisses werden nachfolgend beschrieben.

>[!IMPORTANT]
>
>Nur [Funktionale Administratoren](../../administration/using/users-management.md#functional-administrators) <!--being part of the **[!UICONTROL All]** [organizational unit](../../administration/using/organizational-units.md) -->haben die entsprechenden Berechtigungen zum Veröffentlichen von Ereigniskonfigurationen.

Eine Grafik, die den gesamten Veröffentlichungsprozess für Transaktionsnachrichten veranschaulicht, einschließlich der Konfigurationen für die Veröffentlichung von Ereignissen und deren Aufhebung, finden Sie in [diesem Abschnitt](../../channels/using/publishing-transactional-message.md).

Nach der Veröffentlichung:
* Die entsprechende Transaktionsnachricht wird automatisch erstellt. Siehe [Transaktionsnachrichten bearbeiten](../../channels/using/editing-transactional-message.md).
* Die von Ihrem Website-Entwickler verwendete API wird bereitgestellt und die Transaktionsereignisse können jetzt gesendet werden. Siehe [Ereignis-Aktivierung integrieren](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger).

## Vorschau erstellen und Ereignis veröffentlichen {#previewing-and-publishing-the-event}

Bevor Sie das Ereignis verwenden können, müssen Sie eine Vorschau erstellen und es veröffentlichen.

1. Verwenden Sie die Schaltfläche **[!UICONTROL API-Vorschau]**, um eine Simulation der von Ihrem Web-Entwickler verwendeten REST-API anzuzeigen, bevor sie veröffentlicht wird.

   Nach der Veröffentlichung des Ereignisses dient diese Schaltfläche auch dazu, eine Vorschau der in Produktion befindlichen API anzuzeigen. Siehe [Ereignis-Aktivierung integrieren](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger).

   ![](assets/message-center_api_preview.png)

   >[!NOTE]
   >
   >Die REST-API variiert je nach ausgewähltem Kanal und nach ausgewählter Zielgruppendimension. Weitere Informationen zu den verschiedenen Konfigurationen finden Sie in [diesem Abschnitt](../../channels/using/configuring-transactional-event.md#transactional-event-specific-configurations).

1. Starten Sie mit der Schaltfläche **[!UICONTROL Veröffentlichen]** die Veröffentlichung.

   ![](assets/message-center_pub.png)

   Die von Ihrem Website-Entwickler verwendete API wird bereitgestellt und die Transaktionsereignisse können jetzt gesendet werden.

1. Die Veröffentlichungslogs lassen sich mithilfe des gleichnamigen Tabs einsehen.

   ![](assets/message-center_logs.png)

   >[!IMPORTANT]
   >
   >Jedes Mal, wenn Sie ein Ereignis ändern, müssen Sie anschließend die Schaltfläche **[!UICONTROL Veröffentlichen]** verwenden, um die von Ihrem Web-Entwickler verwendete REST-API zu aktualisieren.

   Mit Ausführung der Veröffentlichung wird automatisch eine dem neuen Ereignis entsprechende [Transaktionsnachricht](../../channels/using/editing-transactional-message.md) erzeugt.

1. Sie können direkt über den Link auf der linken Seite auf diese Transaktionsnachricht zugreifen.

   ![](assets/message-center_messagegeneration.png)

   >[!NOTE]
   >
   >Damit das Ereignis den Versand der Transaktionsnachricht auslösen kann, muss die Transaktionsnachricht angepasst und veröffentlicht werden. Siehe die Abschnitte [Bearbeiten](../../channels/using/editing-transactional-message.md) und [Transaktionsnachrichten veröffentlichen](../../channels/using/publishing-transactional-message.md). Außerdem müssen Sie [dieses Aktivierungsereignis in Ihre Website integrieren](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger).

1. Sobald Adobe Campaign erste Ereignisse im Zusammenhang mit dieser Ereigniskonfiguration erhält, können Sie über den Link **[!UICONTROL Letzte Transaktionsereignisse]** im Abschnitt **[!UICONTROL Verlauf]** auf die neuesten Ereignisse zugreifen, die von Ihrem Drittanbieterdienst gesendet und von Adobe Campaign verarbeitet wurden.

![](assets/message-center_latest-events.png)

Die Ereignisse (im JSON-Format) werden von den jüngsten hin zu den ältesten aufgelistet. Mit dieser Liste können Sie Daten wie den Inhalt oder Status eines Ereignisses zu Kontroll- und Debugging-Zwecken überprüfen.

## Veröffentlichung eines Ereignisses aufheben   {#unpublishing-an-event}

Mithilfe der **[!UICONTROL Veröffentlichung aufheben]**-Schaltfläche lässt sich die Veröffentlichung des Ereignisses abbrechen, wodurch auch die Ressource aus der REST-API gelöscht wird, die dem zuvor von Ihnen erstellten Ereignis entspricht.

Selbst wenn das Ereignis auf Ihrer Webseite ausgelöst wird, werden die entsprechenden Nachrichten nun nicht mehr gesendet und auch nicht in der Datenbank gespeichert.

![](assets/message-center_unpublish.png)

>[!NOTE]
>
>Sollten Sie die entsprechende Transaktionsnachricht bereits veröffentlicht haben, wird die Transaktionsnachrichtenveröffentlichung ebenfalls abgebrochen. Siehe [Veröffentlichung der Transaktionsnachricht aufheben](../../channels/using/publishing-transactional-message.md#unpublishing-a-transactional-message).

Verwenden Sie die Schaltfläche **[!UICONTROL Veröffentlichen]**, um die neue REST-API zu erzeugen.

<!--## Transactional messaging publication process {#transactional-messaging-pub-process}

The chart below illustrates the transactional messaging publication process.

![](assets/message-center_pub-process.png)

For more on publishing, pausing and unpublishing a transactional message, see [this section](../../channels/using/publishing-transactional-message.md).-->

## Löschen eines Ereignisses {#deleting-an-event}

Wenn die Veröffentlichung eines Ereignisses aufgehoben oder es noch nicht veröffentlicht wurde, können Sie es aus der Ereigniskonfigurationsliste löschen. Gehen Sie dazu wie folgt vor:

1. Klicken Sie auf das  **Adobe**-Logo oben links im Bildschirm und anschließend auf **[!UICONTROL Marketing-Pläne]** > **[!UICONTROL Transaktionsnachrichten]** > **[!UICONTROL Ereigniskonfiguration]**.
1. Bewegen Sie den Mauszeiger über die gewünschte Ereigniskonfiguration und wählen Sie die Schaltfläche **[!UICONTROL Element löschen]**.

   ![](assets/message-center_delete-button.png)

   >[!NOTE]
   >
   >Vergewissern Sie sich, dass die Ereigniskonfiguration den Status **[!UICONTROL Entwurf]** aufweist; andernfalls können Sie sie nicht löschen. Der Status **[!UICONTROL Entwurf]** gilt für ein Ereignis, das noch nicht veröffentlicht bzw. dessen [Veröffentlichung aufgehoben](#unpublishing-an-event) wurde.

1. Wählen Sie die Schaltfläche **[!UICONTROL Bestätigen]**.

   ![](assets/message-center_delete-confirm.png)

>[!IMPORTANT]
>
>Wenn Sie eine bereits veröffentlichte und in Verwendung befindliche Ereigniskonfiguration löschen, werden auch die entsprechenden Transaktionsnachrichten sowie deren Versand- und Trackinglogs gelöscht.

---
title: Triggers in Campaign verwenden
description: null
page-status-flag: never-activated
uuid: d844d013-b38a-4e69-9df5-0edc01fa9c6e
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
discoiquuid: a524c700-bad6-4fcf-857a-c31bfae4d30c
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: dddd147d01f935ec6f1513c5f92bddf6e789abb1
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 87%

---


# Triggers in Campaign verwenden{#using-triggers-in-campaign}

## In Campaign einen gemappten Trigger erstellen {#creating-a-mapped-trigger-in-campaign}

Stellen Sie sicher, dass die Verhaltensweisen, die Sie verfolgen möchten, im Vorhinein in Adobe Experience Cloud (**[!UICONTROL Triggers]** Core Service) definiert wurden. Weiterführende Informationen finden Sie in der [Dokumentation zur Adobe Experience Cloud](https://docs.adobe.com/content/help/de-DE/core-services/interface/activation/triggers.html). Beachten Sie, dass bei der Definition von Triggern die Alias aktiviert werden müssen. In Adobe Experience Cloud muss für jedes Verhalten (abgebrochener Webseitenbesuch/Formularabbruch, hinzugefügter/entfernter Artikel, abgelaufene Sitzung etc.) ein neuer Trigger hinzugefügt werden.

In Adobe Campaign ist nun ein auf einem bereits vorhandenen Trigger der Adobe Experience Cloud basierendes Trigger-Ereignis zu erstellen.

In diesem [Video](https://helpx.adobe.com/de/marketing-cloud/how-to/email-marketing.html#step-two) wird die Einrichtung von Triggern in Adobe Campaign beschrieben.

Gehen Sie hierzu wie folgt vor:

1. Verwenden Sie das **[!UICONTROL Adobe-Campaign]**-Logo oben links im Bildschirm und anschließend die Schaltflächen **[!UICONTROL Marketingpläne]** > **[!UICONTROL Transaktionsnachrichten]** > **[!UICONTROL Experience Cloud Triggers]**.

   ![](assets/remarketing_1.png)

1. Wählen Sie die **[!UICONTROL Erstellen]**-Schaltfläche aus. Im sich öffnenden Assistenten wird die Liste aller in Adobe Experience Cloud definierten Trigger angezeigt. In der Spalte **[!UICONTROL Anzahl an Übermittlungen von Analytics]** wird die Anzahl an Ereignissen angezeigt, die vom Trigger in Adobe Experience Cloud an Adobe Campaign gesendet wurden. Hierbei handelt es sich um ein Mapping der in der Experience Cloud-Benutzeroberfläche erstellten Trigger.

   ![](assets/remarketing_2.png)

1. Wählen Sie den Trigger in Adobe Experience Cloud aus, den Sie verwenden möchten, und danach **[!UICONTROL Weiter]**.
1. Konfigurieren Sie die allgemeinen Eigenschaften des Triggers. Geben Sie bei diesem Schritt des Assistenten auch den Kanal und die Zielgruppendimension an, die vom Trigger verwendet werden sollen (siehe [Zielgruppendimensionen und Ressourcen](../../automating/using/query.md#targeting-dimensions-and-resources)). Bestätigen Sie dann die Trigger-Erstellung.
1. Verwenden Sie die Schaltfläche rechts vom Feld **[!UICONTROL Ereignisinhalt und -anreicherung]**, um den Payload-Inhalt angezeigt zu bekommen. Innerhalb dieses Bildschirms können Sie außerdem die Ereignisdaten mittels in der Adobe-Campaign-Datenbank gespeicherten Profildaten anreichern. Die Anreicherung erfolgt auf die gleiche Weise wie bei Standard-Transaktionsnachrichten.

   ![](assets/remarketing_3.png)

1. Definieren Sie im Feld **[!UICONTROL Gültigkeitsdauer der Transaktionsnachricht]** die Dauer, für welche die Nachricht nach dem Versand des Ereignisses durch Analytics gültig sein soll. Bei einer definierten Dauer von 2 Tagen wird die Nachricht nach Ablauf dieses Zeitraums nicht länger gesendet. Dies stellt sicher, dass Nachrichten, deren Versand ausgesetzt wurde, nach Ablauf der festgesetzten Dauer nicht mehr gesendet werden, auch wenn der Versand wieder aufgenommen wird.

   ![](assets/remarketing_4.png)

1. Sie können Ihre Auslöser jetzt veröffentlichen. Weitere Informationen finden Sie unter [Veröffentlichen eines Auslösers in der Kampagne](../../integrating/using/using-triggers-in-campaign.md#publishing-trigger-in-campaign).

## Veröffentlichen eines Auslösers in der Kampagne {#publishing-trigger-in-campaign}

Nachdem Sie ein auslösendes Ereignis in Adobe Campaign erstellt haben, das auf einem vorhandenen Adobe Experience Cloud-Auslöser basiert, müssen Sie es jetzt veröffentlichen.

1. Klicken Sie von Ihrem zuvor erstellten Auslöser auf die Schaltfläche &quot; **[!UICONTROL Veröffentlichen]** &quot;, um das auslösende Ereignis vom Beginn zu veröffentlichen.

   ![](assets/trigger_publish_1.png)

1. Sie können den Fortschritt Ihrer auslösenden Veröffentlichung unter **[!UICONTROL Veröffentlichung]**&#x200B;überprüfen.

   ![](assets/trigger_publish_2.png)

1. Nach der Veröffentlichung wird unter &quot; **[!UICONTROL Veröffentlichung]**&quot;die folgende Meldung angezeigt.

   ![](assets/trigger_publish_3.png)

1. Wenn Sie nach dem Publizieren Ihres Trigger-Ereignisses das Trigger-Schema verändern müssen, wählen Sie die Schaltfläche **[!UICONTROL Schema aktualisieren]** aus, um die letzten Änderungen abzurufen.

   Bitte beachten Sie, dass durch diese Aktion Ihr Trigger und Ihre Transaktionsnachricht depubliziert werden und Sie diese danach wieder publizieren müssen.

   ![](assets/trigger_publish_4.png)

1. Click **[!UICONTROL Show Trigger in Experience Cloud]** button allows you to view the trigger definition in Adobe Experience Cloud.

Mit Ausführung der Publikation wird automatisch eine dem neuen Ereignis entsprechende Transaktionsvorlage erzeugt. Diese Vorlage muss nun bearbeitet und publiziert werden. Lesen Sie diesbezüglich auch den Abschnitt [Vorlagen bearbeiten](../../start/using/marketing-activity-templates.md).

## Transaktionsnachrichtenvorlage bearbeiten    {#editing-the-transactional-message-template}

Im Zuge der Erstellung und Publikation des Trigger-Ereignisses wird die entsprechende Transaktionsvorlage automatisch erstellt. Lesen Sie diesbezüglich auch den Abschnitt [In Campaign einen gemappten Trigger erstellen](#creating-a-mapped-trigger-in-campaign).

Damit das Ereignis mit dem Versand einer Transaktionsnachricht einhergeht, muss diese Vorlage personalisiert, getestet und dann publiziert werden. Hierbei gilt das gleiche Prinzip wie für standardmäßige Transaktionsnachrichten. Lesen Sie diesbezüglich auch den Abschnitt [Transaktionsvorlagen verwalten](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message).

>[!NOTE]
>
>Bei der Depublikation der Vorlage wird automatisch auch das Trigger-Ereignis depubliziert.

Im Zuge der Erstellung von Nachrichteninhalten haben Sie nun die Möglichkeit, Personalisierungsfelder zu verwenden, die auf vom Analytics-Trigger gesendeten Informationen beruhen. Wenn Sie die Ereignisdaten mit Profildaten aus Adobe Campaign anreichern, können Sie die Nachricht mittels dieser Informationen personalisieren. Um Ihre Nachricht zu personalisieren, wählen Sie im Knoten **[!UICONTROL Transaktionsereignis]** > **[!UICONTROL Ereignis-Kontext]** das gewünschte Feld aus.

![](assets/remarketing_8.png)

## Zugriff auf Berichte {#accessing-the-reports}

Öffnen Sie zur Anzeige des dedizierten Trigger-Berichts in Adobe Campaign das Trigger-Ereignis, das Sie zuvor erstellt haben, und verwenden Sie die Schaltfläche **[!UICONTROL Trigger-Bericht anzeigen]**.

![](assets/remarketing_9.png)

In dem Bericht werden die Anzahl verarbeiteter Ereignisse im Vergleich zur Anzahl der von Analytics gesendeten Ereignisse angezeigt. Außerdem werden darin alle aktuellen Trigger angezeigt.

![](assets/trigger_uc_browse_14.png)


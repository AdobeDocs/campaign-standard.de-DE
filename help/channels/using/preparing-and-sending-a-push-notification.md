---
title: Push-Benachrichtigung vorbereiten und senden
description: Diese Schritte zeigen Ihnen, wie Sie einen einmaligen Push-Benachrichtigungs-Versand mit Adobe Campaign erstellen können.
page-status-flag: never-activated
uuid: 01997725-ca0a-420c-9e81-5ea801652f87
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: push-notifications
discoiquuid: ec930cd4-6365-4e54-babe-9dc2eed041fc
context-tags: delivery,mobileAppContent,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 07d68b5bf8d800ebd95919f491e98f1b7a015705

---


# Push-Benachrichtigung vorbereiten und senden{#preparing-and-sending-a-push-notification}

## Benachrichtigung vorbereiten {#preparing-the-notification}

Die Erstellung einer Push-Benachrichtigung in Adobe Campaign umfasst folgende Etappen:

1. From the **[!UICONTROL Marketing activities]** window, [create a new marketing activity](../../start/using/marketing-activities.md#creating-a-marketing-activity).

   Eine einzelne Push-Benachrichtigung kann auch in einer [Kampagne](../../start/using/marketing-activities.md#creating-a-marketing-activity) oder auf der [Startseite](../../start/using/interface-description.md#home-page) von Adobe Campaign erstellt werden.

   Es besteht außerdem die Möglichkeit, eine Aktivität für einen Push-Benachrichtigungsversand innerhalb eines Workflows zu verwenden. Diese Aktivität wird im Abschnitt [Push-Benachrichtigungsversand](../../automating/using/push-notification-delivery.md) beschrieben.

1. Auswählen **[!UICONTROL Push notification]**.
1. Wählen Sie eine Vorlage aus.

   ![](assets/push_notif_type.png)

   Standardmäßig haben Sie die Wahl zwischen zwei Vorlagen:

   * **[!UICONTROL Send push to Campaign profiles]**: Verwenden Sie diese Vorlage, um auf die Adobe Campaign CRM-Profile abzuzielen, die Ihre mobile Anwendung abonniert haben und sich für den Empfang von Push-Benachrichtigungen entschieden haben. Sie können [Personalisierungsfelder](../../designing/using/personalization.md#inserting-a-personalization-field) in Ihre Push-Benachrichtigung einfügen, wie etwa den Vornamen des Empfängers.
   * **[!UICONTROL Send push to app subscribers]**: Verwenden Sie diese Vorlage, um eine Push-Benachrichtigung an alle bekannten und anonymen Benutzer von Mobilanwendungen zu senden, die sich für den Empfang von Benachrichtigungen von Ihrer Anwendung entschieden haben. Sie können diese Nachrichten mit Daten personalisieren, die von Ihrer Mobile App stammen.
   Es stehen auch mehrsprachige Vorlagen zur Auswahl. Weiterführende Informationen dazu finden Sie unter [Mehrsprachige Push-Benachrichtigungen erstellen](../../channels/using/creating-a-multilingual-push-notification.md).

   Weiterführende Informationen zu Vorlagen finden Sie im Abschnitt [Marketingaktivitäten-Vorlagen](../../start/using/marketing-activity-templates.md).

1. Geben Sie Ihre Push-Benachrichtigungseigenschaften ein und wählen Sie die mobile App im **[!UICONTROL Associate a Mobile App to a delivery]** Feld aus.

   Bitte beachten Sie, dass in der Dropdown-Liste sowohl SDK V4- als auch Experience Platform SDK-Anwendungen enthalten sind.

   ![](assets/push_notif_properties.png)

   Sie können die Push-Benachrichtigung mit einer Kampagne verknüpfen. Wählen Sie diese dazu aus den bereits existierenden Kampagnen aus.

1. Im darauffolgenden Bildschirm besteht die Möglichkeit, eine Audience zu definieren (beispielsweise alle VIP-Kunden, die eine bestimmte Mobile App abonniert haben). Weiterführende Informationen dazu finden Sie im Abschnitt [Erstellung von Audiences](../../audiences/using/creating-audiences.md).

   Ihre Audience wird automatisch auf der Basis der Mobile App gefiltert, die im vorherigen Schritt ausgewählt wurde.

   ![](assets/push_notif_audience.png)

1. Sie können jetzt Ihre Push-Benachrichtigung anpassen. Wählen Sie zunächst den Stil der Nachricht aus: **[!UICONTROL Alert/Message/Badge]** oder **[!UICONTROL Silent push]**. Die Typen von Push-Benachrichtigungen werden im Abschnitt [Über Push-Benachrichtigungen](../../channels/using/about-push-notifications.md) beschrieben.

   Bearbeiten Sie den Inhalt Ihrer Push-Benachrichtigung und definieren Sie die erweiterten Optionen. Siehe [Push-Benachrichtigung anpassen](../../channels/using/customizing-a-push-notification.md).

   ![](assets/push_notif_content.png)

   Der Push-Benachrichtigungs-Inhalt und die Optionen, die hier konfiguriert werden, werden in Form von Payload an Ihr Mobile App übertragen. Die Struktur der Payload wird in der Technote [Understanding ACS push notifications payload structure](https://helpx.adobe.com/campaign/kb/understanding-campaign-standard-push-notifications-payload-struc.html) beschrieben.

1. Klicks **[!UICONTROL Create]**.

   ![](assets/push_notif_content_2.png)

1. Vor dem Versand der Benachrichtigung können Sie diese mit Testprofilen testen und überprüfen, wie die Benachrichtigung in der Inbox der Empfänger dargestellt wird. Select **[!UICONTROL Audiences]** from your delivery summary and click the **[!UICONTROL Test profiles]** tab.

   Weiterführende Informationen zum Senden von Testnachrichten finden Sie in [Testprofile](../../sending/using/sending-proofs.md).

1. Select your test profiles and click **[!UICONTROL Preview]** to display the notification: content is personalized with the test profile data.
1. Überprüfen Sie das Layout der Push-Benachrichtigung auf unterschiedlichen Geräten: Wählen Sie iPhone, Android-Smartphone, iPad oder Android-Tablet aus, um sich die jeweilige Darstellung in der Vorschau anzusehen.

   ![](assets/push_notif_preview.png)

1. Die **[!UICONTROL Estimated Payload Size]** Schätzung basiert auf Testprofildaten. Die tatsächliche Payload-Größe kann davon abweichen. Die maximale Größe einer Nachricht beträgt 4 KB.

   >[!CAUTION]
   >
   >Wenn die Payload-Größe die 4-KB-Grenze überschreitet, wird die Nachricht nicht zugestellt. Personalisierungsdaten wirken sich auf die Größe der Nachricht aus.

## Benachrichtigung senden {#sending-the-notification}

Push-Benachrichtigungen können an eine ausgewählte Audience in Adobe Campaign gesendet werden, indem die Kriterien der Audience definiert werden. Beispielsweise besteht die unten ausgewählte Audience aus vier Mobile-App-Abonnenten.

1. Click **[!UICONTROL Prepare]** to compute the target and generate the notifications.

   ![](assets/push_send_1.png)

1. Once the preparation has finished successfully, the **[!UICONTROL Deployment]** window presents the following KPIs: **[!UICONTROL Target]** and **[!UICONTROL To deliver]**. Note that the **[!UICONTROL To deliver]** count is lower than the **[!UICONTROL Targeted]** one due to exclusions which can be viewed by clicking ![](assets/lp_link_properties.png) button at the bottom of the **[!UICONTROL Deployment]** window.

   ![](assets/push_send_2.png)

1. In the **[!UICONTROL Exclusion logs]** tab, you can find the list of all the messages excluded from the target sent and the reason behind this exclusion.

   In unserem Beispiel sehen wir, dass einer unserer Mobile-App-Abonnenten ausgeschlossen wurde, weil seine Adresse auf der Blacklist steht, und die anderen Abonnenten, weil ihr Profil eine Dublette war.

   ![](assets/push_send_5.png)

1. Click the **[!UICONTROL Exclusion causes]** tab to display the volume of excluded messages.

   ![](assets/push_send_7.png)

1. You can now click **[!UICONTROL Confirm]** to start sending push notifications.
1. Prüfen Sie den Status Ihres Versands über das Nachrichten-Dashboard und die entsprechenden Protokolle. Weiterführende Informationen dazu finden Sie unter [Nachrichten versenden](../../sending/using/confirming-the-send.md) und [Versandlogs](../../sending/using/monitoring-a-delivery.md#delivery-logs).

   In diesem Beispiel wird im Nachrichten-Dashboard angezeigt, dass Adobe Campaign versucht hat, zwei Push-Benachrichtigungen zu senden: eine wurde erfolgreich zugestellt und die andere ist fehlgeschlagen. To know why the delivery has errors, click the ![](assets/lp_link_properties.png) button at the bottom of the **[!UICONTROL Deployment]** window.

   ![](assets/push_send_4.png)

1. From the **[!UICONTROL Deployment]** window, click the **[!UICONTROL Sending logs]** tab to access the list of sent push notifications and their statuses. Bei diesem Versand wurde die eine Push-Benachrichtigung erfolgreich gesendet, während die andere wegen eines fehlerhaften Geräte-Tokens fehlgeschlagen ist. Dieser Abonnent wird folglich auf die Blacklist gesetzt und von weiteren Sendungen ausgeschlossen.

   >[!NOTE]
   >
   >Die Gründe dafür können diverse Fehler im Anschluss an die Verarbeitung durch Adobe Campaign sein. Im Fall von Fehlern beim Provider, wie apns und FCM, werden diese im Grund aufgeführt. Weiterführende Informationen über Fehler bei Providern finden Sie in der Dokumentation von [Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CommunicatingwithAPNs.html) und [Android](https://firebase.google.com/docs/cloud-messaging/http-server-ref).

   ![](assets/push_send_6.png)

Jetzt können Sie die Wirkung Ihres Push-Benachrichtigungs-Versands mit dynamischen Berichten ermitteln.

**Verwandte Themen:**

* [Bericht zu Push-Benachrichtigungen](../../reporting/using/push-notification-report.md)
* [Push-Benachrichtigungen in einem Workflow versenden](../../automating/using/push-notification-delivery.md)


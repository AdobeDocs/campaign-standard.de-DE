---
title: Profil-Transaktionsnachrichten
description: Hier erfahren Sie, wie Sie eine Profil-Transaktionsnachricht erstellen und publizieren können.
page-status-flag: never-activated
uuid: a8efe979-74ae-46ff-a305-b86a90679581
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: transactional-messaging
discoiquuid: dcb90afc-42c3-419e-8345-79cddf969e41
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 3b40a9bba79d04f1635b7522cfc99f9e7566c3c0

---


# Profil-Transaktionsnachrichten{#profile-transactional-messages}

Sie können Transaktionsnachrichten basierend auf Kunden-Marketing-Profilen versenden, bei denen Sie folgende Möglichkeiten haben:

* Apply marketing typology rules such as **[!UICONTROL Blacklisted address]** or [fatigue rules](../../sending/using/fatigue-rules.md).
* einen Abmelde-Link in die Nachricht einfügen
* die Transaktionsnachrichten zur allgemeinen Versandberichterstattung hinzufügen
* Die Transaktionsnachrichten für die Customer Journey nutzen

Nach der Erstellung und Publikation des gewünschten Ereignisses (im vorliegenden [Beispiel](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) &quot;Stehen gelassener Warenkorb&quot;) wird die entsprechende Transaktionsnachricht automatisch erstellt.

Die Konfigurationsschritte finden Sie in Abschnitt [Ereignis konfigurieren, um eine Profil-Transaktionsnachricht zu senden](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message).

Damit das Ereignis mit dem Versand einer Transaktionsnachricht einhergeht, muss diese Nachricht personalisiert, getestet und dann publiziert werden.

>[!NOTE]
>
>To access transactional messages, you must be part of the **[!UICONTROL Administrators (all units)]** security group.
>
>Ermüdungsregeln sind mit Profil-Transaktionsnachrichten kompatibel. Näheres dazu finden Sie unter [Ermüdungsregeln](../../sending/using/fatigue-rules.md).

## Profil-Transaktionsnachricht senden {#sending-a-profile-transactional-message}

Die Schritte für das Erstellen, Personalisieren und Publizieren einer Profil-Transaktionsnachricht sind mit denen einer Ereignis-Transaktionsnachricht identisch. Siehe [Ereignis-Transaktionsnachrichten](../../channels/using/event-transactional-messages.md).

Die Unterschiede sind unten aufgeführt.

1. Rufen Sie die erstellte Transaktionsnachricht auf, um sie zu bearbeiten.
1. In the transactional message, click the **[!UICONTROL Content]** section. In addition to the transactional template, you can also choose any email template targeting **[!UICONTROL Profile]**.

   ![](assets/message-center_marketing_templates.png)

1. Wählen Sie die Standard-E-Mail-Vorlage aus.

   Wie alle Marketing-E-Mails enthält sie einen Abmelde-Link.

   ![](assets/message-center_marketing_perso_unsubscription.png)

   Außerdem haben Sie im Gegensatz zu auf Echtzeit-Ereignissen basierenden Konfigurationen direkten Zugriff auf alle Profilinformationen, um die Nachricht zu personalisieren. Siehe [Personalisierungsfelder einfügen](../../designing/using/personalization.md#inserting-a-personalization-field).

1. Speichern Sie Ihre Änderungen und publizieren Sie die Nachricht. Siehe [Transaktionsnachricht publizieren](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message).

## Versand einer Profil-Transaktionsnachricht verfolgen {#monitoring-a-profile-transactional-message-delivery}

Nachdem die Nachricht publiziert wurde und Ihre Webseiten-Integration abgeschlossen ist, kann der Versand verfolgt werden.

1. To view the message delivery log, click the icon at the bottom right of the **[!UICONTROL Deployment]** block.

   Weiterführende Informationen zum Zugriff auf Logs finden Sie im Abschnitt [Versand verfolgen](../../sending/using/monitoring-a-delivery.md).

1. Wählen Sie die **[!UICONTROL Sending logs]** Registerkarte. In the **[!UICONTROL Status]** column, **[!UICONTROL Sent]** indicates that a profile has opted in.

   ![](assets/message-center_marketing_sending_logs.png)

1. Select the **[!UICONTROL Exclusions logs]** tab to view recipients who have been excluded from the message target, such as blacklisted addresses.

   ![](assets/message-center_marketing_exclusion_logs.png)

For any profile that has opted out, the **[!UICONTROL Blacklisted address]** typology rule excluded the corresponding recipient.

This rule is part of a specific typology that applies to all transactional messages based on the **[!UICONTROL Profile]** table.

![](assets/message-center_marketing_typology.png)

**Verwandte Themen**:

* [Webseiten-Integration](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website)
* [Typologien](../../sending/using/about-typology-rules.md)


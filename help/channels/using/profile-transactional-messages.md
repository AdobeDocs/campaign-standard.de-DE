---
title: Profil-Transaktionsnachrichten
seo-title: Profil-Transaktionsnachrichten
description: Profil-Transaktionsnachrichten
seo-description: Hier erfahren Sie, wie Sie eine Profil-Transaktionsnachricht erstellen und publizieren können.
page-status-flag: nie aktiviert
uuid: a 8 efe 979-74 ae -46 ff-a 305-b 86 a 90679581
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Kanäle
content-type: Referenz
topic-tags: Transaktionsnachrichten
discoiquuid: dcb 90 afc -42 c 3-419 e -8345-79 cddf 969 e 41
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 855db33971afdf9f02bf1b00be67c9e3f50bee06

---


# Profil-Transaktionsnachrichten{#profile-transactional-messages}

Sie können Transaktionsnachrichten basierend auf Kunden-Marketing-Profilen versenden, bei denen Sie folgende Möglichkeiten haben:

* Marketing-Typologieregeln anwenden, wie **[!UICONTROL Adresse auf der Blacklist]** oder [Ermüdungsregeln](../../administration/using/fatigue-rules.md).
* einen Abmelde-Link in die Nachricht einfügen
* die Transaktionsnachrichten zur allgemeinen Versandberichterstattung hinzufügen
* Die Transaktionsnachrichten für die Customer Journey nutzen

Nach der Erstellung und Publikation des gewünschten Ereignisses (im vorliegenden [Beispiel](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) "Stehen gelassener Warenkorb") wird die entsprechende Transaktionsnachricht automatisch erstellt.

Die Konfigurationsschritte finden Sie in Abschnitt [Ereignis konfigurieren, um eine Profil-Transaktionsnachricht zu senden](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message).

Damit das Ereignis mit dem Versand einer Transaktionsnachricht einhergeht, muss diese Nachricht personalisiert, getestet und dann publiziert werden.

>[!NOTE]
>
>To access the transactional messages, you must have administration rights or appear in the **[!UICONTROL Message Center agents]** (mcExec) security group. Ermüdungsregeln sind mit Profil-Transaktionsnachrichten kompatibel. Näheres dazu finden Sie unter [Ermüdungsregeln](../../administration/using/fatigue-rules.md).

## Profil-Transaktionsnachricht senden {#sending-a-profile-transactional-message}

Die Schritte für das Erstellen, Personalisieren und Publizieren einer Profil-Transaktionsnachricht sind mit denen einer Ereignis-Transaktionsnachricht identisch. Siehe [Ereignis-Transaktionsnachrichten](../../channels/using/event-transactional-messages.md).

Die Unterschiede sind unten aufgeführt.

1. Rufen Sie die erstellte Transaktionsnachricht auf, um sie zu bearbeiten.
1. Klicken Sie in der Transaktionsnachricht auf den Bereich **[!UICONTROL Inhalt.]** Anstelle der Transaktionsvorlage können Sie auch die Standard-E-Mail-Vorlage auswählen, die auf die Ressource **[!UICONTROL Profil ausgerichtet ist]**.

   ![](assets/message-center_marketing_templates.png)

1. Wählen Sie die Standard-E-Mail-Vorlage aus.

   Wie alle Marketing-E-Mails enthält sie einen Abmelde-Link.

   ![](assets/message-center_marketing_perso_unsubscription.png)

   Außerdem haben Sie im Gegensatz zu auf Echtzeit-Ereignissen basierenden Konfigurationen direkten Zugriff auf alle Profilinformationen, um die Nachricht zu personalisieren. Siehe [Personalisierungsfelder einfügen](../../designing/using/inserting-a-personalization-field.md).

1. Speichern Sie Ihre Änderungen und publizieren Sie die Nachricht. Siehe [Transaktionsnachricht publizieren](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message).

## Versand einer Profil-Transaktionsnachricht verfolgen {#monitoring-a-profile-transactional-message-delivery}

Nachdem die Nachricht publiziert wurde und Ihre Webseiten-Integration abgeschlossen ist, kann der Versand verfolgt werden.

1. Der Zugriff auf den Versandlog der Nachricht ist über die Schaltfläche rechts unten in der **[!UICONTROL Freigabe]-Kachel möglich.**

   Weiterführende Informationen zum Zugriff auf Logs finden Sie im Abschnitt [Versand verfolgen](../../sending/using/monitoring-a-delivery.md).

1. Wählen Sie den Tab **[!UICONTROL Versandlogs]aus.** In der **[!UICONTROL Status]**-Spalte zeigt **Gesendet]an, dass sich ein Profil angemeldet hat.[!UICONTROL **

   ![](assets/message-center_marketing_sending_logs.png)

1. Wählen Sie den Tab **[!UICONTROL Ausschlusslogs], um die Empfänger anzuzeigen, die von der Versandzielgruppe ausgeschlossen wurden, wie zum Beispiel Adressen auf der Blacklist.**

   ![](assets/message-center_marketing_exclusion_logs.png)

Profile, die sich abgemeldet haben, wurden durch die Typologieregel **[!UICONTROL Adresse auf der Blacklist]ausgeschlossen.**

Diese Regel ist Teil einer spezifischen Typologie, die für alle auf der **[!UICONTROL Profil]-Tabelle basierenden Transaktionsnachrichten gilt.**

![](assets/message-center_marketing_typology.png)

**Verwandte Themen**:

* [Webseiten-Integration](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website)
* [Typologien](../../administration/using/about-typology-rules.md)


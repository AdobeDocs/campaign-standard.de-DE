---
title: Über die Planung von Sendungen
description: Hier erfahren Sie, wie Sie den Nachrichtenversand zeitlich planen können.
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 100%

---


# Über die Planung von Sendungen{#about-scheduling-messages}

>[!CAUTION]
>
>Wenn Sie den Zeitplan eines Versands ändern, müssen Sie den Versand erneut vorbereiten, indem Sie auf die Schaltfläche **Vorbereiten** und danach auf **Bestätigen** klicken.

Der Zeitpunkt des Nachrichtenversands (E-Mails, SMS-Nachrichten oder Push-Benachrichtigungen) wird im Nachrichten-Dashboard in der Kachel **[!UICONTROL Planung]** definiert.

![](assets/delivery_dashboard.png)

Unter **[!UICONTROL Planung]** können Sie Versandoptionen für E-Mails, SMS-Nachrichten oder Push-Benachrichtigungen festlegen:

* **[!UICONTROL Nachrichten werden unmittelbar bei Bestätigung gesendet]**: Nachrichten werden gesendet, sobald der Versand bestätigt wurde. Siehe [Versand bestätigen](../../sending/using/confirming-the-send.md).

   ![](assets/delivery_planning_1.png)

* **[!UICONTROL Nachrichtenversand am unten angegebenen Datum]**: Nachrichten werden an einem späteren Datum gesendet. Geben Sie das gewünschte **Kontaktdatum** im Feld **Versandstart am** an.

   Sie können den Versand vorbereiten und bestätigen, die Nachrichten werden aber erst zum ausgewählten Zeitpunkt gesendet. Informationen zur Vorbereitung und Validierung des Versands finden Sie in den Abschnitten [Versandvorbereitung](../../sending/using/preparing-the-send.md) und [Versand bestätigen](../../sending/using/confirming-the-send.md).

   Mithilfe der Dropdown-Liste **[!UICONTROL Zeitzone des Kontaktdatums]** können Sie die für den Versand zu berücksichtigende Zeitzone anpassen. Wenn Sie beispielsweise im Feld **[!UICONTROL Start des Versands von]** 9:00 Uhr eingeben und in der Dropdown-Liste **[!UICONTROL Zeitzone des Kontaktdatums]** Brüssel, Kopenhagen, Madrid, Paris (GMT+1) auswählen, erhalten alle Empfänger die Nachricht um 9:00 Uhr Pariser Zeit. Folglich erhält ein Empfänger in Moskau (GMT+3) die Nachricht um 11:00 Uhr Moskauer Zeit.

   Aktivieren Sie die Option **[!UICONTROL Vor dem Nachrichtenversand Bestätigung einholen]**, wenn Sie den tatsächlichen Versand der Nachrichten von einer manuellen Bestätigung abhängig machen möchten. Standardmäßig ist diese Option aktiviert.

   ![](assets/delivery_planning.png)

>[!CAUTION]
>
>Beim Duplizieren eines Versands werden alle Terminierungseinstellungen gelöscht. Der duplizierte Versand wird gestartet, sobald er validiert wurde, außer Sie geben ein neues Kontaktdatum an.

**Verwandte Themen**:

* [Versandzeitpunkt optimieren](../../sending/using/optimizing-the-sending-time.md)
* [Nachrichten in der Zeitzone des Empfängers senden](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)
* [Versanddatum berechnen](../../sending/using/computing-the-sending-date.md)


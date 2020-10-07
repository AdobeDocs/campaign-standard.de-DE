---
title: Versandzeitpunkt optimieren
description: Hier erfahren Sie, wie Sie den Versandzeitpunkt festlegen und die Öffnungsrate Ihrer Nachrichten verbessern.
page-status-flag: never-activated
uuid: c2c13934-9819-4e18-b5c7-60915c907f37
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 609355f6-9003-41b9-9981-ea787419fbf5
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 100%

---


# Versandzeitpunkt optimieren{#optimizing-the-sending-time}

Um die Öffnungsrate Ihrer Nachrichten zu erhöhen, können Sie für jeden Empfänger manuell einen Versandzeitpunkt festlegen. Jedes Profil erhält dann die Nachricht zum spezifizierten Zeitpunkt.

Der Versandzeitpunkt kann auf Versandebene oder mit einem Workflow definiert werden.

Je nach der Auslastung des Servers und der Anzahl der weiteren Zustellversuche wird versucht, E-Mail-Nachrichten zu dem für jeden Empfänger festgelegten Zeitpunkt zu versenden.

* Die weiteren Zustellversuche hängen vom ISP und Ihrer Reputation ab. Wenn die Nachricht nicht beim ersten Versuch akzeptiert wird, werden möglicherweise mehrere weitere Zustellversuche unternommen. Näheres wird in Abschnitt [Liste der E-Mail-Kanal-Parameter](../../administration/using/configuring-email-channel.md) beschrieben.
* Wegen unzureichender Bandbreite können Verzögerungen beim Empfang der E-Mails auftreten.

Den tatsächlichen Versandzeitpunkt an jeden Empfänger finden Sie in den [Versandlogs](../../sending/using/monitoring-a-delivery.md#sending-logs).

Mehrere Optionen sind verfügbar:

* **[!UICONTROL Keine Optimierung]**: Der Versandzeitpunkt basiert auf der Zeitzone des Benutzers.

   Wenn Ihre Zeitzone beispielsweise GMT+1 ist und Sie 9 Uhr in das Feld **[!UICONTROL Versandstart am]** eingeben, erhält ein Empfänger in der Zeitzone GMT+3 die Nachricht um 11 Uhr Ortszeit.

* **[!UICONTROL Gemäß der Zeitzone des Empfängers senden]**: Alle Empfänger erhalten die Nachricht unter Berücksichtigung ihrer Zeitzone.

   Wenn Sie beispielsweise 9 Uhr in das Feld **[!UICONTROL Versandstart am]** eingeben, erhält ein Empfänger in der Zeitzone GMT+3 die Nachricht um 9 Uhr Ortszeit.

   Siehe [Nachrichten in der Zeitzone des Empfängers senden](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md).

* **[!UICONTROL An dem durch die Formel definierten Datum senden]**: Jeder Empfänger erhält die Nachricht zu einem mit der speziellen Formel konfigurierten Zeitpunkt.

   Siehe [Versanddatum berechnen](../../sending/using/computing-the-sending-date.md).


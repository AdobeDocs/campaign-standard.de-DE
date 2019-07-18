---
title: Nachrichten in der Zeitzone des Empfängers senden
seo-title: Nachrichten in der Zeitzone des Empfängers senden
description: Nachrichten in der Zeitzone des Empfängers senden
seo-description: Hier erfahren Sie, wie Sie Nachrichten in der Zeitzone des Empfängers senden.
page-status-flag: nie aktiviert
uuid: 70228 c 07-451 f -4 ddb -8 d 26-92 a 5 a 4814 e 3 a
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird gesendet
content-type: Referenz
topic-tags: sheduling-messages
discoiquuid: daa 980 ba -8 c 7 c -4673-a 68 f -379 d 63 e 4 b 8 bd
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 806dc4736ffb395a0eea102090c688102478aaca

---


# Nachrichten in der Zeitzone des Empfängers senden{#sending-messages-at-the-recipient-s-time-zone}

Wenn bei einer Kampagne das Datum und die Uhrzeit wichtig sind, können Sie den Versand so terminieren, dass die Ortszeit eines jeden Empfängers berücksichtigt wird. Ihre Empfänger erhalten dann E-Mails, SMS-Nachrichten oder Push-Benachrichtigungen zum von Ihnen festgelegten Zeitpunkt in ihrer eigenen Zeitzone.

>[!NOTE]
>
>Um diese Funktion verwenden zu können, muss in allen von Ihrem Versand eingeschlossenen Profilen in den Eigenschaften im Bereich **[!UICONTROL Adresse]eine Zeitzone angegeben sein.** Nähere Informationen zum Zugriff auf Profileigenschaften erhalten Sie in [diesem Abschnitt](../../audiences/using/editing-profiles.md).

Zum Senden einer Nachricht in der Zeitzone des Empfängers können Sie auch die Aktivität **[!UICONTROL Planung]in einem Workflow verwenden.** Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../automating/using/scheduler.md).

Im folgenden Beispiel möchten wir allen Kunden auf der ganzen Welt einen nur am Valentinstag gültigen Gutschein-Code senden. Damit die Empfänger genügend Zeit haben, den Gutschein noch am selben Tag einzulösen, müssen sie Ihre Nachricht am 14. Februar um 8 Uhr in ihrer jeweiligen Zeitzone erhalten.

1. Beginnen Sie mit der Erstellung Ihres Versands – in unserem Fall einer E-Mail – im Tab **[!UICONTROL Marketingaktivitäten.]** Weiterführende Informationen zur Versanderstellung finden Sie in diesem [Abschnitt](../../channels/using/creating-an-email.md).
1. Klicken Sie nach der Erstellung Ihrer Valentinstags-E-Mail auf **[!UICONTROL Erstellen], um das Versand-Dashboard zu öffnen.** Weiterführende Informationen zur Erstellung von E-Mails finden Sie auf dieser [Seite](../../designing/using/example--email-personalization.md).

   ![](assets/send-time_opt_valentine_1.png)

1. Wählen Sie im Versand-Dashboard die Kachel **[!UICONTROL Planung].**

   ![](assets/send-time_opt_valentine_2.png)

1. Wählen Sie die Option **[!UICONTROL Nachrichtenversand am unten angegebenen Datum]aus.** Definieren Sie dann das Kontaktdatum im Feld **[!UICONTROL Start des Versands am], in unserem Fall den 14. Februar um 8:00 Uhr, sodass jeder Empfänger die Nachricht am Valentinstag erhält.**

   ![](assets/send-time_opt_valentine.png)

1. Wählen Sie im Feld **[!UICONTROL Zeitzone des Kontaktdatums]aus, in welcher Zeitzone Ihr Versand standardmäßig durchgeführt werden soll.**

   If a profile's **[!UICONTROL Time zone]** is left as **[!UICONTROL Default]**, the recipients will receive the delivery depending on the chosen time zone here.

1. From the **[!UICONTROL Optimize the sending time per recipient]** drop-down menu, choose **[!UICONTROL Send at the recipient's time zone]**. Dadurch erhalten die Empfänger die Valentinstags-E-Mail am 14. Februar ihrer Zeitzone.

   ![](assets/send-time_opt_valentine_3.png)

1. Bestätigen Sie den Zeitplan Ihres Versands und klicken Sie auf die Schaltfläche **[!UICONTROL Vorbereiten]** und danach auf **Bestätigen[!UICONTROL .]**

   Nehmen Sie die Validierung mindestens 24 Stunden vor dem Versand vor. Andernfalls könnten manche Empfänger abhängig von ihrem Standort den Versand schon vor dem Valentinstag erhalten.

   ![](assets/send-time_opt_valentine_4.png)

Alle Empfänger auf der ganzen Welt erhalten daraufhin die Nachricht am 14. Februar um 8 Uhr Ortszeit.

---
title: Fallen verwenden
description: Erfahren Sie, wie Sie Fallen in Nachrichten verwenden.
page-status-flag: never-activated
uuid: eb4d893b-3724-4b15-9312-1ec74784368d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
discoiquuid: 37320ec5-196c-4260-8156-98932da3e4a5
context-tags: seedMember,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a7c2d444b7d971124b676fa2392b51aab40e5629

---


# Fallen verwenden {#using-traps}

Bei der Verwendung von Fallen wird die Nachricht neben der Hauptzielgruppe auch an das [Testprofil](../../audiences/using/managing-test-profiles.md) gesendet. Das Ziel dabei ist insbesondere zu überwachen, ob Ihre Kundendatei für unlautere Zwecke verwendet wird.

Fallen wurden ursprünglich für den Briefpostversand entwickelt. Sie ermöglichen Ihnen Folgendes:

* Sie können überprüfen, ob Ihr Briefpost-Anbieter die Nachricht tatsächlich sendet.
* Sie erhalten die Post zur gleichen Zeit und im selben Zustand wie Ihre Kunden.
* Sie können sich eine exakte Kopie der gesendeten Nachricht aufbewahren.
* Sie können sich vergewissern, dass Ihre Kundenliste nicht von Ihrem Briefpost-Anbieter missbraucht wird. Wenn eine andere Nachricht an die Adresse Ihres Testprofils gesendet wird, wurde Ihre Kundendatei möglicherweise ohne Ihr Wissen verwendet. Deshalb sollte die Adresse des Testprofils nur zu diesem Zweck verwendet werden.

Weiterführende Informationen zum Hinzufügen von Fallen zur Zielgruppe eines Briefpostversands finden Sie unter [Test- und Fallen-Profile hinzufügen](../../channels/using/defining-the-direct-mail-audience.md#adding-test-and-trap-profiles).

Wenn Sie Ihrer Hauptzielgruppe bei den anderen Kommunikationskanälen Fallen-Testprofile hinzufügen, haben Sie folgende Möglichkeiten:

* Sie können überprüfen, ob Ihre Nachricht erfolgreich gesendet wurde.
* Sie können eine exakte Kopie Ihrer Nachricht erhalten und aufbewahren.
* Sie können verfolgen, wann die Nachricht gesendet und empfangen wurde.

Um ein Testprofil als Falle zu verwenden, muss es in der Zielgruppe Ihrer Nachricht enthalten sein.

>[!NOTE]
>
>Im Gegensatz zu Testprofilen, die für [Testsendungen](../../sending/using/sending-proofs.md) oder zum [E-Mail-Rendering](../../sending/using/email-rendering.md) verwendet werden, erfolgt der Nachrichtenversand an die Hauptzielgruppe und die Testprofile, die als Fallen verwendet werden, gleichzeitig.

Gehen Sie beim Definieren der Zielgruppe einer Nachricht folgendermaßen vor:

1. From the **[!UICONTROL Test profiles]** tab, select a test profile. Make sure that it has **[!UICONTROL Trap]** as the intended use.

   ![](assets/trap_select.png)

1. Once your message content is ready, click the **[!UICONTROL Prepare]** button. Siehe [Versandvorbereitung](../../sending/using/preparing-the-send.md).
   >[!NOTE]
   >
   >Stellen Sie sicher, dass Sie eine Hauptzielgruppe ausgewählt haben. Andernfalls kann Ihre Nachricht nicht gesendet werden.

1. Click the **[!UICONTROL Confirm]** button. Siehe [Versand bestätigen](../../sending/using/confirming-the-send.md).

   ![](assets/trap_confirm.png)

Die Nachricht wird an die Hauptzielgruppe und an das Testprofil gesendet.

Sie können beim Senden von Transaktionsnachrichten Traps verwenden. In diesem Fall erhält das Test-Profil eine Nachricht pro Ereignis-Konfiguration. For more on transactional messaging, see this [section](../../channels/using/about-transactional-messaging.md).

>[!NOTE]
>
>Bei Verwendung eines Testprofils als Falle werden die entsprechenden zusätzlichen Daten für alle angereicherten Felder in einer Nachricht nach dem Zufallsprinzip aus einem echten Zielgruppenprofil ausgewählt und dem Fallen-Testprofil zugewiesen. Weiterführende Informationen zur Anreicherung finden Sie in [diesem Beispiel](../../automating/using/enrichment.md#example--enriching-profile-data-with-data-contained-in-a-file).

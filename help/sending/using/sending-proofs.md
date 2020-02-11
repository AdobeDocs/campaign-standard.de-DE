---
title: Testversand durchführen
description: Erfahren Sie, wie Sie Beweise senden.
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
source-git-commit: ff9d0c3ca42606f097a34b1835d285541061e57b

---


# Testversand durchführen {#sending-proofs}

Ein Testversand dient der Validierung einer Nachricht, bevor sie an die Hauptzielgruppe gesendet wird.

Die Empfänger des Testversands haben die Aufgabe, sowohl Inhalt als auch Form der Nachricht zu validieren. Die Profile, die Testsendungen erhalten sollen, werden im Tab **Testprofile** ausgewählt. Weiterführende Informationen dazu finden Sie im Abschnitt [Verwaltung von Testprofilen](../../audiences/using/managing-test-profiles.md).

Um Testsendungen vornehmen zu können, muss die Audience Ihrer Nachricht mindestens ein Testprofil enthalten.

Gehen Sie in einer Nachricht wie folgt vor, um einen Test zu senden:

1. Click the **[!UICONTROL Send a test]** button.

   ![](assets/bat_select.png)

1. Wählen Sie die Art des Testversands aus:

   * **[!UICONTROL Email rendering]**: Wählen Sie diese Option, um zu testen, wie Ihre Nachricht entsprechend den vorgesehenen Postfächern empfangen wird. Weiterführende Informationen finden Sie im Abschnitt [E-Mail-Rendering](../../sending/using/email-rendering.md).
   * **[!UICONTROL Proof]**: Wählen Sie diese Option, um die Nachricht zu testen, bevor sie an das Hauptziel gesendet wird. Die Testversand-Empfänger sind verantwortlich für die Validierung des Inhalts und der Form von Sendungen.
   * **[!UICONTROL Proof + Email rendering]**: Diese Option kombiniert die beiden vorherigen Optionen.
   ![](assets/bat_select1.png)

1. Bestätigen Sie Ihre Auswahl.

   Die Testsendungen werden an die Testprofile geschickt.

   ![](assets/bat_select2.png)

1. You can view your proofs using the **[!UICONTROL Proofs]** drop-down list.

   ![](assets/bat_view.png)

1. Wählen Sie einen Testversand aus, um seine Zusammenfassung anzuzeigen. For an email, if you have selected the **Email rendering** option as the proof type, the **[!UICONTROL Access email rendering]** icon is displayed on the right of the proof label. Siehe [E-Mail-Rendering](../../sending/using/email-rendering.md).

   ![](assets/bat_view2.png)

Nach Prüfung des Testversands durch die Testprofile sind gegebenenfalls Änderungen im Versandinhalt und seiner Form vorzunehmen. Nach jeder Änderung ist der Versand erneut vorzubereiten. Es empfiehlt sich außerdem, einen neuen Testversand zu erzeugen. Each new proof can be accessed using the **[!UICONTROL Show proofs]** button.

Senden Sie so viele Testsendungen wie nötig sind, um zu einer endgültigen Version des Nachrichteninhalts zu gelangen. Danach können Sie den Versand an die Hauptzielgruppe senden und den Validierungszyklus beenden.

**Verwandtes Thema:**

Video [Sending a test, preparing and sending an email](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/getting-started/sending-test-preparing-sending-email.html)

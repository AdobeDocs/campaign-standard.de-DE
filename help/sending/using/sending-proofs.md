---
title: Testversand durchführen
description: Erfahren Sie, wie Sie einen Testversand durchführen.
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
source-git-commit: f7f90991ed4c7323e3a2f8ac7d38da9ff165ef76

---


# Testversand durchführen {#sending-proofs}

## Info zu Testversänden {#about-proofs}

Ein Testversand dient der Validierung einer Nachricht, bevor sie an die Hauptzielgruppe gesendet wird. Die Empfänger des Testversands haben die Aufgabe, sowohl Inhalt als auch Form der Nachricht zu validieren. 

Es gibt zwei Typen von Testversand-Empfängern:

* **Mit Test-Profilen** können Sie zusätzliche Empfänger Zielgruppe werden, die nicht den definierten Targeting-Kriterien entsprechen.

   Sie können der Audience einer Nachricht hinzugefügt werden, um eine betrügerische Nutzung Ihrer Empfänger-Datenbank zu erkennen oder sicherzustellen, dass die E-Mails in den Postfächern eingehen. Weiterführende Informationen dazu finden Sie im Abschnitt [Verwaltung von Testprofilen](../../audiences/using/managing-test-profiles.md).

   >[!NOTE]
   >
   >Um Testsendungen vornehmen zu können, muss die Audience Ihrer Nachricht mindestens ein Testprofil enthalten.

* **Substitution-Profil** ermöglichen es Ihnen, sich in die Position eines der zielgerichteten Profil zu setzen und eine genaue Darstellung der Nachricht zu erhalten, die das Profil erhalten wird. Weitere Informationen finden Sie unter [Testen von E-Mail-Nachrichten mit zielgerichteten Profilen](../../sending/using/testing-messages-using-target.md).

   >[!NOTE]
   >
   >Diese Funktion steht nur für E-Mail-Kanal zur Verfügung.

## Testversand durchführen {#sending-a-proof}

Gehen Sie wie folgt vor, um Testversand zu senden:

1. Vergewissern Sie sich, dass die Testversand-Empfänger konfiguriert wurden:
   * **Test-Profil** müssen in der Audience Ihrer Nachricht enthalten sein.
   * **Nach erfolgreicher Vorbereitung der Nachricht müssen Profil** zum Austausch hinzugefügt werden (siehe [diesen Abschnitt](../../sending/using/testing-messages-using-target.md)).

1. Click the **[!UICONTROL Send a test]** button.

   ![](assets/bat_select.png)

1. Wählen Sie die Art des Testversands aus:

   * **[!UICONTROL Email rendering]**: Wählen Sie diese Option, um zu testen, wie Ihre Nachricht entsprechend den vorgesehenen Postfächern empfangen wird. Weiterführende Informationen finden Sie im Abschnitt [E-Mail-Rendering](../../sending/using/email-rendering.md).
   * **[!UICONTROL Proof]**: Wählen Sie diese Option, um die Nachricht zu testen, bevor sie an die Haupt-Zielgruppe gesendet wird. Die Testversand-Empfänger sind verantwortlich für die Validierung des Inhalts und der Form von Sendungen.
   * **[!UICONTROL Proof + Email rendering]**: Diese Option kombiniert die beiden vorherigen Optionen.
   ![](assets/bat_select1.png)

   >[!NOTE]
   >
   >Das Rendering per Email ist nur mit Test-Profilen möglich. Wenn der Nachricht keine Testelemente hinzugefügt wurden, steht nur die **[!UICONTROL Proof]** Option zur Auswahl zur Verfügung.

1. Bestätigen Sie Ihre Auswahl.

   Die Testversand werden an die konfigurierten Empfänger gesendet.

   ![](assets/bat_select2.png)

1. You can view your proofs using the **[!UICONTROL Proofs]** drop-down list.

   ![](assets/bat_view.png)

1. Wählen Sie einen Testversand aus, um seine Zusammenfassung anzuzeigen. For an email, if you have selected the **Email rendering** option as the proof type, the **[!UICONTROL Access email rendering]** icon is displayed on the right of the proof label. Siehe [E-Mail-Rendering](../../sending/using/email-rendering.md).

   ![](assets/bat_view2.png)

Nach Prüfung des Testversands durch die Testprofile sind gegebenenfalls Änderungen im Versandinhalt und seiner Form vorzunehmen. Nach jeder Änderung ist der Versand erneut vorzubereiten. Es empfiehlt sich außerdem, einen neuen Testversand zu erzeugen. Each new proof can be accessed using the **[!UICONTROL Show proofs]** button.

Senden Sie so viele Testsendungen wie nötig sind, um zu einer endgültigen Version des Nachrichteninhalts zu gelangen. Danach können Sie den Versand an die Hauptzielgruppe senden und den Validierungszyklus beenden.

## Betreffzeile des Testversands konfigurieren {#configuring-proofs-subject-line}

Beim Senden eines Testversands wird die Betreffzeile standardmäßig mit dem Präfix **&quot;Testversand&quot;** sowie einem Zähler mit der Nummer des Testversands konfiguriert.

![](assets/proof-prefix.png)

Gehen Sie wie folgt vor, um die Standardbetreffzeile zu verwenden:

1. Klicken Sie im Dashboard der Nachricht auf die **[!UICONTROL Open properties]** Schaltfläche.
1. Definieren Sie im **[!UICONTROL Advanced parameters]** Abschnitt das Präfix, das Sie standardmäßig in der Betreffzeile verwenden möchten.

Um die Nummer des Testversands in der Betreffzeile auszublenden, aktivieren Sie die **[!UICONTROL Hide proof prefix counter]** Option.

>[!NOTE]
>
>Wenn Sie das gesamte Präfix des Testversands ausblenden möchten, lassen Sie das Feld **[!UICONTROL Subject line prefix]** leer.

![](assets/proof-prefix-configuration.png)

1. Klicks **[!UICONTROL Confirm]**. Die Einstellungen werden standardmäßig auf alle Testversand angewendet, die für die jeweilige Nachricht gesendet werden.

**Verwandtes Thema:**

* Video [Sending a test, preparing and sending an email](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/getting-started/sending-test-preparing-sending-email.html)
* [Testen von E-Mail-Nachrichten mit zielgerichteten Profilen](../../sending/using/testing-messages-using-target.md).
* [Verwaltung von Testprofilen](../../audiences/using/managing-test-profiles.md).
* [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md)
* [E-Mail-Kanal konfigurieren](../../administration/using/configuring-email-channel.md)

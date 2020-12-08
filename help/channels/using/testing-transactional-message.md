---
solution: Campaign Standard
product: campaign
title: Ereignis-Transaktionsnachrichten
description: Hier erfahren Sie, wie Sie eine Ereignis-Transaktionsnachricht erstellen und publizieren.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
translation-type: tm+mt
source-git-commit: caa41d6c727385bd6e77f64750872f191a5ad040
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 76%

---


# Transaktionsnachricht testen {#testing-a-transactional-message}

Bevor Sie Ihre Transaktionsnachricht veröffentlichen, können Sie ein bestimmtes Profil erstellen, mit dem Sie die Nachricht ordnungsgemäß überprüfen können.

## Spezifisches Testprofil definieren {#defining-specific-test-profile}

Definieren Sie ein Profil, das mit Ihrem Ereignis verknüpft wird. Auf diese Weise können Sie eine Vorschau Ihrer Nachricht anzeigen und einen relevanten Testversand durchführen.

1. Klicken Sie im Dashboard [Transaktionsnachricht](../../channels/using/editing-transactional-message.md#accessing-transactional-messages) auf die Schaltfläche **[!UICONTROL Test-Profil erstellen]**.

   ![](assets/message-center_test-profile.png)

1. Geben Sie im Bereich **[!UICONTROL Für die Personalisierung verwendete Ereignisdaten]** die zu übermittelnden Daten im JSON-Format an. Bei den angegebenen Daten handelt es sich um den Inhalt, der in der Vorschau verwendet und dem Testprofil im Testversand übermittelt wird.

   ![](assets/message-center_event-data.png)

   >[!NOTE]
   >
   >Wenn Sie Ihre Nachricht erweitert haben, können Sie auch Informationen zu einer anderen Tabelle eingeben, z. B. **[!UICONTROL Profil]**. Siehe [Anreichern des Ereignisses](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content) und [Personalisieren einer Transaktionsnachricht](../../channels/using/editing-transactional-message.md#personalizing-a-transactional-message).

1. Nach seiner Erstellung ist das Testprofil in der Transaktionsnachricht vorausgefüllt. Verwenden Sie den Block **[!UICONTROL Testprofile]** der Nachricht, um Ihre Testversand-Zielgruppe zu überprüfen.

   ![](assets/message-center_5.png)

Sie haben außerdem die Möglichkeit, ausgehend vom Menü **[!UICONTROL Testprofile]** ein neues Testprofil zu erstellen bzw. ein bereits existierendes zu verwenden. Gehen Sie dazu wie folgt vor:

1. Verwenden Sie hierzu das **[!UICONTROL Adobe-Campaign]**-Logo oben links im Bildschirm und anschließend die Schaltflächen **[!UICONTROL Profile &amp; Audiences]** > **[!UICONTROL Testprofile]**.
1. Wählen Sie im Abschnitt **[!UICONTROL Ereignis]** das soeben erstellte Ereignis aus. Im vorliegenden Beispiel handelt es sich um &quot;Warenkorbabbruch (EVTcartAbandonment)&quot;.
1. Geben Sie im Tab **[!UICONTROL Ereignisdaten]** im Texteditor die zu übermittelnden Daten im JSON-Format an.

   ![](assets/message-center_3.png)

1. Speichern Sie Ihre Änderungen.
1. [Rufen Sie die von Ihnen erstellte Nachricht auf und wählen Sie das aktualisierte Testprofil aus.](../../channels/using/editing-transactional-message.md#accessing-transactional-messages)

**Verwandte Themen:**

* [Verwaltung von Testprofilen](../../audiences/using/managing-test-profiles.md)
* [Audiences erstellen](../../audiences/using/creating-audiences.md)

## Testversand durchführen {#sending-proof}

Nachdem Sie ein oder mehrere spezifische Testprofile erstellt und Ihre Transaktionsnachricht gespeichert haben, können Sie einen Testversand durchführen.

![](assets/message-center_10.png)

Die Schritte zum Senden eines Testversands finden Sie im Abschnitt [Senden von Testversänden](../../sending/using/sending-proofs.md).

---
title: E-Mail-Rendering
description: Hier erfahren Sie Näheres zur E-Mail-Rendering-Funktion.
page-status-flag: never-activated
uuid: c423e237-ad39-4797-ac3a-4320894a8f99
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
discoiquuid: 2b5b13c8-2e51-4985-a161-c1d7f0fc32b4
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 07d68b5bf8d800ebd95919f491e98f1b7a015705

---


# E-Mail-Rendering{#email-rendering}

Before hitting the **[!UICONTROL Send]** button, make sure that your message will be displayed in an optimal way on a variety of web clients, web mails and devices.

Zu diesem Zweck unterstützt Adobe Campaign das Rendering und stellt dessen Ergebnisse in einem entsprechenden Bericht zur Verfügung. Dadurch können Sie sich ansehen, wie Nachrichten je nach verwendetem Empfangsmedium beim Empfänger dargestellt werden.

Die für das **E-Mail-Rendering** in Adobe Campaign verfügbaren Clients für Mobilgeräte, SMS und Webmail finden Sie auf der Litmus-[Website](https://litmus.com/email-testing) (wählen Sie dazu die Option zum **Ansehen aller E-Mail-Clients** aus).

## E-Mail-Rendering-Bericht prüfen {#checking-the-email-rendering-report}

Nachdem Sie Ihren E-Mail-Versand erstellt und seinen Inhalt sowie die Zielpopulation definiert haben, folgen Sie den unten stehenden Schritten.

1. Click **Audience** to access the **[!UICONTROL Test profiles]** tab.

   ![](assets/email_rendering_05.png)

1. Definieren Sie über den Abfrageeditor die Testprofile, die Sie verwenden möchten, einschließlich der Testprofile für das **E-Mail-Rendering**. Siehe [Über Testprofile](../../audiences/using/managing-test-profiles.md).

   ![](assets/email_rendering_06.png)

1. Bestätigen Sie Ihre Abfrage und speichern Sie Ihre Änderungen.
1. Click the **[!UICONTROL Test]** button in the action bar.

   ![](assets/email_rendering_07.png)

1. Wählen Sie die **[!UICONTROL Email rendering]** Option aus und klicken Sie auf **[!UICONTROL OK]**.

   ![](assets/email_rendering_08.png)

   >[!NOTE]
   >
   >The **[!UICONTROL Proof + Email rendering]** option enables you to send a proof and use the email rendering feature simultaneously. Ihre Nachricht wird von den Empfängern des Testversands validiert und gleichzeitig können Sie auch feststellen, wie Ihre Nachricht in der Inbox des Empfängers dargestellt wird. In diesem Fall müssen Sie auch Testprofile mit der Proof-Funktion auswählen. Siehe [Über Testprofile](../../audiences/using/managing-test-profiles.md).

   Der Testversand wird durchgeführt.

1. Die Rendering-Miniaturansichten sind einige Minuten nach dem Versand der Nachrichten verfügbar. To access them, select **[!UICONTROL Proofs]** in the **[!UICONTROL Summary]** drop-down list.

   ![](assets/email_rendering_03.png)

1. Klicken Sie in der **[!UICONTROL Proofs]** Liste auf das **[!UICONTROL Access email rendering]** Symbol.

   ![](assets/email_rendering_04.png)

Der E-Mail-Rendering-Bericht wird angezeigt. Siehe [Beschreibung des E-Mail-Rendering-Berichts](#email-rendering-report-description).

**Verwandte Themen**:

* [E-Mails erstellen](../../channels/using/creating-an-email.md)
* [Testversand durchführen](../../sending/using/sending-proofs.md)
* [Abfrageeditor](../../automating/using/editing-queries.md#about-query-editor)

## Beschreibung des E-Mail-Rendering-Berichts {#email-rendering-report-description}

Dieser Bericht enthält Informationen zum E-Mail-Rendering, d. h. zur Darstellung der E-Mail in der Inbox des Empfängers. E-Mail-Renderings können unterschiedlich aussehen, je nachdem ob die E-Mail in einem Browser, auf einem Mobilgerät oder über eine E-Mail-Anwendung geöffnet wird.

>[!NOTE]
>
>Die Anzahl der verfügbaren Renderings ist in Ihrem Lizenzvertrag vermerkt. Mit jedem Versand, bei dem die Option **E-Mail-Rendering** aktiviert ist, werden Ihre verfügbaren Renderings (auch Token genannt) um eins verringert. Wenn Sie Litmus-Kunde sind, können Sie Ihr eigenes Litmus-Konto für das E-Mail-Rendering in Adobe Campaign verwenden. Weiterführende Informationen dazu erhalten Sie von Ihrem Adobe-Kundenbetreuer.

Die Zusammenfassung des Berichts zeigt die Anzahl an empfangenen, als Spam gekennzeichneten und nicht empfangenen Nachrichten oder die Anzahl an Nachrichten, deren Empfang ausstehend ist.

![](assets/inbox_rendering_report.png)

Der Bericht ist in drei Teile unterteilt: **[!UICONTROL Mobile]**, **[!UICONTROL Messaging clients]** und **[!UICONTROL Webmails]**. Scrollen Sie im Bericht nach unten, um alle in diese drei Kategorien eingeteilten Renderings anzusehen.

![](assets/inbox_rendering_report_3.png)

Klicken Sie auf eine der Karten, um das entsprechende Rendering im Detail anzusehen. Das Rendering wird für das jeweils ausgewählte Empfangsmedium angezeigt.

![](assets/inbox_rendering_report_2.png)

The **[!UICONTROL Technical data]** tab allows you to get more information, such as the receiving and capture dates, and the complete headers of emails.

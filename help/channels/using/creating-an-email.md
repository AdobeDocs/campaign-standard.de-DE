---
title: E-Mails erstellen
seo-title: E-Mails erstellen
description: E-Mails erstellen
seo-description: Diese Schritte zeigen Ihnen, wie Sie einen einmaligen E-Mail-Versand mit Adobe Campaign erstellen können.
page-status-flag: nie aktiviert
uuid: 74 c 7 ef 35-82 c 0-4 bc 4-b 1 f 6-8 e 74 fdcaea 3 c
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Kanäle
content-type: Referenz
topic-tags: E-Email-Nachrichten
discoiquuid: b 27 e 0170-e 73 f -4782-8568-02927 fb 374 f 4
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6df0e764750a31f29d6fe3ec4d92e19b3f07f728

---


# E-Mails erstellen{#creating-an-email}

Die Erstellung von E-Mails erfolgt im Rahmen von [Kampagnen](../../start/using/marketing-activities.md#creating-a-marketing-activity), ausgehend von der [Adobe-Campaign-Startseite](../../start/using/interface-description.md#home-page) oder in der [Liste der Marketingaktivitäten](../../start/using/marketing-activities.md#about-marketing-activities). In Workflows lassen sich ebenfalls E-Mails zum einmaligen oder zum wiederkehrenden Versand erstellen.

1. Erstellen Sie eine neue Marketingaktivität vom Typ E-Mail und wählen Sie die E-Mail-Vorlage aus, die Sie verwenden möchten.

   Für jede Marketingaktivität werden mehrere Standardvorlagen angeboten. Dadurch können Sie bestimmte Parameter nach Bedarf vorkonfigurieren und Ihrem Versand eine Marke zuweisen. Weiterführende Informationen dazu finden Sie im Abschnitt [Marketingaktivitäten-Vorlagen](../../start/using/about-templates.md).

   ![](assets/email_creation_1.png)

   >[!NOTE]
   >
   >Vorlagen für Folgenachrichten und A/B-Tests werden standardmäßig verborgen. Aktivieren Sie die Optionen auf der linken Seite (seitliches Fenster **[!UICONTROL Filter]), um sie anzuzeigen.**

1. Geben Sie die allgemeinen E-Mail-Eigenschaften an. Benennen Sie die Aktivität im Feld **Titel** und passen Sie gegebenenfalls die Kennung an. Titel und Kennung der Aktivität erscheinen in der Benutzeroberfläche, sind jedoch für die Nachrichtenempfänger nicht sichtbar.

   Fügen Sie bei Bedarf eine Beschreibung hinzu. Diese ist im Kampagneninhalt sichtbar.

   ![](assets/email_creation_2.png)

   >[!NOTE]
   >
   >Wenn Sie eine E-Mail von der Startseite oder der Marketingaktivitätenliste ausgehend erstellen, können Sie sie einer bereits existierenden Kampagne zuordnen. Wählen Sie diese unter den bereits existierenden Kampagnen aus.

1. Definieren Sie die Zielgruppe Ihrer Nachricht auf der Basis Ihrer betrieblichen Bedingungen. Siehe [Verwaltung von Profilen](../../audiences/using/about-profiles.md).

   Sie können auch die Testprofile definieren, die die Nachricht überprüfen. Siehe [Verwaltung von Testprofilen](../../sending/using/managing-test-profiles-and-sending-proofs.md#managing-test-profiles).

   ![](assets/email_creation_3.png)

1. Definieren und personalisieren Sie mithilfe von [Email Designer](../../designing/using/about-email-content-design.md#about-the-email-designer) den Nachrichteninhalt, den Namen des Absenders und den Betreff. Weiterführende Informationen dazu finden Sie im Abschnitt [Über die Inhaltserstellung in E-Mails](../../designing/using/about-email-content-design.md).

   ![](assets/email_creation_4.png)

   Die können Ihre Nachricht mit einer vordefinierten Inhaltsvorlage gestalten oder Dreamweaver oder Adobe Experience Manager verwenden. Sie können auch für Sie vorbereitete Inhalte hochladen oder einen vorhandenen Inhalt aus einer URL importieren. Siehe [Existierenden Inhalt auswählen](../../designing/using/selecting-an-existing-content.md).

1. Sehen Sie sich Ihre Nachricht in der Vorschau an. Siehe [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md).
1. Validieren Sie die Erstellung der E-Mail.

   >[!NOTE]
   >
   >Um Ihre E-Mail speichern zu können, müssen Sie zunächst den Inhalt bearbeiten. Wenn Sie jetzt **[!UICONTROL Abbrechen]auswählen, wird der Assistent nicht zu Ende geführt und Ihre E-Mail wird nicht erstellt.**

   Daraufhin wird das Dashboard der E-Mail angezeigt. Lesen Sie diesbezüglich auch den Abschnitt [Nachrichten validieren](../../sending/using/preparing-the-send.md).

   ![](assets/delivery_dashboard_2.png)

1. Terminieren Sie den Versand. Siehe [Versandplanung](../../sending/using/about-scheduling-messages.md).

   ![](assets/delivery_planning.png)

1. Bereiten Sie Ihre Nachricht vor, um ihre Zielgruppe zu analysieren. Siehe [Versandvorbereitung](../../sending/using/confirming-the-send.md).

   ![](assets/preparing_delivery_2.png)

   >[!NOTE]
   >
   >Sie können globale, kanalübergreifende Ermüdungsregeln festlegen, mit denen Profile, die bereits zu oft angesprochen wurden, automatisch von Kampagnen ausgeschlossen werden. Weiterführende Informationen hierzu finden Sie in den [Ermüdungsregeln](../../administration/using/fatigue-rules.md).

1. Führen Sie Testsendungen durch, um Ihre Nachricht zu überprüfen und zu validieren und das Inbox-Rendering zu überprüfen. Siehe [Testversand durchführen](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs).

   ![](assets/bat_select.png)

1. Senden Sie die Nachricht und prüfen Sie die Zustellung über das Nachrichten-Dashboard und die entsprechenden Protokolle. Siehe [Nachrichten senden](../../sending/using/confirming-the-send.md).

   ![](assets/confirm_delivery.png)

1. Messen Sie die Wirksamkeit Ihrer Nachricht mit Versandberichten. Weiterführende Informationen zum Reporting finden Sie in [diesem Abschnitt](../../reporting/using/about-dynamic-reports.md).

**Verwandte Themen**:

* Video [E-Mails erstellen](https://helpx.adobe.com/campaign/kt/acs/using/acs-create-email-from-homepage-feature-video-use.html)
* Schrittweise Anleitung zum [Erstellen einer personalisierten E-Mail](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_GettingStartedEmail.html)
* Video zur [Integration von Adobe Campaign und Dreamweaver](https://helpx.adobe.com/campaign/kt/acs/using/acs-dreamweaver-integration-feature-video-use.html)
* [Integration mit Adobe Experience Manager](../../integrating/using/integrating-with-experience-manager.md)


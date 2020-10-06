---
title: SMS erstellen
description: Diese Schritte zeigen Ihnen, wie Sie einen einmaligen SMS-Versand mit Adobe Campaign erstellen können.
page-status-flag: never-activated
uuid: 591ae97e-2d19-4f93-be4b-d8d20f1d2d12
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: sms-messages
discoiquuid: b27381a9-19e5-4b65-b194-c72f475ba54d
delivercontext-tags: deliveryCreation,wizard
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 9c812b0b622b82ba7aa382f04edb7a2a3f717cd4
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 100%

---


# SMS erstellen{#creating-an-sms-message}

Die Erstellung eines SMS-Versands ist der Erstellung einer üblichen E-Mail sehr ähnlich. Im Folgenden werden die Konfigurationsschritte für diesen Kanal beschrieben. Weiterführende Informationen zu anderen Optionen finden Sie in [E-Mails erstellen](../../channels/using/creating-an-email.md).

Informationen zu erweiterten SMS-Parametern finden Sie im Abschnitt [SMS-Konfiguration](../../administration/using/configuring-sms-channel.md).

Folgende Voraussetzungen müssen gegeben sein, um SMS-Nachrichten an Mobiltelefone senden zu können:

* ein externes Konto vom Typ **[!UICONTROL Routing]**, das für den Kanal **[!UICONTROL Mobiltelefon (SMS)]** mit dem Versandmodus **[!UICONTROL Gebündelter Versand]** konfiguriert wurde. Lesen Sie diesbezüglich auch den Abschnitt [Routing](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing).
* Eine Versandvorlage, die auf das externe Konto Bezug nimmt

1. Erstellen Sie einen SMS-Versand. Ein Versand kann über die Adobe-Campaign-[Startseite](../../start/using/interface-description.md#home-page), im Rahmen einer [Kampagne](../../start/using/marketing-activities.md#creating-a-marketing-activity) oder in der [Liste der Marketingaktivitäten](../../start/using/programs-and-campaigns.md#creating-a-campaign) erstellt werden.

   Es besteht außerdem die Möglichkeit, eine SMS-Aktivität in einem Workflow hinzuzufügen. Weitere Informationen hierzu finden Sie im [Workflow](../../automating/using/sms-delivery.md)-Handbuch.

   Bei der Erstellung einer Nachricht öffnet sich ein Assistent, der Sie durch die wichtigsten Schritte führt. Die im Assistenten vorgenommenen Definitionen können später im Nachrichten-Dashboard geändert werden.

1. Wählen Sie die gewünschte Vorlage aus. Verwenden Sie entweder die Standardvorlage für SMS oder eine Ihrer eigenen Vorlagen.

   ![](assets/sms_creation_1.png)

   Um Nachrichten an Mobiltelefone senden zu können, muss die verwendete Versandvorlage auf das externe SMS-Routing-Konto Bezug nehmen.

1. Geben Sie die allgemeinen Eigenschaften der SMS an.

   ![](assets/sms_creation_2.png)

   Titel und Kennung der Aktivität erscheinen in der Benutzeroberfläche, sind jedoch für die Nachrichtenempfänger nicht sichtbar.

1. Wählen Sie die zu kontaktierende Audience aus. Sie können eine bestehende Audience auswählen oder direkt eine Population erstellen, indem Sie Regeln definieren und kombinieren.

   ![](assets/sms_creation_3.png)

1. Fügen Sie Ihrer SMS Inhalt hinzu. Sie können den Inhalt auch definieren, indem Sie nach Abschluss der SMS-Erstellung den Bereich **[!UICONTROL Inhalt]** des Versand-Dashboards auswählen. Siehe [Über die SMS-Inhaltserstellung](../../channels/using/about-sms-and-push-content-design.md).

   Die Verwendung von Personalisierungsfeldern oder bedingten Texten im SMS-Inhalt kann dazu führen, dass die Nachrichtenlänge je nach Empfänger variiert und dass u. U. nicht von GSM unterstützte Zeichen eingefügt werden. Die Nachrichtenlänge kann daher erst nach erfolgter Personalisierung korrekt eingeschätzt werden. Siehe [SMS personalisieren](../../channels/using/personalizing-sms-messages.md).

   ![](assets/sms_creation_4.png)

1. Validieren Sie die Erstellung der Nachricht. Das Dashboard wird daraufhin angezeigt.
1. Terminieren Sie den Versand. Die SMS kann manuell unmittelbar nach der Vorbereitung der Nachricht oder automatisch zu einem festgelegten Zeitpunkt gesendet werden. Siehe [Versandplanung](../../sending/using/about-scheduling-messages.md).
1. Bereiten Sie die Nachricht vor, um ihre Gültigkeit, Personalisierung und Zielgruppe zu prüfen.

   ![](assets/sms_creation_6.png)

   >[!NOTE]
   >
   >Sie können globale, kanalübergreifende Ermüdungsregeln festlegen, mit denen Profile, die bereits zu oft angesprochen wurden, automatisch von Kampagnen ausgeschlossen werden. Näheres dazu finden Sie unter [Ermüdungsregeln](../../sending/using/fatigue-rules.md).

1. Führen Sie Testsendungen durch, um Ihre Nachricht zu überprüfen und zu validieren und das Inbox-Rendering zu überprüfen; siehe auch den Abschnitt [Testversand durchführen](../../sending/using/sending-proofs.md).
1. Bestätigen Sie den Versand der Nachricht. Der Versand erfolgt an dem von Ihnen festgelegten Zeitpunkt.

   ![](assets/sms_creation_7.png)

Die Nachricht wird gesendet. Sie können die Zustellung über das Nachrichten-Dashboard und die entsprechenden Protokolle prüfen.

Nach Abschluss des Versands können Sie die Wirkung der Nachricht mithilfe integrierter oder benutzerdefinierter Versandberichte messen.

**Verwandte Themen:**

* [Über die Bearbeitung von SMS und Push-Benachrichtigungen](../../channels/using/about-sms-and-push-content-design.md)
* [Marketingaktivitäten-Vorlagen](../../start/using/marketing-activity-templates.md)
* Video [Create an SMS delivery](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/communication-channels/mobile/sms/sms-delivery.html)

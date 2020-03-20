---
title: Definieren der Betreffzeile und des Absenders einer E-Mail
description: Erfahren Sie, wie Sie in Email Designer die Betreffzeile und den Absender einer E-Mail definieren.
page-status-flag: never-activated
uuid: 571ffc01-6e41-4501-9094-2f812b041a10
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-email-content
discoiquuid: 39b86fda-7766-4e5f-ab48-bcc536ab66b3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6f89b420f0f98c13da1bfff8f9b1b29e015aef89

---


# Definieren der Betreffzeile und des Absenders einer E-Mail{#defining-the-subject-line-of-an-email}

## Defining the subject line of an email {#subject-line}

Die Betreffzeile ist für die Vorbereitung und den Versand einer Nachricht unbedingt erforderlich.

>[!NOTE]
>
>Wenn die Betreffzeile leer ist, wird ein Warnhinweis im Nachrichten-Dashboard und in Email Designer angezeigt.

1. Erstellen Sie eine E-Mail.
1. Gehen Sie zur **[!UICONTROL Properties]** Registerkarte &quot;E-Mail-Designer-Startseite&quot;(über das Startsymbol abrufbar).
1. Füllen Sie den **[!UICONTROL Subject]** Abschnitt aus.

   ![](assets/email_designer_subject.png)

1. Sie können zur Betreffzeile auch Personalisierungsfelder, Inhaltsbausteine und dynamische Inhalte hinzufügen, indem Sie die entsprechenden Symbole auswählen. For more on this, see [Personalization](../../designing/using/personalization.md).
1. Sie können verschiedene Betreffzeilen ausprobieren, um eine Schätzung der offenen E-Mail-Rate zu erhalten, bevor Sie sie senden. Weitere Informationen dazu finden Sie unter [Betreffzeile einer E-Mail testen](../../sending/using/testing-subject-line-email.md).

## E-Mail-Absender einer E-Mail definieren {#email-sender}

To define the name of the sender which will appear in the header of messages sent, go the **[!UICONTROL Properties]** tab of the Email Designer home page (accessible through the home icon).

![](assets/delivery_content_edition16.png)

* The **[!UICONTROL From: name]** field allows you to enter the sender name. Wenn nicht anders angegeben, erscheint hier automatisch der **Name des Standard-Absenders**. The default sender email address and sender name are  defined in **[!UICONTROL Brands]** accessible via the Adobe Campaign logo under the advanced menu **[!UICONTROL Administration > Instance settings > Brand configuration]** .

   Sie können den Absendernamen ändern, indem Sie **Name des Absenders** auswählen. Geben Sie nun den gewünschten Absendernamen ein.

   Sie haben die Möglichkeit, den Absendernamen je nach Zielgruppe zu personalisieren. Sie können Personalisierungsfelder, Inhaltsbausteine und dynamische Inhalte hinzufügen, indem Sie die Symbole unter dem Absendernamen auswählen. For more on this, see [Personalization](../../designing/using/personalization.md).

* Das **[!UICONTROL From: email address]** Feld kann in diesem Abschnitt nicht bearbeitet werden. Änderungen der E-Mail-Adresse sind nur über den Eigenschaften-Bildschirm der E-Mail möglich, auf den Sie im Dashboard zugreifen können. Lesen Sie diesbezüglich auch den Abschnitt [Liste der erweiterten E-Mail-Parameter](../../administration/using/configuring-email-channel.md#advanced-parameters).

>[!NOTE]
>
>Header-Parameter dürfen nicht leer sein. Die Angabe der Absenderadresse ist für den E-Mail-Versand zwingend erforderlich (gemäß RFC-Standard). Adobe Campaign führt eine Syntax-Prüfung der angegebenen E-Mail-Adressen durch.

**Verwandte Themen:**

* [Personalisierungsfeld einfügen](../../designing/using/personalization.md#inserting-a-personalization-field)
* [Inhaltsbausteine](../../designing/using/personalization.md#adding-a-content-block)
* [Dynamische Inhalte in einer E-Mail definieren](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)

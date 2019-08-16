---
title: Personalisierung für den Absender einrichten
seo-title: Personalisierung für den Absender einrichten
description: Personalisierung für den Absender einrichten
seo-description: Lernen Sie, wie Sie den Namen oder die Adresse des Absenders Ihrer Nachrichten personalisieren.
page-status-flag: never-activated
uuid: 7aa08d5d-9e6c-4dac-bff8-6fde85368c2d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: personalizing-content
discoiquuid: 49532f6b-3cd0-4d03-932e-bcb7d05c74d4
internal: n
snippet: y
translation-type: ht
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Personalisierung für den Absender einrichten{#personalizing-the-sender}

## E-Mail-Absender {#email-sender}

Um den Absendernamen, der im Kopf der gesendeten Nachrichten erscheint, zu definieren, gehen Sie auf der Startseite von Email Designer zum Tab **[!UICONTROL Eigenschaften]** (der Zugriff erfolgt über das Startseiten-Symbol).

![](assets/delivery_content_edition16.png)

* Der Absendername kann im Feld **[!UICONTROL Von (Name)]** angepasst werden. Wenn nicht anders angegeben, erscheint hier automatisch der **Name des Standard-Absenders**. Dieser wird im Zuge der E-Mail-Kanal-Konfiguration bestimmt. Auf diese können Sie über das Adobe-Campaign-Logo und die Schaltflächen **[!UICONTROL Administration &gt; Kanäle &gt; E-Mail &gt; E-Mail-Konten]** zugreifen.

   Sie können den Absendernamen ändern, indem Sie **Name des Absenders** auswählen. Geben Sie nun den gewünschten Absendernamen ein.

   Sie haben die Möglichkeit, den Absendernamen je nach Zielgruppe zu personalisieren. Sie können Personalisierungsfelder, Inhaltsbausteine und dynamische Inhalte hinzufügen, indem Sie die Symbole unter dem Absendernamen auswählen.

* Das Feld **[!UICONTROL Von (E-Mail)]** kann nicht in diesem Bereich bearbeitet werden. Änderungen der E-Mail-Adresse sind nur über den Eigenschaften-Bildschirm der E-Mail möglich, auf den Sie im Dashboard zugreifen können. Lesen Sie diesbezüglich auch den Abschnitt [Liste der erweiterten E-Mail-Parameter](../../administration/using/configuring-email-channel.md#advanced-parameters).

>[!NOTE]
>
>Header-Parameter dürfen nicht leer sein. Die Angabe der Absenderadresse ist für den E-Mail-Versand zwingend erforderlich (gemäß RFC-Standard). Adobe Campaign führt eine Syntax-Prüfung der angegebenen E-Mail-Adressen durch.

**Verwandte Themen:**

* [Personalisierungsfeld einfügen](../../designing/using/inserting-a-personalization-field.md)
* [Inhaltsbausteine](../../designing/using/adding-a-content-block.md)
* [Dynamische Inhalte in einer E-Mail definieren](../../designing/using/defining-dynamic-content-in-an-email.md)

## SMS-Absender {#sms-sender}

Sie haben die Möglichkeit, den Namen des Absenders von SMS zu personalisieren. Lesen Sie diesbezüglich auch den Abschnitt [SMS-Konfiguration](../../administration/using/configuring-sms-channel.md#configuring-sms-properties).

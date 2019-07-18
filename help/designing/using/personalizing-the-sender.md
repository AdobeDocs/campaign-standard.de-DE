---
title: Personalisierung für den Absender einrichten
seo-title: Personalisierung für den Absender einrichten
description: Personalisierung für den Absender einrichten
seo-description: Lernen Sie, wie Sie den Namen oder die Adresse des Absenders Ihrer Nachrichten personalisieren.
page-status-flag: nie aktiviert
uuid: 7 aa 08 d 5 d -9 e 6 c -4 dac-bff 8-6 fde 85368 c 2 d
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: entwerfen
content-type: Referenz
topic-tags: personalize-content
discoiquuid: 49532 f 6 b -3 cd 0-4 d 03-932 e-bcb 7 d 05 c 74 d 4
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Personalisierung für den Absender einrichten{#personalizing-the-sender}

## E-Mail-Absender {#email-sender}

Um den Absendernamen, der im Kopf der gesendeten Nachrichten erscheint, zu definieren, gehen Sie auf der Startseite von Email Designer zum Tab **[!UICONTROL Eigenschaften](der Zugriff erfolgt über das Startseiten-Symbol).**

![](assets/delivery_content_edition16.png)

* Der Absendername kann im Feld **[!UICONTROL Von (Name)]angepasst werden.** Wenn nicht anders angegeben, erscheint hier automatisch der **Name des Standard-Absenders**. Dieser wird im Zuge der E-Mail-Kanal-Konfiguration bestimmt. Auf diese können Sie über das Adobe-Campaign-Logo und die Schaltflächen **[!UICONTROL Administration &gt; Kanäle &gt; E-Mail &gt; E-Mail-Konten]zugreifen.**

   Sie können den Absendernamen ändern, indem Sie **Name des Absenders** auswählen. Geben Sie nun den gewünschten Absendernamen ein.

   Sie haben die Möglichkeit, den Absendernamen je nach Zielgruppe zu personalisieren. Sie können Personalisierungsfelder, Inhaltsbausteine und dynamische Inhalte hinzufügen, indem Sie die Symbole unter dem Absendernamen auswählen.

* Das Feld **[!UICONTROL Von (E-Mail)]kann nicht in diesem Bereich bearbeitet werden.** Änderungen der E-Mail-Adresse sind nur über den Eigenschaften-Bildschirm der E-Mail möglich, auf den Sie im Dashboard zugreifen können. Lesen Sie diesbezüglich auch den Abschnitt [Liste der erweiterten E-Mail-Parameter](../../administration/using/configuring-email-channel.md#advanced-parameters).

>[!NOTE]
>
>Header-Parameter dürfen nicht leer sein. Die Angabe der Absenderadresse ist für den E-Mail-Versand zwingend erforderlich (gemäß RFC-Standard). Adobe Campaign führt eine Syntax-Prüfung der angegebenen E-Mail-Adressen durch.

**Verwandte Themen:**

* [Personalisierungsfeld einfügen](../../designing/using/inserting-a-personalization-field.md)
* [Inhaltsbausteine](../../designing/using/adding-a-content-block.md)
* [Dynamische Inhalte in einer E-Mail definieren](../../designing/using/defining-dynamic-content-in-an-email.md)

## SMS-Absender {#sms-sender}

Sie haben die Möglichkeit, den Namen des Absenders von SMS zu personalisieren. Lesen Sie diesbezüglich auch den Abschnitt [SMS-Konfiguration](../../administration/using/configuring-sms-channel.md#configuring-sms-properties).

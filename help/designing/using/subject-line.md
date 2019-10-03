---
title: Definieren der Betreffzeile und des Absenders einer E-Mail
seo-title: Definieren der Betreffzeile und des Absenders einer E-Mail
description: Definieren der Betreffzeile und des Absenders einer E-Mail
seo-description: Erfahren Sie, wie Sie in Email Designer die Betreffzeile und den Absender einer E-Mail definieren.
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
source-git-commit: 5847c89b97ede8b03e75d1d90f31c88ed5c8a84e

---


# Definieren der Betreffzeile und des Absenders einer E-Mail{#defining-the-subject-line-of-an-email}

Die Betreffzeile ist für die Vorbereitung und den Versand einer Nachricht unbedingt erforderlich.

>[!NOTE]
>
>Wenn die Betreffzeile leer ist, wird ein Warnhinweis im Nachrichten-Dashboard und in Email Designer angezeigt.

Um den E-Mail-Betreff zu konfigurieren, öffnen Sie auf der Startseite von Email Designer den Tab **[!UICONTROL Eigenschaften]** (der Zugriff erfolgt über das Startseiten-Symbol) und füllen Sie den Bereich **[!UICONTROL Betreff]** aus.

**So definieren Sie die Betreffzeile einer E-Mail**:

1. Erstellen Sie eine E-Mail.
1. Schließen Sie die Startseite.
1. Klicken Sie auf der Startseite von Email Designer, die über das Home-Symbol aufgerufen wird, auf die Registerkarte **[!UICONTROL Eigenschaften]** und füllen Sie den Bereich **[!UICONTROL Betreff]** aus.

![](assets/email_designer_subject.png)

Sie können zur Betreffzeile auch Personalisierungsfelder, Inhaltsbausteine und dynamische Inhalte hinzufügen, indem Sie die entsprechenden Symbole auswählen.

**Verwandte Themen:**

* [Personalisierungsfeld einfügen](../../designing/using/personalization.md#inserting-a-personalization-field)
* [Inhaltsbausteine](../../designing/using/personalization.md#adding-a-content-block)
* [Dynamische Inhalte in einer E-Mail definieren](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)

## Prädiktive Betreffzeile {#predictive-subject-line}

Beim Bearbeiten von E-Mails können Sie verschiedene Betreffzeilen ausprobieren und dabei eine jeweilige Einschätzung der Öffnungsrate erhalten, bevor Sie die E-Mail senden.

Diese Funktion ist standardmäßig deaktiviert. Sie wird beim Import des ersten Modells aktiviert. Bei einem Modell handelt es sich um das Ergebnis aus branchenspezifischen Trainingsdatensätzen. Durch Modelle kann das System bei der Unterbreitung neuer Betreffzeilen darauf bezogene Öffnungsraten für E-Mails voraussagen.

>[!NOTE]
>
>Diese Funktion ist ausschließlich für E-Mail-Nachrichten und Datenbanken mit englischen Inhalten verfügbar. Das trainierte Modell riskiert inkonsistent zu sein und fehlerhafte Ergebnisse zu erzeugen, wenn Ihre Instanz E-Mails beinhaltet, deren Inhalt in anderen Sprachen gehalten ist. Die Option zum Testen von Betreffs ist nur dann sichtbar, wenn in Ihrer Instanz bereits ein Modell verfügbar ist.

**Verwandtes Thema**

* [Betreffzeile einer E-Mail testen](../../sending/using/testing-subject-line-email.md)

## E-Mail-Absender {#email-sender}

Um den Absendernamen, der im Kopf der gesendeten Nachrichten erscheint, zu definieren, gehen Sie auf der Startseite von Email Designer zum Tab **[!UICONTROL Eigenschaften]** (der Zugriff erfolgt über das Startseiten-Symbol).

![](assets/delivery_content_edition16.png)

* Der Absendername kann im Feld **[!UICONTROL Von (Name)]** angepasst werden. Wenn nicht anders angegeben, erscheint hier automatisch der **Name des Standard-Absenders**. Dieser wird im Zuge der E-Mail-Kanal-Konfiguration bestimmt. Auf diese können Sie über das Adobe-Campaign-Logo und die Schaltflächen **[!UICONTROL Administration &gt; Kanäle &gt; E-Mail &gt; E-Mail-Konten]** zugreifen.

   Sie können den Absendernamen ändern, indem Sie **Name des Absenders** auswählen. Geben Sie nun den gewünschten Absendernamen ein.

   Sie haben die Möglichkeit, den Absendernamen je nach Zielgruppe zu personalisieren. Sie können Personalisierungsfelder, Inhaltsbausteine und dynamische Inhalte hinzufügen, indem Sie die Symbole unter dem Absendernamen auswählen.

* Das Feld **[!UICONTROL Von (E-Mail)]** kann nicht in diesem Bereich bearbeitet werden. Änderungen der E-Mail-Adresse sind nur über den Eigenschaften-Bildschirm der E-Mail möglich, auf den Sie im Dashboard zugreifen können. For more information, see [List of email advanced parameters](../../administration/using/configuring-email-channel.md#advanced-parameters).

>[!NOTE]
>
>Header-Parameter dürfen nicht leer sein. Die Angabe der Absenderadresse ist für den E-Mail-Versand zwingend erforderlich (gemäß RFC-Standard). Adobe Campaign führt eine Syntax-Prüfung der angegebenen E-Mail-Adressen durch.

**Verwandte Themen:**

* [Personalisierungsfeld einfügen](../../designing/using/personalization.md#inserting-a-personalization-field)
* [Inhaltsbausteine](../../designing/using/personalization.md#adding-a-content-block)
* [Dynamische Inhalte in einer E-Mail definieren](../../designing/using/personalization.md#defining-dynamic-content-in-an-email)

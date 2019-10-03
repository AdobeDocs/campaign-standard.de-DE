---
title: 'Text- und HTML-Modus    '
seo-title: 'Text- und HTML-Modus    '
description: 'Text- und HTML-Modus    '
seo-description: Entdecken Sie den Plain Text- und den HTML-Modus
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
translation-type: ht
source-git-commit: 2045c69398902a8e942e20c70287d7f3e9570837

---


# Text- und HTML-Modus      {#plain-text-and-html-modes}

## Textversion der E-Mail erstellen {#generating-a-text-version-of-the-email}

Standardmäßig wird eine **[!UICONTROL reine Textversion]** Ihrer E-Mail automatisch erzeugt und mit der **[!UICONTROL bearbeiteten]** Version synchronisiert.

Auch die zur HTML-Version hinzugefügten Personalisierungsfelder und Inhaltsbausteine werden mit der Textversion synchronisiert.

>[!NOTE]
>
>Um Inhaltsbausteine in der Textversion verwenden zu können, dürfen sie keinen HTML-Code enthalten.

Um eine Textversion zu erhalten, die anders ist als die HTML-Version, deaktivieren Sie die Synchronisation, indem Sie den Schalter **[!UICONTROL Mit HTML synchronisieren]** in der **[!UICONTROL Nur Text]**-Ansicht Ihrer E-Mail auswählen.

![](assets/email_designer_textversion.png)

Sie können dann die Textversion nach Bedarf bearbeiten.

>[!NOTE]
>
>Wenn Sie die **[!UICONTROL Nur Text]**-Version bei deaktivierter Synchronisation bearbeiten, werden das nächste Mal, wenn Sie die Option **[!UICONTROL Mit HTML synchronisieren]** aktivieren, alle Änderungen, die Sie in der Textversion vorgenommen haben, durch die HTML-Version ersetzt. Die Änderungen, die Sie in der **[!UICONTROL Nur Text]**-Ansicht vorgenommen haben, werden in der **[!UICONTROL HTML]**-Ansicht nicht dargestellt.

## Die Inhaltsquelle einer E-Mail in HTML bearbeiten {#editing-an-email-content-source-in-html}

Für fortgeschrittene Benutzer und zur Fehlerbehebung kann der E-Mail-Inhalt direkt im HTML-Format angezeigt und bearbeitet werden.

Es gibt zwei Möglichkeiten, die HTML-Version der E-Mail zu bearbeiten:

* Wählen Sie **[!UICONTROL Bearbeiten]** &gt; **[!UICONTROL HTML]** aus, um die HTML-Version der gesamten E-Mail aufzurufen.

   ![](assets/email_designer_html1.png)

* Wählen Sie in der WYSIWYG-Benutzeroberfläche ein Element aus und danach das Symbol **[!UICONTROL Quellcode]**.

   Nur der Quellcode des ausgewählten Elements wird angezeigt. Sie können den Quellcode bearbeiten, wenn das ausgewählte Element eine **[!UICONTROL HTML]**-Inhaltskomponente ist. Andere Komponenten sind schreibgeschützt, können aber in der vollständigen HTML-Version der E-Mail bearbeitet werden.

   ![](assets/email_designer_html2.png)

Wenn Sie den HTML-Code ändern, könnte es sein, dass Ihre E-Mails nicht mehr responsiv sind. Deshalb sollten Sie diese Funktion unbedingt unter Verwendung der Schaltfläche **[!UICONTROL Vorschau]** testen. Siehe [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md).

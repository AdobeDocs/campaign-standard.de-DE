---
title: 'Konvertieren der E-Mail aus dem älteren Editor in den E-Mail-Designer '
description: Erfahren Sie, wie Sie E-Mails verwenden, die im Legacy-Editor erstellt wurden E-Mail an den E-Mail-Designer.
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
source-git-commit: 1de0f5362f3c77fec4b66e330a2d2723f4a0f212

---


# Konvertieren von E-Mail-Inhalten des alten Editors {#converting-an-html-content}

Beginn, der mit dem E-Mail-Designer arbeitet, und erstellen wiederverwendbare Vorlagen und Fragmente aus Ihrem E-Mail-HTML-Code, der im Legacy-Editor erstellt wurde.

In diesem Anwendungsfall können Sie eine E-Mail-Designer-Vorlage erstellen, indem Sie eine HTML-E-Mail verwenden und sie in HTML-Komponenten im E-Mail-Designer aufteilen.

>[!CAUTION]
>
>Dieser Abschnitt richtet sich an Benutzer mit fortgeschrittenen HTML-Kenntnissen.

>[!NOTE]
>
>Wie im Kompatibilitätsmodus ist eine HTML-Komponente nur beschränkt bearbeitbar: Sie kann nur an Ort und Stelle bearbeitet werden.

## Vorbereiten des E-Mail-Inhalts

1. Wählen Sie eine HTML-E-Mail aus.
1. Identifizieren Sie die Abschnitte, die die HTML-E-Mail unterteilen sollen.
1. Schneiden Sie die verschiedenen Blöcke aus Ihrem HTML-Code aus.

## E-Mail-Struktur erstellen

1. Open the **[!UICONTROL Email Designer]**  to create an empty email content.
1. Legen Sie die Attribute für den Hauptteil fest: Hintergrundfarben, Breite etc. Weiterführende Informationen dazu finden Sie im Abschnitt [E-Mail-Stile bearbeiten](../../designing/using/styles.md).
1. Hinzufügen Sie so viele Strukturkomponenten wie Abschnitte. Weiterführende Informationen dazu finden Sie im Abschnitt zum [Bearbeiten des E-Mail-Aufbaus](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

## HTML-Inhalt Hinzufügen

1. Hinzufügen jeder Strukturkomponente eine HTML-Komponente. Weiterführende Informationen dazu finden Sie im Abschnitt [Fragmente und Inhaltskomponenten hinzufügen](../../designing/using/designing-from-scratch.md#defining-the-email-structure).
1. Kopieren Sie den HTML-Code in jede Komponente.

## Verwalten des Stils Ihrer E-Mail {#manage-the-style-of-your-email}

1. Switch to **[!UICONTROL Mobile view]**. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../designing/using/plain-text-html-modes.md#switching-to-mobile-view).

1. Um dieses Problem zu beheben, wechseln Sie zum Quellcode-Modus und kopieren Sie Ihren CSS-Abschnitt in einen neuen CSS-Abschnitt. Beispiel:

   ```
   <style type="text/css">
   a {text-decoration:none;}
   body {min-width:100% !important; margin:0 auto !important; padding:0 !important;}
   img {line-height:100%; text-decoration:none; -ms-interpolation-mode:bicubic;}
   ...
   </style>
   ```

   >[!NOTE]
   >
   >Stellen Sie sicher, dass Sie Ihren Stil nach diesem Abschnitt in einem anderen CSS-Tag hinzufügen.
   >
   >Verändern Sie das von Email Designer erzeugte CSS nicht:
   >
   >* `<style data-name="default" type="text/css">(##)</style>`
   >* `<style data-name="supportIOS10" type="text/css">(##)</style>`
   >* `<style data-name="mediaIOS8" type="text/css">(##)</style>`
   >* `<style data-name="media-default-max-width-500px" type="text/css">(##)</style>`
   >* `<style data-name="media-default--webkit-min-device-pixel-ratio-0" type="text/css">(##)</style>`


1. Kehren Sie zur mobilen Ansicht zurück und prüfen Sie, ob Ihr Inhalt korrekt angezeigt wird, und speichern Sie Ihre Änderungen.

## Anwendungsbeispiel

Versuchen wir, diese E-Mail, die im Legacy-Editor erstellt wurde, in eine **[!UICONTROL Email Designer]** Vorlage zu konvertieren.

## Identifizieren Sie den Abschnitt Ihrer E-Mail.

Wir können 11 Abschnitte in dieser E-Mail identifizieren.

![](assets/html-dce-view-mail.png)

Um zu ermitteln, welches Element welcher Abschnitt des HTML-Codes ist, können Sie es auswählen.

![](assets/breadcrumbs.png)

Um die HTML-Version der E-Mail anzuzeigen, klicken Sie auf **[!UICONTROL Show source]**.

### E-Mail-Vorlage und deren Struktur erstellen

1. Ziehen Sie per Drag &amp; Drop **[!UICONTROL Structure Components]** das Layout unserer E-Mail.

Wir müssen elf Strukturkomponenten erstellen.

![](assets/structure-components-migration.png)

### Einfügen von HTML-Inhaltskomponenten

1. Fügen Sie eine **[!UICONTROL HTML component]** in jede ein **[!UICONTROL structure component]** .

![](assets/html-components.png)

1. Klicken Sie für jeden Abschnitt auf **[!UICONTROL Show source code]** .

![](assets/show-source-code.png)

1. Fügen Sie den HTML-Abschnitt ein.

1. Klicks **[!UICONTROL Save]**.

Sie können nun die Wiedergabe Ihrer E-Mail überprüfen.

![](assets/migrated-email-result.png)

### Verwalten von Stilen für die mobile Ansicht

Fügen Sie CSS-Elemente ein, um sicherzustellen, dass Ihre E-Mail für die mobile Ansicht geeignet ist.

1. Wechseln Sie zum Quellcode und kopieren Sie den Stilabschnitt in einen neuen Stilabschnitt.

Weitere Informationen finden Sie unter [Verwalten des Stils Ihrer E-Mail](#manage-the-style-of-your-email).

Ihre veraltete E-Mail-Adresse ist jetzt im E-Mail-Designer verfügbar.
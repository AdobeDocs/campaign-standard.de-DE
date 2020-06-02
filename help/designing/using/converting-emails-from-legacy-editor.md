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
source-git-commit: bb83fb3b24af0102dc3745517e8604fdac82ee19
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 26%

---


# Konvertieren von E-Mail-Inhalten des alten Editors {#converting-an-html-content}

Beginn, der mit dem E-Mail-Designer arbeitet, und erstellen wiederverwendbare Vorlagen und Fragmente aus Ihrem E-Mail-HTML-Code, der im Legacy-Editor erstellt wurde.

In diesem Anwendungsfall können Sie eine E-Mail-Designer-Vorlage erstellen, indem Sie eine HTML-E-Mail verwenden und sie in HTML-Komponenten im E-Mail-Designer aufteilen.

>[!NOTE]
>
>Wie der Kompatibilitätsmodus kann eine HTML-Komponente mit eingeschränkten Optionen bearbeitet werden: Sie können nur eine ersetzende Ausgabe durchführen.

>[!IMPORTANT]
>
>Dieser Abschnitt richtet sich an Benutzer mit fortgeschrittenen HTML-Kenntnissen.

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

Versuchen wir, diese E-Mail, die im Legacy-Editor erstellt wurde, in eine **[!UICONTROL E-Mail-Designer]** -Vorlage zu konvertieren.

## Identifizieren Sie den Abschnitt Ihrer E-Mail.

Wir können 11 Abschnitte in dieser E-Mail identifizieren.

![](assets/html-dce-view-mail.png)

Um zu ermitteln, welches Element welcher Abschnitt des HTML-Codes ist, können Sie es auswählen.

![](assets/breadcrumbs.png)

Um die HTML-Version der E-Mail anzuzeigen, klicken Sie auf Quelle **[!UICONTROL anzeigen]**.

### E-Mail-Vorlage und deren Struktur erstellen

1. Ziehen Sie **[!UICONTROL Strukturkomponenten]** , die das Layout unserer E-Mail widerspiegeln.

1. Wiederholen Sie diese Schritte nach Bedarf. Wir müssen elf Strukturkomponenten erstellen.

   ![](assets/structure-components-migration.png)

### Einfügen von HTML-Inhaltskomponenten

1. Fügen Sie eine **[!UICONTROL HTML-Komponente]** in jede **[!UICONTROL Strukturkomponente]** ein.

   ![](assets/html-components.png)

1. Klicken Sie für jeden Abschnitt auf Quellcode **[!UICONTROL anzeigen]** .

   ![](assets/show-source-code.png)

1. Fügen Sie den HTML-Abschnitt ein.

1. Wählen Sie **[!UICONTROL Speichern]** aus.

Sie können nun die Wiedergabe Ihrer E-Mail überprüfen.

![](assets/migrated-email-result.png)

### Verwalten von Stilen für die mobile Ansicht

1. Fügen Sie CSS-Elemente ein, um sicherzustellen, dass Ihre E-Mail für die mobile Ansicht geeignet ist.

1. Wechseln Sie zum Quellcode und kopieren Sie den Stilabschnitt in einen neuen Stilabschnitt.

Weitere Informationen finden Sie unter [Verwalten des Stils Ihrer E-Mail](#manage-the-style-of-your-email).

Ihre veraltete E-Mail-Adresse ist jetzt im E-Mail-Designer verfügbar.
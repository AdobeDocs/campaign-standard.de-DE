---
title: Kurzanleitung zum Erstellen von E-Mail-Inhalten
seo-title: Kurzanleitung zum Erstellen von E-Mail-Inhalten
description: Kurzanleitung zum Erstellen von E-Mail-Inhalten
seo-description: Beginnen Sie in Email Designer mit dem Erstellen von E-Mail-Inhalten.
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
source-git-commit: 8e070a4c364c8a5e23870e28add142b46edc8994

---

# Kurzanleitung zum Erstellen von E-Mail-Inhalten{#quick-start}

Email Designer bietet vier Möglichkeiten zum Erstellen von E-Mails.

Sie können eine E-Mail von Grund auf neu erstellen:

* Sie können die E-Mail von Grund auf neu von einer leeren Arbeitsfläche erstellen. Hierzu fügen Sie Struktur- und Inhaltskomponenten hinzu und personalisieren deren Inhalt. Die E-Mail ist dann rasch versendet. Die Stilelemente können Sie auch vollständig verwalten. Weitere Informationen finden Sie in der [Kurzanleitung](#from-scratch-email) oder in der [vollständigen Dokumentation](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).

* Sie können eine E-Mail aus einer vordefinierten Vorlage erstellen. Hierzu wählen Sie die Vorlage aus und erstellen daraus Ihren neuen E-Mail-Inhalt. [Mehr dazu](#building-content-from-an-out-of-the-box-template)

Sie können eine E-Mail auch aus vorhandenem Inhalt erstellen.

* Hierzu konvertieren Sie bestehenden HTML-Inhalt, der extern oder im Legacy-Editor erstellt wurde. [Mehr dazu](#converting-an-html-content)
* Im Kompatibilitätsmodus können Sie vorhandenen HTML-Inhalt sofort importieren. [Mehr dazu](#compatibility-mode)

## Ohne vorhandenen Inhalt {#without-existing-content}

### E-Mail neu erstellen {#from-scratch-email}

Sie können eine E-Mail problemlos neu erstellen, ihr Komponenten hinzufügen und deren Inhalt personalisieren. Die E-Mail ist dann rasch versendet. Bei Bedarf können Sie die Stiloptionen an den Inhalt anpassen. Weiterführende Informationen zur Verwaltung von Stileinstellungen und Inline-Attributen finden Sie im Abschnitt [E-Mail-Stile bearbeiten](../../designing/using/styles.md).

### Hinzufügen einer Betreffzeile {#add-a-subject-line}

Die Betreffzeile ist in einer E-Mail obligatorisch. Weitere Informationen finden Sie unter [Definieren der Betreffzeile einer E-Mail](../../designing/using/subject-line.md).

1. Erstellen Sie eine E-Mail.
1. Schließen Sie die Startseite.
1. Klicken Sie auf der Startseite von Email Designer, die über das Home-Symbol aufgerufen wird, auf die Registerkarte **[!UICONTROL Eigenschaften]** und füllen Sie den Bereich **[!UICONTROL Betreff]** aus.

![](assets/subject-line-quick-start.png)

### Hinzufügen von Strukturkomponenten {#add-structure-components}

Strukturkomponenten definieren das Layout Ihrer E-Mail. Weitere Informationen finden Sie unter [Definieren der E-Mail-Struktur](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

Ziehen Sie die Strukturkomponenten, die Sie für Ihr Layout wünschen, auf die Arbeitsfläche.

>[!NOTE]
>
>Sie können für Ihre E-Mail verschiedene Inhaltslayouts auswählen.

![](assets/structure-components-quick-start.png)

### Hinzufügen von Inhaltskomponenten {#add-content-components}

Sie können Ihrer E-Mail verschiedene Inhaltskomponenten wie Bild, Text und Schaltflächen hinzufügen. Weitere Informationen finden Sie unter [Inhaltskomponenten](../../designing/using/designing-from-scratch.md#about-content-components).

* Bild

1. Ziehen Sie aus **Inhaltskomponenten** die Bildkomponente in eine Ihrer Strukturkomponenten.
1. Klicken Sie auf **Durchsuchen**.
1. Wählen Sie die gewünschte Bilddatei aus Ihrem Dateisystem aus.

![](assets/browse-image-quick-start.png)

* Text mit Personalisierung

1. Ziehen Sie aus **Inhaltskomponenten** die Textkomponente in eine Ihrer Strukturkomponenten.
1. Klicken Sie auf die Komponente und geben Sie den gewünschten Text ein.
1. Zum Hinzufügen eines Personalisierungsfelds klicken Sie in der Symbolleiste auf **Personalisierungsfeld einfügen**.
1. Wählen Sie das gewünschte Feld aus, zum Beispiel „Vorname“.

![](assets/edit-text-quick-start.png)

* HTML

1. Ziehen Sie aus **Inhaltskomponenten** die HTML-Komponente in eine Ihrer Strukturkomponenten.
1. Klicken Sie auf **Quellcode anzeigen**.
1. Geben Sie den gewünschten HTML-Inhalt ein.
1. Wählen Sie **Speichern** aus.

![](assets/html-component-source-code.png)

Wenn Sie HTML-Kenntnisse haben, können Sie den HTML-Code mit der **[!UICONTROL HTML]**-Inhaltskomponente aus der Original-Fußzeile kopieren und einfügen. Weiterführende Informationen dazu finden Sie im Abschnitt [Über Inhaltskomponenten](../../designing/using/designing-from-scratch.md#about-content-components).

![](assets/des_loading_compatible_fragment_9.png)

### Gestalten Ihrer E-Mail-Komponente

Sie können das Design Ihrer E-Mail anpassen, beispielsweise den Abstand einer Komponente ändern. Weiterführende Informationen zur Verwaltung von Stileinstellungen und Inline-Attributen finden Sie im Abschnitt [E-Mail-Stile bearbeiten](../../designing/using/styles.md).

1. Klicken Sie auf die **Textkomponente**.
1. Navigieren Sie rechts in der Palette zu **Abstand**.
1. Klicken Sie auf das Sperrsymbol, um die Synchronisierung zwischen den Parametern oben und unten oder rechts und links aufzuheben.
1. Passen Sie den **Abstand** nach Bedarf an.
1. Wählen Sie **Speichern** aus.

![](assets/padding-quick-start.png)

Sie können Ihre E-Mail nun speichern und senden.

### Erstellen von Inhalt aus einer vordefinierten Vorlage  {#building-content-from-an-out-of-the-box-template}

Ihre E-Mails können Sie auch aus vordefinierten Vorlagen erstellen und diese personalisieren. Hier bieten sich zum Beispiel Willkommensnachrichten für Neukunden, Newsletter und Wiedereinstellungs-E-Mails an.

1. Erstellen Sie eine E-Mail und öffnen Sie ihren Inhalt. Weiterführende Informationen dazu finden Sie im Abschnitt [E-Mails erstellen](../../channels/using/creating-an-email.md).
1. Wählen Sie das Startseiten-Symbol aus, um die Startseite von **[!UICONTROL Email Designer]** zu öffnen.
1. Wählen Sie den Tab **[!UICONTROL Vorlagen]** aus.
1. Wählen Sie eine native HTML-Vorlage aus.
Die unterschiedlichen Vorlagen bestehen aus Kombinationen verschiedener Typen von Elementen. Beispielsweise haben die Vorlagen vom Typ "Feather" Ränder, die Vorlagen vom Typ "Astro" haben dagegen keine. Weiterführende Informationen dazu finden Sie im Abschnitt [Inhaltsvorlagen](../../designing/using/using-reusable-content.md#content-templates).
1. Klicken Sie auf der Startseite von Email Designer, die über das Home-Symbol aufgerufen wird, auf die Registerkarte **[!UICONTROL Eigenschaften]** und füllen Sie den Bereich **[!UICONTROL Betreff]** aus.
1. Sie können diese Elemente zu mehreren E-Mail-Varianten kombinieren. Beispielsweise können Sie einen Teil einer E-Mail duplizieren, indem Sie eine Strukturkomponente markieren und in der dedizierten Symbolleiste **[!UICONTROL Duplizieren]** auswählen.
1. Sie können die Elemente mit den blauen Pfeilen auf der linken Seite verschieben, indem Sie eine Strukturkomponente unter oder über eine andere ziehen. Weiterführende Informationen dazu finden Sie im Abschnitt zum [Bearbeiten des E-Mail-Aufbaus](../../designing/using/designing-from-scratch.md#defining-the-email-structure).
1. Sie können Komponenten auch verschieben und so die Anordnung in jedem Strukturelement ändern. Weiterführende Informationen dazu finden Sie im Abschnitt [Fragmente und Inhaltskomponenten hinzufügen](../../designing/using/designing-from-scratch.md#defining-the-email-structure).
1. Sie können den Inhalt jedes Elements nach Bedarf ändern: Bilder, Text, Links.
1. Sie können auch die Stiloptionen beliebig auf Ihren Inhalt anpassen. Weiterführende Informationen dazu finden Sie im Abschnitt [E-Mail-Stile bearbeiten](../../designing/using/styles.md).

## Aus vorhandenem Inhalt {#with-existing-content}

Wenn Sie sich selbst ein Rahmenwerk aus modularen Vorlagen und Fragmenten erstellen möchten, um sie in künftigen E-Mails wiederzuverwenden und zu kombinieren, sollten Sie Ihre E-Mail-HTML-Inhalte in Email Designer-Vorlagen konvertieren.

### Konvertieren von HTML-Inhalt  {#converting-an-html-content}

In diesem Anwendungsbeispiel erfahren Sie, wie Sie eine HTML-E-Mail rasch in Email Designer-Komponenten konvertieren können.

>[!CAUTION]
>
>Dieser Abschnitt richtet sich insbesondere an Benutzer, die mit HTML-Code vertraut sind.

>[!NOTE]
>
>Wie im Kompatibilitätsmodus ist eine HTML-Komponente nur beschränkt bearbeitbar: Sie kann nur an Ort und Stelle bearbeitet werden.

Achten Sie darauf, dass der ursprüngliche HTML-Code außerhalb von Email Designer in wiederverwendbare Bereiche unterteilt ist.

1. Öffnen Sie Email Designer, um leeren E-Mail-Inhalt zu erstellen.
1. Legen Sie die Attribute für den Hauptteil fest: Hintergrundfarben, Breite etc. Weiterführende Informationen dazu finden Sie im Abschnitt [E-Mail-Stile bearbeiten](../../designing/using/styles.md).

Ist dies nicht der Fall, schneiden Sie die unterschiedlichen Bestandteile aus Ihrem HTML-Code aus. Dies hier ist zum Beispiel ein eindeutig identifizierbarer Abschnitt:

```
<!-- 3 COLUMN w/CTA (SCALED) -->
<table width="100%" align="center" cellspacing="0" cellpadding="0" border="0" role="presentation" style="max-width:680px;">
<tbody>
<tr>
<td class="padh10" align="center" valign="top" style="padding:0 5px 20px 5px;">
<table width="100%" cellspacing="0" cellpadding="0" border="0" role="presentation">
<tbody>
<tr>
...
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>
<!-- //3 COLUMN w/CTA (SCALED) -->
```

Sobald Sie alle Bestandteile identifiziert haben, wiederholen Sie in Email Designer folgenden Vorgang für jeden Teil Ihrer vorhandenen E-Mail:

1. Fügen Sie eine Strukturkomponente hinzu. Weiterführende Informationen dazu finden Sie im Abschnitt zum [Bearbeiten des E-Mail-Aufbaus](../../designing/using/designing-from-scratch.md#defining-the-email-structure).
1. Fügen Sie eine HTML-Komponente hinzu. Weiterführende Informationen dazu finden Sie im Abschnitt [Fragmente und Inhaltskomponenten hinzufügen](../../designing/using/designing-from-scratch.md#defining-the-email-structure).
1. Fügen Sie Ihren HTML-Code mit Copy &amp; Paste in diese Komponente ein.
1. Zur Mobile-Ansicht wechseln. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../designing/using/styles.md#switching-to-mobile-view).

   Die responsive Ansicht ist fehlerhaft, da Ihr CSS fehlt.

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

### Importieren und Bearbeiten einer HTML-E-Mail {#compatibility-mode}

Beim Hochladen von Inhalt muss dieser ein bestimmtes Tagging aufweisen, um vollständig kompatibel und im WYSIWYG-Editor von Email Designer bearbeitbar zu sein.

Wenn die hochgeladenen HTML-Datei oder Teile davon nicht mit dem Tagging kompatibel ist, wird der Inhalt im so genannten Kompatibilitätsmodus geladen, in dem die Bearbeitungsmöglichkeiten über die Benutzeroberfläche eingeschränkt sind.

Im Kompatibilitätsmodus können Sie die folgenden Änderungen über die Benutzeroberfläche vornehmen (nicht verfügbare Aktionen sind verborgen):

* Ändern des Textes oder eines Bildes
* Einfügen von Links und Personalisierungsfeldern
* Bearbeiten einiger Stiloptionen im ausgewählten HTML-Baustein
* Definieren von bedingten Inhalten

![](assets/email_designer_compatibility.png)

Sonstige Änderungen, wie etwa das Hinzufügen neuer Bereiche zu Ihrer E-Mail oder deren zusätzliche Gestaltung, müssen direkt im Quellcode der E-Mail im HTML-Modus vorgenommen werden.
Im Kompatibilitätsmodus ist die Verwendung von Drag &amp; Drop zwar nicht möglich, jedoch bietet dieser Modus die gleichen Funktionen wie der Legacy-Editor.

Weiterführende Informationen zur Konvertierung einer vorhandenen E-Mail in eine mit Email Designer kompatible E-Mail finden Sie in [diesem Abschnitt](../../designing/using/using-existing-content.md).

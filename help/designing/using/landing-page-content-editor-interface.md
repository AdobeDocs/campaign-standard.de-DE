---
title: Benutzeroberfläche des Inhaltseditors für Landingpages
seo-title: Benutzeroberfläche des Inhaltseditors für Landingpages
description: Benutzeroberfläche des Inhaltseditors für Landingpages
seo-description: Hier erfahren Sie, wie Sie den Inhalt der Landingpage mit den unterschiedlichen Bereichen des Editors, wie z. B. der Symbolleiste, bearbeiten können.
page-status-flag: never-activated
uuid: 53729a68-eed2-4c5d-bc14-02c80e897c44
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-landing-page-content
discoiquuid: 08e2bbda-e409-467f-b462-d74256dc6ebc
internal: n
snippet: y
translation-type: ht
source-git-commit: 76c3d473f6cc7e825fdabadeec2405cb5c13abd1

---


# Benutzeroberfläche des Inhaltseditors für Landingpages{#landing-page-content-editor-interface}

Mit dem Landingpage-Inhaltseditor können Sie mühelos Inhalte in Adobe Campaign definieren, ändern und personalisieren. Um ihn zu öffnen, klicken Sie in den **[!UICONTROL Inhaltsbaustein]** in einem Landingpage-Dashboard.

Der Inhaltseditor besteht aus drei Bereichen. In diesen Bereichen können Sie den Inhalt ansehen und bearbeiten.

![](assets/des_lp_content_8.png)

1. Die **Palette** links im Bildschirm ermöglicht die Bearbeitung der Eigenschaften des markierten Blocks, wie z. B. Hintergrundfarbe, Rahmen, Ausrichtung, Sichtbarkeitsbedingungen etc. Siehe [Personalisierungsfelder einfügen](../../designing/using/inserting-a-personalization-field.md).
1. In der **Symbolleiste** bieten Schaltflächen Zugriff auf die verfügbaren Aktionen. Sie können eine Vorlage auswählen und den Anzeigemodus wechseln. Siehe [Symbolleiste des Inhaltseditors für Landingpages](../../designing/using/landing-page-content-editor-interface.md#landing-page-editor-action-bar).
1. Im **Hauptarbeitsbereich** ermöglicht eine kontextabhängige Symbolleiste die direkte Bearbeitung des Inhalts. Sie können beispielsweise ein Bild mit einem Link belegen, die Schriftart anpassen, ein Feld löschen etc. Siehe [Symbolleiste des Inhaltseditors für Landingpages](../../designing/using/landing-page-content-editor-interface.md#landing-page-editor-toolbar).

## Symbolleiste des Inhaltseditors für Landingpages  {#landing-page-editor-action-bar}

Die Symbolleiste enthält Schaltflächen, die die Bearbeitung des angezeigten Inhalts ermöglichen.

![](assets/des_lp_content_9.png)

<table> 
 <thead> 
  <tr> 
   <th> Symbol<br /> </th> 
   <th> Schaltflächenname<br /> </th> 
   <th> Kanal<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <img height="21px" src="assets/download_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Inhalt wechseln</span> <br /> </td> 
   <td> Landingpage und E-Mail<br /> </td> 
   <td> Ermöglicht die Auswahl einer nativen Inhaltsvorlage oder den Import eines anderweitig erstellten HTML-Inhalts. Lesen Sie diesbezüglich auch den Abschnitt <a href="../../designing/using/selecting-an-existing-content.md">Existierenden Inhalt laden</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/undo_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Rückgängig</span> <br /> </td> 
   <td> Alle<br /> </td> 
   <td> Macht die letzte Aktion rückgängig.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/redo_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Wiederherstellen</span> <br /> </td> 
   <td> Alle<br /> </td> 
   <td> Stellt die letzte rückgängig gemachte Aktion wieder her.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/display_block_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Blöcke anzeigen</span> <br /> </td> 
   <td> Landingpage und E-Mail<br /> </td> 
   <td> Umrandet alle Inhaltsblöcke (entspricht in HTML dem <strong>&lt;div&gt;</strong>-Tag).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/code_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Quelle ansehen</span> <br /> </td> 
   <td> Landingpage und E-Mail<br /> </td> 
   <td> Zeigt den HTML-Quellcode der Seite an.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Symbolleiste des Inhaltseditors für Landingpages  {#landing-page-editor-toolbar}

Die dedizierte Symbolleiste ist ein **kontextuelles Element** der Editor-Oberfläche. Je nach markiertem Bereich sind unterschiedliche Schaltflächen verfügbar. Sie enthält Aktionsschaltflächen sowie Schaltflächen zur Anpassung des Textstils. Alle Änderungen beziehen sich somit jeweils nur auf das ausgewählte Element. Wenn Sie beispielsweise einen Block markieren, können Sie diesen löschen oder duplizieren. Wenn Sie Text innerhalb eines Blocks markieren, können Sie ihn in einen Link verwandeln oder die Formatierung anpassen.

![](assets/delivery_content_17.png)

>[!CAUTION]
>
>Gewisse Funktionen der Schaltfläche betreffen die Formatierung des HTML-Inhalts. Wenn die betroffene Seite jedoch ein CSS-Stylesheet enthält, können sich die **Anweisungen** des Stylesheets als **vorrangig** erweisen.

<table> 
 <thead> 
  <tr> 
   <th> Symbol<br /> </th> 
   <th> Schaltflächenname<br /> </th> 
   <th> Kontext<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <img height="21px" src="assets/link_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Link zu einer externen URL</span> <br /> </td> 
   <td> Jegliches Element<br /> </td> 
   <td> Verlinkt mit einer URL. Weiterführende Informationen zur Konfiguration eines Links finden Sie im Abschnitt <a href="../../designing/using/inserting-a-link.md">Link einfügen</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/linkpage_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Link zu einer Landingpage</span> <br /> </td> 
   <td> Jegliches Element<br /> </td> 
   <td> Ermöglicht den Zugriff auf eine Adobe-Campaign-Landingpage. Weiterführende Informationen zur Konfiguration eines Links finden Sie im Abschnitt <a href="../../designing/using/inserting-a-link.md">Link einfügen</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/link_subscribe_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Anmelde-Link</span> <br /> </td> 
   <td> Jegliches Element<br /> </td> 
   <td> Fügt einen Link zur Anmeldung für einen Dienst hinzu. Weiterführende Informationen zur Konfiguration eines Links finden Sie im Abschnitt <a href="../../designing/using/inserting-a-link.md">Link einfügen</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/link_unsubscribe_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Abmelde-Link</span> <br /> </td> 
   <td> Jegliches Element<br /> </td> 
   <td> Fügt einen Link zur Abmeldung von einem Dienst hinzu. Weiterführende Informationen zur Konfiguration eines Links finden Sie im Abschnitt <a href="../../designing/using/inserting-a-link.md">Link einfügen</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/linkoff_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Link entfernen</span> <br /> </td> 
   <td> Link<br /> </td> 
   <td> Löscht (nach Bestätigung) den Link sowie alle verknüpften Konfigurationen.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/personalization_field_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Personalisierungsfeld einfügen</span> <br /> </td> 
   <td> Textelement<br /> </td> 
   <td> Fügt den Wert eines Datenbankfelds in den Inhalt ein. Siehe <a href="../../designing/using/inserting-a-personalization-field.md">Personalisierungsfelder einfügen</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/personalization_block_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Inhaltsbaustein einfügen</span> <br /> </td> 
   <td> Textelement<br /> </td> 
   <td> Fügt einen personalisierten Inhaltsbaustein ein. Siehe <a href="../../designing/using/adding-a-content-block.md">Inhaltsbausteine</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/dynamiccontent_24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Dynamischen Inhalt aktivieren</span> <br /> </td> 
   <td> Textelement<br /> </td> 
   <td> Ermöglicht das Einfügen von dynamischen Inhalten in den Nachrichtenkörper. Siehe <a href="../../designing/using/defining-dynamic-content-in-a-landing-page.md">Dynamische Inhalte definieren</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/dynamiccontentdisable_24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Dynamischen Inhalt deaktivieren</span> <br /> </td> 
   <td> Textelement<br /> </td> 
   <td> Ermöglicht das Löschen eines dynamischen Inhalts.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/increase_fontsize_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Schriftgröße vergrößern</span> <br /> </td> 
   <td> Textelement<br /> </td> 
   <td> Vergrößert den ausgewählten Text (Hinzufügung von <strong>&lt;span style="font-size:"&gt;</strong> im HTML-Code).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/decrease_fontsize_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Schriftgröße verkleinern</span> <br /> </td> 
   <td> Textelement<br /> </td> 
   <td> Verkleinert den ausgewählten Text (Hinzufügung von <strong>&lt;span style="font-size:"&gt;</strong>).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/textbold_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Fett</span> <br /> </td> 
   <td> Textelement<br /> </td> 
   <td> Formatiert den ausgewählten Text fett (Text wird von den Tags <strong>&lt;strong&gt;</strong><strong>&lt;/strong&gt;</strong> umschlossen). <br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/textitalic_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Kursiv</span> <br /> </td> 
   <td> Textelement<br /> </td> 
   <td> Formatiert den ausgewählten Text kursiv (Text wird von den Tags <strong>&lt;em&gt;</strong><strong>&lt;/em&gt;</strong> umschlossen). <br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/textunderline_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Unterstreichen</span> <br /> </td> 
   <td> Textelement<br /> </td> 
   <td> Unterstreicht den ausgewählten Text (Hinzufügung von <strong>&lt;span style="text-decoration: underline;"&gt;</strong> im HTML-Code).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/colorselector_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Hintergrundfarbe ändern</span> <br /> </td> 
   <td> Textelement<br /> </td> 
   <td> Ändert die Hintergrundfarbe des markierten Blocks (Hinzufügung von style="background-color: rgba(170, 86, 255, 0.87)).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/textcolor_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Textfarbe ändern</span> <br /> </td> 
   <td> Textelement<br /> </td> 
   <td> Ändert die Farbe des ganzen Texts innerhalb eines Blocks oder nur des markierten Texts (<strong>&lt;span style="color: #56ff56;"&gt;</strong>).<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/image_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Bild</span> <br /> </td> 
   <td> Block mit einem Bild<br /> </td> 
   <td> Fügt ein Bild aus einer lokalen Datei ein.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/delete_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Löschen</span> <br /> </td> 
   <td> Jegliche Blöcke<br /> </td> 
   <td> Löscht den Block und seinen Inhalt.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/duplicate_fontsize_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Dublette</span> <br /> </td> 
   <td> Jegliche Blöcke<br /> </td> 
   <td> Dupliziert den Block und alle ihn betreffenden Stilmerkmale.<br /> </td> 
  </tr> 
 </tbody> 
</table>


---
title: Landingpage erstellen
description: Erfahren Sie, wie Sie den Inhalt einer Landingpage erstellen.
audience: channels
content-type: reference
topic-tags: landing-pages
context-tags: landingPage,main
feature: Landing Pages
role: User
level: Intermediate
exl-id: 28398843-a170-48cf-b9c0-dca7af56236d
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '1675'
ht-degree: 100%

---

# Landingpage erstellen{#designing-a-landing-page}

## Über die Inhaltserstellung für Landingpages {#about-content-design}

Landingpages werden auf dieselbe Weise erstellt wie [Marketing-Aktivitäten](../../start/using/marketing-activities.md#about-marketing-activities).

Zur Erstellung einer Landingpage müssen Sie den Inhalt der Seite selbst, der Bestätigungsseite und der Fehlerseite definieren. Mithilfe des Schalters unter der Symbolleiste können Sie jede dieser Seiten anzeigen und konfigurieren.

Der Inhalt der Landingpages wird im Campaign-Inhaltseditor gestaltet.

>[!NOTE]
>
>Wenn Ihre Instanz vor dem Erscheinen von Adobe Campaign Standard 19.0 installiert wurde, haben Sie für die E-Mail-Gestaltung immer noch Zugriff auf den alten Editor für E-Mail-Inhalte. Die Benutzeroberfläche, Verwendung und Konfiguration entsprechen größtenteils der für Landingpages geltenden unten stehenden Beschreibung. Es kann jedoch sein, dass nicht alle Funktionen im Legacy-E-Mail-Inhaltseditor verfügbar oder auf dem aktuellen Stand sind, da er ab der Version 19.0 eingestellt wird. Wenn Sie Ihren E-Mail-Inhalt rasch auf einer Drag &amp; Drop-Benutzeroberfläche mithilfe einer Fülle von Funktionen bearbeiten möchten, verwenden Sie [Email Designer](../../designing/using/designing-content-in-adobe-campaign.md).

Auf dieser Seite erfahren Sie die wichtigsten Informationen zum Inhaltseditor für Landingpages: Weiterführende Informationen zu den Aktionen, die häufig bei Marketing-Aktivitäten eingesetzt werden, finden Sie in den folgenden Abschnitten des Handbuchs zum **Entwerfen von E-Mail-Inhalten**:

* [Personalisierungsfeld einfügen](../../designing/using/personalization.md#inserting-a-personalization-field)
* [Inhaltsbaustein hinzufügen](../../designing/using/personalization.md#adding-a-content-block)
* [Link einfügen](../../designing/using/links.md#inserting-a-link)
* [Bilder einfügen](../../designing/using/images.md)
* [Allgemeine Best Practices bei der Inhaltserstellung](../../designing/using/designing-content-in-adobe-campaign.md#content-design-best-practices)

>[!NOTE]
>Sollten Sie bereits über eine vordefinierte Landingpage im HTML-Format verfügen, können Sie sie direkt mittels der Schaltfläche **[!UICONTROL Inhalt ändern]** importieren.
>
>Bevor Sie in Adobe Campaign eine HTML-Seite importieren, ist sicherzustellen, dass sie in unterschiedlichen Browsern korrekt geöffnet und angezeigt werden kann. Wenn die HTML-Seite JavaScript-Elemente enthält, müssen diese außerhalb des Editors fehlerfrei ausführbar sein. Vermeiden Sie im Allgemeinen die Verwendung von Scripts in Nachrichten, um die korrekte Verarbeitung durch E-Mail-Clients zu gewährleisten.

## Benutzeroberfläche des Inhaltseditors für Landingpages{#landing-page-content-editor-interface}

Mit dem Landingpage-Inhaltseditor können Sie mühelos Inhalte in Adobe Campaign definieren, ändern und personalisieren. Um ihn zu öffnen, klicken Sie in den **[!UICONTROL Inhaltsbaustein]** in einem Landingpage-Dashboard.

Der Inhaltseditor besteht aus drei Bereichen. In diesen Bereichen können Sie den Inhalt ansehen und bearbeiten.

![](assets/des_lp_content_8.png)

1. Die **Palette** links im Bildschirm ermöglicht die Bearbeitung der Eigenschaften des markierten Blocks, wie z. B. Hintergrundfarbe, Rahmen, Ausrichtung, Sichtbarkeitsbedingungen etc. Siehe [Personalisierungsfelder einfügen](../../designing/using/personalization.md#inserting-a-personalization-field).
1. In der **Symbolleiste** bieten Schaltflächen Zugriff auf die verfügbaren Aktionen. Sie können eine Vorlage auswählen und den Anzeigemodus wechseln.
1. Im **Hauptarbeitsbereich** ermöglicht eine kontextabhängige Symbolleiste die direkte Bearbeitung des Inhalts. Sie können beispielsweise ein Bild mit einem Link belegen, die Schriftart anpassen, ein Feld löschen etc.

Die **Symbolleiste** enthält Schaltflächen, die die Bearbeitung des angezeigten Inhalts ermöglichen.

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
   <td> Ermöglicht die Auswahl einer nativen Inhaltsvorlage oder den Import eines anderweitig erstellten HTML-Inhalts. Lesen Sie diesbezüglich auch den Abschnitt <a href="../../designing/using/using-existing-content.md">Existierenden Inhalt laden</a>.<br /> </td> 
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

Die dedizierte **Symbolleiste** ist ein kontextuelles Element der Editor-Oberfläche. Je nach markiertem Bereich sind unterschiedliche Schaltflächen verfügbar. Sie enthält Aktionsschaltflächen sowie Schaltflächen zur Anpassung des Textstils. Alle Änderungen beziehen sich somit jeweils nur auf das ausgewählte Element. Wenn Sie beispielsweise einen Block markieren, können Sie diesen löschen oder duplizieren. Wenn Sie Text innerhalb eines Blocks markieren, können Sie ihn in einen Link verwandeln oder die Formatierung anpassen.

![](assets/delivery_content_17.png)

>[!IMPORTANT]
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
   <td> Verlinkt mit einer URL. Weiterführende Informationen zur Konfiguration eines Links finden Sie im Abschnitt <a href="../../designing/using/links.md#inserting-a-link">Link einfügen</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/linkpage_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Link zu einer Landingpage</span> <br /> </td> 
   <td> Jegliches Element<br /> </td> 
   <td> Ermöglicht den Zugriff auf eine Adobe-Campaign-Landingpage. Weiterführende Informationen zur Konfiguration eines Links finden Sie im Abschnitt <a href="../../designing/using/links.md#inserting-a-link">Link einfügen</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/link_Subscribe_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Anmelde-Link</span> <br /> </td> 
   <td> Jegliches Element<br /> </td> 
   <td> Fügt einen Link zur Anmeldung für einen Dienst hinzu. Weiterführende Informationen zur Konfiguration eines Links finden Sie im Abschnitt <a href="../../designing/using/links.md#inserting-a-link">Link einfügen</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/link_unSubscribe_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Abmelde-Link</span> <br /> </td> 
   <td> Jegliches Element<br /> </td> 
   <td> Fügt einen Link zur Abmeldung von einem Dienst hinzu. Weiterführende Informationen zur Konfiguration eines Links finden Sie im Abschnitt <a href="../../designing/using/links.md#inserting-a-link">Link einfügen</a>.<br /> </td> 
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
   <td> Fügt den Wert eines Datenbankfelds in den Inhalt ein. Siehe <a href="../../designing/using/personalization.md#inserting-a-personalization-field">Personalisierungsfelder einfügen</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/personalization_block_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Inhaltsbaustein einfügen</span> <br /> </td> 
   <td> Textelement<br /> </td> 
   <td> Fügt einen personalisierten Inhaltsbaustein ein. Siehe <a href="../../designing/using/personalization.md#adding-a-content-block">Inhaltsbausteine</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/dynamiccontent_24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Dynamischen Inhalt aktivieren</span> <br /> </td> 
   <td> Textelement<br /> </td> 
   <td> Ermöglicht das Einfügen von dynamischen Inhalten in den Nachrichtenkörper. Siehe <a href="../../channels/using/designing-a-landing-page.md#defining-dynamic-content-in-a-landing-page">Dynamische Inhalte definieren</a>.<br /> </td> 
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

## Struktur und Stil von Landingpages verwalten{#managing-landing-page-structure-and-style}

### Bausteine im Inhaltseditor verwalten {#managing-blocks-in-the-content-editor}

Die verschiedenen Elemente des HTML-Inhalts werden auf der Landingpage in Form von Blöcken angezeigt, die in HTML dem **&lt;div>** **&lt;/div>**-Tag entsprechen. Zur Bearbeitung eines Blocks ist dieser zu markieren. Dies wird durch eine blaue Umrandung angezeigt.

![](assets/des_lp_content_1.png)

Wenn ein Block markiert ist, werden die übergeordneten Objekte des entsprechenden HTML-Elements in einer Breadcrumb-Leiste im unteren Teil des Arbeitsbereichs eingeblendet.

Beim Überfahren eines Elements mit der Maus wird dieses farblich unterlegt. Auf diese Weise können Sie leicht von einem Block zum anderen wechseln und das anzupassende HTML-Element präzise auswählen.

![](assets/des_lp_content_2.png)

Anhand der verschiedenen in der Palette oder der kontextuellen Symbolleiste zur Verfügung stehenden Schaltflächen kann der Block dann geändert, dupliziert oder gelöscht werden.

Aktivieren Sie die Textbearbeitung durch einen zweiten Klick in den Block. Der Rahmen um den Block verfärbt sich grün. Danach können Sie Text auswählen oder eingeben. Anhand der verfügbaren Optionen in der Palette und der kontextuellen Symbolleiste können Sie beispielsweise Links hinzufügen oder die Textformatierung anpassen.

![](assets/des_lp_content_3.png)

Die für ein Blockelement (Link, Personalisierungsfeld, Inhaltsbaustein etc.) definierten Parameter können jederzeit über die Palette angepasst werden.

![](assets/des_lp_content_4.png)

### Rahmen und Hintergrund im Inhaltseditor hinzufügen  {#adding-a-border-and-a-background-in-the-content-editor}

Es besteht die Möglichkeit, verschiedene **Hintergrundfarben** aus der Farbpalette für die einzelnen Blöcke auszuwählen. Die Farbe wird jeweils auf den gesamten Block angewendet.

![](assets/des_lp_content_5.png)

Außerdem können die einzelnen Blöcke mit verschiedenen **Rahmen** versehen werden.

![](assets/des_lp_content_6.png)

### Textstil im Inhaltseditor ändern  {#changing-the-text-style-in-the-content-editor}

Um einen Textstil zu ändern, muss sich der Cursor innerhalb eines Textblocks befinden.

Die Textausrichtung kann mit einer der drei Schaltflächen in der Palette links angepasst werden:

![](assets/des_lp_content_7.png)

* **Linksbündig ausrichten** - richtet den Text am linken Rand des markierten Blocks aus (fügt style=&quot;text-align: left;&quot; in den HTML-Code ein).
* **Zentrieren** - richtet den Text im markierten Block mittig aus (fügt style=&quot;text-align: center;&quot; in den HTML-Code ein).
* **Rechtsbündig ausrichten** - richtet den Text am rechten Rand des markierten Blocks aus (fügt style=&quot;text-align: right;&quot; in den HTML-Code ein).

Mithilfe der dedizierten Symbolleiste können darüber hinaus die Schriftattribute wie Schriftgröße, Schriftauszeichnung (fett, kursiv oder unterstrichen) und die Schriftfarbe geändert werden. Siehe [diesen Abschnitt](../../channels/using/designing-a-landing-page.md#landing-page-content-editor-interface).

### Bilder in eine Landingpage einfügen  {#inserting-images-in-a-landing-page}

1. Wählen Sie im Inhalt der Landingpage einen Baustein aus, der ein Bild enthält.
1. Verwenden Sie die Schaltfläche **[!UICONTROL Einfügen]**.

   ![](assets/des_insert_images_lp_1.png)

1. Wählen Sie in der kontextuellen Symbolleiste die Option **[!UICONTROL Lokales Bild]**.

   ![](assets/des_insert_images_lp_2.png)

1. Wählen Sie eine Datei aus.

   ![](assets/des_insert_images_lp_3.png)

1. Passen Sie die Bildeigenschaften nach Bedarf an.

   ![](assets/des_insert_images_lp_4.png)

## Dynamische Inhalte in einer Landingpage definieren{#defining-dynamic-content-in-a-landing-page}

Wenn Sie dynamischen Inhalt in einer Landingpage definieren möchten, verwenden Sie den Breadcrumb-Pfad zur Auswahl eines Bausteins oder wählen Sie direkt ein Element aus.

![](assets/dynamic_content_lp_1.png)

Gewisse Blöcke, beispielsweise Bilder, können nicht direkt ausgewählt werden. Markieren Sie in diesem Fall den übergeordneten Block im Breadcrumb. Dadurch können alle in diesem Block enthaltenen übergeordneten Elemente einschließlich der Bilder bearbeitet werden.
Die definierte Bedingung bezieht sich in diesem Fall auf alle untergeordneten Elemente des übergeordneten Blocks.

Die Breadcrumb-Leiste des Inhaltseditors wird im Abschnitt [Verwaltung der Blöcke](../../channels/using/designing-a-landing-page.md#managing-landing-page-structure-and-style) beschrieben.

Die nächsten Schritte zur Definition von dynamischem Inhalt für Landingpages erfolgen analog zu denen für E-Mails. Siehe [diesen Abschnitt](../../designing/using/personalization.md#defining-dynamic-content-in-an-email).

>[!NOTE]
>
>Die rote Umrandung einer Variante eines Elements zeigt an, dass für diese noch kein Ausdruck definiert wurde.

Sie haben die Möglichkeit, zwischen den verschiedenen dynamischen Inhalten eines Bausteins zu wechseln. Gehen Sie wie folgt vor:

1. Wählen Sie einen Baustein aus.

   Am linken und rechten Bildrand werden Pfeile angezeigt.

1. Benutzen Sie die Pfeile, um zwischen den verfügbaren Inhalten zu wechseln.

   ![](assets/dynamic_content_lp_2.png)

   Der Pfeil verblasst, sobald Sie beim letzten (bzw. bei Verwendung des linken Pfeils beim ersten) dynamischen Inhalt angelangt sind.

   ![](assets/dynamic_content_lp_3.png)

1. Um alle für einen Baustein definierten Bedingungen zu löschen, markieren Sie diesen und klicken Sie erneut auf das Symbol **[!UICONTROL Dynamischen Inhalt deaktivieren]**.
1. Wählen Sie den beizubehaltenden dynamischen Inhalt aus.

   ![](assets/dynamic_content_lp_5.png)

In der Palette:

* Inhalte, für die ein Ausdruck definiert wurde, sind nicht mehr rot umrandet; sie werden in Grautönen angezeigt.
* Der aktuell ausgewählte Inhalt wird in Blautönen angezeigt.

![](assets/dynamic_content_lp_4.png)

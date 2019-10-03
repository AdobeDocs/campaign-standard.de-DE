---
title: Verwalten von Stilen
seo-title: Verwalten von Stilen
description: Verwalten von Stilen
seo-description: Erfahren Sie, wie Sie E-Mail-Stile in Email Designer verwalten.
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
source-git-commit: a7de545e9eec675444245576cddc6eaf8dce05f4

---


# Verwalten von Stilen {#managing-styles}

## E-Mail-Stile bearbeiten{#editing-email-styles}

### Element bearbeiten {#editing-an-element}

In Email Designer werden bei der Auswahl eines Elements mehrere für den Inhaltstyp spezifische Optionen im Bereich **[!UICONTROL Einstellungen]** angezeigt. Mit diesen Optionen können Sie den Stil Ihrer E-Mail ändern.

### Element auswählen   {#selecting-an-element}

Um ein Element in der Benutzeroberfläche von Email Designer auszuwählen, können Sie entweder:

* direkt in die die E-Mail klicken
* oder in der **Palette** auf der linken Seite in den Optionen den Strukturbaum durchsuchen.

![](assets/des_tree_structure.png)

Im Strukturbaum können Sie eine präziseren Auswahl vornehmen. Sie können die folgende Auswahl treffen:

* die gesamte Strukturkomponente,
* eine der Spalten in der Strukturkomponente
* oder eine Komponente innerhalb einer Spalte.

![](assets/des_tree_structure_selection.png)

Um eine Spalte auszuwählen, können Sie auch folgendermaßen vorgehen:

1. Wählen Sie eine Strukturkomponente (direkt in der E-Mail oder unter Verwendung des Strukturbaums in der linken **Palette**).
1. Wählen Sie in der **dedizierten Symbolleiste** die Option **[!UICONTROL Spalte auswählen]**, um die gewünschte Spalte auszuwählen.

In [diesem Abschnitt](../../designing/using/styles.md#example--adjusting-vertical-alignment-and-padding) finden Sie ein Beispiel.

### Einstellungen des Stils anpassen   {#adjusting-style-settings}

1. Wählen Sie in Ihrer E-Mail ein Element aus. Weiterführende Informationen dazu finden Sie unter [Element auswählen](../../designing/using/styles.md#selecting-an-element).
1. Passen Sie die Einstellungen nach Bedarf an. Für jedes ausgewählte Element sind unterschiedliche Einstellungen verfügbar.

   Sie können beispielsweise Hintergründe einfügen, Größen ändern, die horizontale oder senkrechte Ausrichtung ändern, Farben verwalten sowie [Abstände und Spannen](../../designing/using/styles.md#selecting-an-element) hinzufügen.

   Verwenden Sie dazu die im Bereich **[!UICONTROL Einstellungen]** angezeigten Optionen oder [fügen Sie Inline-Styling-Attribute hinzu](../../designing/using/styles.md#adding-inline-styling-attributes).

   ![](assets/des_settings_pane.png)

1. Speichern Sie Ihren Inhalt.

### Über Abstände und Spannen   {#about-padding-and-margin}

In der Benutzeroberfläche von Email Designer können Sie rasch Abstände und Spannen anpassen.

**[!UICONTROL Abstand]**: Mit dieser Einstellung ändern Sie den Raum innerhalb des Rahmens eines Elements.

![](assets/des_padding.png)

Beispiel:

* Verwenden Sie Abstände, um Ränder links und recshts von einem Bild einzurichten.
* Verwenden Sie Abstände oben und unten, um einen Abstand zu einem **[!UICONTROL Text]** oder einen **[!UICONTROL Divider]** zu einer Komponente hinzuzufügen.
* Um in einem Strukturelement Rahmen zwischen Spalten einzurichten, definieren Sie für jede Spalte einen Abstand.

**[!UICONTROL Spanne]**: Mit dieser Einstellung verwalten Sie den Raum zwischen dem Rahmen eines Elements und dem nächsten Element.

![](assets/des_margin.png)

>[!NOTE]
>
>Je nach Ihrer Auswahl (Strukturkomponente, Spalte oder Inhaltskomponente) ist das Ergebnis anders. Adobe empfiehlt die Einrichtung der Parameter **[!UICONTROL Abstand]** und **[!UICONTROL Rand]** auf Spaltenebene.

Wählen Sie für sowohl **[!UICONTROL Abstand]** als auch **[!UICONTROL Spanne]** das Schlosssymbol aus, um die Synchronisation zwischen den Parametern oben und unten bzw. rechts und links aufzuheben. Dadurch können Sie jeden Parameter einzeln anpassen.

![](assets/des_padding_lock_icon.png)

### Über die Ausrichtung   {#about-alignment}

* **Textausrichtung**: Platzieren Sie den Cursor auf einem Text und richten Sie ihn über die dedizierte Symbolleiste aus.

   ![](assets/des_text_alignment.png)

* **Horizontale Ausrichtung** kann auf Text, Bilder und Schaltflächen angewendet werden, aktuell aber nicht auf die Komponenten **[!UICONTROL Divider]** und **[!UICONTROL Sozial]**.

   ![](assets/des_horizontal_alignment.png)

* Um die **senkrechte Ausrichtung** festzulegen, wählen Sie eine Spalte innerhalb einer Strukturkomponente aus und danach eine Option im Einstellungsfenster.

   ![](assets/des_set_vertical_alignment.png)

### Über den Hintergrund   {#about-backgrounds}

Für die Einstellung von Hintergründen mit Email Designer empfiehlt Adobe Folgendes:

1. Wenden Sie eine Hintergrundfarbe auf den Hauptteil Ihrer E-Mail an, wenn das Design es so verlangt.
1. Meistens wird die Hintergrundfarbe auf Spaltenebene festgelegt.
1. Versuchen Sie nicht, Hintergrundfarben für Bilder oder Textkomponenten zu verwenden, da sie schwierig zu handhaben sind.

Unten finden Sie die verfügbaren Einstellungen für den Hintergrund.

* Legen Sie eine **[!UICONTROL Hintergrundfarbe]** für die gesamte E-Mail fest. Wählen Sie die Einstellungen für den Hauptteil im Navigationsbaum aus, auf den Sie über die linke Palette zugreifen können.

   ![](assets/des_background_body.png)

* Legen Sie dieselbe Hintergrundfarbe für alle Strukturkomponenten fest, indem Sie **[!UICONTROL Viewport-Hintergrundfarbe auswählen]**. Mit dieser Option können Sie eine andere Einstellung als die Hintergrundfarbe auswählen.

   ![](assets/des_background_viewport.png)

* Legen Sie für jede Strukturkomponente eine andere Hintergrundfarbe fest. Wählen Sie in der linken Palette eine Struktur im Navigationsbaum aus, um eine bestimmte Hintergrundfarbe nur dieser Struktur zuzuweisen.

   ![](assets/des_background_structure.png)

   Wählen Sie aber keine Viewport-Hintergrundfarbe aus, da diese die Struktur-Hintergrundfarben verdecken könnte.

* Legen Sie für den Inhalt einer Strukturkomponente ein **[!UICONTROL Hintergrundbild]** fest.

   ![](assets/des_background_image.png)

   >[!NOTE]
   >
   >Manche E-Mail-Programme unterstützen keine Hintergrundbilder. Wählen Sie daher eine passende Fallback-Hintergrundfarbe auf, falls das Bild nicht dargestellt werden kann.

* Legen Sie auf Spaltenebene eine Hintergrundfarbe fest.

   ![](assets/des_background_column.png)

   >[!NOTE]
   >
   >Dies ist der häufigste Anwendungsfall. Adobe empfiehlt, Hintergrundfarben auf Spaltenebene festzulegen, da dies mehr Flexibilität bietet, wenn der gesamte E-Mail-Inhalt bearbeitet wird.

   Sie können auch ein Hintergrundbild auf Spaltenebene einrichten, was aber nur selten verwendet wird.

#### Beispiel: Anpassung der senkrechten Ausrichtung und des Abstands {#example--adjusting-vertical-alignment-and-padding}

Sie möchten den Abstand und die senkrechte Ausrichtung innerhalb einer Strukturkomponente bestehend aus drei Spalten anpassen. Gehen Sie dazu wie folgt vor:

1. Wählen Sie eine Strukturkomponente direkt in der E-Mail oder unter Verwendung des Strukturbaums in der linken **Palette** aus.
1. Wählen Sie in der **dedizierten Symbolleiste** mit der Option **[!UICONTROL Spalte auswählen]** die gewünschte Spalte aus. Sie können sie auch im Strukturbaum auswählen.

   ![](assets/des_selecting_column.png)

   Die bearbeitbaren Parameter für diese Spalte werden im Bereich **[!UICONTROL Einstellungen]** auf der rechten Seite angezeigt.

1. Wählen Sie unter **[!UICONTROL Senkrecht ausrichten]** die Option **[!UICONTROL Nach oben]** aus.

   ![](assets/des_vertical_alignment.png)

   Die Inhaltskomponente wird am oberen Rand der Spalte angezeigt.

1. Definieren Sie unter **[!UICONTROL Abstand]** den Abstand der Spalte vom oberen Rand. Wählen Sie das Schlosssymbol aus, um die Synchronisation mit dem Abstand vom unteren Rand aufzuheben.

   Definieren Sie den linken und rechten Abstand für diese Spalte.

   ![](assets/des_adjusting_padding.png)

1. Gehen Sie analog mit den anderen Ausrichtungs- und Abstandseinstellungen der Spalten vor.

   ![](assets/des_adjusting_columns.png)

1. Speichern Sie Ihre Änderungen.

### Inline-Styling-Attribute hinzufügen   {#adding-inline-styling-attributes}

Wenn Sie in der Benutzeroberfläche von Email Designer ein Element auswählen und im seitlichen Fenster seine Einstellungen anzeigen, können Sie seine Inline-Attribute und deren Werte ändern.

1. Wählen Sie in Ihrem Inhalt ein Element aus.
1. Suchen Sie im seitlichen Fenster nach den Einstellungen für **[!UICONTROL Inline-Stile]**.

   ![](assets/email_designer_inlineattributes.png)

1. Ändern Sie die Werte der vorhandenen Attribute oder fügen Sie mit den Schaltflächen **+** neue hinzu. Sie können alle Attribute und Werte hinzufügen, die CSS-kompatibel sind.

Der Stil wird auf das ausgewählte Element angewendet. Wenn für die untergeordneten Elemente keine speziellen Stilattribute definiert sind, wird der Stil des übergeordneten Elements verwendet.

## Zur Mobile-Ansicht wechseln {#switching-to-mobile-view}

Sie können das responsive Design einer E-Mail anpassen, indem Sie alle Stiloptionen für die Darstellung auf Mobilgeräten einzeln bearbeiten. So können Sie beispielsweise für die mobile Version Ihrer E-Mail die Spannen und Abstände verändern sowie kleinere oder größere Schriftgrade verwenden, die Schaltflächen ändern oder unterschiedliche Hintergrundfarben auswählen.

Alle Stiloptionen sind in der Mobile-Ansicht verfügbar. Weiterführende Informationen zu den Stileinstellungen von Email Designer finden Sie im Abschnitt [E-Mail-Stile bearbeiten](../../designing/using/styles.md).

1. Erstellen Sie eine E-Mail und bearbeiten Sie den Inhalt. Weiterführende Informationen dazu finden Sie im Abschnitt [Neuen E-Mail-Inhalt gestalten](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).
1. Öffnen Sie mit der Schaltfläche **[!UICONTROL Zur Mobile-Ansicht wechseln]** die Mobile-Ansicht.

   ![](assets/email_designer_mobile_view_switch.png)

   Die Mobile-Version der E-Mail wird angezeigt. Sie enthält alle in der Desktop-Ansicht definierten Komponenten und Stile.

1. Sie können alle Stileinstellungen unabhängig voneinander bearbeiten, z. B. Hintergrundfarbe, Ausrichtung, Abstand, Spanne, Schriftart, Textfarbe usw.

   ![](assets/email_designer_mobile_view.png)

1. Änderungen von Stileinstellungen in der Mobile-Ansicht werden nur auf die Mobile-Version angewendet.

   Sie können in der Mobile-Ansicht z. B. die Größe eines Bildes verringern, einen grünen Hintergrund hinzufügen und den Abstand verändern.

   ![](assets/email_designer_mobile_view_change.png)

1. Sie können Komponenten auf Mobilgeräten ausblenden. Wählen Sie dazu **[!UICONTROL Nur auf Desktops zeigen]** in den **[!UICONTROL Anzeigeoptionen]** aus.
Sie können eine Komponente auch auf Desktopgeräten ausblenden, sodass sie nur auf Mobilgeräten angezeigt wird. Wählen Sie dazu **[!UICONTROL Nur auf Mobilgeräten zeigen]** aus.
Mit dieser Option haben Sie beispielsweise die Möglichkeit, ein bestimmtes Bild auf Mobilgeräten und ein anderes Bild auf Desktop-Geräten zu zeigen.
Sie können diese Option sowohl in der Mobilgeräte- als auch der Desktop-Ansicht auswählen.

   ![](assets/email_designer_mobile_hide.png)

1. Wählen Sie nochmals die Schaltfläche **[!UICONTROL Zur Mobile-Ansicht wechseln]** aus, um zur Desktop-Ansicht zu wechseln. Die soeben vorgenommenen Stiländerungen sind in dieser Version nicht vorhanden.

   ![](assets/email_designer_mobile_view_desktop_no-change.png)

   >[!NOTE]
   >
   >Die einzige Ausnahme sind die Einstellungen für **[!UICONTROL Inline-Stile]**. Inline-Stil-Einstellungen werden auch von der standardmäßigen Desktop-Ansicht übernommen.

1. Andere Änderungen an der Struktur oder am Inhalt der E-Mail, wie zum Beispiel Textänderungen, der Upload eines neuen Bildes, das Hinzufügen einer neuen Komponente etc. werden auch in der Standardansicht angezeigt.

   Wechseln Sie wieder in die Mobile-Ansicht und ändern Sie z. B. Text und ersetzen Sie ein Bild.

   ![](assets/email_designer_mobile_view_change_content.png)

   Wählen Sie nochmals die Schaltfläche **[!UICONTROL Zur Mobile-Ansicht wechseln]** aus, um zur Desktop-Ansicht zu wechseln. Die Änderungen wurden übernommen.

   ![](assets/email_designer_mobile_view_desktop_content-change.png)

1. Wenn Sie in der Mobile-Version einen Stil entfernen, wird der im Desktop-Modus angewendete Stil übernommen.

   Fügen Sie in der Mobile-Ansicht z. B. für eine Schaltfläche eine grüne Hintergrundfarbe ein.

   ![](assets/email_designer_mobile_view_background_mobile.png)

1. Wechseln Sie in die Desktop-Ansicht und wählen Sie für dieselbe Schaltfläche einen grauen Hintergrund.

   ![](assets/email_designer_mobile_view_background_desktop.png)

1. Wechseln Sie nochmals zur Mobile-Ansicht und deaktivieren Sie die Einstellung **[!UICONTROL Hintergrundfarbe]**.

   ![](assets/email_designer_mobile_view_background_mobile_disabled.png)

   Die in der Desktop-Ansicht ausgewählte Hintergrundfarbe wird jetzt angewendet: Die Schaltfläche wird grau (nicht farblos) dargestellt.

   Die einzige Ausnahme ist die Einstellung für die **[!UICONTROL Randfarbe]**. Wenn diese in der Mobile-Ansicht deaktiviert ist, wird kein Rahmen mehr hinzugefügt, selbst wenn in der Desktop-Ansicht eine Randfarbe definiert wird.

>[!NOTE]
>
>Die Mobile-Ansicht ist nicht in [Fragmenten](../../designing/using/using-reusable-content.md#about-fragments) verfügbar.

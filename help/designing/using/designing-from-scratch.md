---
title: 'Erstellen neuer E-Mails '
description: Erfahren Sie, wie Sie in Email Designer E-Mails aus neuen E-Mail-Inhalten erstellen.
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
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Erstellen neuer E-Mails {#designing-an-email-content-from-scratch}

Erfahren Sie, wie Sie die Bearbeitung Ihrer E-Mail-Inhalte meistern. In Email Designer können Sie E-Mails und Vorlagen mit oder ohne eigene vordefinierte Inhalte erstellen.

## Wichtige Schritte bei der Erstellung von E-Mails {#key-steps-to-create-your-email}

Dies sind die wichtigsten Schritte zum Erstellen und Gestalten eines neuen E-Mail-Inhalts mithilfe von Email Designer:

1. Erstellen Sie eine E-Mail und öffnen Sie ihren Inhalt.
1. Fügen Sie Strukturkomponenten hinzu, um der E-Mail die gewünschte Form zu geben. Siehe auch den Abschnitt [E-Mail-Struktur bearbeiten](#defining-the-email-structure)
1. Fügen Sie Inhaltskomponenten und Fragmente in die Strukturkomponenten ein. Siehe auch den Abschnitt [Fragmente und Inhaltskomponenten hinzufügen](#defining-the-email-structure)
1. Fügen Sie Bilder hinzu und bearbeiten Sie den Text der E-Mail. Siehe [Bilder einfügen](../../designing/using/images.md#inserting-images).
1. Personalisieren Sie Ihre E-Mail durch Hinzufügen von Personalisierungsfeldern, Links etc. Siehe [Personalisierungsfelder einfügen](../../designing/using/personalization.md#inserting-a-personalization-field), [Link einfügen](../../designing/using/links.md#inserting-a-link) und [Dynamische Inhalte in einer E-Mail definieren](../../designing/using/personalization.md#defining-dynamic-content-in-an-email).
1. Definieren Sie die Betreffzeile Ihrer E-Mail. Siehe [Betreffzeile einer E-Mail personalisieren](../../designing/using/subject-line.md#defining-the-subject-line-of-an-email).
1. Sehen Sie sich die E-Mail in der Vorschau an.
1. Speichern Sie den Inhalt und fahren Sie mit der Nachricht fort, nachdem Sie eine Audience definiert und den Versandzeitpunkt festgelegt haben.

Sehen Sie sich dazu auch dieses [Einführungsvideo](https://video.tv.adobe.com/v/22771/?autoplay=true&hidetitle=true&captions=ger) an.

>[!NOTE]
>
>Wenn Sie keinen völlig neuen E-Mail-Inhalt erstellen möchten, können Sie auch die nativen Inhaltsvorlagen verwenden. Weiterführende Informationen dazu finden Sie im Abschnitt [Inhaltsvorlagen](../../designing/using/using-reusable-content.md#content-templates).

### Definieren der E-Mail-Struktur {#defining-the-email-structure}

Email Designer bietet eine einfache Möglichkeit, die Struktur Ihrer E-Mail zu bestimmen. Durch das Hinzufügen und Verschieben von strukturellen Elementen durch einfaches Drag &amp; Drop können Sie Ihrer E-Mail in Sekundenschnelle die gewünschte Form verleihen.

Um die Struktur einer E-Mail zu bearbeiten, gehen Sie wie folgt vor:

1. Öffnen Sie vorhandenen Inhalt oder erstellen Sie neuen.
1. Öffnen Sie die **[!UICONTROL Strukturkomponenten]** durch Auswahl des Zeichens **+** auf der linken Seite.

   ![](assets/email_designer_structure.png)

1. Wählen Sie die für Ihre E-Mail benötigten Strukturkomponenten mit Drag &amp; Drop aus.

   ![](assets/email_designer_structure_components.png)

   Eine blaue Linie kennzeichnet die Stelle, an der die Strukturkomponente platziert wird, wenn Sie sie loslassen. Sie können die Strukturkomponente oberhalb, zwischen oder unterhalb einer anderen Komponente platzieren, nicht jedoch in einer Komponente.

   >[!NOTE]
   >
   >Sobald die Komponenten in der E-Mail platziert sind, können sie nicht mehr verschoben oder entfernt werden, außer es befindet sich bereits eine Inhaltskomponente oder ein Fragment darin.

1. Mehrere Strukturkomponenten bestehend aus einer oder mehreren Spalten sind verfügbar.

   Wählen Sie die Komponente **[!UICONTROL n:n Spalte]** aus, um die Anzahl der Spalten zu definieren (3 bis 10). Sie können auch die Breite jeder Spalte ändern, indem Sie den Pfeil am unteren Rand einer jeden Spalte verschieben.

   ![](assets/email_designer_n-n-column.png)

   >[!NOTE]
   >
   >Die Größe einer Spalte muss immer mindestens 10 % der Gesamtbreite der Strukturkomponente betragen. Sie können nur leere Spalten entfernen.

Sobald die Struktur definiert ist, können Sie Inhaltsfragmente und Komponenten zu Ihrer E-Mail hinzufügen.

### Verwenden von Inhaltskomponenten {#about-content-components}

Inhaltskomponenten sind leere Komponenten, die nach dem Einfügen in eine E-Mail bearbeitet werden können.

Sie können in einer Strukturkomponente beliebig viele Inhaltskomponenten hinzufügen. Sie können sie auch innerhalb einer Strukturkomponente oder in eine andere Strukturkomponente verschieben.

Dies ist die Liste verfügbarer Komponenten in Email Designer:

- **[!UICONTROL Schaltfläche]**

   Wenn Sie mehrere Schaltflächen benötigen, müssen Sie nicht jede einzelne neu erstellen, sondern können die Komponente **[!UICONTROL Schaltfläche]** in der dedizierten Symbolleiste duplizieren.

   Sie können auch Schaltflächen in Fragmenten speichern, die nochmals verwendet werden können. Weiterführende Informationen dazu finden Sie in den Abschnitten [Inhaltsfragment erstellen](../../designing/using/using-reusable-content.md#creating-a-content-fragment) und [Inhalt als Fragment speichern](../../designing/using/using-reusable-content.md#saving-content-as-a-fragment).

1. Wählen Sie **[!UICONTROL Fallback-Ansicht]** aus, um das Fallback-Bild in Email Designer zu zeigen.

- **[!UICONTROL Text]**

   Verwenden Sie diese Komponente, um Text in Ihre E-Mail einzufügen. Sie können die Farbe, den Stil und die Größe des Textes in den **[!UICONTROL Komponenteneinstellungen]** anpassen.

- **[!UICONTROL Divisor]**

   Verwenden Sie diese Komponente, um eine Trennlinie in Ihre E-Mail einzufügen. Sie können die Farbe, den Stil und die Größe der Trennlinie in den **[!UICONTROL Komponenteneinstellungen]** auswählen.

- **[!UICONTROL HTML]**

   Verwenden Sie diese Komponente, um die unterschiedlichen Teile Ihrer existierenden HTML-Datei zu kopieren und einzufügen. Damit können Sie kostenfrei modulare HTML-Komponenten erstellen.

   >[!NOTE]
   >
   >Eine kostenfreie HTML-Komponente ist beschränkt bearbeitbar. Wenn nicht alle Stile inline vorhanden sind, fügen Sie die entsprechende CSS-Datei im       **head**-Abschnitt des HTML-Codes ein. Andernfalls ist die E-Mail nicht responsiv. Verwenden Sie die Schaltfläche **[!UICONTROL Vorschau]**, um Ihren Inhalt zu testen (siehe [Vorschau von Nachrichten ansehen](../../sending/using/previewing-messages.md)).

   Um die Kompatibilität von externem Inhalt mit Email Designer zu gewährleisten, empfiehlt Adobe, eine neue Nachricht zu erstellen und den Inhalt aus der existierenden E-Mail in Fragmente und Komponenten hinzuzufügen.

   Wenn Sie Inhalt haben, der nicht wiederhergestellt werden kann, können Sie den HTML-Code mithilfe der **[!UICONTROL HTML]**-Inhaltskomponente aus der Original-E-Mail kopieren und einfügen. Nur Benutzer, die mit HTML vertraut sind, sollten diese Schritte ausführen.

   <!-- A full example is presented below. -->

   >[!NOTE]
   >
   >Der neue Inhalt ist keine exakte Kopie der ursprünglichen E-Mail, aber mithilfe der unten stehenden Schritte können Sie eine Nachricht erstellen, die dem Original möglichst ähnelt.

   **Vor dem Kopieren des Inhalts**

   1. Stellen Sie fest, welche Bereiche Ihrer ursprünglichen E-Mail Sie in späteren E-Mails wiederverwenden möchten.
   1. Speichern Sie alle Bilder und Assets, die Sie verwenden möchten.
   1. Wenn Sie ausreichende HTML-Kenntnisse haben, teilen Sie Ihren ursprünglichen HTML-Inhalt in unterschiedliche Teile auf.

- **[!UICONTROL Video]**

   Verwenden Sie diese Komponente, um ein Video in Ihre E-Mail einzufügen.

   Fügen Sie die Videokomponente in eine Strukturkomponente Ihrer E-Mail ein und geben Sie den Videolink in die **[!UICONTROL Komponenteneinstellungen]** ein.

- **[!UICONTROL Bild]**

   Verwenden Sie diese Komponente, um ein Bild in Ihre E-Mail einzufügen.

   Fügen Sie die Bildkomponente in eine Strukturkomponente ein und klicken Sie auf „Durchsuchen“, um die gewünschte Bilddatei aus Ihrem Dateisystem hochzuladen.

- **[!UICONTROL Sozial]**

   Verwenden Sie diese Komponente, um Links zu Social-Media-Seiten in Ihre E-Mail einzufügen. Die anzuzeigenden Links und die Größe ihrer Symbole können Sie in den **[!UICONTROL Komponenteneinstellungen]** auswählen.

- **[!UICONTROL Karussell]**

   1. Ziehen Sie die Komponente **[!UICONTROL Karussell]** in eine Strukturkomponente.
   1. Durchsuchen Sie Ihre Festplatte nach Bildern.
   ![](assets/des_carousel_browse.png)

   1. Wählen Sie in den **[!UICONTROL Einstellungen]** die Anzahl der gewünschten Miniaturansichten für das Karussell aus.
   1. Wählen Sie ein Fallback-Bild von Ihrer Festplatte aus.
   ![](assets/des_carousel_fallback.png)

   Die Karussell-Komponente ist nicht mit allen E-Mail-Programmen kompatibel. Wenn das Karussell vom E-Mail-Programm nicht unterstützt wird, laden Sie ein Fallback-Bild hoch.

   >[!NOTE]
   >
   >Die Karussell-Komponente ist mit den folgenden E-Mail-Plattformen kompatibel: Apple Mail 7, Apple Mail 8, Outlook 2011 for Mac, Outlook 2016 for Mac, Mozilla Thunderbird, iPad und iPad mini iOS, iPhone iOS, Android, AOL (Chrome, Firefox und Safari).

**Verwandte Themen**:

- [E-Mails erstellen](../../channels/using/creating-an-email.md)
- [Audience in einer Nachricht auswählen](../../audiences/using/selecting-an-audience-in-a-message.md)
- [Versandplanung](../../sending/using/about-scheduling-messages.md)
- [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md)
- [E-Mail-Rendering](../../sending/using/email-rendering.md)

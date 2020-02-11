---
title: Personalisieren von E-Mail-Inhalten
description: Erfahren Sie, wie Sie eine E-Mail in Email Designer personalisieren.
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
source-git-commit: 07d68b5bf8d800ebd95919f491e98f1b7a015705

---


# Personalisieren von E-Mail-Inhalten {#personalization}

Es gibt verschiedene Möglichkeiten, um den Inhalt und die Darstellung von Nachrichten in Adobe Campaign zu personalisieren. Diese Personalisierungsmöglichkeiten können abhängig von den jeweiligen Profilen kombiniert werden. Im Allgemeinen bietet Adobe Campaign folgende Möglichkeiten:

* Dynamische Personalisierungsfelder einfügen. Siehe [Personalisierungsfelder einfügen](#inserting-a-personalization-field).
* Vordefinierte Personalisierungsbausteine einfügen. Siehe [Inhaltsbausteine](#adding-a-content-block).
* Absender einer E-Mail personalisieren. Siehe [Personalisierung für den Absender einrichten](#personalizing-the-sender).
* Betreff einer E-Mail personalisieren. Siehe [Betreffzeile einer E-Mail personalisieren](../../designing/using/subject-line.md#defining-the-subject-line-of-an-email).
* Bedingte Inhalte erstellen. Siehe [Definieren von dynamischen Inhalten in einer E-Mail](#defining-dynamic-content-in-an-email). .

## Personalisierung für den Absender einrichten {#personalizing-the-sender}

To define the name of the sender which will appear in the header of messages sent, go the **[!UICONTROL Properties]** tab of the Email Designer home page (accessible through the home icon). For more on this, see [Defining the sender of an email](../../designing/using/subject-line.md#email-sender).

Sie können den Absendernamen ändern, indem Sie **Name des Absenders** auswählen. Geben Sie nun den gewünschten Absendernamen ein.

Sie haben die Möglichkeit, den Absendernamen je nach Zielgruppe zu personalisieren. Sie können Personalisierungsfelder, Inhaltsbausteine und dynamische Inhalte hinzufügen, indem Sie die Symbole unter dem Absendernamen auswählen.

>[!NOTE]
>
>Header-Parameter dürfen nicht leer sein. Die Angabe der Absenderadresse ist für den E-Mail-Versand zwingend erforderlich (gemäß RFC-Standard). Adobe Campaign führt eine Syntax-Prüfung der angegebenen E-Mail-Adressen durch.

## URLs personalisieren{#personalizing-urls}

Sie haben in Adobe Campaign die Möglichkeit, in Ihrer Nachricht eine oder mehrere URLs zu personalisieren, indem Sie Personalisierungsfelder, Inhaltsbausteine oder dynamische Inhalte an diese anschließen. Gehen Sie wie folgt vor:

1. Fügen Sie eine externe URL ein und geben Sie deren Parameter an. Siehe [Link einfügen](../../designing/using/links.md#inserting-a-link).
1. Wenn die Personalisierungsoptionen nicht angezeigt werden, verwenden Sie im Einstellungsfenster das Stiftsymbol neben der ausgewählten URL, um die Personalisierungsoptionen aufzurufen.
1. Fügen Sie die gewünschten Personalisierungsfelder, Inhaltsbausteine und dynamischen Inhalte hinzu.

   ![](assets/des_personalize_links.png)

1. Speichern Sie Ihre Änderungen.

>[!NOTE]
>
>Die Personalisierung von URLs kann sich weder auf den Domain-Namen noch auf die URL-Erweiterung beziehen. Bei der Nachrichtenvorbereitung wird eine Fehlernachricht angezeigt, wenn die Personalisierung nicht korrekt ist. Bei der Auswahl eines Inhaltsbausteins dürfen Sie keine Elemente wie **Link zur Mirrorseite** auswählen. Dieser Typ von Inhaltsbausteinen darf nicht innerhalb eines Links verwendet werden.

## Personalisierungsfeld einfügen{#inserting-a-personalization-field}

Adobe Campaign bietet die Möglichkeit, Felder aus der Datenbank, beispielsweise den Vornamen der Profile, in Form von Platzhaltern in Ihren Inhalten zu verwenden.

>[!NOTE]
>
>In den unten stehenden Bildern sehen Sie, wie Sie einen Link mit [Email Designer](../../designing/using/designing-content-in-adobe-campaign.md) einfügen können.

Um ein Personalisierungsfeld einzufügen, gehen Sie folgendermaßen vor:

1. Click inside a text block, click the **[!UICONTROL Personalize]** icon from the contextual toolbar and select **[!UICONTROL Insert personalization field]**. Weiterführende Informationen zur Benutzeroberfläche von Email Designer finden Sie [in diesem Abschnitt](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-interface).

   ![](assets/email_perso_field_1.png)

1. Wählen Sie das Feld aus, das Sie in den Inhalt der Seite einfügen möchten.

   ![](assets/email_perso_field_2.png)

1. Klicks **[!UICONTROL Confirm]**.

Der Name des Felds erscheint daraufhin hervorgehoben im Editor.

![](assets/email_perso_field_3.png)

Der entsprechende Platzhalter wird zum Zeitpunkt der Personalisierung (d. h. bei der Vorschauerzeugung, der E-Mail-Vorbereitung) durch den für das jeweilige Profil gespeicherten Wert aus der Datenbank ersetzt.

>[!NOTE]
>
>Bei von einem Workflow aus erstellten E-Mails stehen außerdem die innerhalb des Workflows berechneten Zusatzdaten in den Personalisierungsfeldern zur Verfügung. Weiterführende Informationen zur Hinzufügung von Zusatzdaten innerhalb von Workflows finden Sie im Abschnitt [Daten anreichern](../../automating/using/targeting-data.md#enriching-data).

## Inhaltsbausteine{#adding-a-content-block}

Adobe Campaign bietet eine Reihe von vorkonfigurierten Inhaltsbausteinen. Diese Bausteine sind dynamisch und personalisierbar und sie weisen ein spezifisches Rendering auf. Sie ermöglichen beispielsweise das Einfügen einer bestimmten Anrede in Abhängigkeit von den verfügbaren Empfängerinformationen oder auch eines Links zur Mirrorseite.

>[!NOTE]
>
>Auf den unten stehenden Bildern sehen Sie, wie Sie einen Inhaltsbaustein mit [Email Designer](../../designing/using/designing-content-in-adobe-campaign.md) einfügen können.

So fügen Sie einen Inhaltsbaustein hinzu:

1. Click inside a text block, click the **[!UICONTROL Personalize]** icon from the contextual toolbar and select **[!UICONTROL Insert content block]**. Weiterführende Informationen zur Benutzeroberfläche von Email Designer finden Sie [in diesem Abschnitt](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-interface).

   ![](assets/email_content_block_1.png)

1. Wählen Sie den einzufügenden Inhaltsbaustein aus der Liste aus. Je nach Kontext (E-Mail oder Landingpage) können unterschiedliche Bausteine verfügbar sein.

   ![](assets/email_content_block_2.png)

1. Klicks **[!UICONTROL Save]**.

Der Name des Bausteins erscheint daraufhin im Editor. Er ist gelb unterlegt. Er wird in der Personalisierungsphase automatisch an das Profil angepasst.

![](assets/email_content_block_3.png)

Es stehen folgende native Inhaltsbausteine zur Verfügung:

* **[!UICONTROL Database URL in emails (EmailUrlBase)]**: Dieser Inhaltsblock kann nur bei einer **Bereitstellung** verwendet werden.
* **[!UICONTROL Mirror page URL (MirrorPageUrl)]**: Dieser Inhaltsblock kann nur bei einer **Bereitstellung** verwendet werden.
* **[!UICONTROL Link to mirror page (MirrorPage)]**: Dieser Inhaltsblock kann nur bei einer **Bereitstellung** verwendet werden.
* **[!UICONTROL Greetings (Greetings)]**
* **[!UICONTROL Unsubscription link (UnsubscriptionLink)]**: Dieser Inhaltsblock kann nur bei einer **Bereitstellung** verwendet werden.
* **[!UICONTROL Social network sharing links (LandingPageViralLinks)]**: Dieser Inhaltsblock kann nur auf einer **Einstiegsseite** verwendet werden.
* **[!UICONTROL Default sender name (DefaultSenderName)]**: Dieser Inhaltsblock kann nur bei einer **Bereitstellung** verwendet werden.
* **[!UICONTROL Name of default reply-to email address (DefaultReplyName)]**: Dieser Inhaltsblock kann nur bei einer **Bereitstellung** verwendet werden.
* **[!UICONTROL Email address of default sender (DefaultSenderAddress)]**: Dieser Inhaltsblock kann nur bei einer **Bereitstellung** verwendet werden.
* **[!UICONTROL Default error email address (DefaultErrorAddress)]**: Dieser Inhaltsblock kann nur bei einer **Bereitstellung** verwendet werden.
* **[!UICONTROL Default reply-to email address (DefaultReplyAddress)]**: Dieser Inhaltsblock kann nur bei einer **Bereitstellung** verwendet werden.
* **[!UICONTROL Brand name (BrandingUsualName)]**
* **[!UICONTROL Link to the brand website (BrandingWebSiteLink)]**
* **[!UICONTROL Brand logo (BrandingLogo)]**
* **[!UICONTROL Notification style (notificationStyle)]**

### Benutzerdefinierte Inhaltsbausteine erstellen {#creating-custom-content-blocks}

Sie haben die Möglichkeit, weitere Inhaltsbausteine zu erstellen, die in Nachrichten oder Landingpages eingefügt werden können.

Gehen Sie wie folgt vor, um einen Inhaltsbaustein zu erstellen:

1. Click **[!UICONTROL Resources > Content blocks]** from the advanced menu to access the list of content blocks.
1. Click the **[!UICONTROL Create]** button or duplicate a pre-existing content block.

   ![](assets/content_bloc_01.png)

1. Geben Sie einen Titel ein.
1. Wählen Sie den Block aus **[!UICONTROL Content type]**. Dabei stehen drei Optionen zur Verfügung:

   * **[!UICONTROL Shared]**: Der Inhaltsblock kann in einer Bereitstellung oder auf einer Landingpage verwendet werden.
   * **[!UICONTROL Delivery]**: Der Inhaltsblock kann nur bei einer Bereitstellung verwendet werden.
   * **[!UICONTROL Landing page]**: Der Inhaltsblock kann nur auf einer Einstiegsseite verwendet werden.
   ![](assets/content_bloc_02.png)

1. Sie können eine **[!UICONTROL Targeting dimension]** auswählen. Weiterführende Informationen dazu finden Sie im Abschnitt [Über Zielgruppendimensionen](#about-targeting-dimension).

   ![](assets/content_bloc_04.png)

1. You can select the **[!UICONTROL Depends on format]** option to define two different blocks: one for HTML emails, and one for emails in text format. Im unteren Teil des Editors werden in diesem Fall zwei Tabs (HTML und Text) angezeigt, um den jeweiligen Inhalt zu definieren.

   ![](assets/content_bloc_03.png)

1. Enter the content of the content block(s), and click the **[!UICONTROL Create]** button.

Der Inhaltsbaustein kann nun im Inhaltseditor einer Nachricht oder einer Landingpage verwendet werden.

>[!CAUTION]
>
>Achten Sie darauf, dass beim Bearbeiten des Inhalts eines Bausteins keine zusätzlichen Leerzeichen zwischen dem Anfang und dem Ende Ihrer *if*-Anweisungen vorhanden sind. In HTML werden die Leerzeichen auf dem Bildschirm angezeigt und wirken sich daher auf die Darstellung des Inhalts aus.

### Über Zielgruppendimensionen  {#about-targeting-dimension}

Mit der Zielgruppendimension können Sie festlegen, in welchem Nachrichtentyp Sie den Inhaltsbaustein verwenden können. Auf diese Weise wird verhindert, dass in einer Nachricht unpassende Bausteine verwendet werden, die zu Fehlern führen könnten.

Beim Bearbeiten einer Nachricht können Sie nur Inhaltsbausteine mit einer Zielgruppendimension auswählen, die mit der Zielgruppendimension der Nachricht kompatibel ist.

For example, the **[!UICONTROL Unsubscription link]** block&#39;s targeting dimension is **[!UICONTROL Profiles]** because it contains personalization fields specific to the **[!UICONTROL Profiles]** resource. Therefore, you cannot use an **[!UICONTROL Unsubscription link]** block in an [event transactional message](../../channels/using/event-transactional-messages.md), because the targeting dimension of that type of message is **[!UICONTROL Real-time events]**. Sie können aber den Baustein **Abmelde-Link** in einer [Profil-Transaktionsnachricht](../../channels/using/profile-transactional-messages.md) verwenden, weil die Zielgruppendimension dieses Nachrichtentyps **Profile** lautet. Finally, the **[!UICONTROL Link to mirror page]** block does not have a targeting dimension, so you can use it in any message.

Wenn Sie dieses Feld leer lassen, ist der Inhaltsbaustein unabhängig von der Zielgruppendimension mit allen Nachrichten kompatibel. Wenn Sie eine Zielgruppendimension festlegen, ist dieser Baustein nur mit Nachrichten kompatibel, die dieselbe Zielgruppendimension aufweisen.

Lesen Sie diesbezüglich auch den Abschnitt [Zielgruppendimensionen und Ressourcen](../../automating/using/query.md#targeting-dimensions-and-resources).

**Verwandte Themen:**

* [Personalisierungsfeld einfügen](#inserting-a-personalization-field)
* [Inhaltsbausteine](#adding-a-content-block)
* [Dynamische Inhalte in einer E-Mail definieren](#defining-dynamic-content-in-an-email)

## Bildquellen personalisieren{#personalizing-an-image-source}

Sie haben in Adobe Campaign die Möglichkeit, in Ihrer Nachricht ein oder mehrere Bilder nach einem bestimmten Kriterium zu personalisieren oder Tracking zu verwenden, indem Sie Personalisierungsfelder, Inhaltsbausteine oder dynamische Inhalte in die Bildquelle einfügen. Gehen Sie wie folgt vor:

1. Fügen Sie entweder ein neues Bild in Ihren Nachrichteninhalt ein oder wählen Sie ein bereits vorhandenes Bild aus.
1. In the image properties palette, check the **[!UICONTROL Enable personalization]** option.

   ![](assets/des_personalize_images_1.png)

   The **[!UICONTROL Source]** field is displayed and the image selected is shown as **personalized** in the editor.

1. Click the pencil next to the **[!UICONTROL Source]** field button to access the personalization options.
1. Fügen Sie im Anschluss an die ursprüngliche Bildquelle die gewünschten Personalisierungsfelder, Inhaltsbausteine und dynamischen Inhalte hinzu.

   ![](assets/des_personalize_images_2.png)

   >[!NOTE]
   >
   >Der Domain-Name (http://meinedomain.com) kann nicht personalisiert werden, sondern muss manuell eingegeben werden. Die restliche URL kann personalisiert werden. Beispiel: http://meinedomain.com/`[Gender]`.jpg

1. Bestätigen Sie Ihre Änderungen.

## Bedingter Inhalt {#conditional-content}

### Sichtbarkeitsbedingung definieren{#defining-a-visibility-condition}

Es besteht die Möglichkeit, für alle Elemente Sichtbarkeitsbedingungen zu definieren. Das entsprechende Element wird nur dann angezeigt, wenn die Bedingung erfüllt ist.

To add a visibility condition, select a block and enter the condition to be respected in the **[!UICONTROL Visibility condition]** field of its settings.

![](assets/delivery_content_5.png)

Diese Option steht nur für folgende Elemente zur Verfügung: ADDRESS, BLOCKQUOTE, CENTER, DIR, DIV, DL, FIELDSET, FORM, H1, H2, H3, H4, H5, H6, NOSCRIPT, OL, P, PRE, UL, TR, TD.

Weiterführende Informationen zum Ausdruckseditor finden Sie im Abschnitt [Ausdrucksbearbeitung](../../automating/using/editing-queries.md#about-query-editor).

Derartige Bedingungen nehmen die Syntax von XTK-Ausdrücken an (z. B. **context.profile.email !=&#39;&#39;** oder **context.profile.status=&#39;0&#39;**). Standardmäßig werden alle Felder angezeigt.

>[!NOTE]
>
>Es ist nicht möglich, Bedingungen für Blöcke zu definieren, die Unterelemente mit dynamischen Inhalten enthalten oder die selbst bereits einem dynamischen Inhalt angehören. Unsichtbare dynamische Blöcke, wie beispielsweise Dropdown-Menüs, können nicht bearbeitet werden.

### Dynamische Inhalte in einer E-Mail definieren{#defining-dynamic-content-in-an-email}

Es besteht die Möglichkeit, für eine E-Mail multiple Inhalte zu erstellen, die in Abhängigkeit von mithilfe des Ausdruckseditors definierten Bedingungen den Empfängern dynamisch angezeigt werden. So kann beispielsweise jedem Profil je nach seiner Altersgruppe ein abweichender Inhalt angezeigt werden.

Die Definition dynamischer Inhalte erfolgt anders als die Definition von [Sichtbarkeitsbedingungen](#defining-a-visibility-condition).

1. Wählen Sie ein Fragment, eine Komponente oder ein Element aus. Wählen Sie für dieses Beispiel ein Bild aus.
1. Click the **[!UICONTROL Dynamic content]** icon from the contextual toolbar.

   ![](assets/dynamic_content_2.png)

   The **[!UICONTROL Dynamic content]** section appears in the palette on the left.

   ![](assets/dynamic_content_3.png)

   Standardmäßig enthält dieser Bereich zwei Elemente: die Standardvariante und eine neue Variante.

   >[!NOTE]
   >
   >Für den Inhalt muss stets eine Standardvariante vorhanden sein. Diese kann nicht gelöscht werden.

1. Click the **[!UICONTROL Edit]** button to define the display conditions for the first alternative variant.

   ![](assets/dynamic_content_4.png)

1. Geben Sie einen Titel ein und wählen Sie die Felder aus, die als Bedingungen spezifiziert werden sollen. For example, from the **[!UICONTROL General]** node, select the **[!UICONTROL Age]** field

   ![](assets/dynamic_content_5.png)

1. Definieren Sie die Filterbedingungen. Beispielsweise könnten Sie Personen zwischen 18 und 25 Jahren einen anderen Inhalt anzeigen lassen.

   ![](assets/dynamic_content_6.png)

1. Nachdem alle Bedingungen spezifiziert sind, definieren Sie die Reihenfolge, in der diese angewendet werden sollen, und speichern Sie die Änderungen.

   ![](assets/dynamic_content_7.png)

   Die Inhalte werden in der Reihenfolge ihrer Priorität von oben nach unten in der Palette angezeigt. Weiterführende Informationen zu Prioritäten finden Sie in [diesem Abschnitt](#defining-dynamic-content-in-an-email).

1. Laden Sie ein neues Bild für die soeben definierte Variante hoch.

   ![](assets/dynamic_content_8.png)

   Den Empfängern zwischen 18 und 25 Jahren wird das neue Bild angezeigt.

   ![](assets/dynamic_content_10.png)

1. Click **[!UICONTROL Add a condition]** to add a new content and its linked rule.

   ![](assets/dynamic_content_9.png)

   Beispielsweise könnten Sie Personen zwischen 26 und 35 Jahren ein anderes Bild anzeigen lassen.

1. Gehen Sie für alle anderen Elemente Ihrer E-Mail, die dynamisch angezeigt werden soll, analog vor. Dabei kann es sich um Text, Schaltflächen, Fragmente etc. handeln. Speichern Sie Ihre Änderungen.

>[!CAUTION]
>
>Nach der Vorbereitung der Nachricht und vor ihrem Versand ist die Nachricht mithilfe eines Testversands zu prüfen. Andernfalls werden etwaige Fehler unter Umständen nicht erkannt und die E-Mail nicht versendet.

**Verwandte Themen:**

* [Testversand durchführen](../../sending/using/sending-proofs.md)
* [Ausdrucksbearbeitung](../../automating/using/editing-queries.md#about-query-editor)

### Prioritätsstufe  {#order-of-priority}

Bei der Definition eines dynamischen Inhalts im Ausdruckseditor wird folgende Priorität verwendet:

1. Definieren Sie zwei verschiedene dynamische Inhalte mit **zwei verschiedenen Bedingungen**, wie z. B.:

   **Bedingung 1**: Das Geschlecht des Profils ist männlich,

   **Bedingung 2**: Das Profil ist zwischen 20 und 30 Jahre alt.

   ![](assets/delivery_content_61.png)

   Gewisse Profile Ihrer Datenbank erfüllen beide Bedingungen, jedes kann jedoch nur eine E-Mail mit einem einzigen dynamischen Inhalt erhalten.

1. Es ist daher notwendig, die Prioritätsstufen der dynamischen Inhalte festzulegen. Ein Profil, das die Bedingung mit Prioritätsstufe **1** erfüllt, wird nur den dynamischen Inhalt erhalten, der dieser Bedingung entspricht, auch wenn es gleichzeitig die Bedingungen mit Prioritätsstufe **2** oder **3** erfüllt.

   ![](assets/delivery_content_62.png)

Pro dynamischer Inhalt lässt sich lediglich eine Prioritätsstufe festlegen.

## Beispiel: E-Mail-Personalisierung{#example-email-personalization}

Das vorliegende Beispiel zeigt eine E-Mail mit einem Sonderangebot. Der E-Mail-Inhalt soll je nach Alter der Empfänger personalisiert werden. Empfänger zwischen 18 und 27 Jahren sollen eine E-Mail mit einer anderen Illustration und einer anderen Anrede erhalten als Empfänger über 27 Jahre.

Gehen Sie bei der E-Mail-Erstellung wie folgt vor:

* Aktivieren Sie für die Illustration den dynamischen Inhalt und konfigurieren Sie ihn in Abhängigkeit vom Alter der Empfänger.

   ![](assets/delivery_content_43.png)

   Weiterführende Informationen zum Hinzufügen und Konfigurieren von dynamischen Inhalten finden Sie im Abschnitt [Dynamische Inhalte in einer E-Mail definieren](#defining-dynamic-content-in-an-email).

* Aktivieren Sie für den Text den dynamischen Inhalt und fügen Sie Personalisierungsfelder ein. Abhängig von der Altersgruppe des Profils beginnt die E-Mail entweder mit dem Vornamen oder dem Titel und dem Nachnamen des Profils.

   ![](assets/delivery_content_44.png)

   Weiterführende Informationen zum Hinzufügen und Konfigurieren der Personalisierungsfelder finden Sie im Abschnitt [Personalisierungsfelder einfügen](#inserting-a-personalization-field).

### Illustrationen konfigurieren {#configuring-images}

Gehen Sie wie folgt vor:

**Für die Zielgruppe 18 bis 27 Jahre:**

1. Select the dynamic content in the **[!UICONTROL Properties]** palette and click the **[!UICONTROL Edit]** button.

   ![](assets/delivery_content_48.png)

1. Edit the label then select the **[!UICONTROL Age]** field from the **[!UICONTROL Profile]** node.

   ![](assets/delivery_content_49.png)

1. Vervollständigen Sie den Ausdruck mit dem Operator **Größer oder gleich** und dem Wert **18**. Auf diese Weise werden alle Profile ausgewählt, für die die Bedingung **18 Jahre und älter** zutrifft.

   ![](assets/delivery_content_50.png)

1. Add a new **[!UICONTROL Age]** condition.

   Vervollständigen Sie den Ausdruck mit dem Operator **Kleiner oder gleich** und 27. Auf diese Weise werden alle Profile ausgewählt, für die die Bedingung **27 Jahre und jünger** zutrifft.

   ![](assets/delivery_content_51.png)

1. Bestätigen Sie Ihre Änderungen.

**Für die Zielgruppe über 27 Jahre:**

1. Markieren Sie den nächsten dynamischen Inhalt in der Palette und öffnen Sie den Ausdruckseditor.
1. Edit the label then select the **[!UICONTROL Age]** field from the **[!UICONTROL Profile]** node.
1. Vervollständigen Sie den Ausdruck mit dem Operator **Größer als** und 27. Auf diese Weise werden alle Profile ausgewählt, für die die Bedingung **älter als 27 Jahre** zutrifft.

   ![](assets/delivery_content_52.png)

1. Bestätigen Sie Ihre Änderungen.

Die dynamischen Inhalte für die Illustrationen wurden korrekt konfiguriert.

### Text konfigurieren  {#configuring-text}

Gehen Sie wie folgt vor:

**Für die Zielgruppe 18 bis 27 Jahre:**

1. Markieren Sie die anzupassende Strukturkomponente und fügen Sie einen dynamischen Inhalt hinzu.
1. Öffnen Sie den Ausdruckseditor des nächsten dynamischen Inhalts und konfigurieren Sie die Bedingung entsprechend der Zielgruppe. Lesen Sie diesbezüglich auch den Abschnitt [Illustrationen konfigurieren](#configuring-images).
1. In the structure component, at the desired position, click the **[!UICONTROL Personalize]** icon from the contextual toolbar and select **[!UICONTROL Insert personalization field]**.

   ![](assets/delivery_content_53.png)

1. In the list that appears, select the **[!UICONTROL First name]** field and confirm.

   ![](assets/delivery_content_54.png)

1. Das Personalisierungsfeld wurde korrekt in den ausgewählten dynamischen Inhalt eingefügt.

**Für die Zielgruppe über 27 Jahre:**

1. Markieren Sie die anzupassende Strukturkomponente und fügen Sie einen dynamischen Inhalt hinzu.
1. Öffnen Sie den Ausdruckseditor des nächsten dynamischen Inhalts und konfigurieren Sie die Bedingung entsprechend der Zielgruppe. Lesen Sie diesbezüglich auch den Abschnitt [Illustrationen konfigurieren](#configuring-images).
1. In the structure component, at the desired position, click the **[!UICONTROL Personalize]** icon from the contextual toolbar and select **[!UICONTROL Insert personalization field]**.
1. Select **[!UICONTROL Title]** from the drop-down list.
1. Gehen Sie ähnlich vor, um das **[!UICONTROL Last name]** Feld hinzuzufügen.

   ![](assets/delivery_content_56.png)

Die Personalisierungsfelder wurden korrekt in den ausgewählten dynamischen Inhalt eingefügt.

### Vorschau der E-Mail erzeugen  {#previewing-emails}

Previewing allows you to check that the personalization fields and the dynamic contents are configured correctly before sending the **[!UICONTROL Proofs]**. Bei der Vorschau können verschiedene Testprofile ausgewählt werden, die den verschiedenen Zielgruppen der E-Mail entsprechen.

Wenn kein Testprofil ausgewählt wird, wird folgende Standard-E-Mail angezeigt:

![](assets/delivery_content_45.png)

Die Anrede ist nicht personalisiert und es wird die Standard-Illustration angezeigt.

Das erste Testprofil stammt aus der Altersgruppe von 18 bis 27 Jahren. Die seiner Altersgruppe entsprechende E-Mail stellt sich wie folgt dar:

![](assets/delivery_content_46.png)

Als Anrede wird wie gewünscht der Vorname des Profils angezeigt und auch die Illustration entspricht der, die für diese Altersgruppe definiert wurde.

Das zweite Testprofil stammt aus der Altersgruppe von über 27 Jahren. Die entsprechende E-Mail stellt sich wie folgt dar:

![](assets/delivery_content_47.png)

Die Illustration zeigt die im dynamischen Inhalt für diese Altersgruppe konfigurierte und auch die Anrede wird korrekt in ihrer langen Version angezeigt.

**Verwandte Themen:**

* [Audiences erstellen](../../audiences/using/creating-audiences.md)
* [Versandvorbereitung](../../sending/using/preparing-the-send.md)


---
solution: Campaign Standard
product: campaign
title: Ereignis-Transaktionsnachrichten
description: Hier erfahren Sie, wie Sie eine Ereignis-Transaktionsnachricht erstellen und publizieren.
page-status-flag: never-activated
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
translation-type: tm+mt
source-git-commit: 9ad23468d3d1cf386d9558e6cd2344ea2316fc82
workflow-type: tm+mt
source-wordcount: '1692'
ht-degree: 73%

---


# Bearbeiten einer Transaktionsnachricht {#editing-transactional-message}

Nachdem Sie ein Ereignis<!--(the cart abandonment example as explained in [this section](../../channels/using/getting-started-with-transactional-msg.md#transactional-messaging-operating-principle))--> erstellt und veröffentlicht haben, wird die entsprechende Transaktionsnachricht automatisch erstellt. Die Schritte zum Konfigurieren und Veröffentlichen des Ereignisses finden Sie im Abschnitt [Konfigurieren eines transaktionalen Ereignisses](../../channels/using/configuring-transactional-event.md) und [Veröffentlichen eines transaktionalen Ereignisses](../../channels/using/publishing-transactional-event.md).

Die Schritte zum Zugriff, zur Bearbeitung und zum Personalisieren dieser Meldung werden nachfolgend beschrieben.

<!--Event transactional messages do not contain profile information, therefore they are not compatible with fatigue rules (even in the case of an enrichment with profiles). See [Fatigue rules](../../sending/using/fatigue-rules.md#choosing-the-channel).-->

Sobald Ihre Nachricht fertig ist, kann sie getestet und veröffentlicht werden. Siehe [Transaktionsnachricht lifecylce](../../channels/using/publishing-transactional-message.md).

## Transaktionsnachrichten aufrufen {#accessing-transactional-messages}

Aufrufen der erstellten Transaktionsnachricht:

1. Wählen Sie oben links das **[!UICONTROL Adobe Campaign]**-Logo aus.
1. Wählen Sie **[!UICONTROL Marketingpläne]** > **[!UICONTROL Transaktionsnachrichten]** > **[!UICONTROL Transaktionsnachrichten]** aus.

   ![](assets/message-center_4.png)

1. Klicken Sie auf die Nachricht Ihrer Wahl, um sie zu bearbeiten.

>[!IMPORTANT]
>
>Sie können nur dann auf Transaktionsnachrichten zugreifen, wenn Sie der Sicherheitsgruppe **[!UICONTROL Administratoren (alle Einheiten)]** angehören. Weitere Informationen finden Sie unter [Benutzerverwaltung](../../administration/using/users-management.md#functional-administrators).

## Transaktionsnachricht personalisieren          {#personalizing-a-transactional-message}

Gehen Sie folgendermaßen vor, um für eine Transaktionsnachricht eine Personalisierung einzurichten.

>[!NOTE]
>
>In diesem Abschnitt wird beschrieben, wie Sie eine **Ereignis-basierte**-Transaktionsnachricht personalisieren.  Die Konfigurationsschritte zum Erstellen einer Ereignis-basierten Transaktionsnachricht finden Sie in [diesem Abschnitt](../../channels/using/configuring-transactional-event.md#event-based-transactional-messages).
>
>Die **Profil-basierten** Transaktionsnachrichten-Spezifikationen sind [unter](#profile-transactional-message-specificities) detailliert.

Beispielsweise möchten Sie eine Benachrichtigung an Benutzer Ihrer Website senden, die Produkte zum Einkaufswagen hinzugefügt haben und die Site verlassen, ohne mit ihren Käufen fertig zu werden. Dieses Beispiel wird im Abschnitt [Geschäftsprinzip für Transaktionsnachrichten](../../channels/using/getting-started-with-transactional-msg.md#transactional-messaging-operating-principle) vorgestellt.

1. Öffnen Sie mithilfe der gleichnamigen Kachel den **[!UICONTROL Inhalt]** der Nachricht, um den Betreff und den Inhalt anzupassen. Wählen Sie für dieses Beispiel eine Vorlage aus, die Bilder und Text enthält. Weitere Informationen zu E-Mail-Inhaltsvorlagen finden Sie unter [Entwerfen von E-Mails mit Vorlagen](../../designing/using/using-reusable-content.md#designing-templates).

   ![](assets/message-center_6.png)

1. Fügen Sie einen Betreff hinzu und bearbeiten Sie den Inhalt Ihrer Nachricht entsprechend Ihren Anforderungen.

   >[!NOTE]
   >
   >Bei dem Link zum stehen gelassenen Warenkorb handelt es sich um einen Link auf eine externe URL, die den Kunden zu seinem Warenkorb weiterleitet. Diese Konfiguration wird außerhalb von Adobe Campaign vorgenommen.

1. In unserem Beispiel möchten Sie drei Felder hinzufügen, die Sie beim [Erstellen des Ereignisses](../../channels/using/configuring-transactional-event.md) definiert haben: Vorname, letztes angesehenes Produkt, Gesamtbetrag des Warenkorbs. Fügen Sie dazu ein [Personalisierungsfeld](../../designing/using/personalization.md#inserting-a-personalization-field) in den Nachrichteninhalt ein.

1. Gehen Sie zu diesen Feldern über **[!UICONTROL Kontext]** > **[!UICONTROL Echtzeit-Ereignis]** > **[!UICONTROL Ereigniskontext]**.

   ![](assets/message-center_7.png)

1. Fügen Sie dann zur Anreicherung Ihres Nachrichteninhalts die gewünschten Felder hinzu, indem Sie diese in der Tabelle auswählen, mit der Sie Ihr Ereignis verknüpft haben. Wählen Sie in diesem Beispiel das Feld **[!UICONTROL title (salutation)]** in der Tabelle **[!UICONTROL Profil]** bis **[!UICONTROL Kontext]** > **[!UICONTROL Echtzeit-Ereignis]** > **[!UICONTROL Ereignis-Kontext]**.

   ![](assets/message-center_7-enrichment.png)

1. Fügen Sie alle erforderlichen Felder ein.

   ![](assets/message-center_8.png)

1. Erzeugen Sie die Vorschau Ihrer Nachricht unter Verwendung des für dieses Ereignis konfigurierten Testprofils.

   Weiterführende Informationen zur Vorschauerzeugung finden Sie im Abschnitt [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md).

   ![](assets/message-center_9.png)

   Die Vorschau zeigt, dass die Personalisierungsfelder wie gewünscht die im Testprofil angegebenen Informationen wiedergeben. Weitere Informationen hierzu finden Sie unter Definieren eines bestimmten Profils](../../channels/using/publishing-transactional-message.md#defining-specific-test-profile).[

## Produktlisten in Transaktionsnachrichten verwenden           {#using-product-listings-in-a-transactional-message}

Sie können Produktlisten erstellen, die eine oder mehrere Datenkollektionen im Inhalt einer Transaktions-E-Mail referenzieren. Beispielsweise können Sie bei einem abgebrochenen Einkauf eine E-Mail versenden, in der alle Produkte samt Bild, Preis und Link aufgelistet sind, die sich beim Verlassen der Website im Warenkorb des Benutzers befanden.

>[!IMPORTANT]
>
>Produktlisten sind nur während der Bearbeitung von Transaktions-E-Mails in der Benutzeroberfläche von [Email Designer](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-interface) verfügbar.

Um eine Liste mit Produkten aus einem abgebrochenen Einkauf in eine Transaktionsnachricht einzufügen, folgen Sie den unten stehenden Schritten.

Sie können auch [diesen Videosatz](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/designing-content/product-listings-in-transactional-email.html?lang=en#configure-product-listings-in-transactional-emails) ansehen, in dem die Schritte erläutert werden, die zum Konfigurieren der Produktauflistungen in einer transaktionalen E-Mail erforderlich sind.

>[!NOTE]
>
>Adobe Campaign unterstützt keine verschachtelten Produktlisten, was bedeutet, dass Sie keine Produktliste in eine andere einfügen können.

### Produktliste definieren         {#defining-a-product-listing}

Damit Sie eine Produktliste in einer Transaktionsnachricht verwenden können, müssen Sie zuerst auf Ereignisebene die Liste der Produkte und die Felder für jedes Produkt der Liste definieren, die angezeigt werden sollen. Weiterführende Informationen dazu finden Sie im Abschnitt [Datenkollektionen definieren](../../channels/using/configuring-transactional-event.md#defining-data-collections).

1. Wählen Sie in der Transaktionsnachricht den jeweiligen **[!UICONTROL Inhaltsbaustein]** aus, um den E-Mail-Inhalt zu ändern.
1. Fügen Sie mit Drag &amp; Drop eine Strukturkomponente in den Arbeitsbereich ein. Weitere Informationen hierzu finden Sie unter [Definieren der E-Mail-Struktur](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

   Wählen Sie beispielsweise den einspaltigen Aufbau aus und fügen Sie eine Textkomponente, eine Bildkomponente und eine Schaltflächen-Komponente hinzu. Weitere Informationen hierzu finden Sie unter [Inhaltskomponenten](../../designing/using/designing-from-scratch.md#about-content-components) verwenden.

1. Wählen Sie die soeben erstellte Strukturkomponente und danach in der Symbolleiste das Symbol zum **[!UICONTROL Aktivieren einer Produktliste]** aus.

   ![](assets/message-center_loop_create.png)

   Die Strukturkomponente wird durch einen orangen Rahmen hervorgehoben und die Einstellungsoptionen für **[!UICONTROL Produktliste]** werden auf der linken Seite geöffnet.

   ![](assets/message-center_loop_palette.png)

1. Wählen Sie aus, wie die Elemente der Kollektion dargestellt werden sollen:

   * **[!UICONTROL Zeile]**: horizontal, also alle Elemente einer Reihe untereinander.
   * **[!UICONTROL Spalte]**: vertikal, also alle Elemente in einer Reihe nebeneinander.

   >[!NOTE]
   >
   >Die Option **[!UICONTROL Spalte]** ist nur verfügbar, wenn eine mehrspaltige Strukturkomponente verwendet wird (**[!UICONTROL 2-2-Spalte]**, **[!UICONTROL 3-3-Spalte]** und **[!UICONTROL 4-4-Spalte]** ). Füllen Sie bei der Bearbeitung der Produktliste nur die erste Spalte aus. Die anderen Spalten werden nicht berücksichtigt. Weitere Informationen zum Auswählen von Strukturkomponenten finden Sie unter [Definieren der E-Mail-Struktur](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

1. Wählen Sie die Datenkollektion aus, die Sie erstellt haben, als Sie das mit der Transaktionsnachricht in Verbindung stehende Ereignis konfiguriert haben. Sie finden sie im Knoten **[!UICONTROL Kontext]** > **[!UICONTROL Echtzeit-Ereignis]** > **[!UICONTROL Ereignis-Kontext]**.

   ![](assets/message-center_loop_selection.png)

   Weiterführende Informationen zur Konfiguration des Ereignisses finden Sie im Abschnitt [Datenkollektionen definieren](../../channels/using/configuring-transactional-event.md#defining-data-collections).

1. Wählen Sie in der Dropdown-Liste **[!UICONTROL 1. Element]** das Element aus, das in der Liste der E-Mail als erstes Element erscheinen soll.

   Wenn Sie z. B. &quot;2&quot; auswählen, wird das erste Element der Kollektion nicht in der E-Mail angezeigt. Die Produktliste beginnt in diesem Fall mit dem zweiten Element.

1. Wählen Sie die Höchstzahl der Elemente aus, die in der Liste angezeigt werden sollen.

   >[!NOTE]
   >
   >Wenn die Elemente in Ihrer Liste senkrecht dargestellt werden sollen (**[!UICONTROL Spalte]**), entspricht die Höchstzahl der Elemente der ausgewählten Strukturkomponente (2, 3 oder 4 Spalten). Weiterführende Informationen zur Auswahl von Strukturkomponenten finden Sie im Abschnitt zum [Bearbeiten des E-Mail-Aufbaus](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

### Produktliste befüllen         {#populating-the-product-listing}

Gehen Sie folgendermaßen vor, um eine Liste mit Produkten darzustellen, die von dem Ereignis stammen, das mit der Transaktions-E-Mail verknüpft ist.

Weiterführende Informationen zur Erstellung einer Kollektion und der entsprechenden Felder bei der Konfiguration des Ereignisses finden Sie unter [Datenkollektionen definieren](../../channels/using/configuring-transactional-event.md#defining-data-collections).

1. Wählen Sie die zuvor eingefügte Bildkomponente und dann **[!UICONTROL Personalisierung aktivieren]** aus. Wählen Sie danach das Stiftsymbol im Einstellungsbereich aus.

   ![](assets/message-center_loop_image.png)

1. Wählen Sie im sich öffnenden Fenster **[!UICONTROL Bildquellen-URL]** die Option **[!UICONTROL Personalisierungsfeld hinzufügen]** aus.

   Öffnen Sie im Knoten **[!UICONTROL Kontext]** > **[!UICONTROL Echtzeit-Ereignis]** > **[!UICONTROL Ereignis-Kontext]** den Knoten der von Ihnen erstellten Kollektion (hier **[!UICONTROL Produktliste]**) und wählen Sie das von Ihnen definierte Bild-Feld aus (hier **[!UICONTROL Produktbild]** ). Wählen Sie **[!UICONTROL Speichern]** aus.

   ![](assets/message-center_loop_product-image.png)

   Das von Ihnen ausgewählte Personalisierungsfeld wird jetzt im Einstellungsbereich angezeigt.

1. Wählen Sie in der dedizierten Symbolleiste an der gewünschten Position **[!UICONTROL Personalisierungsfeld einfügen]** aus.

   ![](assets/message-center_loop_product.png)

1. Öffnen Sie im Knoten **[!UICONTROL Kontext]** > **[!UICONTROL Echtzeit-Ereignis]** > **[!UICONTROL Ereignis-Kontext]** den Knoten der von Ihnen erstellten Kollektion (hier **[!UICONTROL Produktliste]**) und wählen Sie das von Ihnen erstellte Feld aus (hier **[!UICONTROL Produktname]**). Wählen Sie **[!UICONTROL Bestätigen]** aus.

   ![](assets/message-center_loop_product_node.png)

   Das von Ihnen ausgewählte Personalisierungsfeld wird jetzt an der gewünschten Position im E-Mail-Inhalt dargestellt.

1. Gehen Sie beim Einfügen des Preises analog vor.
1. Wählen Sie den Text und dann in der dedizierten Symbolleiste **[!UICONTROL Link einfügen]** aus.

   ![](assets/message-center_loop_link_insert.png)

1. Wählen Sie im sich öffnenden Fenster **[!UICONTROL Link einfügen]** die Option **[!UICONTROL Personalisierungsfeld hinzufügen]** aus.

   Öffnen Sie im Knoten **[!UICONTROL Kontext]** > **[!UICONTROL Echtzeit-Ereignis]** > **[!UICONTROL Ereignis-Kontext]** den Knoten der von Ihnen erstellten Kollektion (hier **[!UICONTROL Produktliste]**) und wählen Sie das von Ihnen erstellte URL-Feld aus (hier **[!UICONTROL Produkt-URL]**). Wählen Sie **[!UICONTROL Speichern]** aus.

   >[!IMPORTANT]
   >
   >Achten Sie aus Sicherheitsgründen darauf, dass Sie das Personalisierungsfeld in einen Link einfügen, der mit einem statischen Domain-Namen beginnt.

   ![](assets/message-center_loop_link_select.png)

   Das von Ihnen ausgewählte Personalisierungsfeld wird jetzt im Einstellungsbereich angezeigt.

1. Wählen Sie die Strukturkomponente aus, auf die die Produktliste angewendet wird, und wählen Sie danach **[!UICONTROL Fallback zeigen]** aus, um den Standardinhalt zu definieren.

   ![](assets/message-center_loop_fallback_show.png)

1. Ziehen Sie eine oder mehrere Inhaltskomponenten in den Arbeitsbereich und bearbeiten Sie sie nach Bedarf.

   ![](assets/message-center_loop_fallback.png)

   Der Fallback-Inhalt wird angezeigt, wenn die Kollektion beim Auslösen des Triggers leer ist. Das ist beispielsweise dann der Fall, wenn ein Kunde nichts im Warenkorb liegen hat.

1. Bearbeiten Sie im Einstellungsbereich den Stil der Produktliste. Weitere Informationen hierzu finden Sie unter [Verwalten von E-Mail-Stilen](../../designing/using/styles.md).
1. Sehen Sie sich die E-Mail in der Vorschau an, indem Sie ein Testprofil verwenden, das mit dem entsprechenden Transaktionsereignis verknüpft ist und für das Sie Kollektionsdaten definiert haben. Fügen Sie für das Testprofil, das Sie verwenden möchten, beispielsweise die folgenden Informationen zum Abschnitt **[!UICONTROL Ereignisdaten]** hinzu:

   ![](assets/message-center_loop_test-profile_payload.png)

   Weiterführende Informationen zur Definition eines Testprofils in einer Transaktionsnachricht finden Sie in [diesem Abschnitt](../../channels/using/publishing-transactional-message.md#defining-specific-test-profile).

## Profil-basierte Transaktionsnachricht-Spezifikationen {#profile-transactional-message-specificities}

Sie können Transaktionsnachrichten auf Grundlage von Kundenmarketing-Profilen senden, mit denen Sie alle Profil-Informationen nutzen können, um den Nachrichteninhalt zu personalisieren, den Link &quot;Abmeldung&quot;zu verwenden und Marketingregeln wie [Ermüdungsregeln](../../sending/using/fatigue-rules.md) anzuwenden.

* Weitere Informationen zu den Unterschieden zwischen Ereignis- und Profil-basierten Transaktionsnachrichten finden Sie in [diesem Abschnitt](../../channels/using/getting-started-with-transactional-msg.md#transactional-message-types).

* Die Konfigurationsschritte zum Erstellen einer Profil-basierten Transaktionsnachricht sind in [diesem Abschnitt ](../../channels/using/configuring-transactional-event.md#profile-based-transactional-messages) beschrieben.

### Bearbeiten einer Profil-Transaktionsnachricht {#editing-profile-transactional-message}

Die Schritte zum Erstellen, Anpassen und Veröffentlichen einer Profil-Transaktionsnachricht sind meist die gleichen wie bei einer Ereignis-Transaktionsnachricht.

Die Unterschiede sind unten aufgeführt.

1. [Rufen Sie die erstellte Transaktionsnachricht auf, um sie zu bearbeiten.](#accessing-transactional-messages)
1. Wählen Sie in der Transaktionsnachricht den Bereich **[!UICONTROL Inhalt]** aus. Zusätzlich zu den transaktionalen E-Mail-Vorlagen können Sie auch eine beliebige E-Mail-Vorlage für die **[!UICONTROL Profil]**-Ressource auswählen.

   ![](assets/message-center_marketing_templates.png)

1. Wählen Sie die Standard-E-Mail-Vorlage aus. Ähnlich wie alle Marketing-E-Mails enthält es einen **Link &quot;Abmeldung**&quot;.

   ![](assets/message-center_marketing_perso_unsubscription.png)

   Weitere Informationen zu Vorlagen finden Sie in [diesem Abschnitt](../../designing/using/using-reusable-content.md#content-templates).

1. Im Gegensatz zu Konfigurationen, die auf Echtzeit-Ereignissen basieren, haben Sie **direkten Zugriff auf alle Profil-Informationen**, um Ihre Nachricht zu personalisieren. Sie können [Personalisierungsfelder](../../designing/using/personalization.md#inserting-a-personalization-field) wie bei jeder anderen Standard-Marketing-E-Mail hinzufügen.

1. Speichern Sie Ihre Änderungen, bevor Sie die Nachricht veröffentlichen. Weiterführende Informationen dazu finden Sie unter [Transaktionsnachricht publizieren](../../channels/using/publishing-transactional-message.md#publishing-a-transactional-message).

### Versand einer Profil-Transaktionsnachricht verfolgen        {#monitoring-a-profile-transactional-message-delivery}

Nachdem die Nachricht publiziert wurde und Ihre Webseiten-Integration abgeschlossen ist, kann der Versand verfolgt werden.

1. Der Zugriff auf den Versandlog der Nachricht ist über die Schaltfläche rechts unten in der **[!UICONTROL Freigabe]**-Kachel möglich.

   Weitere Informationen zum Zugriff auf die Protokolle finden Sie unter [Überwachen eines Versands](../../sending/using/monitoring-a-delivery.md).

1. Wählen Sie den Tab **[!UICONTROL Versandlogs]** aus. In der **[!UICONTROL Status]**-Spalte zeigt **[!UICONTROL Gesendet]** an, dass sich ein Profil angemeldet hat.

   ![](assets/message-center_marketing_sending_logs.png)

1. Wählen Sie den Tab **[!UICONTROL Ausschlusslogs]** aus, um die Empfänger anzuzeigen, die von der Versandzielgruppe ausgeschlossen wurden, wie zum Beispiel Adressen auf der Blockierungsliste.

   ![](assets/message-center_marketing_exclusion_logs.png)

Profile, die sich abgemeldet haben, wurden durch die Typologieregel **[!UICONTROL Adresse auf Blockierungsliste]** ausgeschlossen.

Diese Regel ist Teil einer spezifischen Typologie, die für alle auf der **[!UICONTROL Profil]**-Tabelle basierenden Transaktionsnachrichten gilt.

![](assets/message-center_marketing_typology.png)

**Verwandte Themen**:

* Integrate-Ereignis-Triggerung(../../channels/using/getting-started-with-transactional-msg.md#integrate-Ereignis-trigger)
* [Über Typologien und Typologieregeln](../../sending/using/about-typology-rules.md)

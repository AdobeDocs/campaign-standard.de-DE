---
title: Ereignis-Transaktionsnachrichten
description: Hier erfahren Sie, wie Sie eine Ereignis-Transaktionsnachricht erstellen und publizieren.
page-status-flag: never-activated
uuid: d747feb5-58fb-4e12-a176-404f0eca5391
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: transactional-messaging
discoiquuid: 4f6317a1-9dfe-4714-bc1c-393629d855cd
context-tags: deliveryTransactionalTemplate,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 816d550d8bd0de085a47f97c1f6cc2fbb5e7acb9
workflow-type: tm+mt
source-wordcount: '2626'
ht-degree: 93%

---


# Ereignis-Transaktionsnachrichten{#event-transactional-messages}

Sie können Ereignis-Transaktionsnachrichten senden, die auf der Basis eines Ereignisses ausgewählt werden. Diese Art von Transaktionsnachrichten enthält keine Profilinformationen: Die Versandzielgruppe wird durch Daten definiert, die im Ereignis selbst enthalten sind.

Nach der Erstellung und Publikation des gewünschten Ereignisses (&quot;Stehen gelassener Warenkorb&quot; wie in [diesem Abschnitt](../../channels/using/about-transactional-messaging.md#transactional-messaging-operating-principle) beschrieben) wird die entsprechende Transaktionsnachricht automatisch erstellt.

Die Konfigurationsschritte finden Sie im Abschnitt [Ereignis konfigurieren, um eine Transaktionsnachricht zu senden](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message).

Damit das Ereignis mit dem Versand einer Transaktionsnachricht einhergeht, muss diese Nachricht personalisiert, getestet und dann publiziert werden.

>[!NOTE]
>
>Sie können nur dann auf Transaktionsnachrichten zugreifen, wenn Sie der Sicherheitsgruppe **[!UICONTROL Administratoren (alle Einheiten)]** angehören.
>
>Ereignis-Transaktionsnachrichten enthalten keine Profilinformationen, weshalb sie nicht mit Ermüdungsregeln kompatibel sind (auch nicht, wenn sie mit Profilen angereichert werden). Näheres dazu finden Sie unter [Ermüdungsregeln](../../sending/using/fatigue-rules.md#choosing-the-channel).

## Testprofil in einer Transaktionsnachricht definieren    {#defining-a-test-profile-in-a-transactional-message}

Konfigurieren Sie ein entsprechendes Testprofil, mit dem Sie zum Zweck der Validierung eine Vorschau Ihrer Nachricht sowie einen Testversand erzeugen können.

### Testprofil in einer Transaktionsnachricht erstellen    {#creating-a-test-profile-within-the-transactional-----------message}

1. Gehen Sie zum Zugriff auf die neu erstellte Nachricht mithilfe des **[!UICONTROL Adobe-Campaign]**-Logos oben links im Bildschirm in das Menü **[!UICONTROL Marketingpläne]** > **[!UICONTROL Transaktionsnachrichten]** > **[!UICONTROL Transaktionsnachrichten]**.

   ![](assets/message-center_4.png)

1. Erstellen Sie ein Testprofil, das mit Ihrem Ereignis verknüpft wird.

   ![](assets/message-center_test-profile.png)

1. Geben Sie im Bereich **[!UICONTROL Für die Personalisierung verwendete Ereignisdaten]** die zu übermittelnden Daten im JSON-Format an. Bei den angegebenen Daten handelt es sich um den Inhalt, der in der Vorschau verwendet und dem Testprofil im Testversand übermittelt wird.

   ![](assets/message-center_event-data.png)

   >[!NOTE]
   >
   >Sie können auch die Information von der Profiltabelle eingeben. Siehe [Inhalt der Transaktionsnachricht anreichern](../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content).

1. Nach seiner Erstellung ist das Testprofil in der Transaktionsnachricht vorausgefüllt. Verwenden Sie die Kachel **[!UICONTROL Testprofile]** der Nachricht, um Ihre Testversand-Zielgruppe zu überprüfen.

   ![](assets/message-center_5.png)

### Testprofil außerhalb einer Transaktionsnachricht erstellen {#creating-a-test-profile-outside-the-transactional-----------message}

Sie haben außerdem die Möglichkeit, ausgehend vom Menü **[!UICONTROL Testprofile]** ein neues Testprofil zu erstellen bzw. ein bereits existierendes zu verwenden.

1. Verwenden Sie hierzu das **[!UICONTROL Adobe-Campaign]**-Logo oben links im Bildschirm und anschließend die Schaltflächen **[!UICONTROL Profile &amp; Audiences]** > **[!UICONTROL Testprofile]**.
1. Wählen Sie auf der Seite Ihres gewünschten Testprofils im Abschnitt **[!UICONTROL Ereignis]** das Ereignis aus, das Sie erstellt haben. Im vorliegenden Beispiel handelt es sich um &quot;Warenkorbabbruch (EVTcartAbandonment)&quot;.
1. Geben Sie im Tab **[!UICONTROL Ereignisdaten]** im Texteditor die zu übermittelnden Daten im JSON-Format an.

   ![](assets/message-center_3.png)

1. Speichern Sie Ihre Änderungen.

Jetzt können Sie auf die von Ihnen erstellte Nachricht zugreifen und das aktualisierte Testprofil auswählen.

**Verwandte Themen:**

* [Verwaltung von Testprofilen](../../audiences/using/managing-test-profiles.md)
* [Audiences bestimmen](../../audiences/using/creating-audiences.md)

## Transaktionsnachricht personalisieren    {#personalizing-a-transactional-message}

Gehen Sie folgendermaßen vor, um für eine Transaktionsnachricht eine Personalisierung einzurichten:

1. Öffnen Sie mithilfe der gleichnamigen Kachel den **[!UICONTROL Inhalt]** der Nachricht, um den Betreff und den Inhalt anzupassen. Wählen Sie für dieses Beispiel eine Vorlage aus, die Bilder und Text enthält. Weiterführende Informationen zu E-Mail-Inhaltsvorlagen finden Sie unter [Erstellen mit Vorlagen](../../designing/using/using-reusable-content.md#designing-templates).

   ![](assets/message-center_6.png)

1. Fügen Sie einen Betreff hinzu und bearbeiten Sie den Inhalt Ihrer Nachricht entsprechend Ihren Anforderungen.

   >[HINWEIS]
   >
   >Bei dem Link zum stehen gelassenen Warenkorb handelt es sich um einen Link auf eine externe URL, die den Kunden zu seinem Warenkorb weiterleitet. Diese Konfiguration wird außerhalb von Adobe Campaign vorgenommen.

1. In unserem Beispiel möchten Sie drei Felder hinzufügen, die Sie beim [Erstellen des Ereignisses](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message) definiert haben: Vorname, letztes angesehenes Produkt, Gesamtbetrag des Warenkorbs. Fügen Sie dazu ein [Personalisierungsfeld](../../designing/using/personalization.md#inserting-a-personalization-field) in den Nachrichteninhalt ein.

1. Gehen Sie zu diesen Feldern über **[!UICONTROL Kontext]** > **[!UICONTROL Echtzeit-Ereignis]** > **[!UICONTROL Ereigniskontext]**.

   ![](assets/message-center_7.png)

1. Fügen Sie dann zur Anreicherung Ihres Nachrichteninhalts die gewünschten Felder hinzu, indem Sie diese in der Tabelle auswählen, mit der Sie Ihr Ereignis verknüpft haben. Wählen Sie für unser Beispiel das Feld **[!UICONTROL Titel (Anrede)]** in der Tabelle **[!UICONTROL Profil]**&#x200B;über **[!UICONTROL Kontext]** > **[!UICONTROL Echtzeit-Ereignis]****[!UICONTROL > Ereigniskontext]** aus.

   ![](assets/message-center_7-enrichment.png)

1. Fügen Sie alle erforderlichen Felder ein.

   ![](assets/message-center_8.png)

1. Erzeugen Sie die Vorschau Ihrer Nachricht unter Verwendung des für dieses Ereignis konfigurierten Testprofils.

   Weiterführende Informationen zur Vorschauerzeugung finden Sie im Abschnitt [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md).

   ![](assets/message-center_9.png)

   Die Vorschau zeigt, dass die Personalisierungsfelder wie gewünscht die im Testprofil angegebenen Informationen wiedergeben. Weiterführende Informationen hierzu finden Sie im Abschnitt [Testprofil in einer Transaktionsnachricht definieren](#defining-a-test-profile-in-a-transactional-message).

## Produktlisten in Transaktionsnachrichten verwenden    {#using-product-listings-in-a-transactional-message}

Sie können Produktlisten erstellen, die eine oder mehrere Datenkollektionen im Inhalt einer Transaktions-E-Mail referenzieren. Beispielsweise können Sie bei einem abgebrochenen Einkauf eine E-Mail versenden, in der alle Produkte samt Bild, Preis und Link aufgelistet sind, die sich beim Verlassen der Website im Warenkorb des Benutzers befanden.

>[!IMPORTANT]
>
>Produktlisten sind nur während der Bearbeitung von Transaktions-E-Mails in der Benutzeroberfläche von [Email Designer](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-interface) verfügbar.

Um eine Liste mit Produkten aus einem abgebrochenen Einkauf in eine Transaktionsnachricht einzufügen, folgen Sie den unten stehenden Schritten.

Sie können sich die erforderlichen Schritte zur Konfiguration von Produktlisten in einer Transaktions-E-Mail auch in Videos ansehen. Weiterführende Informationen hierzu finden Sie auf [dieser Seite](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/designing-content/product-listings-in-transactional-email.html).

>[!NOTE]
>
>Adobe Campaign unterstützt keine verschachtelten Produktlisten, was bedeutet, dass Sie keine Produktliste in eine andere einfügen können.

### Produktliste definieren    {#defining-a-product-listing}

Damit Sie eine Produktliste in einer Transaktionsnachricht verwenden können, müssen Sie zuerst auf Ereignisebene die Liste der Produkte und die Felder für jedes Produkt der Liste definieren, die angezeigt werden sollen. Weiterführende Informationen dazu finden Sie im Abschnitt [Datenkollektionen definieren](../../administration/using/configuring-transactional-messaging.md#defining-data-collections).

1. Wählen Sie in der Transaktionsnachricht den jeweiligen **[!UICONTROL Inhaltsbaustein]** aus, um den E-Mail-Inhalt zu ändern.
1. Fügen Sie mit Drag &amp; Drop eine Strukturkomponente in den Arbeitsbereich ein. Weiterführende Informationen dazu finden Sie im Abschnitt zum [Bearbeiten des E-Mail-Aufbaus](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

   Wählen Sie beispielsweise den einspaltigen Aufbau aus und fügen Sie eine Textkomponente, eine Bildkomponente und eine Schaltflächen-Komponente hinzu. Weiterführende Informationen dazu finden Sie im Abschnitt [Fragmente und Inhaltskomponenten hinzufügen](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

1. Wählen Sie die soeben erstellte Strukturkomponente und danach in der Symbolleiste das Symbol zum **[!UICONTROL Aktivieren einer Produktliste]** aus.

   ![](assets/message-center_loop_create.png)

   Die Strukturkomponente wird durch einen orangen Rahmen hervorgehoben und die Einstellungsoptionen für **[!UICONTROL Produktliste]** werden auf der linken Seite geöffnet.

   ![](assets/message-center_loop_palette.png)

1. Wählen Sie aus, wie die Elemente der Kollektion dargestellt werden sollen:

   * **[!UICONTROL Zeile]**: horizontal, also alle Elemente einer Reihe untereinander.
   * **[!UICONTROL Spalte]**: vertikal, also alle Elemente in einer Reihe nebeneinander.
   >[!NOTE]
   >
   >Die Option **[!UICONTROL Spalte]** ist nur verfügbar, wenn eine mehrspaltige Strukturkomponente verwendet wird (**[!UICONTROL 2-2-Spalte]**, **[!UICONTROL 3-3-Spalte]** und **[!UICONTROL 4-4-Spalte]** ). Füllen Sie bei der Bearbeitung der Produktliste nur die erste Spalte aus. Die anderen Spalten werden nicht berücksichtigt. Weiterführende Informationen zur Auswahl von Strukturkomponenten finden Sie im Abschnitt zum [Bearbeiten des E-Mail-Aufbaus](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

1. Wählen Sie die Datenkollektion aus, die Sie erstellt haben, als Sie das mit der Transaktionsnachricht in Verbindung stehende Ereignis konfiguriert haben. Sie finden sie im Knoten **[!UICONTROL Kontext]** > **[!UICONTROL Echtzeit-Ereignis]** > **[!UICONTROL Ereignis-Kontext]**.

   ![](assets/message-center_loop_selection.png)

   Weiterführende Informationen zur Konfiguration des Ereignisses finden Sie im Abschnitt [Datenkollektionen definieren](../../administration/using/configuring-transactional-messaging.md#defining-data-collections).

1. Wählen Sie in der Dropdown-Liste **[!UICONTROL 1. Element]** das Element aus, das in der Liste der E-Mail als erstes Element erscheinen soll.

   Wenn Sie z. B. &quot;2&quot; auswählen, wird das erste Element der Kollektion nicht in der E-Mail angezeigt. Die Produktliste beginnt in diesem Fall mit dem zweiten Element.

1. Wählen Sie die Höchstzahl der Elemente aus, die in der Liste angezeigt werden sollen.

   >[!NOTE]
   >
   >Wenn die Elemente in Ihrer Liste senkrecht dargestellt werden sollen (**[!UICONTROL Spalte]**), entspricht die Höchstzahl der Elemente der ausgewählten Strukturkomponente (2, 3 oder 4 Spalten). Weiterführende Informationen zur Auswahl von Strukturkomponenten finden Sie im Abschnitt zum [Bearbeiten des E-Mail-Aufbaus](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

### Produktliste befüllen    {#populating-the-product-listing}

Gehen Sie folgendermaßen vor, um eine Liste mit Produkten darzustellen, die von dem Ereignis stammen, das mit der Transaktions-E-Mail verknüpft ist.

Weiterführende Informationen zur Erstellung einer Kollektion und der entsprechenden Felder bei der Konfiguration des Ereignisses finden Sie unter [Datenkollektionen definieren](../../administration/using/configuring-transactional-messaging.md#defining-data-collections).

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

1. Bearbeiten Sie im Einstellungsbereich den Stil der Produktliste. Weiterführende Informationen dazu finden Sie im Abschnitt [E-Mail-Stile bearbeiten](../../designing/using/styles.md).
1. Sehen Sie sich die E-Mail in der Vorschau an, indem Sie ein Testprofil verwenden, das mit dem entsprechenden Transaktionsereignis verknüpft ist und für das Sie Kollektionsdaten definiert haben. Fügen Sie für das Testprofil, das Sie verwenden möchten, beispielsweise die folgenden Informationen zum Abschnitt **[!UICONTROL Ereignisdaten]** hinzu:

   ![](assets/message-center_loop_test-profile_payload.png)

   Weiterführende Informationen zur Definition eines Testprofils in einer Transaktionsnachricht finden Sie in [diesem Abschnitt](#defining-a-test-profile-in-a-transactional-message).

## Transaktionsnachricht testen {#testing-a-transactional-message}

Nach Speicherung der Transaktionsnachricht können Sie nun einen Test senden.

![](assets/message-center_10.png)

Lesen Sie diesbezüglich auch den Abschnitt [Testversand erzeugen](../../sending/using/sending-proofs.md).

## Transaktionsnachricht publizieren    {#publishing-a-transactional-message}

Nach Validierung der Transaktionsnachricht kann diese publiziert werden.

![](assets/message-center_12.png)

Bei jeder Auslösung des Ereignisses &quot;Stehen gelassener Warenkorb&quot; wird nun automatisch eine Nachricht hinzugefügt, die die Anrede und den Namen des Empfängers, die URL des Warenkorbs, den zuletzt hinzugefügten Artikel bzw. eine Produktliste, falls eine Produktliste definiert wurde, sowie den Gesamtbetrag des Warenkorbs enthält.

Über die Schaltfläche **[!UICONTROL Berichte]** können Sie auf Statistiken zur entsprechenden Transaktionsnachricht zugreifen. Siehe [Berichte](../../reporting/using/about-dynamic-reports.md).

![](assets/message-center_13.png)

## Publikation einer Transaktionsnachricht aussetzen    {#suspending-a-transactional-message-publication}

Sie haben die Möglichkeit, die Publikation Ihrer Transaktionsnachricht mittels der Verwendung der Schaltfläche **[!UICONTROL Aussetzen]** zeitweise zu unterbinden, um beispielsweise die in der Nachricht enthaltenen Daten abzuändern. Die Ereignisse werden so nicht länger verarbeitet, sondern stattdessen in einer Warteschlange der Adobe Campaign-Datenbank aufbewahrt.

Die in der Warteschlange befindlichen Ereignisse werden für einen Zeitraum aufbewahrt, der in der REST-API (siehe [REST-API-Dokumentation](../../api/using/get-started-apis.md)) oder im Trigger-Ereignis definiert ist, wenn Sie den Triggers Core Service verwenden (siehe [Campaign- und Experience Cloud-Triggers verwenden](../../integrating/using/about-adobe-experience-cloud-triggers.md)).

![](assets/message-center_pause.png)

Bei Verwendung der Schaltfläche **[!UICONTROL Wieder aufnehmen]** werden alle Ereignisse verarbeitet, sofern ihre Gültigkeit nicht abgelaufen ist. Diese Nachrichten beinhalten nun die während der Aussetzung der Vorlagenpublikation vorgenommenen Änderungen.

## Transaktionsnachricht depublizieren    {#unpublishing-a-transactional-message}

Mithilfe der **[!UICONTROL Depublizieren]**-Schaltfläche lässt sich die Publikation der Transaktionsnachricht und zudem des entsprechenden Ereignisses abbrechen, wodurch auch die Ressource aus der REST-API gelöscht wird, die dem zuvor von Ihnen erstellten Ereignis entspricht.

![](assets/message-center_unpublish-template.png)

Selbst wenn das Ereignis auf Ihrer Webseite ausgelöst wird, werden die entsprechenden Nachrichten nun nicht mehr gesendet und auch nicht in der Datenbank gespeichert.

>[!NOTE]
>
>Zur erneuten Publikation der Nachricht müssen Sie zunächst zur entsprechenden Ereigniskonfiguration zurückkehren und diese veröffentlichen, bevor Sie die Nachricht veröffentlichen. Weiterführende Informationen dazu finden Sie unter [Transaktionsnachricht publizieren](#publishing-a-transactional-message).

Wenn Sie eine ausgesetzte Transaktionsnachricht depublizieren, müssen Sie ggf. bis zu 24 Stunden warten, bevor Sie sie erneut publizieren können. In dieser Zeit können alle in die Warteschlange gesendeten Ereignisse durch den **[!UICONTROL Datenbankbereinigung]**-Workflow (cleanup) entfernt werden.

Die Vorgehensweise zum Aussetzen einer Nachricht wird im Abschnitt [Publikation einer Transaktionsnachricht aussetzen](#suspending-a-transactional-message-publication) beschrieben.

Auf den Workflow **[!UICONTROL Datenbankbereinigung]**, der standardmäßig jeden Tag um 4 Uhr gestartet wird, kann über das Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungsparameter]** > **[!UICONTROL Workflows]** zugegriffen werden.

## Transaktionsnachricht löschen {#deleting-a-transactional-message}

Nachdem die Veröffentlichung einer Transaktionsnachricht rückgängig gemacht wurde oder eine Transaktionsnachricht noch nicht veröffentlicht wurde, können Sie sie aus der Liste &quot;Transaktionsnachricht&quot;löschen. Gehen Sie dazu wie folgt vor:

1. Verwenden Sie das **[!UICONTROL Adobe-Campaign]**-Logo oben links im Bildschirm und anschließend die Schaltflächen **[!UICONTROL Marketingpläne]** > **[!UICONTROL Transaktionsnachrichten]** > **[!UICONTROL Transaktionsnachrichten]**.
1. Bewegen Sie die Maus über die Nachricht Ihrer Wahl.
1. Click the **[!UICONTROL Delete element]** button.

![](assets/message-center_delete-template.png)

Transaktionsnachrichten können jedoch nur unter gewissen Voraussetzungen gelöscht werden:

* Make sure the transactional message has the **[!UICONTROL Draft]** status, otherwise you will not be able to delete it. The **[!UICONTROL Draft]** status applies to a message that has not been published yet, or that has been [unpublished](#unpublishing-a-transactional-message) (and not [paused](#suspending-a-transactional-message-publication)).

* **Transaktionsnachrichten**: Wenn keine andere Transaktionsnachricht mit dem entsprechenden Ereignis verknüpft ist und die Veröffentlichung der Transaktionsnachricht rückgängig gemacht wird, muss auch die Veröffentlichung der Ereignis-Konfiguration rückgängig gemacht werden, damit die Transaktionsnachricht erfolgreich gelöscht werden kann. Weitere Informationen finden Sie unter [Rückgängigmachen der Veröffentlichung eines Ereignisses](../../administration/using/configuring-transactional-messaging.md#unpublishing-an-event).

   >[!IMPORTANT]
   >
   >Durch das Löschen einer Transaktionsnachricht, über die bereits Benachrichtigungen versendet wurden, werden auch ihre Versand- und Trackinglogs gelöscht.

* **Transaktionsnachrichten aus einer vordefinierten Ereignis-Vorlage (interne Transaktionsnachrichten)**: Ist eine interne Transaktionsnachricht die einzige, die mit dem entsprechenden internen Ereignis verknüpft ist, kann sie nicht gelöscht werden. Sie müssen zuerst eine andere Transaktionsnachricht erstellen, indem Sie sie duplizieren oder über das Menü **[!UICONTROL Ressourcen]** > **[!UICONTROL Vorlagen]** > **[!UICONTROL Transaktionsnachrichtenvorlagen]** .

## Transaktionsnachricht erneut versenden    {#transactional-message-retry-process}

Vorläufig nicht zugestellte Transaktionsnachrichten werden so lange automatisch erneut versendet, bis ihre Gültigkeit abgelaufen ist. Weiterführende Informationen zur Versandlaufzeit finden Sie in Abschnitt [Parameter für den Gültigkeitszeitraum](../../administration/using/configuring-email-channel.md#validity-period-parameters).

Wenn eine Transaktionsnachricht nicht gesendet werden kann, gibt es zwei Systeme, durch die erneute Zustellversuche unternommen werden.

* Auf der Ebene der Transaktionsnachrichten kann eine Transaktionsnachricht fehlschlagen, bevor das Ereignis einem Ausführungsversand zugewiesen wurde, d. h. zwischen dem Ereignisempfang und der Versandvorbereitung. Siehe [Wiederholungsverfahren bei der Ereignisverarbeitung](#event-processing-retry-process).
* Auf der Ebene des Versandverfahrens kann die Transaktionsnachricht nach der Zuweisung des Ereignisses zu einem Ausführungsversand wegen eines temporären Fehlers fehlschlagen. Siehe [Wiederholungsverfahren beim Nachrichtenversand](#message-sending-retry-process).

### Wiederholungsverfahren bei der Ereignisverarbeitung    {#event-processing-retry-process}

Wenn ein Ereignis keinem Ausführungsversand zugewiesen werden kann, wird die Ereignisverarbeitung verschoben. Wiederholungen werden dann durchgeführt, bis das Ereignis einem neuen Ausführungsversand zugewiesen wird.

>[!NOTE]
>
>Ein verschobenes Ereignis wird nicht in den Versandlogs für Transaktionsnachrichten angezeigt, weil das Ereignis noch keinem Ausführungsversand zugeordnet ist.

Beispielsweise kann es sein, dass das Ereignis keinem Ausführungsversand zugewiesen werden konnte, weil der Inhalt nicht korrekt war, es ein Problem mit den Zugriffsrechten oder dem Branding gab oder ein Fehler beim Anwenden von Typologieregeln erkannt wurde. In diesem Fall können Sie die Nachricht vorläufig anhalten, bearbeiten, um den Fehler zu beheben, und erneut publizieren. Das Wiederholungssystem weist die Nachricht daraufhin einem neuen Ausführungsversand zu.

### Wiederholungsverfahren beim Nachrichtenversand    {#message-sending-retry-process}

Nachdem das Ereignis einem Ausführungsversand zugewiesen wurde, kann die Transaktionsnachricht aufgrund eines temporären Fehlers fehlschlagen, z. B. falls das Postfach des Empfängers voll ist. Weiterführende Informationen dazu finden Sie in Abschnitt [Weitere Zustellversuche nach einem vorübergehend fehlgeschlagenen Versand](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).

>[!NOTE]
>
>Wenn ein Ereignis einem Ausführungsversand zugewiesen wird, wird es nur dieses eine Mal in den Versandlogs dieses Ausführungsversands angezeigt. Die fehlgeschlagenen Sendungen werden im Tab **[!UICONTROL Liste der Ausführungen]** der Transaktionsnachricht angezeigt.

### Einschränkungen {#limitations}

**Aktualisierung der Versandlogs**

Im Wiederholungsvorgang werden die Versandlogs des neuen Ausführungsversands nicht sofort aktualisiert (die Aktualisierung erfolgt über einen zeitversetzten Workflow). Das bedeutet, dass die Nachricht den Status **[!UICONTROL Ausstehend]** aufweisen könnte, selbst wenn das Transaktionsereignis vom neuen Ausführungsversand verarbeitet worden ist.

**Fehlgeschlagener Ausführungsversand**

Ein Ausführungsversand kann nicht angehalten werden. Wenn jedoch ein aktueller Ausführungsversand fehlschlägt, wird ein neuer erstellt, sobald ein neues Ereignis empfangen wird, und alle neuen Ereignisse werden von diesem neuen Ausführungsversand verarbeitet. Vom fehlgeschlagenen Ausführungsversand werden keine neuen Ereignisse verarbeitet.

Wenn manche, einem Ausführungsversand bereits zugewiesenen Ereignisse verschoben wurden und dieser Ausführungsversand fehlschlägt, weist das Wiederholungssystem dem neuen Ausführungsversand nicht die verschobenen Ereignisse zu. Diese Ereignisse gehen verloren.

---
title: Confirming subscription to a service
seo-title: Bestätigung des Abonnements für einen Dienst
description: Confirming subscription to a service
seo-description: Führen Sie die folgenden Schritte aus, um eine Bestätigungsmeldung für Profile einzurichten, die einen Dienst in Adobe Campaign abonnieren.
page-status-flag: never-activated
uuid: 23e6c4c2-e2c7-472f-b616-36a95225ac1d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-subscriptions
discoiquuid: 1a24504e-7f9d-4297-b39e-c5f085b0f388
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 8b85bbad7458286252a2900ce730288f6e52442e

---


# Bestätigung des Abonnements für einen Dienst{#confirming-subscription-to-a-service}

## Informationen zum Senden der Abonnementbestätigung {#sending-subscription-confirmation}

In diesem Abschnitt wird beschrieben, wie Sie eine automatische benutzerdefinierte Bestätigungs-E-Mail an die Profile senden, die einen bestimmten Dienst abonnieren.

Wenn Sie eine Bestätigungsnachricht für ein Abonnement (oder eine Rückmeldung) an einen Dienst senden möchten, können Sie die Standardnachricht oder eine benutzerdefinierte Nachricht verwenden. Die Schritte zur Auswahl einer Bestätigungsmeldung finden Sie im Abschnitt [Erstellen eines Dienstes](../../audiences/using/creating-a-service.md) .

Wenn Sie die Standardnachricht verwenden, können Sie deren Inhalt mit folgenden Einschränkungen bearbeiten:
* Sie können den Inhalt der Nachricht nur mit begrenzten Feldern aus dem Ereigniskontext personalisieren.
* Diese Meldung ist für alle Dienste identisch, die den Standardmodus verwenden.

Um eine bestimmte Bestätigungs-E-Mail für einen bestimmten Dienst zu senden, können Sie eine benutzerdefinierte Nachricht erstellen, in der Sie auch Personalisierungsfelder aus anderen Ressourcen nutzen können. Dazu müssen Sie eine Transaktionsmeldung erstellen und konfigurieren. Diese Meldung kann referenziert werden:
* Vom Dienst selbst. Weitere Informationen hierzu finden Sie unter [Konfigurieren der Bestätigungsmeldung von einem Dienst](../../audiences/using/confirming-subscription-to-a-service.md#configuring-confirmation-message-from-service).
* From a subscription landing page. Weitere Informationen hierzu finden Sie unter [Konfigurieren der Bestätigungsmeldung von einer Einstiegsseite](../../audiences/using/confirming-subscription-to-a-service.md#configuring-confirmation-message-from-landing-page).

## Konfigurieren der Bestätigungsmeldung eines Dienstes {#configuring-confirmation-message-from-service}

Beispielsweise möchten Sie den Besuchern Ihrer Website automatisch eine Bestätigungsmeldung senden, wenn sie Ihren Marken-Newsletter abonnieren.

Sie müssen eine transaktionssichere E-Mail konfigurieren und auf diese Nachricht vom gewünschten Dienst (in diesem Fall Abonnement für Ihren Marken-Newsletter) verweisen. Um die Transaktionsnachricht mit Dienstinformationen zu bereichern, können Sie beim Erstellen des Ereignisses eine Absöhnung definieren.

Beim Konfigurieren des Dienstes wird die Transaktionsnachricht zur Bestätigung nur dann gesendet, wenn jeder Besucher diesen Dienst zum ersten Mal abonniert. Wenn bereits ein Profil abonniert wurde, wird keine Bestätigungsmeldung erneut an dieses Profil gesendet.

### Schritt 1: Bestätigungs-E-Mail erstellen   {#step-1--create-the-confirmation-email-1}

Eine Bestätigungs-E-Mail wird automatisch an jedes Profil gesendet, das den Newsletter abonniert (über eine Landingpage oder andere Mittel). Das Abonnement gilt als Ereignis und die E-Mail ist eine [Transaktionsnachricht](../../channels/using/about-transactional-messaging.md) , die jedes Profil, das den Dienst abonniert, als Ziel hat.

Die Schritte zum Erstellen der Bestätigungs-E-Mail werden nachfolgend beschrieben. Da die Transaktionsnachricht im Dienst referenziert wird, müssen Sie sie zuerst erstellen.

#### Ereignis erstellen    {#create-the-event-1}

The confirmation email is a transactional message as it reacts to an event: the subscription to a service. Diese Meldung wird gesendet, um das Abonnement für Ihren Newsletter zu bestätigen.

1. Create an event from the **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]** &gt; **[!UICONTROL Event configuration]** menu, accessible from the Adobe Campaign logo.
1. Geben Sie eine Bezeichnung ein, wählen Sie eine Targeting-Dimension und klicken Sie auf **[!UICONTROL Erstellen]**.

   The configuration steps are presented in the Configuring transactional messaging section.[](../../administration/using/configuring-transactional-messaging.md)

1. In the **[!UICONTROL Fields]** section, click **[!UICONTROL Create element]** and add **[!UICONTROL publicLabel]** to the data structure in order to enable reconciliation.

   ![](assets/confirmation_publicLabel-field.png)

   >[HINWEIS]
   >
   >The **[!UICONTROL publicLabel]** field is mandatory. Wenn Sie sie nicht zur Ereignisdatenstruktur hinzufügen, kann Adobe Campaign keine Abstimmung mit dem Dienst durchführen. When subscribing to a service, this field will be filled with the Service label of the corresponding service.****

1. In the **[!UICONTROL Enrichment]** section, click **[!UICONTROL Create element]** and select the **[!UICONTROL Service]** target resource.

   ![](assets/confirmation_enrichment-service.png)

1. In the Join definition section, map the publicLabel field of the Service resource with the publicLabel field of the event configuration.****************

   ![](assets/confirmation_publicLabel-join.png)

   >[HINWEIS]
   >
   >Auf diese Weise können Sie Personalisierungsfelder aus der **[!UICONTROL Dienstressource]** in der Transaktionsmeldung verwenden.

1. Save the event configuration and click Publish to publish the event.****

Das Ereignis ist somit fertig eingerichtet. Sie können nun die transaktionelle E-Mail-Nachricht entwerfen.

#### Bestätigungsnachricht erstellen    {#design-the-confirmation-message-1}

The confirmation email is a transactional message based on the event that you just published.

1. Wählen Sie ausgehend vom Adobe Campaign-Logo die Option **[!UICONTROL Marketingpläne]** &gt; **[!UICONTROL Transaktionsnachrichten]** und nochmals **[!UICONTROL Transaktionsnachrichten]**.
1. Select the transactional email corresponding to the event that you just published.

1. Click the Content section and select an email template. **** For more on editing a transactional message content, see [Event transactional messages](../../channels/using/event-transactional-messages.md).
1. As you have direct access to all fields from the **[!UICONTROL Service]** resource, you can select any field from the **[!UICONTROL Context]** &gt; **[!UICONTROL Real-time event (rtEvent)]** &gt; **[!UICONTROL Event context (ctx)]** &gt;**[!UICONTROL Service]** node to personalize your content.

   ![](assets/confirmation_personalization-service.png)

   For more on personalizing a transactional message, see this section.[](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message)

1. Zeigen Sie eine Vorschau Ihrer Nachricht mit einem Testprofil an. Weiterführende Informationen hierzu finden Sie im Abschnitt [Testprofil in einer Transaktionsnachricht definieren](../../channels/using/event-transactional-messages.md#defining-a-test-profile-in-a-transactional-message).

1. Klicken Sie auf **[!UICONTROL Speichern &amp; Schließen]** , um den Inhalt zu speichern.
1. Veröffentlichen Sie die Transaktionsnachricht. Siehe [Transaktionsnachricht publizieren](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message).

### Step 2: Create and configure the service {#step-2--create-and-configure-the-service-1}

1. From the advanced menu **Profiles &amp; audiences** &gt; **Services** via the Adobe Campaign logo, create a service.
1. Go to the Service properties section, accessed via the  button in the service dashboard.****![](assets/edit_darkgrey-24px.png)
1. Fill in the Service label field.****

   ![](assets/confirmation_service-label.png)

   >[HINWEIS]
   >
   >You must fill in this field to enable reconciliation with the transactional message.

1. Wählen Sie im Abschnitt **[!UICONTROL Bestätigungsmeldungen]** die Option **[!UICONTROL Benutzerspezifische Nachricht]**: In diesem Modus können Sie auf eine bestimmte Bestätigungsmeldung für Profile verweisen, die Ihren Dienst abonnieren.
1. Wählen Sie die Konfiguration **[!UICONTROL des]** benutzerspezifischen Abonnementereignisses aus, die der von Ihnen erstellten Transaktionsnachricht zugeordnet ist.

   ![](assets/confirmation_service-confirmation-message.png)

1. Click **[!UICONTROL Confirm]** and save the service.

Jedes Mal, wenn ein Profil diesen Dienst abonniert, erhält er die von Ihnen definierte Transaktionsmeldung mit personalisierten Feldern, die dem ausgewählten Dienst zugeordnet sind. Eine Nachricht wird nur gesendet, wenn der Benutzer das erste Mal registriert.

## Konfigurieren der Bestätigungsmeldung von einer Einstiegsseite {#configuring-confirmation-message-from-landing-page}

Sie können auch auf die Bestätigungsmeldung von einer Abonnement-Landingpage verweisen, indem Sie die Option **[!UICONTROL Nachrichten]** starten im Abschnitt **[!UICONTROL Auftrag]** der Landingpage verwenden.

Beim Verweisen auf die Bestätigungsmeldung von der Einstiegsseite wird jedes Mal, wenn die Einstiegsseite gesendet wird (auch wenn das Profil bereits abonniert ist), eine Nachricht gesendet.

### Schritt 1: Bestätigungs-E-Mail erstellen   {#step-1--create-the-confirmation-email-2}

Eine Bestätigungs-E-Mail wird automatisch über eine Landingpage an jedes Profil gesendet, das den Newsletter abonniert. Das Abonnement gilt als Ereignis und die E-Mail ist eine [Transaktionsnachricht](../../channels/using/about-transactional-messaging.md) , die jedes Profil, das den Dienst abonniert, als Ziel hat.

Die Schritte zur Erstellung dieser Elemente werden unten beschrieben. Da die Transaktionsnachricht auf der Einstiegsseite referenziert wird, müssen Sie sie zuerst erstellen.

#### Ereignis erstellen    {#create-the-event-2}

The confirmation email is a [transactional message](../../channels/using/about-transactional-messaging.md) as it reacts to an event: the subscription to a service. Diese Meldung wird gesendet, um das Abonnement für Ihren Newsletter zu bestätigen.

1. Create an event from the **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]** &gt; **[!UICONTROL Event configuration]** menu, accessible from the Adobe Campaign logo.
1. Geben Sie eine Bezeichnung ein, wählen Sie eine Targeting-Dimension und klicken Sie auf **[!UICONTROL Erstellen]**.

   Die Konfigurationsschritte werden im Abschnitt [Konfigurieren von Transaktionsnachrichten](../../administration/using/configuring-transactional-messaging.md) beschrieben.

1. In the **[!UICONTROL Fields]** section, click **[!UICONTROL Create element]** and add **[!UICONTROL serviceName]** to the data structure in order to enable reconciliation.

   ![](assets/confirmation_serviceName-field.png)

   >[HINWEIS]
   >
   >The **[!UICONTROL serviceName]** field is mandatory. Wenn Sie sie nicht zur Ereignisdatenstruktur hinzufügen, kann Adobe Campaign keine Abstimmung mit dem abonnierten Dienst durchführen.

1. In the **[!UICONTROL Enrichment]** section, click **[!UICONTROL Create element]** and select the **[!UICONTROL Service]** target resource.
1. Ordnen Sie im Abschnitt **[!UICONTROL Verbindungsdefinition]** das Feld **[!UICONTROL serviceName]** der **[!UICONTROL Dienstressource dem Feld]** name **** der Ereigniskonfiguration zu.

   ![](assets/confirmation_serviceName-join.png)

   >[HINWEIS]
   >
   >Auf diese Weise können Sie Personalisierungsfelder aus der [!UICONTROL Dienstressource] in der Transaktionsmeldung verwenden.

#### Bestätigungsnachricht erstellen    {#design-the-confirmation-message-2}

Die Schritte zum Entwerfen der Transaktionsnachricht werden in diesem [Abschnitt](../../audiences/using/confirming-subscription-to-a-service.md#design-the-confirmation-message-1)beschrieben.

### Schritt 2: Dienst erstellen und konfigurieren {#step-2--create-and-configure-the-service-2}

1. Erstellen Sie im erweiterten Menü **[!UICONTROL Profiles &amp; audiences]** &gt; **[!UICONTROL Services]** über das Adobe Campaign-Logo einen Dienst.
1. Gehen Sie zum Abschnitt **[!UICONTROL Diensteigenschaften]** , auf den Sie über die Schaltfläche im Dienst-Dashboard ![](assets/edit_darkgrey-24px.png) zugreifen können.
1. Füllen Sie das Feld **[!UICONTROL Dienstbezeichnung]** aus. Diese Bezeichnung wird in der Bestätigungsmeldung und auf der Abonnement-Landingpage angezeigt.
1. Click **[!UICONTROL Confirm]** and save the service.

### Schritt 3: Landingpage erstellen und konfigurieren {#step-3--create-and-configure-the-landing-page}

Erstellen Sie eine Abonnement-Landingpage, die auf Ihrer Website veröffentlicht wird.

To create and configure this landing page, follow the steps below:

1. Design a [new landing page](../../channels/using/about-landing-pages.md) based on the **[!UICONTROL Subscription]** template.
1. Bearbeiten Sie die Eigenschaften der Einstiegsseite. Wählen Sie im Abschnitt " **[!UICONTROL Auftrag]** "&gt; " **[!UICONTROL Spezifische Aktionen]** "die Option " **[!UICONTROL Spezifischer Dienst]** "und wählen Sie den soeben erstellten Dienst aus der Dropdownliste.

   ![](assets/confirmation_lp-specific-service.png)

1. Wählen Sie die Option **[!UICONTROL Nachricht]** starten und wählen Sie die soeben erstellte Transaktionsnachricht aus der Dropdownliste aus.

   ![](assets/confirmation_lp-start-sending-message.png)

1. Passen Sie den Inhalt der Einstiegsseite an.

1. [Testen und publizieren](../../channels/using/sharing-a-landing-page.md) Sie die Landingpage.

Now each time a profile subscribes to your newsletter by submitting the landing page, he receives the confirmation message that you defined with personalized fields mapped to the service.

>[HINWEIS]
>
>Eine Nachricht wird jedes Mal gesendet, wenn die Einstiegsseite gesendet wird, auch wenn das Profil bereits abonniert ist.

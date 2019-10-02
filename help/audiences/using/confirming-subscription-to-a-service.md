---
title: Bestätigung des Abonnements für einen Dienst
seo-title: Bestätigung des Abonnements für einen Dienst
description: Bestätigung des Abonnements für einen Dienst
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
source-git-commit: bcf4a2e2b522b084d63c7bf15293b177f1c96333

---


# Bestätigung des Abonnements für einen Dienst{#confirming-subscription-to-a-service}

## Informationen zum Senden der Abonnementbestätigung {#sending-subscription-confirmation}

In diesem Abschnitt wird beschrieben, wie Sie eine automatische benutzerdefinierte Bestätigungs-E-Mail an die Profile senden, die einen bestimmten Dienst abonnieren.

Wenn Sie eine Bestätigungsnachricht für ein Abonnement (oder eine Rückmeldung) an einen Dienst senden möchten, können Sie die Standardnachricht oder eine benutzerdefinierte Nachricht verwenden. Die Schritte zur Auswahl einer Bestätigungsmeldung finden Sie im Abschnitt [Erstellen eines Dienstes](../../audiences/using/creating-a-service.md) .

Wenn Sie die Standardnachricht verwenden, können Sie deren Inhalt mit folgenden Einschränkungen bearbeiten:
* Sie können den Inhalt der Nachricht nur mit begrenzten Feldern aus dem Ereigniskontext personalisieren.
* Diese Meldung ist für alle Dienste identisch, die den Standardmodus verwenden.

To send a specific confirmation message for a given service, you can create a custom confirmation message, where you will also be able to leverage personalization fields from other resources. Dazu müssen Sie eine Transaktionsmeldung erstellen und konfigurieren. Diese Meldung kann referenziert werden:
* From the service itself. For more on this, see Configuring confirmation message from a service.[](../../audiences/using/confirming-subscription-to-a-service.md#configuring-confirmation-message-from-service)
* Von einer Abonnement-Landingpage. For more on this, see Configuring confirmation message from a landing page.[](../../audiences/using/confirming-subscription-to-a-service.md#configuring-confirmation-message-from-landing-page)

## Configuring confirmation message from a service {#configuring-confirmation-message-from-service}

Beispielsweise möchten Sie den Besuchern Ihrer Website automatisch eine Bestätigungsmeldung senden, wenn sie Ihren Marken-Newsletter abonnieren.

You need to configure a transactional email and reference that message from the desired service (subscription to your brand newsletter in this case). In order to enrich the transactional message with service information, you can define a reconciliation when creating the event.

When configuring it from the service, the confirmation transactional message will be sent only the first time each visitor subscribes to that service. If a profile is already subscribed, no confirmation message will be sent again to that profile.

### Schritt 1: Bestätigungs-E-Mail erstellen   {#step-1--create-the-confirmation-email-1}

A confirmation email will be automatically sent to each profile subscribing to the newsletter (through a landing page or any other means). The subscription is considered as an event and the email is a transactional message which will target each profile that subscribes to the service.[](../../channels/using/about-transactional-messaging.md)

Steps to create the confirmation email are described below. As the transactional message will be referenced in the service, you need to create it first.

#### Ereignis erstellen    {#create-the-event-1}

Die Bestätigungs-E-Mail ist eine Transaktionsnachricht, da sie auf ein Ereignis reagiert: das Abonnement eines Dienstes. This message will be sent to confirm subscription to your newsletter.

1. Create an event from the **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]** &gt; **[!UICONTROL Event configuration]** menu, accessible from the Adobe Campaign logo.
1. Geben Sie eine Bezeichnung ein, wählen Sie eine Targeting-Dimension und klicken Sie auf **[!UICONTROL Erstellen]**.

   The configuration steps are presented in the Configuring transactional messaging section.[](../../administration/using/configuring-transactional-messaging.md)

1. In the **[!UICONTROL Fields]** section, click **[!UICONTROL Create element]** and add **[!UICONTROL publicLabel]** to the data structure in order to enable reconciliation.

   ![](assets/confirmation_publicLabel-field.png)

   >[HINWEIS]
   >
   >The **[!UICONTROL publicLabel]** field is mandatory. Wenn Sie sie nicht zur Ereignisdatenstruktur hinzufügen, kann Adobe Campaign keine Abstimmung mit dem Dienst durchführen. Beim Abonnieren eines Dienstes wird dieses Feld mit der **[!UICONTROL Dienstbezeichnung]** des entsprechenden Dienstes ausgefüllt.

1. In the **[!UICONTROL Enrichment]** section, click **[!UICONTROL Create element]** and select the **[!UICONTROL Service]** target resource.

   ![](assets/confirmation_enrichment-service.png)

1. Ordnen Sie im Abschnitt **[!UICONTROL Verbindungsdefinition]** das Feld **[!UICONTROL publicLabel]** der **[!UICONTROL Dienstressource dem Feld]** publicLabel **** der Ereigniskonfiguration zu.

   ![](assets/confirmation_publicLabel-join.png)

   >[HINWEIS]
   >
   >Auf diese Weise können Sie Personalisierungsfelder aus der **[!UICONTROL Dienstressource]** in der Transaktionsmeldung verwenden.

1. Speichern Sie die Ereigniskonfiguration und klicken Sie auf **[!UICONTROL Veröffentlichen]** , um das Ereignis zu veröffentlichen.

Das Ereignis ist somit fertig eingerichtet. Sie können nun die transaktionelle E-Mail-Nachricht entwerfen.

#### Bestätigungsnachricht erstellen    {#design-the-confirmation-message-1}

Die Bestätigungs-E-Mail ist eine Transaktionsnachricht, die auf dem soeben veröffentlichten Ereignis basiert.

1. Wählen Sie ausgehend vom Adobe Campaign-Logo die Option **[!UICONTROL Marketingpläne]** &gt; **[!UICONTROL Transaktionsnachrichten]** und nochmals **[!UICONTROL Transaktionsnachrichten]**.
1. Wählen Sie die Transaktionsemail für das Ereignis aus, das Sie gerade veröffentlicht haben.

1. Klicken Sie auf den Abschnitt **[!UICONTROL Inhalt]** und wählen Sie eine E-Mail-Vorlage aus. Weitere Informationen zum Bearbeiten von Transaktionsnachrichten finden Sie unter [Ereignistransaktionsmeldungen](../../channels/using/event-transactional-messages.md).
1. Da Sie direkten Zugriff auf alle Felder aus der **[!UICONTROL Dienstressource]** haben, können Sie ein beliebiges Feld aus dem Knoten **[!UICONTROL Kontext]** &gt; **[!UICONTROL Echtzeit-Ereignis (rtEvent)]** &gt; **[!UICONTROL Ereigniskontext (ctx)]** &gt;**[!UICONTROL Dienst]** auswählen, um Ihren Inhalt zu personalisieren.

   ![](assets/confirmation_personalization-service.png)

   Weitere Informationen zum Personalisieren einer Transaktionsnachricht finden Sie in [diesem Abschnitt](../../channels/using/event-transactional-messages.md#personalizing-a-transactional-message).

1. Zeigen Sie eine Vorschau Ihrer Nachricht mit einem Testprofil an. Weiterführende Informationen hierzu finden Sie im Abschnitt [Testprofil in einer Transaktionsnachricht definieren](../../channels/using/event-transactional-messages.md#defining-a-test-profile-in-a-transactional-message).

1. Klicken Sie auf **[!UICONTROL Speichern &amp; Schließen]** , um den Inhalt zu speichern.
1. Veröffentlichen Sie die Transaktionsnachricht. Siehe [Transaktionsnachricht publizieren](../../channels/using/event-transactional-messages.md#publishing-a-transactional-message).

### Schritt 2: Dienst erstellen und konfigurieren {#step-2--create-and-configure-the-service-1}

1. Erstellen Sie im erweiterten Menü **Profiles &amp; audiences** &gt; **Services** über das Adobe Campaign-Logo einen Dienst.
1. Gehen Sie zum Abschnitt **[!UICONTROL Diensteigenschaften]** , auf den Sie über die Schaltfläche im Dienst-Dashboard ![](assets/edit_darkgrey-24px.png) zugreifen können.
1. Füllen Sie das Feld **[!UICONTROL Dienstbezeichnung]** aus.

   ![](assets/confirmation_service-label.png)

   >[HINWEIS]
   >
   >Sie müssen dieses Feld ausfüllen, um die Versöhnung mit der Transaktionsnachricht zu aktivieren.

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
1. Enter a label, select a targeting dimension and click Create.****

   The configuration steps are presented in the Configuring transactional messaging section.[](../../administration/using/configuring-transactional-messaging.md)

1. In the **[!UICONTROL Fields]** section, click **[!UICONTROL Create element]** and add **[!UICONTROL serviceName]** to the data structure in order to enable reconciliation.

   ![](assets/confirmation_serviceName-field.png)

   >[HINWEIS]
   >
   >The **[!UICONTROL serviceName]** field is mandatory. If you do not add it to the event data structure, Adobe Campaign will not be able to perform reconciliation with the subscribed service.

1. In the **[!UICONTROL Enrichment]** section, click **[!UICONTROL Create element]** and select the **[!UICONTROL Service]** target resource.
1. Ordnen Sie im Abschnitt **[!UICONTROL Verbindungsdefinition]** das Feld **[!UICONTROL serviceName]** der **[!UICONTROL Dienstressource dem Feld]** name **** der Ereigniskonfiguration zu.

   ![](assets/confirmation_serviceName-join.png)

   >[HINWEIS]
   >
   >This will enable you to use personalization fields from the Service  resource in the transactional message.

#### Bestätigungsnachricht erstellen    {#design-the-confirmation-message-2}

The steps for designing the transactional message are presented in this section.[](../../audiences/using/confirming-subscription-to-a-service.md#design-the-confirmation-message-1)

### Step 2: Create and configure the service {#step-2--create-and-configure-the-service-2}

1. From the advanced menu Profiles &amp; audiences &gt; ervices via the Adobe Campaign logo, create a service.******[!UICONTROLS]**
1. Go to the Service properties section, accessed via the  button in the service dashboard.****![](assets/edit_darkgrey-24px.png)
1. Fill in the Service label field. **** This label will be displayed in the confirmation message and in the subscription landing page.
1. Click **[!UICONTROL Confirm]** and save the service.

### Step 3: Create and configure the landing page {#step-3--create-and-configure-the-landing-page}

Create a subscription landing page which will be published on your website.

To create and configure this landing page, follow the steps below:

1. Design a [new landing page](../../channels/using/about-landing-pages.md) based on the **[!UICONTROL Subscription]** template.
1. Edit the landing page properties. In the Job &gt; Specific actions section, select the Specific service option and choose the service that you just created from the drop-down list.************

   ![](assets/confirmation_lp-specific-service.png)

1. Wählen Sie die Option **[!UICONTROL Nachricht]** starten und wählen Sie die soeben erstellte Transaktionsnachricht aus der Dropdownliste aus.

   ![](assets/confirmation_lp-start-sending-message.png)

1. Passen Sie den Inhalt der Einstiegsseite an.

1. [Testen und publizieren](../../channels/using/sharing-a-landing-page.md) Sie die Landingpage.

Jedes Mal, wenn ein Profil Ihren Newsletter abonniert, indem er die Einstiegsseite eingibt, erhält er die Bestätigungsmeldung, die Sie mit personalisierten Feldern definiert haben, die dem Dienst zugeordnet sind.

>[HINWEIS]
>
>Eine Nachricht wird jedes Mal gesendet, wenn die Einstiegsseite gesendet wird, auch wenn das Profil bereits abonniert ist.

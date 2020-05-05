---
title: Adobe Experience Platform-Audiences auswählen
description: Erfahren Sie, wie Sie in Workflows Adobe Experience Platform-Audiences auswählen.
page-status-flag: never-activated
uuid: 528d9472-e447-47af-a6b2-3181aa5fb5ad
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: channel-activities
discoiquuid: 19796aca-6e9e-4d3a-8917-ba660ec7993c
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 68e825bc3b6b7f94f61875e7da2bc8f63f06d9cb

---


# Adobe Experience Platform-Audiences auswählen {#targeting-aep-audiences}

>[!IMPORTANT]
>
>Der Audience Destinations-Dienst befindet sich derzeit in der Betaphase, die häufig ohne Vorankündigung aktualisiert werden kann. Kunden müssen auf Azure gehostet werden (derzeit nur für Nordamerika in der Betaphase), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an die Adobe-Kundenunterstützung, wenn Sie Zugriff haben möchten.

Nachdem Sie mit dem Unified Profile Segment Builder eine [Adobe Experience Platform-Audience](../../audiences/using/aep-about-audience-destinations-service.md) erstellt haben, können Sie diese wie eine Campaign-Audience innerhalb von Workflows verwenden, um Nachrichten zu personalisieren und zu senden.

Gehen Sie wie folgt vor, um eine Adobe Experience Platform-Audience in Ihren Workflows zu aktivieren:

1. Add a **[!UICONTROL Read audience]** activity into the workflow, then open it.

1. Wählen Sie die **[!UICONTROL Adobe Experience Platform]** Option unter **[!UICONTROL Type of audience]** und fügen Sie dann die gewünschte Audience hinzu.

   ![](assets/aep_wkf_readaudience.png)

1. (Optional) Nachdem die Audience ausgewählt wurde, können Sie auf die Augenschaltfläche klicken, um die Segmentdefinition zu überprüfen und/oder zu bearbeiten (stellen Sie sicher, dass Sie die Änderungen erneut speichern).

   Wenn Sie auf die Augenschaltfläche klicken, gelangen Sie direkt zum Unified Segment Builder (in einem anderen Tab), der der ausgewählten Audience in Campaign zugeordnet ist.

1. Select a **[!UICONTROL Platform data mapping]** element to specify the desired targeting dimension for the selected Adobe Experience Platform audience.

   Standardmäßig ist der Primärschlüssel (z. B. iRecipientID für die Profiltabelle, iAppSubscriptionID für die AppSubscription-Tabelle), der für die Abstimmung verwendet wird, automatisch in der Dropdown-Liste verfügbar. Um eine Zielgruppenbestimmung außerhalb des Primärschlüssels durchzuführen, müssen Sie einen benutzerdefinierten **Namespace** erstellen.

   >[!NOTE]
   >
   >Bei Zielgruppen außerhalb des Primärschlüssels müssen Sie auch ein benutzerdefiniertes Zielgruppen-Mapping erstellen, das dem benutzerdefinierten Namensraum entspricht. Weiterführende Informationen zum Zielgruppen-Mapping erfahren Sie in [diesem Abschnitt](../../administration/using/target-mappings-in-campaign.md).

   ![](assets/aep_wkf_readaudience_namespace.png)

   Diese Liste enthält alle XDM-Mappings (Experience-Datenmodell), die für Ihre Instanz konfiguriert wurden. Weitere Informationen zu Adobe Experience Platform Data Connector finden Sie in [diesem Dokument](../../developing/using/aep-about-data-connector.md).

   ![](assets/aep_wkf_readaudience_namespace2.png)

1. Once the audience and targeting dimensions are configured properly, click the **[!UICONTROL Confirm]** button to save your changes.

Sie können Ihren Workflow jetzt mit anderen Aktivitäten konfigurieren. You can, for example, link an **[!UICONTROL Email delivery]** activity to send an email to the audience that has been selected.

![](assets/aep_wkf_email.png)

>[!NOTE]
>
>Mit Campaign Standard können Sie Adobe Experience Platform-Audiences in allen Versandkanälen auswählen: E-Mails, SMS-Nachrichten, Briefpostnachrichten, Push-Benachrichtigungen und In-App-Nachrichten.
>
>*Hinweis: Bei allen Push- und In-App-Nachrichten unterstützt Campaign Standard nur Sendungen an bekannte Profile.

Weitere Informationen zur Verwendung von Workflows und Sendungen finden Sie in den folgenden Abschnitten:

* [Workflows](../../automating/using/get-started-workflows.md)
* [Workflow erstellen](../../automating/using/building-a-workflow.md)
* [Kommunikationskanäle](../../channels/using/get-started-communication-channels.md)
* [Über Kanalaktivitäten](../../automating/using/about-channel-activities.md)

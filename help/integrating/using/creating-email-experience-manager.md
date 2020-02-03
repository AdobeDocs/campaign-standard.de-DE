---
title: Erstellen von E-Mail-Inhalten in Adobe Experience Manager
description: Durch die Integration von Adobe Experience Manager können Sie Inhalte direkt in AEM erstellen und später in Adobe Campaign verwenden.
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 5c1a540475b7d93c18c957243ee2a403b8154aa3

---


# Creating an email content in Adobe Experience Manager {#creating-email-aem}

Durch die Integration von Adobe Campaign Standard mit Adobe Experience Manager können Sie die in Adobe Experience Manager erstellten Inhalte in E-Mails in Adobe Campaign verwenden.

Dieser Verwendungsfall zeigt Ihnen, wie Sie E-Mail-Inhalte in Adobe Experience Manager erstellen.

## Voraussetzungen {#prerequisites}

Vergewissern Sie sich zunächst, dass Sie über folgende Elemente verfügen:

* Adobe-Experience-Manager-**Authoring**-Instanz zur Erstellung der Inhalte,
* Adobe-Experience-Manager-**Publishing**-Instanz zur Veröffentlichung der Inhalte,
* Adobe-Campaign-Instanz.

## Konfiguration {#configuration}

Um die kombinierte Nutzung von Adobe Campaign und Adobe Experience Manager zu ermöglichen, ist zunächst eine Konfiguration beider Lösungen erforderlich.

1. Konfiguration in Adobe Campaign: Gehen Sie wie folgt vor:

   * Konfigurieren Sie ein externes Konto vom Typ Adobe Experience Manager.
   * Konfigurieren Sie die Option **[!UICONTROL AEMResourceTypeFilter]**, die zur Identifizierung von in Adobe Experience Manager erstellten, für Adobe Campaign bestimmten Inhaltstypen dient.
   * Erstellen Sie eine E-Mail-Vorlage und definieren Sie den Inhalt als aus Adobe Experience Manager stammend.

1. Ordnen Sie der Vorlage das zuvor erstellte externe Konto zu. Gehen Sie wie folgt vor:

   * Konfigurieren Sie die Replikation zwischen der Authoring-Instanz und der Publishing-Instanz von Adobe Experience Manager.
   * Stellen Sie die Verbindung zwischen Adobe Experience Manager und Adobe Campaign her, indem Sie einen dedizierten **[!UICONTROL Cloud Service konfigurieren]**.

## Creating an email content in Adobe Experience Manager {#use-case}

So erstellen Sie E-Mail-Inhalt in Adobe Experience Manager:

1. Erstellen Sie einen E-Mail-Inhalt anhand einer der speziell für Adobe Campaign konzipierten Vorlagen.
1. Wählen Sie in den Inhaltseigenschaften den **[!UICONTROL Cloud Service]**aus, der Ihrer Adobe Campaign-Instanz entspricht.
1. Bearbeiten Sie den Inhalt, indem Sie beispielsweise Text, Bilder oder Personalisierungselemente einfügen.
1. Validieren Sie den Inhalt.

Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](https://docs.adobe.com/content/help/en/experience-manager-65/authoring/aem-adobe-campaign/campaign.html).

![](assets/aem_content.png)

So rufen Sie den Inhalt in Adobe Campaign ab:

1. Erstellen Sie eine E-Mail anhand einer Vorlage, deren Inhaltstyp Adobe Experience Manager entspricht.
1. Verknüpfen Sie ausgehend vom Bildschirm zur Inhaltserstellung in Adobe Campaign einen in Adobe Experience Manager erstellten Inhalt.

![](assets/aem_linked_content.png)


---
title: Integration mit Experience Manager
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
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Integration mit Experience Manager{#integrating-with-experience-manager}

Durch die Integration von Adobe Campaign Standard mit Adobe Experience Manager können Sie die in Adobe Experience Manager erstellten Inhalte in E-Mails in Adobe Campaign verwenden.

Auf diese Weise profitieren Sie gleichermaßen von den fortgeschrittenen Funktionen zur Inhaltsgestaltung in Adobe Experience Manager und den außerordentlichen Versand- sowie Datenverwaltungskapazitäten Adobe Campaigns.

>[!NOTE]
>
>Für aus Adobe Experience Manager importierte Inhalte können keine A/B-Tests durchgeführt werden.

Adobe Campaign Standard ist mit Adobe Experience Manager 6.1, 6.2, 6.3 und 6.4 kompatibel. Im Folgenden finden Sie eine Übersicht der möglichen Aktionen. Weiterführende Informationen finden Sie in den Abschnitten [Konfiguration](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/campaignstandard.html) und [Vorgehensweise](https://helpx.adobe.com/experience-manager/6-4/sites/authoring/using/campaign.html).

## Voraussetzungen {#prerequisites}

Vergewissern Sie sich zunächst, dass Sie über folgende Elemente verfügen:

* Adobe-Experience-Manager-**Authoring**-Instanz zur Erstellung der Inhalte,
* Adobe-Experience-Manager-**Publishing**-Instanz zur Veröffentlichung der Inhalte,
* Adobe-Campaign-Instanz.

## Umsetzung  {#use-case}

So erstellen Sie E-Mail-Inhalt in Adobe Experience Manager:

1. Erstellen Sie einen E-Mail-Inhalt anhand einer der speziell für Adobe Campaign konzipierten Vorlagen.
1. Wählen Sie in den Inhaltseigenschaften den **[!UICONTROL Cloud Service]** aus, der Ihrer Adobe Campaign-Instanz entspricht.
1. Bearbeiten Sie den Inhalt, indem Sie beispielsweise Text, Bilder oder Personalisierungselemente einfügen.
1. Validieren Sie den Inhalt.

Weitere Informationen finden Sie im [entsprechenden Handbuch](https://docs.adobe.com/docs/en/aem/6-2/author/personalization/adobe-campaign/campaign.html).

![](assets/aem_content.png)

So rufen Sie den Inhalt in Adobe Campaign ab:

1. Erstellen Sie eine E-Mail anhand einer Vorlage, deren Inhaltstyp Adobe Experience Manager entspricht.
1. Verknüpfen Sie ausgehend vom Bildschirm zur Inhaltserstellung in Adobe Campaign einen in Adobe Experience Manager erstellten Inhalt.

![](assets/aem_linked_content.png)

## Konfiguration  {#configuration}

Um die kombinierte Nutzung von Adobe Campaign und Adobe Experience Manager zu ermöglichen, ist zunächst eine Konfiguration beider Lösungen erforderlich.

1. Konfiguration in Adobe Campaign: Gehen Sie wie folgt vor:

   * Konfigurieren Sie ein externes Konto vom Typ Adobe Experience Manager.
   * Konfigurieren Sie die Option **AEMResourceTypeFilter**, die zur Identifizierung von in Adobe Experience Manager erstellten, für Adobe Campaign bestimmten Inhaltstypen dient.
   * Erstellen Sie eine E-Mail-Vorlage und definieren Sie den Inhalt als aus Adobe Experience Manager stammend.

1. Ordnen Sie der Vorlage das zuvor erstellte externe Konto zu. Gehen Sie wie folgt vor:

   * Konfigurieren Sie die Replikation zwischen der Authoring-Instanz und der Publishing-Instanz von Adobe Experience Manager.
   * Stellen Sie die Verbindung zwischen Adobe Experience Manager und Adobe Campaign her, indem Sie einen dedizierten **[!UICONTROL Cloud Service konfigurieren]**.


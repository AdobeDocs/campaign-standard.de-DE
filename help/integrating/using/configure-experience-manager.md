---
title: Konfiguration der Campaign-Experience Manager-Integration
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
source-git-commit: 37b1c17234a300b092db3c810a32de3600bb8f2f

---


# Konfiguration der Campaign-Experience Manager-Integration {#configuration-aem}

Durch die Integration von Adobe Campaign Standard mit Adobe Experience Manager können Sie die in Adobe Experience Manager erstellten Inhalte in E-Mails in Adobe Campaign verwenden.

In diesem Anwendungsfall erfahren Sie, wie Sie E-Mail-Inhalte in Adobe Experience Manager erstellen und verwalten und diese dann für Ihre Marketingkampagnen verwenden, indem Sie sie in Ihre E-Mails in Adobe Campaign Standard importieren.

## Voraussetzungen {#prerequisites}

Vergewissern Sie sich zunächst, dass Sie über folgende Elemente verfügen:

* Adobe-Experience-Manager-**Authoring**-Instanz zur Erstellung der Inhalte,
* Adobe-Experience-Manager-**Publishing**-Instanz zur Veröffentlichung der Inhalte,
* Adobe-Campaign-Instanz.

## Konfiguration in Adobe Campaign Standard {#config-acs}

Um die kombinierte Nutzung von Adobe Campaign und Adobe Experience Manager zu ermöglichen, ist zunächst eine Konfiguration beider Lösungen erforderlich.
Gehen Sie wie folgt vor:

1. Zunächst müssen Sie das **[!UICONTROL Adobe Experience Manager instance]** externe Konto unter **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > konfigurieren **[!UICONTROL External accounts menu]**.

1. Konfigurieren Sie das externe Adobe Experience Manager-Konto mit Ihrer **[!UICONTROL Server]** URL **[!UICONTROL Account]** und **[!UICONTROL Password]**.

   ![](assets/aem_1.png)

1. Überprüfen Sie, ob die **[!UICONTROL AEMResourceTypeFilter]** Option richtig konfiguriert wurde. Öffnen Sie das **[!UICONTROL Options]** Menü unter **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Options]** Menü.

1. Überprüfen Sie im **[!UICONTROL Value (text)]** Feld, ob die folgende Syntax korrekt ist:

   ```
   mcm/campaign/components/newsletter,mcm/campaign/components/campaign_newsletterpage,mcm/neolane/components/newsletter
   ```

   ![](assets/aem_2.png)

1. Duplizieren Sie dann im erweiterten Menü unter **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Delivery templates]** eine vorhandene Vorlage, um eine für Adobe Experience Manager spezifische E-Mail-Vorlage zu erstellen.

   ![](assets/aem_3.png)

1. Click the **[!UICONTROL Edit properties]** icon.

   ![](assets/aem_4.png)

1. Wählen Sie unter der **[!UICONTROL Content]** Dropdownliste **[!UICONTROL Adobe Experience Manager]** im Feld Ihr zuvor erstelltes externes Konto **[!UICONTROL Content source]** im **[!UICONTROL Adobe Experience Manager account]**.

Sie müssen die Integration jetzt in Adobe Experience Manager konfigurieren.

## Konfiguration in Adobe Experience Manager {#config-aem}

Um Adobe Experience Manager mit Adobe Campaign Standard zu konfigurieren, müssen Sie die folgenden Schritte ausführen:

1. Zunächst müssen Sie die Replizierung zwischen den Instanzen für Authoring und Veröffentlichung von Adobe Experience Manager konfigurieren. Siehe diesen [Abschnitt](https://docs.adobe.com/content/help/en/experience-manager-65/administering/integration/campaignstandard.html#configuring-adobe-experience-manager).

1. Then, connect Adobe Experience Manager to Adobe Campaign by configuring a dedicated **[!UICONTROL Cloud Service]**. Siehe diesen [Abschnitt](https://docs.adobe.com/content/help/en/experience-manager-65/administering/integration/campaignstandard.html#connecting-aem-to-adobe-campaign).

1. Sie müssen den Externalisierer jetzt in Adobe Experience Manager auf Ihrer Autoreninstanz konfigurieren. Siehe diesen [Abschnitt](https://docs.adobe.com/content/help/en/experience-manager-65/administering/integration/campaignstandard.html#configuring-the-externalizer).


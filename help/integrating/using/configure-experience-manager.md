---
title: Integration von Campaign mit Experience Manager konfigurieren
description: Durch die Integration von Adobe Experience Manager können Sie Inhalte direkt in AEM erstellen und später in Adobe Campaign verwenden.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
feature: Triggers
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: f56f5a19-6283-4eef-8127-c69a16a42a37
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 100%

---

# Integration von Campaign mit Experience Manager konfigurieren {#configuration-aem}

Durch die Integration von Adobe Campaign Standard mit Adobe Experience Manager können Sie die in Adobe Experience Manager erstellten Inhalte in E-Mails in Adobe Campaign verwenden.

Anhand dieses Anwendungsbeispiels lernen Sie, in Adobe Experience Manager E-Mail-Inhalte zu erstellen und zu verwalten und diese anschließend für Ihre Marketing-Kampagnen zu verwenden, indem Sie sie in Ihre Adobe Campaign Standard-E-Mails importieren.

## Voraussetzungen {#prerequisites}

Vergewissern Sie sich zunächst, dass Sie über folgende Elemente verfügen:

* Adobe-Experience-Manager-**Authoring**-Instanz zur Erstellung der Inhalte,
* Adobe-Experience-Manager-**Publishing**-Instanz zur Veröffentlichung der Inhalte,
* Adobe Campaign-Instanz.

## Konfiguration in Adobe Campaign Standard {#config-acs}

Um die kombinierte Nutzung von Adobe Campaign und Adobe Experience Manager zu ermöglichen, ist zunächst eine Konfiguration beider Lösungen erforderlich.
Gehen Sie wie folgt vor:

1. Konfigurieren Sie zunächst das externe Konto der **[!UICONTROL Adobe-Experience-Manager-Instanz]** im Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Externe Konten]**.

1. Konfigurieren Sie das externe Adobe Experience Manager-Konto mit Ihrer **[!UICONTROL Server]**-URL, Ihrem **[!UICONTROL Konto]** und Ihrem **[!UICONTROL Passwort]**.

   ![](assets/aem_1.png)

1. Überprüfen Sie, ob die Option **[!UICONTROL AEMResourceTypeFilter]** richtig konfiguriert wurde. Rufen Sie das Menü **[!UICONTROL Optionen]** unter **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Optionen]** auf.

1. Überprüfen Sie im Feld **[!UICONTROL Wert (text)]**, ob die folgende Syntax korrekt ist:

   ```
   mcm/campaign/components/newsletter,mcm/campaign/components/campaign_newsletterpage,mcm/neolane/components/newsletter
   ```

   ![](assets/aem_2.png)

1. Duplizieren Sie dann im erweiterten Menü unter **[!UICONTROL Ressourcen]** > **[!UICONTROL Vorlagen]** > **[!UICONTROL Versandvorlagen]** eine der vorhandenen Vorlagen, um eine für Adobe Experience Manager spezifische E-Mail-Vorlage zu erstellen.

   ![](assets/aem_3.png)

1. Klicken Sie auf das Symbol **[!UICONTROL Eigenschaften bearbeiten]**.

   ![](assets/aem_4.png)

1. Wählen Sie in der Dropdown-Liste **[!UICONTROL Inhalt]** die Option **[!UICONTROL Adobe Experience Manager]** im Feld **[!UICONTROL Inhaltsquelle]** und dann Ihr zuvor erstelltes externes Konto im **[!UICONTROL Adobe Experience Manager-Konto]** aus.

Konfigurieren Sie jetzt die Integration in Adobe Experience Manager.

## Konfiguration in Adobe Experience Manager {#config-aem}

Führen Sie die folgenden Schritte aus, um Adobe Experience Manager mit Adobe Campaign Standard zu konfigurieren:

1. Konfigurieren Sie zunächst die Replikation zwischen der Autoren- und der Veröffentlichungsinstanz von Adobe Experience Manager. Siehe diesen [Abschnitt](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html?lang=de#configuring-adobe-experience-manager?lang=de).

1. Stellen Sie dann die Verbindung zwischen Adobe Experience Manager und Adobe Campaign her, indem Sie einen dedizierten **[!UICONTROL Cloud Service]** konfigurieren. Siehe diesen [Abschnitt](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html?lang=de#connecting-aem-to-adobe-campaign?lang=de).

1. Konfigurieren Sie jetzt den Externalizer in Adobe Experience Manager auf Ihrer Autoreninstanz. Siehe diesen [Abschnitt](https://experienceleague.adobe.com/docs/experience-manager-65/administering/integration/campaignstandard.html?lang=de#configuring-the-externalizer).

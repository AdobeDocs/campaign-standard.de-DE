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
TQID: https://experienceleague.adobe.com/LluSzpCdzqvBNFz9HmI4MCLj8hhXO0Wp-kefaoNLB5U
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: a075b2c1-7748-4328-b7f6-343aa314616a
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 392
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

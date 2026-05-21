---
title: Integration von Campaign mit Target konfigurieren
description: Hier erfahren Sie, wie Sie die Adobe-Target-Integration konfigurieren müssen, um dynamischen Inhalt in Adobe Campaign verwenden zu können.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-target
feature: Triggers
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: d382bfdd-418d-46c1-98dd-df8626f85cac
TQID: https://experienceleague.adobe.com/trfuEp6pEd2jFADsK6NMw6tx8ASi86ZFur56AjwnpWQ
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 100%

---

# Integration von Campaign mit Target konfigurieren{#configuring-the-campaign-target-integration}

Durch die Integration von Adobe Campaign mit Adobe Target können dynamische Inhalte in Sendungen eingefügt werden.

Um die Integrationsfunktionen mit Adobe Target nutzen zu können, ist zunächst eine Konfiguration in Adobe Campaign erforderlich. Diese muss vom funktionalen Administrator vorgenommen werden.

Für dieses Verfahren sind die folgenden Elemente erforderlich:

* Adobe-Experience-Cloud-Mandant,
* Mandant für Adobe Target,
* Adobe-Target-Rawbox für Adobe Campaign.

1. Wählen Sie im erweiterten Menü über das Adobe Campaign-Logo oben links im Bildschirm die Schaltflächen  **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Optionen]**.
1. Um die Server- und Mandantenoptionen für Adobe Target zu konfigurieren, füllen Sie die folgenden Felder aus:

   * **[!UICONTROL TNT_TenantName]**, Name des Mandanten für Adobe Target. Dieser Wert entspricht dem Adobe-Target-**[!UICONTROL Client-Namen]**.
   * **[!UICONTROL TNT_EdgeServer]**, der für die Integration verwendete Adobe-Target-Server. Diese Option ist standardmäßig ausgefüllt. Dieser Wert entspricht der Adobe-Target-**[!UICONTROL Server-Domain]** und wird vom Wert **/m2** gefolgt. Beispiel: **tt.omtrdc.net/m2**.

   ![](assets/tar_options.png)

Ihre Benutzer können jetzt mit Adobe Target in einen Versand dynamische Bilder einfügen.

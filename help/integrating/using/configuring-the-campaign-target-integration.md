---
title: Integration von Campaign mit Target konfigurieren
seo-title: Integration von Campaign mit Target konfigurieren
description: Integration von Campaign mit Target konfigurieren
seo-description: Hier erfahren Sie, wie Sie die Adobe-Target-Integration konfigurieren müssen, um dynamischen Inhalt in Adobe Campaign verwenden zu können.
page-status-flag: nie aktiviert
uuid: 0 df 7701 c-dc 26-4 c 30-9 af 9-ebf 92815 d 90 c
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird integriert
content-type: Referenz
topic-tags: working-with-campaign-and-target
discoiquuid: f 7 fb 2084-dd 6 f -4 aa 2-940 f-e 48713146635
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Integration von Campaign mit Target konfigurieren{#configuring-the-campaign-target-integration}

Durch die Integration von Adobe Campaign mit Adobe Target können dynamische Inhalte in Sendungen eingefügt werden.

Um die Integrationsfunktionen mit Adobe Target nutzen zu können, ist zunächst eine Konfiguration in Adobe Campaign erforderlich. Diese muss vom funktionalen Administrator vorgenommen werden.

Für dieses Verfahren sind die folgenden Elemente erforderlich:

* Adobe-Experience-Cloud-Mandant,
* Mandant für Adobe Target,
* Adobe-Target-Rawbox für Adobe Campaign.

1. From the advanced menu, via the Adobe Campaign logo in the top left corner, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]** &gt; **[!UICONTROL Options]**.
1. Um die Server- und Mandantenoptionen für Adobe Target zu konfigurieren, füllen Sie die folgenden Felder aus:

   * **[!UICONTROL TNT_TenantName]**, Name des Mandanten für Adobe Target. Dieser Wert entspricht dem Adobe-Target-**[!UICONTROL Client-Namen]**.
   * **[!UICONTROL TNT_EdgeServer]**, der für die Integration verwendete Adobe-Target-Server. Diese Option ist standardmäßig ausgefüllt. Dieser Wert entspricht der Adobe-Target-**[!UICONTROL Server-Domain]** und wird vom Wert **/m2** gefolgt. Beispiel: **tt.omtrdc.net/m2**.
   ![](assets/tar_options.png)

Ihre Benutzer können jetzt mit Adobe Target in einen Versand dynamische Bilder einfügen.

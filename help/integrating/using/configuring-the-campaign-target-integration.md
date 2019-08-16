---
title: Integration von Campaign mit Target konfigurieren
seo-title: Integration von Campaign mit Target konfigurieren
description: Integration von Campaign mit Target konfigurieren
seo-description: Hier erfahren Sie, wie Sie die Adobe-Target-Integration konfigurieren müssen, um dynamischen Inhalt in Adobe Campaign verwenden zu können.
page-status-flag: never-activated
uuid: 0df5701c-dc26-4c30-9af9-ebf92815d90c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-target
discoiquuid: f7fb2084-dd6f-4aa2-940f-e48713146635
internal: n
snippet: y
translation-type: ht
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Integration von Campaign mit Target konfigurieren{#configuring-the-campaign-target-integration}

Durch die Integration von Adobe Campaign mit Adobe Target können dynamische Inhalte in Sendungen eingefügt werden.

Um die Integrationsfunktionen mit Adobe Target nutzen zu können, ist zunächst eine Konfiguration in Adobe Campaign erforderlich. Diese muss vom funktionalen Administrator vorgenommen werden.

Für dieses Verfahren sind die folgenden Elemente erforderlich:

* Adobe-Experience-Cloud-Mandant,
* Mandant für Adobe Target,
* Adobe-Target-Rawbox für Adobe Campaign.

1. Wählen Sie im erweiterten Menü über das Adobe-Campaign-Logo oben links im Bildschirm die Schaltflächen **[!UICONTROL Administration]** &gt; **[!UICONTROL Anwendungskonfiguration]** &gt; **[!UICONTROL Optionen]**.
1. Um die Server- und Mandantenoptionen für Adobe Target zu konfigurieren, füllen Sie die folgenden Felder aus:

   * **[!UICONTROL TNT_TenantName]**, Name des Mandanten für Adobe Target. Dieser Wert entspricht dem Adobe-Target-**[!UICONTROL Client-Namen]**.
   * **[!UICONTROL TNT_EdgeServer]**, der für die Integration verwendete Adobe-Target-Server. Diese Option ist standardmäßig ausgefüllt. Dieser Wert entspricht der Adobe-Target-**[!UICONTROL Server-Domain]** und wird vom Wert **/m2** gefolgt. Beispiel: **tt.omtrdc.net/m2**.
   ![](assets/tar_options.png)

Ihre Benutzer können jetzt mit Adobe Target in einen Versand dynamische Bilder einfügen.

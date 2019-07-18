---
title: Datenspeicherung und -abstimmung
seo-title: Datenspeicherung und -abstimmung
description: Datenspeicherung und -abstimmung
seo-description: In Adobe Campaign können Sie definieren, wie mit den von Besuchern in der Landingpage gemachten Angaben verfahren werden soll.
page-status-flag: nie aktiviert
uuid: 5 b 222 ea 2-6628-457 f-a 618-bfc 0 e 5 eb 93 dd
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Kanäle
content-type: Referenz
topic-tags: landing-pages
discoiquuid: 899 c 7152-f 415-4 df 9-b 4 b 4-5 ff 3470 a 4 e 32
context-tags: Landingpage, main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: d50d486ed77cb7989df47133bb49fde3227ae3a5

---


# Datenspeicherung und -abstimmung{#data-storage-and-reconciliation}

In den Abstimmparametern wird definiert, wie mit den von Besuchern in der Landingpage gemachten Angaben verfahren werden soll.

Gehen Sie wie folgt vor:

1. Bearbeiten Sie die Landingpage-Eigenschaften über das Symbol ![](assets/edit_darkgrey-24px.png) im Landingpage-Dashboard und rufen Sie die Parameter **Vorgang]auf.[!UICONTROL **

   ![](assets/lp_parameters_4.png)

1. Select the **[!UICONTROL Reconciliation key]**: these database fields (for example: email, first name, last name) are used to determine whether the visitor has a profile that is already known in the Adobe Campaign database. Dies erlaubt je nach gewählter Aktualisierungsstrategie, das existierende Profil zu aktualisieren oder ein neues zu erstellen.
1. Define the **[!UICONTROL Form parameter mapping]**: this section allows you to map the landing page field parameters and those used in the reconciliation key.
1. Select the **[!UICONTROL Update strategy]**: if the reconciliation key recovers an existing database profile, you can choose for this profile to be updated with the data entered in the form or instead prevent this update.


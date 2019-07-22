---
title: Ressource erstellen oder erweitern
seo-title: Ressource erstellen oder erweitern
description: Ressource erstellen oder erweitern
seo-description: Hier erfahren Sie, wie Sie eine neue Ressource definieren.
page-status-flag: nie aktiviert
uuid: 7 c 26 b 63 d -9587-472 b -804 f-cde 5 c 45 dfb 3 c
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird entwickelt
content-type: Referenz
topic-tags: adding-or-extending-a-resource
discoiquuid: 8 dc 45 c 37-6908-407 e -8 e 41-4 a 4188 cba 2 b 3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a7c7a46fdba2395c773582923c6bd647c2d6c9d6

---


# Ressource erstellen oder erweitern{#creating-or-extending-the-resource}

Administratoren können eine neue Ressource erstellen oder eine existierende Ressource erweitern, wenn Daten bearbeitet werden müssen, die nicht im vordefinierten Datenmodell enthalten sind.

Nur die folgenden nativen Ressourcen können erweitert werden:

* **[!UICONTROL Campaign (campaign)]**
* **[!UICONTROL Sendungen (delivery)]**
* **[!UICONTROL Landingpage (Landingpage)]**
* **[!UICONTROL Profile (profile)]**
* **[!UICONTROL Programm (program)]**
* **[!UICONTROL Service (service)]**
* **[!UICONTROL App-Abonnements (appSubscriptionRcp)]**
* **[!UICONTROL Testprofile (seedMember)]**
* **[!UICONTROL Workflow (workflow)]**

Wenn Sie eine Ressource erstellen oder erweitern möchten, gehen Sie wie folgt vor:

1. From **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Custom Resources]**, click the **[!UICONTROL Create]** button.
1. Wählen Sie die gewünschte Aktion:

   * **[!UICONTROL Neue Ressource erstellen]**: Füllen Sie die Felder **[!UICONTROL Titel]** und **ID]aus.[!UICONTROL ** Das Feld **[!UICONTROL Kennung]ist ein Pflichtfeld.** Falls kein Titel angegeben wird, wird dieser automatisch ausgehend von der Kennung vergeben.

      ![](assets/schema_extension_2.png)

      >[!NOTE]
      >
      >Wir führen einen Maximalbefehl von 30 Zeichen durch.

   * **[!UICONTROL Existierende Ressource erweitern]**: Wählen Sie die zu erweiternde Ressource aus.

      ![](assets/schema_extension_10.png)

1. Wählen Sie **[!UICONTROL Erstellen]** aus, um die Ressource zu erstellen. Diese erhält daraufhin den Status **[!UICONTROL Entwurf], falls es sich um eine neue Ressource handelt, oder den Status** In Bearbeitung] im Fall einer Erweiterung.**[!UICONTROL **

Die neue Ressource wird erstellt und kann jetzt konfiguriert werden. Weiterführende Informationen zur Ressourcenkonfiguration finden Sie im Abschnitt [Datenstruktur der Ressource konfigurieren](../../developing/using/configuring-the-resource-s-data-structure.md).

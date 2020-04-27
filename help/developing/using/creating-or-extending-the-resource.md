---
title: Ressource erstellen oder erweitern
description: Hier erfahren Sie, wie Sie eine neue Ressource definieren.
page-status-flag: never-activated
uuid: 7c26b63d-9587-472b-804f-cde5c45dfb3c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: 8dc45c37-6908-407e-8e41-4a4188cba2b3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 8852adb5edeb42eba1acf2911c988071104f1401

---


# Ressource erstellen oder erweitern{#creating-or-extending-the-resource}

Administratoren können eine neue Ressource von Grund auf neu erstellen oder eine Erweiterung einer vorhandenen Ressource erstellen, wenn Sie an Daten arbeiten müssen, die nicht Teil des integrierten Datenmodells sind.

Nur die folgenden integrierten Ressourcen können erweitert werden:

* **[!UICONTROL Campaign (campaign)]**
* **[!UICONTROL Deliveries (delivery)]**
* **[!UICONTROL Landing page (Landingpage)]**
* **[!UICONTROL Profiles (profile)]**
* **[!UICONTROL Program (program)]**
* **[!UICONTROL Service (service)]**
* **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]**
* **[!UICONTROL Test profiles (seedMember)]**
* **[!UICONTROL Workflow (workflow)]**

Wenn Sie eine Ressource erstellen oder erweitern möchten, gehen Sie wie folgt vor:

1. Klicken Sie **[!UICONTROL Administration]** > **[!UICONTROL Development]** > **[!UICONTROL Custom Resources]** auf die **[!UICONTROL Create]** Schaltfläche.
1. Wählen Sie die gewünschte Aktion:

   * **[!UICONTROL Create a new resource]**: Geben Sie die Felder **[!UICONTROL Label]** und **[!UICONTROL ID]** ein. The **[!UICONTROL ID]** field is mandatory. Falls kein Titel angegeben wird, wird dieser automatisch ausgehend von der Kennung vergeben.

      ![](assets/schema_extension_2.png)

      >[!NOTE]
      >
      >Verwenden Sie maximal 30 Zeichen.

   * **[!UICONTROL Extend an existing resource]**: Wählen Sie die Ressource aus, die Sie erweitern möchten.

      ![](assets/schema_extension_10.png)

1. Click **[!UICONTROL Create]** to create the resource, which will then take on the **[!UICONTROL Draft]** status in case of new resource or the **[!UICONTROL Editing]** status in case of extension.

Die neue Ressource wird erstellt und kann jetzt konfiguriert werden. Weiterführende Informationen zur Ressourcenkonfiguration finden Sie im Abschnitt [Datenstruktur der Ressource konfigurieren](../../developing/using/configuring-the-resource-s-data-structure.md).

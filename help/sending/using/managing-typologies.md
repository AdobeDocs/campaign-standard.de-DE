---
title: Typologien verwalten
description: Erfahren Sie, wie Sie Typologien verwenden.
page-status-flag: never-activated
uuid: a98ebc36-172d-4f46-b6ee-b2636a1007c9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
discoiquuid: 2590d94c-51ef-4c0f-b1ec-c2837e94da40
context-tags: typology,overview;typologyRule,main;typologyRule,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ba1fcca02ce9582d85e57bde815ccf3f551ac7a3

---


# Typologien verwalten {#managing-typologies}

## Typologien {#about-typologies}

Typologien sind Regelsätze, mit denen Sie die Gültigkeit Ihrer Nachricht überprüfen können, bevor Sie sie senden. Beispiel: Der Inhalt der Nachricht ist nicht leer, eine Abmeldung vorhanden, der Ausschluss von Duplikaten usw.

Auf Typologien kann über das Menü **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Typologies]** zugegriffen werden. Standardmäßig ist in der Anwendung eine Standardtypologie verfügbar. Sie können nach Bedarf auch eigene Typologien erstellen oder vorhandene abändern.

![](assets/typologies-list.png)

Für jede Typologie wird im **[!UICONTROL Typology rules]** Abschnitt der Regelsatz Liste, der bei Verwendung der Typologie mit einer Meldung ausgeführt wird.

![](assets/typology_typo-rule-list.png)

>[!NOTE]
>
>Wenn Sie weitere Informationen zu einer der Typologieregeln erhalten möchten, klicken Sie mit der Dublette darauf. Die Regel wird im schreibgeschützten Modus angezeigt.

## Creating a typology {#creating-a-typology}

Gehen Sie wie folgt vor, um eine neue Typologie zu erstellen:

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Typologies]** auf.

1. Die Liste der Typologien wird angezeigt. Click the **[!UICONTROL Create]** button.

   ![](assets/typologies-create.png)

1. Definieren Sie die Typologie **[!UICONTROL Label]** und klicken Sie dann auf die **[!UICONTROL Add an element]** Schaltfläche , um die Typologieregeln auszuwählen, die Sie darin aufnehmen möchten. For more on typology rules, refer to [this section](../../sending/using/managing-typology-rules.md).

   ![](assets/typology_addrules.png)

   >[!NOTE]
   >
   >The **[!UICONTROL IP affinity]** field allows you to manage the affinities according to your configuration. Sie werden in der Konfigurationsdatei der Instanz definiert. Wenn Sie die Affinitäten verwenden möchten, wenden Sie sich an Ihren Administrator.

1. Klicken Sie auf **[!UICONTROL Create]** , um Ihre Auswahl zu bestätigen. Ihre Typologie kann jetzt in Nachrichten verwendet werden.

## Typologien auf Nachrichten anwenden {#applying-typologies-to-messages}

Wenn Sie eine Typologie mit einer Meldungs- oder Meldungsvorlage verknüpfen, werden die in der Typologie enthaltenen Typologieregeln ausgeführt, um die Gültigkeit der Meldung zu überprüfen.

>[!NOTE]
>
>Jeder Nachrichten- oder Nachrichtenvorlage kann nur eine einzige Typologie zugewiesen werden.

Gehen Sie wie folgt vor, um eine Typologie mit einer Nachricht zu verknüpfen:

1. Greifen Sie auf die Meldungseigenschaften zu. Beachten Sie, dass Meldungsvorlagen über das **[!UICONTROL Resources]** > **[!UICONTROL Templates]** Navigationsmenü aufgerufen werden können.

1. Wählen Sie im Abschnitt **[!UICONTROL Advanced parameters]** > **[!UICONTROL Prearation]** die Typologie aus, die mit der Nachricht verknüpft werden soll.

   ![](assets/typology_message.png)

1. Klicks **[!UICONTROL Confirm]**.

   Die ausgewählte Typologie ist jetzt mit der Nachricht verknüpft. Alle zugehörigen Typologieregeln werden ausgeführt, um die Gültigkeit der Nachricht zu überprüfen.

---
title: '"Workflow-Anwendungsfall: Schaffung einer wöchentlichen Lieferung"'
seo-title: '"Workflow-Anwendungsfall: Schaffung einer wöchentlichen Lieferung"'
description: '"Workflow-Anwendungsfall: Schaffung einer wöchentlichen Lieferung"'
seo-description: '"Workflow-Anwendungsfall: Schaffung einer wöchentlichen Lieferung"'
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: 'execution-activities '
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: Workflow, Anwendungsfall, Abfrage, Lieferung, Scheduler
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4a38b1f3d7d6dbf12fa71c819147bf2d91acb0c4

---


# Worflow-Anwendungsfall: Erstellen Sie jeden Dienstag eine E-Mail{#creating-email-every-tuesday}

Sie können jeden Dienstag eine E-Mail an alle Kunden für Sonderangebote schicken.

1. In **[!UICONTROL Marketing Activities]**, click **[!UICONTROL Create]** and select **[!UICONTROL Workflow]**.
1. Wählen Sie **[!UICONTROL Neuer Workflow]** als Workflowtyp aus, und klicken Sie auf **[!UICONTROL Weiter]**.
1. Geben Sie die Eigenschaften des Workflows ein, und klicken Sie auf **[!UICONTROL Erstellen]**.

## Creating a Scheduler activity{#creating-a-scheduler-activity}

1. Bei **[!UICONTROL Aktivitäten]** &gt; **[!UICONTROL Ausführung]** ziehen Sie eine **[!UICONTROL Scheduler-Aktivität]** per Drag &amp; Drop.
1. Doppelklicken Sie auf die Aktivität.
1. Konfigurieren Sie die Ausführung Ihrer Lieferung.
1. Wählen Sie in der **[!UICONTROL Ausführungsfrequenz]** die Option **[!UICONTROL wöchentlich]** aus.
1. Wählen Sie eine **[!UICONTROL Zeit]** und eine **[!UICONTROL Wiederholungshäufigkeit]** für Ihre Lieferungen.
1. Wählen Sie in **[!UICONTROL Wochentagen]** den **[!UICONTROL Dienstag]** aus.
1. Geben Sie einen **[!UICONTROL Start]** - und einen **[!UICONTROL Ablaufparameter]** für den Workflow an.
1. Validieren Sie die Aktivität und speichern Sie den Workflow.

![](assets/scheduler_properties.png)

>[!NOTE]
>
>Um den Workflow in einer bestimmten **[!UICONTROL Zeitzone]** zu starten, legen Sie im Register **[!UICONTROL Ausführungsoptionen]** die Zeitzone für Ihren Scheduler im Feld Zeitzone fest.

## Creating a Query activity{#creating-a-query-activity}

1. Bei **[!UICONTROL Aktivitäten]** &gt; **[!UICONTROL Zielsetzung]**, um Empfänger auszuwählen, ziehen und löschen Sie eine **[!UICONTROL Abfrage]** Aktivität und doppelklicken Sie darauf.
1. Bei **[!UICONTROL Tastenkombinationen]** &gt; **[!UICONTROL Profil]** ziehen und ziehen Sie **[!UICONTROL E-Mail]**.
1. Als Operator **[!UICONTROL ist Select nicht leer]** .
1. Fügen Sie in **[!UICONTROL Tastenkombinationen]** &gt; **[!UICONTROL Allgemein]** Profile hinzu und wählen Sie **[!UICONTROL keinen Kontakt mehr per E-Mail]** mit dem Wert **[!UICONTROL Nein]** aus.
1. Wählen Sie **[!UICONTROL Bestätigen]**.

![](assets/wf-complement-query.png)

## Creating an Email delivery{#creating-an-email-delivery}

1. Bei **[!UICONTROL Aktivitäten]** &gt; **[!UICONTROL Kanäle]** ziehen und löschen Sie eine **[!UICONTROL E-Mail-Auslieferung]**.
1. Klicken Sie auf die Aktivität und wählen Sie ![](assets/edit_darkgrey-24px.png) zu bearbeiten.
1. Wählen Sie **[!UICONTROL E-Mail]** wiederherstellen aus, und klicken Sie auf **[!UICONTROL Weiter]**.
1. Wählen Sie eine E-Mail-Vorlage aus, und klicken Sie auf **[!UICONTROL Weiter]**.
1. Geben Sie die E-Mail-Eigenschaften ein und klicken Sie auf **[!UICONTROL Weiter]**.
1. Um das Layout Ihrer E-Mail zu erstellen, klicken Sie auf **[!UICONTROL E-Mail-Designer]** verwenden.
1. Fügen Sie Elemente ein oder wählen Sie eine vorhandene Vorlage aus.
1. Personalisieren Sie Ihre E-Mail mit Feldern und Links.
1. Wählen Sie **[!UICONTROL Speichern aus]**.

Weitere Informationen finden Sie unter [Entwerfen einer E-Mail](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).

**Verwandte Themen:**

* [Abfrageaktivität](../..//automating/using/query.md)
* [Aktivität "Planung"](../..//automating/using/scheduler.md)
* [E-Mail-Versand](../..//automating/using/email-delivery.md)
* [E-Mail-Kanal](../..//channels/using/creating-an-email.md)

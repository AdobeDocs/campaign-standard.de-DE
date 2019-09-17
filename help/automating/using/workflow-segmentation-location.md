---
title: '"Workflow-Anwendungsfall: Segmentierung am Standort"'
seo-title: '"Workflow-Anwendungsfall: Segmentierung am Standort"'
description: '"Workflow-Anwendungsfall: Segmentierung am Standort"'
seo-description: '"Workflow-Anwendungsfall: Segmentierung am Standort"'
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: 'Workflow, Anwendungsfall, Abfrage, Segmentierung, Lieferung '
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f7e56dcb4c2bbdc802c9d271d4a44d9a72b239ed

---


# Workflow-Anwendungsfall: Standortabgrenzung {#segmentation-on-location}

Sie können eine zielgerichtete E-Mail an Kunden mit Angeboten in ihren lokalen Geschäften schicken.

1. In **[!UICONTROL Marketing Activities]**, click **[!UICONTROL Create]** and select **[!UICONTROL Workflow]**.
1. Wählen Sie **[!UICONTROL Neuer Workflow]** als Workflowtyp aus, und klicken Sie auf **[!UICONTROL Weiter]**.
1. Geben Sie die Eigenschaften des Workflows ein, und klicken Sie auf **[!UICONTROL Erstellen]**.

## Auswählen der Empfänger per E-Mail{#selecting-recipients-contactable-via-email}

1. Bei **[!UICONTROL Aktivitäten]** &gt; **[!UICONTROL Targeting]** ziehen und löschen Sie eine **[!UICONTROL Abfrageaktivität]**![](assets/query.png).
1. Doppelklicken Sie auf die Aktivität.
1. Ziehen Sie in **[!UICONTROL Tastenkombinationen]** die **[!UICONTROL Profile]** , und wählen Sie das Feld **[!UICONTROL E-Mail]** mit dem Operator **[!UICONTROL ist nicht leer]**.
1. Ziehen Sie in **[!UICONTROL Tastenkombinationen]** die **[!UICONTROL Profile]** , und wählen Sie das Feld **[!UICONTROL nicht mehr per E-Mail]** mit dem Wert **[!UICONTROL nein]**.
1. Klicken Sie auf **[!UICONTROL Zweimal bestätigen]** .

![](assets/wf-complement-query.png)

## Creating a Segmentation activity{#creating-a-segmentation-activity}

1. Ziehen Sie eine **[!UICONTROL Segmentierungsaktivität]** ab und doppelklicken Sie darauf.
1. Klicken Sie auf Segment und öffnen Sie dann den Übergang zu Zielgruppen in der ersten Stadt. Hier Boston.
1. Ziehen und Ablegen von **[!UICONTROL Standort]** und wählen Sie **[!UICONTROL Stadt]** mit dem Operator **[!UICONTROL entspricht]** und den Wert **[!UICONTROL Boston]**.
Hinweis: Um alle Personen zu erreichen, die in Boston eintrafen, deaktivieren Sie die Option für die Groß- und Kleinschreibung, ohne Rücksicht auf den Fall.
1. Wählen Sie **[!UICONTROL Bestätigen]**.
1. Klicken Sie in der **[!UICONTROL Liste der ausgehenden Segmente]** auf **[!UICONTROL Element]** hinzufügen, und klicken Sie auf ![](assets/edit_darkgrey-24px.png) , um ein Segment zu erstellen, das auf Personen in der zweiten Stadt zugeschnitten ist. Hier Chicago.
1. Ziehen und Ablegen **[!UICONTROL Location]** und wählen Sie **[!UICONTROL City]** mit dem Operator **[!UICONTROL gleicht]** und geben Sie **[!UICONTROL Chicago]** in Wert ein.
1. Um alle Personen zu erreichen, die Chicago betraten, deaktivieren Sie die Option Groß-/Kleinschreibung, ohne den Fall zu berücksichtigen.
1. Wählen Sie **[!UICONTROL Bestätigen]**.

## Creating an email delivery{#creating-an-email-delivery}

1. Bei **[!UICONTROL Aktivitäten]** &gt; **[!UICONTROL Channels]** ziehen Sie nach jedem Segment eine **[!UICONTROL E-Mail-Zustellung]** , und lassen Sie diese abbrechen.
1. Klicken Sie auf die Aktivität und wählen Sie ![](assets/edit_darkgrey-24px.png) zu bearbeiten.
1. Wählen Sie **[!UICONTROL Einfache E-Mail]** aus, und klicken Sie auf **[!UICONTROL Weiter]**.
1. Wählen Sie eine E-Mail-Vorlage aus, und klicken Sie auf **[!UICONTROL Weiter]**.
1. Geben Sie die E-Mail-Eigenschaften ein und klicken Sie auf **[!UICONTROL Weiter]**.
1. Um das Layout Ihrer E-Mail zu erstellen, klicken Sie auf **[!UICONTROL E-Mail-Designer]**.
1. Fügen Sie Elemente ein oder wählen Sie eine vorhandene Vorlage aus.
1. Personalisieren Sie Ihre E-Mail mit spezifischen Angeboten für jeden Standort.

Weitere Informationen finden Sie unter [Entwerfen einer E-Mail](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).

1. Klicken Sie auf **[!UICONTROL Vorschau]** , um Ihr Layout zu überprüfen.
1. Wählen Sie **[!UICONTROL Speichern aus]**.

![](assets/wf-segmentation-location.png)

**Verwandte Themen:**

* [Abfrageaktivität](../../automating/using/query.md)
* [Segmenttätigkeit](../../automating/using/segmentation.md)
* [E-Mail-Versand](../../automating/using/email-delivery.md)

---
solution: Campaign Standard
product: campaign
title: Wöchentlichen Versand erstellen
description: Dieser Anwendungsfall zeigt, wie man einen wöchentlichen Versand erstellt.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: workflow,use-case,query,delivery,scheduler
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 100%

---


# Jeden Dienstag einen E-Mail-Versand erstellen{#creating-email-every-tuesday}

Sie haben die Möglichkeit, beispielsweise jeden Dienstag allen Kunden eine E-Mail mit speziellen Angeboten zu senden.

1. Wählen Sie dazu in **[!UICONTROL Marketingaktivitäten]** die Option **[!UICONTROL Erstellen]** und dann **[!UICONTROL Workflow]** aus.
1. Wählen Sie als Workflow-Typ **[!UICONTROL Neuer Workflow]** und danach **[!UICONTROL Weiter]** aus.
1. Geben Sie die Eigenschaften des Workflows ein und wählen Sie **[!UICONTROL Erstellen]** aus.

## Planungsaktivität erstellen{#creating-a-scheduler-activity}

1. Ziehen Sie in **[!UICONTROL Aktivitäten]** > **[!UICONTROL Ausführung]** eine [](../../automating/using/scheduler.md)Planungsaktivität in den Arbeitsbereich.
1. Doppelklicken Sie auf die Aktivität.
1. Konfigurieren Sie Ihren Versand.
1. Wählen Sie in **[!UICONTROL Ausführungsfrequenz]** die Option **[!UICONTROL Wöchentlich]** aus.
1. Wählen Sie eine **[!UICONTROL Zeit]** und das **[!UICONTROL Ausführungsintervall]** für Ihre Sendungen aus.
1. Wählen Sie in **[!UICONTROL Wochentage]** **[!UICONTROL Dienstag]** aus.
1. Geben Sie für Ihren Workflow einen **[!UICONTROL Start]** und einen **[!UICONTROL Gültigkeitsparameter]** ein.
1. Bestätigen Sie die Aktivität und speichern Sie den Workflow.

![](assets/scheduler_properties.png)

>[!NOTE]
>
>Um Ihren Workflow in einer bestimmten Zeitzone auszuführen, richten Sie in den **[!UICONTROL Ausführungsoptionen]** die Zeitzone für Ihren Zeitplan im Feld **[!UICONTROL Zeitzone]** ein. Standardmäßig ist die ausgewählte Zeitzone die in den Eigenschaften des Workflows definierte Zeitzone (siehe [Workflow erstellen](../../automating/using/building-a-workflow.md)).

## Abfrageaktivität erstellen{#creating-a-query-activity}

1. Um Empfänger auszuwählen, ziehen Sie in **[!UICONTROL Aktivitäten]** > **[!UICONTROL Targeting]** eine [Abfrageaktivität](../../automating/using/query.md) in den Arbeitsbereich und doppelklicken Sie darauf.
1. Ziehen Sie in **[!UICONTROL Schnellzugriffe]** > **[!UICONTROL Profil]** die Option **[!UICONTROL E-Mail]** in den Arbeitsbereich.
1. Wählen Sie als Operator **[!UICONTROL Ist nicht leer]** aus.
1. Fügen Sie in **[!UICONTROL Schnellzugriffe]** > **[!UICONTROL Allgemein]** Profile hinzu und wählen Sie **[!UICONTROL Nicht mehr per E-Mail kontaktieren]** mit dem Wert **[!UICONTROL Nein]** aus.
1. Wählen Sie **[!UICONTROL Bestätigen]** aus.

![](assets/wf-complement-query.png)

## E-Mail-Versand erstellen{#creating-an-email-delivery}

1. Ziehen Sie in **[!UICONTROL Aktivitäten]** > **[!UICONTROL Kanäle]** die Aktivität [E-Mail-Versand](../../automating/using/email-delivery.md) in den Arbeitsbereich.
1. Wählen Sie die Aktivität aus und danach ![](assets/edit_darkgrey-24px.png), um die Bearbeitung zu ermöglichen.
1. Wählen Sie **[!UICONTROL Wiederkehrende E-Mail]** und danach **[!UICONTROL Weiter]** aus.
1. Wählen Sie eine E-Mail-Vorlage und danach **[!UICONTROL Weiter]** aus.
1. Geben Sie die E-Mail-Eigenschaften ein und wählen Sie **[!UICONTROL Weiter]** aus.
1. Um das Layout Ihrer E-Mail zu definieren, wählen Sie **[!UICONTROL Email Designer]** aus.
1. Fügen Sie Elemente ein oder wählen Sie eine bestehende Vorlage aus.
1. Personalisieren Sie Ihre E-Mail mit Feldern und Links.
1. Wählen Sie **[!UICONTROL Speichern]** aus.

Weiterführende Informationen dazu finden Sie im Abschnitt zum [Gestalten einer E-Mail](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).

**Verwandte Themen:**

* [E-Mail-Kanal](../../channels/using/creating-an-email.md)

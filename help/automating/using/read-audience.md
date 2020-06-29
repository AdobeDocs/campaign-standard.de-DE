---
title: Audience lesen
description: Die Lesen-der-Audience-Aktivität ermöglicht es Ihnen, eine vorhandene Audience abzurufen und sie durch zusätzliche Filterbedingungen einzuengen.
page-status-flag: never-activated
uuid: 58c54e71-f4a7-4ae9-80a3-33c379ab1db9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 674684e5-8830-4d2f-ba97-59ed4ba7422f
context-tags: readAudience,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c3911232a3cce00c2b9a2e619f090a7520382dde
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 93%

---


# Audience lesen{#read-audience}

## Beschreibung {#description}

![](assets/prefill.png)

Die Aktivität **[!UICONTROL Lesen der Audience]** ermöglicht es Ihnen, eine vorhandene Audience abzurufen und sie durch zusätzliche Filterbedingungen einzuengen.

## Anwendungskontext {#context-of-use}

Die Aktivität **[!UICONTROL Lesen der Audience]** ist eine einfachere Version der **[!UICONTROL Abfrage]**-Aktivität und eignet sich für Fälle, in denen Sie nur eine bestehende Audience auswählen müssen.

**Verwandte Themen**

* [Verwendungsfall: Vereinigung auf zwei raffinierten Audiencen](../../automating/using/union-on-two-refined-audiences.md)
* [Verwendungsfall: Datei-Audience mit der Datenbank abgleichen](../../automating/using/reconcile-file-audience-with-database.md)

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Lesen der Audience]**-Aktivität in den Workflow-Arbeitsbereich.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der im Schnellzugriff angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Wählen Sie die Audience, die Sie abrufen möchten, im Tab **[!UICONTROL Eigenschaften]** aus.

   Sie können die folgenden Typen von Audiences abrufen: **[!UICONTROL Liste]**, **[!UICONTROL Abfrage]**, **[!UICONTROL Datei]** und **[!UICONTROL Experience Cloud]**. Lesen Sie für weiterführende Informationen das [Audience-Handbuch](../../audiences/using/about-audiences.md).

   Mit der Option **[!UICONTROL Dynamische Audience verwenden]** können Sie den Namen der jeweiligen Audience auf der Basis der Ereignisvariablen des Workflows definieren. Weiterführende Informationen dazu finden Sie im Abschnitt [Anpassen von Aktivitäten mit Ereignisvariablen](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables).

   ![](assets/readaudience_activity1.png)

1. Wenn Sie an die ausgewählte Audience weitere Filter anlegen möchten, fügen Sie Bedingungen über den Tab **[!UICONTROL Quellenfilterung]** der Aktivität hinzu.

   Weiterführende Informationen zur Erstellung von Filterbedingungen finden Sie im Abschnitt [Vorlagen erstellen](../../automating/using/editing-queries.md#creating-queries).

1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

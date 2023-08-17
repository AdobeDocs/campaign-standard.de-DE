---
title: Audience lesen
description: Die Lesen-der-Audience-Aktivität ermöglicht es Ihnen, eine vorhandene Audience abzurufen und sie durch zusätzliche Filterbedingungen einzuengen.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: readAudience,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 9a77a2c7-cc1c-416f-8103-bb7d5c84a373
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 100%

---

# Audience lesen{#read-audience}

## Beschreibung {#description}

![](assets/prefill.png)

Die Aktivität **[!UICONTROL Audience lesen]** ermöglicht es Ihnen, eine vorhandene Audience abzurufen und sie durch zusätzliche Filterbedingungen einzuengen.

## Anwendungskontext {#context-of-use}

Die Aktivität **[!UICONTROL Audience lesen]** ist eine einfachere Version der **[!UICONTROL Abfrage]**-Aktivität und eignet sich für Fälle, in denen Sie nur eine bestehende Audience auswählen müssen.

**Verwandte Themen**

* [Anwendungsfall: Vereinigung von zwei eingegrenzten Audiences](../../automating/using/union-on-two-refined-audiences.md)
* [Anwendungsfall: Eine Audience vom Typ &quot;Datei&quot; mit der Datenbank abstimmen](../../automating/using/reconcile-file-audience-with-database.md)

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Audience lesen]**-Aktivität in den Workflow-Arbeitsbereich.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in der Schnellaktion angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Wählen Sie die Audience, die Sie abrufen möchten, im Tab **[!UICONTROL Eigenschaften]** aus.

   Sie können die folgenden Typen von Audiences abrufen: **[!UICONTROL Liste]**, **[!UICONTROL Abfrage]**, **[!UICONTROL Datei]** und **[!UICONTROL Experience Cloud]**. Lesen Sie für weiterführende Informationen das [Audience-Handbuch](../../audiences/using/about-audiences.md).

   Mit der Option **[!UICONTROL Dynamische Audience verwenden]** können Sie den Namen der jeweiligen Audience auf der Basis der Ereignisvariablen des Workflows definieren. Weitere Informationen hierzu finden Sie auf [dieser Seite](../../automating/using/customizing-workflow-external-parameters.md).

   ![](assets/readaudience_activity1.png)

1. Wenn Sie an die ausgewählte Audience weitere Filter anlegen möchten, fügen Sie Bedingungen über den Tab **[!UICONTROL Quellenfilterung]** der Aktivität hinzu.

   Weiterführende Informationen zur Erstellung von Filterbedingungen finden Sie im Abschnitt [Vorlagen erstellen](../../automating/using/editing-queries.md#creating-queries).

1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

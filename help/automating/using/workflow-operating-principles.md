---
title: Funktionsweise von Workflows
description: Hier erhalten Sie die wichtigsten Informationen zu Workflows.
page-status-flag: never-activated
uuid: 85755e85-617b-4a9b-bb30-96ba8333f4f0
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
discoiquuid: 3a13785d-1ef7-4043-9927-2d495b83709f
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Funktionsweise von Workflows{#workflow-operating-principles}

Ein Workflow besteht aus einer **Abfolge konfigurierbarer Aktivitäten**. Jeder Aktivität kommt im Rahmen des Prozesses eine spezifische Rolle zu. Das Ergebnis der Aktivitäten wird über eine durch einen Pfeil symbolisierte **Transition** an die anschließende Aktivität übermittelt.

Die Art der von einer Aktivität zur nächsten übermittelten Daten kann die Konfiguration der Folgeaktivitäten beeinflussen. Wenn beispielsweise ein E-Mail-Versand auf eine Zielbestimmungsaktivität folgt, kann die in letzterer ermittelte Population als Zielgruppe für den Versand verwendet werden.

Sie können Aktivitäten vor oder nach der Ausführung des Workflows öffnen, um Parameter zu überprüfen oder abzuändern.

Sie können Transitionen vor oder nach der Ausführung des Workflows öffnen, um zu überprüfen, ob die übermittelten Daten korrekt sind. Um zur Detailansicht der Transitionen zu gelangen, müssen Sie die Option **[!UICONTROL Zwischenergebnis festhalten]** im Abschnitt **[!UICONTROL Ausführung]** der Workflow-Eigenschaften ankreuzen.

![](assets/workflow_overview.png)


---
title: Workflow-Daten verwenden
description: Hier erfahren Sie, wie Sie die von Ihnen importierten oder ausgewählten Daten nutzen können.
page-status-flag: never-activated
uuid: 3dd66aeb-3a26-4214-b6a0-242c2b7fbc49
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 90b250f1-f32d-4256-83ea-4c0627628610
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Workflow-Daten verwenden{#using-workflow-data}

Nach Identifizierung und Aufbereitung der Daten können diese in folgenden Kontexten verwendet werden:

* Ein **[!UICONTROL Daten-Update]** ermöglicht eine gebündelte Aktualisierung der Datenbankfelder.
* Mithilfe der **[!UICONTROL Audience-Speicherung]** können existierende Audiences aktualisiert oder neue erstellt werden. Die hierfür erforderlichen Populationen werden im Vorfeld durch andere Workflow-Aktivitäten ermittelt. Auf diese Weise erstellte oder aktualisierte Audiences sind vom Typ **Liste** oder **Datei.** Außerdem ermöglicht diese Aktivität den Export von Profilen in Form von Adobe-Experience-Cloud-Zielgruppen/Segmenten.
* Mithilfe der Aktivität **[!UICONTROL An-/Abmeldedienst]** lassen sich Profile gesammelt für Dienste an- bzw. von Diensten abmelden.
* Die Aktivität **[!UICONTROL Dateiextraktion]** erlaubt den Export von in Adobe Campaign enthaltenen Daten in Form von externen Dateien.

Nach der Definition eines Profilziels können Sie mehrere Aktivitäten verwenden, um Sendungen zu erstellen und durchzuführen:

* Die **[!UICONTROL E-Mail-Versandaktivität]** ermöglicht den Versand von E-Mails innerhalb eines Workflows. Dabei kann es sich um eine **Einmalige E-Mail** handeln, die nur einmal gesendet wird, oder um eine **Wiederkehrende E-Mail**.
* Die **[!UICONTROL SMS-Versandaktivität]** ermöglicht den Versand von SMS innerhalb eines Workflows. Bei **einmaligen Versandaktionen** handelt es sich um Standard-SMS, die nur **einmal** gesendet werden.
* Der **[!UICONTROL Mobile-App-Versand]** ermöglicht das Konfigurieren des Versands von Push-Benachrichtigungen innerhalb eines Workflows. Diese Benachrichtigung kann **einmalig** sein oder **wiederkehrend**.


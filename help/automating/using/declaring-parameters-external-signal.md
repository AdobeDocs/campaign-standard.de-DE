---
solution: Campaign Standard
product: campaign
title: Workflow mit externen Parametern aufrufen
description: In diesem Abschnitt wird beschrieben, wie ein Workflow mit externen Parametern aufgerufen wird.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 100%

---


# Parameter in der Aktivität &quot;Externes Signal&quot; deklarieren     {#declaring-the-parameters-in-the-external-signal-activity}

Um einen Workflow mit Parametern aufzurufen, müssen Sie diese zunächst in der Aktivität **[!UICONTROL Externes Signal]** deklarieren.

1. Öffnen Sie die Aktivität **[!UICONTROL Externes Signal]** und wählen Sie den Tab **[!UICONTROL Parameter]** aus.
1. Wählen Sie die Schaltfläche **[!UICONTROL Element erstellen]** aus und geben Sie den Namen und den Typ eines jeden Parameters an.

   >[!CAUTION]
   >
   >Stellen Sie sicher, dass Name und Anzahl der Parameter mit der Definition beim Aufrufen des Workflows übereinstimmen (siehe [diese Seite](../../automating/using/defining-parameters-calling-workflow.md)). Darüber hinaus müssen die Parametertypen den erwarteten Werten entsprechen.

   ![](assets/extsignal_declaringparameters_1.png)

1. Schließen Sie nach der Deklaration der Parameter die Konfiguration des Workflows ab und führen Sie ihn aus.

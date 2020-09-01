---
title: Workflow mit externen Parametern aufrufen
description: In diesem Abschnitt wird beschrieben, wie ein Workflow mi externen Parametern aufgerufen wird.
page-status-flag: never-activated
uuid: beccd1b6-8e6d-4504-9152-9ff537459c4a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 1676da91-55e3-414f-bcd3-bb0804b682bd
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 51e98bb6212ad96d9c11b848df9dcad25b3f1b61
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 70%

---


# Parameter in der Aktivität &quot;Externes Signal&quot; deklarieren   {#declaring-the-parameters-in-the-external-signal-activity}

Um einen Workflow mit Parametern aufzurufen, müssen Sie diese zunächst in der Aktivität **[!UICONTROL Externes Signal]** deklarieren.

1. Öffnen Sie die Aktivität **[!UICONTROL Externes Signal]** und wählen Sie den Tab **[!UICONTROL Parameter]** aus.
1. Wählen Sie die Schaltfläche **[!UICONTROL Element erstellen]** aus und geben Sie den Namen und den Typ eines jeden Parameters an.

   >[!CAUTION]
   >
   >Stellen Sie sicher, dass Name und Anzahl der Parameter identisch mit denen sind, die beim Aufrufen des Workflows definiert wurden (siehe [](../../automating/using/defining-parameters-calling-workflow.md)). Darüber hinaus müssen die Parametertypen den erwarteten Werten entsprechen.

   ![](assets/extsignal_declaringparameters_1.png)

1. Nachdem die Parameter deklariert wurden, beenden Sie die Workflow-Konfiguration und führen Sie sie aus.

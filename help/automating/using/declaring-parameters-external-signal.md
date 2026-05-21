---
title: Parameter in der Aktivität Externes Signal deklarieren
description: In diesem Abschnitt wird beschrieben, wie ein Workflow mit externen Parametern aufgerufen wird.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: e6148b40-f608-4aab-81f6-756608c6828e
TQID: https://experienceleague.adobe.com/au0xUZ7C8m3hiK9wbm3QBiHd9RtpZQW-AEoc-SvnhfE
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 100%

---

# Parameter in der Aktivität „Externes Signal“ deklarieren {#declaring-the-parameters-in-the-external-signal-activity}

Um einen Workflow mit Parametern aufzurufen, müssen Sie diese zunächst in der Aktivität **[!UICONTROL Externes Signal]** deklarieren.

1. Öffnen Sie die Aktivität **[!UICONTROL Externes Signal]** und wählen Sie den Tab **[!UICONTROL Parameter]** aus.
1. Wählen Sie die Schaltfläche **[!UICONTROL Element erstellen]** aus und geben Sie den Namen und den Typ eines jeden Parameters an.

   >[!CAUTION]
   >
   >Stellen Sie sicher, dass Name und Anzahl der Parameter mit der Definition beim Aufrufen des Workflows übereinstimmen (siehe [diese Seite](../../automating/using/defining-parameters-calling-workflow.md)). Darüber hinaus müssen die Parametertypen den erwarteten Werten entsprechen.

   ![](assets/extsignal_declaringparameters_1.png)

1. Schließen Sie nach der Deklaration der Parameter die Konfiguration des Workflows ab und führen Sie ihn aus.

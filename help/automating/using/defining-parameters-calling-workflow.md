---
title: Parameter beim Aufruf des Workflows definieren
description: In diesem Abschnitt wird beschrieben, wie ein Workflow mit externen Parametern aufgerufen wird.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: f7de0186-4136-4603-8f80-9f58c641cd9d
TQID: https://experienceleague.adobe.com/-YjlK1Op8P08sxb--BOHl8AWyciX4BqPnCPQ3lpD3Co
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: b12f6872-9271-4369-85e5-86969a0b99a2
subfeature_v2: id: bf97c196-a4d1-4fa3-a151-e68a114c8ac0
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 203
ht-degree: 100%

---

# Parameter beim Aufruf des Workflows definieren {#defining-the-parameters-when-calling-the-workflow}

In diesem Abschnitt wird beschrieben, wie Sie Parameter beim Aufruf eines Workflows definieren können. Weiterführende Informationen zur Durchführung dieses Vorgang mit einem API-Aufruf finden Sie in der [REST-APIs-Dokumentation](../../api/using/triggering-a-signal-activity.md).

Vor der Definition der Parameter müssen folgende Voraussetzungen gegeben sein:

* Die Parameter wurden in der Aktivität **[!UICONTROL Externes Signal]** deklariert. Weitere Informationen finden Sie auf [dieser Seite](../../automating/using/declaring-parameters-external-signal.md).
* Der Workflow, der die Signalaktivität enthält, wird ausgeführt.

Gehen Sie zur Konfiguration der **[!UICONTROL Ende]**-Aktivität folgendermaßen vor:

1. Öffnen Sie die Aktivität **[!UICONTROL Ende]** und wählen Sie dann den Tab **[!UICONTROL Externes Signal]** aus.
1. Wählen Sie den Workflow und die Aktivität &quot;Externes Signal&quot; aus, die aufgerufen werden sollen.
1. Wählen Sie die Schaltfläche **[!UICONTROL Element erstellen]** aus, um einen Parameter hinzuzufügen. Geben Sie dann Namen und Wert ein.

   * **[!UICONTROL Name]**: der Name, der in der Aktivität **[!UICONTROL Externes Signal]** angegeben wurde (siehe [diese Seite](../../automating/using/declaring-parameters-external-signal.md)).
   * **[!UICONTROL Wert]**: der Wert, der dem Parameter zugewiesen werden soll. Der Wert sollte der **Standardsyntax** entsprechen, die in [diesem Abschnitt](../../automating/using/advanced-expression-editing.md#standard-syntax) beschrieben wird.

   ![](assets/extsignal_definingparameters_2.png)

   >[!CAUTION]
   >
   >Stellen Sie sicher, dass alle Parameter in der Aktivität **[!UICONTROL Externes Signal]** deklariert wurden. Andernfalls tritt ein Fehler beim Ausführen der Aktivität auf.

1. Bestätigen Sie nach der Definition der Parameter die Aktivität und speichern Sie Ihren Workflow.

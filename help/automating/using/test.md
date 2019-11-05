---
title: Test
description: Die Test-Aktivität ermöglicht eine Transition auf der Basis eines Testergebnisses.
page-status-flag: never-activated
uuid: 1562ec7a-253a-4f4f-b66a-c2948b57775a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 2650bf1f-0bce-4049-a226-2369f6666b95
context-tags: jstest,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Test{#test}

## Beschreibung {#description}

![](assets/test.png)

Die **[!UICONTROL Test]**-Aktivität ermöglicht eine Transition auf der Basis eines Testergebnisses.

## Anwendungskontext {#context-of-use}

Mit einer **Test**-Aktivität wird die erste Transition aktiviert, die die damit verknüpfte Bedingung erfüllt.

Wenn keine Bedingung erfüllt wird und die Option **Use default transition** aktiviert ist, wird eine Standardtransition aktiviert.

![](assets/wkf_test_activity_example.png)

Bedingungen können auf **Funktionen** oder **Variablen** basieren, z. B. Ereignisvariablen, die in der Workflow-Aktivität **[!UICONTROL Externes Signal]** deklariert wurden.

**Verwandte Themen:**

* [Funktionsliste](../../automating/using/list-of-functions.md)
* [Workflow mit externen Parametern aufrufen](../../automating/using/calling-a-workflow-with-external-parameters.md)

## Konfiguration  {#configuration}

1. Ziehen Sie eine **[!UICONTROL Test]**-Aktivität in den Workflow-Arbeitsbereich.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der ![-Schaltfläche aus den angezeigten Quick Actions.](assets/edit_darkgrey-24px.png)
1. Definieren Sie die Attribute einer jeden Bedingung:

   Zur Bearbeitung des Felds **[!UICONTROL Bedingung]** stehen zwei Schaltflächen zur Verfügung, mit denen Ereignisvariablen aufgerufen und Ausdrücke durch die Kombination von Variablen und Funktionen bearbeitet werden können:

   * ![](assets/extsignal_picker.png): Wählen Sie die Ereignisvariable unter den im Workflow verfügbaren Variablen aus (siehe [Workflow mit externen Parametern anpassen](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-a-workflow-with-external-parameters)).

      ![](assets/wkf_test_activity_variables.png)

   * ![](assets/extsignal_expression_editor.png): Hier können Sie Ausdrücke durch eine Kombination von Variablen und Funktionen bearbeiten. Weiterführende Informationen zum Ausdruckseditor finden Sie in [diesem Abschnitt](../../automating/using/advanced-expression-editing.md).

      ![](assets/wkf_test_activity_variables_expression.png)


---
title: Test
seo-title: Test
description: Test
seo-description: Die Test-Aktivität ermöglicht eine Transition auf der Basis eines Testergebnisses.
page-status-flag: nie aktiviert
uuid: 1562 ec 7 a -253 a -4 f 4 f-b 66 a-c 2948 b 57775 a
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird automatisiert
content-type: Referenz
topic-tags: execution-activities
discoiquuid: 2650 bf 1 f -0 bce -4049-a 226-2369 f 6666 b 95
context-tags: längste, Haupt
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Test{#test}

## Beschreibung {#description}

![](assets/test.png)

Die **[!UICONTROL Test]-Aktivität ermöglicht eine Transition auf der Basis eines Testergebnisses.**

## Anwendungskontext {#context-of-use}

Mit einer **Test**-Aktivität wird die erste Transition aktiviert, die die damit verknüpfte Bedingung erfüllt.

Wenn keine Bedingung erfüllt wird und die Option **Use default transition** aktiviert ist, wird eine Standardtransition aktiviert.

![](assets/wkf_test_activity_example.png)

Bedingungen können auf **Funktionen** oder **Variablen** basieren, z. B. Ereignisvariablen, die in der Workflow-Aktivität **[!UICONTROL Externes Signal]deklariert wurden.**

**Verwandte Themen:**

* [Funktionsliste](../../automating/using/list-of-functions.md)
* [Workflow mit externen Parametern aufrufen](../../automating/using/calling-a-workflow-with-external-parameters.md)

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Test]-Aktivität in den Workflow-Arbeitsbereich.**
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der ![-Schaltfläche aus den angezeigten Quick Actions.](assets/edit_darkgrey-24px.png)
1. Definieren Sie die Attribute einer jeden Bedingung:

   Zur Bearbeitung des Felds **[!UICONTROL Bedingung]stehen zwei Schaltflächen zur Verfügung, mit denen Ereignisvariablen aufgerufen und Ausdrücke durch die Kombination von Variablen und Funktionen bearbeitet werden können:**

   * ![](assets/extsignal_picker.png): Wählen Sie die Ereignisvariable unter den im Workflow verfügbaren Variablen aus (siehe [Workflow mit externen Parametern anpassen](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-a-workflow-with-external-parameters)).

      ![](assets/wkf_test_activity_variables.png)

   * ![](assets/extsignal_expression_editor.png): Hier können Sie Ausdrücke durch eine Kombination von Variablen und Funktionen bearbeiten. Weiterführende Informationen zum Ausdruckseditor finden Sie in [diesem Abschnitt](../../automating/using/advanced-expression-editing.md).

      ![](assets/wkf_test_activity_variables_expression.png)


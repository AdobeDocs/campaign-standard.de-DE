---
title: Test
description: Die Test-Aktivität ermöglicht eine Transition auf der Basis eines Testergebnisses.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: jstest,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 62a064f7-6d0b-49ca-9834-eccb5bf42496
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: ht
source-wordcount: '196'
ht-degree: 100%

---

# Test{#test}

## Beschreibung {#description}

![](assets/test.png)

Die Aktivität **[!UICONTROL Test]** ermöglicht eine Transition auf der Basis eines Testergebnisses.

## Anwendungskontext {#context-of-use}

Mit einer **Test**-Aktivität wird die erste Transition aktiviert, die die damit verknüpfte Bedingung erfüllt.

Wenn keine Bedingung erfüllt wird und die Option **Use default transition** aktiviert ist, wird eine Standardtransition aktiviert.

![](assets/wkf_test_activity_example.png)

Bedingungen können auf **Funktionen** oder **Variablen** basieren, z. B. Ereignisvariablen, die in der Workflow-Aktivität **[!UICONTROL Externes Signal]** deklariert wurden.

**Verwandte Themen:**

* [Funktionsliste](../../automating/using/list-of-functions.md)
* [Workflow mit externen Parametern aufrufen](../../automating/using/calling-a-workflow-with-external-parameters.md)

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Test]**-Aktivität in den Workflow-Arbeitsbereich.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in der Schnellaktion angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Definieren Sie die Attribute einer jeden Bedingung:

   Zur Bearbeitung des Felds **[!UICONTROL Bedingung]** stehen zwei Schaltflächen zur Verfügung, mit denen Ereignisvariablen aufgerufen und Ausdrücke durch die Kombination von Variablen und Funktionen bearbeitet werden können:

   * ![](assets/extsignal_picker.png): Wählen Sie die Ereignisvariable aus den im Workflow verfügbaren Variablen aus (siehe [diese Seite](../../automating/using/customizing-workflow-external-parameters.md)).

     Beispielsweise können Sie die Anzahl der heruntergeladenen Dateien nach einer [Dateiübertragungsaktivität](../../automating/using/transfer-file.md) mit der Variablen **[!UICONTROL filesCount]** überprüfen.

     ![](assets/wkf_test_activity_variables.png)

   * ![](assets/extsignal_expression_editor.png): Hier können Sie Ausdrücke durch eine Kombination von Variablen und Funktionen bearbeiten. Weiterführende Informationen zum Ausdruckseditor finden Sie in [diesem Abschnitt](../../automating/using/advanced-expression-editing.md).

     ![](assets/wkf_test_activity_variables_expression.png)

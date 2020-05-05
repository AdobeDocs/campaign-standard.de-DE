---
title: Audiences erstellen
description: Hier erfahren Sie, wie Sie Audiences in Adobe Campaign erstellen.
page-status-flag: never-activated
uuid: fe99b31b-a949-4832-b0e6-2b36d1c8be80
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
discoiquuid: df8bdcfb-be5e-4044-bc26-aa3466accbbe
context-tags: readAudience,main;audience,overview;delivery,audience,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 68e825bc3b6b7f94f61875e7da2bc8f63f06d9cb

---


# Audiences erstellen{#creating-audiences}

## Audiences vom Typ Abfrage erstellen {#creating-query-audiences}

In diesem Abschnitt wird die Erstellung einer Audience vom Typ **Abfrage** beschrieben. Audiences lassen sich des Weiteren in einem [Workflow](../../automating/using/get-started-workflows.md) mithilfe eines Dateiimports oder einer Zielgruppenbestimmung erstellen.

Ausgehend von der Audience-Liste erfolgt die Erstellung von Audiences entweder mittels Abfrage von Adobe-Campaign-Profilen oder durch Importieren einer Zielgruppe aus Adobe Experience Cloud.

1. Der Zugriff auf die Audience-Liste erfolgt über den Tab bzw. die Karte **[!UICONTROL Audiences]**.

   ![](assets/audiences_query_1.png)

1. Select **[!UICONTROL Create]** to access the screen to create a new audience.

   ![](assets/audiences_query.png)

1. Vergeben Sie einen Titel für Ihre Audience. Der Titel wird in der Audience-Liste und in der Palette des Abfragetools verwendet.
1. Choose a **[!UICONTROL Query]** audience type: the audiences defined by a query are recomputed at each further use.

   ![](assets/audience_type_selection.png)

1. Then select the **[!UICONTROL Targeting dimension]** that you would like to use to filter your customers. Die Zielgruppendimension ist für jede Audience eindeutig. Sie können also keine Audience erstellen, die etwa aus Testprofilen und Abonnenten zugleich besteht. Weiterführende Informationen zum Thema Zielgruppendimension finden Sie auf [dieser Seite](../../automating/using/query.md#targeting-dimensions-and-resources).
1. Erstellen Sie die Abfrage zur Bestimmung der Audience-Population. Lesen Sie diesbezüglich auch den Abschnitt [Abfragen erstellen](../../automating/using/editing-queries.md).
1. Click the **[!UICONTROL Create]** button to save your audience.

>[!NOTE]
>
>You can add a description to this audience and define the access authorizations via the **[!UICONTROL Edit properties]** icon.

## Audiences vom Typ Liste erstellen {#creating-list-audiences}

In diesem Abschnitt wird die Erstellung einer Audience vom Typ **Liste** beschrieben. Audiences dieser Art werden in Workflows unter Verwendung von Zielgruppenbestimmungsaktivitäten erstellt.  lassen sich des Weiteren mithilfe eines Dateiimports in einem [Workflow](../../automating/using/get-started-workflows.md) oder im **[!UICONTROL Audiences]** Audiences-Menü mithilfe einer Abfrage erstellen.

Gehen Sie zur Erstellung einer Audience vom Typ **Liste** wie folgt vor:

1. Wählen Sie im Tab **Marketingaktivitäten** die Option **Erstellen** und dann **Workflow**.

   ![](assets/audiences_list_1.png)

1. Platzieren und konfigurieren Sie Zielgruppenbestimmungsaktivitäten im Workflow-Arbeitsbereich, um eine Population auszuwählen, deren Dimension **bekannt** ist. Die Liste der verfügbaren Aktivitäten und die entsprechenden Konfigurationen werden im Abschnitt [Über Zielgruppenbestimmungsaktivitäten](../../automating/using/about-targeting-activities.md) erläutert.

   You can use a **[!UICONTROL Query]** activity, or import data using a **[!UICONTROL Load file]** activity before using a **[!UICONTROL Reconciliation]** activity to identify the dimension of the data imported. Here, we want to target recipients who subscribed to the Sport Newsletter with a **[!UICONTROL Query]** activity .

   ![](assets/audiences_list_2.png)

1. After your targeting, drag and drop a **[!UICONTROL Save audience]** activity into your workflow. For example, you can chose to **[!UICONTROL Create or update an audience]**, this allows you to create then automatically update your audience with new data. In this case, add a **[!UICONTROL Scheduler]** activity at the beginning of your workflow.

   Weiterführende Informationen zur Konfiguration und Verwendung dieser Aktivität finden Sie im Abschnitt [Audience-Speicherung](../../automating/using/save-audience.md).

   ![](assets/audiences_list_3.png)

1. Speichern und starten Sie den Workflow.

   As the **[!UICONTROL Save audience]** is placed after a targeting with a known dimension, the audiences created via this activity are **List** audiences.

   Der Inhalt der gespeicherten Audience kann anschließend in der Detailansicht der Audience eingesehen werden. Auf letztere können Sie in der Liste der Audiences zugreifen. Die in dieser Ansicht gezeigten Spalten entsprechen den Spalten der in die Speicherungsaktivität des Workflows eingehenden Transition. Dies sind beispielsweise die Spalten der importierten Datei, über eine Abfrage hinzugefügte Zusatzdaten etc.

   ![](assets/audiences_list_4.png)

## Audiences vom Typ Datei erstellen {#creating-file-audiences}

In diesem Abschnitt wird die Erstellung einer Audience vom Typ **Datei** mithilfe eines Dateiimports in einem Workflow beschrieben.  lassen sich des Weiteren im Anschluss an eine Zielgruppenbestimmung in einem [Workflow](../../automating/using/get-started-workflows.md) oder im **[!UICONTROL Audiences]** Audiences-Menü mithilfe einer Abfrage erstellen.

Gehen Sie zur Erstellung einer Audience vom Typ **Datei** wie folgt vor:

1. Wählen Sie im Tab **Marketingaktivitäten** die Option **Erstellen** und dann **Workflow**.
1. Drag and drop, and then configure a **[!UICONTROL Load file]** activity which will allow you to import a population that has an **unknown** dimension when the workflow is executed. Weiterführende Informationen zur Konfiguration und Verwendung dieser Aktivität finden Sie im Abschnitt [Datei laden](../../automating/using/load-file.md).

   ![](assets/audience_files_1.png)

1. Ziehen Sie eine **[!UICONTROL Save audience]** Aktivität nach der **[!UICONTROL Load file]** Aktivität per Drag &amp; Drop. Weiterführende Informationen zur Konfiguration und Verwendung dieser Aktivität finden Sie im Abschnitt [Audience-Speicherung](../../automating/using/save-audience.md).
1. Speichern und starten Sie den Workflow.

   ![](assets/audience_files_2.png)

   As the **[!UICONTROL Save audience]** is placed after an import, the data dimension is unknown and the audiences created via this activity are **File** audiences.

   Der Inhalt der gespeicherten Audience kann anschließend in der Detailansicht der Audience eingesehen werden. Auf letztere können Sie in der Liste der Audiences zugreifen. Die in dieser Ansicht gezeigten Spalten entsprechen den Spalten der in die Speicherungsaktivität des Workflows eingehenden Transition. Dies sind beispielsweise die Spalten der importierten Datei, über eine Abfrage hinzugefügte Zusatzdaten etc.

   ![](assets/audience_files_3.png)

## Erstellen von Experience Cloud-Audiences {#creating-experience-cloud-audiences}

Adobe Campaign ermöglicht die gemeinsame Nutzung von Audiences mit Adobe Experience Cloud. An **Experience Cloud** type audience is directly imported from People core service to Adobe Campaign with the **[!UICONTROL Import shared audience]** technical workflow.

Im Gegensatz zur Audience vom Typ **Abfrage**, mit der Profile in Adobe Campaign abgefragt werden, besteht die Audience vom Typ **Experience Cloud** aus einer Liste mit Besucherkennungen.

Damit diese Integration funktioniert, muss sie zuerst konfiguriert werden. Weiterführende Informationen zur Konfiguration und zum Import oder Export von Audiences mit People Core Service finden Sie im folgenden [Abschnitt](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md).

![](assets/audience_peoplecore.png)

## Audiences ändern {#editing-audiences}

Die Vorgehensweise zur Änderung von Audiences hängt vom jeweiligen Typ ab:

* Greifen Sie zur Änderung einer Audience vom Typ **Abfrage** über das **[!UICONTROL Audiences]**-Menü oder die **[!UICONTROL Audiences]**-Karte auf der Adobe-Campaign-Startseite auf die Liste der Audiences zu.

   Öffnen Sie die gewünschte Audience. Alle Elemente einer bereits konfigurierten Audience können geändert werden.

   >[!CAUTION]
   >
   >If you change the **[!UICONTROL Filtering dimension]** in the query, the rules that have previously been defined will be lost.

* To edit a **List** or **File** audience, edit the workflow from which it was created and modify the **[!UICONTROL Save audience]** activity. Starten Sie den Workflow, damit die Änderungen für die Audience übernommen werden.
* Weiterführende Informationen dazu, wie Sie Audiences vom Typ **Experience Cloud** bearbeiten, finden Sie im Abschnitt [Importieren/Exportieren von Audiences mit People Core Service](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md).

## Audiences löschen {#deleting-audiences}

Es gibt zwei Möglichkeiten, um eine oder mehrere Audiences zu löschen. Die erste Möglichkeit besteht darin, zu Ihrer Audience ein Ablaufdatum hinzuzufügen.

Gehen Sie dabei folgendermaßen vor:

1. Öffnen Sie eine Audience.
1. Wählen Sie die Schaltfläche ![](assets/edit_darkgrey-24px.png) aus, um auf die Konfiguration der Audience zuzugreifen.

   ![](assets/audience_delete_2.png)

1. In the **[!UICONTROL Expires on]** field, add an expiration date to your audience.

   ![](assets/audience_delete_3.png)

1. Klicken Sie **[!UICONTROL Confirm]** dann auf **[!UICONTROL Save]**.

Ihr Ablaufdatum ist jetzt konfiguriert. Sobald dieses Datum erreicht ist, wird die Audience automatisch gelöscht.

Or if you need to delete an audience, you can simply select one or several audiences then click the **[!UICONTROL Delete element]** button.

![](assets/audience_delete_1.png)


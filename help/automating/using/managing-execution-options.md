---
solution: Campaign Standard
product: campaign
title: Ausführungsoptionen verwalten
description: Erfahren Sie, wie Sie Ausführungsoptionen von Workflows verwalten.
audience: automating
content-type: reference
topic-tags: workflow-general-operation
context-tags: workflow,overview;workflow,main
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 100%

---


# Ausführungsoptionen verwalten {#managing-execution-options}

Sie haben die Möglichkeit, die globalen Ausführungsoptionen eines Workflows anzupassen. Verwenden Sie hierzu die Schaltfläche ![](assets/edit_darkgrey-24px.png), um auf die Eigenschaften des Workflows zuzugreifen, und öffnen Sie den Bereich **[!UICONTROL Ausführung]**.

![](assets/wkf_execution_6.png)

Mögliche Optionen sind:

* **[!UICONTROL Standard-Affinität]**: Hier können Sie für die Ausführung eines Workflows oder einer Workflow-Aktivität die Verwendung einer bestimmten Engine vorschreiben.

* **[!UICONTROL Verlauf in Tagen]**: Gibt die Anzahl der Tage an, nach denen der Verlauf bereinigt werden muss. Der Verlauf enthält Elemente, die mit dem Workflow verbunden sind: Protokolle, Aufgaben, Ereignisse (technische Objekte, die mit dem Workflow-Ablauf verknüpft sind) sowie Dateien, die von der Aktivität **[!UICONTROL Dateiübertragung]** heruntergeladen wurden. Der Standardwert bei nativen Workflow-Vorlagen beträgt 30 Tage.

   Die Bereinigung des Verlaufs erfolgt durch den technischen Workflow für die Datenbankbereinigung, der standardmäßig täglich ausgeführt wird (siehe [Liste der technischen Workflows](../../administration/using/technical-workflows.md)).

   >[!IMPORTANT]
   >
   >Wenn das Feld **[!UICONTROL Verlauf in Tagen]** leer gelassen wird, wird sein Wert als „1“ betrachtet; der Verlauf wird also nach einem Tag bereinigt.

* **[!UICONTROL SQL-Abfragen im Protokoll speichern]**: Hier können Sie die SQL-Abfragen aus dem Workflow in den Protokollen speichern.

* **[!UICONTROL Zwischenergebnis festhalten]**: Aktivieren Sie diese Option, wenn Sie in der Lage sein möchten, die Detailansicht der Transitionen zu visualisieren.

   >[!CAUTION]
   >
   >Diese Option belegt viel Speicherplatz. Sie hilft Ihnen aber bei der Erstellung eines Workflows, dessen Konfiguration und Verhalten fehlerfrei sind. Aktivieren Sie sie nicht bei Produktionsinstanzen.

* **[!UICONTROL In der Engine ausführen (nicht im Produktionsmodus benutzen)]**: Ermöglicht Ihnen, den Workflow lokal auszuführen, um die Entwicklungsumgebung zu testen.

* **[!UICONTROL Prioritätsstufe]**: Hier haben Sie die Möglichkeit, die Workflow-Ausführung in Ihrer Adobe Campaign-Instanz als eher vorrangig oder eher nachrangig zu kennzeichnen. Dieses Feld wird von Adobe-Teams nur zu Überwachungszwecken verwendet.

Der Abschnitt **[!UICONTROL Umgang mit Fehlern]** enthält zusätzliche Optionen, mit denen Sie verwalten können, wie sich Workflows bei Fehlern verhalten. Diese Optionen werden im Abschnitt [Umgang mit Fehlern](../../automating/using/monitoring-workflow-execution.md#error-management) genauer beschrieben.

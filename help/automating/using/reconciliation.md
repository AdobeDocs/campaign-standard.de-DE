---
title: Abstimmung
description: Mithilfe der Abstimmungsaktivität lässt sich eine Verbindung zwischen nicht-identifizierten Daten und bereits existierenden Ressourcen herstellen.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: reconciliation,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: ed2e3793-6164-48af-9043-42dc43fa8ed4
source-git-commit: c2c8d2d05bbc376e2153448ca0a9e6ba0f367420
workflow-type: ht
source-wordcount: '584'
ht-degree: 100%

---

# Abstimmung{#reconciliation}

## Beschreibung {#description}

![](assets/reconciliation.png)

Mithilfe der Aktivität **[!UICONTROL Abstimmung]** lässt sich eine Verbindung zwischen nicht-identifizierten Daten und bereits existierenden Ressourcen herstellen.

## Anwendungskontext {#context-of-use}

Die Aktivität **[!UICONTROL Abstimmung]** dient hauptsächlich der Datenverwaltung und wird in zwei unterschiedlichen Anwendungsfällen verwendet:

* Hinzufügung von Relationen: Mithilfe des **[!UICONTROL Relationen]**-Tabs lassen sich Beziehungen zwischen eingehenden Daten und mehreren Dimensionen der Adobe-Campaign-Datenbank hinzufügen.

   Beispielsweise kann eine Datei neben Verkaufsdaten Informationen enthalten, die der Identifizierung der verkauften Produkte sowie des Kunden dienen. Die Daten der Datei betreffen also (zusätzlich zum **Verkauf**) zwei weitere Dimensionen: die Dimensionen **Produkte** und **Profile**. Folglich müssen Relationen zwischen letzteren beiden und der **Verkauf**-Dimension hergestellt werden (siehe hierzu nachstehendes Beispiel).

   Bei der Definition einer Relation werden die eingehenden Daten um eine Spalte zur Referenzierung des Fremdschlüssels der verknüpften Dimension erweitert.

   >[!NOTE]
   >
   >Dieser Vorgang setzt voraus, dass die Daten der verknüpften Dimensionen bereits in der Datenbank vorhanden sind. Wenn Sie beispielsweise eine Verkaufsaktivitäten enthaltende Datei importieren möchten, in der verzeichnet ist, welches Produkt wann von welchem Kunden gekauft wurde, müssen sowohl das Produkt als auch der Kunde bereits in der Datenbank angelegt sein. Identifizierung der Daten:

* Mithilfe des Tabs **[!UICONTROL Identifizierung]** lassen sich eingehende Daten den Spalten einer bereits in der Adobe-Campaign-Datenbank existierenden Dimension zuordnen. Die aus der Aktivität ausgehenden Daten werden so als der bestimmten Dimension zugehörig identifiziert.

   Im Anschluss können Sie zum Beispiel eine Audience speichern, die Datenbank aktualisieren etc.

Die Aktivität **[!UICONTROL Abstimmung]** kann beispielsweise auf eine Datenladeaktivität folgen, um nicht standardmäßige Daten in die Datenbank zu importieren.

Mit der Aktivität **Anreicherung** können Sie zusätzliche Daten definieren, die in Ihrem Workflow verarbeitet werden sollen. So können Sie mit der Aktivität **Anreicherung** Daten aus mehreren Datensätzen kombinieren oder Verknüpfungen zu einer temporären Ressource erstellen. Dagegen ermöglicht Ihnen die Aktivität **Abstimmung**, nicht identifizierte Daten mit bestehenden Ressourcen zu verknüpfen. Der Abstimmungsvorgang setzt voraus, dass die Daten der verknüpften Dimensionen bereits in der Datenbank vorhanden sind. Weitere Anwendungsbeispiele sind in [diesem Abschnitt](#use-cases-reconciliation) verfügbar.


## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Abstimmung]** in den Workflow-Arbeitsbereich und schließen Sie diese an eine Transition mit einer Population an, deren Zieldimension nicht direkt Adobe Campaign entstammt. Lesen Sie diesbezüglich auch den Abschnitt [Zielgruppendimensionen und Ressourcen](../../automating/using/query.md#targeting-dimensions-and-resources).
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der im Schnellzugriff angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Nutzen Sie zur Definition von Beziehungen zwischen eingehenden Daten und anderen Dimensionen der Datenbank den Tab **[!UICONTROL Relationen]**.

   Fügen Sie so viele Relationen wie nötig hinzu. Wählen Sie für jede Relation zunächst die verknüpfte Dimension aus, geben Sie anschließend in der Detailansicht der Relation die entsprechenden Felder an.

1. Gehen Sie zur bloßen Identifizierung der eingehenden Daten in den Tab **[!UICONTROL Identifizierung]** und aktivieren Sie die Option **[!UICONTROL Dokument zur Zielgruppenbestimmung aufgrund der Arbeitsdaten identifizieren]**.

   Wählen Sie die Zielgruppendimension aus, mit der Sie die eingehenden Daten abstimmen möchten.

   Fügen Sie Abstimmkriterien hinzu, mithilfe derer ein Datensatz der eingehenden Transition einem Datensatz der ausgewählten Zielgruppendimension zugeordnet werden kann. Bei mehreren Abstimmkriterien müssen alle erfüllt sein, damit eine Zuordnung der Daten möglich ist.

   Wählen Sie den **[!UICONTROL Umgang mit nicht-identifizierten Quellzeilen]** aus:

   * **[!UICONTROL Ignorieren]**: Nur die identifizierbaren Daten werden in der ausgehenden Transition beibehalten.
   * **[!UICONTROL In die Ausgabepopulation einschließen]**: Alle Daten der eingehenden Transition werden in der ausgehenden Transition beibehalten.

1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.


## Anwendungsfälle{#use-cases-reconciliation}

Erfahren Sie, wie Sie diese Aktivität in den folgenden Anwendungsfällen verwenden können:

* [Anwendungsfall: Datenabstimmung mithilfe von Relationen](../../automating/using/reconciliation-using-relations.md)
* [Anwendungsfall: Datenaktualisierung mittels Abstimmung](../../automating/using/data-update-reconciliation.md)
* [Anwendungsfall: Eine Audience vom Typ &quot;Datei&quot; mit der Datenbank abstimmen](../../automating/using/reconcile-file-audience-with-database.md)
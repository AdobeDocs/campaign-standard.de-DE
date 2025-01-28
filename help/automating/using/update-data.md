---
title: Daten-Update
description: Ein Daten-Update ermöglicht eine gebündelte Aktualisierung der Datenbankfelder.
audience: automating
content-type: reference
topic-tags: data-management-activities
context-tags: writer,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: d362563f-5ab3-4f7f-ae9f-a42b6f0bb2b9
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 100%

---

# Daten-Update{#update-data}

## Beschreibung {#description}

![](assets/data_update.png)

Ein **[!UICONTROL Daten-Update]** ermöglicht eine gebündelte Aktualisierung der Datenbankfelder.

## Anwendungskontext {#context-of-use}

Das **Daten-Update** wird insbesondere im Anschluss an einen Dateiimport verwendet, um die neuen Daten in die Adobe Campaign-Datenbank zu integrieren. Die Art der Datenbankaktualisierung kann über verschiedene Optionen definiert werden.

**Verwandte Themen:**

* [Anwendungsfall: Daten basierend auf einer Datei aktualisieren](../../automating/using/update-database-file.md)
* [Daten basierend auf einem automatischen Datei-Download aktualisieren](../../automating/using/update-data-automatic-download.md)

## Konfiguration {#configuration}

1. Ziehen Sie ein **[!UICONTROL Daten-Update]** in den Workflow-Arbeitsbereich.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in der Schnellaktion angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Geben Sie im Feld **[!UICONTROL Aktionstyp]** an, auf welche Weise die Daten aktualisiert werden sollen:

   * **[!UICONTROL Hinzufügen oder aktualisieren]** – fügt neue Daten zur Datenbank hinzu oder aktualisiert existierende Datensätze.
   * **[!UICONTROL Nur hinzufügen]** – fügt nur neue Daten hinzu, existierende Datensätze werden nicht verändert. Wenn Abstimmkriterien definiert wurden, werden nur nicht abgestimmte Datensätze hinzugefügt.

     Kreuzen Sie die Option **[!UICONTROL Ausgehende Transition für Zurückweisungen erzeugen]** an, wenn die importierten Daten bestimmte, bereits in der Datenbank vorhandene Datensätze enthalten, um Fehler zu vermeiden.

   * **[!UICONTROL Aktualisieren]** – aktualisiert Daten existierender Datensätze, fügt keine neuen Datensätze hinzu.
   * **[!UICONTROL Löschen]** – löscht in der Datenbank existierende Daten.

   >[!NOTE]
   >
   >Im Feld **[!UICONTROL Batch-Größe]** können Sie die maximale Batch-Größe für das Hochladen von Daten angeben.

1. Geben Sie im Tab **[!UICONTROL Identifizierung]** an, auf welche Weise die Datensätze der Datenbank erkannt werden können:

   * **[!UICONTROL Über Abstimmschlüssel]**. Wählen Sie die **[!UICONTROL Zu aktualisierende Dimension]** aus und definieren Sie die **[!UICONTROL Schlüssel, die das Auffinden der Datensätze ermöglichen]**. Lesen Sie diesbezüglich auch den Abschnitt [Zielgruppendimensionen und Ressourcen](../../automating/using/query.md#targeting-dimensions-and-resources).
   * Verwenden Sie die Option **[!UICONTROL Über eine oder mehrere Relationen]**, wenn die eingehenden Daten einer existierenden Zielgruppendimension entsprechen. Wählen Sie die **[!UICONTROL Zu aktualisierende Dimension aus]**.

   Wenn eine Aktualisierung durchgeführt werden soll, ist die Verwendung von Abstimmschlüsseln zwingend erforderlich.

1. Wählen Sie im entsprechenden Tab alle **[!UICONTROL zu aktualisierenden Felder]** aus und geben Sie bei Bedarf Bedingungen für die Aktualisierung an. Dies ist in der Spalte **[!UICONTROL Berücksichtigt wenn]** möglich. Die Bedingungen werden nacheinander, in Reihenfolge der Liste geprüft. Die Reihenfolge kann mithilfe der Pfeile rechts der Tabelle angepasst werden. Es ist möglich, mehrmals dasselbe Zielfeld zu verwenden.

   Mithilfe der Schaltfläche ![](assets/wkf_magic_wand-24px.png) können Sie die Felder automatisch zuordnen. Die Funktion erkennt Felder gleichen Namens.

   Wenn Sie die Option **[!UICONTROL Hinzufügen oder aktualisieren]** gewählt haben, können Sie in der Spalte **[!UICONTROL Aktion]** für jedes Feld individuell entscheiden, welche der möglichen Aktionen ausgeführt werden soll.

   >[!NOTE]
   >
   >**Bei der Verwaltung von Updates werden** die Felder **[!UICONTROL lastModified]**, **[!UICONTROL modifiedBy]**, **[!UICONTROL created]** und **[!UICONTROL createdBy]** im Zuge der Daten-Update-Aktivität automatisch aktualisiert, es sei denn, in der Tabelle der zu aktualisierenden Felder wird explizit etwas anderes konfiguriert. Nur Datensätze, die mindestens eine Änderung aufweisen, werden aktualisiert. Alle anderen bleiben unverändert.

1. Bei Bedarf können Sie unter Verwendung von [Transitionen](../../automating/using/activity-properties.md) auf erweiterte Optionen zur Ausgabepopulation zugreifen.

   Aktivieren Sie, um Fehler zu vermeiden, die Option **[!UICONTROL Ausgehende Transition für die Zurückweisungen erzeugen]**, wenn Sie **[!UICONTROL Nur hinzufügen]** ausgewählt haben und die importierten Daten möglicherweise bereits in der Datenbank vorhandene Datensätze enthalten.

1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

---
title: Daten aktualisieren
description: Ein Daten-Update ermöglicht eine gebündelte Aktualisierung der Datenbankfelder.
page-status-flag: never-activated
uuid: 1dc55db5-affd-4688-b673-adfb8c1338b5
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: 4db83c95-4b75-4a16-8dbf-bd8940431fa9
context-tags: writer,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 21faea89b3b38f3e667ed6c4de0be6d07f0b7197
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 100%

---


# Daten aktualisieren{#update-data}

## Beschreibung {#description}

![](assets/data_update.png)

Ein **[!UICONTROL Daten-Update]** ermöglicht eine gebündelte Aktualisierung der Datenbankfelder.

## Anwendungskontext {#context-of-use}

Das **Daten-Update** wird insbesondere im Anschluss an einen Dateiimport verwendet, um die neuen Daten in die Adobe-Campaign-Datenbank zu integrieren. Die Art der Datenbankaktualisierung kann über verschiedene Optionen definiert werden.

## Konfiguration {#configuration}

1. Ziehen Sie ein **[!UICONTROL Daten-Update]** in den Workflow-Arbeitsbereich.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der im Schnellzugriff angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Geben Sie im Feld **[!UICONTROL Aktionstyp]** an, auf welche Weise die Daten aktualisiert werden sollen:

   * **[!UICONTROL Hinzufügen oder aktualisieren]** - fügt neue Daten zur Datenbank hinzu oder aktualisiert existierende Datensätze.
   * **[!UICONTROL Nur hinzufügen]** - fügt nur neue Daten hinzu, existierende Datensätze werden nicht verändert. Wenn Abstimmkriterien definiert wurden, werden nur nicht abgestimmte Datensätze hinzugefügt.

      Kreuzen Sie die Option **[!UICONTROL Ausgehende Transition für Zurückweisungen erzeugen]** an, wenn die importierten Daten bestimmte, bereits in der Datenbank vorhandene Datensätze enthalten, um Fehler zu vermeiden.

   * **[!UICONTROL Aktualisieren]** - aktualisiert Daten existierender Datensätze, fügt keine neuen Datensätze hinzu.
   * **[!UICONTROL Löschen]** - löscht in der Datenbank existierende Daten.
   >[!NOTE]
   >
   >Im Feld **[!UICONTROL Batch-Größe]** können Sie die maximale Batch-Größe für das Hochladen von Daten angeben.

1. Geben Sie im Tab **[!UICONTROL Identifizierung]** an, auf welche Weise die Datensätze der Datenbank erkannt werden können:

   * **[!UICONTROL Über Abstimmschlüssel]**. Wählen Sie die **[!UICONTROL Zu aktualisierende Dimension]** aus und definieren Sie die **[!UICONTROL Schlüssel, die das Auffinden der Datensätze ermöglichen]**. Lesen Sie diesbezüglich auch den Abschnitt [Zielgruppendimensionen und Ressourcen](../../automating/using/query.md#targeting-dimensions-and-resources).
   * **[!UICONTROL Über die Zielgruppendimension]**, wenn die eingehenden Daten einer existierenden Zielgruppendimension entsprechen. Wählen Sie die **[!UICONTROL Zu aktualisierende Dimension aus]**.
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

## Beispiel {#example}

Unten stehende Abbildung zeigt die Konfiguration eines **[!UICONTROL Daten-Updates]** im Anschluss an eine **[!UICONTROL Datei laden]**-Aktivität. Ziel ist die Anreicherung der Adobe-Campaign-Datenbank mit neuen Profilen und gegebenenfalls die Aktualisierung existierender Profile mit den in der importierten Datei enthaltenen Daten. Als Abstimmschlüssel wird die E-Mail-Adresse verwendet.

Beim Format der geladenen Datei handelt es sich um **.txt**. Folgende Beispieldaten sind enthalten:

```
lastname;firstname;email;birthdate
jackman;megan;megan.jackman@testmail.com;07/08/1975
phillips;edward;phillips@testmail.com;09/03/1986
weaver;justin;justin_w@testmail.com;11/15/1990
martin;babeth;babeth_martin@testmail.net;11/25/1964
reese;richard;rreese@testmail.com;02/08/1987
cage;nathalie;cage.nathalie227@testmail.com;07/03/1989
xiuxiu;andrea;andrea.xiuxiu@testmail.com;09/12/1992
grimes;daryl;daryl_890@testmail.com;12/06/1979
tycoon;tyreese;tyreese_t@testmail.net;10/08/1971
```

Das **[!UICONTROL Daten-Update]** wurde wie folgt konfiguriert:

![](assets/deduplication_example2_writer1.png)

![](assets/deduplication_example2_writer2.png)


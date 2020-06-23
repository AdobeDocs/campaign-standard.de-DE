---
title: Best Practices beim Datenimport
description: Erfahren Sie mehr über die Best Practices, die beim Importieren von Daten in die Datenbank anzuwenden sind.
page-status-flag: never-activated
uuid: d909d26a-cf50-46af-ae09-f0fd7258ca27
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 75b83165-dcbd-4bb7-b703-ed769f489b16
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b4d0aa1a9f116f022890d5eccd87730a7a513103
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 97%

---


# Best Practices beim Datenimport {#import-best-practices}

Eine sorgfältige Arbeitsweise und die Befolgung der unten stehenden einfachen Regeln helfen Ihnen, die Datenbank konsistent zu halten und gängige Fehler bei der Datenbankaktualisierung oder beim Datenexport zu vermeiden.

## Importvorlagen verwenden    {#using-import-templates}

Import-Workflows sollten die folgenden Aktivitäten beinhalten: **[!UICONTROL Datei laden]**, **[!UICONTROL Abstimmung]**, **[!UICONTROL Segmentierung]**, **[!UICONTROL Deduplizierung]**, **[!UICONTROL Daten-Update]**.

Importvorlagen vereinfachen die Durchführung ähnlicher Importe und halten die Datenbank konsistent.

In vielen Projekten werden Importe ohne **[!UICONTROL Deduplizierung]** erstellt, da die im Projekt verwendeten Dateien ohnehin keine Duplikate aufweisen. Beim Import verschiedener Dateien können jedoch Duplikate entstehen. Dann ist eine Deduplizierung schwierig. Deshalb ist eine Deduplizierung eine gute Vorsichtsmaßnahme bei jedem Import-Workflow.

Verlassen Sie sich nicht darauf, dass die eingehenden Daten konsistent und korrekt sind oder dass sich die IT-Abteilung oder der Adobe-Campaign-Verantwortliche darum kümmert. Führen Sie stattdessen während des Projekts die Datenbereinigung durch. Achten Sie beim Datenimport auf die Deduplizierung, die Abstimmung und die Gewährleistung der Konsistenz.

Ein Beispiel für eine allgemeine Workflow-Vorlage zum Datenimport finden Sie in Abschnitt [Import-Workflow-Vorlage](../../automating/using/creating-import-workflow-templates.md).

>[!NOTE]
>
>Sie können auch [Importvorlagen](../../automating/using/importing-data-with-import-templates.md) verwenden. Dies sind von einem Administrator definierte Workflow-Vorlagen, die nach ihrer Aktivierung nur mehr die Möglichkeit bieten, die Datei zu spezifizieren, die die Importdaten enthält.

**Verwandte Themen:**

* [Aktivität „Datei laden“](../../automating/using/load-file.md)
* [Aktivität „Abstimmung“](../../automating/using/reconciliation.md)
* [Aktivität „Segmentierung“](../../automating/using/segmentation.md)
* [Aktivität „Deduplizierung“](../../automating/using/deduplication.md)
* [Aktivität „Daten-Update“](../../automating/using/update-data.md)

## Dateiformate mit einfach strukturierten Daten verwenden    {#using-flat-file-formats}

Das effizienteste Format für Importe sind flache Dateien, die im Bulk-Modus auf Datenbankebene importiert werden können.

Beispiel:

* Trennzeichen: Tabulator oder Semikolon
* Erste Zeile mit Headern
* Keine Zeichenketten-Qualifizierer
* Datumsformat: JJJJ/MM/TT hh:mm:ss

Beispiel einer zu importierenden Datei:

```
lastname;firstname;birthdate;email;crmID
Smith;Hayden;23/05/1989;hayden.smith@example.com;124365
Mars;Daniel;17/11/1987;dannymars@example.com;123545
Smith;Clara;08/02/1989;hayden.smith@example.com;124567
Durance;Allison;15/12/1978;allison.durance@example.com;120987
```

## Komprimierung verwenden    {#using-compression}

Verwenden Sie für Importe und Exporte möglichst ZIP-Dateien. GZIP wird standardmäßig unterstützt. Beim Import von Dateien können Sie über die Workflow-Aktivität **[!UICONTROL Datei laden]** eine Vorbearbeitung hinzufügen. Bei der Datenextraktion können Sie über die Workflow-Aktivität **[!UICONTROL Dateiextraktion]** eine Nachbearbeitung hinzufügen.

**Verwandte Themen:**

* [Aktivität „Datei laden“](../../automating/using/load-file.md)
* [Aktivität „Dateiextraktion“](../../automating/using/extract-file.md)

## Im Deltamodus importieren {#importing-in-delta-mode}

Regelmäßige Importe müssen im Deltamodus durchgeführt werden. Damit wird gewährleistet, dass nicht jedes Mal die gesamte Tabelle, sondern nur geänderte oder neue Daten an Adobe Campaign gesendet werden.

Vollständige Importe sollten nur für das erstmalige Laden verwendet werden.

## Konsistenz gewährleisten    {#maintaining-consistency}

Um die Konsistenz der Adobe-Campaign-Datenbank zu gewährleisten, befolgen Sie die unten stehenden Grundsätze:

* Wenn die importierten Daten einer Referenztabelle in Adobe Campaign entsprechen, sollten sie im Workflow mit dieser Tabelle abgeglichen werden. Nicht übereinstimmende Datensätze sollten abgelehnt werden.
* Achten Sie darauf, dass die importierten Daten (E-Mail, Telefonnummer, Postanschrift) stets **&quot;bereinigt&quot;** werden und dass diese Bereinigung zuverlässig ist und sich im Laufe der Jahre nicht verändert. Andernfalls könnten in der Datenbank Duplikate entstehen. Da Adobe Campaign keine Tools zum &quot;unscharfen&quot; Abgleich besitzt, ist es dann sehr schwierig, diese Duplikate zu verwalten und zu entfernen.
* Transaktionsdaten sollten einen Abstimmschlüssel aufweisen und mit den bestehenden Daten abgestimmt werden, damit keine Duplikate entstehen.
* **Importieren Sie verknüpfte Dateien in der richtigen Reihenfolge**. Wenn der Import aus mehreren miteinander verbundenen Dateien besteht, sollte im Workflow darauf geachtet werden, dass die Dateien in der richtigen Reihenfolge importiert werden. Wenn der Import einer Datei fehlschlägt, werden auch die anderen nicht importiert.
* Achten Sie beim Datenimport auf die **Deduplizierung**, die Abstimmung und die Gewährleistung der Konsistenz.

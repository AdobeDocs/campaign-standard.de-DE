---
title: Erste Schritte mit Prozessen und Data Management
description: Adobe Campaign verfügt über eine weitreichende grafische Umgebung, in der Prozesse konzipiert und automatisiert werden können.
page-status-flag: never-activated
uuid: 7c1e8cea-90d0-491f-ab8f-6cd69f8a6c3b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
discoiquuid: 40503917-7a53-4d99-96a4-57aa9e98ec87
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a9fbf0479019dfbe2964c517a0370f015d0f380a
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 29%

---


# Erste Schritte mit Prozessen und Data Management {#get-started-processes-data-management}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_workflows.svg" width="60px"><p><a href="#workflow-activities">Workflow-Aktivitäten</a></p></td><td><img src="assets/do-not-localize/icon_activities.svg" width="60px"><p><a href="../../automating/using/workflow-created-query-with-complement.md">Anwendungsbeispiele</a></p></td><td><img src="assets/do-not-localize/icon_filter.svg" width="60px"><p><a href="#filter-data">Daten filtern</a></p></td>
<td><img src="assets/do-not-localize/icon_manage.svg" width="60px"><p><a href="#import-export-data">Importieren/Exportieren von Daten</a></p></td></tr>
</table>

Adobe Campaign Angebots bietet eine umfassende grafische Umgebung, mit der Sie komplexe Prozesse wie Segmentierung, Ausführung von Kampagnen, Dateiverarbeitung usw. entwerfen können. Erstellen Sie zum Beispiel einen Workflow, um eine Datei von einem Server herunterzuladen, sie zu entkomprimieren und die Datensätze in die Adobe-Campaign-Datenbank zu importieren.

Oder fordern Sie andere Benutzer auf, Aufgaben auszuführen oder zu validieren. Auf diese Weise ist es möglich, anderen Benutzern Aufgaben wie Inhaltsgestaltung, Zielgruppenbestimmung und Validierung von Testsendungen zuzuweisen, bevor eine Nachricht an die Empfänger verschickt wird.

Workflows können in unterschiedlichsten Kontexten zum Einsatz kommen:

* Targeting zur Verwaltung von Audiencen oder zum Senden von Nachrichten.
* Daten-Management (ETL) zum Bearbeiten von Daten.
* Import von Daten in die Campaign-Datenbank.
* Technische Prozesse wie Datenbankbereinigung (Cleanup), Abruf von Trackinginformationen etc.

## Workflow-Aktivitäten {#workflow-activities}

<img src="assets/do-not-localize/icon_workflows.svg" width="60px">

Es stehen verschiedene Aktivitäten zur Verfügung, mit denen Sie Ihre Workflows entwerfen können.

[Mit Targeting-Aktivitäten](../../automating/using/about-targeting-activities.md) können Sie eine oder mehrere Zielgruppen erstellen, indem Sie Sätze definieren und diese Sätze mithilfe von Schnittpunkten, Vereinigungen oder Ausschlussvorgängen teilen oder kombinieren.

Koordinieren Sie mit [Execution-Aktivitäten](../../automating/using/about-execution-activities.md)Ihren Workflow und dessen Aktivitäten, während Sie mit den [Kanal-Aktivitäten](../../automating/using/about-channel-activities.md) Campaign Standard-Kommunikations-Kanal kombinieren können, um Kanal-übergreifende Workflows zu erstellen.

Schließlich können Sie mit [Data Management-Aktivitäten](../../automating/using/about-data-management-activities.md) Daten aus Ihrer Datenbank bearbeiten.

mehr dazu:

* [Workflow erstellen](../../automating/using/building-a-workflow.md)
* [Workflow ausführen](../../automating/using/about-workflow-execution.md)
* [Best Practices bei Workflows](../../automating/using/best-practices-workflows.md)

## Daten filtern {#filter-data}

<img src="assets/do-not-localize/icon_filter.svg" width="60px">

Verwenden Sie den **Abfrage-Editor** , um Daten aus Ihrer Datenbank zu filtern und eine Population zu erstellen, um Ihre Empfänger besser Zielgruppe. Der Abfrage-Editor ist verfügbar, um in Campaign Standard mehrere Aktionen auszuführen: Erstellen Sie Audiencen vom Typ Abfrage, definieren Sie Zielgruppen von Versänden oder Populationen in Workflow-Aktivitäten.

Der Abfragen-Editor enthält **Vordefinierte Filter und Regeln** für eine schnelle und einfache Filterung. Sie können jedoch auch **erweiterte Funktionen zur Bearbeitung** von Ausdrücken verwenden. Auf diese Weise können Sie Bedingungen manuell eingeben und Funktionen verwenden, um eigene Regeln zu bilden.

mehr dazu:

* [Abfrageeditor](../../automating/using/editing-queries.md)
* [Ausdrucksbearbeitung](../../automating/using/advanced-expression-editing.md)
* [Funktionsliste](../../automating/using/list-of-functions.md)

## Importieren/Exportieren von Daten {#import-export-data}

<img src="assets/do-not-localize/icon_manage.svg" width="60px">

Campaign Standard verfügt über mehrere **Data Management-Funktionen** zum Importieren und Exportieren von Daten.

[Workflows Data Management-Aktivitäten](../../automating/using/about-data-management-activities.md) ermöglichen es Ihnen, Daten zu importieren, Massenaktualisierungen in Feldern durchzuführen, Dateien zu empfangen oder zu senden oder nicht identifizierte Daten mit vorhandenen Ressourcen zu verknüpfen.

Mit [Importvorlagen](../../automating/using/importing-data-with-import-templates.md)können Sie bestimmte Importtypen verwalten, die von Administratoren definiert werden, indem Sie vereinfachte Importfunktionen verwenden.

[Mit dem Exportieren von Protokollen](../../automating/using/exporting-logs.md) können Sie Protokolldaten über einen einfachen Arbeitsablauf exportieren, sodass Sie die Ergebnisse Ihrer Marketing-Kampagnen in Ihren eigenen Berichte- oder BI-Tools analysieren können.

Nutzen Sie [Pakete](../../automating/using/managing-packages.md) zum Austausch von Ressourcen zwischen verschiedenen Instanzen der Kampagne, um beispielsweise die Konfiguration einer Instanz zu replizieren oder Daten von einem Server auf einen anderen zu übertragen, einschließlich benutzerspezifischer Ressourcen.

Schließlich können Sie mit [Exportieren von Listen](../../automating/using/exporting-lists.md) beliebige Listen aus Campaign Standards exportieren, z. B. die Liste von Test-Profilen, die Liste von Quarantänen-E-Mail-Adressen usw.

mehr dazu:

* [Datenimport und -export](../../automating/using/about-data-import-and-export.md)
* [Anwendungsbeispiel: Exportieren/Importieren benutzerdefinierter Ressourcen](../../automating/using/exporting-importing-custom-resources.md)

## Zusätzliche Ressourcen

* [Prozessvideos und Data Management-Lernvideos](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/getting-started/create-workflow.html)
* [Technische Workflows](../../administration/using/technical-workflows.md)
* [Erste Schritte mit dem Campaign Standard-Datenmodell](../../developing/using/get-started-data-model.md)

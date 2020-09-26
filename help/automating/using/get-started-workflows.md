---
title: Erste Schritte mit Prozessen und Daten-Management
description: Automatisieren Sie Prozesse mit Workflows, verwalten Sie Daten und Audiencen, senden Sie Nachrichten und vieles mehr.
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
source-git-commit: 5636b2ab5a673b0a52158b1a5411e090e4b45ca7
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 93%

---


# Erste Schritte mit Prozessen und Daten-Management {#get-started-processes-data-management}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_workflows.svg" width="60px"><p><a href="#workflow-activities">Workflow-Aktivitäten</a></p></td><td><img src="assets/do-not-localize/icon_activities.svg" width="60px"><p><a href="../../automating/using/workflow-created-query-with-complement.md">Anwendungsfälle</a></p></td><td><img src="assets/do-not-localize/icon_filter.svg" width="60px"><p><a href="#filter-data">Daten filtern</a></p></td>
<td><img src="assets/do-not-localize/icon_manage.svg" width="60px"><p><a href="#import-export-data">Daten importieren/exportieren</a></p></td></tr>
</table>

Adobe Campaign Angebots bietet eine umfassende grafische Umgebung, mit der Sie komplexe Prozesse wie Segmentierung, Ausführung von Kampagnen, Dateiverarbeitung usw. entwerfen können. Erstellen Sie zum Beispiel einen Workflow, um eine Datei von einem Server herunterzuladen, sie zu entkomprimieren und die Datensätze in die Adobe-Campaign-Datenbank zu importieren.

Oder fordern Sie andere Benutzer auf, Aufgaben auszuführen oder zu validieren. Auf diese Weise ist es möglich, anderen Benutzern Aufgaben wie Inhaltsgestaltung, Zielgruppenbestimmung und Validierung von Testsendungen zuzuweisen, bevor eine Nachricht an die Empfänger verschickt wird.

Workflows können in unterschiedlichsten Kontexten zum Einsatz kommen:

* Zielgruppenbestimmung für Audiences oder zum Versand von Nachrichten.
* Daten-Management (ETL) zum Bearbeiten von Daten.
* Import von Daten in die Campaign-Datenbank.
* Technische Prozesse wie Datenbankbereinigung (Cleanup), Abruf von Tracking-Informationen etc.

## Workflow-Aktivitäten {#workflow-activities}

<img src="assets/do-not-localize/icon_workflows.svg" width="60px">

Es stehen verschiedene Aktivitäten zur Verfügung, mit denen Sie Ihre Workflows entwerfen können.

[Zielgruppenbestimmungsaktivitäten](../../automating/using/about-targeting-activities.md) dienen der Definition einer oder mehrerer Zielpopulationen, welche im Anschluss durch die Aktivitäten &quot;Schnittmenge&quot;, &quot;Vereinigung&quot; und &quot;Ausschluss&quot; gesplittet oder zusammengefasst werden können.

Mit [Ausführungsaktivitäten](../../automating/using/about-execution-activities.md) koordinieren Sie Ihren Workflow und seine Aktivitäten, während Sie mit [Kanalaktivitäten](../../automating/using/about-channel-activities.md) die Kommunikationskanäle von Campaign Standard kombinieren können, um kanalübergreifende Workflows zu erstellen.

Schließlich können Sie mit [Daten-Management-Aktivitäten](../../automating/using/about-data-management-activities.md) die Daten aus Ihrer Datenbank bearbeiten.

Mehr dazu:

* [Workflow erstellen](../../automating/using/building-a-workflow.md)
* [Workflow ausführen](../../automating/using/about-workflow-execution.md)
* [Best Practices bei Workflows](../../automating/using/best-practices-workflows.md)

## Daten filtern {#filter-data}

<img src="assets/do-not-localize/icon_filter.svg" width="60px">

Verwenden Sie den **Abfrageeditor**, um Daten aus Ihrer Datenbank zu filtern und eine Population zu erstellen, um Ihre Empfänger besser zu erreichen. Der Abfrageeditor steht für verschiedene Aktionen in Campaign Standard zur Verfügung: Erstellen von Audiences für Abfragetypen, Definieren von Versandzielen oder Populationen in Workflow-Aktivitäten.

Der Abfrageneditor enthält **vordefinierte Filter und Regeln** für eine schnelle und einfache Filterung. Sie können jedoch auch die **erweiterte Ausdrucksbearbeitung** verwenden. Auf diese Weise können Sie Bedingungen manuell eingeben und Funktionen verwenden, um eigene Regeln zu bilden.

Mehr dazu:

* [Abfrageeditor](../../automating/using/editing-queries.md)
* [Ausdrucksbearbeitung](../../automating/using/advanced-expression-editing.md)
* [Funktionsliste](../../automating/using/list-of-functions.md)

## Daten importieren/exportieren {#import-export-data}

<img src="assets/do-not-localize/icon_manage.svg" width="60px">

Campaign Standard verfügt über verschiedene **Daten-Management-Funktionen** zum Importieren und Exportieren von Daten.

Die [Daten-Management-Aktivitäten](../../automating/using/about-data-management-activities.md) in Workflows ermöglichen es Ihnen, Daten zu importieren, gebündelte Updates von Feldern durchzuführen, Dateien zu empfangen oder zu senden oder nicht identifizierte Daten mit vorhandenen Ressourcen zu verknüpfen.

Mit [Importvorlagen](../../automating/using/importing-data-with-import-templates.md) können Sie bestimmte, von Administratoren definierte Importtypen durch vereinfachte Importfunktionen verwalten.

Durch das [Exportieren von Protokollen](../../automating/using/exporting-logs.md) können Sie Protokolldaten über einen einfachen Workflow exportieren und die Ergebnisse Ihrer Marketing-Kampagnen in Ihren eigenen Berichts- oder BI-Tools analysieren.

Nutzen Sie [Packages](../../automating/using/managing-packages.md)um Ressourcen zwischen verschiedenen Campaign-Instanzen auszutauschen, um beispielsweise die Konfiguration einer Instanz zu replizieren oder um Daten von einem Server auf einen anderen zu übertragen, einschließlich benutzerdefinierter Ressourcen.

Schließlich können Sie mit dem [Listenexport](../../automating/using/exporting-lists.md) beliebige Listen aus Campaign Standard exportieren, z. B. die Liste der Testprofile, die Liste der E-Mail-Adressen in Quarantäne usw.

Mehr dazu:

* [Datenimport und -export](../../automating/using/about-data-import-and-export.md)
* [Anwendungsfall: Exportieren/Importieren benutzerdefinierter Ressourcen](../../automating/using/exporting-importing-custom-resources.md)

## Zusätzliche Ressourcen

* [Video-Tutorials zu Prozessen und Daten-Management](https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/getting-started/create-workflow.html)
* [Technische Workflows](../../administration/using/technical-workflows.md)
* [Erste Schritte mit dem Campaign Standard-Datenmodell](../../developing/using/get-started-data-model.md)

---
title: Erste Schritte mit Prozessen und Daten-Management
description: Automatisieren Sie Prozesse mit Workflows, verwalten Sie Daten und Audiences, senden Sie Nachrichten und vieles mehr.
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
feature: Workflows
role: Data Architect
level: Beginner
exl-id: 26be942a-c252-458f-a590-eb235567ca67
source-git-commit: 31f62227736daf4f215fcbe1cf7b0a0a8574cda3
workflow-type: ht
source-wordcount: '506'
ht-degree: 100%

---

# Erste Schritte mit Prozessen und Daten-Management {#get-started-processes-data-management}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_workflows.svg" width="60px"><p><a href="#workflow-activities">Workflow-Aktivitäten</a></p></td><td><img src="assets/do-not-localize/icon_activities.svg" width="60px"><p><a href="../../automating/using/workflow-created-query-with-complement.md">Anwendungsfälle</a></p></td><td><img src="assets/do-not-localize/icon_filter.svg" width="60px"><p><a href="#filter-data">Daten filtern</a></p></td>
<td><img src="assets/do-not-localize/icon_manage.svg" width="60px"><p><a href="#import-export-data">Daten importieren/exportieren</a></p></td></tr>
</table>

Adobe Campaign bietet eine umfassende grafische Oberfläche, die den Entwurf komplexer Arbeitsabläufe ermöglicht. Diese umfassen die Segmentierung von Zielgruppen, die Ausführung von Kampagnen, die Verarbeitung von Dateien usw. Erstellen Sie zum Beispiel einen Workflow, um eine Datei von einem Server herunterzuladen, sie zu entkomprimieren und die Datensätze in die Adobe Campaign-Datenbank zu importieren.

Workflows können in unterschiedlichsten Kontexten zum Einsatz kommen:

* Zielgruppenbestimmung für Audiences oder zum Versand von Nachrichten.
* Daten-Management (ETL) zum Bearbeiten von Daten.
* Import von Daten in die Campaign-Datenbank.
* Technische Prozesse wie Datenbankbereinigung (Cleanup), Abruf von Tracking-Informationen etc.

>[!IMPORTANT]
>
> Adobe empfiehlt Kunden, nicht mehr als 20 aktive Workflows gleichzeitig auszuführen und die Ausführung von Workflows zu priorisieren sowie über die Zeit zu verteilen. Weitere Informationen hierzu finden Sie in den Best Practices auf [dieser Seite](../../automating/using/best-practices-workflows.md).

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

Nutzen Sie [Packages](../../automating/using/managing-packages.md), um Ressourcen zwischen verschiedenen Campaign-Instanzen auszutauschen, um beispielsweise die Konfiguration einer Instanz zu replizieren oder um Daten, einschließlich benutzerdefinierter Ressourcen, von einem Server auf einen anderen zu übertragen.

Schließlich können Sie mit dem [Listenexport](../../automating/using/exporting-lists.md) beliebige Listen aus Campaign Standard exportieren, z. B. die Liste der Testprofile, die Liste der E-Mail-Adressen in Quarantäne usw.

Mehr dazu:

* [Datenimport und -export](../../automating/using/about-data-import-and-export.md)
* [Anwendungsfall: Exportieren/Importieren benutzerdefinierter Ressourcen](../../automating/using/exporting-importing-custom-resources.md)

## Zusätzliche Ressourcen

* [Video-Tutorials zu Prozessen und Daten-Management](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/managing-processes-and-data/creating-a-workflow.html?lang=de)
* [Technische Workflows](../../administration/using/technical-workflows.md)
* [Erste Schritte mit dem Campaign Standard-Datenmodell](../../developing/using/get-started-data-model.md)

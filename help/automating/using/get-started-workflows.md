---
title: Erste Schritte mit Prozessen und Daten-Management
description: Automatisieren Sie Prozesse mit Workflows, verwalten Sie Daten und Zielgruppen, senden Sie Nachrichten und vieles mehr.
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
feature: Workflows
old-role: Data Architect
role: Developer
level: Beginner
exl-id: 26be942a-c252-458f-a590-eb235567ca67
TQID: https://experienceleague.adobe.com/iTJyQV-76oRhjJ4vDLKfSMpYTA27UcYt9UmVW-9YVq4
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: a075b2c1-7748-4328-b7f6-343aa314616aid: a4671286-a59f-47e3-b97b-90627a1977d5id: a658c786-869b-4194-a780-2594d663adda
subfeature_v2: id: b5f0aaf4-1e48-400d-95ac-6eb3078cf22fid: f5293531-9312-4099-bfa3-9e67df6a8750id: fcb46c0f-76e1-48bc-9dd0-fcf9d97526cf
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 520
ht-degree: 89%

---

# Erste Schritte mit Prozessen und Daten-Management {#get-started-processes-data-management}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_workflows.svg" width="60px"><p><a href="#workflow-activities">Workflow-Aktivitäten</a></p></td><td><img src="assets/do-not-localize/icon_activities.svg" width="60px"><p><a href="../../automating/using/workflow-created-query-with-complement.md">Anwendungsfälle</a></p></td><td><img src="assets/do-not-localize/icon_filter.svg" width="60px"><p><a href="#filter-data">Daten filtern</a></p></td>
<td><img src="assets/do-not-localize/icon_manage.svg" width="60px"><p><a href="#import-export-data">Daten importieren/exportieren</a></p></td></tr>
</table>

Adobe Campaign bietet eine umfassende grafische Umgebung, mit der Sie komplexe Prozesse wie Segmentierung, Kampagnenausführung, Dateiverarbeitung usw. entwerfen können. Beispielsweise können Sie einen Workflow verwenden, um eine Datei von einem Server herunterzuladen, sie zu entkomprimieren und dann ihre Datensätze in die Adobe Campaign-Datenbank zu importieren.

Workflows können in unterschiedlichsten Kontexten zum Einsatz kommen:

* Zielgruppenbestimmung für Audiences oder zum Versand von Nachrichten.
* Daten-Management (ETL) zum Bearbeiten von Daten.
* Import von Daten in die Campaign-Datenbank.
* Technische Prozesse wie Datenbankbereinigung (Cleanup), Abruf von Tracking-Informationen etc.

>[!IMPORTANT]
>
> Adobe empfiehlt Kunden, nicht mehr als 20 aktive Workflows gleichzeitig auszuführen und die Ausführung von Workflows zu priorisieren sowie über die Zeit zu verteilen. Weitere Informationen hierzu finden Sie in den Best Practices auf [dieser Seite](../../automating/using/best-practices-workflows.md).

## Workflow-Aktivitäten {#workflow-activities}

Es stehen verschiedene Aktivitäten zur Verfügung, mit denen Sie Ihre Workflows entwerfen können.

[Zielgruppenbestimmungsaktivitäten](../../automating/using/about-targeting-activities.md) dienen der Definition einer oder mehrerer Zielpopulationen, welche im Anschluss durch die Aktivitäten &quot;Schnittmenge&quot;, &quot;Vereinigung&quot; und &quot;Ausschluss&quot; gesplittet oder zusammengefasst werden können.

Mit [Ausführungsaktivitäten](../../automating/using/about-execution-activities.md) koordinieren Sie Ihren Workflow und seine Aktivitäten, während Sie mit [Kanalaktivitäten](../../automating/using/about-channel-activities.md) die Kommunikationskanäle von Campaign Standard kombinieren können, um kanalübergreifende Workflows zu erstellen.

Schließlich können Sie mit [Daten-Management-Aktivitäten](../../automating/using/about-data-management-activities.md) die Daten aus Ihrer Datenbank bearbeiten.

mehr dazu:

* [Workflow erstellen](../../automating/using/building-a-workflow.md)
* [Workflow ausführen](../../automating/using/about-workflow-execution.md)
* [Best Practices bei Workflows](../../automating/using/best-practices-workflows.md)

## Filtern von Daten {#filter-data}

Verwenden Sie den **Abfrage-Editor**, um Daten aus Ihrer Datenbank zu filtern und eine Population zu erstellen, um Ihre Empfänger besser zu erreichen. Der Abfrage-Editor steht für verschiedene Aktionen in Campaign Standard zur Verfügung: Erstellen von Zielgruppen für Abfragetypen, Definieren von Versandzielen oder Populationen in Workflow-Aktivitäten.

Der Abfrage-Editor enthält **vordefinierte Filter und Regeln** für eine schnelle und einfache Filterung. Sie können jedoch auch die **erweiterte Ausdrucksbearbeitung** verwenden. Auf diese Weise können Sie Bedingungen manuell eingeben und Funktionen verwenden, um eigene Regeln zu bilden.

mehr dazu:

* [Abfrageeditor](../../automating/using/editing-queries.md)
* [Ausdrucksbearbeitung](../../automating/using/advanced-expression-editing.md)
* [Funktionsliste](../../automating/using/list-of-functions.md)

## Daten importieren/exportieren {#import-export-data}

Campaign Standard verfügt über verschiedene **Daten-Management-Funktionen** zum Importieren und Exportieren von Daten.

Die [Daten-Management-Aktivitäten](../../automating/using/about-data-management-activities.md) in Workflows ermöglichen es Ihnen, Daten zu importieren, gebündelte Updates von Feldern durchzuführen, Dateien zu empfangen oder zu senden oder nicht identifizierte Daten mit vorhandenen Ressourcen zu verknüpfen.

Mit [Importvorlagen](../../automating/using/importing-data-with-import-templates.md) können Sie bestimmte, von Administratoren definierte Importtypen durch vereinfachte Importfunktionen verwalten.

Durch das [Exportieren von Protokollen](../../automating/using/exporting-logs.md) können Sie Protokolldaten über einen einfachen Workflow exportieren und die Ergebnisse Ihrer Marketing-Kampagnen in Ihren eigenen Berichts- oder BI-Tools analysieren.

Nutzen Sie [Packages](../../automating/using/managing-packages.md), um Ressourcen zwischen verschiedenen Campaign-Instanzen auszutauschen, um beispielsweise die Konfiguration einer Instanz zu replizieren oder um Daten, einschließlich benutzerdefinierter Ressourcen, von einem Server auf einen anderen zu übertragen.

Schließlich können Sie mit dem [Listenexport](../../automating/using/exporting-lists.md) beliebige Listen aus Campaign Standard exportieren, z. B. die Liste der Testprofile, die Liste der E-Mail-Adressen in Quarantäne usw.

mehr dazu:

* [Datenimport und -export](../../automating/using/about-data-import-and-export.md)
* [Anwendungsfall: Exportieren/Importieren benutzerdefinierter Ressourcen](../../automating/using/exporting-importing-custom-resources.md)

## Zusätzliche Ressourcen

* [Anleitungsvideos zu Prozessen und Daten-Management](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/managing-processes-and-data/creating-a-workflow.html?lang=de)
* [Technische Workflows](../../administration/using/technical-workflows.md)
* [Erste Schritte mit dem Campaign Standard-Datenmodell](../../developing/using/get-started-data-model.md)

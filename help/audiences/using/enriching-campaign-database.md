---
title: Datenbank anreichern
description: Hier erfahren Sie mehr über die verschiedenen Methoden zur Anreicherung der Datenbank.
audience: start
content-type: reference
topic-tags: about-adobe-campaign
feature: Profiles
role: User
level: Intermediate
exl-id: 9c55a8b3-034e-4319-8a88-7b59e83fa458
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 100%

---

# Datenbank anreichern{#enriching-the-database}

Campaign Standard bietet verschiedene Tools zur Erweiterung Ihrer Marketing-Datenbank. Dieser Abschnitt beinhaltet Erläuterungen zu den verschiedenen Methoden zum Einfügen von Daten in Campaign sowie Hinweise zu den entsprechenden Dokumentationen.

## Importieren von Daten mit Workflows {#importing-data-through-workflows}

Mit Workflows können Sie Daten erfassen und mithilfe von [[!UICONTROL Datenverwaltungsaktivitäten]](../../automating/using/about-data-management-activities.md) in die Campaign-Datenbank importieren.

Allgemeine Informationen und Best Practices zum Importieren von Daten über Workflows werden in [diesem Abschnitt](../../automating/using/about-data-import-and-export.md) erläutert.

Darüber hinaus können Sie Vorlagen für den Datenimport einrichten. Die Verwendung von Importvorlagen ist eine Best Practice, wenn Sie regelmäßig Dateien mit derselben Struktur importieren müssen.

Sie können zwei Arten von Vorlagen einrichten:

* **Workflow-Vorlagen**: Hierbei handelt es sich um vorkonfigurierte Workflows, die Sie einmal entsprechend Ihren Anforderungen einrichten und jedes Mal wiederverwenden können, wenn Sie Daten importieren und die Datenbank aktualisieren möchten.

  Ein Beispiel für eine Workflow-Vorlage zum Importieren von Daten finden Sie in [diesem Abschnitt](../../automating/using/creating-import-workflow-templates.md).

* **Vorlagen zum Datenimport**: Ebenso wie Workflow-Vorlagen sind auch dies Vorlagen, die auf Workflows basieren. Sie werden zum Hochladen von Dateien zur Aktualisierung der Datenbank eingerichtet. Nach der Konfiguration werden sie Benutzern mit einer vereinfachten Ansicht im Menü **[!UICONTROL Profile &amp; Audiences]** / **[!UICONTROL Importe]** zur Verfügung gestellt.

  Weiterführende Informationen zu Vorlagen zum Datenimport finden Sie im [entsprechenden Handbuch](../../automating/using/importing-data-with-import-templates.md).

## Erfassen von Daten über Landingpages {#collecting-data-from-landing-pages}

Landingpages sind Webformulare, die zur Datenerfassung und zur Erstellung oder Aktualisierung vorhandener Daten in Ihrer Datenbank verwendet werden können.

Das Prinzip dahinter sieht folgendermaßen aus:

* Erstellen und gestalten Sie eine Landingpage, indem Sie Eingabefelder hinzufügen, mit denen Daten erfasst werden können (Vorname, Nachname, E-Mail usw.).
* Mappen Sie jedes Eingabefeld mit dem entsprechenden Feld in der Datenbank.
* Stellen Sie die Landingpage online über eine Website oder über einen direkten Link in einer Nachricht zur Verfügung.

Weiterführende Informationen zu Landingpages finden Sie im [entsprechenden Handbuch](../../channels/using/getting-started-with-landing-pages.md).

## Synchronisieren von Profilen in Microsoft Dynamics 365

Die Campaign Standard-Integration mit Microsoft Dynamics 365 ermöglicht Ihnen die Übermittlung von Kontaktdaten von Microsoft Dynamics 365 an die Campaign-Datenbank.
Diese Kontakte sind dann in der Profilliste sichtbar und können für Marketing-Kampagnen verwendet werden.

Weiterführende Informationen zu dieser Integration finden Sie im [entsprechenden Handbuch](../../integrating/using/d365-acs-get-started.md).

>[!NOTE]
>
>Bitte beachten Sie, dass der Connector für Campaign Standard und Microsoft Dynamics 365 derzeit nur beschränkt verfügbar ist und einige Beschränkungen gelten. Diese werden in der Dokumentation beschrieben.

## Importieren von Daten über API-Aufrufe

Mit Campaign Standard-APIs können Sie Prozesse zum Aktualisieren der Datenbank durchführen, z. B. die Erstellung, Aktualisierung oder Löschung von Profilen oder Diensten.

Weiterführende Informationen zur Verwendung von APIs finden Sie im [entsprechenden Handbuch](../../api/using/get-started-apis.md).

>[!IMPORTANT]
>
>Bevor Sie Profile in großen Mengen erstellen oder die Aktualisierung über API-Aufrufe durchführen, überprüfen Sie in Ihrer Lizenzvereinbarung etwaige Volumensbeschränkungen. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://helpx.adobe.com/de/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers).

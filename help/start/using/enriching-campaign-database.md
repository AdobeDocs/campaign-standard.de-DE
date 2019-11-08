---
title: Datenbank anreichern
description: Hier erfahren Sie mehr über die verschiedenen Methoden zur Anreicherung der Datenbank.
page-status-flag: never-activated
uuid: 71f53808-0309-49f6-a4ee-3446eac9758a
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: about-adobe-campaign
discoiquuid: d8c8a318-9433-4aec-b378-fd0beb50e9fb
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Datenbank anreichern{#enriching-the-database}

Campaign Standard bietet verschiedene Tools zur Erweiterung Ihrer Marketing-Datenbank. In diesem Abschnitt werden die verschiedenen Methoden beschrieben, mit denen Sie Daten in Campaign injizieren können, mit Verweisen auf die dedizierten Dokumentation.

## Importieren von Daten mit Workflows {#importing-data-through-workflows}

Mit Workflows können Sie Daten erfassen und mithilfe von [**[!UICONTROL Datenverwaltungsaktivitäten]**](../../automating/using/about-data-management-activities.md) in die Campaign-Datenbank importieren.

Allgemeine Informationen und Best Practices zum Importieren von Daten über Workflows werden in [diesem Abschnitt](../../automating/using/importing-data.md) erläutert.

Darüber hinaus können Sie Vorlagen für den Datenimport einrichten. Die Verwendung von Importvorlagen ist eine Best Practice, wenn Sie regelmäßig Dateien mit derselben Struktur importieren müssen.

Sie können zwei Arten von Vorlagen einrichten:

* **Workflow-Vorlagen**: Hierbei handelt es sich um vorkonfigurierte Workflows, die Sie einmal entsprechend Ihren Anforderungen einrichten und jedes Mal wiederverwenden können, wenn Sie Daten importieren und die Datenbank aktualisieren möchten.

   Ein Beispiel für eine Workflow-Vorlage zum Importieren von Daten finden Sie in [diesem Abschnitt](../../automating/using/importing-data.md#example--import-workflow-template).

* **Vorlagen zum Datenimport**: Ebenso wie Workflow-Vorlagen sind auch dies Vorlagen, die auf Workflows basieren. Sie werden zum Hochladen von Dateien zur Aktualisierung der Datenbank eingerichtet. Nach der Konfiguration werden sie Benutzern mit einer vereinfachten Ansicht im Menü **[!UICONTROL Profile &amp; Audiences]** / Menü **[!UICONTROL Importe]** zur Verfügung gestellt.

   Weiterführende Informationen zu Vorlagen zum Datenimport finden Sie im [entsprechenden Handbuch](../../automating/using/importing-data-with-import-templates.md).

## Erfassen von Daten über Landingpages{#collecting-data-from-landing-pages}

Landingpages sind Webformulare, die zur Datenerfassung und zur Erstellung oder Aktualisierung vorhandener Daten in Ihrer Datenbank verwendet werden können.

Das Prinzip dahinter sieht folgendermaßen aus:

* Erstellen und gestalten Sie eine Landingpage, indem Sie Eingabefelder hinzufügen, mit denen Daten erfasst werden können (Vorname, Nachname, E-Mail usw.).
* Mappen Sie jedes Eingabefeld mit dem entsprechenden Feld in der Datenbank.
* Stellen Sie die Landingpage online über eine Website oder über einen direkten Link in einer Nachricht zur Verfügung.

Weiterführende Informationen zu Landingpages finden Sie im [entsprechenden Handbuch](../../channels/using/about-landing-pages.md).

## Synchronisieren von Profilen in Microsoft Dynamics 365

Die Campaign Standard-Integration mit Microsoft Dynamics 365 ermöglicht Ihnen die Übermittlung von Kontaktdaten von Microsoft Dynamics 365 an die Campaign-Datenbank.
Diese Kontakte sind dann in der Profilliste sichtbar und können für Marketingkampagnen verwendet werden.

Weiterführende Informationen zu dieser Integration finden Sie im [entsprechenden Handbuch](https://helpx.adobe.com/campaign/kb/acs-ms-dynamics.html).

>[!NOTE]
>
>Bitte beachten Sie, dass der Connector für Campaign Standard und Microsoft Dynamics 365 derzeit nur beschränkt verfügbar ist und einige Beschränkungen gelten. Diese werden in der Dokumentation beschrieben.

## Importieren von Daten über API-Aufrufe

Mit Campaign Standard-APIs können Sie Prozesse zum Aktualisieren der Datenbank durchführen, z. B. die Erstellung, Aktualisierung oder Löschung von Profilen oder Diensten.

Weiterführende Informationen zur Verwendung von APIs finden Sie im [entsprechenden Handbuch](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html).

>[!CAUTION]
>
>Bevor Sie Profile in großen Mengen erstellen oder die Aktualisierung über API-Aufrufe durchführen, überprüfen Sie in Ihrer Lizenzvereinbarung etwaige Volumensbeschränkungen. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers).

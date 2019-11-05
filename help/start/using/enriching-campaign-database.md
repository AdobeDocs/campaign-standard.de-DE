---
title: Datenbank anreichern
description: Erfahren Sie mehr über die verschiedenen Methoden zur Erweiterung der Datenbank.
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

Campaign Standard bietet verschiedene Tools zum Aufbau Ihrer Marketing-Datenbank. In diesem Abschnitt werden die verschiedenen Methoden beschrieben, mit denen Sie Daten in Campaign injizieren können, mit Verweisen auf die dedizierten Dokumentation.

## Importieren von Daten über Workflows {#importing-data-through-workflows}

Mit Workflows können Sie Daten erfassen und mithilfe von [**[!UICONTROL Datenverwaltungsaktivitäten]**](../../automating/using/about-data-management-activities.md) in die Kampagnendatenbank importieren.

Generische Informationen und Best Practices zum Importieren von Daten über Workflows werden in [diesem Abschnitt](../../automating/using/importing-data.md)erläutert.

Darüber hinaus können Sie Vorlagen für den Datenimport einrichten. Die Verwendung von Importvorlagen ist eine Best Practice, wenn Sie regelmäßig Dateien mit derselben Struktur importieren müssen.

Sie können zwei Arten von Vorlagen einrichten:

* **Workflow-Vorlagen**: Hierbei handelt es sich um vorkonfigurierte Workflows, die Sie je nach Bedarf einmal einrichten und jedes Mal wiederverwenden können, wenn Sie Daten importieren und die Datenbank aktualisieren möchten.

   Ein Beispiel für eine Workflow-Vorlage zum Importieren von Daten wird in [diesem Abschnitt](../../automating/using/importing-data.md#example--import-workflow-template)beschrieben.

* **Datenvorlagen** importieren: Wie Workflow-Vorlagen sind dies Vorlagen, die auf Workflows basieren und für das Hochladen von Dateien zum Aktualisieren der Datenbank eingerichtet sind. Nach der Konfiguration werden sie Benutzern mit einer vereinfachten Ansicht im Menü **[!UICONTROL Profile &amp; Zielgruppen]** / **[!UICONTROL Importe]** zur Verfügung gestellt.

   Weitere Informationen zu Importdatenvorlagen finden Sie in der [Dokumentation](../../automating/using/importing-data-with-import-templates.md).

## Erfassen von Daten von Einstiegsseiten {#collecting-data-from-landing-pages}

Einstiegsseiten sind Webformulare, die zur Datenerfassung und zur Erstellung oder Aktualisierung vorhandener Daten in Ihrer Datenbank verwendet werden können.

Der Grundsatz lautet:

* Erstellen und entwerfen Sie Ihre Einstiegsseite, indem Sie Eingabefelder zur Datenerfassung hinzufügen (Vorname, Nachname, E-Mail usw.).
* Ordnen Sie jedem Eingabefeld das entsprechende Feld aus der Datenbank zu.
* Machen Sie die Landingpage online über eine Website oder über einen direkten Link in eine Nachricht verfügbar.

For more on landing pages, refer to the [dedicated documentation](../../channels/using/about-landing-pages.md).

## Synchronisieren von Profilen aus Microsoft Dynamics 365

Die Campaign Standard Integration mit Microsoft Dynamics 365 ermöglicht Ihnen die Weitergabe von Kontaktdaten von Microsoft Dynamics 365 an die Kampagnendatenbank.
Diese Kontakte werden dann in der Liste "Profile"angezeigt und können in Marketingkampagnen zielgerichtet eingesetzt werden.

For more on this integration, refer to the [dedicated documentation](https://helpx.adobe.com/campaign/kb/acs-ms-dynamics.html).

>[!NOTE]
>
>Bitte beachten Sie, dass Campaign Standard-Microsoft Dynamics 365 Connector derzeit in beschränkter Verfügbarkeit verfügbar ist und dass es einigen Einschränkungen unterliegt, die in der Dokumentation beschrieben werden.

## Importieren von Daten über API-Aufrufe

Mit Campaign Standard-APIs können Sie Vorgänge zum Aktualisieren der Datenbank durchführen, z. B. die Erstellung, Aktualisierung oder Löschung von Profilen oder Diensten.

For more on how to use the APIs, refer to the [dedicated documentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html).

>[!CAUTION]
>
>Bevor Sie Profile Massenerstellung oder Aktualisierung über API-Aufrufe durchführen, überprüfen Sie bitte die Skalenbeschränkungen, die Ihrer Lizenzvereinbarung entsprechen. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers).

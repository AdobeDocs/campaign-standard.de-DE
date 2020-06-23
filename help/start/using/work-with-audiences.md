---
title: Listen anpassen
description: '"Hier erfahren Sie, wie Sie in Adobe Campaign Standard die Anzeige anpassen und bei Bildschirmen des Typs Liste vorgehen, um Elemente zu sortieren, zu filtern, zu löschen oder zu duplizieren. Bildschirme vom Typ Liste ermöglichen die Anzeige der Elemente einer oder mehrerer Ressourcen."'
page-status-flag: never-activated
uuid: 3350583c-91ca-4ea5-ac14-6b6f11c4a64a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: discovering-the-interface
discoiquuid: 4ba4f766-fdee-4ff0-8fe4-0612ed2b69a4
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: d4ac80810a77c0a6b512b3ed4c925fa0fb8a219c
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 96%

---


# Arbeiten mit Profilen und Audiencen

<table>
<tr>
    <td valign="top">
        <a href="../../start/using/work-with-audiences.md"><img width="60px" alt="Bedingungen" src="assets/icon_profile.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/creating-a-service.md"><img width="60px" alt="Bedingungen" src="assets/icon_profile.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/interacting-with-custom-resources.md"><img width="60px" alt="Bedingungen" src="assets/icon_profile.svg"/></a>
    </td>
    <td valign="top">
        <a href="../../api/using/interacting-with-marketing-history.md"><img width="60px" alt="Bedingungen" src="assets/icon_profile.svg"/></a>
    </td>
</tr>
<tr>
<td>Profile von Kunden</td>
<td>Datenbank erweitern</td>
<td>Audiencen organisieren</td>
<td>Datenschutzverwaltung</td>
</tr>
</table>

## Profile von Kunden {#customer-profiles}

<img width="60px" alt="Bedingungen" src="assets/icon_profile.svg"/>

Die Adobe-Campaign-Profile stellen die Gesamtheit an in der Datenbank gespeicherten Kontakten dar. Jedes Profil entspricht einem Datensatz in der Datenbank, welcher alle nötigen Informationen zu seiner Qualifizierung, Verwendung in Zielgruppen und zum Tracking enthält. Bei einem Profil kann es sich also - je nach in der Organisation verwendeten Bezeichnungen - um Kunden, Interessenten, Newsletter-Abonnenten, Empfänger, Benutzer etc. handeln.

**mehr dazu**

* [Über Profile](../../audiences/using/about-profiles.md)
* [Zugriff auf die Anzahl der aktiven Profil in Ihrem Unternehmen](../../audiences/using/active-profiles.md)

## Datenbank erweitern {#populating-database}

<img width="60px" alt="Bedingungen" src="assets/icon_populate.svg"/>

Campaign Standard bietet verschiedene Tools zur Erweiterung Ihrer Marketing-Datenbank. Dieser Abschnitt beinhaltet Erläuterungen zu den verschiedenen Methoden zum Einfügen von Daten in Campaign sowie Hinweise zu den entsprechenden Dokumentationen.

### Importieren von Daten mit Workflows {#importing-data-through-workflows}

Mit Workflows können Sie Daten erfassen und mithilfe von [**[!UICONTROL Datenverwaltungsaktivitäten]**](../../automating/using/about-data-management-activities.md) in die Campaign-Datenbank importieren. Allgemeine Informationen und Best Practices zum Importieren von Daten über Workflows werden in [diesem Abschnitt](../../automating/using/about-data-import-and-export.md) erläutert.

Darüber hinaus können Sie Vorlagen für den Datenimport einrichten. Die Verwendung von Importvorlagen ist eine Best Practice, wenn Sie regelmäßig Dateien mit derselben Struktur importieren müssen. Sie können zwei Arten von Vorlagen einrichten:

* **Workflow-Vorlagen**: Hierbei handelt es sich um vorkonfigurierte Workflows, die Sie einmal entsprechend Ihren Anforderungen einrichten und jedes Mal wiederverwenden können, wenn Sie Daten importieren und die Datenbank aktualisieren möchten. Ein Beispiel für eine Workflow-Vorlage zum Importieren von Daten finden Sie in [diesem Abschnitt](../../automating/using/creating-import-workflow-templates.md).

* **Vorlagen zum Datenimport**: Ebenso wie Workflow-Vorlagen sind auch dies Vorlagen, die auf Workflows basieren. Sie werden zum Hochladen von Dateien zur Aktualisierung der Datenbank eingerichtet. Nach der Konfiguration werden sie Benutzern mit einer vereinfachten Ansicht im Menü **[!UICONTROL Profile &amp; Audiences]** / **[!UICONTROL Importe]** zur Verfügung gestellt. Weiterführende Informationen zu Vorlagen zum Datenimport finden Sie im [entsprechenden Handbuch](../../automating/using/importing-data-with-import-templates.md).

### Erfassen von Daten über Landingpages{#collecting-data-from-landing-pages}

Landingpages sind Webformulare, die zur Datenerfassung und zur Erstellung oder Aktualisierung vorhandener Daten in Ihrer Datenbank verwendet werden können. Das Prinzip dahinter sieht folgendermaßen aus:

* Erstellen und gestalten Sie eine Landingpage, indem Sie Eingabefelder hinzufügen, mit denen Daten erfasst werden können (Vorname, Nachname, E-Mail usw.).
* Mappen Sie jedes Eingabefeld mit dem entsprechenden Feld in der Datenbank.
* Stellen Sie die Landingpage online über eine Website oder über einen direkten Link in einer Nachricht zur Verfügung.

Weiterführende Informationen zu Landingpages finden Sie im [entsprechenden Handbuch](../../channels/using/getting-started-with-landing-pages.md).

**mehr dazu**

* xxxx
* xxxx

### Synchronisieren von Profilen in Microsoft Dynamics 365

Die Campaign Standard-Integration mit Microsoft Dynamics 365 ermöglicht Ihnen die Übermittlung von Kontaktdaten von Microsoft Dynamics 365 an die Campaign-Datenbank.
Diese Kontakte sind dann in der Profilliste sichtbar und können für Marketingkampagnen verwendet werden. Weiterführende Informationen zu dieser Integration finden Sie im [entsprechenden Handbuch](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md).

>[!NOTE]
>
>Bitte beachten Sie, dass der Connector für Campaign Standard und Microsoft Dynamics 365 derzeit nur beschränkt verfügbar ist und einige Beschränkungen gelten. Diese werden in der Dokumentation beschrieben.

**mehr dazu**

* xxxx
* xxxx

### Importieren von Daten über API-Aufrufe

Mit Campaign Standard-APIs können Sie Prozesse zum Aktualisieren der Datenbank durchführen, z. B. die Erstellung, Aktualisierung oder Löschung von Profilen oder Diensten. Weiterführende Informationen zur Verwendung von APIs finden Sie im [entsprechenden Handbuch](../../api/using/get-started-apis.md).

>[!CAUTION]
>
>Bevor Sie Profile in großen Mengen erstellen oder die Aktualisierung über API-Aufrufe durchführen, überprüfen Sie in Ihrer Lizenzvereinbarung etwaige Volumensbeschränkungen. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://helpx.adobe.com/de/legal/product-descriptions/campaign-standard.html#ITInfrastructureResourcesbyActiveProfilesTiers).

**mehr dazu**

* xxxx
* xxxx

## Audiencen organisieren {#organizing-audiences}

<img width="60px" alt="Bedingungen" src="assets/icon_audience.svg"/>

Adobe Campaign vereint fortschrittliche Analyse- und Zielgruppenbestimmungsfunktionen, damit Sie relevante und effiziente Nachrichten versenden und mit Kunden effektiv interagieren können.

Workflows und das grafische Abfragetool erlauben die Erstellung von Audiences, die verfügbare Informationen, das Verhalten, die Sprache, die Einstellungen und den Marketingverlauf Ihrer Kontakte berücksichtigen, um Ihre unterschiedlichen Kampagnen perfekt auf die angesprochenen Zielgruppen zuzuschneiden. Sie können beispielsweise angemeldete Profile filtern oder auf einer unbegrenzten Anzahl von Kriterien basierende Zielgruppen erstellen.

**mehr dazu**

* [Über Audiences](../../audiences/using/about-audiences.md)
* [Audiences erstellen](../../audiences/using/creating-audiences.md)

## Datenschutzverwaltung {#privacy-management}

<img width="60px" alt="Bedingungen" src="assets/icon_privacy.svg"/>

Die DSGVO ist die neue Datenschutz-Grundverordnung der Europäischen Union (EU), in der die Anforderungen an den Datenschutz harmonisiert und neu geregelt werden. Die DSGVO gilt für Adobe-Campaign-Kunden, die Daten von Personen erfassen, die in der EU wohnhaft sind. Aus diesem Grund möchten wir als Datenverarbeiter Ihnen als Datenverantwortlichen zusätzlich zu den bereits in Adobe Campaign verfügbaren Datenschutzoptionen (Einverständnisverwaltung, Einstellungen für die Datenbeibehaltung und Benutzerrollen etc.) weitere Funktionen bereitstellen, mit deren Hilfe Sie DSGVO-konformes Verhalten sicherstellen können.

In diesem [Handbuch](https://docs.campaign.adobe.com/doc/standard/getting_started/de/ACS_GDPR.html) erfahren Sie mehr zu den Tools und Funktionen von Adobe Campaign, die Ihnen helfen, die DSGVO gesetzeskonform umzusetzen.

**mehr dazu**

* xxxx
* xxxx
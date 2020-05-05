---
title: Erste Schritte mit dem Campaign Standard-Datenmodell
description: Erweitern Sie das Datenmodell des Campaign Standards mit Ihren eigenen Feldern und Ressourcen und überwachen Sie alle Änderungen am Datenmodell in einer einzigen Ansicht.
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
source-git-commit: aeaddca2188e2bdeda71bd35299ccd14398f3c52

---


# Erste Schritte mit dem Campaign Standard-Datenmodell {#get-started-data-model}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_datamodel.svg" width="60px"><p><a href="#data-model">Datenmodell</a></p></td>
<td><img src="assets/do-not-localize/icon_custom.svg" width="60px"><p><a href="#custom-resources">Benutzerdefinierte Ressourcen</a></p></td><td><img src="assets/do-not-localize/icon_api.svg" width="60px"><p><a href="#custom-resources">Arbeiten mit APIs</a></p></td></tr>
</table>

Erweitern Sie das Datenmodell des Campaign Standards mit Ihren eigenen Feldern und Ressourcen und überwachen Sie alle Änderungen am Datenmodell in einer einzigen Ansicht.

## Datenmodell {#data-model}

<img src="assets/do-not-localize/icon_datamodel.svg" width="60px">

Die von der Kampagne verwendeten Daten werden durch verschiedene Ressourcen definiert, die in einem **vordefinierten Datenmodell** definiert sind. Das Datenmodell zeigt eine vordefinierte SQL-Struktur für eine Reihe von Marketingressourcen an: Versand, Audience, Landingpages, Profil usw. Jede Ressource wird mit zugehörigen Filtern geliefert, sodass Sie durch die Ressourcen navigieren können.

Das Menü **Diagnose** ermöglicht die Liste der technischen Objekte, die von Campaign Standard generiert werden: Schema, Webseiten, Filter usw., mit denen Sie das Datenmodell und alle daran vorgenommenen Änderungen überwachen können.

mehr dazu:

* [Datenmodellkonzepte](../../developing/using/data-model-concepts.md)
* [Best Practices für Datenmodelle](../../developing/using/data-model-best-practices.md)
* [Datenmodellbeschreibung](../../developing/using/datamodel-introduction.md)
* [Änderungen an Datenmodellen verfolgen](../../developing/using/monitoring-data-model-changes.md)

## Benutzerdefinierte Ressourcen {#custom-resources}

<img src="assets/do-not-localize/icon_custom.svg" width="60px">

Mit Campaign Standard können Sie das vordefinierte Datenmodell **** anreichern, um eigene Ressourcen zu erstellen (z. B. zum Hinzufügen von Kauf- oder Produkttabellen), oder vorhandene Ressourcen um neue Felder erweitern. Sie können auch Kampagnen-Bildschirme konfigurieren, um die Navigation durch die neu erstellten Ressourcen und Felder zu optimieren.

Darüber hinaus können Sie **Campaign Standard-REST-APIs** erweitern, um erweiterte Felder für die APIs für die Profil für benutzerdefinierte Ressourcen verfügbar zu machen. So können Sie beispielsweise das Profil eines Kunden mit einem Promo-Code aktualisieren, der aus einem Rechnungssystem generiert wurde.

mehr dazu:

* [Ressource hinzufügen oder erweitern](../../developing/using/key-steps-to-add-a-resource.md)
* [Die API erweitern](../../developing/using/about-extending-the-api.md)
* [Verwendungsfall: Erweitern der Profil-Ressource mit einem neuen Feld](../../developing/using/extending-the-profile-resource-with-a-new-field.md)
* [Verwendungsfall: Erweitern der Abonnement zu einer Anwendungsressource](../../developing/using/extending-the-subscriptions-to-an-application-resource.md)

## Arbeiten mit APIs {#apis}

<img src="assets/do-not-localize/icon_api.svg" width="60px">

Erstellen Sie mit Campaign Standard-APIs Integrationen für Adobe Campaign Standard und erstellen Sie ein eigenes Ökosystem, indem Sie die Kampagne mit dem von Ihnen verwendeten Technologiebereich verbinden. [Erste Schritte mit Campaign Standard-REST-APIs](../../api/using/about-campaign-standard-apis.md)

## Zusätzliche Ressourcen

* [Über Adobe Experience Platform Data Connector](../../developing/using/aep-about-data-connector.md)
* [Erstellen benutzerdefinierter Ressourcen (Video)](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/developing/custom-resources-develop/creating-custom-resources.html)
* [Exportieren/Importieren benutzerdefinierter Ressourcen](https://helpx.adobe.com/campaign/kb/acs-get-started-with-cusres.html)

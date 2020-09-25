---
title: Erste Schritte mit dem Campaign Standard-Datenmodell
description: Greifen Sie auf die Beschreibung des integrierten Datenmodells zu, erweitern Sie das Datenmodell des Campaign Standards mit benutzerdefinierten Feldern und Ressourcen und überwachen Sie alle Änderungen des Datenmodells in einer einzigen Ansicht.
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
source-git-commit: e67a173c5409d7693a3d7dab8f8ca3b03aeb886f
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 92%

---


# Erste Schritte mit dem Campaign Standard-Datenmodell {#get-started-data-model}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_datamodel.svg" width="60px"><p><a href="#data-model">Datenmodell</a></p></td>
<td><img src="assets/do-not-localize/icon_custom.svg" width="60px"><p><a href="#custom-resources">Benutzerdefinierte Ressourcen</a></p></td><td><img src="assets/do-not-localize/icon_api.svg" width="60px"><p><a href="#custom-resources">Mit APIs arbeiten</a></p></td></tr>
</table>

Erweitern Sie das Datenmodell von Campaign Standard mit Ihren eigenen Feldern und Ressourcen und überwachen Sie alle Änderungen daran in einer einzigen Ansicht.

## Datenmodell {#data-model}

<img src="assets/do-not-localize/icon_datamodel.svg" width="60px">

Die von Campaign verwendeten Daten werden durch verschiedene Ressourcen definiert, die in einem **vordefinierten Datenmodell** festgelegt werden. Das Datenmodell verfügt über eine native SQL-Struktur für eine Reihe von Marketing-Ressourcen: Versand, Audience, Landingpages, Profil usw. Jede Ressource wird mit zugehörigen Filtern geliefert, sodass Sie durch die Ressourcen navigieren können.

Im Menü **Diagnose** können Sie die von Campaign Standard generierten technischen Objekte auflisten: Datenschemata, Websites, Filter usw., um das Datenmodell und alle daran vorgenommenen Änderungen zu überwachen.

Mehr dazu:

* [Datenmodellkonzepte](../../developing/using/data-model-concepts.md)
* [Best Practices für Datenmodelle](../../developing/using/data-model-best-practices.md)
* [Beschreibung des Datenmodells](../../developing/using/datamodel-introduction.md)
* [Änderungen an Datenmodellen verfolgen](../../developing/using/monitoring-data-model-changes.md)

## Benutzerdefinierte Ressourcen {#custom-resources}

<img src="assets/do-not-localize/icon_custom.svg" width="60px">

Mit Campaign Standard können Sie das **vordefinierte Datenmodell anreichern**, um eigene Ressourcen zu erstellen (z. B., um Kauf- oder Produkttabellen hinzuzufügen) oder vorhandene Ressourcen um neue Felder zu erweitern. Sie können auch Campaign-Bildschirme konfigurieren, um die Navigation durch die neu erstellten Ressourcen und Felder zu optimieren.

Darüber hinaus können Sie die **Campaign Standard-REST-APIs erweitern**, um in den APIs erweiterte Felder für die benutzerdefinierten Ressourcenprofile anzuzeigen. Damit können Sie beispielsweise ein Kundenprofil mit einem durch ein Verrechnungssystem erzeugten Angebots-Code aktualisieren.

Mehr dazu:

* [Ressource hinzufügen oder erweitern](../../developing/using/key-steps-to-add-a-resource.md)
* [Die API erweitern](../../developing/using/about-extending-the-api.md)
* [Anwendungsfall: Profilressource um ein neues Feld erweitern](../../developing/using/extending-the-profile-resource-with-a-new-field.md)
* [Anwendungsfall: App-Abonnementsressource erweitern](../../developing/using/extending-the-subscriptions-to-an-application-resource.md)

## Mit APIs arbeiten {#apis}

<img src="assets/do-not-localize/icon_api.svg" width="60px">

Mit Campaign Standard-APIs können Sie Integrationen für Campaign erstellen und Ihr eigenes Ökosystem einrichten, indem Sie Adobe Campaign Standard mit den von Ihnen verwendeten Technologien verbinden. [Erste Schritte mit Campaign Standard-REST-APIs](../../api/using/get-started-apis.md)

## Zusätzliche Ressourcen

* [Über Adobe Experience Platform Data Connector](../../developing/using/aep-about-data-connector.md)
* [Benutzerdefinierte Ressourcen erstellen (Video)](https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/developing/custom-resources-develop/creating-custom-resources.html)
* [Exportieren/Importieren benutzerdefinierter Ressourcen](https://helpx.adobe.com/de/campaign/kb/acs-get-started-with-cusres.html)

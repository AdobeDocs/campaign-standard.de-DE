---
title: Erste Schritte mit dem Campaign Standard-Datenmodell
description: Reichern Sie das Datenmodell von Campaign Standard mit benutzerdefinierten Feldern und Ressourcen an und erweitern Sie REST-APIs, um erweiterte Felder sichtbar zu machen.
audience: automating
content-type: reference
topic-tags: about-workflows-and-data-management
feature: Data Model
role: Developer
level: Intermediate
exl-id: a8d15053-c20f-4334-a732-3b36cb00794d
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: ht
source-wordcount: '334'
ht-degree: 100%

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

Die von Campaign verwendeten Daten werden durch verschiedene Ressourcen definiert, die in einem **vordefinierten Datenmodell** festgelegt werden. Das Datenmodell verfügt über eine native SQL-Struktur für eine Reihe von Marketing-Ressourcen: Versand, Zielgruppe, Landingpages, Profil usw. Jede Ressource wird mit zugehörigen Filtern geliefert, sodass Sie durch die Ressourcen navigieren können.

Im Menü **Diagnose** können Sie die von Campaign Standard generierten technischen Objekte auflisten: Datenschemata, Websites, Filter usw., um das Datenmodell und alle daran vorgenommenen Änderungen zu überwachen.

mehr dazu:

* [Konzepte von Datenmodellen](../../developing/using/data-model-concepts.md)
* [Best Practices für Datenmodelle](../../developing/using/data-model-best-practices.md)
* [Beschreibung des Datenmodells](../../developing/using/datamodel-introduction.md)
* [Änderungen an Datenmodellen verfolgen](../../developing/using/monitoring-data-model-changes.md)

## Benutzerdefinierte Ressourcen {#custom-resources}

<img src="assets/do-not-localize/icon_custom.svg" width="60px">

Mit Campaign Standard können Sie das **vordefinierte Datenmodell anreichern**, um eigene Ressourcen zu erstellen (z. B., um Kauf- oder Produkttabellen hinzuzufügen) oder vorhandene Ressourcen um neue Felder zu erweitern. Sie können auch Campaign-Bildschirme konfigurieren, um die Navigation durch die neu erstellten Ressourcen und Felder zu optimieren.

Darüber hinaus können Sie die **Campaign Standard-REST-APIs erweitern**, um in den APIs erweiterte Felder für die benutzerdefinierten Ressourcenprofile anzuzeigen. Damit können Sie beispielsweise ein Kundenprofil mit einem durch ein Verrechnungssystem erzeugten Angebots-Code aktualisieren.

mehr dazu:

* [Ressource hinzufügen oder erweitern](../../developing/using/key-steps-to-add-a-resource.md)
* [Die API erweitern](../../developing/using/about-extending-the-api.md)
* [Anwendungsfall: Profilressource um ein neues Feld erweitern](../../developing/using/extending-the-profile-resource-with-a-new-field.md)
* [Anwendungsfall: App-Abonnementsressource erweitern](../../developing/using/extending-the-subscriptions-to-an-application-resource.md)

## Mit APIs arbeiten {#apis}

<img src="assets/do-not-localize/icon_api.svg" width="60px">

Mit Campaign Standard-APIs können Sie Integrationen für Campaign erstellen und Ihr eigenes Ökosystem einrichten, indem Sie Adobe Campaign Standard mit den von Ihnen verwendeten Technologien verbinden. [Erste Schritte mit Campaign Standard-REST-APIs](../../api/using/get-started-apis.md)

## Zusätzliche Ressourcen

* [Exportieren/Importieren benutzerdefinierter Ressourcen](https://helpx.adobe.com/de/campaign/kb/acs-get-started-with-cusres.html)
* [Daten von Campaign nach Adobe Experience Platform exportieren](../../integrating/using/export-campaign-data.md)

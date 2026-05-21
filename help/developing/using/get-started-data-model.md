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
TQID: https://experienceleague.adobe.com/LHlfIZ24iApQfr6dL-x-nQViltSetibBgt1slLDsRi4
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2:
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
  - id: d5ef99fa-df0c-4153-bf94-105ad0724167
subfeature_v2:
  - id: bf97c196-a4d1-4fa3-a151-e68a114c8ac0
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 348
ht-degree: 89%

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

Die von Campaign verwendeten Daten werden durch verschiedene Ressourcen definiert, die in einem **vordefinierten Datenmodell** festgelegt werden. Das Datenmodell zeigt eine vorkonfigurierte SQL-Struktur für eine Reihe von Marketing-bezogenen Ressourcen an: Versand, Zielgruppe, Landingpages, Profil usw. Jeder Ressource sind Filter zugeordnet, mit denen Sie durch die Ressourcen navigieren können.

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

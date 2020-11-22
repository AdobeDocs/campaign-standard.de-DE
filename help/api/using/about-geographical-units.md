---
solution: Campaign Standard
product: campaign
title: Über geografische Einheiten
description: Erfahren Sie mehr über geografische Einheiten und APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 100%

---


# Über geografische Einheiten {#about-geographical-units}

>[!CAUTION]
>
>Die Funktion &quot;Geografische Einheiten&quot; wird seit Version 18.7 von Campaign Standard nicht mehr unterstützt.
>
>Daher kann die Funktion ab Version 18.7 nicht mehr für neue Campaign Standard-Instanzen oder für vorhandene Instanzen ohne geografische Einheiten implementiert werden.
>
>Weiterführende Informationen dazu finden Sie auf der Seite <a href="https://helpx.adobe.com/de/campaign/kb/acs-deprecated-and-removed-features.html">Eingestellte Funktionen</a>.

Über den Endpunkt **geoUnitBase** können Sie mit geografischen Einheiten interagieren, um beispielsweise deren Attribute oder die Einheit eines Profils zu aktualisieren.

Das Feld **Geografische Einheiten** wird zu einem Profil hinzugefügt, wenn die Profilressource erweitert wird. Daher sollten Sie stets den Endpunkt **profileAndServicesExt** verwenden, um mit geografischen Einheiten zu interagieren. Weiterführende Informationen zur Ressourcenerweiterung des Profils finden Sie in der [Campaign-Dokumentation](https://helpx.adobe.com/de/campaign/standard/administration/using/organizational-units.html#partitioning-profiles).

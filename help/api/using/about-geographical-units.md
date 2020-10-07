---
title: Über geografische Einheiten
description: Erfahren Sie mehr über geografische Einheiten und APIs.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
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

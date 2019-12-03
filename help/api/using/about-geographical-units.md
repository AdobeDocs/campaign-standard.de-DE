---
title: Geografische Einheiten
description: Erfahren Sie mehr über geografische Einheiten und APIs.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: aee0e0437cbfe578cb2f715a2433099c79dd1748

---


# Geografische Einheiten {#about-geographical-units}

>[!CAUTION]
>
>Die Funktion "Geografische Einheit"wurde mit Version 18.7 von Campaign Standard nicht mehr unterstützt.
Daher kann diese Funktion nicht für neue Campaign Standard-Instanzen sowie für vorhandene Instanzen ohne geografische Einheiten ab Version 18.7 implementiert werden.
For more on this, refer to the <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">Deprecated features</a> page.

Mit dem **Endpunkt "geoUnitBase** "können Sie mit geografischen Einheiten interagieren, um beispielsweise deren Attribute zu aktualisieren oder die Einheit eines Profils zu aktualisieren.

Das Feld **Geografische Einheit** wird zu einem Profil hinzugefügt, wenn die Profilatressource erweitert wird. Daher sollten Sie immer den Endpunkt **profileAndServicesExt** verwenden, um mit geografischen Einheiten zu interagieren. Weitere Informationen zur Ressourcenerweiterung des Profils finden Sie in der [Kampagnendokumentation](https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles).

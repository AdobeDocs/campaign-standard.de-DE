---
title: Über geografische Einheiten
description: Erfahren Sie mehr über geografische Einheiten und APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: ht
source-wordcount: '127'
ht-degree: 100%

---


# Über geografische Einheiten {#about-geographical-units}

>[!CAUTION]
>
>Die Funktion &quot;Geografische Einheiten&quot; wird seit Version 18.7 von Campaign Standard nicht mehr unterstützt.
>
>Daher kann die Funktion ab Version 18.7 nicht mehr für neue Campaign Standard-Instanzen oder für vorhandene Instanzen ohne geografische Einheiten implementiert werden.
>
>Weiterführende Informationen dazu finden Sie auf der Seite <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/deprecated-features.html?lang=de">Eingestellte Funktionen</a>.

Über den Endpunkt **geoUnitBase** können Sie mit geografischen Einheiten interagieren, um beispielsweise deren Attribute oder die Einheit eines Profils zu aktualisieren.

Das Feld **Geografische Einheiten** wird zu einem Profil hinzugefügt, wenn die Profilressource erweitert wird. Daher sollten Sie stets den Endpunkt **profileAndServicesExt** verwenden, um mit geografischen Einheiten zu interagieren. Weiterführende Informationen zur Ressourcenerweiterung des Profils finden Sie in der [Campaign-Dokumentation](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/organizational-units.html?lang=de#organizational-units).

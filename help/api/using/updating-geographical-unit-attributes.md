---
title: Aktualisieren von Attributen geografischer Einheiten
description: Erfahren Sie, wie Sie Attribute geografischer Einheiten mit APIs aktualisieren
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


# Aktualisieren von Attributen geografischer Einheiten {#managing-geographical-units}

1. Führen Sie eine GET-Anforderung für die **Ressource geoUnitBase** durch, um die geografische Einheit PKey abzurufen.
1. Führen Sie eine PATCH-Anforderung an die geografische Einheit mit den Attributen durch, die in der Nutzlast aktualisiert werden sollen.

<br/>

***Musteranforderung***

Rufen Sie die Liste der geografischen Einheiten ab.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/geoUnitBase/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es werden alle geografischen Einheiten zurückgegeben. Rufen Sie den PKey der gewünschten Einheit ab.

```
{
 "PKey": "<PKEY>",
 "created": "2019-04-06 22:36:19.089Z",
 "desc": "",
 "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/geoUnitBase/<PKEY>",
 "label": "Europe",
 "lastModified": "2019-04-06 22:36:19.086Z",
 "name": "eu",
 "parentTitle": "All (all)",
 "title": "Europe (eu)"
},
```

Führen Sie eine PATCH-Anforderung an die geografische Einheit mit den Attributen durch, die in der Nutzlast aktualisiert werden sollen.

```
-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "label":"Asia",
-d "name":"asia"
-d }
```

<!-- + réponse -->

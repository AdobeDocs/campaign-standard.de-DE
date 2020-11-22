---
solution: Campaign Standard
product: campaign
title: Aktualisieren der Attribute einer geografischen Einheit
description: Erfahren Sie, wie Sie mit APIs Attribute einer geografischen Einheit aktualisieren können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 100%

---


# Aktualisieren der Attribute einer geografischen Einheit {#managing-geographical-units}

1. Führen Sie eine GET-Anfrage für die Ressource **geoUnitBase** aus, um den PKey der geografischen Einheit abzurufen.
1. Führen Sie eine PATCH-Anfrage für die geografische Einheit mit den Attributen aus, die in der Payload aktualisiert werden sollen.

<br/>

***Beispielanfrage***

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

Führen Sie eine PATCH-Anfrage für die geografische Einheit mit den Attributen aus, die in der Payload aktualisiert werden sollen.

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

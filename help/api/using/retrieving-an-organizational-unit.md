---
solution: Campaign Standard
product: campaign
title: Abrufen der Organisationseinheit eines Profils
description: Erfahren Sie, wie Sie mit APIs die Organisationseinheit eines Profils abrufen können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 100%

---


# Abrufen der Organisationseinheit eines Profils {#retrieving-organizational-units}

1. Führen Sie eine GET-Anfrage für den PKey des Profils aus, um die URL **orgUnit** abzurufen.
1. Führen Sie eine GET-Anfrage für die URL aus, um weitere Details zur Organisationseinheit abzurufen.

<br/>

***Beispielanfrage***

Rufen Sie den Profildatensatz ab.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es wird die orgUnit-URL für das Profil zurückgegeben.

```
{
  ...
  "orgUnit": {
    "PKey": "<PKEY>",
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY>",
    "title": "All (all)"
    },
  ...
}
```

Führen Sie eine GET-Anfrage für die URL aus, um weitere Informationen abzurufen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es werden Details zur Organisationseinheit zurückgegeben.

```
{
  "PKey": "<PKEY>",
  "created": "2019-04-02 22:36:13.252Z",
  "desc": "",
  "label": "Brand 4",
  "lastModified": "2019-04-03 08:17:19.100Z",
  "name": "brand4",
  "parentTitle": "All (all)",
  "title": "Brand 4 (brand4)"
}
```

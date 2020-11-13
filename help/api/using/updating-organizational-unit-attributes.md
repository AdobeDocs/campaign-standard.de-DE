---
title: Aktualisieren der Attribute einer Organisationseinheit
description: Erfahren Sie, wie Sie Attribute einer Organisationseinheit aktualisieren können.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '84'
ht-degree: 100%

---


# Aktualisieren der Attribute einer Organisationseinheit {#updating-organizational-unit-attributes}

1. Führen Sie eine GET-Anfrage für die Ressource **orgUnitBase** aus, um den PKey der Organisationseinheit abzurufen.
1. Führen Sie eine PATCH-Anfrage für die Organisationseinheit mit den Attributen aus, die in der Payload aktualisiert werden sollen.

<br/>

***Beispielanfrage***

Rufen Sie die Liste der Organisationseinheiten ab.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es werden alle Organisationseinheiten zurückgegeben. Rufen Sie den PKey der gewünschten Einheit ab.

```
{
  "PKey": "<PKEY>",
  "created": "2019-04-02 22:36:13.252Z",
  "desc": "",
  "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY>",
  "label": "Brand 4",
  "lastModified": "2019-04-03 07:34:56.579Z",
  "name": "brand4",
  "parentTitle": "All (all)",
  "title": "Brand 4 (brand1)"
},
```

Führen Sie eine PATCH-Anfrage für die Organisationseinheit mit den Attributen aus, die in der Payload aktualisiert werden sollen.

```
-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "label":"brand1",
-d "name":"brand1"
-d }
```

<!-- + réponse -->

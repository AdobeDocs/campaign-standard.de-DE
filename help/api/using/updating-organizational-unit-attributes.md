---
solution: Campaign Standard
product: campaign
title: Aktualisieren der Attribute einer Organisationseinheit
description: Erfahren Sie, wie Sie Attribute einer Organisationseinheit aktualisieren können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Erfahren
translation-type: ht
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: ht
source-wordcount: '88'
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

---
title: Aktualisieren der Organisationseinheit eines Profils
description: Erfahren Sie, wie Sie die Organisationseinheit eines Profils mit APIs aktualisieren.
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


# Aktualisieren der Organisationseinheit eines Profils {#managing-organizational-units}

1. Führen Sie eine GET-Anforderung an die **orgUnitBase** -Ressource aus, um die Organisationseinheit PKey abzurufen
1. Führen Sie eine PATCH-Anforderung auf dem Profil PKey durch, wobei die gewünschte organisatorische Einheit PKey in der Nutzlast enthalten ist.

<br/>

***Musteranforderung***

Rufen Sie die Liste der Einheiten im Unternehmen ab.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es werden alle organisatorischen Einheiten zurückgegeben. Rufen Sie den PKey der Einheit ab, der Sie das Profil zuweisen möchten.

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

Führen Sie eine PATCH-Anforderung im Profil durch, wobei der PKey der gewünschten Organisationseinheit in der Nutzlast enthalten ist.

```
-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "orgUnit":{
-d    "PKey":"<PKEY>"
-d  }
-d }
```

<!-- + réponse -->

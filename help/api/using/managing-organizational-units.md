---
title: Verwalten von Unternehmenseinheiten
description: Erfahren Sie, wie Sie Organisationseinheiten mit APIs verwalten.
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
source-git-commit: c0c0be79613f99a15676343d8ce10d335baf968a

---


# Verwalten von Unternehmenseinheiten {#managing-organizational-units}

Mit dem **Endpunkt orgUnitBase** können Sie mit Einheiten im Unternehmen interagieren und beispielsweise deren Attribute aktualisieren oder die Organisationseinheit eines Profils aktualisieren. Weitere Informationen zu Organisationseinheiten in Campaign finden Sie in der [Kampagnendokumentation](https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html).

Das Feld **Organisatorische Einheit** wird zu einem Profil hinzugefügt, wenn die Profilatressource erweitert wird. Daher sollten Sie immer den Endpunkt **profileAndServicesExt** verwenden, um mit geografischen Einheiten zu interagieren. Weitere Informationen zur Ressourcenerweiterung des Profils finden Sie in der [Kampagnendokumentation](https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles).

## Abrufen der Organisationseinheit eines Profils

1. Führen Sie eine GET-Anforderung für das Profil PKey durch, um die **orgUnit** -URL abzurufen.
1. Führen Sie eine GET-Anforderung für die URL durch, um weitere Details zur Organisationseinheit abzurufen.

<br/>

***Musteranforderung***

Abrufen des Profildatensatzes.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Gibt die URL der orgUnit für das Profil zurück.

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

Führen Sie eine GET-Anforderung für die URL durch, um weitere Informationen abzurufen.

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

## Aktualisieren der Organisationseinheit eines Profils

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

## Aktualisieren von Attributen einer Organisationseinheit

1. Führen Sie eine GET-Anforderung an die **orgUnitBase** -Ressource aus, um die Organisationseinheit PKey abzurufen.
1. Führen Sie eine PATCH-Anforderung auf der Organisationseinheit mit den Attributen durch, die in der Nutzlast aktualisiert werden sollen.

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

Es werden alle organisatorischen Einheiten zurückgegeben. Rufen Sie den PKey der gewünschten Einheit ab.

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

Führen Sie eine PATCH-Anforderung auf der Organisationseinheit mit den Attributen durch, die in der Nutzlast aktualisiert werden sollen.

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

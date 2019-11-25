---
title: Verwaltung geografischer Einheiten
description: Erfahren Sie, wie Sie geografische Einheiten mit APIs verwalten.
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


# Verwaltung geografischer Einheiten {#managing-geographical-units}

>[!CAUTION]
>
>Die Funktion "Geografische Einheit"wurde mit Version 18.7 von Campaign Standard nicht mehr unterstützt.
Daher kann diese Funktion nicht für neue Campaign Standard-Instanzen sowie für vorhandene Instanzen ohne geografische Einheiten ab Version 18.7 implementiert werden.
For more on this, refer to the <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">Deprecated features</a> page.

Mit dem **Endpunkt "geoUnitBase** "können Sie mit geografischen Einheiten interagieren, um beispielsweise deren Attribute zu aktualisieren oder die Einheit eines Profils zu aktualisieren.

Das Feld **Geografische Einheit** wird zu einem Profil hinzugefügt, wenn die Profilatressource erweitert wird. Daher sollten Sie immer den Endpunkt **profileAndServicesExt** verwenden, um mit geografischen Einheiten zu interagieren. Weitere Informationen zur Ressourcenerweiterung des Profils finden Sie in der [Kampagnendokumentation](https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles).

## Abrufen der geografischen Einheit eines Profils

1. Führen Sie eine GET-Anforderung für das Profil PKey durch, um die **geoUnit** -URL abzurufen.
1. Führen Sie eine GET-Anforderung für die URL durch, um weitere Details zur geografischen Einheit abzurufen.

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

Gibt die geoUnit-URL für das Profil zurück.

```
{
  ...
  "geoUnit": {
    "PKey": "@zYV4vIjP1wpBebml6s71hjGiDhs4_gHgbC_UhuJFk8h7XTZxZ5QnZrPnQPEfB__TxwR2ge6sz61D8RR4zvD75CLDZtc<PKEY>",
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/orgUnitBase/<PKEY>",
    "title": "All (all)"
    },
  ...
}
```

Führen Sie eine GET-Anforderung für die URL durch, um weitere Informationen abzurufen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/geoUnitBase/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es gibt Details zur geografischen Einheit zurück.

```
{
  "PKey": "<PKEY>",
  "created": "2019-04-02 22:36:13.252Z",
  "desc": "Default geographical entity (accessible to everyone)",
  "label": "All",
  "lastModified": "2019-04-03 08:17:19.100Z",
  "name": "all",
  "parentTitle": "",
  "title": "All (all)"
}
```

## Aktualisieren der geografischen Einheit eines Profils

1. Führen Sie eine GET-Anforderung für die **Ressource geoUnitBase** durch, um die geografische Einheit PKey abzurufen.
1. Führen Sie eine PATCH-Anfrage auf dem Profil PKey mit der gewünschten geografischen Einheit PKey in der Nutzlast durch.

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

Es werden alle geografischen Einheiten zurückgegeben. Rufen Sie den PKey der Einheit ab, der Sie das Profil zuweisen möchten.

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

Führen Sie eine PATCH-Anfrage für das Profil mit dem PKey der gewünschten geografischen Einheit in der Nutzlast durch.

```
-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "geoUnit":{
-d    "PKey":"<PKEY>"
-d  }
-d }
```

<!-- + réponse -->

## Aktualisieren von Attributen geografischer Einheiten

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

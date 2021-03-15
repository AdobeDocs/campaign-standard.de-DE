---
solution: Campaign Standard
product: campaign
title: Aktualisieren der geografischen Einheit eines Profils
description: Erfahren Sie, wie Sie mit APIs geografische Einheiten verwalten können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Dateningenieur
level: Erfahren
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 96%

---


# Aktualisieren der geografischen Einheit eines Profils {#updating-a-geographical-unit}

1. Führen Sie eine GET-Anfrage für die Ressource **geoUnitBase** aus, um den PKey der geografischen Einheit abzurufen.
1. Führen Sie eine PATCH-Anfrage für den PKey des Profils mit dem PKey der gewünschten geografischen Einheit in der Payload aus.

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

Führen Sie eine PATCH-Anfrage für das Profil mit dem PKey der gewünschten geografischen Einheit in der Payload aus.

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

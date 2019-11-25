---
title: Interaktion mit der Marketinggeschichte
description: Erfahren Sie, wie Sie mit der Marketing-Geschichte von Profilen interagieren.
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


# Interaktion mit der Marketinggeschichte {#interacting-with-marketing-history}

Der **Verlaufsendpunkt** ermöglicht die Interaktion mit dem Marketingverlauf eines Profils.
Auf diese Weise können Sie z. B. die Spiegelseite für eine Lieferung abrufen, die an ein Profil gesendet wurde. Gehen Sie dazu wie folgt vor:

1. Führen Sie ein GET mit dem **Verlaufsendpunkt** und dem primären Schlüssel des Profils durch.
1. Führen Sie eine GET-Anforderung für die zurückgegebenen **events** href durch.
1. Gibt die Liste der Ereignisse für das Profil mit Links zu Spiegelseiten im Knoten **spiegelPage** zurück.

<br/>

***Musteranforderung***

Rufen Sie den Marketingverlauf des Profils mit einer GET-Anforderung ab.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/History/"<PKEY>" \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Der Knoten "events"gibt die URL zurück, über die Sie auf die Ereignisse im Profil zugreifen können.

```
{
  "PKey": "<PKEY>",
  "firstName": "John",
  "lastName":"Doe",
  "birthDate": "1980-10-24",
  "events": {
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events/",
    "metadata": "subHisto"
    },
}
```

Führen Sie eine GET-Anforderung für die zurückgegebenen events href durch.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es gibt die Liste der Ereignisse für das Profil mit Links zu Spiegelseiten im Knoten "spiegelPage"zurück.

```
    {
      "PKey": "<PKEY>",
      "category": "email",
      "date": "2018-05-17 08:44:49.366Z",
      "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events/<PKEY>",
      "label": "Send via email",
      "mirrorPage": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events/<PKEY>/mirrorPage/"
      },
      "type": "outbound"
    }
```

---
title: Vornehmen von Anmeldungen
description: Erfahren Sie, wie Sie mit APIs Anmeldungen vornehmen können.
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
translation-type: ht
source-git-commit: aee0e0437cbfe578cb2f715a2433099c79dd1748

---


# Vornehmen von Anmeldungen {#performing-subscriptions}

## Methode 1: Anmelden eines Profils für einen Dienst

Führen Sie eine GET-Anfrage aus, um das Profil abzurufen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es wird die Anmeldungs-URL für das Profil zurückgegeben.

```
  {
    ...
    "postalAddress":...,
    "preferredLanguage": "none",
    "subscriptions": {
      "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>/subscriptions/"
    },
    ...
  }
```

Führen Sie eine POST-Anfrage für die Anmeldungs-URL mit dem gewünschten Primärschlüssel des Diensts in der Payload aus.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>/subscriptions \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{"service":{"PKey":"<PKEY>"}}'
```

Es wird das aktualisierte Profil mit dem abgeschlossenen Dienstknoten zurückgegeben.

```
{
  ...
  "service": {
    "PKey": "<PKEY>",
    "title": "Sport Newsletter (SVC1)"
  },
  "serviceName": "",
  "subscriber": ...,
  ...
}
```

## Methode 2: Hinzufügen eines Profils zu den Abonnenten eines Diensts

Führen Sie eine GET-Anfrage aus, um den Dienst abzurufen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es wird die Anmeldungs-URL für den Dienst zurückgegeben.

```
  {
    ...
    "messageType": "email",
    "name": "SVC1",
    "subscriptions": {
                "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>/subscriptions/"
    },
    ...
  },
```

Führen Sie eine POST-Anfrage für die Anmeldungs-URL mit dem gewünschten Primärschlüssel des Profils in der Payload aus.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign//profileAndServices/service/<PKEY>/subscriptions/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{"subscriber":{"PKey":"<PKEY>"}}'
```

Es wird der aktualisierte Dienst mit dem abgeschlossenen Abonnentenknoten zurückgegeben.

```
{
  ...
  "service": ...,
  "serviceName": "",
  "subscriber": {
    "PKey": "<PKEY>",
    ...
  },
}
```

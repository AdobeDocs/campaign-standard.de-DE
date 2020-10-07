---
title: Abrufen von Anmeldungen
description: Erfahren Sie, wie Sie mit APIs Anmeldungen abrufen können.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 100%

---


# Abrufen von Anmeldungen {#retrieving-subscriptions}

## Abrufen der Profile, die einen Dienst abonniert haben

Dies ist ein zweistufiges Verfahren.

1. Rufen Sie die Anmeldungs-URL für den gewünschten Dienst ab.
1. Führen Sie eine GET-Anfrage für die Anmeldungs-URL aus. Es wird eine Liste der Anmeldungen für den Dienst mit jedem zugehörigen Profil zurückgegeben.

>[!CAUTION]
>
>Die REST-API gibt die Eigenschaft &quot;href&quot; zurück; diese enthält die zu verwendende URL. <b>Nutzen Sie stets die in der Antwort enthaltene URL, um die nachfolgende API-Anfrage zu erstellen</b>.

<br/>

***Beispielanfrage***

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

Führen Sie eine GET-Anfrage für die Anmeldungs-URL aus.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>/subscriptions \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Eine Liste der Anmeldungen für den Dienst mit jedem zugehörigen Profil wird angezeigt.

```
  {
    ...
    "service": ...,
    "serviceName": "SVC3",
    "subscriber": {
        "PKey": "<PKEY>",
        "email": "",
        "firstName": "John",
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>",
        "lastName": "Doe",
    },
  }
```

## Abrufen der Dienste, die ein Profil abonniert hat

Dies ist ein zweistufiges Verfahren.

1. Rufen Sie die Anmeldungs-URL für ein bestimmtes Profil ab.
1. Führen Sie eine GET-Anfrage für die URL aus. Es wird eine Liste der Anmeldungen für das Profil mit jedem zugehörigen Dienst zurückgegeben.

<br/>

***Beispielanfrage***

Führen Sie eine GET-Anfrage aus, um das Profil abzurufen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Gibt die Anmeldungs-URL für das Profil zurück.

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

Führen Sie eine GET-Anfrage für die Anmeldungs-URL aus.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>/subscriptions \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es wird eine Liste der Dienste zurückgegeben, die das Profil abonniert hat.

```
  {
    ...
    "PKey": "<PKEY>",
    "created": "2017-03-03 10:54:00.363Z",
    "service": {
      "PKey": "<PKEY>",
      "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>",
      "label": "Sport Newsletter",
      "name": "SVC1",
      "title": "Sport Newsletter (SVC1)"
    },
    ...
  }
```

---
title: Abonnements abrufen
description: Erfahren Sie, wie Sie Abonnements mit APIs abrufen.
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


# Abonnements abrufen {#retrieving-subscriptions}

## Abrufen der Profile, die einen Dienst abonniert haben

Dies ist ein zweistufiger Vorgang.

1. Rufen Sie die Abonnement-URL für den gewünschten Dienst ab.
1. Führen Sie eine GET-Anforderung für die Abonnement-URL durch. Es gibt die Liste der Abonnements für den Dienst mit jedem zugehörigen Profil zurück.

>[!CAUTION]
>
>Die REST-API gibt die Eigenschaft "href"zurück, die die zu verwendende URL enthält. <b>Verwenden Sie immer die in der Antwort enthaltene URL, um die nachfolgende API-Anforderung</b>zu erstellen.

<br/>

***Musteranforderung***

Führen Sie eine GET-Anforderung aus, um den Dienst abzurufen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Gibt die Abonnement-URL für den Dienst zurück.

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

Führen Sie eine GET-Anforderung für die Abonnement-URL durch.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>/subscriptions \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Die Liste der Abonnements für den Dienst wird mit jedem zugehörigen Profil angezeigt.

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

## Abrufen der Dienste, für die ein Profil abonniert hat

Dies ist ein zweistufiger Vorgang.

1. Rufen Sie die Abonnement-URL für ein bestimmtes Profil ab.
1. Führen Sie eine GET-Anforderung für die URL durch. Es gibt die Liste der Abonnements für das Profil mit jedem zugehörigen Dienst zurück.

<br/>

***Musteranforderung***

Führen Sie eine GET-Anforderung durch, um das Profil abzurufen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Gibt die Abonnement-URL für das Profil zurück.

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

Führen Sie eine GET-Anforderung für die Abonnement-URL durch.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>/subscriptions \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Gibt die Liste der Dienste zurück, für die das Profil abonniert hat.

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

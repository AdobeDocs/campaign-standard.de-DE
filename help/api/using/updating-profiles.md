---
title: Profile aktualisieren
description: Erfahren Sie, wie Sie mit APIs Profile aktualisieren können.
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
source-wordcount: '96'
ht-degree: 100%

---


# Profile aktualisieren {#updating-profiles}

Das Aktualisieren von Profilen erfolgt über eine **PATCH**-Anfrage.

`https://mc.adobe.io/<ORGANIZATION>/campaign/<apiName>/<resourceName>/<PKEY>`

1. Der erste Schritt besteht aus dem **Abrufen des Profils**.

1. Im zweiten Schritt führen wir eine **PATCH-Anfrage** für das Profil mit den ausgefüllten Informationen in der Payload aus.

1. Um zu überprüfen, ob die PATCH-Anfrage das Profil aktualisiert hat, können wir eine letzte GET-Anfrage ausführen.

<br/>

***Beispielanfrage***

Beispielhafte GET-Anfrage zum Abrufen eines Profils.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>\
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Antwort auf die Anfrage.

```
{
    "content": [
        {
            "PKey": "<PKEY>",
            "firstName": "Amy",
            "lastName":"Dakota",
            "birthDate": "1980-10-24",
            ...
        }
    ]
}
```

PATCH-Anfrage zum Aktualisieren des Attributs &quot;phone&quot;.

```
-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-d '{"phone":"3301020304"}'
```

Es werden der PKEY und die URL zum Abrufen des aktualisierten Profils zurückgegeben.

```
{
    "PKey": "<PKEY>",
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/@2v1dr3ZKJveMDhAdh0MPnh9hNQQ93qb7AW6BNVVKknjwXvTZRBAgUqz1SNcB4ZndgjqOofx3BwBZYBftlmObISoM3rs"
}
```

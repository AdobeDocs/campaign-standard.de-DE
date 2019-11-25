---
title: Verwalten von Diensten und Abonnements
description: Erfahren Sie, wie Sie Dienste und Abonnements mit APIs verwalten.
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


# Verwalten von Diensten und Abonnements {#managing-services-and-subscriptions}

## Dienst erstellen

Die Diensterstellung wird mit einer **POST** -Anforderung an die Dienstressource ausgeführt.

Wenn Sie den Dienst mit bestimmten Attributen erstellen möchten, fügen Sie sie der Nutzlast hinzu. Andernfalls wird der neue Dienst mit Standarddiensten erstellt.

<br/>

***Musteranforderung***

Beispiel-POST-Anforderung, um einen Dienst mit bestimmten Attributen zu erstellen.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
-i
-d {
-d "label": "My newsletter",
-d "messageType": "email",
-d "name": "email_newsletter",
-d "start": "2019-10-06"
-d }
```

Gibt den neu erstellten Dienst mit den aktualisierten Attributen zurück.

```
{
    "PKey": "<PKEY>",
    "builtIn": false,
    "created": "2019-09-26 12:00:37.005Z",
    "href": "https://mc.adobe.io/<ORGANIZATION>/profileAndServices/service/@NLscZuVHxdVu9rPftvrMWFfR1zRIxQGswSOmGLrK09JTF_iWhB0JCUHEndA_vvy__k9mzOYa5NVkcWDcrK8qGh0wygahX9kRcD44kiWWSEceShn3",
    "label": "My newsletter",
    ...
}
```

## Abonnements abrufen

### Abrufen der Profile, die einen Dienst abonniert haben

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

### Abrufen der Dienste, für die ein Profil abonniert hat

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

## Ausführen von Abonnements

### Methode 1: Abonnieren eines Profils für einen Dienst

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

Führen Sie eine POST-Anforderung auf der Abonnement-URL mit dem gewünschten primären Dienstschlüssel in der Payload aus.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>/subscriptions \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{"service":{"PKey":"<PKEY>"}}'
```

Gibt das aktualisierte Profil mit dem abgeschlossenen Dienstknoten zurück.

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

### Methode 2: Hinzufügen eines Profils zu den Abonnenten eines Dienstes

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

Erstellen Sie eine POST-Anforderung auf der Abonnement-URL mit dem gewünschten Profil-Primärschlüssel in der Payload.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign//profileAndServices/service/<PKEY>/subscriptions/ \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{"subscriber":{"PKey":"<PKEY>"}}'
```

Gibt den aktualisierten Dienst mit dem abonnierten Knoten zurück.

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

## Löschen von Abonnements

### Löschen eines Dienstabonnements für ein bestimmtes Profil

Dies ist ein dreistufiger Vorgang.

1. Rufen Sie die Abonnement-URL für das gewünschte Profil ab.
1. Führen Sie eine GET-Anforderung für die Abonnement-URL durch.
1. Führen Sie eine DELETE-Anforderung für die gewünschte Dienst-URL durch.

Ist die Löschanforderung erfolgreich, lautet der Antwortstatus 204 Kein Inhalt.

<br/>

***Musteranforderung***

Die folgenden Beispielnutzdaten zeigen, wie Sie ein Profil von einem Dienst abmelden. Führen Sie zuerst eine GET-Anforderung durch, um das Profil abzurufen.

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

Gibt die Liste der Abonnements für das ausgewählte Profil mit einer URL für jeden abonnierten Dienst zurück.

```
...
"service": {
  "PKey": "<PKEY>",
  "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>",
  "label": "Sport Newsletter",
  "name": "SVC1",
  "title": "Sport Newsletter (SVC1)"
},
...
```

Führen Sie eine DELETE-Anforderung für die gewünschte Dienst-URL durch.

```
-X DELETE https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

<!-- + réponse -->

### Löschen eines Dienstabonnements für ein bestimmtes Profil

Dies ist ein dreistufiger Vorgang.

1. Rufen Sie den gewünschten Dienst und dessen Abonnement-URL ab.
1. Führen Sie eine GET-Anforderung für die Abonnement-URL durch, um alle Profilabonnements abzurufen.
1. Führen Sie eine DELETE-Anforderung für die gewünschte Profilabonnement-URL durch.

Ist die Löschanforderung erfolgreich, lautet der Antwortstatus 204 Kein Inhalt.

<br/>

***Musteranforderung***

Rufen Sie den Dienstdatensatz ab.

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
  "mode": "newsletter",
  "name": "SVC3",
  "subScenarioEventType": "subscriptionEvent",
  "subscriptions": {
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>/subscriptions/"
  },
  "targetResource": "profile",
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

Gibt die Liste der Abonnements für den ausgewählten Dienst mit einer URL (href) für jedes Profilabonnement zurück.

```
{
  "PKey": "<PKEY>",
  "created": "2019-03-26 08:58:04.764Z",
  "email": "",
  "expirationDate": "",
  "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>/subscriptions/<PKEY>",
  "metadata": "subscriptionRcp",
  "service": ...,
  "serviceName": "SVC3",
  "subscriber": ...,
  ...
}
```

Führen Sie eine DELETE-Anforderung für die gewünschte Profilabonnement-URL durch.

```
-X DELETE https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>/subscriptions/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

<!-- + réponse -->

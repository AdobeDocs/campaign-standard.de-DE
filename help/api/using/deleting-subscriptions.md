---
title: Löschen von Abonnements
description: Erfahren Sie, wie Sie Abonnements mit APIs löschen.
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


# Löschen von Abonnements {#mdeleting-subscriptions}

## Löschen eines Dienstabonnements für ein bestimmtes Profil

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

## Löschen eines Dienstabonnements für ein bestimmtes Profil

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

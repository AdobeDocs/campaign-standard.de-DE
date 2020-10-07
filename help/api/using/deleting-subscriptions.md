---
title: Löschen von Anmeldungen
description: Erfahren Sie, wie Sie Anmeldungen mit APIs löschen können.
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
source-wordcount: '233'
ht-degree: 100%

---


# Löschen von Anmeldungen {#mdeleting-subscriptions}

## Löschen einer Dienstanmeldung für ein bestimmtes Profil

Dies ist ein dreistufiges Verfahren.

1. Rufen Sie die Anmeldungs-URL für das gewünschte Profil ab.
1. Führen Sie eine GET-Anfrage für die Anmeldungs-URL aus.
1. Führen Sie eine DELETE-Anfrage für die gewünschte Dienst-URL aus.

Ist die Löschanfrage erfolgreich, lautet der Antwortstatus &quot;204 Kein Inhalt&quot;.

<br/>

***Beispielanfrage***

Die folgenden beispielhaften Payloads zeigen, wie Sie ein Profil von einem Dienst abmelden können. Führen Sie zuerst eine GET-Anfrage aus, um das Profil abzurufen.

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

Es wird eine Liste der Anmeldungen für das ausgewählte Profil mit einer URL für jeden abonnierten Dienst zurückgegeben.

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

Führen Sie eine DELETE-Anfrage für die gewünschte Dienst-URL aus.

```
-X DELETE https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

<!-- + réponse -->

## Löschen einer Dienstanmeldung für ein bestimmtes Profil

Dies ist ein dreistufiges Verfahren.

1. Rufen Sie den gewünschten Dienst und dessen Anmeldungs-URL ab.
1. Führen Sie eine GET-Anfrage für die Anmeldungs-URL durch, um alle Profilanmeldungen abzurufen.
1. Führen Sie eine DELETE-Anfrage für die gewünschte Profilanmeldungs-URL aus.

Ist die Löschanfrage erfolgreich, lautet der Antwortstatus &quot;204 Kein Inhalt&quot;.

<br/>

***Beispielanfrage***

Rufen Sie den Dienstdatensatz ab.

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

Führen Sie eine GET-Anfrage für die Anmeldungs-URL aus.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>/subscriptions \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Für den ausgewählten Dienst wird die Liste aller Anmeldungen zurückgegeben, wobei für jede Profilanmeldung eine URL (href) angegeben ist.

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

Führen Sie eine DELETE-Anfrage für die gewünschte Profilanmeldungs-URL aus.

```
-X DELETE https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>/subscriptions/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

<!-- + réponse -->

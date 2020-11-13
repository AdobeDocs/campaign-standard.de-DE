---
title: Dienst erstellen
description: Erfahren Sie, wie Sie mit APIs einen Dienst erstellen können.
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
source-wordcount: '73'
ht-degree: 100%

---


# Dienst erstellen {#creating-a-service}

Dienste lassen sich mit einer **POST**-Anfrage für die Dienstressource erstellen.

Wenn Sie den Dienst mit bestimmten Attributen erstellen möchten, fügen Sie sie der Payload hinzu. Andernfalls wird der neue Dienst mit Standardattributen eingerichtet.

<br/>

***Beispielanfrage***

Beispielhafte POST-Anfrage zum Erstellen eines Diensts mit bestimmten Attributen.

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

Es wird der neu erstellte Dienst mit den aktualisierten Attributen zurückgegeben.

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

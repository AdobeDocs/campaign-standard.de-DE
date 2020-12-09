---
solution: Campaign Standard
product: campaign
title: Dienst erstellen
description: Erfahren Sie, wie Sie mit APIs einen Dienst erstellen können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: ht
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
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

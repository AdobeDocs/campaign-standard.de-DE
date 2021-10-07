---
title: Interagieren mit dem Marketingverlauf
description: Erfahren Sie, wie Sie mit dem Marketingverlauf von Profilen interagieren können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 67282d21-b4ed-4af5-b751-848a6d705118
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: ht
source-wordcount: '147'
ht-degree: 100%

---

# Interagieren mit dem Marketing-Verlauf {#interacting-with-marketing-history}

Über den Endpunkt **Verlauf** können Sie mit dem Marketingverlauf eines Profils interagieren.
So können Sie z. B. die Mirrorseite für einen Versand abrufen, der an ein Profil gesendet wurde. Gehen Sie dazu wie folgt vor:

1. Führen Sie eine GET-Anfrage für den Endpunkt **Verlauf** und den Primärschlüssel des Profils aus.
1. Führen Sie eine GET-Anfrage für das zurückgegebene href-Attribut **events** aus.
1. Es wird eine Liste der Ereignisse für das Profil mit Links zu Mirrorseiten im Knoten **mirrorPage** zurückgegeben.

<br/>

***Beispielanfrage***

Rufen Sie mit einer GET-Anfrage den Marketingverlauf des Profils ab.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/"<PKEY>" \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Der Knoten &quot;Ereignisse&quot; gibt die URL zurück, über die Sie Zugriff auf die Ereignisse im Profil erhalten.

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

Führen Sie eine GET-Anfrage für das href-Attribut &quot;events&quot; aus.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/history/<PKEY>/events \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es wird eine Liste der Ereignisse für das Profil mit Links zu Mirrorseiten im Knoten &quot;mirrorPage&quot; zurückgegeben.

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

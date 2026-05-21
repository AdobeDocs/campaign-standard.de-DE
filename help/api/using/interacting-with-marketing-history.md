---
title: Interagieren mit dem Marketing-Verlauf
description: Erfahren Sie, wie Sie mit dem Marketing-Verlauf von Profilen interagieren können
feature: API
old-role: Data Architect
role: Developer
level: Experienced
exl-id: 67282d21-b4ed-4af5-b751-848a6d705118
TQID: https://experienceleague.adobe.com/C5r-qK6kpvssv6eFdJNuOw61OXFapg8L8hrlxyb0vcA
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2:
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 100%

---

# Interagieren mit dem Marketing-Verlauf{#interacting-with-marketing-history}

Über den Endpunkt **Verlauf** können Sie mit dem Marketing-Verlauf eines Profils interagieren.
So können Sie z. B. die Mirrorseite für einen Versand abrufen, der an ein Profil gesendet wurde. Gehen Sie dazu wie folgt vor:

1. Führen Sie eine GET-Anfrage für den Endpunkt **Verlauf** und den Primärschlüssel des Profils aus.
1. Führen Sie eine GET-Anfrage für das zurückgegebene href-Attribut **events** aus.
1. Es wird eine Liste der Ereignisse für das Profil mit Links zu Mirrorseiten im Knoten **mirrorPage** zurückgegeben.

<br/>

***Beispielanfrage***

Rufen Sie mit einer GET-Anfrage den Marketing-Verlauf des Profils ab.

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

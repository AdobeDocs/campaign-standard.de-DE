---
solution: Campaign Standard
product: campaign
title: Zählung
description: Erfahren Sie, wie Sie Zählvorgänge durchführen können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: ht
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: ht
source-wordcount: '87'
ht-degree: 100%

---


# Zählung

Die Adobe Campaign REST-API kann die Anzahl der Datensätze in einer Anfrage zählen. Verwenden Sie dazu die URL, die im Knoten **Zählung** zurückgegeben wird.

<br/>

***Beispielanfrage***

Um alle Dienste zu zählen, deren **messageType**-Wert &quot;sms&quot; ist, führen Sie eine GET-Anfrage mit dem Filter **byChannel** aus.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/byChannel?channel=sms \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es werden die Dienste zurückgegeben, die dem Filter entsprechen.

```
{
    "content": [
        {
            ...
            "messageType": "sms",
            "mode": "newsletter",
            "name": "SVC6",
            ...
        },
        ...
    ],
    "count": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/byChannel/_count?channel=sms&_lineStart=@iKTZ2q3IiSEDqZ5Nw1vdoGnQCqF-8DAUJRaVwR9obqqTxhMy"
    },
    "serverSidePagination": true
}
```

Führen Sie eine GET-Anfrage für die URL des Knotens **Zählung** aus, um die Anzahl der Ergebnisse abzurufen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/byChannel/_count?channel=sms&_lineStart=@iKTZ2q3IiSEDqZ5Nw1vdoGnQCqF-8DAUJRaVwR9obqqTxhMy \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es wird die Anzahl der Datensätze zurückgegeben.

```
{
    "count": 26
}
```


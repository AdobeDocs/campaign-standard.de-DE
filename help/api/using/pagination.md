---
solution: Campaign Standard
product: campaign
title: Paginierung
description: Erfahren Sie, wie Sie Paginierungsvorgänge durchführen können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Erfahren
translation-type: ht
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: ht
source-wordcount: '161'
ht-degree: 100%

---


# Paginierung

Standardmäßig werden 25 Ressourcen in eine Liste geladen.

Mit dem Parameter **_lineCount** können Sie die Zahl der in der Antwort aufgelisteten Ressourcen einschränken.  Anschließend können Sie mit dem Knoten **Nächste** die nächsten Ergebnisse anzeigen.

>[!NOTE]
>
>Verwenden Sie stets den URL-Wert, der im Knoten **Nächste** zurückgegeben wird, um eine Paginierungsanfrage auszuführen.
>
>Die Anfrage **_lineStart** wird berechnet und muss stets in der URL, die im Knoten **Nächste** zurückgegeben wird, verwendet werden.

<br/>

***Beispielanfrage***

Beispielhafte GET-Anfrage zum Anzeigen eines Datensatzes der Profilressource

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile?_lineCount=1 \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Antwort auf die Anfrage, wobei der Knoten **Nächste** die Paginierung ausführt.

```
{
    "content": [
        {
            "PKey": "<PKEY>",
            "firstName": "John",
            "lastName":"Doe",
            "birthDate": "1980-10-24",
            ...
        }
    ],
    "next": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10&_
        lineStart=@Qy2MRJCS67PFf8soTf4BzF7BXsq1Gbkp_e5lLj1TbE7HJKqc"
    }
    ...
}
```

Standardmäßig ist der Knoten **Nächste** nicht verfügbar, wenn Tabellen mit einer großen Datenmenge verarbeitet werden. Um die Paginierung auszuführen, müssen Sie den Parameter **_forcePagination=true** zu Ihrer Aufruf-URL hinzufügen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile?_forcePagination=true \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

>[!NOTE]
>
>Die Anzahl der Datensätze, ab der eine Tabelle als groß angesehen wird, wird in der Campaign Standard-Option **XtkBigTableThreshold** definiert. Der Standardwert ist 100.000 Datensätze.

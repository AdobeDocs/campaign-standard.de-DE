---
title: Paginierung
description: Erfahren Sie, wie Sie Paginierungsvorgänge durchführen können.
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
source-git-commit: 59405df2bbb51d7cd944a0630b2b82db864f3920

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

***Beispielanfrage ***

Beispielhafte GET-Anfrage zum Anzeigen eines Datensatzes der Profilressource

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile?_lineCount=1 \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Antwort auf die Anforderung mit dem **nächsten** Knoten, der Paginierung durchführen soll.

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

Standardmäßig ist der **nächste** Knoten nicht verfügbar, wenn Tabellen mit einer großen Datenmenge interagieren. Um Paginierung durchführen zu können, müssen Sie den Parameter **_forcePagination=true** zu Ihrer Aufruf-URL hinzufügen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile?_forcePagination=true \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

>[!NOTE]
>
>Die Anzahl der Datensätze, über denen eine Tabelle als groß betrachtet wird, wird in der Option &quot;Kampagnenstandard XtkBigTableThreshold&quot; **definiert** . Der Standardwert ist 100.000 Datensätze.

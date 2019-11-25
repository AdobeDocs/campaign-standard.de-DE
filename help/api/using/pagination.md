---
title: Paginierung
description: Erfahren Sie, wie Sie Paginierungsvorgänge durchführen.
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


# Paginierung

Standardmäßig werden 25 Ressourcen in eine Liste geladen.

Mit dem Parameter **_lineCount** können Sie die Anzahl der in der Antwort aufgelisteten Ressourcen einschränken.  Anschließend können Sie mit dem **nächsten** Knoten die nächsten Ergebnisse anzeigen.

>[!NOTE]&gt;
>
>Verwenden Sie immer den URL-Wert, der im **nächsten** Knoten zurückgegeben wird, um eine Paginierungsanfrage durchzuführen.
>
>Die **_lineStart** -Anforderung wird berechnet und muss immer innerhalb der URL verwendet werden, die im **nächsten** Knoten zurückgegeben wird.

<!-- serverside pagination. quand table très longue (au delà de 100.000), on peut plus faire de next. doit utiliser à la place les trucs type lineStart etc. si false: voudra dirre que ça a atteint la limite-->

<br/>

***Musteranforderung***

Beispiel-GET-Anforderung, um 1 Datensatz der Profilressource anzuzeigen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile?_lineCount=1 \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

<!-- dans l'exemple, avoir le node "next"-->

Antwort auf die Anfrage.

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
    ...
}
```

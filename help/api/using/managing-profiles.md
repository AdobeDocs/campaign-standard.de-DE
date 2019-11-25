---
title: Verwaltung von Profilen
description: Erfahren Sie, wie Profile mit APIs verwaltet werden.
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


# Verwaltung von Profilen {#managing-profiles}

## Profile abrufen

Das Abrufen von Profilen wird mit einer **GET** -Anforderung ausgeführt.

Anschließend können Sie die Suche mithilfe von Filtern, der Reihenfolge und Paginierung verfeinern. For more on this, refer to the [Additional operations](../../api/using/sorting.md) section.

<br/>

***Beispielanforderungen***

* Beispiel-GET-Anforderung zum Abrufen aller Profile.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

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
           },
           ...
   }
   ```

* Beispiel-GET-Anforderung zum Abrufen der ersten 10 E-Mail-Werte.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10 \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   Antwort auf die Anfrage. Der Knoten "Weiter"gibt die URL zurück, über die Sie auf die 10 nächsten E-Mail-Werte zugreifen können.

   ```
   {
   "content": [
       "amy.dakota@mail.com",
       "kristen.smith@mail.com",
       "omalley@mail.com",
       "xander.harrys@mail.com",
       "jane.summer@mail.com",
       "gloria.boston@mail.com",
       "edward.snow@mail.com",
       "dorian.simons@mail.com",
       "peter.paolini@mail.com",
       "mingam+test08@adobe.com"
   ],
   "next": {
       "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10&_
       lineStart=@Qy2MRJCS67PFf8soTf4BzF7BXsq1Gbkp_e5lLj1TbE7HJKqc"
   }
   }
   ```

## Aktualisieren von Profilen

Das Aktualisieren von Profilen erfolgt mit einer **PATCH** -Anforderung.

`https://mc.adobe.io/<ORGANIZATION>/campaign/<apiName>/<resourceName>/<PKEY>`

1. Der erste Schritt besteht darin, das Profil **abzurufen**.

1. Bei einer zweiten Anforderung führen wir eine **PATCH-Anforderung** im Profil mit den ausgefüllten Informationen in der Nutzlast durch.

1. Um zu überprüfen, ob die PATCH-Anforderung das Profil aktualisiert hat, können wir eine letzte GET-Anforderung durchführen.

<br/>

***Musteranforderung***

Beispiel-GET-Anforderung zum Abrufen eines Profils.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>\
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Antwort auf die Anfrage.

```
{
    "content": [
        {
            "PKey": "<PKEY>",
            "firstName": "Amy",
            "lastName":"Dakota",
            "birthDate": "1980-10-24",
            ...
        }
    ]
}
```

PATCH-Anfrage zur Aktualisierung des Attributs "phone".

```
-X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-d '{"phone":"3301020304"}'
```

Gibt die PKEY und URL zurück, um das aktualisierte Profil abzurufen.

```
{
    "PKey": "<PKEY>",
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/@2v1dr3ZKJveMDhAdh0MPnh9hNQQ93qb7AW6BNVVKknjwXvTZRBAgUqz1SNcB4ZndgjqOofx3BwBZYBftlmObISoM3rs"
}
```

## Profile erstellen

Das Erstellen von Profilen wird mit einer **POST** -Anforderung in der Profilinstanz durchgeführt.

>[!CAUTION]
>
>Wenn Sie eine <b>orgUnit</b> mit dem erstellten Profil verknüpfen möchten, müssen Sie die Profilressource mit diesem Feld erweitern und nach der Veröffentlichung der Erweiterung eine POST-Anforderung am <b>ProfilAndServicesExt</b> -Endpunkt durchführen.
>
>Weitere Informationen zur Ressourcenerweiterung des Profils finden Sie in der <a href="https://helpx.adobe.com/campaign/standard/administration/using/organizational-units.html#partitioning-profiles">Kampagnendokumentation</a>.

<br/>

***Musteranforderung***

Beispiel-POST-Anfrage, um ein Profil mit der E-Mail "john.doe@mail.com"zu erstellen.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-i
-d '{"email":"john.doe@mail.com"}'
```

Es wird das neu erstellte Profil mit der E-Mail-Adresse "john.doe@mail.com"zurückgegeben.

```
{
    "PKey": "<PKEY>",
    "firstName": "John",
    "lastName":"Doe",
    "birthDate": "1980-10-24",
    "email": "john.doe@mail.com",
    ...
}
```

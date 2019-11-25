---
title: Filter
description: Erfahren Sie, wie Sie Filtervorgänge durchführen.
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


# Filter {#filtering}

## Abrufen von Filtermetadaten

Für jede Ressource stehen Filter zur Verfügung. Um die mit einer Ressource verknüpften Filter zu identifizieren, müssen Sie eine GET-Anforderung für die Ressourcenmetadaten durchführen. Diese Anforderung gibt die URL zurück, unter der alle Filter für eine bestimmte Ressource definiert sind. For more on metadata, refer to [this section](../../api/using/metadata-mechanism.md).

Um die Metadaten eines Filters zu identifizieren und zu bestimmen, wie er verwendet werden soll, müssen Sie eine GET-Anforderung für die zuvor zurückgegebene URL durchführen.

<br/>

***Musteranforderung***

Die folgenden Beispielnutzdaten zeigen, wie die "byText"-Filtermetadaten für die "Profil"-Ressource abgerufen werden. Führen Sie zuerst eine GET-Anforderung für die "Profil"-Ressourcenmetada durch.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/resourceType/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Gibt die URL zurück, in der die Filter beschrieben sind.

```
{
"filters": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/resourceType/<PKEY>/filters/"
    }
  }
```

Führen Sie eine GET-Anforderung für die URL durch. Es wird die Liste der Filter für die Profilatressource mit den jedem Filter zugeordneten Metadaten zurückgegeben.

```
{
"birthday": {
        "PKey": "@FL-CbDFXbnHbXcVpeCGWL46VXJLn1LqxLMPagt2vz8sCxQ52lvB15KiUaxXkxJYQw-tZXYrgUWG6K8QcB4gxVY9RKoba5bRFY3294YFshDmorRr8",
        "category": "0150_profile",
        "condition": ...,
        "data": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/birthday?type=$value&precision=$value&operator=$value&day=$value&month=$value&includeStart=$value&endDay=$value&endMonth=$value&includeEnd=$value&relativeValue=$value&nextUnitsValue=$value&previousUnitsValue=$value",
        "formType": "webPage",
        "fragmentName": "",
        "label": "Birthday",
}
```

## Filtert Metadatenstruktur

Für jeden Filter ist dieselbe Metadatenstruktur verfügbar:

* Die Felder **@formType** und **@webPage** sind technische Felder.
* Das **Datenfeld** enthält ein Beispiel zur Verwendung des Filters.
* Der **Metadaten** -Knoten beschreibt die Filterparameter.
* Der Knoten **Bedingung** beschreibt, was der Filter tun soll. Die im Metadaten-Knoten beschriebenen Filterparameter werden zum Erstellen von Filterbedingungen verwendet. Wenn **enabledIf** true ist, wird für jede Filterbedingung der **expr** angewendet.

<br/>

Beispiel für die Metadatenstruktur:

```
"byText": {
        "PKey": "...",
        "category": "99_none",
        "condition": ...,
        "data": "/profileAndServices/profile/byText?text=$value",
        "formType": "none",
        "fragmentName": "",
        "label": "By name or email",
    }
```

## Verwenden von Filtern

Die Filterung wird mit der folgenden Anforderung durchgeführt:

`GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/<resourceName>/by<filterName>?<filterParam>=<filterValue>`

Es ist möglich, mehrere Filter in einer einzigen Anforderung zu kombinieren:

`GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/<resourceName>/<filter1name>/<filter2name>?<filter1param>=<filter1value>&<filter2param>=<filter2value>`

<br/>

***Beispielanforderungen***

* Beispiel-GET-Anforderung zum Abrufen der "Service"-Ressourcen mit dem Typ "email".

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/byChannel?channel=email \
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
               "created": "2019-09-25 23:20:35.000Z",
               "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/@I_FIiDush4OQPc0mbOVR9USoh36Tt5CsD35lATvQjdWlXrYc0lFkvle2XIwZUbD8GqTVvSp8AfWFUvjkGMe1fPe5nok",
               "label": "Marketing Newsletter",
               "lastModified": "2019-09-25 23:20:35.000Z",
               "limitedDuration": false,
               "messageType": "email",
               "mode": "newsletter",
               ...
           },
           ...
       ],
       ...
   }
   ```

* Beispiel-GET-Anforderung zum Abrufen der "Profil"-Ressourcen, die "Mustermann"in den Feldern "E-Mail"oder "Nachname"enthalten (der byText-Filter sucht sowohl in den Feldern "E-Mail"als auch "Nachname").

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/byText?text=Doe \
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
           }
           ...
       ],
       ...
   }
   ```

* Beispiel-GET-Anfrage, um die Services-Ressourcen mit dem Typ "email" und der Bezeichnung "sport" abzurufen.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/byChannel/byText?channel=email&text=sport \
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
               "created": "2019-09-26 09:36:01.014Z",
               "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>",
               "label": "sport",
               "lastModified": "2019-09-26 09:36:01.014Z",
               "limitedDuration": false,
               "messageType": "email",
               "mode": "newsletter",
               "name": "SVC13",
               ...
           }
       ],
       ...
   }
   ```

## Benutzerdefinierte Filter

Wenn Sie einen benutzerspezifischen Filter verwenden möchten, müssen Sie ihn in der Benutzeroberfläche von Adobe Campaign Standard erstellen und anpassen. Der benutzerspezifische Filter hat dann dasselbe Verhalten wie die standardmäßigen Filter:

`GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/<resourceName>/by<customFilterName>?<customFilterparam>=<customFilterValue>`

Weitere Informationen finden Sie in der Dokumentation zu Campaign Standard:

* [Filterdefinition konfigurieren](https://helpx.adobe.com/campaign/standard/developing/using/configuring-filter-definition.html).
* [Verwendungsfall: Aufruf einer Ressource mit einem zusammengesetzten Identifizierungsschlüssel](https://docs.adobe.com/content/help/en/campaign-standard/using/developing/adding-or-extending-a-resource/uc-calling-resource-id-key.html).

<br/>

***Musteranforderung***

Beispiel-GET-Anforderung zum Abrufen der "Profil"-Ressourcen mit Transaktionsbeträgen von 100$ oder mehr. Beachten Sie, dass der Filter "byAmount"zunächst in der Benutzeroberfläche von Adobe Campaign Standard definiert und mit der benutzerdefinierten Tabelle "Transaction"verknüpft wurde.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/byAmount?amount_parameter=100 \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

<!--
Response to the request.

```

{
    "content": [
        {
            "PKey": "<PKEY>",
            "builtIn": false,
            "created": "2019-09-26 09:36:01.014Z",
            "desc": "",
            "end": "",
            "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>",
            ...
        }
    ],
}

```

-->

<!-- exemple à vérifier de bout en bout-->

<!--+category = query editor
privacy ?
displayFOrmat ?
pour faire un POST sur une enum, il faut lui passer le @name décrit dans le noeud values, chaque @name a une correspondance en format = au format définit par le resType
-->





<!--
 if link ou collection.* resName +
* resTarget tout ca, ca va ensemble : le système de lien, resTarget va donner la ressource targetée par le lien. type
resType = type technique (long..) resType = link alors unbound='false' ou 'true'
If type = enumeration alors champ "values" rajouté et les valeurs sont dans values
pour faire un POST sur une enum, il faut lui passer le @name décrit dans le noeud values, chaque @name a une correspondance en format = au format définit par le resType
ail faut que la valeur poster soit conforme ,elle doit valider la dataPolicy . La dataPolicy peut soit controler la valeur (email invalide), soit transformé (cas du smartCase par exemple)
type dans les metadata = type de haut-niveau (nombre, text)
-->

---
title: GET/POST/PATCH/LÖSCHEN VON Verben
description: Erfahren Sie mehr über die Verben, die in Campaign Standard-APIs verwendet werden.
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


# GET/POST/PATCH/LÖSCHEN VON Verben {#verbs}

Folgende Verben stehen zur Durchführung von Vorgängen für die Ressourcen zur Verfügung:

* `GET`: ruft ein Element oder eine Sammlung von Elementen ab
* `POST`: erstellt eine Ressource mit Parametern.
* `PATCH`: aktualisiert eine Ressource mit Parametern.
* `DELETE`: löscht eine Ressource.

<!-- ajouter codes retour -->

<br/>

***Beispielanforderungen***

* Beispiel-GET-Anforderung in der Profilsammlung.


   ```
   $curl  
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   Es wird ein Array von Profilen zurückgegeben.


   ```
   {
       "content": [
           {
               "PKey": "<PKEY>",
               "firstName": "Olivia",
               "lastName": "Varney",
               "birthDate": "1977-09-°4",
               "email": "o.varney@mail.com",
           },
           {
               "PKey": "<PKEY>",
               "firstName": "John",
               "lastName": "Doe",
               "birthDate": "1985-08-17",
               "email": "johndoe@mail.com",
           }
       ],
   }
   ```

* Beispiel-GET-Anforderung für ein bestimmtes Profil.


   ```
   $curl  
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   Gibt das angeforderte Profil zurück.


   ```
   {
       "PKey": "<PKEY>",
       "firstName": "John",
       "lastName": "Doe",
       "birthDate": "1985-08-17",
       "email": "johndoe@mail.com",
       ...
   }
   ```

* Beispiel-POST-Anforderung zum Erstellen eines Profils.


   ```
   -X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -d '{"lastName":"Doe"}'
   ```

   Gibt das Profil mit den Standardfeldern zurück.

   ```
   {
       "PKey": "<PKEY>",
       "firstName": "John",
       "lastName": "Doe",
       "birthDate": "1985-08-17",
       "email": "johndoe@mail.com",
   }
   ```

* Beispiel-PATCH-Anforderung zum Aktualisieren eines Profils.

   ```
   -X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -d '{"firstName":"Mark"',"lastName":"Smith"}'
   ```

   Gibt die PKEY und URL zurück, um das aktualisierte Profil abzurufen.

   ```
   {
       "PKey": "<PKEY>",
       "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY>"
   }
   ```

* Beispiel-DELETE-Anforderung zum Löschen eines Profils.

   ```
   -X DELETE https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/<PKEY> \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   Die Anforderung gibt eine Antwort von 200 zurück und bestätigt, dass das Profil gelöscht wurde.

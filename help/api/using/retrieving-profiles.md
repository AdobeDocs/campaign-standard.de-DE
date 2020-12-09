---
solution: Campaign Standard
product: campaign
title: Profile abrufen
description: Erfahren Sie, wie Sie mit APIs Profile abrufen können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: ht
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: ht
source-wordcount: '83'
ht-degree: 100%

---


# Profile abrufen {#retrieving-profiles}

Profile lassen sich mit einer **GET**-Anfrage abrufen.

Anschließend können Sie die Suche mithilfe von Filtern, Reihenfolge und Paginierung verfeinern. Weiterführende Informationen dazu finden Sie im Abschnitt [Zusätzliche Vorgänge](../../api/using/sorting.md).

<br/>

***Beispielanfragen***

* Beispielhafte GET-Anfrage zum Abrufen aller Profile.

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

* Beispielhafte GET-Anfrage zum Abrufen der ersten 10 E-Mail-Werte.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_lineCount=10 \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   Antwort auf die Anfrage. Der Knoten &quot;Nächste&quot; gibt die URL zurück, mit der Sie auf die nächsten 10 E-Mail-Werte zugreifen können.

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

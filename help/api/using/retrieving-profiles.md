---
solution: Campaign Standard
product: campaign
title: Profile abrufen
description: Erfahren Sie, wie Sie mit APIs Profile abrufen können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: da0aa6c111f3e44bb502c1e5c4ad7feff9108d81
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 40%

---


# Profile abrufen {#retrieving-profiles}

Profile lassen sich mit einer **GET**-Anfrage abrufen.

Anschließend können Sie die Suche mithilfe von Filtern, Reihenfolge und Paginierung verfeinern. Weiterführende Informationen dazu finden Sie im Abschnitt [Zusätzliche Vorgänge](../../api/using/sorting.md).

Darüber hinaus können Sie mit Campaign Standard-APIs nach Profilen suchen, die auf einem der folgenden Felder basieren: E-Mail, Vorname, Nachname oder ein benutzerdefiniertes Feld. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](#searching-field).

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

## Suchen nach Profilen anhand eines Felds {#searching-field}

Mit dem Parameter **[!UICONTROL filterType]** können Sie Profil auf Grundlage eines der folgenden Felder abrufen: E-Mail, Vorname, Nachname oder ein benutzerdefiniertes Feld, das beim Erweitern der Profil-Ressource in der erweiterten Filterung hinzugefügt wurde.

>[!NOTE]
>
>Bei Suchvorgängen wird die Groß-/Kleinschreibung beachtet und nur bei Präfixen ausgeführt. So können Sie z. B. nicht mit den letzten Briefen seines Nachnamens nach einem Profil suchen.

***Beispielanfragen***

* Beispielanforderung zum Filtern von Profilen auf Grundlage des Vornamens.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/byText?text=John&filterType=firstName \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

* Beispielanforderung zum Filtern von Profilen auf Basis des Nachnamens.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/byText?text=Miller&filterType=lastName \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

* Beispielanforderung zum Filtern von Profilen auf Basis von E-Mails.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/byText?text=John%40gmail.com&filterType=email \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

* Beispielanforderung zum Filtern von Profilen basierend auf dem benutzerdefinierten Feld &quot;Hobby&quot;.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/byText?cusHobby=Dancing&filterType=Hobby \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

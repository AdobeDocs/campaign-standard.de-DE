---
solution: Campaign Standard
product: campaign
title: Verwalten des CCPA-Opt-outs
description: Erfahren Sie, wie Sie mit APIs das CCPA-Opt-out verwalten können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 100%

---


# Verwalten des CCPA-Opt-outs {#managing-ccpa-optout}

Der CCPA-Opt-out-Status eines Profils kann mithilfe des Profilattributs **ccpaOptOut** und der Werte &quot;true&quot; oder &quot;false&quot; überwacht und verwaltet werden:

`"ccpaOptOut": <value>`

* **true**: untersagt den Verkauf von personenbezogenen Daten.
* **false**: genehmigt den Verkauf von personenbezogenen Daten.

>[!CAUTION]
>
>Das Attribut &quot;CCPA-Opt-out&quot; ist erst ab Version 19.4 verfügbar. In 19.3-Umgebungen müssen Sie die Profilressource erweitern und ein boolesches Feld hinzufügen. Dieses Feld wird der API mit dem ausgewählten Titel hinzugefügt. Wir empfehlen Ihnen die Verwendung von &quot;Opt-out für CCPA&quot;.
>
>Weitere Informationen finden Sie in der Dokumentation [Verwalten von Datenschutzanfragen](../../start/using/privacy-requests.md#sale-of-personal-information-ccpa).

<br/>

***Beispielanfragen***

* Beispielhafte GET-Anfrage zum Abrufen des CCPA-Opt-out-Status eines Profils.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profilesAndServices/profile/<PKEY> \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -H 'Content-Type: application/json;charset=utf-8'
   ```

   Antwort auf die GET-Anfrage.

   ```
   {
   "PKey": "<PKEY>",
     "ccpaOptOut": false,
     "firstName": "John",
     "lastName": "Doe",
   ...
   }
   ```

* Beispielhafte POST-Anfrage zum Markieren eines Profils für CCPA-Opt-out.

   ```
   -X POST https://mc.adobe.io/<ORGANIZATION>/campaign/profilesAndServices/profile/ \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -H 'Content-Type: application/json;charset=utf-8'
   -i
   -d {
   -d  "firstName": "John",
   -d  "lastName": "Doe",
   -d  "email": "jdoe@mail.com",
   -d  "ccpaOptOut": true
   -d }'
   ```

   Antwort auf die GET-Anfrage.

   ```
   {
       ...
       "email": "john.doe@mail.com",
       "firstName": "John",
       "lastName": "Doe",
       "ccpaOptOut": true,
       ...
   }
   ```

* Beispielhafte PATCH-Anfrage zum Aktualisieren eines Profils für CCPA-Opt-out.

   ```
   -X PATCH https://mc.adobe.io/<ORGANIZATION>/campaign/profilesAndServices/profile/<PKEY> \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -H 'Content-Type: application/json;charset=utf-8'
   -i
   -d {
   -d  "ccpaOptOut": true
   -d }'
   ```

   Antwort auf die GET-Anfrage.

   ```
   {
       ...
       "email": "john.doe@mail.com",
       "firstName": "John",
       "lastName": "Doe",
       "ccpaOptOut": true,
       ...
   }
   ```

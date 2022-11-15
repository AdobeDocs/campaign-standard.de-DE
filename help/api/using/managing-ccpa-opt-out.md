---
title: Verwalten des CCPA-Opt-outs
description: Erfahren Sie, wie Sie mit APIs das CCPA-Opt-out verwalten können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: bfc52511-f66f-4948-a939-d0d77e8ef03c
source-git-commit: e41667405b54a7ed0e02889e3002807e4bfd3a05
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 100%

---

# Verwalten des CCPA-Opt-outs {#managing-ccpa-optout}

Der CCPA-Opt-out-Status eines Profils kann mithilfe des Profilattributs **ccpaOptOut** und der Werte &quot;true&quot; oder &quot;false&quot; überwacht und verwaltet werden:

`"ccpaOptOut": <value>`

* **true**: untersagt den Verkauf von personenbezogenen Daten.
* **false**: genehmigt den Verkauf von personenbezogenen Daten.

<!--The “CCPA Opt-Out” attribute is only available starting 19.4. For 19.3 environments, you need to extend the Profiles resource and add a boolean field. This field will be added to the API with the chosen label. We suggest you use “Opt-Out for CCPA”.
>
>For more on this, refer to the [Managing Privacy requests documentation](../../start/using/privacy-requests.md#sale-of-personal-information-ccpa).-->

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

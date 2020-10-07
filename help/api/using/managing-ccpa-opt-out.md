---
title: Verwalten des CCPA-Opt-outs
description: Erfahren Sie, wie Sie mit APIs das CCPA-Opt-out verwalten können.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '153'
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
>Weiterführende Informationen dazu finden Sie in der [Dokumentation zur Datenschutzverwaltung](https://helpx.adobe.com/de/campaign/kb/acs-privacy.html#ccpa).

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

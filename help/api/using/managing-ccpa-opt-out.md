---
title: Verwalten der CCPA-Abmeldung
description: Erfahren Sie, wie Sie CCPA-Ausschluss mit APIs verwalten
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
source-git-commit: aee0e0437cbfe578cb2f715a2433099c79dd1748

---


# Verwalten der CCPA-Abmeldung {#managing-ccpa-optout}

Der CCPA-Ausschluss-Status eines Profils kann mithilfe des Profilattributs **ccpaOptOut** und der Werte "true"oder "false"überwacht und verwaltet werden:

`"ccpaOptOut": <value>`

* **true**:  untersagt den Verkauf von persönlichen Daten.
* **false**: genehmigt den Verkauf von personenbezogenen Daten.

>[!CAUTION]
>
>Das Attribut "CCPA Opt-out"ist erst ab 19.4 verfügbar. Für 19.3-Umgebungen müssen Sie die Profiles-Ressource erweitern und ein boolesches Feld hinzufügen. Dieses Feld wird der API mit der ausgewählten Beschriftung hinzugefügt. Wir empfehlen Ihnen die Verwendung von "Opt-out for CCPA".
>
>For more on this, refer to the [Privacy management documentation](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa).

<br/>

***Beispielanforderungen***

* Beispiel-GET-Anforderung zum Abrufen des CCPA-Abmeldestatus eines Profils.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profilesAndServices/profile/<PKEY> \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>' \
   -H 'Content-Type: application/json;charset=utf-8'
   ```

   Antwort auf die GET-Anforderung.

   ```
   {
   "PKey": "<PKEY>",
     "ccpaOptOut": false,
     "firstName": "John",
     "lastName": "Doe",
   ...
   }
   ```

* Beispiel-POST-Anfrage zur Markierung eines Profils für CCPA-Ausschluss.

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

   Antwort auf die GET-Anforderung.

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

* Beispiel-PATCH-Anfrage zur Aktualisierung eines Profils für CCPA-Ausschluss.

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

   Antwort auf die GET-Anforderung.

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

---
title: Datenschutzverwaltung
description: Weitere Informationen zur Datenschutzverwaltung mit APIs
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


# Datenschutzverwaltung {#privacy-management}

Campaign Standard-APIs bieten Funktionen, die den automatischen Prozess von Anforderungen im Zusammenhang mit Datenschutzbestimmungen wie GDPR und CCPA ermöglichen.

Folgende Aktionen sind möglich:

* Erstellen Sie eine neue Datenschutzanforderung,
* Überwachung einer Datenschutzanforderung,
* Abrufen einer Datenschutzdatendatei,
* Verwalten Sie den CCPA-Abmeldestatus eines Profils.

Der Endpunkt der Datenschutz-API lautet **/privacy/privacyTool**. Die Beschreibung der PrivacyTool-Ressource und die zugehörigen Filter sind in den Ressourcenmetadaten verfügbar. Siehe [Metadatenmechanismus](../../api/using/metadata-mechanism.md).

Die CCPA-Abmeldung wird mithilfe des Profilattributs **ccpaOptOut** verwaltet.

Weitere Informationen zu Adobe Campaign Standard und zur Einhaltung der Datenschutzbestimmungen finden Sie in der [Dokumentation](https://helpx.adobe.com/campaign/kb/acs-privacy.html).

## Erstellen einer Datenschutzanforderung {#creating-a-privacy-request}

>[!CAUTION]
>
>Die Integration des [Datenschutz-Core-Service](https://adobe.io/apis/cloudplatform/gdpr.html) ist die Methode, die Sie für alle Zugriffe und Löschanforderungen verwenden sollten. Ab 19.4 wird die Verwendung der Kampagnen-API und -Schnittstelle für den Zugriff und das Löschen von Anforderungen nicht mehr unterstützt. Weitere Informationen zu veralteten und entfernten Funktionen von Campaign Standard finden Sie auf [dieser Seite](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html).

Datenschutzanforderungen werden mit einer **POST** -Anforderung erstellt.

Bevor Sie Anforderungen erstellen, müssen Sie den zu verwendenden Namespace definieren. Weitere Informationen finden Sie in der Dokumentation zur [Datenschutzverwaltung](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ManagingPrivacyRequests).

Die Payload muss die folgenden Parameter enthalten:

* **name**: einen eindeutigen internen Namen
* **namespace**: der in der Benutzeroberfläche von Campaign Standard konfigurierte Namespace-Name
* **alignValue**: der Abgleichwert, der auf dem im Namespace definierten Abgleichschlüssel basiert
* **label**: Anforderungsbeschriftung
* **type**: den Anforderungstyp. Zulässige Werte sind "access"oder "delete".
* **Regulierung**: die Art der Regelung. Beispiel: "GDPR", "CCPA". Dieser Parameter ist obligatorisch und ab Version 19.4 von Campaign Standard verfügbar. Wenn Sie sich auf einem älteren Build befinden, müssen Sie ihn nicht zu Ihrer Nutzlast hinzufügen.

<br/>

***Musteranforderung***

Diese POST-Anforderung erstellt eine Datenschutzanforderung basierend auf einem E-Mail-Versöhnungsschlüssel, der im Namespace AMCDS2 definiert ist:

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'

{
"name":"PT11832",
"namespaceName": "AMCDS2",
"reconciliationValue": "customers@adobe.com",
"regulation": "gdpr",
"label":"Delete customers",
"type":"delete"
}
```

Antwort auf die POST-Anforderung.

```
{
    "PKey": "<PKEY>",
    "audit": "",
    "created": "2018-03-21 10:41:58.570Z",
    "desc": "",
    "gdprRequestData": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/head/privacyTool/<PKEY>/gdprRequestData/"
    },
    "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>",
    "label": "Delete customers",
    "lastModified": "2018-03-21 10:41:58.570Z",
    "name": "PT11832",
    "namespace": {
        "PKey": "<PKEY>",
        "title": "Doc (AMCDS2)"
    },
    "namespaceName": "AMCDS2",
    "reconciliationValue": "customers@adobe.com",
    "regulation": "gdpr",
    "retryCount": 0,
    "status": "new",
    "title": "Delete customers (PT11832)",
    "type": "delete"
}
```

## Überwachen einer Datenschutzanforderung

Sie können Informationen zu einer erstellten Datenschutzanforderung mithilfe einer **GET** -Anforderung überwachen.

Die Statuslistenbeschreibung finden Sie in der Dokumentation zur [Datenschutzverwaltung](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ManagingPrivacyRequests).

<br/>

***Musteranforderung***

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool \
-H 'Authorization: Bearer <ACCESS_TOKEN>'
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'
```

Antwort auf die GET-Anforderung.

```
{
            "PKey": "<PKEY>",
            "audit": "",
            "created": "2018-03-09 12:28:37.319Z",
            "desc": "",
            "gdprRequestData": {
                "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>/gdprRequestData/"
            },
            "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>",
            "label": "Delete customer profile",
            "lastModified": "2018-03-09 12:39:21.232Z",
            "name": "GDPR6",
            "namespace": {
                "PKey": "<PKEY>",
                "title": "Email (defaultNamespace1)"
            },
            "namespaceName": "defaultNamespace1",
            "reconciliationValue": "customers@adobe.com",
            "regulation": "gdpr",
            "retryCount": 0,
            "status": "errorDataNotFound",
            "title": "Delete customer profile (GDPR6)",
            "type": "delete"
        }
```

## Abrufen einer Datenschutzdatendatei

>[!CAUTION]
>
>Die Integration des [Datenschutz-Core-Service](https://adobe.io/apis/cloudplatform/gdpr.html) ist die Methode, die Sie für alle Zugriffe und Löschanforderungen verwenden sollten. Ab 19.4 wird die Verwendung der Kampagnen-API und -Schnittstelle für den Zugriff und das Löschen von Anforderungen nicht mehr unterstützt. Weitere Informationen zu veralteten und entfernten Funktionen von Campaign Standard finden Sie auf [dieser Seite](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html).

Gehen Sie wie folgt vor, um die Datei abzurufen, die alle mit einem Abgleichungswert verknüpften Informationen enthält:

1. Führen Sie eine **POST** -Anforderung durch, um eine neue Anforderung mit dem Attribut **type="access"** zu erstellen, siehe [Erstellen einer neuen Datenschutzanforderung](#creating-a-privacy-request).

1. Führen Sie eine **GET** -Anforderung durch, um Informationen zur Anforderung abzurufen.

1. Rufen Sie die Datendatei ab, indem Sie eine **POST** -Anforderung an die zurückgegebene **privacyRequestData** -URL mit dem internen Namen der Datenschutzanforderung innerhalb der Nutzlast durchführen. Beispiel: {"name":"PT17"}.

<br/>

***Musteranforderung***

Erstellen Sie eine Datenschutzanforderung mit dem Attribut type="access".

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'

{
"name":"PT11832",
"namespaceName": "AMCDS2",
"reconciliationValue": "customers@adobe.com",
"regulation": "gdpr",
"label":"Delete customers",
"type":"access"
}
```

<!-- + réponse -->

Führen Sie eine GET-Anforderung durch, um Informationen zur Anforderung abzurufen.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'
```

Gibt das Attribut privacyRequestData mit einer verknüpften URL zurück.

```
{
    ...
    "name": "PR2",
    "namespace": ...,
    "namespaceName": "defaultNamespace1",
    "privacyRequestData": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>/privacyRequestData/"
    },
    "reconciliationValue": "johndoe@mail.com",
    "regulation": "gdpr",
    "retryCount": 0,
    "status": "complete",
    "title": "EPR (PR2)",
    "type": "access"
    ...
},
```

Führen Sie eine POST-Anforderung an die URL privacyRequestData mit dem internen Namen der Anforderung innerhalb der Payload durch.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool/<PKEY>/privacyRequestData \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'
-d '{"name": "PR1"}'
```

Gibt den Dateiinhalt zurück.

```
"{data:<gdprRequestData _cs=\" ()\" id=\"8565163\" reconciliationValue=\"'customer@adobe.com'\">\n  <table name=\"nms:recipient\">\n    <rowId='8569152'\n\t\tlastName='customer'\n\t\tfirstName='customer'\n\t\tgender='1'\n\t\temail='customer@adobe.com'\n\t\tcreatedBy-id='8565162'\n\t\tmodifiedBy-id='8565162'\n\t\tlastModified='2018-03-15 13:54:28.708Z'\n\t\tcreated='2018-03-15 13:54:28.708Z'\n\t\tthumbnail='/nl/img/thumbnails/defaultProfil.png'\n\t\temailFormat='2'</row>\n  </table>\n  <table name=\"nms:broadLogRcp\">\n    <row>deliveryLabel='Send via email'\n\t\tdeliveryType='0'\n\t\tcontactDate='2018-03-15 13:58:31.667Z'\n\t\tid='8003'\n\t\taddress='customer@adobe.com'\n\t\tstatus='1'\n\t\tmsg-id='1194'\n\t\teventDate='2018-03-15 13:58:34.726Z'\n\t\tlastModified='2018-03-15 13:59:02.008Z'\n\t\tvariant='default'\n\t\tdelivery-id='8569153'\n\t\tpublicId='1'\n\t\tprofile-id='8569152'</row>\n  </table>\n  <table name=\"nms:trackingLogRcp\">\n    <row>deliveryLabel='Send via email'\n\t\tdeliveryType='0'\n\t\tcontactDate='2018-03-15 13:58:31.667Z'\n\t\turlLabel='Open'\n\t\turlSource=''\n\t\tuserAgent='-1178080215'\n\t\ttrackedDevice='pc'\n\t\tid='5000'\n\t\tlogDate='2018-03-15 14:00:51.650Z'\n\t\tsourceType='html'\n\t\tuserAgent='-1178080215'\n\t\turl-id='1'\n\t\tdelivery-id='8569153'\n\t\tbroadLog-id='8003'\n\t\trecipient-id='8569152'</row>\n    <row>deliveryLabel='Send via email'\n\t\tdeliveryType='0'\n\t\tcontactDate='2018-03-15 13:58:31.667Z'\n\t\turlLabel='Open'\n\t\turlSource=''\n\t\tuserAgent='0'\n\t\ttrackedDevice=''\n\t\tid='6000'\n\t\tlogDate='2018-03-15 16:00:41.110Z'\n\t\tsourceType='html'\n\t\turl-id='1'\n\t\tdelivery-id='8569153'\n\t\tbroadLog-id='8003'\n\t\trecipient-id='8569152'</row>\n  </table>\n</gdprRequestData>}"
```

## Verwalten der CCPA-Abmeldung

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

---
title: Datenschutzanfrage erstellen
description: Erfahren Sie, wie Sie mit APIs eine Datenschutzanfrage erstellen können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 06ad2e13-922b-4f35-8726-007427125c63
source-git-commit: 4b0c4fb13cc11c06e2487e531ca96574e49b6beb
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 100%

---

# Datenschutzanfrage erstellen {#creating-a-privacy-request}

>[!CAUTION]
>
>Die [Privacy Core Service](https://developer.adobe.com/experience-platform-apis/references/privacy-service)-Integration ist die Methode, die Sie für alle Zugriffs- und Löschanfragen verwenden sollten. <!--Starting 19.4, the use of the Campaign API and interface for access and delete requests is deprecated. For more on Campaign Standard deprecated and removed features, refer to [this page](../../rn/using/deprecated-features.md).-->

Datenschutzanfragen werden mit einer **POST**-Anfrage erstellt.

Bevor Sie Anfragen erstellen, müssen Sie den zu verwendenden Namespace definieren. Weiterführende Informationen dazu finden Sie in der [Dokumentation zur Datenschutzverwaltung](../../start/using/privacy-requests.md).

Die Payload muss folgende Parameter enthalten:

* **name**: einen eindeutigen internen Namen
* **namespace**: den Namen des in der Benutzeroberfläche von Campaign Standard konfigurierten Namespace
* **alignValue**: den Abstimmungswert, der auf dem im Namespace definierten Abstimmschlüssel basiert
* **label**: den Titel der Anfrage
* **type**: den Anfragetyp; zulässige Werte sind &quot;access&quot; oder &quot;delete&quot;
* **regulation**: die Art der Vorschrift; Beispiel: &quot;DSGVO&quot;, &quot;CCPA&quot;; dieser Parameter ist obligatorisch und ab Version 19.4 von Campaign Standard verfügbar. Bei Verwendung eines älteren Builds müssen Sie ihn nicht zur Payload hinzufügen.

<br/>

***Beispielanfrage***

Diese POST-Anfrage erstellt eine Datenschutzanfrage basierend auf einem E-Mail-Abstimmschlüssel, der im Namespace AMCDS2 definiert ist:

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

Antwort auf die POST-Anfrage:

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

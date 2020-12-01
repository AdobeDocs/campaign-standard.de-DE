---
solution: Campaign Standard
product: campaign
title: Datenschutzanfrage erstellen
description: Erfahren Sie, wie Sie mit APIs eine Datenschutzanfrage erstellen können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: ad7322905c69f9575e11efc9d8f68cf909dc425f
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 100%

---


# Datenschutzanfrage erstellen {#creating-a-privacy-request}

>[!CAUTION]
>
>Die [Privacy Core Service](https://adobe.io/apis/cloudplatform/gdpr.html)-Integration ist jene Methode, die Sie für alle Zugriffs- und Löschanfragen verwenden sollten. Mit Version 19.4. wurde die Campaign-API und -Schnittstelle für Zugriffs- und Löschanfragen eingestellt. Weiterführende Informationen zu veralteten und entfernten Funktionen von Campaign Standard finden Sie auf [dieser Seite](../../rn/using/deprecated-features.md).

Datenschutzanfragen werden mit einer **POST**-Anfrage erstellt.

Bevor Sie Anfragen erstellen, müssen Sie den zu verwendenden Namensraum definieren. Weiterführende Informationen dazu finden Sie in der [Dokumentation zur Datenschutzverwaltung](https://helpx.adobe.com/de/campaign/kb/acs-privacy.html#ManagingPrivacyRequests).

Die Payload muss folgende Parameter enthalten:

* **name**: einen eindeutigen internen Namen
* **namespace**: den Namen des in der Benutzeroberfläche von Campaign Standard konfigurierten Namensraums
* **alignValue**: den Abstimmungswert, der auf dem im Namensraum definierten Abstimmschlüssel basiert
* **label**: den Titel der Anfrage
* **type**: den Anfragetyp; zulässige Werte sind &quot;access&quot; oder &quot;delete&quot;
* **regulation**: die Art der Vorschrift; Beispiel: &quot;DSGVO&quot;, &quot;CCPA&quot;; dieser Parameter ist obligatorisch und ab Version 19.4 von Campaign Standard verfügbar. Bei Verwendung eines älteren Builds müssen Sie ihn nicht zur Payload hinzufügen.

<br/>

***Beispielanfrage***

Diese POST-Anfrage erstellt eine Datenschutzanfrage basierend auf einem E-Mail-Abstimmschlüssel, der im Namensraum AMCDS2 definiert ist:

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

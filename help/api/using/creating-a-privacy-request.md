---
title: Erstellen einer Datenschutzanforderung
description: Erfahren Sie, wie Sie eine Datenschutzanforderung mit APIs erstellen
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


# Erstellen einer Datenschutzanforderung {#creating-a-privacy-request}

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

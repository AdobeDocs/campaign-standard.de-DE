---
title: Überwachen einer Datenschutzanfrage
description: Erfahren Sie, wie Sie mit APIs eine Datenschutzanfrage überwachen können.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 63864f0f-2c22-4a65-86ae-21897031f30a
source-git-commit: 013293fce8a923e771e10585c41e4ad482003080
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Überwachen einer Datenschutzanfrage {#monitoring-a-privacy-request}

Sie können Informationen zu einer erstellten Datenschutzanfrage mithilfe einer **GET**-Anfrage überwachen.

Die Beschreibung der Statusliste finden Sie in der [Dokumentation zur Datenschutzverwaltung](../../start/using/privacy-requests.md).

<br/>

***Beispielanfrage***

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/privacy/privacyTool \
-H 'Authorization: Bearer <ACCESS_TOKEN>'
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8'
```

Antwort auf die GET-Anfrage.

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

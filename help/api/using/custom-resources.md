---
title: Benutzerdefinierte Ressourcen
description: Weitere Informationen zur Verwaltung benutzerdefinierter Ressourcen mit APIs/
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
source-git-commit: 538739417c4ed28ff2991186dac5fb69d1af3afd

---


# Benutzerdefinierte Ressourcen {#custom-resources}

Adobe Campaign verfügt über ein vordefiniertes Datenmodell, bei dem Daten über verschiedene Ressourcen definiert werden. Sie können das bereitgestellte Datenmodell bereichern, indem Sie die Ressourcen erweitern, um eigene benutzerdefinierte Felder oder Tabellen hinzuzufügen, z. B. Einkaufs- oder Produkttabellen.

Benutzerdefinierte Ressourcen können über APIs mit dem Endpunkt **/profileAndServicesExt** und dem benutzerdefinierten Ressourcennamen aufgerufen werden.

`https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/<resourceName>/`

>[!NOTE]
>
>Verwenden Sie für Ressourcen, die nicht standardmäßig verfügbar sind, immer das Präfix <b>&quot;cus&quot;</b> vor dem Namen der Ressource.

Sie können beliebige Vorgänge mit benutzerdefinierten Ressourcen durchführen, solange diese mit der Profiltabelle verknüpft sind. Betrachten wir zum Beispiel die folgende Tabellenstruktur:

![ALT-Text](assets/cusresources.png)

In diesem Fall sind alle Ressourcen aus den Tabellen **Transaction**, **TransactionDetails** und **Product** verfügbar, solange sie mit der **Profiltabelle** verknüpft sind.

<br/>

***Musteranforderung ***

Beispiel-GET-Anforderung für den Zugriff auf die erweiterte profileAndServicesExt-Ressource.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/\
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
```

Gibt die Liste aller verknüpften benutzerdefinierten Ressourcen zurück. Anschließend können Sie die Ressourcen-URLs verwenden, um alle in dieser Dokumentation beschriebenen API-Aufgaben auszuführen.

```
{
"apiName": "resourceType",
"cusProduct": {
        "content": ...,
        "data": "/profileAndServicesExt/cusProduct/",
        "help": "Product",
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/cusProduct/metadata",
        "name": "cusProduct",
        "type": "collection"
    },
"cusTransaction": {
        "content": ...,
        "data": "/profileAndServicesExt/cusTransaction/",
        "help": "Product",
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/cusTransaction/metadata",
        "name": "cusProduct",
        "type": "collection"
    },
    ...
}
```

Weitere Informationen zur Datenmodellerweiterung finden Sie in der Kampagnendokumentation:

* [Datenmodelle](../../developing/using/data-model-concepts.md)
* [API erweitern](../../developing/using/about-extending-the-api.md)
* [Relationen mit anderen Ressourcen definieren](https://helpx.adobe.com/campaign/standard/developing/using/configuring-the-resource-s-data-structure.html#defining-links-with-other-resources)

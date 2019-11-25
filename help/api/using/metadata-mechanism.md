---
title: Metadatenmechanismus
description: Weitere Informationen zum Metadatenmechanismus.
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


# Metadatenmechanismus {#metadata-mechanism}

Sie können die Ressourcenmetadaten mit **resourceType** in einer GET-Anforderung abrufen:

`GET /profileAndServices/resourceType/<resourceName>`

Die Antwort gibt die Hauptmetadaten aus der Ressource zurück (alle anderen Felder sind beschreibend oder intern):

* Der Knoten **Inhalt** gibt die Felder der Ressource zurück. Für jedes Feld im Knoten **content** können die folgenden Felder gefunden werden:

   * "apiName": Name des Attributs, das in den APIs verwendet wird.
   * "type": dies ist die allgemeine Typdefinition (Zeichenfolge, Zahl, Link, Sammlung, Aufzählung...).
   * "dataPolicy": Der Wert des Felds muss den angegebenen Regeln entsprechen. Wenn die Regel "dataPolicy"beispielsweise auf "email"gesetzt ist, muss der Wert eine gültige E-Mail sein. Während eines PATCH- oder POST-Tests kann die dataPolicy den Wert überprüfen oder den zu transformenden Wert ändern (z. B. smartCase).
   * "category": gibt die Kategorie des Felds im Abfrageeditor an.
   * "resType": dies der technische Typ ist.

      Wenn "type"mit dem Wert "link"oder "collection"ausgefüllt wird, ist der resTarget-Wert der Name der Ressource, auf die der Link abzielt.
Wenn "type"mit dem Wert "enumeration"ausgefüllt wird, wird ein Feld "values"hinzugefügt und jeder Enumeration-Wert wird in der Node **values** detailliert beschrieben.

* Der Knoten **Filter** gibt die URL zum Abrufen der zugehörigen Filter zurück. For more on filters, refer to [this section](../../api/using/filtering.md) section.

<!-- créer une section au même niveau sur les liens -->
<!-- dans l'exemple: birthdate, email +  mettre 2 liens : un de type 1-1 , 1-N
si on prend l'exemple de l'org unit, on aura un bon exemple lien -->
<!-- plus reparler du node Data -->

<br/>

***Musteranforderung***

Führen Sie eine GET-Anforderung für die Ressource aus.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/resourceType/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es gibt die vollständige Beschreibung der Profilatressource zurück.

```
{
...
"content": {
  "email": {...},
    ...
    },
"data": "/profileAndServices/profile/",
"filters": {
        "href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/resourceType/<PKEY>"
    },
"help": "Identified profiles",
"href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/metadata",
"label": "Profiles",
"mandatory": false,
"name": "profile",
"pkgStatus": "never",
"readOnly": false,
"schema": "nms:recipient",
"type": "item"
}
```

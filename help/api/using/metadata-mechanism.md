---
title: Metadatenmechanismus
description: Erfahren Sie mehr über den Metadatenmechanismus.
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
translation-type: ht
source-git-commit: c0c0be79613f99a15676343d8ce10d335baf968a

---


# Metadatenmechanismus {#metadata-mechanism}

Sie können die Metadaten von Ressourcen mit **resourceType** in einer GET-Anfrage abrufen:

`GET /profileAndServices/resourceType/<resourceName>`

In der Antwort werden die Hauptmetadaten der Ressource zurückgegeben (alle anderen Felder sind beschreibend oder intern):

* Der Knoten **Inhalt** gibt die Felder der Ressource zurück. Für jedes Feld im Knoten **Inhalt** können wir folgende Felder finden:

   * &quot;apiName&quot;: Name des Attributs, das in den APIs verwendet wird.
   * &quot;type&quot;: Dies ist die übergeordnete Typdefinition (Zeichenfolge, Zahl, Link, Kollektion, Auflistung...).
   * &quot;dataPolicy&quot;: Der Wert des Felds muss den angegebenen Regeln entsprechen. Wenn die Regel &quot;dataPolicy&quot; beispielsweise auf &quot;email&quot; gesetzt ist, muss der Wert eine gültige E-Mail-Adresse sein. Während eines PATCH- oder POST-Vorgangs kann &quot;dataPolicy&quot; den Wert überprüfen oder den umzuwandelnden Wert ändern (z. B. smartCase).
   * &quot;category&quot;: Gibt die Kategorie des Felds im Abfrageeditor an.
   * &quot;resType&quot;: Dies ist der technische Typ.

      Wenn &quot;type&quot; mit dem Wert &quot;link&quot; oder &quot;collection&quot; ausgefüllt wird, ist der resTarget-Wert der Name der Ressource, auf die der Link abzielt.
Wenn &quot;type&quot; mit dem Wert &quot;enumeration&quot; ausgefüllt wird, wird ein Feld &quot;values&quot; hinzugefügt und jeder Auflistungswert im Knoten **Werte** detailliert beschrieben.

* Der Knoten **Filter** gibt die URL zum Abrufen der zugehörigen Filter zurück. Weiterführende Informationen zu Filtern finden Sie in [diesem Abschnitt](../../api/using/filtering.md).

<!-- créer une section au même niveau sur les liens -->
<!-- dans l'exemple: birthdate, email +  mettre 2 liens : un de type 1-1 , 1-N
si on prend l'exemple de l'org unit, on aura un bon exemple lien -->
<!-- plus reparler du node Data -->

<br/>

***Beispielanfrage ***

Führen Sie eine GET-Anfrage für die Ressource aus.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/resourceType/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es wird die vollständige Beschreibung der Profil-Ressource zurückgegeben.

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

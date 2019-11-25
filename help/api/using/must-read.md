---
title: Must-read
description: Vor der Verwendung von APIs muss gelesen werden.
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


# Must-Read {#must-read}

## Technische Anforderungen

* Adobe Campaign-APIs dürfen nur vom Server zum Server verwendet werden.
* Wenden Sie sich an Ihren technischen Ansprechpartner bei Adobe, wenn der Anwendungsfall, den Sie implementieren möchten, mit der von Adobe Campaign APIs zulässigen Skala übereinstimmt.
* Für das Einrichten eines AdobeIO-Zugriffs sind spezifische Berechtigungen erforderlich. Wenden Sie sich bei Problemen an den Adobe-Support.

## Ressourcendarstellung

Alle API-Ressourcen sind in **JSON** mit einer URL-Erweiterung oder in einem HTTP Accept Header verfügbar:

`GET /profileAndServices/<resourceName>.json`

>[!NOTE]
>
>Ohne Erweiterung in der URL ist das **JSON-Format das Standardformat** für den Inhaltstyp.

<br/>

***Anforderungsmuster***

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile.json \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

## Primärschlüssel und URLs

* Versuchen Sie nicht, eine URL selbst zu erstellen. Alle URLs werden von der API zurückgegeben. Es ist jedoch möglich, eine URL basierend auf dem Ressourcennamen der obersten Ebene zu erstellen.

* Die Werte des automatischen primären Schlüssels (PKey), die die Beispiele illustrieren, sind nicht für eine andere spezifische Bereitstellung vorgesehen. Sie werden von der Adobe Campaign API erstellt.

* Die von Adobe Campaign generierten Werte des automatischen primären Schlüssels dürfen niemals in einer externen Datenbank oder Website gespeichert werden. Sie müssen bestimmte Schlüsselfelder in Ihrer Datenbankdefinition generieren und diese während der Entwicklung verwenden.

## Benutzerdefinierte Schlüssel {#custom-keys}

Wenn die Profilressource mit einem benutzerdefinierten Schlüsselfeld erweitert wurde, können Sie dieses Feld als Schlüssel anstelle des von Adobe Campaign generierten automatischen Primärschlüssels verwenden:

`GET /.../profileAndServicesExt/profile/<customKey>`

Benutzerdefinierte Schlüssel können nicht mit einem PATCH-Vorgang geändert werden, wenn der Schlüsselwert vom Ursprungsschlüssel abweicht oder wenn Sie einen eigenen Geschäftsschlüssel als URI anstelle des von Adobe bereitgestellten verwenden.

Verwenden Sie einen benutzerspezifischen Schlüssel nur für **Profilinstrumente** der obersten Ebene. URLs werden von der API zurückgegeben und sollten niemals von Ihnen selbst erstellt werden.

<br/>

***Musteranforderung***

Um die Abonnements für ein Profil mit einem benutzerdefinierten Schlüssel abzurufen, führen Sie einen GET-Vorgang für den benutzerdefinierten Schlüssel durch.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<customKey> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Führen Sie eine GET-Anforderung für die zurückgegebene Abonnement-URL durch.

```
-X GET <SUBSCRIPTION_URL> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Gibt die Liste der Abonnements für das Profil zurück.

```
"service": {
"PKey": "<PKEY>",
"href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>",
"label": "Sport Newsletter",
"name": "SVC1",
"title": "Sport Newsletter (SVC1)"
}
```

---
title: Wichtige Informationen
description: Wichtige Informationen vor dem Verwenden von APIs.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '320'
ht-degree: 100%

---


# Wichtige Informationen {#must-read}

## Technische Anforderungen

* Adobe Campaign-APIs dürfen nur von Server zu Server verwendet werden.
* Fragen Sie bitte stets Ihren technischen Ansprechpartner bei Adobe, ob der Anwendungsfall, den Sie implementieren möchten, mit dem Funktionsbereich von Adobe Campaign-APIs übereinstimmt.
* Für das Einrichten eines Adobe I/O-Zugriffs sind spezifische Berechtigungen erforderlich. Wenden Sie sich bei Problemen an den Adobe-Support.

## Ressourcendarstellung

Alle API-Ressourcen sind in **JSON** mit einer URL-Erweiterung oder in einer HTTP-Accept-Kopfzeile verfügbar:

`GET /profileAndServices/<resourceName>.json`

>[!NOTE]
>
>Ohne Erweiterung in der URL ist das **JSON-Format das Standardformat** für den Inhaltstyp.

<br/>

***Beispielanfrage***

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile.json \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

## Primärschlüssel und URLs

* Versuchen Sie nicht, selbst eine URL einzurichten. Alle URLs werden von der API zurückgegeben. Es ist jedoch möglich, eine URL basierend auf dem Top-Level-Ressourcennamen zu erstellen.

* Die Werte des automatischen Primärschlüssels (PKey), die zur Veranschaulichung der Beispiele verwendet werden, funktionieren in keiner anderen Bereitstellung. Sie werden von der Adobe Campaign-API erzeugt.

* Die von Adobe Campaign generierten Werte des automatischen Primärschlüssels dürfen niemals in einer externen Datenbank oder Website gespeichert werden. Sie müssen bestimmte Schlüsselfelder in Ihrer Datenbankdefinition generieren und diese bei der Entwicklung verwenden.

## Benutzerdefinierte Schlüssel {#custom-keys}

Wenn die Profilressource um ein benutzerdefiniertes Schlüsselfeld erweitert wurde, können Sie dieses Feld anstelle des von Adobe Campaign generierten automatischen Primärschlüssels als Schlüssel verwenden:

`GET /.../profileAndServicesExt/profile/<customKey>`

Benutzerdefinierte Schlüssel können nicht mithilfe eines PATCH-Vorgangs geändert werden, wenn der Schlüsselwert vom ursprünglichen Schlüssel abweicht oder Sie einen eigenen Schlüssel als URI anstelle des von Adobe bereitgestellten verwenden.

Verwenden Sie einen benutzerdefinierten Schlüssel nur für **Top-Level-Profilressourcen**. URLs werden von der API zurückgegeben und sollten niemals selbst erstellt werden.

<br/>

***Beispielanfrage***

Um die Anmeldungen für ein Profil mit einem benutzerdefinierten Schlüssel abzurufen, führen Sie eine GET-Operation für den benutzerdefinierten Schlüssel aus.

```
-X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServicesExt/profile/<customKey> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Führen Sie eine GET-Anfrage für die zurückgegebene Anmelde-URL aus.

```
-X GET <SUBSCRIPTION_URL> \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Es wird eine Liste der Anmeldungen für das Profil zurückgegeben.

```
"service": {
"PKey": "<PKEY>",
"href": "https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/service/<PKEY>",
"label": "Sport Newsletter",
"name": "SVC1",
"title": "Sport Newsletter (SVC1)"
}
```

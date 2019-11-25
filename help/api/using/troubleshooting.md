---
title: Problembehebung
description: Erfahren Sie mehr über häufige Probleme bei Kampagnen Standard-APIs.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ab5725b326de2f1cb4c5d15d0d3c0303a6bf0f06

---


# Problembehebung {#troubleshooting}

* **Wenn Sie zur Adobe.io-Konsole wechseln, erhalten Sie den folgenden Fehler: "Die Adobe I/O-Konsole steht nur zur Auswahl von Mitgliedern von Unternehmenskonten zur Verfügung. Wenden Sie sich an Ihren Systemadministrator, wenn Sie Zugriff haben möchten."**

Sie können nur API-Schlüssel für die IMS-Organisationen erstellen, deren Administrator Sie sind. Wenn diese Meldung angezeigt wird und Sie API-Schlüssel erstellen möchten und einen Administrator des IMS-Unternehmens fragen möchten.

* **Bei einer Anforderung an Adobe.io erhalten Sie {"error_code":"403023","message":"Profile is not valid"}**

Das bedeutet, dass es ein Problem mit der IMS-Bereitstellung Ihres spezifischen Kampagnenprodukts gibt: Das IMS-Team muss es reparieren.

Um weitere Details zu erhalten, rufen Sie die IMS-API mit Ihrem Token auf, um zu sehen, wie Ihr IMS-Profil aussieht: Sie müssen über einen prodCtx verfügen, wobei die Datei "organisation_id"mit der URL übereinstimmt, die Sie eingegeben haben, damit Adobe.io Ihre Anforderung weiterleiten kann.
Wenn die IMS-Bereitstellung fehlt, muss sie behoben werden.

```
-X GET https://mc.adobe.io/{ORGANIZATION}/campaign/profileAndServices/profile \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

Gibt den folgenden Fehler zurück.

```
{"error_code":"403023","message":"Profile is not valid"}
```

Überprüfen Sie Ihr IMS-Profil mit dieser Anforderung.

```
-X GET https://ims-na1.adobelogin.com/ims/profile/v1 \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>'
```

In der Antwort muss der Wert ORGANISATION_ID in Ihrer ersten GET-Anforderung gleich sein.

```
{
  "countryCode": "FR",
  "mrktPermEmail": null,
  "projectedProductContext": [
    {
    "prodCtx": {
      "statusCode": "ACTIVE",
      "ident": "ZQ9FRQK7BF09YXAESFY9DDQP1G",
      "modDts": 1448307260000,
      "organization_id": "actest",
      "owningEntity": "6096892F54B5819E0A4C98A2@AdobeOrg",
      "serviceCode": "dma_tartan",
      "label": "Adobe Marketing Cloud",
      "serviceLevel": "standard",
      "createDts": 1421181343000,
      "deal_id": " "
      }
    }
  ]
}
```

* **Wenn Sie eine Anfrage an Adobe.io richten, erhalten Sie {"code":500, "message":"Oops. Etwas ist schiefgelaufen. Überprüfen Sie Ihren URI und versuchen Sie es erneut."}**

Adobe.io erklärt Ihre ungültige URI: Der von Ihnen angeforderte URI ist höchstwahrscheinlich ungültig. Wenn Sie auf Adobe.io den Kampagnendienst auswählen, erhalten Sie eine Auswahl mit einer Liste möglicher Organisations_IDs. Sie müssen überprüfen, ob es sich bei der von Ihnen gewählten Option um die URL handelt.

* **Bei einer Anforderung an Adobe.io erhalten Sie {"error_code":"401013","message":"Oauth-Token ist nicht gültig"}**

Entweder Ihr Token ist ungültig (unsachgemäßer IMS-Aufruf zum Generieren eines Tokens) oder Ihr Token ist abgelaufen.

* **Ich sehe mein Profil nach der Erstellung nicht mehr**

Je nach Instanzkonfiguration muss das erstellte Profil einer **orgUnit** zugeordnet werden. Informationen zum Hinzufügen dieses Felds zu Ihrer Erstellung finden Sie in [diesem Abschnitt](../../api/using/managing-profiles.md).

<!-- * (error duplicate key : quand tu crées un profile qui existe déjà , il faut faire un patch pour updater le profile plutôt qu’un POST)

With Curl
List all profiles

Create a profile

Update the mobilePhone attribute of a profile

API Calls on Service

GET the list of services

-->

<!--

How to find and use a filter?
Error codes:

* PAtch sur Age = message d'erreur :
500
Cannot update the 'age' property that is read-only
'age' property is not valid for the 'profile' resource.
-->

<!--
How to filter a list of subscribed profiles with available profile filters ? by date (by les filtres dispo sur la ressource) ?

Pattern classique :

recupérer la liste des subscriptions filtrées d'un profile
1) get sur profile
2) recup PKey
3) get sur PKey
4) get sur href des subscriptions

Comment savoir quel filtre appliquer ?

1) get sur metadata de profile
2) retourne description de la collection subscription
3) get sur la valeur du champ resTarget
4) get sur le href dans filters
5) retourne les filtres applicables sur l'url des data.

-->

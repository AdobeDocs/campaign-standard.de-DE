---
title: Verwalten von Transaktionsmeldungen
description: Erfahren Sie, wie Sie Transaktionsmeldungen mit APIs verwalten.
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


# Managing transactional messages {#managing-transactional-messages}

## Über den Versand von Transaktionsnachrichten

Nach der Erstellung des gewünschten Ereignisses muss die Auslösung dieses Ereignisses in Ihre Webseite integriert werden.

>[!NOTE]
>
>Erstellen und Veröffentlichen von Ereignissen finden Sie in <a href="https://helpx.adobe.com/campaign/standard/administration/using/configuring-transactional-messaging.html">der Kampagnendokumentation</a>.

Sie möchten z. B., dass ein "Warenkorbabbruch"ausgelöst wird, wenn ein Kunde Ihre Website verlässt, bevor er die Produkte in seinem Einkaufswagen kauft. Dazu muss Ihr Webentwickler die REST Transactional Messages API verwenden.

1. Der Entwickler sendet eine Anforderung gemäß der POST-Methode, die das [Senden des Transaktionsereignisses](#sending-a-transactional-event)auslöst.
1. Die Antwort auf die POST-Anforderung enthält einen primären Schlüssel, mit dem der Entwickler eine oder mehrere Anforderungen über eine GET-Anforderung senden kann. So kann er den [Ereignisstatus](#transactional-event-status)abrufen.

## Senden eines Transaktionsereignisses {#sending-a-transactional-event}

Das Transaktionsereignis wird über eine POST-Anforderung mit der folgenden URL-Struktur gesendet:

```
POST https://mc.adobe.io/<ORGANIZATION>/campaign/<transactionalAPI>/<eventID>
```

* **&lt;ORGANISATION&gt;**: Ihre persönliche Organisations-ID. Siehe [diesen Abschnitt](../../api/using/must-read.md).

* **&lt;transactionalAPI&gt;**: die EndPoints der Transactional Messages API.

   Der Name des API-Endpunkts für Transaktionsmeldungen hängt von Ihrer Instanzkonfiguration ab. Es entspricht dem Wert "mc", gefolgt von Ihrer persönlichen Organisations-ID. Nehmen wir das Beispiel des Unternehmens Geometrixx mit der Organisations-ID "geometrixx". In diesem Fall lautet der POST-Antrag wie folgt:

   `POST https://mc.adobe.io/geometrixx/campaign/mcgeometrixx/<eventID>`

   (Beachten Sie, dass der API-Endpunkt für Transaktionsmeldungen auch während der API-Vorschau sichtbar ist)

* **&lt;eventID&gt;**: der Ereignistyp, den Sie senden möchten. Diese ID wird beim Erstellen der Ereignisdefinition generiert. Refer to the [Campaign documentation](https://helpx.adobe.com/campaign/standard/administration/using/configuring-transactional-messaging.html).

### POST-Anforderungsheader

Die Anforderung muss einen "Content-Type: application/json".

Sie müssen ein Zeichensatz hinzufügen, z. B. **utf-8**. Beachten Sie, dass dieser Wert von der verwendeten REST-Anwendung abhängt.

```
-X POST \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8' \
-H 'Content-Length:79' \
```

### POST-Anforderungstext

Die Ereignisdaten sind im JSON POST-Textkörper enthalten. Die Ereignisstruktur hängt von ihrer Definition ab. Die Schaltfläche "API-Vorschau"im Bildschirm "Ressourcendefinition"enthält ein Anforderungsbeispiel. Refer to the [Campaign documentation](https://helpx.adobe.com/campaign/standard/administration/using/configuring-transactional-messaging.html).

Die folgenden optionalen Parameter können zum Ereignisinhalt hinzugefügt werden, um das Senden von mit dem Ereignis verknüpften Transaktionsmeldungen zu verwalten:

* **Ablauf** (optional): nach diesem Datum wird das Senden des Transaktionsereignisses abgebrochen.
* **geplant** (optional): ab diesem Datum wird das Transaktionsereignis verarbeitet und die Transaktionsnachricht gesendet.

>[!NOTE]
>
>Die Werte der Parameter "expiration"und "geplante"entsprechen dem ISO 8601-Format. ISO 8601 gibt die Verwendung des Großbuchstabens "T"zur Trennung von Datum und Uhrzeit an. Es kann jedoch aus der Eingabe oder Ausgabe entfernt werden, um die Lesbarkeit zu verbessern.

### Antwort auf die POST-Anforderung

Die POST-Antwort gibt den Transaktionsstatus zum Zeitpunkt der Erstellung zurück. Verwenden Sie zum Abrufen des aktuellen Status (Ereignisdaten, Ereignisstatus...) den von der POST-Antwort zurückgegebenen primären Schlüssel in einer GET-Anforderung:

`GET https://mc.adobe.io/<ORGANIZATION>/campaign/<transactionalAPI>/<eventID>/`

<br/>

***Musteranforderung***

POST-Anfrage zum Senden des Ereignisses.

```
-X POST https://mc.adobe.io/<ORGANIZATION>/campaign/mcAdobe/EVTcartAbandonment \
-H 'Authorization: Bearer <ACCESS_TOKEN>' \
-H 'Cache-Control: no-cache' \
-H 'X-Api-Key: <API_KEY>' \
-H 'Content-Type: application/json;charset=utf-8' \
-H 'Content-Length:79'

{
  "email":"test@example.com",
  "scheduled":"2017-12-01 08:00:00.768Z",
  "expiration":"2017-12-31 08:00:00.768Z",
  "ctx":
  {
    "cartAmount": "$ 125",
    "lastProduct": "Leather motorbike jacket",
    "firstName": "Jack"
  }
}
```

Antwort auf die POST-Anforderung.

```
{
  "PKey":"<PKEY>",
  "ctx":
  {
    "cartAmount": "",
    "lastProduct": "",
    "firstName": ""
  }
  "email":"",
  "scheduled":"2017-12-01 08:00:00.768Z",
  "expiration":"2017-12-31 08:00:00.768Z",
  "href": "mcAdobe/EVTcartAbandonment/<PKEY>",
  "serverUrl":" https://myserver.com ",
  "status":"pending",
  "type":""
}
```

### Status des Transaktionsereignisses {#transactional-event-status}

In der Antwort können Sie im Feld "Status"wissen, ob das Ereignis verarbeitet wurde oder nicht:

* **ausstehend**: das Ereignis aussteht - das Ereignis nimmt diesen Status ein, wenn es gerade ausgelöst wurde.
* **Verarbeitung**: das Ereignis aussteht - es wird in eine Nachricht umgewandelt und die Nachricht wird gesendet.
* **angehalten**: der Ereignisvorgang angehalten wird. Es wird nicht mehr verarbeitet, sondern in einer Warteschlange in der Adobe Campaign-Datenbank aufbewahrt. For more on this, refer to the [Campaign documentation](https://helpx.adobe.com/campaign/standard/channels/using/event-transactional-messages.html#unpublishing-a-transactional-message).
* **verarbeitet**: das Ereignis verarbeitet und die Nachricht erfolgreich gesendet wurde.
* **ignoriert**: das Ereignis wurde von der Bereitstellung ignoriert, normalerweise, wenn eine Adresse in Quarantäne steht.
* **deliveryFehlgeschlagen**: während der Verarbeitung des Ereignisses ein Bereitstellungsfehler aufgetreten ist.
* **Routingfehler**: Die Routingphase ist fehlgeschlagen. Dies kann beispielsweise eintreten, wenn der angegebene Ereignistyp nicht gefunden werden kann.
* **tooOld**: das Ereignis abgelaufen ist, bevor es verarbeitet werden konnte - dies kann aus verschiedenen Gründen passieren, z. B. wenn ein Senden mehrmals fehlschlägt (was dazu führt, dass das Ereignis nicht mehr aktuell ist) oder wenn der Server Ereignisse nach dem Überladen nicht mehr verarbeiten kann.
* **targetingFehlgeschlagen**: Campaign Standard konnte einen Link, der für das Nachrichten-Targeting verwendet wird, nicht vergrößern.

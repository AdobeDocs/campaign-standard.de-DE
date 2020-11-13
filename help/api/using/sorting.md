---
title: Sortieren
description: Erfahren Sie mehr über die Verwendung von Sortiervorgängen.
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
source-wordcount: '89'
ht-degree: 100%

---


# Sortieren

Sortiervorgänge sind in auf- oder absteigender Reihenfolge verfügbar. Verwenden Sie dazu in Ihrer Anfrage den Parameter **%20desc** oder **%20asc**.

Um zu erfahren, ob sich ein Feld sortieren lässt, prüfen Sie den Parameter &quot;sortable&quot; in den Metadaten der Ressource. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../api/using/metadata-mechanism.md).

<br/>

***Beispielanfragen***

* Beispielhafte GET-Anfrage zum Abrufen von E-Mails in der Datenbank in alphabetischer Reihenfolge.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email/email?_order=email \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   Antwort auf die Anfrage

   ```
   {
   "content": [
       "adam@email.com",
       "allison.durance@example.com",
       "amy.dakota@mail.com",
       "andrea.johnson@mail.com",
       ...
   ]
   ...
   }
   ```

* Beispielhafte GET-Anfrage zum Abrufen der E-Mails in der Datenbank in absteigender alphabetischer Reihenfolge.

   ```
   -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_order=email%20desc \
   -H 'Content-Type: application/json' \
   -H 'Authorization: Bearer <ACCESS_TOKEN>' \
   -H 'Cache-Control: no-cache' \
   -H 'X-Api-Key: <API_KEY>'
   ```

   Antwort auf die Anfrage

   ```
   {
   "content": [
       "tombinder@example.com",
       "tombinder@example.com",
       "timross@example.com",
       "john.smith@example.com",
       ...
   ]
   }
   ```

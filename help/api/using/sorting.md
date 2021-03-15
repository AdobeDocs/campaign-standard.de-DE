---
solution: Campaign Standard
product: campaign
title: Sortieren
description: Erfahren Sie mehr über die Verwendung von Sortiervorgängen.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Dateningenieur
level: Erfahren
translation-type: tm+mt
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 96%

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

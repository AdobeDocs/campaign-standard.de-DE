---
title: Sortieren
description: Erfahren Sie mehr über die Verwendung von Sortiervorgängen.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 7db25b8d-a6f1-4151-bf37-c47e9991ae48
source-git-commit: 13fc1b011f61d67dda128e77b854032801bda263
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Sortieren

Die Sortierung ist standardmäßig in aufsteigender Reihenfolge verfügbar. Um in absteigender Reihenfolge zu sortieren, hängen Sie **%20desc** an den Wert des Parameters **_order** an.

Um zu erfahren, ob sich ein Feld sortieren lässt, prüfen Sie den Parameter &quot;sortable&quot; in den Metadaten der Ressource. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../api/using/metadata-mechanism.md).

<br/>

***Beispielanfragen***

* Beispielhafte GET-Anfrage zum Abrufen von E-Mails in der Datenbank in alphabetischer Reihenfolge.

  ```
  -X GET https://mc.adobe.io/<ORGANIZATION>/campaign/profileAndServices/profile/email?_order=email \
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

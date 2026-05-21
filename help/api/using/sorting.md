---
title: Sortieren
description: Erfahren Sie mehr über die Verwendung von Sortiervorgängen.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
old-role: Data Architect
role: Developer
level: Experienced
exl-id: 7db25b8d-a6f1-4151-bf37-c47e9991ae48
TQID: https://experienceleague.adobe.com/T3EzbDAi8kAK9dVJccPlvIF155gtACzDNnEjEKLpNis
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: b12f6872-9271-4369-85e5-86969a0b99a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 100%

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

---
solution: Campaign Standard
product: campaign
title: '"Schritt 3: Erweiterung überprüfen"'
description: Hier erfahren Sie, wie Sie mit der REST API auf das erweiterte Feld zugreifen können.
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
feature: Datenmodell
role: Entwickler
level: Erfahren
translation-type: ht
source-git-commit: 088b49931ee5047fa6b949813ba17654b1e10d60
workflow-type: ht
source-wordcount: '63'
ht-degree: 100%

---


# Schritt 3: Erweiterung überprüfen{#step-verify-the-extension}

1. Wenden Sie eine GET-Operation auf die Metadaten der Profiles &amp; Services Erweiterungs-API an, um zu überprüfen, ob das in der benutzerdefinierten Ressource Profile hinzugefügte Feld nun verfügbar ist.

   ```
   GET profileAndServicesExt/resourceType/profile
   ```

1. Dabei wird Folgendes ausgegeben:

   ![](assets/extendpandsapiview.png)

   Das Feld steht nun zur Verfügung und kann für weitere Entwicklungs- und Integrationszwecke genutzt werden.


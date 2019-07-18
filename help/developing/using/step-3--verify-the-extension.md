---
title: '"Schritt 3: Erweiterung überprüfen"'
seo-title: '"Schritt 3: Erweiterung überprüfen"'
description: '"Schritt 3: Erweiterung überprüfen"'
seo-description: Hier erfahren Sie, wie Sie mit der REST API auf das erweiterte Feld zugreifen können.
page-status-flag: nie aktiviert
uuid: 35 ba 89 a 5-a 354-466 f -91 a 0-50 de 111 a 2 e 00
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird entwickelt
content-type: Referenz
topic-tags: use-case—extending-the-api
discoiquuid: 21 bad 242-5921-445 c -8 df 9-3 d 57 dbe 35197
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Schritt 3: Erweiterung überprüfen{#step-verify-the-extension}

1. Wenden Sie eine GET-Operation auf die Metadaten der Profiles &amp; Services Erweiterungs-API an, um zu überprüfen, ob das in der benutzerdefinierten Ressource Profile hinzugefügte Feld nun verfügbar ist.

   ```
   GET profileAndServicesExt/resourceType/profile
   ```

1. Dabei wird Folgendes ausgegeben:

   ![](assets/extendpandsapiview.png)

   Das Feld steht nun zur Verfügung und kann für weitere Entwicklungs- und Integrationszwecke genutzt werden.


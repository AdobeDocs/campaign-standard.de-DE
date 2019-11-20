---
title: '"Schritt 3: Erweiterung überprüfen"'
description: Hier erfahren Sie, wie Sie mit der REST API auf das erweiterte Feld zugreifen können.
page-status-flag: never-activated
uuid: 35ba89a5-a354-466f-91a0-50de111a2e00
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
discoiquuid: 21bad242-5921-445c-8df9-3d57dbe35197
internal: n
snippet: y
translation-type: ht
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Schritt 3: Erweiterung überprüfen{#step-verify-the-extension}

1. Wenden Sie eine GET-Operation auf die Metadaten der Profiles &amp; Services Erweiterungs-API an, um zu überprüfen, ob das in der benutzerdefinierten Ressource Profile hinzugefügte Feld nun verfügbar ist.

   ```
   GET profileAndServicesExt/resourceType/profile
   ```

1. Dabei wird Folgendes ausgegeben:

   ![](assets/extendpandsapiview.png)

   Das Feld steht nun zur Verfügung und kann für weitere Entwicklungs- und Integrationszwecke genutzt werden.


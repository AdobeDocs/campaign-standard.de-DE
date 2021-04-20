---
solution: Campaign Standard
product: campaign
title: '"Schritt 3: Erweiterung überprüfen"'
description: Hier erfahren Sie, wie Sie mit der REST API auf das erweiterte Feld zugreifen können.
audience: developing
content-type: reference
topic-tags: use-case--extending-the-api
feature: Data Model
role: Developer
level: Experienced
exl-id: 34cb416c-ee3d-4b7c-a75b-640432db320d
translation-type: ht
source-git-commit: e7fdaa4b1d77afdae8004a88bbe41bbbe75a3f3c
workflow-type: ht
source-wordcount: '61'
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

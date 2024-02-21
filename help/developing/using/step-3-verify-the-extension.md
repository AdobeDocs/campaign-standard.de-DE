---
title: "Schritt 3: Erweiterung überprüfen"
description: Hier erfahren Sie, wie Sie mit der REST API auf das erweiterte Feld zugreifen können.
audience: developing
content-type: reference
topic-tags: use-case-extending-the-api
feature: Data Model
role: Developer
level: Experienced
exl-id: 34cb416c-ee3d-4b7c-a75b-640432db320d
source-git-commit: dcfd4e2610cbf9d250359cab6ed43e8c97dd4536
workflow-type: tm+mt
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

---
title: Benutzerdefinierte Ressourcen
description: Weitere Informationen zur Verwaltung benutzerdefinierter Ressourcen mit APIs/
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
source-git-commit: 5c4d3fc9853bf9bad4efcefaea242fecc9c4c61f

---


# Interaktion mit benutzerdefinierten Ressourcen {#interacting-with-custom-resources}

Mit dem Endpunkt **/customResources** können Sie die benutzerdefinierten ACS-Entitäten in REST verfügbar machen. Auf der Grundlage dieser API ist eine Integration zwischen benutzerdefinierten Entitäten und externen Endpunkten verfügbar.

/customResources hat genau das gleiche Verhalten wie /profileAndServices-Endpunkt.

Die benutzerdefinierten Entitäten, die in dieser API verfügbar sind, sind:

* alle mit der Profilentität verknüpften Entitäten
* alle Entitäten, die mit den untergeordneten Elementen des Profilunternehmens verknüpft sind
* alle Entitäten, die nicht mit dem Profil verknüpft sind, und für diese Entitäten ihre Kinder und Enkel.

>[!NOTE]
>Die benutzerdefinierten Entitäten, die unter "/profileAndServicesExt"verfügbar sind, werden nicht in der /customResources-API bereitgestellt.

Hier ein Beispiel zum Abrufen der Metadaten aus einer benutzerdefinierten Ressource:

```
GET /customResources/resourceType/<customResourceName>
```

Zum Erstellen, Aktualisieren oder Löschen werden GET, POST, PATCH, DELETE verwendet.

```
POST /customResources/<customResourceName>
```

>[!NOTE]
>Der Datenschutz-API-Endpunkt und die Arbeitsabläufe (/privacy/privacyTool) verwalten keine benutzerdefinierten Ressourcen, die nicht mit der Profilentität verknüpft sind.
>Sie sind dafür verantwortlich, alle PII für diese benutzerdefinierten Ressourcen zu verwalten und zu bereinigen. Weitere Informationen zum Datenschutzwerkzeug [finden Sie hier](../../api/using/privacy-management.md).
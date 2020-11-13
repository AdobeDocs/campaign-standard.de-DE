---
title: Benutzerdefinierte Ressourcen
description: Erfahren Sie mehr über die Verwaltung benutzerdefinierter Ressourcen mit APIs.
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
source-wordcount: '183'
ht-degree: 100%

---


# Interagieren mit benutzerdefinierten Ressourcen {#interacting-with-custom-resources}

Über den Endpunkt **/customResources** können Sie die benutzerdefinierten ACS-Ressourcen in REST verfügbar machen. Auf Grundlage dieser API ist eine Integration zwischen benutzerdefinierten Entitäten und externen Endpunkten möglich.

Der Endpunkt /customResources verhält sich genauso wie der Endpunkt /profileAndServices.

Die benutzerdefinierten Ressourcen, die mit dieser API verfügbar werden, beinhalten:

* alle mit der Profilentität verknüpften Entitäten
* alle Entitäten, die mit den untergeordneten Elementen der Profilentität verknüpft sind
* alle Entitäten, die nicht mit dem Profil verknüpft sind, und für diese Entitäten auch die untergeordneten und weiter untergeordneten Elemente

>[!NOTE]
>Die benutzerdefinierten Ressourcen, die unter /profileAndServicesExt verfügbar sind, werden nicht in der API /customResources bereitgestellt.

Hier ein Beispiel zum Abrufen der Metadaten aus einer benutzerdefinierten Ressource:

```
GET /customResources/resourceType/<customResourceName>
```

Zum Erstellen, Aktualisieren oder Löschen werden GET, POST, PATCH und DELETE verwendet.

```
POST /customResources/<customResourceName>
```

>[!NOTE]
>Der Datenschutz-API-Endpunkt und die Workflows (/privacy/privacyTool) verwalten keine benutzerdefinierten Ressourcen, die nicht mit der Profilentität verknüpft sind.
>Bei diesen benutzerdefinierten Ressourcen sind Sie für die Verwaltung und Bereinigung aller personenbezogenen Daten verantwortlich. Weiterführende Informationen zum Datenschutz-Tool [finden Sie hier](../../api/using/creating-a-privacy-request.md).


---
solution: Campaign Standard
product: campaign
title: Benutzerdefinierte Ressourcen
description: Erfahren Sie mehr über die Verwaltung benutzerdefinierter Ressourcen mit APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
feature: API
role: Data Engineer
level: Experienced
exl-id: 19bfeecb-da60-479c-a929-0cfb72ef59e3
translation-type: ht
source-git-commit: e7fdaa4b1d77afdae8004a88bbe41bbbe75a3f3c
workflow-type: ht
source-wordcount: '184'
ht-degree: 100%

---

# Interagieren mit benutzerdefinierten Ressourcen {#interacting-with-custom-resources}

Über den Endpunkt **/customResources** können Sie die benutzerdefinierten Campaign-Ressourcen in REST verfügbar machen. Auf Grundlage dieser API ist eine Integration zwischen benutzerdefinierten Entitäten und externen Endpunkten möglich.

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

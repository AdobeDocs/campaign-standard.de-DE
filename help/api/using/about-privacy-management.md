---
solution: Campaign Standard
product: campaign
title: Über die Datenschutzverwaltung
description: Erfahren Sie mehr über die Datenschutzverwaltung mit APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 100%

---


# Über die Datenschutzverwaltung {#about-privacy-management}

Campaign Standard-APIs bieten Funktionen, die eine automatische Verarbeitung von Anfragen im Zusammenhang mit Datenschutzbestimmungen wie DSGVO und CCPA ermöglichen.

Folgende Aktionen sind möglich:

* Neue Datenschutzanfrage erstellen
* Datenschutzanfrage überwachen
* Datei mit Datenschutz-Daten abrufen
* CCPA-Opt-out-Status eines Profils verwalten

Der Datenschutz-API-Endpunkt lautet **/privacy/privacyTool**. Eine Beschreibung der PrivacyTool-Ressource sowie der zugehörigen Filter finden Sie in den Metadaten der Ressource. Siehe [Metadatenmechanismus](../../api/using/metadata-mechanism.md).

Das CCPA-Opt-out wird mithilfe des Profilattributs **ccpaOptOut** verwaltet.

Weiterführende Informationen zu Adobe Campaign Standard und zur Einhaltung von Datenschutzbestimmungen finden Sie in der [entsprechenden Dokumentation](https://helpx.adobe.com/de/campaign/kb/acs-privacy.html).

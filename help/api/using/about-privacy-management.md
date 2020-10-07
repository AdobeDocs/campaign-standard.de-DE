---
title: Über die Datenschutzverwaltung
description: Erfahren Sie mehr über die Datenschutzverwaltung mit APIs.
page-status-flag: never-activated
uuid: c7b9c171-0409-4707-9d45-3fa72aee8008
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
discoiquuid: 304e7779-42d2-430a-9704-8c599a4eb1da
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
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

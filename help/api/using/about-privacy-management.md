---
title: Über die Datenschutzverwaltung
description: Erfahren Sie mehr über die Datenschutzverwaltung mit APIs.
audience: developing
content-type: reference
topic-tags: campaign-standard-apis
source-git-commit: 210289d44f0ad0ebf0b2654f6e9795adad7dd458
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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

Weiterführende Informationen zu Adobe Campaign Standard und zur Einhaltung von Datenschutzbestimmungen finden Sie in der [entsprechenden Dokumentation](../../start/using/privacy-requests.md).

---
title: Übersicht über das Experience-Datenmodell
description: Das Experience-Datenmodell (XDM) ist ein Standardsatz von Datenschemata, in die Daten eingebunden und mit Adobe Experience Platform-Lösungen und -Produkten verwendet werden können.
page-status-flag: never-activated
uuid: 867b1c4b-4c79-4c52-9d0a-ef71993e50a2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 406c955a-b2d2-4099-9918-95f5fa966067
internal: n
snippet: y
translation-type: ht
source-git-commit: 67223cf8eed46e2431c03674bd837262e37c7473

---


# Übersicht über das Experience-Datenmodell {#experience-data-model-overview}

>[!IMPORTANT]
>
>Der Campaign Standard-Datendienst befindet sich derzeit in der Betaphase, die häufig ohne Vorankündigung aktualisiert werden kann. Kunden müssen auf Azure gehostet werden (derzeit nur für Nordamerika in der Betaphase), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an die Adobe-Kundenunterstützung, wenn Sie Zugriff haben möchten.

Das Experience-Datenmodell (XDM) ist ein Standardsatz von Datenschemata, in die Daten eingebunden und mit Adobe Experience Platform-Lösungen und -Produkten verwendet werden können.

Die Erstellung und Verwaltung von XDM-Schemata ist mit einer speziellen API oder mit der XDM-Benutzeroberfläche möglich.

## XDM-Arbeitsbereich {#xdm-workspace}

Der XDM-Arbeitsbereich bietet die Möglichkeit, Datenschemata anzuzeigen, zu erstellen und zu erweitern.

Um auf die XDM-Benutzeroberfläche zuzugreifen, öffnen Sie Adobe Experience Platform. Navigieren Sie zum Fenster „Datenmodell“, um ein XDM-Schema zu erstellen oder zu erweitern.

Lesen Sie die vollständige [Dokumentation zum XDM-Arbeitsbereich](https://www.adobe.io/apis/experienceplatform/home/xdm/xdmservices.html#!api-specification/markdown/narrative/technical_overview/schema_registry/xdm_system/xdm_system_in_experience_platform.md).

![](assets/aep_xdmworkspace.png)

## XDM-API {#xdm-api}

Sie können die folgenden Aktionen über die XDM-Schema-API ausführen:

* Liste vorhandener Schemata anzeigen
* Ein bestimmte Schema anzeigen, ein bestehende Schema erweitern
* Felder zu einer Erweiterung hinzufügen
* Neues Schema erstellen und aktualisieren
* Schema-Deskriptoren anzeigen
* Schema-Deskriptoren erstellen, aktualisieren und löschen

Alle Details zum Bearbeiten von API-Aufrufen finden Sie im [Entwicklerhandbuch](https://www.adobe.io/apis/experienceplatform/home/xdm/xdmservices.html#!api-specification/markdown/narrative/technical_overview/schema_registry/schema_registry_developer_guide.md).

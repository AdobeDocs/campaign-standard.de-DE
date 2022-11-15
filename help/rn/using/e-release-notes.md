---
title: Vorzeitige Versionshinweise
description: Vorzeitige Versionshinweise
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: 20a59e064afeb93a2a6260439b09790692971071
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 100%

---


# Vorzeitige Versionshinweise {#e-new-release}

Auf dieser Seite werden Verbesserungen und Fehlerbehebungen beschrieben, die in der nächsten Campaign Standard-Version enthalten sind.

>[!CAUTION]
>
> Dieser Inhalt kann ohne vorherige Ankündigung bis zum Aktualisierungsdatum der Staging-Umgebung geändert werden. Weitere Informationen finden Sie auf der [Seite mit der Versionsplanung](../../rn/using/release-planning.md).

## Version 22.3 – Herbst/Winter 2022 {#e-rn-2022}

<!--
### Improvement{#e-rn-improvements}


**Accessibility**

Campaign Standard 22.3 comes with accessibility fixes and improvements which facilitate users to navigate and get the most out of Adobe Campaign.

These capabilities are released in Limited Availability and rolled out to a set of customers only. To have these improvements enabled on your Campaign environment(s), contact your Adobe representative.
-->

### Sicherheits-Update{#e-rn-security}

Diese Version umfasst die folgende Sicherheitsaktualisierung: Apache Tomcat wurde von v7.0 auf v8.0 aktualisiert.

### Fehlerbehebungen{#e-rn-fixes}

* Fehlerkorrektur – Terminierte Berichte werden jetzt nicht mehr eine Stunde vor dem geplanten Zeitpunkt ausgelöst. (CAMP-51502)
* Fehlerkorrektur – Die Versandindikatoren im Versand-Dashboard stimmen jetzt mit den Versandlogs überein (nms:broadLogRcp). (CAMP-51127)
* Fehlerkorrektur – Die Erweiterung benutzerdefinierter Ressourcen mit dem ACS-Connector (Prime-Angebot) ist jetzt möglich. (CAMP-51033)
* Der Veröffentlichungsprozess für Antworten auf Datenschutzanfragen wurde verbessert, um Verzögerungen zu vermeiden. (CAMP-50613)
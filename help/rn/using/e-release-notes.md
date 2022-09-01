---
title: Vorzeitige Versionshinweise
description: Vorzeitige Versionshinweise
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: 3f9adbf4e8c9066b1954a1443654d82ee7b53fea
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 20%

---


# Vorzeitige Versionshinweise {#e-new-release}

Auf dieser Seite werden Verbesserungen und Fehlerbehebungen beschrieben, die in der nächsten Campaign Standard-Version enthalten sind.

>[!CAUTION]
>
> Dieser Inhalt kann ohne vorherige Ankündigung bis zum Aktualisierungsdatum der Staging-Umgebung geändert werden. Weitere Informationen finden Sie auf der [Seite mit der Versionsplanung](../../rn/using/release-planning.md).

## Version 22.3 – September 2022 {#e-rn-2022}


### Verbesserung{#e-rn-improvements}

**Barrierefreiheit**

Campaign Standard 22.3 enthält Fehlerbehebungen und Verbesserungen für die Barrierefreiheit, die den Benutzern die Navigation und Nutzung von Adobe Campaign erleichtern.

Diese Funktionen werden unter &quot;Eingeschränkte Verfügbarkeit&quot;veröffentlicht und nur für eine Reihe von Kunden bereitgestellt. Wenden Sie sich an Ihren Kundenbetreuer, um diese Verbesserungen für Ihre Campaign-Umgebung(en) aktivieren zu lassen.

<!--
* **Data retention**

    Data retention periods have been reduced to avoid overloading Campaign server. However, you can still modify these values and define a custom period of time based on your needs and data retention policies. To change retention periods, contact Adobe.
-->

### Sicherheitsupdate{#e-rn-security}

Diese Version umfasst die folgende Sicherheitsaktualisierung: Apache Tomcat wurde von v7.0 auf v8.0 aktualisiert.

### Fehlerbehebungen{#e-rn-fixes}

* Es wurde ein Problem mit terminierten Berichten behoben, die eine Stunde vor dem geplanten Zeitpunkt ausgelöst wurden. (CAMP-51502)
* Fehlerkorrektur - Die Versandindikatoren im Versand-Dashboard stimmen jetzt mit den Versandlogs überein (nms:broadLogRcp). (CAMP-51127)
* Fehlerkorrektur - Die Erweiterung benutzerdefinierter Ressourcen mit ACS Connector (Prime-Angebot) ist jetzt möglich. (CAMP-51033)
* Der Veröffentlichungsprozess für Antworten auf Datenschutzanfragen wurde verbessert, um Verzögerungen zu vermeiden. (CAMP-50613)
---
title: Aktuelle Version
description: Auf dieser Seite finden Sie Informationen zum Inhalt der aktuellen Version von Campaign Standard.
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: 93f1a6cb0727859f3c3f645366a9d2dc25795a79
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 20%

---


# Aktuelle Version{#latest-release}

![Control Panel](assets/do-not-localize/cp-icon.png) **Neue Control Panel-Version**. [Weitere Informationen](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html?lang=de){target=&quot;_blank&quot;}.


## Version 22.3 - Herbst/Winter 2022 {#sept-22}

### Verbesserung{#rn-improvements}

**Barrierefreiheit**

Campaign Standard 22.3 enthält Fehlerbehebungen und Verbesserungen für die Barrierefreiheit, die den Benutzern die Navigation und Nutzung von Adobe Campaign erleichtern.

Diese Funktionen werden unter &quot;Eingeschränkte Verfügbarkeit&quot;veröffentlicht und nur für eine Reihe von Kunden bereitgestellt. Wenden Sie sich an Ihren Kundenbetreuer, um diese Verbesserungen für Ihre Campaign-Umgebung(en) aktivieren zu lassen.

<!--
* **Data retention**

    Data retention periods have been reduced to avoid overloading Campaign server. However, you can still modify these values and define a custom period of time based on your needs and data retention policies. To change retention periods, contact Adobe.
-->

### Sicherheitsupdate{#rn-security}

Diese Version umfasst die folgende Sicherheitsaktualisierung: Apache Tomcat wurde von v7.0 auf v8.0 aktualisiert.

### Fehlerbehebungen{#e-rn-fixes}

* Es wurde ein Problem mit terminierten Berichten behoben, die eine Stunde vor dem geplanten Zeitpunkt ausgelöst wurden. (CAMP-51502)
* Fehlerkorrektur - Die Versandindikatoren im Versand-Dashboard stimmen jetzt mit den Versandlogs überein (nms:broadLogRcp). (CAMP-51127)
* Fehlerkorrektur - Die Erweiterung benutzerdefinierter Ressourcen mit ACS Connector (Prime-Angebot) ist jetzt möglich. (CAMP-51033)
* Der Veröffentlichungsprozess für Antworten auf Datenschutzanfragen wurde verbessert, um Verzögerungen zu vermeiden. (CAMP-50613)


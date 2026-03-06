---
title: Versionshinweise 2025
description: Auf dieser Seite werden alle Versionen von Adobe Campaign Standard von 2025 aufgelistet.
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89114
source-git-commit: 4df02bb5bbac105057a33d61a7158482bbc48a53
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 100%

---

# Versionshinweise 2025 {#release-notes-2025}

## Version 25.2 – Version Sommer 2025 {#summer-25}

### Korrekturen von Sicherheitsproblemen {#summer-25-security}

* Diese Version enthält mehrere Korrekturen von Sicherheitsproblemen.
* Diese Version umfasst die folgende Sicherheitsaktualisierung: PostgreSQL 14.18, Migration von CentOS zu Rocky für Azure-Instanzen.

### Andere Fehlerbehebungen {#summer-25-fixes}

* Optimierte Handhabung der Sequenzerschöpfung, um die Systemzuverlässigkeit zu erhöhen. (CAMP-57281)
* Allgemeine Aktualisierungen zur Produktstabilisierung. (CAMP-57339)
* Optimierung dynamischer Berichte zum Erhöhen der Stabilität und Verringern von Datendiskrepanzen. (CAMP-58157)
* Es wurde ein Problem mit falschen Zeilenumbrüchen von Text in Dropdown-Menüs behoben. (CAMP-57360)
* Die Berichtfunktion wurde aktualisiert, damit Benutzende keine Daten abfragen können, die älter als zwei Jahre sind. (CAMP-59262)

## Version 25.1.2 {#25.1.2}

### Korrekturen von Sicherheitsproblemen {#25.1.2-security}

* Diese Version enthält mehrere Korrekturen von Sicherheitsproblemen.
* Diese Version umfasst die folgende Sicherheitsaktualisierung: Apache Tomcat wurde auf v10.1.36 aktualisiert.

### Andere Fehlerbehebungen {#25.1.2-fixes}

* Fehlerkorrektur – Es wurde ein Token-Parsing-Problem behoben, das für Benutzende eine Anmeldung über IMS verhindern konnte. (CAMP-57337)
* Fehlerkorrektur – Der Mechanismus für die ID-Generierung mit automatischer Sequenz wurde optimiert, um die Systemzuverlässigkeit zu erhöhen. (CAMP-57281)

## Version 25.1 – Version Winter 2025 {#winter-25}

### Korrekturen von Sicherheitsproblemen {#winter-25-security}

* Diese Version enthält mehrere Korrekturen von Sicherheitsproblemen.
* Diese Version umfasst die folgende Sicherheitsaktualisierung: Apache Tomcat wurde auf v10.1.33 aktualisiert.

### Andere Fehlerbehebungen {#winter-25-fixes}


* Fehlerkorrektur – Die Datenschema-URL im Bildschirm für die Zusammenfassung des Abonnements ist jetzt richtig (CAMP-56168, CAMP-56296).
* Fehlerkorrektur – Die Ermüdungsregeln werden jetzt nicht mehr umgangen, wenn die Option **Nachricht sofort senden** verwendet wird (CAMP-56866, CAMP-57033).
* Fehlerkorrektur – In Vorlagen tritt jetzt kein Duplikatproblem mehr auf (CAMP-56340).
* Fehlerkorrektur – Es wurde eine Tracking-Regression behoben, die auftrat, wenn in Adobe Experience Manager-Vorlagen dynamische URLs verwendet wurden (CAMP-51932).
* Fehlerkorrektur – Beim Abrechnungsprozess treten jetzt keine Leistungsprobleme mehr auf (CAMP-56796).
* Fehlerkorrektur – Es wurde ein HTML-Kodierungsproblem mit dem Zeichen „`>`“ auf JSSP-Web-Seiten behoben (CAMP-56497).
* Fehlerkorrektur – Bei der Verwendung der Option **In ausgewählten Zeilen anzeigen** in dynamischen Berichten tritt jetzt kein Fehler mehr auf (CAMP-55895).


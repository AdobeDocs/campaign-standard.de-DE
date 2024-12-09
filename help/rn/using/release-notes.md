---
title: Neueste Versionshinweise
description: Auf dieser Seite finden Sie Informationen zum Inhalt der aktuellen Version von Campaign Standard.
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: c2d2f3843801d108f007fea52a76e41abe16d76c
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 76%

---


# Neueste Versionshinweise {#latest-release}

<!--
![Control Panel](assets/do-not-localize/cp-icon.png) **New Control Panel release**. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html){target="_blank"}.-->


## Frühzeitige Versionshinweise {#e-new-release}

In diesem Abschnitt werden Verbesserungen und Änderungen beschrieben, die in der nächsten Version von Campaign Standard enthalten sein werden.

>[!CAUTION]
>
>Dieser Inhalt kann ohne vorherige Ankündigung bis zum Aktualisierungsdatum der Staging-Umgebung geändert werden. Weitere Informationen finden Sie auf der [Seite mit der Versionsplanung](../../rn/using/release-planning.md).

### Version 25.1 – Version Winter 2025 {#winter-25}

#### Sicherheitskorrekturen {#winter-25-security}

* Diese Version beinhaltet Sicherheitskorrekturen.
* Diese Version enthält die folgende Sicherheitsaktualisierung: Apache Tomcat wurde auf Version 10.1.33 aktualisiert.

#### Weitere Fehlerbehebungen {#winter-25-fixes}

* Korrektur eines Duplikatsproblems in Vorlagen (CAMP-56340)
* Fehlerkorrektur - Es wurde eine Tracking-Regression behoben, wenn dynamische URLs in Adobe Experience Manager-Vorlagen verwendet wurden. (CAMP-51932)
* Es wurde ein Leistungsproblem beim Abrechnungsprozess behoben (CAMP-56796).
* Fehlerkorrektur - Es wurde ein HTML-Kodierungsproblem mit dem Zeichen `>` auf JSSP-Webseiten behoben (CAMP-56497)
* Fehlerkorrektur - Bei der Verwendung der Option **In ausgewählten Zeilen anzeigen** in dynamischen Berichten tritt jetzt kein Fehler mehr auf. (CAMP-55895)


## Version 24.2 - Sommerversion 2024 (LA) {#summer-24}

### Verbesserung {#summer-24-rn-improvements}

**Migration zu OAuth-Server-zu-Server-Anmeldedaten**

Ab dieser Version sind ausgehende Campaign-Integrationen in Adobe-Lösungen und -Apps auf OAuth-Server-zu-Server-Anmeldedaten angewiesen, weil die Anmeldedatenoption „Service-Konto (JWT)“ eingestellt wurde. Adobe führt die Migration von JWT zu OAuth für Ihre ausgehenden Integrationen durch, z. B. die Integration von Campaign-Analytics oder die Integration von Experience Cloud Triggers.

Wenn Sie eingehende Integrationen mit Campaign implementiert haben und [Campaign-APIs](../../api/using/get-started-apis.md) verwenden, müssen Sie Ihr technisches Konto gemäß den Anweisungen in [dieser Dokumentation](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/){target="_blank"} migrieren. Bestehende Anmeldedaten für Service-Konten (JWT) sind noch bis zum **27. Januar 2025** gültig.

### Fehlerbehebungen {#summer-24-rn-fixes}

* Fehlerkorrektur – Die Workflow-Planung startet jetzt nicht mehr vor der geplanten Zeit. (CAMP-55412)
* Fehlerkorrektur – Beim Duplizieren benutzerdefinierter Felder in Push-Benachrichtigungen zu Transaktionen tritt jetzt kein Fehler mehr auf. (CAMP-54459)
* Fehlerkorrektur – Die Verwendung der Uhrzeit- und Datumsplanung für In-App-Messaging funktioniert jetzt ordnungsgemäß. (CAMP-54495)
* Fehlerkorrektur – Das Tracking funktioniert jetzt ordnungsgemäß, wenn die Funktion für den benutzerdefinierten Tracking-Alias verwendet wird und der gesamte Link dynamisch ist. (CAMP-56044)
* Fehlerkorrektur – Bei der Suche nach bestimmten Vorlagen ist die Anzahl der angezeigten Vorlagen jetzt nicht mehr begrenzt. (CAMP-55273)
* Die folgenden Sprachen wurden der Dropdown-Liste der bevorzugten Sprachen hinzugefügt: en_kz (Englisch – Kasachstan) und en_ua (Englisch – Ukraine). (CAMP-55336)
* Fehlerkorrektur – Die Schaltflächen zum Anpassen der Zeit funktionieren jetzt in den Planungseinstellungen. (CAMP-53602)
* Es wurden mehrere Probleme mit der Benutzeroberfläche in Bezug auf die Leiste zum Anpassen der Zeit in den Planungseinstellungen behoben. (CAMP-55291)

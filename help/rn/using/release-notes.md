---
title: Neueste Versionshinweise
description: Auf dieser Seite finden Sie Informationen zum Inhalt der aktuellen Version von Campaign Standard.
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: 625b2341b1f7da17d202ef1edcdf97f3cb46b801
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 73%

---


# Neueste Versionshinweise {#latest-release}

<!--
![Control Panel](assets/do-not-localize/cp-icon.png) **New Control Panel release**. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html){target="_blank"}.-->

<!--
## Early release notes {#e-new-release}

This section lists improvements and changes included in the next Campaign Standard release.

>[!CAUTION]
>
>This content is subject to changes without prior notice until the stage environments upgrade date. Learn more in the [Release planning page](../../rn/using/release-planning.md).
-->

## Version 24.2 – Version Sommer 2024 {#summer-24}

<!--**Release date**: August 2024 (Limited Availability) - [Learn more](../../rn/using/release-planning.md).-->

### Verbesserung {#summer-24-rn-improvements}

**Migration zu OAuth-Server-zu-Server-Anmeldedaten**

Ab dieser Version sind ausgehende Campaign-Integrationen in Adobe-Lösungen und -Apps auf OAuth-Server-zu-Server-Anmeldedaten angewiesen, weil die Anmeldedatenoption „Service-Konto (JWT)“ eingestellt wurde. Adobe führt die Migration von JWT zu OAuth für Ihre ausgehenden Integrationen durch, z. B. die Integration von Campaign-Analytics oder die Integration von Experience Cloud Triggers.

Wenn Sie eingehende Integrationen mit Campaign implementiert haben und [Campaign-APIs](../../api/using/get-started-apis.md) verwenden, müssen Sie Ihr technisches Konto gemäß den Anweisungen in [dieser Dokumentation](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/){target="_blank"} migrieren. Bestehende Anmeldedaten für Service-Konten (JWT) sind noch bis zum **27. Januar 2025** gültig.

### Fehlerbehebungen {#summer-24-rn-fixes}

* Fehlerkorrektur - Die Workflow-Planung startet jetzt nicht mehr vor der geplanten Zeit. (CAMP-55412)
* Fehlerkorrektur - Beim Duplizieren von benutzerdefinierten Feldern in Transaktions-Push-Benachrichtigungen tritt jetzt kein Fehler mehr auf. (CAMP-54459)
* Es wurden Probleme behoben, die sich auf die Benutzerfreundlichkeit der Planung von Uhrzeit und Datum für In-App-Nachrichten auswirkten. (CAMP-54495)
* Es wurde ein Fehler behoben, der dazu führte, dass Tracking bei der Verwendung der Funktion &quot;Benutzerspezifischer Tracking-Alias&quot;nicht funktionierte und der gesamte Link dynamisch war. (CAMP-56044)
* Es wurde ein Fehler behoben, der dazu führte, dass bei der Suche nach bestimmten Vorlagen eine begrenzte Anzahl von Vorlagen angezeigt wurde. (CAMP-55273)
* Die folgenden Sprachen wurden zur Dropdown-Liste der bevorzugten Sprachen hinzugefügt: en_kz (Englisch - Kasachstan) und en_ua (Englisch - Ukraine). (CAMP-55336)
* Es wurde ein Fehler behoben, der dazu führte, dass die Schaltflächen zur Zeitanpassung in den Planungseinstellungen nicht funktionierten. (CAMP-53602)
* Fehlerkorrektur - Es wurden mehrere Probleme mit der Benutzeroberfläche in Bezug auf die Zeitanpassungsleiste in den Planungseinstellungen behoben. (CAMP-55291)

## Version 24.1 – Version Winter 2024 {#winter-24}

### Verbesserungen {#e-rn-improvements}

* **Android-Push-Benachrichtigungen**: Adobe Campaign Standard 24.1 verwendet die HTTP v1-APIs zum Senden von Android-Push-Benachrichtigungen, um die Kompatibilität mit anstehenden FCM-Änderungen sicherzustellen. Weitere Informationen finden Sie in [dieser Technote](../../administration/using/push-technote.md).

* **iOS-Push-Benachrichtigungen**: Adobe Campaign Standard 24.1 unterstützt jetzt p8-Authentifizierungszertifikate für iOS-Push-Benachrichtigungen. Ihre Implementierung muss angepasst werden, um diese Änderungen zu aktivieren. Weitere Informationen finden Sie in [dieser Technote](../../administration/using/push-technote.md).

* **Ein-Klick-Abmeldung**: Ab dem 1. Juni 2024 verlangen Google und Yahoo! von Absenderinnen und Absendern die Einhaltung der Vorschrift, eine Ein-Klick-Abmeldung anzubieten. Campaign unterstützt diese Funktion jetzt standardmäßig. Weiterführende Informationen finden Sie in [diesem Abschnitt](../../administration/using/configuring-email-channel.md#list-of-email-smtp-parameters).

* **Infrastruktur**: Die Postgres-Datenbank wurde von Version 11.22 auf Version 12.17 aktualisiert.

* **CTA-Tracking**: Wenn Benutzende eine personalisierte URL öffnen und darauf klicken, wird jetzt die aufgelöste personalisierte URL anstelle der codierten personalisierten URL getrackt. Diese Änderung ist nicht standardmäßig aktiviert. Wenden Sie sich an Ihre Adobe-Kontaktperson, damit sie in Ihrer Campaign-Instanz aktiviert wird.

* **Dropdown-Liste für Personalisierungsfelder**: Beim Erstellen von Vorlagen für Transaktions-E-Mail-Nachrichten in Adobe Experience Manager können Sie jetzt Personalisierungsfelder aus einer Dropdown-Liste auswählen. Diese Änderung ist nicht standardmäßig aktiviert. Wenden Sie sich an Ihre Adobe-Kontaktperson, damit sie in Ihrer Campaign-Instanz aktiviert wird.

### Fehlerbehebungen {#e-rn-fixes}

* Fehlerkorrektur – Bounce-E-Mail-Adressen können jetzt nach 30 Tagen aus der Quarantäne genommen werden. (CAMP-52977)
* Fehlerkorrektur – Der Workflow „Versandwarnung“ wird jetzt nicht mehr mit folgendem Fehler angehalten: `division by zero`. (CAMP-49786)


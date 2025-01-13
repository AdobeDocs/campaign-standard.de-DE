---
title: Versionshinweise 2024
description: Auf dieser Seite werden alle Versionen von Adobe Campaign Standard von 2024 aufgelistet.
feature: Overview
role: User
level: Beginner
exl-id: 26616ecc-a009-485c-b13d-d4e0c23969f2
source-git-commit: 85f3a3d8fe9e41eaa78fac955bc2d0f3f3d2c35e
workflow-type: ht
source-wordcount: '490'
ht-degree: 100%

---

# Versionshinweise 2024 {#release-notes-2024}


## Version 24.2 – Version Sommer 2024 (LA) {#summer-24}

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

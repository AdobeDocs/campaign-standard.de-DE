---
title: Aktuelle Version
description: Auf dieser Seite finden Sie Informationen zum Inhalt der aktuellen Version von Campaign Standard.
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: 9291eb06c35b1d06c0a992fa64a460215477f57e
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 38%

---


# Aktuelle Version{#latest-release}

<!--
![Control Panel](assets/do-not-localize/cp-icon.png) **New Control Panel release**. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html){target="_blank"}.-->

## Version 24.1 – Version Winter 2024 {#winter-24}

### Verbesserungen {#e-rn-improvements}

* **Android-Push-Benachrichtigungen** - Adobe Campaign Standard 24.1 verwendet die HTTP v1-APIs zum Senden von Android-Push-Benachrichtigungen, um die Kompatibilität mit anstehenden FCM-Änderungen sicherzustellen. Weitere Informationen finden Sie in [dieser Technote](../../administration/using/push-technote.md).

* **Push-Benachrichtigungen in iOS** - Adobe Campaign Standard 24.1 unterstützt jetzt p8-Authentifizierungszertifikate für iOS-Push-Benachrichtigungen. Ihre Implementierung muss angepasst werden, um diese Änderungen zu aktivieren. Weitere Informationen finden Sie in [dieser Technote](../../administration/using/push-technote.md).

**One-Click List-Unsubscribe** - Ab dem 1. Juni 2024, Google und Yahoo! von Absenderinnen und Absendern die Einhaltung der Vorschrift, eine Ein-Klick-Abmeldung anzubieten. Campaign unterstützt diese Funktion jetzt standardmäßig. Weiterführende Informationen finden Sie in [diesem Abschnitt](../../administration/using/configuring-email-channel.md#list-of-email-smtp-parameters).

* **Infrastruktur** - Die Postgres-Datenbank wurde von Version 11.22 auf Version 12.17 aktualisiert.

* **CTA-Tracking** - Wenn die Benutzer eine personalisierte URL öffnen und darauf klicken, wird die aufgelöste personalisierte URL jetzt anstelle der codierten personalisierten URL verfolgt. Diese Änderung ist standardmäßig nicht aktiviert. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, damit sie in Ihrer Campaign-Instanz aktiviert wird.

* **Dropdown-Liste für Personalisierungsfelder** - Bei der Erstellung von Vorlagen für Transaktions-E-Mail-Nachrichten in Adobe Experience Manager können Sie jetzt Personalisierungsfelder aus einer Dropdown-Liste auswählen. Diese Änderung ist standardmäßig nicht aktiviert. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, damit sie in Ihrer Campaign-Instanz aktiviert wird.

### Fehlerbehebungen {#e-rn-fixes}

* Fehlerkorrektur – Bounce-E-Mail-Adressen können jetzt nach 30 Tagen aus der Quarantäne genommen werden. (CAMP-52977)
* Fehlerkorrektur – Der Workflow „Versandwarnung“ wird jetzt nicht mehr mit folgendem Fehler angehalten: `division by zero`. (CAMP-49786)


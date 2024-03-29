---
title: Aktuelle Version
description: Auf dieser Seite finden Sie Informationen zum Inhalt der aktuellen Version von Campaign Standard.
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: 26a1c36003645446fb8b827d76afba749d64e9f2
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 100%

---


# Aktuelle Version{#latest-release}

<!--
![Control Panel](assets/do-not-localize/cp-icon.png) **New Control Panel release**. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html){target="_blank"}.-->

## Version 24.1 – Version Winter 2024 {#winter-24}

### Verbesserungen {#e-rn-improvements}

Adobe Campaign Standard 24.1 verwendet die HTTP v1-APIs zum Senden von Android-Push-Benachrichtigungen, um die Kompatibilität mit anstehenden FCM-Änderungen sicherzustellen. Weitere Informationen finden Sie in [dieser Technote](../../administration/using/push-technote.md).

Adobe Campaign Standard 24.1 unterstützt jetzt p8-Authentifizierungszertifikate für iOS-Push-Benachrichtigungen. Ihre Implementierung muss angepasst werden, um diese Änderungen zu aktivieren. Weitere Informationen finden Sie in [dieser Technote](../../administration/using/push-technote.md).

Ab dem 1. Juni 2024, verlangen Google und Yahoo von Absenderinnen und Absendern die Einhaltung der Vorschrift, eine Ein-Klick-Abmeldung anzubieten. Campaign unterstützt diese Funktion jetzt standardmäßig. Weiterführende Informationen finden Sie in [diesem Abschnitt](../../administration/using/configuring-email-channel.md#email-channel-parameters).

### Fehlerbehebungen {#e-rn-fixes}

* Fehlerkorrektur – Bounce-E-Mail-Adressen können jetzt nach 30 Tagen aus der Quarantäne genommen werden. (CAMP-52977)
* Fehlerkorrektur – Der Workflow „Versandwarnung“ wird jetzt nicht mehr mit folgendem Fehler angehalten: `division by zero`. (CAMP-49786)


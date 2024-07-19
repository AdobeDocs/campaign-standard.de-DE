---
title: Neueste Versionshinweise
description: Auf dieser Seite finden Sie Informationen zum Inhalt der aktuellen Version von Campaign Standard.
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: 44c436a74a0a4aa688427bfb36d506566d57ac3a
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 100%

---


# Neueste Versionshinweise {#latest-release}

<!--
![Control Panel](assets/do-not-localize/cp-icon.png) **New Control Panel release**. [Learn more](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html){target="_blank"}.-->


## Frühzeitige Versionshinweise {#e-new-release}

In diesem Abschnitt werden Verbesserungen und Änderungen beschrieben, die in der nächsten Version von Campaign Standard enthalten sein werden.

>[!CAUTION]
>
>Dieser Inhalt kann ohne vorherige Ankündigung bis zum Aktualisierungsdatum der Staging-Umgebung geändert werden. Weitere Informationen finden Sie auf der [Seite mit der Versionsplanung](../../rn/using/release-planning.md).

**Version 24.2 – Version Sommer 2024**

* **Veröffentlichungsdatum**: August 2024 (eingeschränkte Verfügbarkeit) – [Weitere Informationen](../../rn/using/release-planning.md).

* **Migration zu OAuth-Server-zu-Server-Anmeldedaten**

  Ab dieser Version sind ausgehende Campaign-Integrationen in Adobe-Lösungen und -Apps auf OAuth-Server-zu-Server-Anmeldedaten angewiesen, weil die Anmeldedatenoption „Service-Konto (JWT)“ eingestellt wurde. Adobe führt die Migration von JWT zu OAuth für Ihre ausgehenden Integrationen durch, z. B. die Integration von Campaign-Analytics oder die Integration von Experience Cloud Triggers.

  Wenn Sie eingehende Integrationen mit Campaign implementiert haben und [Campaign-APIs](../../api/using/get-started-apis.md) verwenden, müssen Sie Ihr technisches Konto gemäß den Anweisungen in [dieser Dokumentation](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/){target="_blank"} migrieren. Bestehende Anmeldedaten für Service-Konten (JWT) sind noch bis zum **27. Januar 2025** gültig.


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


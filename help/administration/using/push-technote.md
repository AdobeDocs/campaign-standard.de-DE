---
title: Künftige Änderungen am Push-Benachrichtigungskanal
description: Künftige Änderungen am Push-Benachrichtigungskanal
audience: channels
feature: Instance Settings
role: Admin
level: Experienced
hide: true
hidefromtoc: true
source-git-commit: f9a0d01196ac4c31e57ae14cdfa448a9ffd6106f
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 42%

---

# Künftige Änderungen am Push-Benachrichtigungskanal {#push-upgrade}

Sie können Campaign verwenden, um Push-Benachrichtigungen auf Android- und iOS-Geräten zu senden. Dazu benötigt Campaign bestimmte Abonnementdienste. Einige wichtige Änderungen am Android Firebase Cloud Messaging (FCM)-Dienst werden 2024 veröffentlicht und wirken sich auf Ihre Adobe Campaign-Implementierung aus. Darüber hinaus ändert Adobe bei iOS-Apps die Art und Weise, wie Administratoren Zertifikate konfigurieren können.

## Was hat sich geändert? {#push-changes}

### Android {#push-android}

Im Rahmen der kontinuierlichen Bemühungen von Google, seine Dienste zu verbessern, werden die veralteten FCM-APIs eingestellt auf **20. Juni 2024**. Weitere Informationen zum Firebase Cloud Messaging-HTTP-Protokoll finden Sie in [Dokumentation zu Google Firebase](https://firebase.google.com/docs/cloud-messaging/http-server-ref){target="_blank"}.

Derzeit verwendet Adobe Campaign Standard ältere HTTP-APIs, um Android-Push-Benachrichtigungen zu senden, und wird in den kommenden Monaten Änderungen vornehmen, um auf die HTTP v1-APIs zu aktualisieren.

### iOS {#push-ios}

Adobe aktualisiert außerdem Adobe Campaign Standard für den iOS-Kanal für Push-Benachrichtigungen und ändert die Art und Weise, wie Admins Zertifikate für ihre iOS-Anwendungen konfigurieren können. Admins müssen jetzt die iOS-Zertifikate über die Benutzeroberfläche von Adobe Campaign Standard hochladen.

## Sind Sie betroffen? {#push-impact}

Wenn Sie als Campaign Standard Push-Benachrichtigungen an Ihre Zielgruppen senden, sind Sie betroffen.

## Wie wird die Migration durchgeführt? {#push-migration}

Diese Updates erfordern eine Aktualisierung des Campaign Standard-Builds, da sie sich auf die Konfiguration und Berechtigungsverwaltung für Mobilkanäle auswirken.

In Kürze werden detaillierte Anweisungen bereitgestellt, um einen reibungslosen Übergangsprozess zu erleichtern.

Unser Support-Team steht Ihnen während des gesamten Übergangszeitraums zur Verfügung. Unter Umständen werden wir auch Webinare und Aktivierungssitzungen veranstalten, um die technischen Aspekte und Best Practices für die Umstellung abzudecken.

In der Zwischenzeit wird empfohlen, diese Zeit zu benötigen, um Ihre aktuelle Konfiguration und Anpassung in Adobe Campaign Standard zu überprüfen, damit Sie bei Bedarf bereit sind, erforderliche Änderungen vorzunehmen.

Wenn Sie Fragen oder Anliegen haben, wenden Sie sich bitte an unser Support-Team.

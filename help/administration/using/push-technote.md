---
title: Künftige Änderungen am Push-Benachrichtigungskanal
description: Künftige Änderungen am Push-Benachrichtigungskanal
audience: channels
feature: Push
role: Admin
level: Experienced
exl-id: e273b443-7c43-482b-8f86-60ada4b57cbf
source-git-commit: ac4a52263482557a6d5c370af6df5d54a42671b4
workflow-type: ht
source-wordcount: '338'
ht-degree: 100%

---

# Künftige Änderungen am Push-Benachrichtigungskanal {#push-upgrade}

Sie können Campaign verwenden, um Push-Benachrichtigungen an Android- und iOS-Geräte zu senden. Dazu benötigt Campaign bestimmte Abonnementdienste. Mit der Winterversion 24.1 2024 werden einige wichtige Änderungen am FCM-Dienst (Android Firebase Cloud Messaging) veröffentlicht, die sich auf Ihre Implementierung von Adobe Campaign auswirken werden. Darüber hinaus ändert Adobe bei iOS-Apps die Art und Weise, wie Administratoren Zertifikate konfigurieren können.

## Was hat sich geändert? {#push-changes}

### Android {#push-android}

Im Rahmen der kontinuierlichen Bemühungen von Google, seine Dienste zu verbessern, werden die veralteten FCM-APIs am **20. Juni 2024** eingestellt. Weitere Informationen zum HTTP-Protokoll von Firebase Cloud Messaging finden Sie in der [Google Firebase-Dokumentation](https://firebase.google.com/docs/cloud-messaging/http-server-ref){target="_blank"}.

Derzeit verwendet Adobe Campaign Standard ältere HTTP-APIs, um Android-Push-Benachrichtigungen zu senden, und wird in den kommenden Monaten Änderungen vornehmen, um auf die HTTP v1-APIs zu aktualisieren.

### iOS {#push-ios}

Adobe aktualisiert außerdem Adobe Campaign Standard für den iOS-Kanal für Push-Benachrichtigungen und ändert die Art und Weise, wie Admins Zertifikate für ihre iOS-Anwendungen konfigurieren können. Ab der Winterversion 24.2 2024 müssen Admins die iOS-Zertifikate über die Benutzeroberfläche von Adobe Campaign Standard in den Eigenschaften Ihrer Mobile App hochladen.

## Sind Sie betroffen? {#push-impact}

Sie sind davon betroffen, wenn Sie als Benutzerin oder Benutzer von Campaign Standard Push-Benachrichtigungen an Ihre Zielgruppen senden.

## Wie wird die Migration durchgeführt? {#push-migration}

Diese Updates erfordern eine Aktualisierung des Campaign Standard-Builds auf die Winterversion 24.1.2024, da sie sich auf die mobile Kanalkonfiguration und Berechtigungsverwaltung auswirken.

In Kürze werden detaillierte Anweisungen bereitgestellt, um einen reibungslosen Übergangsprozess zu erleichtern.

Unser Support-Team steht Ihnen während des gesamten Übergangszeitraums zur Verfügung. Unter Umständen werden wir auch Webinare und Aktivierungssitzungen veranstalten, um die technischen Aspekte und Best Practices für die Umstellung abzudecken.

Wir empfehlen Ihnen in der Zwischenzeit Ihre aktuelle Konfiguration und Anpassung in Adobe Campaign Standard zu überprüfen, damit Sie vorbereitet sind, bei Bedarf Änderungen vornehmen zu können.

Wenn Sie Fragen oder Anliegen haben, wenden Sie sich bitte an unseren Support.

---
title: Campaign-Dynamics-Integrationsanwendung konfigurieren
description: Erfahren Sie, wie Sie die Campaign-Dynamics-Integrationsanwendung konfigurieren.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
feature: Microsoft CRM Integration
role: Data Architect
level: Intermediate
exl-id: e0fb289a-6b6e-473d-80af-50f6d0d72af1
source-git-commit: abdcd3f9f7f709818dee794b4c830e486fefa290
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 100%

---

# Migrieren von Anmeldedaten von JWT zu OAuth-Server-zu-Server

Die Anmeldedaten für Service-Konten (JWT) wurden zugunsten der neuen OAuth-Server-zu-Server-Anmeldedaten eingestellt. Die neuen Anmeldedaten erleichtern die Wartung von Adobe-Anwendungen. Außerdem entfällt die Notwendigkeit, Zertifikate regelmäßig zu rotieren, und es funktioniert sofort mit standardmäßigen OAuth2-Bibliotheken.

Die Anmeldedaten für das Service-Konto (JWT) wurden zwar als veraltet markiert, funktionieren jedoch bis zum 1. Januar 2025 weiterhin. Daher müssen Sie Ihre Integration migrieren, um die neue OAuth-Server-zu-Server-Anmeldedaten vor dem 1. Januar 2025 zu verwenden. Weitere Informationen sind unter [Einstellungszeitpläne](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/#deperecation-timelines) zu finden.

## Schritte zum Migrieren von Anmeldedaten von JWT zu OAuth-Server-zu-Server

Die Migration zu OAuth-Server-zu-Server-Anmeldedaten ist ein einfacher Prozess, der eine Migration ohne Ausfallzeiten für Ihre Anwendung ermöglicht. Sie können die folgenden Schritte ausführen, um die Anmeldedaten zu migrieren.

1. Anmelden bei der [Adobe Developer-Konsole](https://developer.adobe.com/console)
2. Wählen Sie im Filtermenü auf der linken Seite die Option „Hat Anmeldedaten von Service-Konto (JWT)“. Auf diese Weise werden alle Projekte angezeigt, die über eine Service-Konto(JWT)-Anmeldedaten verfügen. Klicken Sie in der Projektliste auf das Projekt, das Sie migrieren möchten.

   ![](assets/JwtToOAuthMigration1.png)

3. Öffnen Sie die Registerkarte für die Service-Konto(JWT)-Anmeldedaten in der linken Navigationsleiste und zeigen Sie die Migrationskarte an. Klicken Sie auf der Migrationskarte auf die Schaltfläche **Neue Anmeldedaten hinzufügen**, um entsprechende OAuth-Server-zu-Server-Anmeldedaten hinzuzufügen. Durch Hinzufügen von OAuth-Server-zu-Server-Anmeldedaten zu Ihrem Projekt wird die Migration gestartet.
   ![](assets/JwtToOAuthMigration2.png)
4. Die neuen Anmeldedaten von **OAuth-Server-zu-Server** werden zur linken Seitennavigation hinzugefügt.
   * Klicken Sie auf „Migration abbrechen“, wenn Sie die Migration abbrechen möchten.
   * Klicken Sie erst auf die Schaltfläche „Überprüfen und löschen“, wenn Sie sichergestellt haben, dass die neuen OAuth-Server-to-Server-Anmeldedaten funktionieren.
     ![](assets/JwtToOAuthMigration3.png)

5. Aktualisieren der Anmeldedaten in Microsoft Dynamics 365 auf die Adobe Campaign Standard-App
   * Melden Sie sich bei der Integrations-App an und navigieren Sie zur Seite „Einstellungen“.
   * Wählen Sie OAuth als Authentifizierungstyp aus.
   * Da die neuen OAuth-Server-zu-Server-Anmeldedaten dieselben Anmeldedaten wie die alten Service-Konto(JWT)-Anmeldedaten verwenden, sind die meisten Felder bereits ausgefüllt.
   * Geben Sie die Client-ID und das Client-Geheimnis ein. Diese finden Sie im Projekt in der Adobe Developer Console.
   * Klicken Sie auf „Speichern“, um die Einstellungen zu speichern.
     ![](assets/JwtToOAuthMigration4.png)

6. Überprüfen Sie, ob die neuen Anmeldedaten funktionieren.
   * Melden Sie sich bei der Integrations-App an und navigieren Sie zur Seite „Workflows“.
   * Stoppen Sie die aktiven Workflows. Warten Sie, bis die Workflows angehalten wurden.
   * Starten Sie die Workflows. Warten Sie, bis sich die Workflows im Status WIRD AUSGEFÜHRT befinden.
   * Überwachen Sie die Workflows einige Minuten, um sicherzustellen, dass die Workflows ordnungsgemäß funktionieren. Sie können auch die Daten in Adobe Campaign Standard und Microsoft Dynamics 365 überprüfen, um sicherzustellen, dass die Daten korrekt synchronisiert werden.

7. Löschen Sie die JWT-Anmeldedaten, um die Migration abzuschließen.
   * Melden Sie sich bei der [Adobe Developer Console](https://developer.adobe.com/console) an.
   * Klicken Sie auf die Projekte und wählen Sie das soeben migrierte Projekt aus.
   * Klicken Sie in der linken Navigationsleiste auf die Registerkarte für die Service-Konto(JWT)-Anmeldedaten.
   * Klicken Sie auf die Schaltfläche „Überprüfen und löschen“.
     ![](assets/JwtToOAuthMigration5.png)
   * Überprüfen Sie den Zeitstempel des letzten Zugriffs oder des zuletzt verwendeten Menüs, um zu überprüfen, ob die Integrationsanwendung Zugriffstoken mit den neuen OAuth-Anmeldedaten generiert oder weiterhin die alten JWT-Anmeldedaten verwendet.
     ![](assets/JwtToOAuthMigration6.png)
   * Nachdem sichergestellt ist, dass die Integrations-App die neuen OAuth-Anmeldedaten und keine JWT-Anmeldedaten mehr verwendet, fahren Sie mit dem Löschen der alten Anmeldedaten fort, indem Sie auf die Schaltfläche **Bestätigen und fortfahren** klicken und damit die Migration abzuschließen.
     ![](assets/JwtToOAuthMigration7.png)

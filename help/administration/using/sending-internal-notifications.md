---
title: Interne Benachrichtigungen senden
seo-title: Interne Benachrichtigungen senden
description: Interne Benachrichtigungen senden
seo-description: Erfahren Sie, wie Sie Adobe Campaign-Benutzern in Echtzeit Systembenachrichtigungen senden können.
page-status-flag: nie aktiviert
uuid: f 196 f 025-dbb 9-4268-9 d 7 d-ff 626994 b 447
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Administration
content-type: Referenz
topic-tags: application-settings
discoiquuid: 4 d 51229 a -745 a -4 f 24-b 1 c 2-22 fa 203 b 499 c
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6a877d878f01fa1e541dc20b8b0941602113d15b

---


# Interne Benachrichtigungen senden{#sending-internal-notifications}

Adobe Campaign ermöglicht es Ihnen, Benachrichtigungen zu wichtigen Systemaktivitäten direkt in der Anwendung zu empfangen. Echtzeit-Benachrichtigungen informieren die jeweiligen Interessengruppen und ermöglichen es Benutzern, unverzüglich und direkt auf Aktivitätsbenachrichtigungen innerhalb der Anwendung zu reagieren. Teams profitieren dadurch von verbesserter Agilität und Effizienz sowie von einer reibungslosen Ausführung der Kampagnen.

![](assets/pulse_3.png)

Für die folgenden Objekte können Benachrichtigungen konfiguriert werden:

* **[!UICONTROL A/B-Test-E-Mails]**: Verfasser und Bearbeiter einer E-Mail werden benachrichtigt, dass eine Variante ausgewählt wurde (automatischer Modus) oder dass eine Variante ausgewählt werden muss (manueller Modus). Durch Anklicken der Benachrichtigung wird die entsprechende E-Mail angezeigt. Die Benachrichtigungsfunktion ist in der vordefinierten A/B-Test-Vorlage standardmäßig aktiviert. Um sie zu deaktivieren, bearbeiten Sie die Eigenschaften der E-Mail oder der E-Mail-Vorlage und deaktivieren Sie die Option unter **Allgemein &gt; Benachrichtigungen**. Weiterführende Informationen zu A/B-Test-E-Mails finden Sie in Abschnitt [A/B-Tests erstellen](../../channels/using/designing-an-a-b-test-email.md). Lesen Sie zu E-Mail-Eigenschaften auch den Abschnitt [Liste der E-Mail-Eigenschaften](../../administration/using/configuring-email-channel.md#list-of-email-properties).

   ![](assets/pulse_2.png)

* **[!UICONTROL Workflows]**: Jedes Mitglied der ausgewählten Sicherheitsgruppe wird benachrichtigt (E-Mail und In-App-Benachrichtigung), wenn ein Workflow fehlerhaft ist. Durch Anklicken der Benachrichtigung oder des E-Mail-Links wird der entsprechende Workflow angezeigt. Die Benachrichtigungsfunktion ist standardmäßig in der vordefinierten Workflow-Vorlage deaktiviert. Um sie zu aktivieren, bearbeiten Sie die Eigenschaften des Workflows oder der Workflow-Vorlage und fügen Sie eine Sicherheitsgruppe über **Allgemein &gt; Ausführung &gt; Umgang mit Fehlern &gt; Supervisoren** hinzu. Weiterführende Informationen zu Sicherheitsgruppen finden Sie unter [Gruppen und Benutzer verwalten](../../administration/using/managing-groups-and-users.md). Weiterführende Informationen zu Workflow-Eigenschaften finden Sie auch in Abschnitt [Eigenschaften des Workflows](../../automating/using/executing-a-workflow.md#workflow-properties).

   ![](assets/pulse_1.png)


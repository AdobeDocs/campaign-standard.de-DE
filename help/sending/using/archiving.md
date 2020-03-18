---
title: Archivieren von Nachrichten in Adobe Campaign Standard
description: Erfahren Sie, wie Sie E-Mails mit Adobe Campaign Standard mithilfe einer BCC-E-Mail-Adresse archivieren.
page-status-flag: never-activated
uuid: c3721647-0663-4614-a9c9-3b3a40af328a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages
discoiquuid: 6fa50f0d-3dcf-4a9e-bccc-1ecda2bfb449
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 2bf1f8acb581645a6f89f50443a8d9a49d8acaf1

---


# Archivierung mit E-Mail-BCC{#archiving-emails}

Sie können Adobe Campaign so konfigurieren, dass eine Kopie der E-Mails, die über E-Mail-BCC von Ihrer Plattform gesendet werden, erhalten bleibt.

Wenn Ihr Unternehmen alle ausgehenden E-Mail-Nachrichten zur Einhaltung der Vorschriften archivieren muss, können Sie diese Funktion aktivieren. Es ermöglicht Ihnen, eine exakte, versteckte Kopie der gesendeten Nachrichten an eine BCC-E-Mail-Adresse (die für die Empfänger des Versands unsichtbar ist) zu senden, die Sie angeben müssen.

Nach der Aktivierung müssen Sie E-Mail-BCC über die **[!UICONTROL Archive emails]** Option in der E-Mail-Versandvorlage aktivieren.

>[!NOTE]
>
>Adobe Campaign selbst verwaltet keine archivierten Dateien. Sie können aber die gewünschten Nachrichten an eine bestimmte Adresse senden, wo sie mithilfe eines externen Systems verarbeitet und archiviert werden.

## Empfehlungen und Einschränkungen   {#recommendations-and-limitations}

* Hierbei handelt es sich um eine optionale Funktion. Bitte prüfen Sie Ihren Lizenzvertrag und kontaktieren Sie den Ansprechpartner für Ihr Konto, um diese Funktion zu aktivieren.
* Die BCC-Adresse Ihrer Wahl muss dem Adobe-Team zur Verfügung gestellt werden, das sie für Sie konfiguriert.
* Sie können nur eine einzige BCC-E-Mail-Adresse verwenden.
* Nur erfolgreich gesendete E-Mails werden berücksichtigt. Bounces werden nicht berücksichtigt.
* Aus Datenschutzgründen müssen BCC-E-Mails von einem Archivierungssystem bearbeitet werden, in dem personenbezogene Daten (PII, Personally Identifiable Information) sicher aufbewahrt werden.
* Bei der Erstellung einer neuen Versandvorlage ist E-Mail-BCC nicht standardmäßig aktiviert, selbst wenn diese Option erworben wurde. Sie muss manuell in jeder Versandvorlage aktiviert werden, in der sie verwendet werden soll.

>[!NOTE]
>
>Derzeit können die archivierten E-Mails nicht mit der [Adobe Campaign Enhanced MTA](https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html)gesendet werden, selbst wenn Sie bereits auf die erweiterte MTA aktualisiert wurden.

## E-Mail-Archivierung aktivieren   {#activating-email-archiving}

Once enabled, Email BCC is activated in the [email template](../../start/using/marketing-activity-templates.md), through a dedicated option:

1. Gehen Sie in den Knoten **Ressourcen** > **Vorlagen** > **Versandvorlagen**.
1. Duplikat der vordefinierten **[!UICONTROL Send via email]** Vorlage.
1. Wählen Sie die duplizierte Vorlage aus.
1. Click the **[!UICONTROL Edit properties]** button to edit the template&#39;s properties.
1. Erweitern Sie den **[!UICONTROL Send]** Abschnitt.
1. Check the **[!UICONTROL Archive emails]** box to keep a copy of all sent messages for each delivery based on this template.

   ![](assets/email_archiving.png)

>[!NOTE]
>
>If the emails sent to the BCC address are opened and clicked through, this will be taken into account in the **[!UICONTROL Total opens]** and **[!UICONTROL Clicks]** from the send analysis, which could cause some miscalculations.
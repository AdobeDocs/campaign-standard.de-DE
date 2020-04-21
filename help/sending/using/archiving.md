---
title: Archivieren von Nachrichten in Adobe Campaign Standard
description: Erfahren Sie, wie Sie E-Mails mit Adobe Campaign Standard unter Verwendung einer BCC-E-Mail-Adresse archivieren können.
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
source-git-commit: 72366d56e21933bcd79e907e5f8d5a9ad5281725

---


# Archivieren mit E-Mail-BCC{#archiving-emails}

Sie können Adobe Campaign so konfigurieren, dass von E­Mails, die von der Plattform per E-Mail-BCC gesendet werden, eine Kopie beibehalten wird.

Wenn Ihr Unternehmen aus Compliance-Gründen alle ausgehenden E-Mail-Nachrichten archivieren muss, können Sie diese Funktion aktivieren. So können Sie eine genaue, versteckte Kopie der jeweiligen gesendeten Nachrichten an eine BCC-E-Mail-Adresse (die für die Empfänger des Versands unsichtbar ist) senden, die von Ihnen angegeben werden muss.

Once enabled, you need to activate Email BCC from the **[!UICONTROL Archive emails]** option in the email delivery template.

>[!NOTE]
>
>Adobe Campaign selbst ermöglicht keine Verwaltung von archivierten Dateien. Sie können aber die gewünschten Nachrichten an eine bestimmte Adresse senden, wo sie mithilfe eines externen Systems verarbeitet und archiviert werden.

## Empfehlungen und Einschränkungen     {#recommendations-and-limitations}

* Hierbei handelt es sich um eine optionale Funktion. Bitte prüfen Sie Ihren Lizenzvertrag und kontaktieren Sie den Ansprechpartner für Ihr Konto, um diese Funktion zu aktivieren.
* Die gewünschte BCC-Adresse muss dem Adobe-Team übermittelt werden, das die Adresse für Sie konfigurieren wird.
* Sie können nur eine einzige BCC-E-Mail-Adresse verwenden.
* Nur erfolgreich gesendete E-Mails werden berücksichtigt. Bounces werden nicht berücksichtigt.
* Aus Datenschutzgründen müssen BCC-E-Mails von einem Archivierungssystem bearbeitet werden, in dem personenbezogene Daten (PII, Personally Identifiable Information) sicher aufbewahrt werden.
* Bei der Erstellung einer neuen Versandvorlage ist E-Mail-BCC nicht standardmäßig aktiviert, selbst wenn diese Option erworben wurde. Sie muss manuell in jeder Versandvorlage aktiviert werden, in der sie verwendet werden soll.

>[!NOTE]
>
>Aktuell können die archivierten E-Mails nicht mit dem erweiterten MTA von Adobe Campaign gesendet werden, selbst wenn Sie bereits eine Aktualisierung auf den erweiterten MTA vorgenommen haben.

## E-Mail-Archivierung aktivieren     {#activating-email-archiving}

Nach der Aktivierung wird E-Mail-BCC in der [E-Mail-Vorlage](../../start/using/marketing-activity-templates.md) über die folgende Option aktiviert:

1. Rufen Sie den Knoten **Ressourcen** > **Vorlagen** > **Versandvorlagen** auf.
1. Duplikat der vordefinierten **[!UICONTROL Send via email]** Vorlage.
1. Wählen Sie die duplizierte Vorlage aus.
1. Click the **[!UICONTROL Edit properties]** button to edit the template&#39;s properties.
1. Erweitern Sie den **[!UICONTROL Send]** Abschnitt.
1. Check the **[!UICONTROL Archive emails]** box to keep a copy of all sent messages for each delivery based on this template.

   ![](assets/email_archiving.png)

>[!NOTE]
>
>If the emails sent to the BCC address are opened and clicked through, this will be taken into account in the **[!UICONTROL Total opens]** and **[!UICONTROL Clicks]** from the send analysis, which could cause some miscalculations.
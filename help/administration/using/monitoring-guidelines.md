---
solution: Campaign Standard
product: campaign
title: Richtlinien für das Monitoring
description: Dieser Abschnitt enthält allgemeine Richtlinien für die Überwachung von Campaign Standard.
audience: production
content-type: reference
topic-tags: introduction
index: y
translation-type: tm+mt
source-git-commit: 4b87ebc2585b87f918bbd688c5858394d8d4a742
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 74%

---


# Richtlinien für das Monitoring {#monitoring-guidelines}

<table>
<tr><td><img src="assets/do-not-localize/icon_system.svg" width="60px"><p><a href="#monitoring-system">Überwachen des Systems</a></p></td>
<td><img src="assets/do-not-localize/icon_workflows.svg" width="60px"><p><a href="#moniroting-workflows">Überwachung von Workflows</a></p></td>
<td><img src="assets/do-not-localize/icon_send.svg" width="60px"><p><a href="#monitoring-deliveries">Sendungen überwachen</a></p></td></tr>
</table>

Campaign Standard bietet verschiedene Möglichkeiten zur Überwachung Ihrer Instanzen, um sicherzustellen, dass Ihr System fehlerfrei ist, und schließlich Probleme zu beheben, die beim Einrichten von Workflows, beim Ausführen von Sendungen usw. auftreten können.

## Überwachen des Systems {#monitoring-system}

<img src="assets/do-not-localize/icon_system.svg" width="60px">

**Systembenachrichtigungen**
Die Benutzeroberfläche von Campaign Standard verfügt über einen Benachrichtigungsbereich, der Sie über die Vorgänge im System auf dem Laufenden hält: Ereignisstatus, Systemaktualisierungen, erforderliche Aktionen usw. [Mehr dazu](../../start/using/interface-description.md#top-bar)


**Technische Workflows**
Technische Workflows dienen der programmierten periodischen Ausführung von Server-Vorgängen. Um sicherzustellen, dass Ihre Instanz fehlerfrei ist und ordnungsgemäß funktioniert, müssen Sie sicherstellen, dass sie immer betriebsbereit ist. [Mehr dazu](../../administration/using/technical-workflows.md)

**Control Panel**
Das Control Panel erlaubt Ihnen, verschiedene Einstellungen Ihrer Instanz zu verwalten: URL-Berechtigungen, Überprüfung Ihrer Instanzdetails wie die Build-Versionen Ihrer Server, Überwachung der Nutzung aktiver Profile usw. Das Control Panel ermöglicht Ihnen auch, den verfügbaren Speicherplatz auf den SFTP-Servern zu überwachen, die mit Ihrer Instanz verbunden sind. [Mehr dazu](https://docs.adobe.com/content/help/de-DE/control-panel/using/control-panel-home.html)

>[!NOTE]
>
>Bitte beachten Sie, dass das Control Panel nur für Admin-Benutzer zugänglich ist und für alle Kunden zur Verfügung steht, die Adobe Managed Services nutzen.

**Technische Objekte**
Das Menü **[!UICONTROL Diagnose]** ist ein wichtiges Werkzeug zur Überwachung und Analyse der verschiedenen technischen Objekte, die von der Anwendung generiert werden: Datenschemata, Web-Seiten, Batch-Vorgänge usw. [Mehr dazu](../../developing/using/monitoring-data-model-changes.md)

**Export-Audits**
Export-Audits ermöglichen es Ihnen, die auf Ihren Instanzen durchgeführten Exporte zu überwachen: Dateien, die von Workflows hochgeladen wurden, Listenexporte und Dateien, die von Briefpost-Nachrichten heruntergeladen wurden.
[Mehr dazu](../../administration/using/auditing-export-logs.md)

****
LizenzenÜberwachen Sie im Menü &quot; **** Lizenzen&quot;Informationen zu Ihren Instanzen: installierte Lizenzen, Buildversionen und Vertragsabschlüsse akzeptiert.
[Mehr dazu](../../administration/using/licenses.md)

## Überwachung von Workflows {#monitoring-workflows}

<img src="assets/do-not-localize/icon_workflows.svg" width="60px">

**Best Practices und Fehlerbehebung**
Die Befolgung von Best Practices und Richtlinien zur Fehlerbehebung bei der Verwendung von Workflows kann zur Leistungsverbesserung beitragen.
[Mehr dazu](../../automating/using/best-practices-workflows.md)

**Protokolle und**
AufgabenDie Überwachung von Workflow-Protokollen ist ein wichtiger Schritt zur Analyse Ihrer Workflows und zur Gewährleistung ihrer ordnungsgemäßen Ausführung.
[Mehr dazu](../../automating/using/monitoring-workflow-execution.md#workflow-log-and-tasks)

**Mit**
NotificationsCampaign Standard können Sie Benachrichtigungen an Aufsichtsbehörden senden, um die Ausführung Ihrer Workflows zu überwachen und festzustellen, ob ein Fehler vorliegt, der Ihre Aufmerksamkeit erfordert.
[Mehr dazu](../../automating/using/monitoring-workflow-execution.md#error-management)

## Sendungen überwachen {#monitoring-deliveries}

<img src="assets/do-not-localize/icon_send.svg" width="60px">

****
DeliverabilityCampaign Standard bietet mehrere Bereitstellungs-Tools, mit deren Hilfe Sie die Anzahl der erfolgreich ausgelieferten Nachrichten verbessern können: Berichte zum Durchsatz von Versänden, Optimierung der Sendezeit, Vorschau von Nachrichten, E-Mail-Rendering, Verwaltung von Quarantänen usw.
[Mehr dazu](../../sending/using/about-deliverability.md)

**Sendungen**
Sobald Ihre Nachrichten gesendet wurden, können Sie mithilfe detaillierter Protokolle die Sendungen überwachen, den Erfolg Ihrer Kampagne messen sowie das Verhalten der Empfänger verfolgen.
[Mehr dazu](../../sending/using/monitoring-a-delivery.md)

**Versandwarnung**
Mit der Funktion für Versandwarnungen können Sie Warnungen einrichten, die bezüglich der Ausführung von Sendungen automatisch an eine Gruppe von Benutzern gesendet werden: fehlgeschlagene Sendungen oder Vorbereitung, schlechte Bounce-Rate, niedriger Durchsatz usw.
[Mehr dazu](../../sending/using/receiving-alerts-when-failures-happen.md)

**Dynamische**
BerichterstellungDynamischer Berichte bietet verschiedene Berichte, die Ihnen helfen, über die Leistung Ihrer Versand auf dem Laufenden zu bleiben: Absprünge, am häufigsten angezeigte Versand nach Empfängern, Durchsatz der Versand usw.
[Mehr dazu](../../reporting/using/about-dynamic-reports.md)

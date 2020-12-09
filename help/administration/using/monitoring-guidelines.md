---
solution: Campaign Standard
product: campaign
title: Richtlinien für das Monitoring
description: Dieser Abschnitt enthält allgemeine Richtlinien für die Überwachung von Campaign Standard.
audience: production
content-type: reference
topic-tags: introduction
index: y
translation-type: ht
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: ht
source-wordcount: '498'
ht-degree: 100%

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

**Lizenzen**
Im Menü **[!UICONTROL Lizenzen]** können Sie Informationen zu Ihren Instanzen überwachen: installierte Lizenzen, Build-Versionen und akzeptierte Bestimmungen.
[Mehr dazu](../../administration/using/licenses.md)

## Überwachung von Workflows {#monitoring-workflows}

<img src="assets/do-not-localize/icon_workflows.svg" width="60px">

**Best Practices und Fehlerbehebung**
Die Befolgung von Best Practices und Richtlinien zur Fehlerbehebung bei der Verwendung von Workflows kann zur Leistungsverbesserung beitragen.
[Mehr dazu](../../automating/using/best-practices-workflows.md)

**Protokolle und Aufgaben**
Die Überwachung von Workflow-Protokollen ist ein wichtiger Schritt, um Ihre Workflows zu analysieren und sicherzustellen, dass sie ordnungsgemäß ausgeführt werden.
[Mehr dazu](../../automating/using/monitoring-workflow-execution.md#workflow-log-and-tasks)

**Benachrichtigungen**
Mit Campaign Standard können Sie Benachrichtigungen an Supervisoren senden, um die Ausführung Ihrer Workflows zu überwachen und festzustellen, ob ein Fehler vorliegt, der Ihre Aufmerksamkeit erfordert.
[Mehr dazu](../../automating/using/monitoring-workflow-execution.md#error-management)

## Sendungen überwachen {#monitoring-deliveries}

<img src="assets/do-not-localize/icon_send.svg" width="60px">

**Zustellbarkeit**
Campaign Standard bietet verschiedene Zustellbarkeits-Tools, mit denen Sie die Anzahl der erfolgreich zugestellten Nachrichten verbessern können: Berichte zum Versanddurchsatz, Optimierung der Sendungsdauer, Vorschau von Nachrichten, E-Mail-Rendering, Quarantäneverwaltung usw.
[Mehr dazu](../../sending/using/about-deliverability.md)

**Sendungen**
Sobald Ihre Nachrichten gesendet wurden, können Sie mithilfe detaillierter Protokolle die Sendungen überwachen, den Erfolg Ihrer Kampagne messen sowie das Verhalten der Empfänger verfolgen.
[Mehr dazu](../../sending/using/monitoring-a-delivery.md)

**Versandwarnung**
Mit der Funktion für Versandwarnungen können Sie Warnungen einrichten, die bezüglich der Ausführung von Sendungen automatisch an eine Gruppe von Benutzern gesendet werden: fehlgeschlagene Sendungen oder Vorbereitung, schlechte Bounce-Rate, niedriger Durchsatz usw.
[Mehr dazu](../../sending/using/receiving-alerts-when-failures-happen.md)

**Dynamische Berichterstellung**
Die dynamische Berichterstellung bietet verschiedene Berichte, mit denen Sie über die Leistung Ihrer Sendungen auf dem Laufenden gehalten werden können: Bounces, die von den Empfängern am häufigsten angesehenen Sendungen, der Durchsatz der Sendungen usw.
[Mehr dazu](../../reporting/using/about-dynamic-reports.md)

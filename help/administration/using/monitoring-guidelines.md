---
title: Richtlinien für das Monitoring
description: Diese Seite enthält allgemeine Richtlinien für das Überwachen von Campaign Standard
audience: production
feature: Access Management
role: Admin
level: Experienced
exl-id: 5f25f2b2-ca41-4baf-ade2-42bbafb4790d
source-git-commit: 6530ca1726a2aff18c5be9566d8008c317918e64
workflow-type: ht
source-wordcount: '493'
ht-degree: 100%

---

# Richtlinien für das Monitoring {#monitoring-guidelines}

<table>
<tr><td><img src="assets/do-not-localize/icon_system.svg" width="60px"><p><a href="#monitoring-system">Überwachen des Systems</a></p></td>
<td><img src="assets/do-not-localize/icon_workflows.svg" width="60px"><p><a href="#moniroting-workflows">Überwachung von Workflows</a></p></td>
<td><img src="assets/do-not-localize/icon_send.svg" width="60px"><p><a href="#monitoring-deliveries">Überwachen von Sendungen</a></p></td></tr>
</table>

Campaign Standard bietet verschiedene Möglichkeiten zur Überwachung Ihrer Instanzen, um sicherzustellen, dass Ihr System fehlerfrei ist, und schließlich Probleme zu beheben, die beim Einrichten von Workflows, beim Ausführen von Sendungen usw. auftreten können.

## Überwachen des Systems {#monitoring-system}

<img src="assets/do-not-localize/icon_system.svg" width="60px">

**Systembenachrichtigungen**

Die Benutzeroberfläche von Campaign Standard verfügt über einen Benachrichtigungsbereich, der Sie über die Vorgänge im System auf dem Laufenden hält: Ereignisstatus, Systemaktualisierungen, erforderliche Aktionen usw. [Weitere Informationen](../../start/using/interface-description.md#top-bar)


**Technische Workflows**

Technische Workflows dienen der programmierten periodischen Ausführung von Server-Aufträgen. Um sicherzustellen, dass Ihre Instanz fehlerfrei ist und ordnungsgemäß funktioniert, müssen Sie sicherstellen, dass sie immer betriebsbereit ist. [Weitere Informationen](../../administration/using/technical-workflows.md)

**Control Panel**

Das Control Panel erlaubt Ihnen, verschiedene Einstellungen Ihrer Instanz zu verwalten: URL-Berechtigungen, Überprüfung Ihrer Instanzdetails wie die Build-Versionen Ihrer Server, Überwachung der Nutzung aktiver Profile usw. Das Control Panel ermöglicht Ihnen auch, den verfügbaren Speicherplatz auf den SFTP-Servern zu überwachen, die mit Ihrer Instanz verbunden sind. [Weitere Informationen](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=de)

>[!NOTE]
>
>Das Control Panel steht allen Administratoren zur Verfügung. Die Schritte, um einem Benutzer Administratorzugriff zu gewähren, finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=de#discover-control-panel).

**Technische Objekte**

Das Menü **[!UICONTROL Diagnose]** ist ein wichtiges Werkzeug zur Überwachung und Analyse der verschiedenen technischen Objekte, die von der Anwendung generiert werden: Datenschemata, Web-Seiten, Batch-Aufträge usw. [Weitere Informationen](../../developing/using/monitoring-data-model-changes.md)

**Export-Audits**

Export-Audits ermöglichen es Ihnen, die auf Ihren Instanzen durchgeführten Exporte zu überwachen: Dateien, die von Workflows hochgeladen wurden, Listenexporte und Dateien, die von Briefpost-Nachrichten heruntergeladen wurden.
[Weitere Informationen](../../administration/using/auditing-export-logs.md)

**Lizenzen**

Im Menü **[!UICONTROL Lizenzen]** können Sie Informationen zu Ihren Instanzen überwachen: installierte Lizenzen, Build-Versionen und akzeptierte Vertragsbestimmungen.
[Weitere Informationen](../../administration/using/licenses.md)

## Überwachung von Workflows {#monitoring-workflows}

<img src="assets/do-not-localize/icon_workflows.svg" width="60px">

**Best Practices und Fehlerbehebung**

Die Befolgung von Best Practices und Richtlinien zur Fehlerbehebung beim Verwenden von Workflows kann zur Performance-Verbesserung beitragen.
[Weitere Informationen](../../automating/using/best-practices-workflows.md)

**Protokolle und Aufgaben**

Die Überwachung von Workflow-Protokollen ist ein wichtiger Schritt, um Ihre Workflows zu analysieren und sicherzustellen, dass sie ordnungsgemäß ausgeführt werden.
[Weitere Informationen](../../automating/using/monitoring-workflow-execution.md#workflow-log-and-tasks)

**Benachrichtigungen**

Mit Campaign Standard können Sie Benachrichtigungen an Verantwortliche senden, um die Ausführung Ihrer Workflows zu überwachen und festzustellen, ob ein Fehler vorliegt, der Ihre Aufmerksamkeit erfordert.
[Weitere Informationen](../../automating/using/monitoring-workflow-execution.md#error-management)

## Überwachen von Sendungen {#monitoring-deliveries}

<img src="assets/do-not-localize/icon_send.svg" width="60px">

**Zustellbarkeit**

Campaign Standard bietet verschiedene Zustellbarkeits-Tools, mit denen Sie die Anzahl der erfolgreich zugestellten Nachrichten verbessern können: Berichte zum Versanddurchsatz, Optimierung des Sendezeitpunkts, Vorschau von Nachrichten, E-Mail-Rendering, Quarantäneverwaltung usw.
[Weitere Informationen](../../sending/using/about-deliverability.md)

**Sendungen**

Sobald Ihre Nachrichten gesendet wurden, können Sie mithilfe detaillierter Protokolle die Sendungen überwachen, den Erfolg Ihrer Kampagne messen sowie das Verhalten der Empfänger verfolgen.
[Weitere Informationen](../../sending/using/monitoring-a-delivery.md)

**Versandwarnungen**

Mit der Funktion für Versandwarnungen können Sie Warnungen einrichten, die bezüglich der Ausführung von Sendungen automatisch an eine Gruppe von Benutzern gesendet werden: fehlgeschlagenes Senden/Vorbereiten, schlechte Bounce-Rate, niedriger Durchsatz usw.
[Weitere Informationen](../../sending/using/receiving-alerts-when-failures-happen.md)

**Dynamische Berichterstellung**

Die dynamische Berichterstellung bietet verschiedene Reports, mit denen Sie sich über die Leistung Ihrer Sendungen auf dem Laufenden halten können: Bounces, die von den Empfängern am häufigsten angesehenen Sendungen, der Durchsatz der Sendungen usw.
[Weitere Informationen](../../reporting/using/about-dynamic-reports.md)

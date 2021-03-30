---
solution: Campaign Standard
product: campaign
title: Richtlinien für das Monitoring
description: Dieser Abschnitt enthält allgemeine Richtlinien für die Überwachung von Campaign Standard.
audience: production
content-type: reference
topic-tags: introduction
index: y
feature: Zugriffsverwaltung
role: Administrator
level: Erfahren
translation-type: tm+mt
source-git-commit: 7979d8fd88b93a1cdd7b5a11bb66e894ab12f1c2
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 38%

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

Die Benutzeroberfläche von Campaign Standard bietet einen Benachrichtigungsbereich, in dem Sie über die Vorgänge im System auf dem Laufenden gehalten werden können: Status von Ereignissen, Systemaktualisierungen, erforderliche Aktionen usw. [Mehr dazu](../../start/using/interface-description.md#top-bar)


**Technische Workflows**

Technische Workflows dienen der programmierten periodischen Ausführung von Server-Vorgängen. Um sicherzustellen, dass Ihre Instanz fehlerfrei ist und ordnungsgemäß funktioniert, müssen Sie sicherstellen, dass sie immer betriebsbereit ist. [Mehr dazu](../../administration/using/technical-workflows.md)

**Control Panel**

Das Control Panel erlaubt Ihnen, verschiedene Einstellungen Ihrer Instanz zu verwalten: URL-Berechtigungen, Überprüfung Ihrer Instanzdetails wie die Build-Versionen Ihrer Server, Überwachung der Nutzung aktiver Profile usw. Das Control Panel ermöglicht Ihnen auch, den verfügbaren Speicherplatz auf den SFTP-Servern zu überwachen, die mit Ihrer Instanz verbunden sind. [Mehr dazu](https://docs.adobe.com/content/help/de-DE/control-panel/using/control-panel-home.html)

>[!NOTE]
>
>Die Systemsteuerung steht allen Administratoren zur Verfügung. Die Schritte zum Gewähren des Administratorzugriffs für einen Benutzer sind in [dieser Seite](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=en#discover-control-panel) beschrieben.

**Technische Objekte**

Das Menü **[!UICONTROL Diagnose]** ist ein wichtiges Tool zur Überwachung und Analyse der verschiedenen technischen Objekte, die von der Anwendung generiert wurden: Schema, Webseiten, Stapelaufträge usw. [Mehr dazu](../../developing/using/monitoring-data-model-changes.md)

**Export-Audits**

Mit Exportprüfungen können Sie die Exporte überwachen, die an Ihren Instanzen ausgeführt werden: Dateien, die aus Workflows, Listen exportiert und aus Direktnachrichten heruntergeladen wurden.
[Mehr dazu](../../administration/using/auditing-export-logs.md)

**Lizenzen**

Überwachen Sie mithilfe des Menüs **[!UICONTROL Lizenzen]** Informationen zu Ihren Instanzen: installierte Lizenzen, Buildversionen und Vertragsabschlüsse akzeptiert.
[Mehr dazu](../../administration/using/licenses.md)

## Überwachung von Workflows {#monitoring-workflows}

<img src="assets/do-not-localize/icon_workflows.svg" width="60px">

**Best Practices und Fehlerbehebung**

Die Einhaltung bewährter Verfahren und Richtlinien zur Fehlerbehebung bei der Verwendung von Workflows können dabei helfen, die Leistung zu verbessern.
[Mehr dazu](../../automating/using/best-practices-workflows.md)

**Protokolle und Aufgaben**

Die Überwachung von Workflow-Protokollen ist ein wichtiger Schritt, um Ihre Workflows zu analysieren und sicherzustellen, dass sie ordnungsgemäß ausgeführt werden.
[Mehr dazu](../../automating/using/monitoring-workflow-execution.md#workflow-log-and-tasks)

**Benachrichtigungen**

Campaign Standard ermöglicht es Ihnen, Benachrichtigungen an die Aufsichtsbehörden zu senden, um die Ausführung Ihrer Workflows zu überwachen und festzustellen, ob ein Fehler vorliegt, der Ihre Aufmerksamkeit erfordert.
[Mehr dazu](../../automating/using/monitoring-workflow-execution.md#error-management)

## Sendungen überwachen {#monitoring-deliveries}

<img src="assets/do-not-localize/icon_send.svg" width="60px">

**Zustellbarkeit**

Campaign Standard bietet mehrere Bereitstellungs-Tools, mit denen Sie die Anzahl der erfolgreich ausgelieferten Nachrichten verbessern können: Berichte zum Durchsatz von Versänden, Optimierung der Sendezeit, Vorschau von Nachrichten, E-Mail-Rendering, Verwaltung von Quarantänen usw.
[Mehr dazu](../../sending/using/about-deliverability.md)

**Sendungen**

Sobald Ihre Nachrichten gesendet wurden, können Sie mit detaillierten Protokollen die Versand überwachen und den Erfolg Ihrer Kampagne messen sowie das Verhalten der Empfänger nachverfolgen.
[Mehr dazu](../../sending/using/monitoring-a-delivery.md)

**Versandwarnung**

Mit der Versand-Warnfunktion können Sie Warnungen einrichten, die automatisch an eine Benutzergruppe zur Ausführung von Versänden gesendet werden: fehlgeschlagenes Senden oder Aufbereiten, schlechtes Absprungverhältnis, niedriger Durchsatz usw.
[Mehr dazu](../../sending/using/receiving-alerts-when-failures-happen.md)

**Dynamische Berichterstellung**

Der dynamische Berichte bietet verschiedene Berichte, die Ihnen helfen, über die Leistung Ihrer Versand auf dem Laufenden zu bleiben: Absprünge, am häufigsten angezeigte Versand nach Empfängern, Durchsatz der Versand usw.
[Mehr dazu](../../reporting/using/about-dynamic-reports.md)

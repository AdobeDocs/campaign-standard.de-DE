---
title: Richtlinien für das Monitoring
description: Dieser Abschnitt enthält allgemeine Leitlinien für die Überwachung der Campaign Standards.
page-status-flag: never-activated
uuid: cf0d782d-47bf-40ae-ab6f-d1d47fa15792
contentOwner: sauviat
products: SG_CAMPAIGN/CLASSIC
audience: production
content-type: reference
topic-tags: introduction
discoiquuid: 8b33e6af-15c3-4b30-8ad6-d76a1f33be21
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b4bac585ec25340d1f1d047f9a1f8dcd8e243821
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 9%

---


# Richtlinien für das Monitoring {#monitoring-guidelines}

<table>
<tr><td><img src="assets/do-not-localize/icon_system.svg" width="60px"><p><a href="#monitoring-system">Systemüberwachung</a></p></td>
<td><img src="assets/do-not-localize/icon_workflows.svg" width="60px"><p><a href="#moniroting-workflows">Überwachung von Workflows</a></p></td>
<td><img src="assets/do-not-localize/icon_send.svg" width="60px"><p><a href="#monitoring-deliveries">Sendungen beobachten</a></p></td></tr>
</table>

Campaign Standard bietet verschiedene Möglichkeiten zur Überwachung Ihrer Instanzen, um sicherzustellen, dass Ihr System einwandfrei ist, und eventuell Probleme zu beheben, die beim Einrichten von Workflows, Senden von Versänden usw. auftreten können.

## Systemüberwachung {#monitoring-system}

<img src="assets/do-not-localize/icon_system.svg" width="60px">

**Die Benutzeroberfläche für Systembenachrichtigungen** Campaign Standard bietet einen Benachrichtigungsbereich, über den Sie über die Vorgänge im System auf dem Laufenden gehalten werden können: Status von Ereignissen, Systemaktualisierungen, erforderliche Aktionen usw. [Mehr dazu](../../start/using/interface-description.md#top-bar)


**Technischen Workflows**-Technischen Workflows sind Vorgänge oder Aufträge, die regelmäßig auf dem Server ausgeführt werden sollen. Um sicherzustellen, dass Ihre Instanz gesund und ordnungsgemäß funktioniert, müssen Sie sicherstellen, dass sie immer betriebsbereit ist. [Mehr dazu](../../administration/using/technical-workflows.md)

**Control Panel** Mit dem Control Panel können Sie mehrere Einstellungen Ihrer Instanz verwalten: URL-Zugriffsberechtigungen, Überprüfen Sie die Instanzdetails wie die Build-Versionen Ihrer Server, überwachen Sie die Nutzung aktiver Profil usw. Außerdem können Sie damit den verfügbaren Speicherplatz auf den SFTP-Servern überwachen, die mit Ihrer Instanz verbunden sind. [Mehr dazu](https://docs.adobe.com/content/help/de-DE/control-panel/using/control-panel-home.html).

>[!NOTE]
>
>Bitte beachten Sie, dass der Control Panel nur Admin-Benutzern zur Verfügung steht und für alle Adobe Managed Services verfügbar ist.

**Technische Objekte** Das Menü **[!UICONTROL Diagnose]** ist ein wichtiges Werkzeug zur Überwachung und Analyse der verschiedenen technischen Objekte, die von der Anwendung generiert werden: Schema, Webseiten, Stapelaufträge usw. [Mehr dazu](../../developing/using/monitoring-data-model-changes.md)

**Exportprüfungen**Mit Exportprüfungen können Sie die Exporte Ihrer Instanzen überwachen: Dateien, die aus Workflows, Listen exportiert und aus Direktnachrichten heruntergeladen wurden.
[Mehr dazu](../../administration/using/auditing-export-logs.md)

**Lizenzen** Im Menü &quot; **[!UICONTROL Lizenzen]** &quot;können Sie Informationen zu Ihren Instanzen überwachen: installierte Lizenzen, Buildversionen und Vertragsabschlüsse akzeptiert.
[Mehr dazu](../../administration/using/licenses.md)

## Überwachung von Workflows {#monitoring-workflows}

<img src="assets/do-not-localize/icon_workflows.svg" width="60px">

**Best Practices und Fehlerbehebung**Die Verwendung von Workflows Best Practices und Richtlinien zur Fehlerbehebung können dabei helfen, die Leistung zu verbessern.
[Mehr dazu](../../automating/using/best-practices-workflows.md)

**Protokolle und Aufgaben**Die Überwachung von Worklow-Protokollen ist ein wichtiger Schritt, um Ihre Workflows zu analysieren und sicherzustellen, dass sie ordnungsgemäß ausgeführt werden.
[Mehr dazu](../../automating/using/monitoring-workflow-execution.md#workflow-log-and-tasks)

**Mit dem Benachrichtigungs**-Campaign Standard können Sie Benachrichtigungen an Aufsichtsbehörden senden, um die Ausführung Ihrer Arbeitsabläufe zu überwachen und festzustellen, ob ein Fehler vorliegt, der Ihre Aufmerksamkeit erfordert.
[Mehr dazu](../../automating/using/monitoring-workflow-execution.md#error-management)

## Sendungen beobachten {#monitoring-deliveries}

<img src="assets/do-not-localize/icon_send.svg" width="60px">

**Der**Campaign Standard zur Auslieferbarkeitbietet mehrere Bereitstellungs-Tools, mit denen Sie die Anzahl der erfolgreich ausgelieferten Nachrichten verbessern können: Versand-Berichte, Optimierung der Sendezeit, Vorschau von Nachrichten, E-Mail-Rendering, Verwaltung von Quarantänen usw.
[Mehr dazu](../../sending/using/about-deliverability.md)

**Versand**Sobald Ihre Nachrichten gesendet wurden, können Sie mit detaillierten Protokollen die Versand überwachen und den Erfolg Ihrer Kampagne messen sowie das Verhalten der Empfänger nachverfolgen.
[Mehr dazu](../../sending/using/monitoring-a-delivery.md)

**Versand-Warnhinweise**Mit der Versand-Warnfunktion können Sie Warnungen einrichten, die automatisch an eine Benutzergruppe gesendet werden, wenn es um die Ausführung von Versänden geht: fehlgeschlagenes Senden oder Aufbereiten, schlechtes Absprungverhältnis, niedriger Durchsatz usw.
[Mehr dazu](../../sending/using/receiving-alerts-when-failures-happen.md)

**Der dynamische Berichte**Dynamischer Berichte bietet verschiedene Berichte, die Ihnen helfen, über die Leistung Ihrer Versand auf dem Laufenden zu bleiben: Absprünge, am häufigsten angezeigte Liefermengen nach Empfängern, Durchsatz der Versand usw.
[Mehr dazu](../../reporting/using/about-dynamic-reports.md)

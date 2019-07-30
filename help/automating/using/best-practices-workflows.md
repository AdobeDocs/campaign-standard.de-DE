---
title: Best Practices für Workflows
seo-title: Best Practices für Workflows
description: Best Practices für Workflows
seo-description: Erfahren Sie, wie Best Practices für Ihre Arbeitsabläufe angewendet werden.
page-status-flag: nie aktiviert
uuid: ff 02 b 74 e -53 e 8-49 c 6-bf 8 e -0 c 729 eaa 7 d 25
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird automatisiert
content-type: Referenz
topic-tags: workflow-general-operation
context-tags: workflow, overview; workflow, main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e02ca92032c298fe1b5dbc7094de201d0a106be5

---


# Workflow best practices{#workflow-best-practices}

Mit Adobe Campaign können Sie alle Arten von Arbeitsabläufen einrichten, um einen umfangreichen Umfang an Aufgaben durchzuführen. Beim Entwerfen und Ausführen Ihrer Arbeitsabläufe müssen Sie jedoch sehr vorsichtig sein, da eine schlechte Implementierung zu schlechten Leistungen, Fehlern und Plattformproblemen führen kann. Sie finden eine Liste der Best Practices und Tipps zur Fehlerbehebung.

>[!NOTE]
>
>Workflow-Design und -ausführung müssen von einem Adobe Campaign Advanced User durchgeführt werden.

## Naming{#naming}

Um Workflow-Fehlerbehebung zu vereinfachen, empfiehlt Adobe, Ihre Arbeitsabläufe explizit zu benennen und zu beschriften. Füllen Sie das Beschreibungsfeld des Workflows aus, um den zu erstellenden Prozess zusammenzufassen, damit der Operator sie leicht verstehen kann.
Wenn der Arbeitsablauf Teil eines Prozesses ist, der mehrere Workflows umfasst, können Sie Zahlen verwenden, wenn Sie eine Beschriftung eingeben, um sie klar zu ordnen.

Beispiel:

* 001 - Importieren - Empfänger importieren
* 002 - Importieren - Importieren von Verkäufen
* 003 - Importieren - Verkaufsdetails importieren
* 010 - Exportieren - Versandprotokolle exportieren
* 011 - Exportieren - Exportrackingprotokolle

## Duplicating workflows{#duplicating-workflows}

Sie können Workflows duplizieren. In the **[!UICONTROL Marketing Activities]**, hover over the workflow and click **[!UICONTROL Duplicate element]**. Nach der Duplizierung werden Änderungen des Workflows nicht in die Kopie des Workflows übernommen. Die Kopie des Workflows kann bearbeitet werden.

![](assets/duplicating_workflow.png)

## Ausführung{#execution}

### Anzahl der Workflows

Standardmäßig wird empfohlen, nicht mehr als 20 aktive Workflows gleichzeitig auszuführen. Nach Erreichen dieses Limits werden Workflows in die Warteschlange gestellt, um die Leistung nicht zu beeinträchtigen. Entsprechend empfiehlt Adobe, Ihre Workflow-Ausnutzung im Laufe der Zeit zu verteilen.
In bestimmten Kontexten müssen Sie möglicherweise mehr als 20 Workflows ausführen. Es gilt nicht für Workflows, die auf eine geplante Ausführung warten. Falls ja, müssen Sie die Anwendungsfälle mit einem Kampagnenexperten überprüfen und den Adobe-Kundendienst kontaktieren, um den Grenzwert zu erhöhen.

### Häufigkeit

Ein Arbeitsablauf kann nicht automatisch mehr als einmal alle zehn Minuten ausgeführt werden.
Das Ausführungsintervall der Aktivität kann nicht weniger als 10 Minuten betragen. Wenn die Wiederholungshäufigkeit auf 0 gesetzt ist (auch als Standardwert), wird diese Option nicht berücksichtigt und der Workflow wird gemäß der Ausführungshäufigkeit ausgeführt.

### Angehaltene Arbeitsabläufe

Arbeitsabläufe, die für mehr als sieben Tage in Pause oder Fehlgeschlagen waren, werden gestoppt, um weniger Speicherplatz zu belegen. Die Bereinigungsaufgabe wird in den Workflow-Protokollen angezeigt.

### Übergänge

Ein Workflow mit nicht unterstützten Übergängen kann weiterhin ausgeführt werden: Dadurch wird eine Warnmeldung generiert und der Arbeitsablauf wird angehalten, sobald er den Übergang erreicht, aber kein Fehler generiert wird. Sie können einen Workflow auch ohne fertiggelegtes Design starten und es dann abschließen.

For more information, refer to [Executing workflows](../../automating/using//executing-a-workflow.md).

## Aktivität{#activity}

### Workflow-Design

To ensure that the workflow ends properly, use an **[!UICONTROL End activity]**. Vermeiden Sie den letzten Übergang eines Arbeitsablaufs selbst.

To access the detail view of the transitions, check the **[!UICONTROL Keep interim results]** option in the Execution section of the workflow properties.

>[!CAUTION]
>
>Diese Option belegt viel Speicherplatz und hilft Ihnen dabei, einen Workflow zu erstellen und eine ordnungsgemäße Konfiguration und ein Verhalten sicherzustellen. Aktivieren Sie sie nicht bei Produktionsinstanzen.

![](assets/keep_interim_best_practices.png)


### Labelling activities{#activity-labeling}

Bei der Entwicklung Ihres Arbeitsablaufs wird für jede Aktivität ein Name generiert, wie für alle Adobe Campaign-Objekte. Obwohl der Name einer Aktivität durch das Tool erzeugt wird und nicht bearbeitet werden kann, empfehlen wir, sie bei der Konfiguration mit einem expliziten Namen zu versehen.

### Duplicating activities{#activity-duplicating}

Zum Duplizieren vorhandener Aktivitäten können Sie Kopieren und Einfügen verwenden. Dadurch bleiben die ursprünglich definierten Einstellungen unverändert. For more information, refer to [Duplicating workflow activities](../../automating/using/workflow-interface.md).

### Scheduler activity{#acheduler-activity}

When building your workflow, only use one **[!UICONTROL Scheduler activity]** per branch. Wenn dieselbe Verzweigung eines Workflows mehrere Zeitplaner enthält (verknüpft miteinander verknüpft), wird die Anzahl der auszuführenden Aufgaben exponentiell multipliziert, wodurch die Datenbank erheblich überlastet würde.

You can preview the next ten executions of your workflows by clicking **[!UICONTROL Preview next executions]**.

![](assets/preview_scheduler.png)

For more information, refer to [Scheduler activity](../../automating/using/scheduler.md).

## Calling workflow with parameters{#workflow-with-parameters}

Achten Sie darauf, dass der Name und die Anzahl der Parameter mit den beim Aufruf des Workflows definierten übereinstimmen (siehe [Parameter beim Aufruf des Workflows definieren](../../automating/using/calling-a-workflow-with-external-parameters.md#defining-the-parameters-when-calling-the-workflow)). Die Typen der Parameter müssen ebenfalls mit den erwarteten Werten konsistent sein.

Make sure that all the parameters have been declared in the **[!UICONTROL External signal activity]**. Andernfalls tritt ein Fehler beim Ausführen der Aktivität auf.

For more information, see [Calling a workflow with external parameters](../../automating/using/calling-a-workflow-with-external-parameters.md).

## Exporting packages{#exporting-packages}

Um Pakete zu exportieren, dürfen die exportierten Ressourcen keine Standard-IDs enthalten. Daher müssen die IDs der exportierbaren Ressourcen durch einen anderen Namen von den Vorlagen geändert werden, die als Standard von Adobe Campaign Standard bereitgestellt werden.
For more information, see [Managing packages](../../automating/using/managing-packages.md).

## Listenexport{#exporting-lists}

Die Exportlisten-Option erlaubt standardmäßig den Export von maximal 100.000 Zeilen, die durch die Option **Nms_ExportListLimit definiert wurden**. This option can be managed by the functional administrator, under **Administration** &gt; **Application settings** &gt; **Options**.
For more information, see [Exporting lists](../../automating/using/exporting-lists.md).

## Problembehebung{#workflow-troubleshooting}

Adobe Campaign bietet verschiedene Protokolle, um Ihre Arbeitsablaufprobleme besser zu verstehen.

### Using workflow logs{#using-workflow-logs}

Sie können auf Workflow-Protokolle zugreifen, um die Ausführung Ihrer Aktivitäten zu überwachen. Er zeigt in chronologischer Abfolge alle Vorgänge und Ausführungsfehler.
For more information, refer to [Monitoring workflow execution](../../automating/using/executing-a-workflow.md#monitoring).

### Using delivery logs{#using-delivery-logs}

Mit Bereitstellungsprotokollen können Sie den Erfolg Ihrer Auslieferung überwachen. Ausschluss-Protokolle geben während der Vorbereitung des sendenden Vorgangs ausgeschlossene Meldungen zurück. Beim Senden von Protokollen wird der Status der Auslieferung für jedes Profil angegeben.
For more information, refer to [Understanding delivery failures](../../sending/using/understanding-delivery-failures.md).

### Using delivery alerting{#delivery-alerting}

Bei der Funktion Versandwarnungen handelt es sich um ein Warnungsmanagementsystem, über das eine Benutzergruppe automatisch Benachrichtigungen zu ihren Sendungen erhält.
For more information, refer to [Delivery alerting](../../sending/using/receiving-alerts-when-failures-happen.md).

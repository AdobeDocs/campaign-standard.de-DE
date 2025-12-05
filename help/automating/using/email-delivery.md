---
title: E-Mail-Versand
description: Die E-Mail-Versandaktivität ermöglicht den Versand von einmaligen oder wiederkehrenden E-Mails innerhalb eines Workflows.
audience: automating
content-type: reference
topic-tags: channel-activities
context-tags: delivery,workflow,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: e38ff3dd-8fb0-419b-9090-a3165852bf83
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: ht
source-wordcount: '904'
ht-degree: 100%

---

# E-Mail-Versand{#email-delivery}

## Beschreibung {#description}

![](assets/email.png)

![](assets/recurrentemail.png)

Die Aktivität **[!UICONTROL E-Mail-Versand]** ermöglicht das Konfigurieren eines E-Mail-Versands innerhalb eines Workflows. Dabei kann es sich um eine **Einmalige E-Mail** handeln, die nur einmal gesendet wird, oder um eine **Wiederkehrende E-Mail**.

Bei einmaligen Versandaktionen handelt es sich um Standard-E-Mails, die nur einmal gesendet werden.

Wiederkehrende Versandaktionen ermöglichen den wiederholten Versand der gleichen E-Mail an verschiedene Zielgruppen. Für Berichtzwecke können bei Bedarf die einzelnen Sendungen nach Zeiträumen aggregiert werden.

## Anwendungskontext          {#context-of-use}

Der **[!UICONTROL E-Mail-Versand]** dient insbesondere der Automatisierung des Nachrichtenversands an eine innerhalb desselben Workflows berechnete Zielgruppe.

In Verbindung mit einer Planungsaktivität ist es möglich, wiederkehrende E-Mails zu konfigurieren.

Die E-Mail-Empfänger werden in vorangeschalteten Zielgruppenbestimmungsaktivitäten des Workflows, wie beispielsweise Abfragen, Schnittmengen etc. definiert.

Die Vorbereitung der Nachricht wird in Abhängigkeit von den Ausführungsparametern des Workflows ausgelöst. Sie können im Nachrichten-Dashboard auswählen, ob eine manuelle Bestätigung zum Nachrichtenversand erforderlich ist oder nicht (standardmäßig erforderlich). Sie können den Workflow entweder manuell starten oder eine Planung verwenden, um die Ausführung zu automatisieren.

**Verwandte Themen:**

* [Anwendungsfall: Erstellung eines einmaligen E-Mail-Versands pro Woche](../../automating/using/workflow-weekly-offer.md)
* [Anwendungsfall: Erstellung eines Standort-segmentierten Versands](../../automating/using/workflow-segmentation-location.md)
* [Anwendungsfall: Erstellen von Sendungen mit einem Komplement](../../automating/using/workflow-created-query-with-complement.md)
* [Anwendungsfall: Retargeting-Workflow für einen erneuten Versand an Nicht-Öffner](../../automating/using/workflow-cross-channel-retargeting.md)
* [Anwendungsfall: Versand zum Geburtstag](../../automating/using/birthday-delivery.md)

## Konfiguration {#configuration}

1. Ziehen Sie einen **[!UICONTROL E-Mail-Versand]** in den Workflow-Arbeitsbereich.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in den Schnellaktionen angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).

   >[!NOTE]
   >
   >Die Schaltfläche ![](assets/dlv_activity_params-24px.png) in den Schnellaktionen bietet Zugriff auf die allgemeinen Eigenschaften und erweiterten Optionen der Aktivität (aber nicht des Versands selbst). Sie ist spezifisch für die jeweilige **[!UICONTROL E-Mail-Versand]**-Aktivität. Auf die Eigenschaften der E-Mail können Sie über die Aktionsleiste Ihres Dashboards zugreifen.

1. Wählen Sie den Versandtyp der E-Mail aus:

   * **[!UICONTROL E-Mail]**: Die E-Mail wird ein einziges Mal versendet. Sie können an dieser Stelle entscheiden, ob Sie der Aktivität eine ausgehende Transition hinzufügen möchten oder nicht. Die unterschiedlichen Transitionstypen werden in Etappe 7 dieser Prozedur beschrieben.
   * **[!UICONTROL E-Mail zum wiederkehrenden Versand]**: Die E-Mail wird wiederholt versendet. Die Frequenz des Versands wird in einer vorangeschalteten **[!UICONTROL Planung]** definiert. Wählen Sie einen Aggregatzeitraum für die wiederkehrenden Sendungen aus. Auf diese Weise werden alle E-Mails, die im angegebenen Zeitraum versendet wurden, in einer E-Mail zusammengefasst, die auch **wiederkehrende Ausführung** genannt wird. Diese ist in der Marketing-Aktivitätenliste der Anwendung zugänglich.

     Es besteht beispielsweise die Möglichkeit, die Ausführungen einer täglich gesendeten Geburtstags-E-Mail pro Monat zu aggregieren. Auf diese Weise lässt sich ein monatlicher Versandbericht für eine täglich gesendete E-Mail generieren.

   >[!NOTE]
   >
   >Ein wiederkehrender Versand wird auf Basis des **Aggregat-Zeitraums** vorbereitet. Wenn der Aggregat-Zeitraum beispielsweise &quot;nach Tag&quot; lautet, wird der Versand nur einmal pro Tag erneut vorbereitet. Wenn Sie diesen Workflow mehrmals am Tag aufrufen möchten, verwenden Sie [!UICONTROL Nicht aggregieren].

1. Wählen Sie einen E-Mail-Typ aus. Die verschiedenen E-Mail-Typen entsprechen Vorlagen, die im Menü **[!UICONTROL Ressourcen]** > **[!UICONTROL Vorlagen]** > **[!UICONTROL Versandvorlagen]** definiert sind.
1. Geben Sie die allgemeinen Eigenschaften der E-Mail an und ordnen Sie sie gegebenenfalls einer existierenden Kampagne zu. Der Titel der Versandaktivität des Workflows wird mit dem Titel der E-Mail aktualisiert.
1. Erstellen Sie den E-Mail-Inhalt. Weiterführende Informationen hierzu finden Sie im Abschnitt [Inhaltseditor](../../designing/using/designing-content-in-adobe-campaign.md).
1. Die Aktivität **[!UICONTROL E-Mail-Versand]** verfügt standardmäßig über keinerlei ausgehende Transitionen. Sie haben jedoch die Möglichkeit, eine ausgehende Transition **[!UICONTROL für Ihre E-Mail-Versand]**-Aktivität zu erzeugen, indem Sie unter Verwendung der in der Schnellaktion der Aktivität verfügbaren Schaltfläche **[!UICONTROL die erweiterten Optionen öffnen und im]** Allgemein![](assets/dlv_activity_params-24px.png)-Tab eine der folgenden Optionen aktivieren:

   * **[!UICONTROL Ausgehende Transition ohne Population hinzufügen]**: ermöglicht die Erstellung einer ausgehenden Transition, die exakt dieselbe Population enthält wie die eingehende Transition.
   * **[!UICONTROL Ausgehende Transition mit Population hinzufügen]**: ermöglicht die Erstellung einer ausgehenden Transition, die die Population enthält, an die die E-Mail gesendet wurde. Der Teil der Zielgruppe, der in der Versandvorbereitung ausgeschlossen wurde (Quarantäne, ungültige E-Mail-Adresse etc.), ist von dieser Transition ausgeschlossen.

1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

Wenn Sie die Aktivität später erneut öffnen, gelangen Sie direkt in das Dashboard der E-Mail. Nur der Inhalt kann zu diesem Zeitpunkt noch geändert werden.

Standardmäßig wird durch den Versand-Workflow nur die Vorbereitung der Nachricht ausgelöst. Der in einem Workflow erstellte Nachrichtenversand muss noch bestätigt werden, nachdem der Workflow gestartet wurde. Sie können aber im Nachrichten-Dashboard die Option **[!UICONTROL Vor dem Nachrichtenversand Bestätigung einholen]** deaktivieren. Dies ist jedoch nur möglich, wenn die Nachricht in einem Workflow erstellt wurde. Ist diese Option deaktiviert, werden Nachrichten ohne weiteren Hinweis gesendet, sobald die Vorbereitung abgeschlossen ist.

## Bemerkungen          {#remarks}

Auf die von einem Workflow aus erstellten Sendungen kann in der Marketing-Aktivitätenliste der Anwendung zugegriffen werden. Über das Dashboard lässt sich der Ausführungsstatus des Workflows visualisieren. Die Links im Übersichtsmenü der E-Mail ermöglichen einen direkten Zugriff auf verknüpfte Elemente (Workflow, Kampagne, übergeordneter Versand im Fall einer E-Mail zum wiederkehrenden Versand).

![](assets/wkf_display_recurrent_executions_2.png)

Die Ausführungen wiederkehrender Sendungen sind jedoch standardmäßig ausgeblendet. Um sie anzuzeigen, aktivieren Sie im Suchmenü der Marketing-Aktivitäten die Option **[!UICONTROL Wiederkehrende Ausführungen anzeigen]**.

![](assets/wkf_display_recurrent_executions.png)

Ausgehend von den übergeordneten Sendungen, auf die über die Marketing-Aktivitätenliste oder direkt über die verknüpften wiederkehrenden Ausführungen zugegriffen werden kann, lässt sich die Gesamtheit aller getätigten Sendungen visualisieren (in Abhängigkeit vom bei der Konfiguration der **[!UICONTROL E-Mail-Versand]**-Aktivität festgelegten Aggregat-Zeitraum). Öffnen Sie hierzu mithilfe der **[!UICONTROL -Schaltfläche die Detailansicht der]** Bereitstellung![](assets/wkf_dlv_detail_button.png)-Kachel des übergeordneten Versands.

![](assets/wkf_display_recurrent_executions_3.png)

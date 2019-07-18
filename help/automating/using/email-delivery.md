---
title: E-Mail-Versand
seo-title: E-Mail-Versand
description: E-Mail-Versand
seo-description: Die E-Mail-Versandaktivität ermöglicht den Versand von einmaligen oder wiederkehrenden E-Mails innerhalb eines Workflows.
page-status-flag: nie aktiviert
uuid: 7 de 53431-84 ae -4 d 21-8361-2775 ad 314 ed 2
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird automatisiert
content-type: Referenz
topic-tags: channel-activities
discoiquuid: 5 f 288 cf 6-f 8 ff -4 ac 9-9 c 1 a -8010260554 bb
context-tags: Bereitstellung, Arbeitsablauf, Haupt
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# E-Mail-Versand{#email-delivery}

## Beschreibung {#description}

![](assets/email.png)

![](assets/recurrentemail.png)

Die **[!UICONTROL E-Mail-Versandaktivität]ermöglicht den Versand von E-Mails innerhalb eines Workflows.** Dabei kann es sich um eine **Einmalige E-Mail** handeln, die nur einmal gesendet wird, oder um eine **Wiederkehrende E-Mail**.

Bei einmaligen Versandaktionen handelt es sich um Standard-E-Mails, die nur einmal gesendet werden.

Wiederkehrende Versandaktionen ermöglichen den wiederholten Versand der gleichen E-Mail an verschiedene Zielgruppen. Für Berichtzwecke können bei Bedarf die einzelnen Sendungen nach Zeiträumen aggregiert werden.

## Anwendungskontext {#context-of-use}

Der **[!UICONTROL E-Mail-Versand]dient insbesondere der Automatisierung des Nachrichtenversands an eine innerhalb desselben Workflows berechnete Zielgruppe.**

In Verbindung mit einer Planungsaktivität ist es möglich, wiederkehrende E-Mails zu konfigurieren.

Die E-Mail-Empfänger werden in vorangeschalteten Zielgruppenbestimmungsaktivitäten des Workflows, wie beispielsweise Abfragen, Schnittmengen etc. definiert.

Die Vorbereitung der Nachricht wird in Abhängigkeit von den Ausführungsparametern des Workflows ausgelöst. Sie können im Nachrichten-Dashboard auswählen, ob eine manuelle Bestätigung zum Nachrichtenversand erforderlich ist oder nicht (standardmäßig erforderlich). Sie können den Workflow entweder manuell starten oder eine Planung verwenden, um die Ausführung zu automatisieren.

## Konfiguration {#configuration}

1. Ziehen Sie einen **[!UICONTROL E-Mail-Versand]in den Workflow-Arbeitsbereich.**
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der ![-Schaltfläche aus den angezeigten Quick Actions.](assets/edit_darkgrey-24px.png)

   >[!NOTE]
   >
   >Die Schaltfläche ![ in den Quick Actions bietet Zugriff auf die allgemeinen Eigenschaften und erweiterten Optionen der Aktivität (nicht des Versands selbst).](assets/dlv_activity_params-24px.png) Sie ist spezifisch für die **[!UICONTROL E-Mail-Versandaktivität.]** Auf die Eigenschaften der E-Mail können Sie über die Symbolleiste ihres Dashboards zugreifen.

1. Wählen Sie den Versandtyp der E-Mail aus:

   * **[!UICONTROL E-Mail]**: Die E-Mail wird ein einziges Mal versendet. Sie können an dieser Stelle entscheiden, ob Sie der Aktivität eine ausgehende Transition hinzufügen möchten oder nicht. Die unterschiedlichen Transitionstypen werden in Etappe 7 dieser Prozedur beschrieben.
   * **[!UICONTROL E-Mail zum wiederkehrenden Versand]**: Die E-Mail wird wiederholt versendet. Die Frequenz des Versands wird in einer vorangeschalteten **[!UICONTROL Planung]definiert.** Wählen Sie einen Aggregatzeitraum für die wiederkehrenden Sendungen aus. Auf diese Weise werden alle E-Mails, die im angegebenen Zeitraum versendet wurden, in einer E-Mail zusammengefasst, die auch **wiederkehrende Ausführung** genannt wird. Diese ist in der Marketingaktivitätenliste der Anwendung zugänglich.

      Es besteht beispielsweise die Möglichkeit, die Ausführungen einer täglich gesendeten Geburtstags-E-Mail pro Monat zu aggregieren. Auf diese Weise lässt sich ein monatlicher Versandbericht für eine täglich gesendete E-Mail generieren.

1. Wählen Sie einen E-Mail-Typ aus. The email types come from email templates defined in the **[!UICONTROL Resources]** &gt; **[!UICONTROL Templates]** &gt; **[!UICONTROL Delivery templates]** menu.
1. Geben Sie die allgemeinen Eigenschaften der E-Mail an und ordnen Sie sie gegebenenfalls einer existierenden Kampagne zu. Der Titel der Versandaktivität des Workflows wird mit dem Titel der E-Mail aktualisiert.
1. Erstellen Sie den E-Mail-Inhalt. Weiterführende Informationen hierzu finden Sie im Abschnitt [Inhaltseditor](../../designing/using/about-email-content-design.md).
1. Die **[!UICONTROL E-Mail-Versandaktivität]verfügt standardmäßig über keinerlei ausgehende Transition.** Sie haben jedoch die Möglichkeit, eine ausgehende Transition zu erzeugen, indem Sie unter Verwendung der in den Quick Actions der Aktivität verfügbaren Schaltfläche **[!UICONTROL die erweiterten Optionen öffnen und im]** Allgemein **[!UICONTROL -Tab eine der folgenden Optionen aktivieren:]**![](assets/dlv_activity_params-24px.png)

   * **[!UICONTROL Ausgehende Transition ohne Population hinzufügen]**: ermöglicht die Erstellung einer ausgehenden Transition, die exakt dieselbe Population enthält wie die eingehende Transition.
   * **[!UICONTROL Ausgehende Transition mit Population hinzufügen]**: ermöglicht die Erstellung einer ausgehenden Transition, die die Population enthält, der die E-Mail gesendet wurde. Die Mitglieder des Ziels, die während der Bereitstellungsvorbereitung (Quarantäne, ungültige E-Mail usw.) ausgeschlossen wurden, werden aus diesem Übergang ausgeschlossen.

1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

Wenn Sie die Aktivität später erneut öffnen, gelangen Sie direkt in das Dashboard der E-Mail. Nur der Inhalt kann zu diesem Zeitpunkt noch geändert werden.

Standardmäßig wird durch den Versand-Workflow nur die Vorbereitung der Nachricht ausgelöst. Der in einem Workflow erstellte Nachrichtenversand muss noch bestätigt werden, nachdem der Workflow gestartet wurde. Sie können aber im Nachrichten-Dashboard die Option **[!UICONTROL Vor dem Nachrichtenversand Bestätigung einholen]deaktivieren. Dies ist jedoch nur möglich, wenn die Nachricht in einem Workflow erstellt wurde.** Ist diese Option deaktiviert, werden Nachrichten ohne weiteren Hinweis gesendet, sobald die Vorbereitung abgeschlossen ist.

## Bemerkungen {#remarks}

Auf die von einem Workflow aus erstellten Sendungen kann in der Marketingaktivitätenliste der Anwendung zugegriffen werden. Über das Dashboard lässt sich der Ausführungsstatus des Workflows visualisieren. Die Links im Übersichtsmenü der E-Mail ermöglichen einen direkten Zugriff auf verknüpfte Elemente (Workflow, Kampagne, Elternversand im Fall einer E-Mail zum wiederkehrenden Versand).

![](assets/wkf_display_recurrent_executions_2.png)

Die Ausführungen wiederkehrender Sendungen sind jedoch standardmäßig ausgeblendet. Um sie anzuzeigen, aktivieren Sie im Suchmenü der Marketingaktivitäten die Option **[!UICONTROL Wiederkehrende Ausführungen anzeigen].**

![](assets/wkf_display_recurrent_executions.png)

Ausgehend von den Elternsendungen, auf die über die Marketingaktivitätenliste oder direkt über die verknüpften wiederkehrenden Ausführungen zugegriffen werden kann, lässt sich die Gesamtheit aller getätigten Sendungen visualisieren (in Abhängigkeit vom bei der Konfiguration der **[!UICONTROL E-Mail-Versandaktivität]festgelegten Aggregat-Zeitraum).** To do this, open the detail view of the parent delivery's **[!UICONTROL Deployment]** block by selecting ![](assets/wkf_dlv_detail_button.png).

![](assets/wkf_display_recurrent_executions_3.png)

## Beispiel {#example}

![](assets/wkf_delivery_example_1.png)

Das folgende Beispiel zeigt einen Geburtstags-Workflow. Jeden Tag wird eine E-Mail an alle Profile gesendet, die Geburtstag haben. Gehen Sie wie folgt vor:

* Eine **[!UICONTROL Planung]startet den Workflow täglich um 8 Uhr.**

   ![](assets/wkf_delivery_example_2.png)

* Die auf die Planung folgende **[!UICONTROL Abfrage]ruft alle Profile aus der Datenbank ab, die am aktuellen Datum Geburtstag haben und deren E-Mail-Adresse bekannt ist.** Der Geburtstagsfilter ist standardmäßig im Abfragetool enthalten.

   ![](assets/wkf_delivery_example_3.png)

* **[!UICONTROL E-Mail zum wiederkehrenden Versand]-** die Sendungen werden pro Monat aggregiert. Auf diese Weise sind alle innerhalb eines Monats gesendeten E-Mails in einer einzigen Ansicht enthalten. Innerhalb eines Jahres werden folglich 365 Sendungen ausgeführt, die jedoch innerhalb der Adobe-Campaign-Benutzeroberfläche in nur 12 Ansichten (auch **wiederkehrende Ausführungen** genannt) zusammengefasst werden. Der Verlauf und die Berichte zeigen monatliche Zusammenfassungen und nicht jeden einzelnen Versand.

   ![](assets/wkf_delivery_example_4.png)


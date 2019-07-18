---
title: Workflow ausführen
seo-title: Workflow ausführen
description: Workflow ausführen
seo-description: Hier erfahren Sie, wie Sie einen Workflow ausführen und überwachen können.
page-status-flag: nie aktiviert
uuid: ff 02 b 74 e -53 e 8-49 c 6-bf 8 e -0 c 729 eaa 7 d 25
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird automatisiert
content-type: Referenz
topic-tags: workflow-general-operation
discoiquuid: 906 c 85 ea -83 b 7-4268-86 da-cd 353 f 1 dc 591
context-tags: workflow, overview; workflow, main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 0454dac1a7976c1be2838c2a846d33e77e60c3b3

---


# Workflow ausführen{#executing-a-workflow}

## Über die Ausführung von Workflows {#about-workflow-execution}

Workflows werden grundsätzlich manuell gestartet, können jedoch anschließend inaktiv bleiben, wenn dies mithilfe einer [Planung](../../automating/using/scheduler.md) konfiguriert wurde.

>[!CAUTION]
>
>Wir empfehlen, nicht mehr als fünf Workflows gleichzeitig auszuführen. Wenn zu viele Workflows gleichzeitig ausgeführt werden, könnte das System nicht mehr über genügend Ressourcen verfügen und instabil werden. Wir empfehlen auch, die Workflows auf einen möglichst langen Zeitraum zu verteilen.

Bei Aktionen bezüglich der Ausführung des Workflows (Start, Stopp, Pause etc.) handelt es sich um **asynchrone** Prozesse, d. h. der jeweilige Befehl wird gespeichert und erst dann ausgeführt, wenn ein Server verfügbar ist.

Die Übermittlung der Ergebnisse der einzelnen Workflow-Aktivitäten erfolgt über Transitionen, welche in Form von Pfeilen dargestellt werden.

Transitionen, die nicht mit einer Zielaktivität verbunden sind, werden als schwebend bezeichnet.

![](assets/wkf_execution_1.png)

>[!NOTE]
>
>Auch mit schwebenden Transitionen kann ein Workflow ausgeführt werden: Die Ausführung erzeugt einen Warnhinweis und wird bei Aktivierung einer derartigen Transition ausgesetzt. Es wird jedoch kein Fehler erzeugt. Auf diese Weise ist es möglich, einen Workflow zu starten, auch wenn seine Konzeption noch nicht vollständig abgeschlossen ist, und ihn nach und nach zu vervollständigen.

Sobald eine Aktivität ausgeführt worden ist, wird die Anzahl der in der Transition übertragenen Datensätze oberhalb der Transition angezeigt.

![](assets/wkf_transition_count.png)

Sie können Transitionen vor oder nach der Ausführung des Workflows öffnen, um zu überprüfen, ob die übermittelten Daten korrekt sind. Die vorhandenen Daten sowie deren Struktur lassen sich visualisieren.

Standardmäßig können nur die Details der letzten Transition des Workflows abgerufen werden. Um auch auf die Ergebnisse der vorangehenden Aktivitäten zugreifen zu können, ist vor dem Start des Workflows in den Workflow-Eigenschaften im Bereich **[!UICONTROL Ausführung]** die Option **Zwischenergebnis festhalten]zu aktivieren.[!UICONTROL **

>[!NOTE]
>
>Diese Option verbraucht eine große Menge an Speicherplatz und dient der Erstellung eines Workflows und der korrekten Konfiguration. Aktivieren Sie sie nicht bei Produktionsinstanzen.

Bei einer geöffneten Transition kann ihr **[!UICONTROL Titel]** geändert oder derselben ein **Segment-Code]zugewiesen werden.[!UICONTROL ** Bearbeiten Sie hierzu die entsprechenden Felder und validieren Sie Ihre Änderungen.

## Workflow mit der REST API steuern {#controlling-a-workflow-from-the-rest-api}

Mit der REST API können Sie einen Workflow **starten******, aussetzen, wieder aufnehmen und **anhalten**.****

Weiterführende Informationen und Beispiele von REST-Aufrufen finden Sie in der [API-Dokumentation](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#controlling-a-workflow).

## Workflow-Lebenszyklen {#life-cycle}

Der Lebenszyklus eines Workflows gestaltet sich in drei Hauptetappen:

* **In Bearbeitung** (grau)

   Hierbei handelt es sich um die Phase der Erstellung (siehe [Workflow erstellen](../../automating/using/building-a-workflow.md#creating-a-workflow)). Ein derartiger Workflow wurde noch nicht vom Server übernommen und kann daher problemlos geändert werden.

* **Gestartet** (blau)

   Nach Abschluss der Erstellungsphase kann der Workflow gestartet werden. Daraufhin wird er vom Server übernommen.

* **Abgeschlossen** (grün)

   Ein Workflow ist abgeschlossen, wenn keine Aufgaben mehr zur Verarbeitung anstehen, oder wenn die Ausführung ausdrücklich angehalten wurde.

Nach dem Start kann ein Workflow zwei weitere Status aufweisen:

* **Warnhinweis** (gelb)

   Der Workflow konnte nicht abgeschlossen werden oder er wurde anhand der Schaltflächen ![](assets/pause_darkgrey-24px.png) bzw. ![ ausgesetzt.](assets/check_pause_darkgrey-24px.png)

* **Fehlerhaft** (rot)

   Bei der Ausführung des Workflows ist ein Fehler aufgetreten. Die Ausführung wurde angehalten und ein Eingreifen des Benutzers ist erforderlich. Mithilfe der Schaltfläche ![](assets/printpreview_darkgrey-24px.png) gelangen Sie in das Workflow-Protokoll, dem Sie die Fehlerursache entnehmen können (siehe [Monitoring](../../automating/using/executing-a-workflow.md#monitoring)).

Die Liste der Marketingaktivitäten ermöglicht die Anzeige aller Workflows inklusive ihrer Status. Weiterführende Informationen dazu finden Sie im Abschnitt [Marketingaktivitäten verwalten](../../start/using/marketing-activities.md#about-marketing-activities).

![](assets/wkf_execution_3.png)

## Ausführungsbefehle {#execution-commands}

Die Schaltflächen der Symbolleiste dienen dazu, die Workflow-Ausführung zu starten, zu verfolgen und eventuell anzupassen. Siehe den Abschnitt [Symbolleiste](../../automating/using/workflow-interface.md#action-bar).

![](assets/wkf_execution_2.png)

Folgende Aktionen sind möglich:

**Starten**

Die Schaltfläche ![](assets/play_darkgrey-24px.png) löst die Workflow-Ausführung aus. Der Workflow wechselt in den Status **Gestartet** (blau). Wenn der Workflow zuvor ausgesetzt war, handelt es sich um eine Wiederaufnahme, ansonsten werden die ersten Aktivitäten aktiviert.

>[!NOTE]
>
>Der Start eines Workflows ist ein asynchroner Prozess, d. h. der jeweilige Befehl wird gespeichert und erst dann ausgeführt, wenn ein Server verfügbar ist.

**Aussetzen**

Die Schaltfläche ![ setzt die Workflow-Ausführung aus. ](assets/pause_darkgrey-24px.png) Der Workflow wechselt in den Status **Warnhinweis** (gelb). Bis zur Wiederaufnahme werden keine neuen Aktivitäten aktiviert, laufende Vorgänge werden jedoch fortgeführt.

**Anhalten**

Die Schaltfläche ![](assets/stop_darkgrey-24px.png) hält die Workflow-Ausführung an. Der Workflow wechselt in den Status **Abgeschlossen** (grün). Importe und SQL-Abfragen werden sofort abgebrochen. Eine Wiederaufnahme an der Stelle der Unterbrechung ist nicht möglich.

**Neu starten**

Die Schaltfläche ![ hält die Workflow-Ausführung zunächst an und startet sie dann erneut. ](assets/pauseplay_darkgrey-24px.png) In den meisten Fällen ermöglicht dies einen schnelleren Neustart. Dieser Befehl bietet sich vor allem auch dann an, wenn das Anhalten eines Workflows geraume Zeit in Anspruch nimmt, da die Schaltfläche ![ erst wieder verfügbar ist, wenn der Workflow tatsächlich angehalten wurde.](assets/play_darkgrey-24px.png)

Wenn im Workflow Aktivitäten markiert sind, stehen weitere Schaltflächen zur Verfügung:

**Vorgezogene Ausführung**

Die Schaltfläche ![ bietet die Möglichkeit, so schnell wie möglich die markierten ausstehenden Aufgaben zu starten.](assets/pending_darkgrey-24px.png)

**Normale Ausführung**

Die Schaltfläche ![ aktiviert ausgesetzte oder deaktivierte Aktivitäten neu.](assets/check_darkgrey-24px.png)

**Ausführung ab Markierung aussetzen**

Die Schaltfläche ![ setzt die Ausführung des Workflows ab der ausgewählten Aktivität aus. Diese und alle im Zweig folgenden Aktivitäten werden nicht ausgeführt.](assets/check_pause_darkgrey-24px.png)

**Keine Ausführung**

Die Schaltfläche ![ deaktiviert die markierten Aktivitäten.](assets/checkdisable.png)

>[!NOTE]
>
>Auf die der Bearbeitung einer bestimmten Aktivität dienenden Aktionen kann auch über die Quick Actions zugegriffen werden, die bei der Markierung einer Aktivität angezeigt werden.

## Monitoring {#monitoring}

Über die Schaltfläche ![ können Sie auf das Protokoll und die Aufgaben des Workflows zugreifen.](assets/printpreview_darkgrey-24px.png)

Der Workflow-Verlauf wird für die in den Ausführungseigenschaften eines Workflows angegebene Dauer gespeichert (siehe [Eigenschaften des Workflows](../../automating/using/executing-a-workflow.md#workflow-properties)). Innerhalb dieser Dauer werden alle Logs gespeichert, auch wenn der Workflow neu gestartet wurde. Wenn Sie die Logs einer früheren Ausführung nicht beibehalten möchten, können Sie den Verlauf unter Verwendung der Schaltfläche ![ bereinigen.](assets/delete_darkgrey-24px.png)

Der **[!UICONTROL Protokoll]-Tab enthält den Ausführungsverlauf aller oder aller markierten Aktivitäten.** Er zeigt in chronologischer Abfolge alle Vorgänge und Ausführungsfehler.

![](assets/wkf_execution_4.png)

Der **[!UICONTROL Aufgaben]-Tab zeigt die Ausführungsabfolge der Aktivitäten.** Klicken Sie auf eine Aufgabe zur Anzeige weiterer Details.

![](assets/wkf_execution_5.png)

In beiden Listen:

* gibt der Zähler Auskunft über die Anzahl an Listeneinträgen. Bei mehr als 30 Listenelementen wird durch einen Klick auf den Zähler die Gesamtzahl angezeigt.
* ermöglicht die Schaltfläche **[!UICONTROL Liste konfigurieren]die Auswahl der anzuzeigenden Informationen, die Bestimmung der Spaltenreihenfolge sowie die Sortierung.**
* Mithilfe von Filtern können Sie Informationen schneller auffinden. Über das Suchfeld können Sie nach einem bestimmten Text in den Namen der Workflow-Aktivitäten (Beispiel: "Abfrage") und Protokollen suchen.

## Umgang mit Fehlern {#error-management}

Wenn ein Fehler auftritt, wird der Workflow ausgesetzt und die bei Fehlerauftritt ausgeführte Aktivität blinkt rot.

Der Workflow wechselt in den roten Status und der Fehler wird im Protokoll verzeichnet.

Es besteht die Möglichkeit, das Aussetzen des Workflows im Falle von Fehlern zu vermeiden und die sich anschließenden Aufgaben wie geplant auszuführen. Öffnen Sie hierzu die Workflow-Eigenschaften mithilfe der Schaltfläche ![](assets/edit_darkgrey-24px.png) und wählen Sie im Bereich **[!UICONTROL Ausführung]** im Feld **Bei Fehler** die Option **Ignorieren** aus der Dropdown-Liste aus.

In diesem Fall wird die fehlerhafte Aufgabe abgebrochen. Dieser Modus ist insbesondere bei Workflows mit wiederkehrenden Vorgängen angebracht, da die nächste Ausführung auf diese Weise wie geplant starten kann.

>[!NOTE]
>
>Es besteht die Möglichkeit, diese Vorgehensweise innerhalb eines Workflows nur für bestimmte Aktivitäten zu konfigurieren. To do this, select an activity and open it using the quick action ![](assets/edit_darkgrey-24px.png). und wählen Sie im Bereich **Ausführungsoptionen** den gewünschten Umgang mit Fehlern aus. Siehe [Ausführungsoptionen von Aktivitäten](../../automating/using/executing-a-workflow.md#activity-execution-options).

Im Bereich **[!UICONTROL Ausführung]** der Workflow-Eigenschaften kann die Anzahl an **Folgefehlern]bestimmt werden, die zulässig sind, bevor die Ausführung des Workflows automatisch ausgesetzt wird.[!UICONTROL ** Solange diese Anzahl nicht erreicht ist, werden die fehlerhaften Elemente ignoriert und die anderen Workflow-Zweige regulär ausgeführt. Sobald diese Anzahl erreicht ist, wird der Workflow ausgesetzt und die Workflow-Supervisoren werden automatisch benachrichtigt (E-Mail und In-App-Benachrichtigung). Siehe [Eigenschaften des Workflows](../../automating/using/executing-a-workflow.md#workflow-properties) und [Benachrichtigungen in Adobe Campaign](../../administration/using/sending-internal-notifications.md).

Die Supervisoren werden ebenfalls in den Ausführungseigenschaften des Workflows bestimmt.

## Ausführungseigenschaften {#workflow-properties}

Sie haben die Möglichkeit, die globalen Ausführungseigenschaften eines Workflows anzupassen. Verwenden Sie hierzu die Schaltfläche ![](assets/edit_darkgrey-24px.png), um auf die Eigenschaften des Workflows zuzugreifen und öffnen Sie den Bereich **Ausführung[!UICONTROL .]**

Im Feld **[!UICONTROL Standardaffinität]können Sie nun für die Ausführung des Workflows die Verwendung einer bestimmten Engine vorschreiben.**

Geben Sie im Feld **[!UICONTROL Verlaufsumfang]die Dauer in Tagen an, nach der der Verlauf bereinigt werden soll.**

Aktivieren Sie bei Bedarf die Optionen **[!UICONTROL SQL-Abfragen im Protokoll speichern]** und **[!UICONTROL In der Engine ausführen (nicht im Produktionsmodus benutzen)]**.

Kreuzen Sie die Option **[!UICONTROL Zwischenergebnis festhalten]an, wenn Sie die Detailansicht der Transitionen visualisieren können möchten.** Achtung: Durch das Ankreuzen dieser Option kann sich die Ausführung des Workflows stark verlangsamen.

Im Feld **[!UICONTROL Prioritätsstufe]haben Sie die Möglichkeit, die Workflow-Ausführung als eher vorrangig oder eher nachrangig zu kennzeichnen.** Kritische Workflows werden vorrangig ausgeführt.

Im Feld **[!UICONTROL Supervisoren]wird die Gruppe von Personen bestimmt, die im Fall eines fehlerhaften Workflows benachrichtigt werden (E-Mail und In-App-Benachrichtigung).** Sollte keine Gruppe angegeben sein, wird niemand benachrichtigt. Weiterführende Informationen zu Adobe Campaign-Benachrichtigungen finden Sie in Abschnitt [Benachrichtigungen in Adobe Campaign](../../administration/using/sending-internal-notifications.md).

Im Feld **[!UICONTROL Bei Fehler]lassen sich mögliche Reaktionen bei Auftreten eines Fehlers bestimmen.** Zwei Optionen stehen zur Wahl:

* **Prozess aussetzen** - der Workflow wird automatisch angehalten. Der Workflow-Status wechselt in **fehlerhaft** und sein Symbol wird rot hinterlegt. Nach Beseitigung der Fehlerursache kann der Workflow neu gestartet werden.
* **Ignorieren** - die den Fehler verursachende Aktivität sowie alle im selben Zweig folgenden Aktivitäten werden nicht ausgeführt. Diese Konfiguration empfiehlt sich bei wiederkehrenden Aufgaben. Wenn der Workflow-Zweig eine Planungsaktivität enthält, führt diese automatisch zum nächsten geplanten Zeitpunkt zu einer erneuten Ausführung.

   Bei Auswahl dieser Option können Sie außerdem eine Anzahl zulässiger **[!UICONTROL Folgefehler]bestimmen:**

   * If the number specified is **[!UICONTROL 0]**, or as long as the number specified is not reached, activities that encounter errors are ignored. Die anderen Workflow-Zweige werden regulär ausgeführt.
   * Bei Erreichen der angegebenen Anzahl wird der gesamte Workflow ausgesetzt und nimmt den Status **[!UICONTROL Mit Fehlern an]**. Sollten zuvor Supervisoren bestimmt worden sein, werden diese automatisch per E-Mail benachrichtigt.

![](assets/wkf_execution_6.png)

## Aktivitätseigenschaften {#activity-properties}

### Allgemeine Eigenschaften einer Aktivität {#general-properties-of-an-activity}

Jede Aktivität verfügt über einen **[!UICONTROL Eigenschaften]-Tab.** In diesem Tabs lassen sich die allgemeinen Parameter der Aktivität, insbesondere Titel und Kennung anpassen. Die Konfiguration dieses Tabs is optional.

### Verwaltung ausgehender Transitionen von Aktivitäten {#managing-an-activity-s-outbound-transitions}

Standardmäßig verfügen bestimmte Aktivitäten nicht über ausgehende Transitionen. Sie haben jedoch die Möglichkeit, diese in den Tabs **[!UICONTROL Transitionen]** oder **Eigenschaften]der Aktivität hinzuzufügen, um Ihre Population im selben Workflow mithilfe angeschlossener Aktivitäten weiter zu bearbeiten.[!UICONTROL **

Je nach Aktivität lassen sich verschiedene Arten ausgehender Transitionen hinzufügen:

* Standardtransition: mittels der Aktivität berechnete Population.
* Transition ohne Population: Dieser Typ der ausgehenden Transition kann hinzugefügt werden, um den Workflow fortzusetzen. Er enthält keine Population, um nicht unnötig Speicherplatz im System zu belegen.
* Zurückweisungen: zurückgewiesene Population. Dies trifft zu, wenn z. B. in eine Aktivität eingehende Daten aufgrund von Fehlerhaftig- oder Unvollständigkeit nicht verarbeitet werden konnten.
* Komplement: nach der Ausführung der Aktivität verbleibende Population. Dies trifft zu, wenn z. B. eine Segmentierungsaktivität dahingehend konfiguriert ist, dass lediglich ein bestimmter Prozentsatz der eingehenden Population beibehalten wird.

Es besteht die Möglichkeit für die aus der Aktivität ausgehende Transition einen **[!UICONTROL Segmentcode]anzugeben.** Der Segmentcode ermöglicht es, die Herkunft von Teilmengen der Zielpopulation zu identifizieren, und kann im weiteren Verlauf für die Nachrichtenpersonalisierung verwendet werden.

### Ausführungsoptionen von Aktivitäten {#activity-execution-options}

In einer Workflow-Aktivität erlaubt Ihnen der Tab **[!UICONTROL Ausführungsoptionen]im Eigenschaften-Bildschirm insbesondere die Definition des Ausführungsmodus sowie des Verhaltens beim Auftritt von Fehlern.**

Markieren Sie zum Zugriff auf diese Optionen die gewünschte Aktivität im Workflow und öffnen Sie sie unter Verwendung der Schaltfläche ![ in der Symbolleiste.](assets/edit_darkgrey-24px.png)

![](assets/wkf_advanced_parameters.png)

Im Feld **[!UICONTROL Ausführung]können Sie die Aktion definieren, die bei Aktivierung der Aufgabe ausgelöst werden soll.** Dabei stehen drei Optionen zur Wahl:

* **Normal** - die Aufgabe wird ausgeführt.
* **Aktivieren aber nicht ausführen** - die Aktivität wird ausgesetzt. Dies bedeutet, dass auch die nachfolgenden Aktivitäten nicht ausgeführt werden. Dies kann sich als nützlich erweisen, wenn Sie beispielsweise zum Zeitpunkt der Aufgabenaktivierung den Workflow überwachen möchten.
* **Nicht aktivieren** - die Aktivität sowie alle im selben Zweig folgenden Aktivitäten werden nicht ausgeführt.

Im Feld **[!UICONTROL Bei Fehler]lassen sich mögliche Reaktionen bei Auftreten eines Fehlers bestimmen.** Zwei Optionen stehen zur Wahl:

* **Prozess aussetzen** - der Workflow wird automatisch angehalten. Der Workflow-Status wechselt in **fehlerhaft** und sein Symbol wird rot hinterlegt. Nach Beseitigung der Fehlerursache kann der Workflow neu gestartet werden.
* **Ignorieren** - die den Fehler verursachende Aktivität sowie alle im selben Zweig folgenden Aktivitäten werden nicht ausgeführt. Diese Konfiguration empfiehlt sich bei wiederkehrenden Aufgaben. Wenn der Workflow-Zweig eine Planungsaktivität enthält, führt diese automatisch zum nächsten geplanten Zeitpunkt zu einer erneuten Ausführung.

Im Feld **[!UICONTROL Verhalten]können Sie das Verhalten des Workflows im Fall von asynchronen Aufgaben bestimmen.** Zwei Optionen stehen zur Wahl:

* **Mehrere autorisierte Aufgaben** - mehrere Aufgaben können gleichzeitig ausgeführt werden.
* **Laufende Aufgabe hat Vorrang** - solange eine Aufgabe läuft, wird keine neue Aufgabe gestartet. Solange eine Aufgabe läuft, wird keine neue Aufgabe gestartet.

The **[!UICONTROL Max. execution duration]** field allows you to specify a duration such as "30s" or "1h". Wenn eine Aufgabe die angegebene Dauer überschreitet, wird ein Warnhinweis erzeugt. Die Workflow-Ausführung wird hiervon jedoch nicht beeinflusst.

Das Feld **[!UICONTROL Affinität]bietet die Möglichkeit, die Ausführung eines Workflows oder einer Workflow-Aktivität an eine bestimmte Engine zu binden.** Hierzu müssen eine oder mehrere Affinitäten auf Workflow- oder Aktivitätsniveau definiert werden.

Im Feld **[!UICONTROL Zeitzone]können Sie der Aktivität eine bestimmte Zeitzone zuweisen.** Adobe Campaign ist in der Lage, verschiedene Zeitzonen innerhalb einer Instanz zu verwalten. Die entsprechenden Einstellungen werden bei der Instanzerstellung vorgenommen.

Im Feld **Kommentar** kann eine Bemerkung eingegeben werden. Es handelt sich um ein freies Textfeld.

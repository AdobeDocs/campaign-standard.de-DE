---
title: Workflows
description: Integration von Kampagne und Dynamik Workflows
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
translation-type: tm+mt
source-git-commit: 6be7a20cde8fcaee73972b8919765ea631f2f1ee
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 1%

---


# Kampagne - Microsoft Dynamics 365-Workflows

Auf der Seite **[!UICONTROL Workflows]** werden die Technischen Workflows und ihr Status Liste.

Die Integrationsanwendung umfasst drei Workflows:

![](assets/d365-to-acs-ui-page-workflows.png)

**Microsoft Dynamics 365 zur Kampagne**
* *Ansprechpartner* von Microsoft Dynamics 365 in Adobe Campaign senden
* *Benutzerdefinierte Entitäten*: Fügen Sie benutzerdefinierte Tabellen von Microsoft Dynamics 365 in Adobe Campaign ein. [Mehr dazu](../../integrating/using/d365-acs-using-the-integration.md#data-flows)
* Dies wird auch als **Ingress** (in Bezug auf die Erfassung von Daten von Microsoft Dynamics 365 zu Adobe Campaign) bezeichnet.

**Kampagne auf Microsoft Dynamics 365**
* E-Mail-Marketing-Ereignisse von Adobe Campaign Standard werden an Dynamics 365 gesendet (E-Mail senden, öffnen, klicken, springen). [Mehr dazu](../../integrating/using/d365-acs-using-the-integration.md#email-marketing-event-flow)
* Dies wird auch als **Egress** bezeichnet (bezogen auf den Datenfluss von Adobe Campaign zu Microsoft Dynamics 365)

**Teilnahme/Out**

Ausschlussstatus (z. B. Blockierungsliste) können von Microsoft Dynamics 365 zu Adobe Campaign oder von Adobe Campaign zu Microsoft Dynamics 365 synchronisiert werden. Die Daten können auch bidirektionell synchronisiert werden (d. h. Datenflüsse in beide Richtungen). [Weitere Informationen](../../integrating/using/d365-acs-self-service-app-data-sync.md#opt-in-out-wf).

>[!IMPORTANT]
>
>Es wird dringend empfohlen, den Arbeitsablauf **Microsoft Dynamics 365 zu Kampagne** zu beenden, bevor Sie Änderungen auf Adobe Campaign Standard oder Microsoft Dynamics 365 veröffentlichen. Zu diesen Änderungen gehören Aktualisierungen von Ressourcen/Entitäten (und den zugehörigen Feldern), Links, Bezeichnerspalten usw., die derzeit von der Integration verwendet werden. Andernfalls kann es zu Datenverlusten und/oder zu einem unerwarteten Beenden des Workflows kommen.

## Workflow-Backlog

Diese Integrationsanwendung liest zuerst in Daten und schreibt dann Daten an das Ziel. Die Spalte **[!UICONTROL Backlog]** gibt die Anzahl der Datensätze an, die in die Warteschlange gestellt wurden und darauf warten, geschrieben zu werden. Dieser Wert wird voraussichtlich zunehmen, wenn eine große Datenmenge verarbeitet werden muss (z. B. wenn Sie die Integration zum ersten Mal ausführen, die Daten erneut abspielen usw.).

>[!NOTE]
>Wenn Ihre Microsoft Dynamics 365- und/oder Kampagne-Datensätze nicht aktualisiert werden, sollten Sie zunächst prüfen, ob eine große Anzahl von Datensätzen auf die Aufnahme in das Ziel warten.


## Workflow status {#workflow-status}

Die Spalte **[!UICONTROL Status]** gibt den Status der Hintergrundprozesse an, die mit dem Workflow verknüpft sind. Mögliche Werte:

* **WIRD AUSGEFÜHRT**: Der Prozess wird derzeit ausgeführt und Ihre Daten sollten synchronisiert werden.
* **BEENDET**: Der Prozess wird derzeit nicht ausgeführt. Daher sollten Sie nicht erwarten, dass Ihre Daten synchronisiert werden.
* **BEGINN**: Sie haben angefordert, dass der Workflow in Beginn verarbeitet wird. Die Anwendung hat noch nicht begonnen, die mit diesem Workflow verknüpften Daten zu synchronisieren. Sie können jedoch davon ausgehen, dass die Synchronisierung nach einigen Minuten erfolgt (wenn der Status von **WIRD AUSGEFÜHRT** angezeigt wird)
* **FEHLGESCHLAGEN**: Die Workflow-Prozesse wurden ausgeführt, es traten jedoch Fehler auf und sie konnten nicht von diesen wiederhergestellt werden.

## Verfügbare Aktionen

Nachfolgend sind mögliche Aktionen aufgeführt.

* **Bearbeiten**: Durch Klicken auf das Stiftsymbol gelangen Sie zu einer anderen Seite, auf der Sie Aktualisierungen am Workflow vornehmen können. Denken Sie daran, dass Änderungen, die Sie vornehmen, erst dann wirksam werden, wenn Sie den Workflow beenden und dann neu starten.

* **Beginn**: Eine Schaltfläche &quot;Beginn&quot;fordert den Start eines angehaltenen Workflows an. Diese Schaltfläche wird nur angezeigt, wenn die mit dem Workflow verknüpften Prozesse aktuell beendet sind. Die Prozesse werden zuerst zu &quot;STARTEN&quot;und dann zu &quot;WIRD AUSGEFÜHRT&quot;geändert. Die mit dem Workflow verknüpften Daten werden erst dann synchronisiert, wenn der Workflow im Status &quot;WIRD AUSGEFÜHRT&quot;ausgeführt wird.

   Die Schaltfläche &quot;Beginn&quot;ist ein Umschalter. Wenn die Workflow-Prozesse bereits gestartet wurden, ändert sich die Schaltfläche in eine Schaltfläche **Stopp**.

* **Stopp**: Ein  **** Stopbutton fordert, dass ein ausgeführter Workflow beendet wird. Diese Schaltfläche wird nur angezeigt, wenn die mit dem Workflow verknüpften Prozesse aktuell ausgeführt werden.

Wenn Sie einen Workflow bearbeiten, werden Ihre Updates NICHT sofort in die Regeln der laufenden Prozesse integriert, bis Sie den Workflow beenden und dann auf die Schaltfläche **Beginn** klicken. Anschließend werden Ihre Updates in die laufenden Prozesse integriert (sobald der Prozess in den Status **AUSFÜHREN** zurückkehrt).

Der Schaltfläche **Stopp** wird eine Warnmeldung hinzugefügt, um Sie darüber zu informieren, wann Sie a) Aktualisierungen am Workflow vorgenommen haben, b) jedoch keinen Stopp/Beginn dieses Workflows durchgeführt haben.

![](assets/d365-to-acs-icon-stop-with-changes.png)

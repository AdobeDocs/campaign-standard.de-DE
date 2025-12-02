---
title: Workflows für die Integrationsanwendung
description: Workflows für die Integration von Campaign und Dynamics
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
feature: Microsoft CRM Integration
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 51f07f08-5d57-4c4c-aff2-d03e5956ec6f
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 100%

---

# Workflows für die Integration von Campaign und Microsoft Dynamics 365

Auf der Seite **[!UICONTROL Workflows]** sind die technischen Workflows und deren Status aufgelistet.

Für die Integrationsanwendung stehen drei Workflows zur Verfügung:

![](assets/do-not-localize/d365-to-acs-ui-page-workflows.png)

**Microsoft Dynamics 365 zu Campaign**
* Senden von *Kontakten* von Microsoft Dynamics 365 an Adobe Campaign.
* *Benutzerdefinierte Entitäten*: Einbinden von benutzerdefinierten Tabellen aus Microsoft Dynamics 365 in Campaign. [Mehr dazu](../../integrating/using/d365-acs-using-the-integration.md#data-flows)
* Dies wird auch als **Eingang** bezeichnet (und bezieht sich auf den Eingang von Daten von Microsoft Dynamics 365 in Adobe Campaign).

**Campaign zu Microsoft Dynamics 365**
* E-Mail-Marketing-Ereignisse von Adobe Campaign Standard werden an Dynamics 365 gesendet (E-Mail-Versand, Öffnung, Klick, Bounce). [Mehr dazu](../../integrating/using/d365-acs-using-the-integration.md#email-marketing-event-flow)
* Dies wird auch als **Ausgang** bezeichnet (und bezieht sich auf die Ausgabe von Daten von Adobe Campaign an Microsoft Dynamics 365).

**Opt-in/Opt-out**

Opt-out-Status (z. B. Blockierungsliste) können in Microsoft Dynamics 365 mit Adobe Campaign oder in Adobe Campaign mit Microsoft Dynamics 365 synchronisiert werden. Die Daten können auch bidirektional synchronisiert werden (d. h. Datenflüsse in beide Richtungen). [Weitere Informationen](../../integrating/using/d365-acs-self-service-app-data-sync.md#opt-in-out-wf).

>[!IMPORTANT]
>
>Es wird dringend empfohlen, den Workflow **Microsoft Dynamics 365 zu Campaign** zu stoppen, bevor Sie Änderungen in Adobe Campaign Standard oder Microsoft Dynamics 365 veröffentlichen. Zu diesen Änderungen gehören Aktualisierungen von Ressourcen/Entitäten (und den zugehörigen Feldern), Links, Spalten mit Kennungen usw., die derzeit von der Integration verwendet werden. Andernfalls kann es zu Datenverlusten und/oder zu einem unerwarteten Stopp des Workflows kommen.

## Workflow-Rückstand

Diese Integrationsanwendung liest zuerst Daten ein und schreibt dann Daten in das Ziel. Die Spalte **[!UICONTROL Rückstand]** gibt die Anzahl der Einträge an, die in die Warteschlange gestellt wurden und darauf warten, geschrieben zu werden. Es ist zu erwarten, dass dieser Wert zunimmt, wenn Sie eine große Datenmenge verarbeiten müssen (z. B. wenn Sie die Integration zum ersten Mal ausführen, die Daten erneut abspielen usw.). 

>[!NOTE]
>Wenn Ihre Microsoft Dynamics 365- und/oder Campaign-Datensätze nicht aktualisiert werden, sollten Sie zunächst prüfen, ob eine große Anzahl von Datensätzen darauf wartet, in das Ziel geschrieben zu werden.
>

## Workflow-Status {#workflow-status}

Die Spalte **[!UICONTROL Status]** gibt den Status der Hintergrundprozesse an, die mit dem Workflow verknüpft sind. Mögliche Werte:

* **WIRD AUSGEFÜHRT**: Der Prozess wird derzeit ausgeführt und Ihre Daten sollten synchronisiert werden.
* **ANGEHALTEN**: Der Prozess wird derzeit nicht ausgeführt. Ihre Daten werden daher nicht synchronisiert.
* **WIRD GESTARTET**: Sie haben angefordert, dass der Workflow-Prozess gestartet werden soll. Die Anwendung hat noch nicht begonnen, die mit diesem Workflow verknüpften Daten zu synchronisieren. Sie können jedoch davon ausgehen, dass die Synchronisation nach einigen Minuten erfolgt (dann wird der Status **WIRD AUSGEFÜHRT** angezeigt).
* **FEHLGESCHLAGEN**: Die Workflow-Prozesse wurden ausgeführt. Es sind aber Fehler aufgetreten, die nicht behoben werden konnten.

## Verfügbare Aktionen

Nachfolgend sind mögliche Aktionen aufgeführt.

* **Bearbeiten**: Durch Klicken auf das Stiftsymbol gelangen Sie zu einer anderen Seite, auf der Sie Änderungen am Workflow vornehmen können. Beachten Sie, dass vorgenommene Änderungen erst dann wirksam werden, wenn Sie den Workflow anhalten und wieder neu starten.

* **Starten**: Mit der Schaltfläche &quot;Start&quot; können Sie einen angehaltenen Workflow wieder starten. Diese Schaltfläche wird nur angezeigt, wenn die mit dem Workflow verbundenen Prozesse derzeit angehalten sind. Die Prozesse ändern sich zuerst in &quot;WIRD GESTARTET&quot; und dann in &quot;WIRD AUSGEFÜHRT&quot;. Die mit dem Workflow verknüpften Daten werden erst dann synchronisiert, wenn sich der Workflow im Zustand &quot;WIRD AUSGEFÜHRT&quot; befindet.

  Die Schaltfläche &quot;Starten&quot; ist ein Umschalter. Wenn die Workflow-Prozesse bereits gestartet wurden, ändert sich die Schaltfläche in eine **Stoppen**-Schaltfläche.

* **Anhalten**: Mit einer **Anhalten**-Schaltfläche können Sie einen laufenden Workflow anhalten. Diese Schaltfläche wird nur angezeigt, wenn die mit dem Workflow verknüpften Prozesse aktuell ausgeführt werden.

Wenn Sie einen Workflow bearbeiten, werden Ihre Aktualisierungen NICHT sofort in die Regeln der laufenden Prozesse übernommen. Dazu müssen Sie den Workflow zuerst anhalten und dann auf die Schaltfläche **Starten** klicken. Anschließend werden Ihre Aktualisierungen in die laufenden Prozesse integriert (sobald der Prozess in den Status **WIRD AUSGEFÜHRT** zurückkehrt).

Die Schaltfläche **Anhalten** gibt eine Warnmeldung aus, wenn Sie (a) Aktualisierungen am Workflow vorgenommen haben, aber (b) diesen Workflow noch nicht angehalten und wieder gestartet haben.

![](assets/do-not-localize/d365-to-acs-icon-stop-with-changes.png)

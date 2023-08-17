---
title: Push-Benachrichtigungsversand
description: Die Aktivität zum Push-Benachrichtigungsversand ermöglicht den Versand von einmaligen oder wiederkehrenden Push-Benachrichtigungen innerhalb eines Workflows.
audience: automating
content-type: reference
topic-tags: channel-activities
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: b6a43d51-32d4-4806-b4e4-33236f1e27f5
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 100%

---

# Push-Benachrichtigungsversand{#push-notification-delivery}

## Beschreibung {#description}

![](assets/push.png)

![](assets/recurrentpush.png)

Die Aktivität **[!UICONTROL Push-Benachrichtigung]** ermöglicht das Konfigurieren des Versands von Push-Benachrichtigungen innerhalb eines Workflows. Diese Benachrichtigung kann einmalig sein oder wiederkehrend.

* **Einmalige** Benachrichtigungen sind standardmäßige Mobile-App-Push-Benachrichtigungen, die einmal gesendet werden.
* **Wiederkehrende** Versandaktionen ermöglichen den wiederholten Versand der gleichen Mobile-App-Push-Benachrichtigung über einen bestimmten Zeitraum an verschiedene Zielgruppen. Für Berichtzwecke können bei Bedarf die einzelnen Sendungen nach Zeiträumen aggregiert werden.

## Anwendungskontext          {#context-of-use}

Die Aktivität **[!UICONTROL Push-Benachrichtigung]** dient im Allgemeinen dazu, den Versand von Benachrichtigungen an eine innerhalb des gleichen Workflows berechnete Zielgruppe zu automatisieren.

In Verbindung mit einer Planungsaktivität ist es möglich, wiederkehrende Push-Benachrichtigungen zu konfigurieren.

Die Empfänger werden in vorangeschalteten Zielgruppenbestimmungsaktivitäten des Workflows, wie beispielsweise Abfragen, Schnittmengen etc. definiert.

Die Vorbereitung der Nachricht wird in Abhängigkeit von den Ausführungsparametern des Workflows ausgelöst. Sie können im Nachrichten-Dashboard auswählen, ob eine manuelle Bestätigung zum Nachrichtenversand erforderlich ist oder nicht (standardmäßig erforderlich). Sie können den Workflow entweder manuell starten oder eine Planung verwenden, um die Ausführung zu automatisieren.

**Verwandte Themen**

* [Wiederkehrende Push-Benachrichtigung mithilfe von Workflows versenden](../../automating/using/recurring-push-notifications.md)

## Konfiguration {#configuration}

1. Ziehen Sie die Aktivität **[!UICONTROL Push-Benachrichtigung]** in Ihren Workflow.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der in der Schnellaktion angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).

   >[!NOTE]
   >
   >Die Schaltfläche ![](assets/dlv_activity_params-24px.png) iin der Schnellaktion bietet Zugriff auf die allgemeinen Eigenschaften und erweiterten Optionen der Aktivität (aber nicht des Versands selbst). Diese Schaltfläche ist speziell für die Aktivität **[!UICONTROL Push-Benachrichtigung]** vorgesehen. Auf die Eigenschaften der Push-Benachrichtigung können Sie über die Aktionsleiste des Push-Dashboards zugreifen.

1. Wählen Sie den Versandtyp der Push-Benachrichtigung aus:

   * **[!UICONTROL Einzelne Benachrichtigung]**: Die Push-Benachrichtigung wird ein einziges Mal versendet. Sie können an dieser Stelle entscheiden, ob Sie der Aktivität eine ausgehende Transition hinzufügen möchten oder nicht. Die unterschiedlichen Transitionstypen werden in Etappe 7 dieser Prozedur beschrieben.
   * **[!UICONTROL Wiederkehrende Benachrichtigung]**: Die Push-Benachrichtigung wird wiederholt versendet. Die Frequenz des Versands wird in der Aktivität **[!UICONTROL Planung]** definiert. Wählen Sie einen Aggregatzeitraum für die wiederkehrenden Sendungen aus. Auf diese Weise werden alle Sendungen, die im angegebenen Zeitraum versendet wurden, in einer Push-Benachrichtigung zusammengefasst, die auch **wiederkehrende Ausführung** genannt wird. Diese ist in der Marketing-Aktivitätenliste der Anwendung zugänglich.

     Es besteht beispielsweise die Möglichkeit, die Ausführungen einer täglich gesendeten Geburtstagsnachricht pro Monat zu aggregieren. Auf diese Weise lässt sich ein monatlicher Versandbericht für eine täglich gesendete Nachrichten generieren.

1. Wählen Sie einen Benachrichtigungstyp aus. Die Typen stammen aus Push-Benachrichtigungsvorlagen, die im Menü **[!UICONTROL Ressourcen]** > **[!UICONTROL Vorlagen]** > **[!UICONTROL Versandvorlagen]** definiert sind.
1. Bestimmen Sie die allgemeinen Eigenschaften für die Push-Benachrichtigung und ordnen Sie sie gegebenenfalls einer existierenden Kampagne zu. Der Titel der Versandaktivität des Workflows wird mit dem Titel der Push-Benachrichtigung aktualisiert.
1. Definieren Sie den Inhalt der Push-Benachrichtigung. Siehe [Push-Benachrichtigungen erstellen](../../channels/using/preparing-and-sending-a-push-notification.md).
1. Die Aktivität **[!UICONTROL Push-Benachrichtigung]** verfügt standardmäßig über keinerlei ausgehende Transitionen. Wenn Sie der Aktivität **[!UICONTROL Push-Benachrichtigung]** eine ausgehende Transition hinzufügen möchten, gehen Sie zum Tab **[!UICONTROL Allgemein]** der erweiterten Aktivitätsoptionen (Schaltfläche ![](assets/dlv_activity_params-24px.png) in der Schnellaktion der Aktivität) und aktivieren Sie eine der folgenden Optionen:

   * **[!UICONTROL Ausgehende Transition ohne Population hinzufügen]**: ermöglicht die Erstellung einer ausgehenden Transition, die exakt dieselbe Population enthält wie die eingehende Transition.
   * **[!UICONTROL Ausgehende Transition mit Population hinzufügen]**: ermöglicht die Erstellung einer ausgehenden Transition, die die Population enthält, der die Benachrichtigung gesendet wurde. Der Teil der Zielgruppe, der in der Versandvorbereitung ausgeschlossen wurde, ist von dieser Transition ebenfalls ausgeschlossen.

1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

Wenn Sie die Aktivität später erneut öffnen, gelangen Sie direkt in das Dashboard der Push-Benachrichtigung. Nur der Inhalt kann zu diesem Zeitpunkt noch geändert werden.

Standardmäßig wird durch den Versand-Workflow nur die Vorbereitung der Nachricht ausgelöst. Der in einem Workflow erstellte Nachrichtenversand muss noch bestätigt werden, nachdem der Workflow gestartet wurde. Sie können aber im Nachrichten-Dashboard die Option **[!UICONTROL Vor dem Nachrichtenversand Bestätigung einholen]** deaktivieren. Dies ist jedoch nur möglich, wenn die Nachricht in einem Workflow erstellt wurde. Ist diese Option deaktiviert, werden Nachrichten ohne weiteren Hinweis gesendet, sobald die Vorbereitung abgeschlossen ist.

## Bemerkungen          {#remarks}

Auf die von einem Workflow aus erstellten Sendungen kann in der Marketing-Aktivitätenliste der Anwendung zugegriffen werden. Über das Dashboard lässt sich der Ausführungsstatus des Workflows visualisieren. Über die Links im Übersichtsmenü der Push-Benachrichtigung können Sie direkt auf verknüpfte Elemente wie den Workflow oder die Kampagne zugreifen.

Ausgehend von den übergeordneten Sendungen, auf die über die Liste der Marketing-Aktivitäten zugegriffen werden kann, lässt sich die Gesamtheit aller getätigten Sendungen visualisieren (in Abhängigkeit vom bei der Konfiguration der **[!UICONTROL Push-Benachrichtigung]** festgelegten Aggregat-Zeitraum). Öffnen Sie hierzu mithilfe der **[!UICONTROL -Schaltfläche die Detailansicht der Kachel]** Bereitstellung![](assets/wkf_dlv_detail_button.png) des übergeordneten Versands.

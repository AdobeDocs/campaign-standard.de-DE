---
title: Push-Benachrichtigungsversand
description: Die Aktivität zum Push-Benachrichtigungsversand ermöglicht den Versand von einmaligen oder wiederkehrenden Push-Benachrichtigungen innerhalb eines Workflows.
page-status-flag: never-activated
uuid: 994d8fe3-29f0-4b5c-89ee-c6be7c60a31b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: channel-activities
discoiquuid: e61bdaee-4b48-4845-a2a5-574b577ea796
internal: n
snippet: y
translation-type: ht
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Push-Benachrichtigungsversand{#push-notification-delivery}

## Beschreibung {#description}

![](assets/push.png)

![](assets/recurrentpush.png)

Die Aktivität **[!UICONTROL Push-Benachrichtigung]** ermöglicht das Konfigurieren des Versands von Push-Benachrichtigungen innerhalb eines Workflows. Diese Benachrichtigung kann **einmalig** sein oder **wiederkehrend**.

Einmalige Benachrichtigungen sind standardmäßige Mobile-App-Push-Benachrichtigungen, die einmal gesendet werden.

Wiederkehrende Versandaktionen ermöglichen den wiederholten Versand der gleichen Mobile-App-Push-Benachrichtigung über einen bestimmten Zeitraum an verschiedene Zielgruppen. Für Berichtzwecke können bei Bedarf die einzelnen Sendungen nach Zeiträumen aggregiert werden.

## Anwendungskontext {#context-of-use}

Die Aktivität **[!UICONTROL Push-Benachrichtigung]** dient im Allgemeinen dazu, den Versand von Benachrichtigungen an eine innerhalb des gleichen Workflows berechnete Zielgruppe zu automatisieren.

In Verbindung mit einer Planungsaktivität ist es möglich, wiederkehrende Push-Benachrichtigungen zu konfigurieren.

Die Empfänger werden in vorangeschalteten Zielgruppenbestimmungsaktivitäten des Workflows, wie beispielsweise Abfragen, Schnittmengen etc. definiert.

Die Vorbereitung der Nachricht wird in Abhängigkeit von den Ausführungsparametern des Workflows ausgelöst. Sie können im Nachrichten-Dashboard auswählen, ob eine manuelle Bestätigung zum Nachrichtenversand erforderlich ist oder nicht (standardmäßig erforderlich). Sie können den Workflow entweder manuell starten oder eine Planung verwenden, um die Ausführung zu automatisieren.

## Konfiguration {#configuration}

1. Ziehen Sie die Aktivität **[!UICONTROL Push-Benachrichtigung]** in Ihren Workflow.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der ![](assets/edit_darkgrey-24px.png)-Schaltfläche aus den angezeigten Quick Actions.

   >[!NOTE]
   >
   >Die Schaltfläche ![](assets/dlv_activity_params-24px.png) in den Quick Actions bietet Zugriff auf die allgemeinen Eigenschaften und erweiterten Optionen der Aktivität (nicht des Versands selbst). Diese Schaltfläche ist speziell für die Aktivität **[!UICONTROL Push-Benachrichtigung]** vorgesehen. Auf die Eigenschaften der Push-Benachrichtigung können Sie über die Symbolleiste des Push-Dashboards zugreifen.

1. Wählen Sie den Versandtyp der Push-Benachrichtigung aus:

   * **[!UICONTROL Einzelne Benachrichtigung]**: Die Push-Benachrichtigung wird ein einziges Mal versendet. Sie können an dieser Stelle entscheiden, ob Sie der Aktivität eine ausgehende Transition hinzufügen möchten oder nicht. Die unterschiedlichen Transitionstypen werden in Etappe 7 dieser Prozedur beschrieben.
   * **[!UICONTROL Wiederkehrende Benachrichtigung]**: Die Push-Benachrichtigung wird wiederholt versendet. Die Frequenz des Versands wird in einer vorangeschalteten **[!UICONTROL Planung]** definiert. Wählen Sie einen Aggregatzeitraum für die wiederkehrenden Sendungen aus. Auf diese Weise werden alle Sendungen, die im angegebenen Zeitraum versendet wurden, in einer Push-Benachrichtigung zusammengefasst, die auch **wiederkehrende Ausführung** genannt wird. Diese ist in der Marketingaktivitätenliste der Anwendung zugänglich.

      Es besteht beispielsweise die Möglichkeit, die Ausführungen einer täglich gesendeten Geburtstagsnachricht pro Monat zu aggregieren. Auf diese Weise lässt sich ein monatlicher Versandbericht für eine täglich gesendete Nachrichten generieren.

1. Wählen Sie einen Benachrichtigungstyp aus. Die Typen stammen aus Push-Benachrichtigungsvorlagen, die im Menü **[!UICONTROL Ressourcen]** &gt; **[!UICONTROL Vorlagen]** &gt; **[!UICONTROL Versandvorlagen]** definiert sind.
1. Bestimmen Sie die allgemeinen Eigenschaften für die Push-Benachrichtigung und ordnen Sie sie gegebenenfalls einer existierenden Kampagne zu. Der Titel der Versandaktivität des Workflows wird mit dem Titel der Push-Benachrichtigung aktualisiert.
1. Definieren Sie den Inhalt der Push-Benachrichtigung. Siehe [Push-Benachrichtigungen erstellen](../../channels/using/preparing-and-sending-a-push-notification.md).
1. Die Aktivität **[!UICONTROL Push-Benachrichtigung]** verfügt standardmäßig über keinerlei ausgehende Transitionen. Sie haben jedoch die Möglichkeit, zu Ihrer Aktivität **[!UICONTROL Push-Benachrichtigung]** eine ausgehende Transition zu erzeugen, indem Sie unter Verwendung der in den Quick Actions der Aktivität verfügbaren ![](assets/dlv_activity_params-24px.png) Schaltfläche die erweiterten Optionen öffnen und im **[!UICONTROL Allgemein]**-Tab eine der folgenden Optionen aktivieren:

   * **[!UICONTROL Ausgehende Transition ohne Population hinzufügen]**: ermöglicht die Erstellung einer ausgehenden Transition, die exakt dieselbe Population enthält wie die eingehende Transition.
   * **[!UICONTROL Ausgehende Transition mit Population hinzufügen]**: ermöglicht die Erstellung einer ausgehenden Transition, die die Population enthält, der die Benachrichtigung gesendet wurde. Der Teil der Zielgruppe, der in der Versandvorbereitung ausgeschlossen wurde, ist von dieser Transition ebenfalls ausgeschlossen.

1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

Wenn Sie die Aktivität später erneut öffnen, gelangen Sie direkt in das Dashboard der Push-Benachrichtigung. Nur der Inhalt kann zu diesem Zeitpunkt noch geändert werden.

Standardmäßig wird durch den Versand-Workflow nur die Vorbereitung der Nachricht ausgelöst. Der in einem Workflow erstellte Nachrichtenversand muss noch bestätigt werden, nachdem der Workflow gestartet wurde. Sie können aber im Nachrichten-Dashboard die Option **[!UICONTROL Vor dem Nachrichtenversand Bestätigung einholen]** deaktivieren. Dies ist jedoch nur möglich, wenn die Nachricht in einem Workflow erstellt wurde. Ist diese Option deaktiviert, werden Nachrichten ohne weiteren Hinweis gesendet, sobald die Vorbereitung abgeschlossen ist.

## Bemerkungen {#remarks}

Auf die von einem Workflow aus erstellten Sendungen kann in der Marketingaktivitätenliste der Anwendung zugegriffen werden. Über das Dashboard lässt sich der Ausführungsstatus des Workflows visualisieren. Über die Links im Übersichtsmenü der Push-Benachrichtigung können Sie direkt auf verknüpfte Elemente wie den Workflow oder die Kampagne zugreifen.

Ausgehend von den Elternsendungen, auf die über die Marketingaktivitätenliste zugegriffen werden kann, lässt sich die Gesamtheit aller getätigten Sendungen visualisieren (in Abhängigkeit vom bei der Konfiguration der **[!UICONTROL Push-Benachrichtigung]** festgelegten Aggregat-Zeitraum). Öffnen Sie hierzu mithilfe der ![](assets/wkf_dlv_detail_button.png)-Schaltfläche die Detailansicht der **[!UICONTROL Freigabe]**-Kachel des Elternversands.

## Wiederkehrende Push-Benachrichtigung mithilfe von Workflows versenden {#sending-a-recurring-push-notification-with-a-workflow}

![](assets/wkf_push_example_1.png)

In diesem Beispiel wird eine personalisierte Push-Benachrichtigung am ersten Tag des Monats um 20 Uhr an die Abonnenten Ihrer Mobile App in ihrer jeweiligen Zeitzone gesendet. Gehen Sie wie folgt vor:

1. Die Aktivität **[!UICONTROL Planung]** ermöglicht es Ihnen, den Workflow schon Tage vor dem Versand zu aktivieren, damit Sie die Benachrichtigung jedem Abonnenten um 20 Uhr in seiner Zeitzone senden können:

   * Wählen Sie im Feld **[!UICONTROL Ausführungsfrequenz]** die Option "Monatlich" aus.
   * Wählen Sie im Feld **[!UICONTROL Uhrzeit]** 20 Uhr aus.
   * Wählen Sie aus, an welchem Tag im Monat der Versand stattfinden soll.
   * Wählen Sie ein Startdatum für Ihren Workflow aus. Dieses sollte mindestens einen Tag vor dem Beginn des Versands sein. Ansonsten könnten Empfänger die Nachricht einen Tag zu spät erhalten, wenn die ausgewählte Uhrzeit in ihrer Zeitzone bereits vorüber ist.
   * Wählen Sie im Tab **[!UICONTROL Ausführungsoptionen]** im Feld **[!UICONTROL Zeitzone]** aus, in welcher Zeitzone Ihr Workflow starten soll. In unserem Beispiel beginnt der Workflow um 20 Uhr (Pacific Time) eine Woche vor dem ersten Tag im Monat. Damit bleibt genügend Zeit, die Sendungen für alle Zeitzonen zu erstellen.
   ![](assets/wkf_push_example_5.png)

1. Mithilfe der Aktivität **Abfrage** können Sie als Zielgruppe Ihre VIP-Kunden im Alter zwischen 20 und 30 Jahren festlegen, die Ihre mobile App abonniert und die von Ihnen gesendete E-Mail nicht geöffnet haben:

   * Wählen Sie eine Audience (Ihre VIP-Kunden) aus und legen Sie einen Altersfilter fest.
   * Ziehen Sie das Element **App-Abonnements** in den Arbeitsbereich. Wählen Sie **Existiert** und dann die Mobile App aus, die Sie verwenden möchten.
   * Wählen Sie die E-Mail aus, die Sie an Ihre Kunden geschickt haben.
   * Ziehen Sie das Element **Versandlogs (logs)** in den Arbeitsbereich und wählen Sie **Existiert** aus, um alle Kunden in die Zielgruppe einzuschließen, die die E-Mail erhalten haben.
   * Ziehen Sie das Element **Trackinglogs (tracking)** in den Arbeitsbereich und wählen Sie **Existiert nicht** aus, um nur Kunden in die Zielgruppe einzuschließen, die die E-Mail nicht geöffnet haben.

      ![](assets/wkf_push_example_2.png)

1. Definieren Sie dann über die Aktivität **Push-Benachrichtigung** den Inhalt der Nachricht. Sie haben die Möglichkeit, sie unter Verwendung von Personalisierungsfeldern an den jeweiligen Empfänger anzupassen.

   * Wählen Sie die Option **[!UICONTROL Wiederkehrende Benachrichtigung]** aus.
   * Definieren Sie den Inhalt der Push-Benachrichtigung. Nähere Informationen zum Inhalt von Push-Benachrichtigungen erhalten Sie in [diesem Abschnitt](../../channels/using/preparing-and-sending-a-push-notification.md).
   * Wählen Sie im Fenster **[!UICONTROL Planung]** die Option **[!UICONTROL Nachrichten werden automatisch in der unten spezifizierten Zeitzone gesendet]** aus. In unserem Beispiel wählen wir im Workflow **[!UICONTROL Planung**] als **[!UICONTROL Zeitzone des Kontaktdatums]** "Pacific" aus.
   * Wählen Sie im Feld **[!UICONTROL Versandzeitpunkt für jeden Empfänger optimieren]** die Option **[!UICONTROL In der Zeitzone des Empfängers senden]** aus.

      ![](assets/wkf_push_example_4.png)

1. Wählen Sie nun zur Ausführung des wiederkehrenden Workflows die Schaltfläche **[!UICONTROL Starten]** aus.

   ![](assets/wkf_push_example_3.png)

Ihr Workflow wird jetzt ausgeführt. Er beginnt an dem in der **[!UICONTROL Planung]** ausgewählten Startdatum, also um 20 Uhr Pacific Time, und die wiederkehrende Push-Benachrichtigung wird jeden ersten Tag im Monat um 20 Uhr in der Zeitzone des Kunden gesendet.

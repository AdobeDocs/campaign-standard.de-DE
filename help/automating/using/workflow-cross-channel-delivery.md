---
title: '"Anwendungsfall des Arbeitsablaufs: Kanalübergreifende Bereitstellung"'
description: '"Anwendungsfall des Arbeitsablaufs: Kanalübergreifende Bereitstellung"'
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow,use-case,query,wait,delivery
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f959441647d1fea41ecce2fc41e3cad3cb536bac

---


# Workflow use-case: Creating a cross-channel delivery{#cross-channel-delivery}

Anhand dieses typischen Anwendungsbeispiels wird insbesondere die folgende Adobe-Campaign-Funktion vorgestellt: Erstellung eines Workflows zum kanalübergreifenden Versand.

Das Ziel besteht darin, aus den Empfängern der Datenbank eine Audience auszuwählen und diese in zwei gesonderte Gruppen zu unterteilen, um der ersten Gruppe eine E-Mail und der zweiten Gruppe eine SMS zukommen zu lassen.

![](assets/wkf_segment_overview.png)

Weiterführende Informationen zu Workflows und den in Adobe Campaign verfügbaren Kanälen finden Sie in den folgenden Dokumenten:

* [Workflows](../../automating/using/discovering-workflows.md)
* [Kommunikationskanäle](../../channels/using/discovering-communication-channels.md)

## Workflow erstellen  {#creating-workflow}

Bestimmen Sie im ersten Schritt die Zielgruppe, die Sie mit Ihrer Kommunikation erreichen möchten. Nachfolgend wird diese dann je nach Kommunikationsmedium in zwei Gruppen unterteilt.

Hierzu sind zur Identifizierung der Empfänger die Erstellung einer Abfrage und zur anschließenden Segmentierung die Erstellung eines Workflows notwendig.

Erstellen Sie also innerhalb des Programms oder der Kampagne Ihrer Wahl einen neuen Workflow:

1. Wählen Sie dazu in **[!UICONTROL Marketingaktivitäten]**die Option**[!UICONTROL  Erstellen]** und dann **[!UICONTROL Workflow]**aus.
1. Wählen Sie als Workflow-Typ **[!UICONTROL Neuer Workflow]**und danach**[!UICONTROL  Weiter]** aus.
1. Geben Sie die Eigenschaften des Workflows ein und wählen Sie **[!UICONTROL Erstellen]**aus.

Die detaillierten Schritte zum Erstellen eines Workflows werden im Abschnitt [Workflow erstellen](../../automating/using/building-a-workflow.md) beschrieben.

## Abfrageaktivität erstellen {#creating-query-activity}.

Nach der Erstellung des Workflows werden Sie zu dessen Arbeitsbereich weitergeleitet.

Fügen Sie eine Abfrageaktivität in Ihren Workflow ein, um die Profile, die Ihre Auslieferungen erhalten, als Ziel festzulegen.

1. In **[!UICONTROL Activities]**>**[!UICONTROL  Targeting]**, drag and drop a **[!UICONTROL Query activity]**.
1. Doppelklicken Sie auf die Aktivität.
1. Durchsuchen Sie auf der Registerkarte &quot; **[!UICONTROL Target]**&quot;die Verknüpfungen und wählen Sie eine Ihrer[Zielgruppen](../../audiences/using/about-audiences.md)aus.
1. Ziehen Sie den Schnellzugriff in den Arbeitsbereich. Je nach Typ des ausgewählten Schnellzugriffs öffnet sich ein bestimmtes Fenster.
1. Konfigurieren Sie die Zielgruppenbestimmungselemente und validieren Sie Ihre Abfrage.

![](assets/wkf_segment_query.png)

Sie können eine auf ein oder mehrere Element(e) bezogene Abfrage erstellen.

Verwenden Sie die Schaltfläche **[!UICONTROL Zählung]**, um die Anzahl an Profilen angezeigt zu bekommen, auf die die Abfrage zutrifft.

Die detaillierten Schritte zum Erstellen einer Abfrageaktivität werden im Abschnitt [Abfrage](../../automating/using/query.md) beschrieben.

## Segmentierungsaktivität erstellen{#creating-segmentation-activity}.

Unterteilen Sie im nächsten Schritt Ihre mithilfe der Abfrage-Aktivität bestimmte Zielgruppe in zwei Segmente: das eine erhält eine E-Mail, das andere eine SMS.

Verwenden Sie hierzu die Aktivität Segmentierung, um die zuvor ermittelte Population in zwei Segmente zu unterteilen.

![](assets/wkf_segment_activity.png)

Die erste Gruppe namens **E-Mail** enthält jene Empfänger, die ihre E-Mail-Adresse, aber keine Mobiltelefonnummer angegeben haben. Die zweite Gruppe namens **SMS** enthält jene Empfänger, deren Profil eine Mobiltelefonnummer aufweist.

So konfigurieren Sie den ersten Übergang (E-Mail):

1. Auf der Registerkarte &quot; **[!UICONTROL Segmente]**&quot;ist standardmäßig ein erstes Segment vorhanden. Bearbeiten Sie die Eigenschaften, um dieses Segment zu konfigurieren.

   ![](assets/wkf_segment_properties.png)

1. Wählen Sie als Filterkriterium die **[!UICONTROL E-Mail]**des Profils aus.

   ![](assets/wkf_segment_email.png)

1. Wählen Sie im neuen Fenster, das auf dem Bildschirm angezeigt wird, den Operator **[!UICONTROL Ist nicht leer]**.

   ![](assets/wkf_segment_email_not_empty.png)

1. Add a second filtering criterion, **[!UICONTROL Mobile]**, and select the operator**[!UICONTROL  Is empty]**.

   ![](assets/wkf_segment_mobile_empty.png)

   Alle Profile, die aus der Abfrage stammen, die eine E-Mail, aber keine Mobiltelefonnummer definiert haben, befinden sich in diesem Übergang.

1. Bei Bedarf können Sie den Titel der Transition zwecks einer besseren Übersichtlichkeit des Workflows anpassen. Bestätigen Sie Ihre Änderungen.

   ![](assets/wkf_segment_transition_label.png)

Die Konfiguration Ihrer ersten Transition ist abgeschlossen. Konfigurieren des zweiten Übergangs (SMS):

1. Verwenden Sie die Schaltfläche **[!UICONTROL Element hinzufügen]**, um eine neue Transition hinzuzufügen.
1. Definieren Sie eine Bedingung, mit der Sie alle Profile abrufen können, deren Handynummern angegeben wurden. Erstellen Sie dazu eine Regel im Feld **[!UICONTROL Mobil]**mit dem logischen Operator**[!UICONTROL  Ist nicht leer]** .

   ![](assets/wkf_segment_mobile_not_empty.png)

   Alle Profile, die von der Abfrage stammen und eine Mobiltelefonnummer definiert haben, befinden sich in diesem Übergang.

1. Sie können die Beschriftung des Übergangs bearbeiten. Bestätigen Sie Ihre Änderungen.

Der zweite Übergang ist jetzt ebenfalls konfiguriert.

![](assets/wkf_segment_transitions.png)

Die detaillierten Schritte zum Erstellen einer Segmentierungsaktivität werden im Abschnitt [Segmentierung](../../automating/using/segmentation.md) beschrieben.

## Sendungen erstellen {#creating-deliveries}

As two transitions were already created, you must now add two types of deliveries to the outbound transitions of the Segmentation activity: an **[!UICONTROL Email delivery]**and an**[!UICONTROL  SMS delivery]**.

Adobe Campaign bietet die Möglichkeit, innerhalb von Workflows Sendungen zu konfigurieren. Wählen Sie hierzu in der Kategorie **[!UICONTROL Kanäle]**der Aktivitätenpalette Ihres Workflows einen Versand aus.

![](assets/wkf_segment_deliveries1.png)

So erstellen Sie eine E-Mail-Auslieferung:

1. Drag and drop an **[!UICONTROL Email delivery]**after the first segment.
1. Doppelklicken Sie auf die Aktivität, um sie zu bearbeiten.
1. Wählen Sie **[!UICONTROL Einfache E-Mail]**.
1. Select **[!UICONTROL Add an outbound transition with the population]**and click**[!UICONTROL  Next]**.

   ![](assets/wkf_segment_deliveries2.png)

   Mit dem ausgehenden Übergang können Sie die Population und die Verfolgungsprotokolle wiederherstellen. Sie können dies beispielsweise verwenden, um eine zweite Mail an die Personen zu senden, die nicht in der ersten Mail geklickt haben.

1. Wählen Sie eine E-Mail-Vorlage und danach **[!UICONTROL Weiter]**aus.
1. Geben Sie die E-Mail-Eigenschaften ein und wählen Sie **[!UICONTROL Weiter]**aus.
1. To create the layout of your email, select **[!UICONTROL Use the Email Designer]**.
1. Bearbeiten und speichern Sie Ihre Inhalte.
1. Deaktivieren Sie im Nachrichten-Dashboard im Bereich **[!UICONTROL Planung]**die Option**[!UICONTROL Vor dem Nachrichtenversand Bestätigung einholen]**.

Die detaillierten Schritte zum Erstellen einer E-Mail-Aktivität finden Sie im Abschnitt [E-Mail-Versand](../../automating/using/email-delivery.md).

So erstellen Sie eine SMS-Auslieferung:

1. Drag and drop an **[!UICONTROL SMS delivery]**after the other segment.
1. Doppelklicken Sie auf die Aktivität, um sie zu bearbeiten.
1. Select **[!UICONTROL SMS]**and click**[!UICONTROL  Next]**.
1. Select an SMS template and click **[!UICONTROL Next]**.
1. Enter the SMS properties and click **[!UICONTROL Next]**.
1. Bearbeiten und speichern Sie Ihre Inhalte.

The detailed steps to build an SMS activity are presented in the [SMS delivery](../../automating/using/sms-delivery.md) section.

Nach der Konfiguration Ihrer Sendungen kann der Workflow gestartet werden.

![](assets/wkf_segment_deliveries.png)

## Workflow ausführen {#running-the-workflow}

Sobald der Workflow gestartet wurde, wird die Zielgruppe der Abfrageaktivität segmentiert, um eine E-Mail- oder SMS-Zustellung zu erhalten.

To execute your workflow, click the **[!UICONTROL Start]**button from the action bar.

You can access your deliveries from the **[!UICONTROL Marketing plans]**>**[!UICONTROL  Marketing activities]** advanced menu via the Adobe Campaign logo. Click the delivery then the **[!UICONTROL Reports]**button to access the[delivery reports](../../reporting/using/about-dynamic-reports.md#accessing-dynamic-reports), such as the delivery summary, the open rate or the email rendering according to the recipients&#39; message inbox.
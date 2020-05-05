---
title: '„Workflow-Anwendungsbeispiel: Kanalübergreifender Versand"'
description: '"Workflow-Anwendungsbeispiel: Kanalübergreifender Versand"'
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
source-git-commit: 68e825bc3b6b7f94f61875e7da2bc8f63f06d9cb

---


# Workflow-Anwendungsbeispiel: Kanalübergreifenden Versand erstellen{#cross-channel-delivery}

Anhand dieses typischen Anwendungsbeispiels wird insbesondere die folgende Adobe-Campaign-Funktion vorgestellt: Erstellung eines Workflows zum kanalübergreifenden Versand.

Das Ziel besteht darin, aus den Empfängern der Datenbank eine Audience auszuwählen und diese in zwei gesonderte Gruppen zu unterteilen, um der ersten Gruppe eine E-Mail und der zweiten Gruppe eine SMS zukommen zu lassen.

![](assets/wkf_segment_overview.png)

Weiterführende Informationen zu Workflows und den in Adobe Campaign verfügbaren Kanälen finden Sie in den folgenden Dokumenten:

* [Workflows](../../automating/using/get-started-workflows.md)
* [Kommunikationskanäle](../../channels/using/get-started-communication-channels.md)

## Workflow erstellen   {#creating-workflow}

Bestimmen Sie im ersten Schritt die Zielgruppe, die Sie mit Ihrer Kommunikation erreichen möchten. Nachfolgend wird diese dann je nach Kommunikationsmedium in zwei Gruppen unterteilt.

Hierzu sind zur Identifizierung der Empfänger die Erstellung einer Abfrage und zur anschließenden Segmentierung die Erstellung eines Workflows notwendig.

Erstellen Sie also innerhalb des Programms oder der Kampagne Ihrer Wahl einen neuen Workflow:

1. Klicken Sie in **[!UICONTROL Marketing Activities]** und wählen Sie **[!UICONTROL Create]** **[!UICONTROL Workflow]** aus.
1. Wählen Sie **[!UICONTROL New Workflow]** als Workflow-Typ aus und klicken Sie auf **[!UICONTROL Next]**.
1. Enter the properties of the workflow and click **[!UICONTROL Create]**.

Die detaillierten Schritte zum Erstellen eines Workflows werden im Abschnitt [Workflow erstellen](../../automating/using/building-a-workflow.md) beschrieben.

## Abfrageaktivität erstellen {#creating-query-activity}.

Nach der Erstellung des Workflows werden Sie zu dessen Arbeitsbereich weitergeleitet.

Ziehen Sie eine Abfrage in Ihren Workflow, um die mittels Ihrer Sendungen zu kontaktierenden Profile zu bestimmen.

1. Ziehen Sie **[!UICONTROL Activities]** > **[!UICONTROL Targeting]** eine Datei per Drag &amp; Drop **[!UICONTROL Query activity]**.
1. Doppelklicken Sie auf die Aktivität.
1. In the **[!UICONTROL Target]** tab, browse the shortcuts and select one of your [audiences](../../audiences/using/about-audiences.md).
1. Ziehen Sie den Schnellzugriff in den Arbeitsbereich. Je nach Typ des ausgewählten Schnellzugriffs öffnet sich ein bestimmtes Fenster.
1. Konfigurieren Sie die Zielgruppenbestimmungselemente und validieren Sie Ihre Abfrage.

![](assets/wkf_segment_query.png)

Sie können eine auf ein oder mehrere Element(e) bezogene Abfrage erstellen.

Use the **[!UICONTROL Count]** button to see an estimation of the number of profiles targeted by the query.

Die detaillierten Schritte zum Erstellen einer Abfrageaktivität werden im Abschnitt [Abfrage](../../automating/using/query.md) beschrieben.

## Segmentierungsaktivität erstellen{#creating-segmentation-activity}.

Unterteilen Sie im nächsten Schritt Ihre mithilfe der Abfrage-Aktivität bestimmte Zielgruppe in zwei Segmente: das eine erhält eine E-Mail, das andere eine SMS.

Verwenden Sie hierzu die Aktivität Segmentierung, um die zuvor ermittelte Population in zwei Segmente zu unterteilen.

![](assets/wkf_segment_activity.png)

Die erste Gruppe namens **E-Mail** enthält jene Empfänger, die ihre E-Mail-Adresse, aber keine Mobiltelefonnummer angegeben haben. Die zweite Gruppe namens **SMS** enthält jene Empfänger, deren Profil eine Mobiltelefonnummer aufweist.

Gehen sie wie folgt vor, um die erste Transition (E-Mail) zu konfigurieren:

1. In the **[!UICONTROL Segments]** tab, a first segment is present by default. Bearbeiten Sie die Eigenschaften des Segments, um es zu konfigurieren.

   ![](assets/wkf_segment_properties.png)

1. Wählen Sie als Filterbedingung die **[!UICONTROL Email]** des Profils aus.

   ![](assets/wkf_segment_email.png)

1. In the new window that appears on the screen, select the **[!UICONTROL Is not empty]** operator.

   ![](assets/wkf_segment_email_not_empty.png)

1. Hinzufügen ein zweites Filterkriterium, **[!UICONTROL Mobile]** und wählen Sie den Operator **[!UICONTROL Is empty]**.

   ![](assets/wkf_segment_mobile_empty.png)

   Alle aus der Abfrage hervorgehenden Profile, die eine E-Mail-Adresse aber keine Mobiltelefonnummer aufweisen, sind in dieser Transition enthalten.

1. Bei Bedarf können Sie den Titel der Transition zwecks einer besseren Übersichtlichkeit des Workflows anpassen. Bestätigen Sie Ihre Änderungen.

   ![](assets/wkf_segment_transition_label.png)

Die Konfiguration Ihrer ersten Transition ist abgeschlossen. Gehen Sie wie folgt vor, um die zweite Transition (SMS) zu konfigurieren:

1. Klicken Sie auf die **[!UICONTROL Add an element]** Schaltfläche, um eine neue Transition hinzuzufügen.
1. Definieren Sie eine Bedingung, mit der Sie alle Profile abrufen können, deren Mobiltelefonnummern angegeben wurden. To do this, create a rule on the **[!UICONTROL Mobile]** field with the **[!UICONTROL Is not empty]** logical operator.

   ![](assets/wkf_segment_mobile_not_empty.png)

   Alle aus der Abfrage hervorgehenden Profile, die eine Mobiltelefonnummer aufweisen, werden in diese Transition aufgenommen.

1. Bei Bedarf können Sie den Titel der Transition anpassen. Bestätigen Sie Ihre Änderungen.

Die zweite Transition ist jetzt ebenfalls konfiguriert.

![](assets/wkf_segment_transitions.png)

Die detaillierten Schritte zum Erstellen einer Segmentierungsaktivität werden im Abschnitt [Segmentierung](../../automating/using/segmentation.md) beschrieben.

## Sendungen erstellen {#creating-deliveries}

As two transitions were already created, you must now add two types of deliveries to the outbound transitions of the Segmentation activity: an **[!UICONTROL Email delivery]** and an **[!UICONTROL SMS delivery]**.

Mit Adobe Campaign können Sie Versand zu einem Workflow hinzufügen. Wählen Sie dazu in der Palette &quot;Aktivität&quot;Ihres Workflows einen Versand aus der **[!UICONTROL Channels]** Kategorie aus.

![](assets/wkf_segment_deliveries1.png)

Gehen Sie wie folgt vor, um einen E-Mail-Versand zu erstellen:

1. Drag and drop an **[!UICONTROL Email delivery]** after the first segment.
1. Doppelklicken Sie auf die Aktivität, um sie zu bearbeiten.
1. Auswählen **[!UICONTROL Simple email]**.
1. Wählen Sie **[!UICONTROL Add an outbound transition with the population]** und klicken Sie auf **[!UICONTROL Next]**.

   ![](assets/wkf_segment_deliveries2.png)

   Die ausgehende Transition ermöglicht es, die Population und die Trackinglogs abzurufen. Dies kann beispielsweise dazu dienen, jenen Personen erneut eine Sendung zukommen zu lassen, die nicht in der ersten E-Mail geklickt haben.

1. Select an email template and click **[!UICONTROL Next]**.
1. Enter the email properties and click **[!UICONTROL Next]**.
1. Um das Layout Ihrer E-Mail zu erstellen, wählen Sie **[!UICONTROL Use the Email Designer]**.
1. Bearbeiten und speichern Sie Ihre Inhalte.
1. In the **[!UICONTROL Schedule]** section of the message dashboard, unselect the **[!UICONTROL Request confirmation before sending messages}** option.

Die detaillierten Schritte zum Erstellen einer E-Mail-Aktivität finden Sie im Abschnitt [E-Mail-Versand](../../automating/using/email-delivery.md).

Gehen Sie wie folgt vor, um einen SMS-Versand zu erstellen:

1. Drag and drop an **[!UICONTROL SMS delivery]** after the other segment.
1. Doppelklicken Sie auf die Aktivität, um sie zu bearbeiten.
1. Wählen Sie **[!UICONTROL SMS]** und klicken Sie auf **[!UICONTROL Next]**.
1. Select an SMS template and click **[!UICONTROL Next]**.
1. Enter the SMS properties and click **[!UICONTROL Next]**.
1. Bearbeiten und speichern Sie Ihre Inhalte.

Die detaillierten Schritte zum Erstellen einer SMS-Aktivität finden Sie im Abschnitt [SMS-Versand](../../automating/using/sms-delivery.md).

Nach der Konfiguration Ihrer Sendungen kann der Workflow gestartet werden.

![](assets/wkf_segment_deliveries.png)

## Workflow ausführen {#running-the-workflow}

Durch Starten des Workflows wird die mithilfe der Abfrage-Aktivität ermittelte Population segmentiert, damit die Populationssegmente anschließend einen E-Mail- bzw. SMS-Versand erhalten.

Verwenden Sie zur Ausführung des Workflows die Schaltfläche **[!UICONTROL Start]** in der Symbolleiste.

Über das Adobe Campaign-Logo können Sie Ihre Versand über das **[!UICONTROL Marketing plans]** > **[!UICONTROL Marketing activities]** Menü &quot;Erweitert&quot;aufrufen. Klicken Sie auf den Versand und dann auf die **[!UICONTROL Reports]** Schaltfläche, um auf die [Versandberichte](../../reporting/using/about-dynamic-reports.md#accessing-dynamic-reports)zuzugreifen, z. B. die Zusammenfassung des Versands, die Öffnungsrate oder die E-Mail-Wiedergabe entsprechend dem Posteingang der Empfänger.
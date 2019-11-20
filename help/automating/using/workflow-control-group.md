---
title: '"Anwendungsfall des Arbeitsablaufs: Kontrollgruppe"'
seo-title: '"Anwendungsfall des Arbeitsablaufs: Kontrollgruppe"'
description: '"Anwendungsfall des Arbeitsablaufs: Kontrollgruppe"'
seo-description: '"Anwendungsfall des Arbeitsablaufs: Kontrollgruppe"'
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow,use-case,query,segmentation,delivery
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 2912e3b75b817347b832f9c89ca2320868cbc355

---


# Anwendungsfall des Arbeitsablaufs: Erstellen einer Kontrollgruppe {#building-control-group}

Um die Auswirkungen einer Bereitstellung zu messen, sollten Sie einige Profile aus Ihrem Ziel ausschließen, damit sie keine bestimmte Nachricht erhalten. Diese Kontrollgruppe kann verwendet werden, um einen Vergleich mit dem Verhalten der Zielgruppe zu erstellen, die die Nachricht erhalten hat.

Um dies in Adobe Campaign Standard zu tun, können Sie einen Workflow mit den folgenden Aktivitäten erstellen:
* Eine Abfrageaktivität zur Ausrichtung auf eine bestimmte Population.
* Eine Segmentierungsaktivität, um eine zufällige Kontrollgruppe von dieser Population zu isolieren.
* Eine E-Mail-Zustellaktivität, um eine Nachricht an das Hauptziel zu senden.
* Eine Datenaktivität aktualisieren, um die Profile zu aktualisieren, die aus dem Ziel (der Gruppe mit zufälligen Steuerelementen) ausgeschlossen wurden.

![](assets/wkf_control-group.png)

## Profilressource erweitern {#extending-profile}

Zunächst müssen Sie die **[!UICONTROL Profilressource]** um ein neues Feld erweitern, das der Kontrollgruppe entspricht. Sobald der Workflow ausgeführt wurde, wird dieses Feld auf die Profile überprüft, die vom Ziel ausgeschlossen wurden.

1. From **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]** &gt; **[!UICONTROL Custom Resources]**, click **[!UICONTROL Create]**.
1. Wenn Sie die Ressource noch nicht erweitert haben, wählen Sie "Vorhandene Ressource **** erweitern"und wählen Sie die **[!UICONTROL Profilatressource]** .
1. Fügen Sie auf der Registerkarte **[!UICONTROL Datenstruktur]** ein neues Feld für die Kontrollgruppe hinzu und wählen Sie **[!UICONTROL Boolescher]** Wert für das Feld **[!UICONTROL Typ]** .

   ![](assets/wkf_control-group-profile-field.png)

1. Öffnen Sie auf der Registerkarte **[!UICONTROL Bildschirmdefinition]** den Konfigurationsabschnitt für den **[!UICONTROL Detailbildschirm]** und wählen Sie das soeben erstellte Feld aus, damit es für jedes Profil angezeigt wird.

   ![](assets/wkf_control-group-profile-field-screen.png)

1. Speichern Sie Ihre Änderungen.
1. Aktualisieren Sie die Datenbankstruktur, um die **[!UICONTROL erweiterte Ressource Profil]** zu veröffentlichen. See [Publishing a custom resource](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).

Weitere Informationen zum Erweitern einer benutzerdefinierten Ressource finden Sie unter [Wichtige Schritte zum Hinzufügen einer Ressource](../../developing/using/key-steps-to-add-a-resource.md).

## Workflow erstellen {#creating-a-workflow}

1. Wählen Sie dazu in **[!UICONTROL Marketingaktivitäten]** die Option **[!UICONTROL Erstellen]** und dann **[!UICONTROL Workflow]** aus.
1. Wählen Sie als Workflow-Typ **[!UICONTROL Neuer Workflow]** und danach **[!UICONTROL Weiter]** aus.
1. Geben Sie die Eigenschaften des Workflows ein und wählen Sie **[!UICONTROL Erstellen]** aus.

Die detaillierten Schritte zum Erstellen eines Workflows werden im Abschnitt [Erstellen eines Workflows](../../automating/using/building-a-workflow.md) beschrieben.

## Abfrageaktivität erstellen {#create-a-query-activity}.

1. Ziehen Sie in **[!UICONTROL Aktivitäten]** &gt; **[!UICONTROL Targeting]** eine **[!UICONTROL Abfrageaktivität]** in den Arbeitsbereich.
1. Doppelklicken Sie auf die Aktivität, um Ihr Ziel zu definieren.
1. Wählen Sie beispielsweise unter **[!UICONTROL Tastaturbefehle]****[!UICONTROL Profil]** per Drag &amp; Drop **[!UICONTROL Alter]** mit dem Operator **[!UICONTROL Größer als]** und geben Sie 25 in das Feld **[!UICONTROL Wert]** ein.
1. Wählen Sie **[!UICONTROL Bestätigen]** aus.

Die detaillierten Schritte zum Erstellen einer Abfrageaktivität werden im Abschnitt [Abfrage](../../automating/using/query.md) beschrieben.

## Segmentierungsaktivität erstellen{#creating-a-segmentation-activity}.

1. Ziehen Sie eine **[!UICONTROL Segmentierungsaktivität]** in den Arbeitsbereich und doppelklicken Sie darauf.
1. Wählen Sie auf der Registerkarte " **[!UICONTROL Segmente]** "ein Segment aus, das bearbeitet werden soll.
1. Wählen Sie auf der Registerkarte **[!UICONTROL Konfiguration]** dieses Segments die Option Population dieses Segments **** beschränken.

   ![](assets/wkf_control-segment-configuration.png)

1. Stellen Sie sicher, dass auf der Registerkarte " **[!UICONTROL Einschränkungen]** "die Option " **[!UICONTROL Zufallsauswahl]** "ausgewählt ist.

   ![](assets/wkf_control-segment-limitation.png)

1. Definieren Sie einen Prozentsatz der ursprünglichen Population, z. B. 10 %, und klicken Sie auf **[!UICONTROL Bestätigen]**. Die Kontrollgruppe besteht zu 10 % aus der Zielgruppe, die zufällig ausgewählt wird.
1. Wählen Sie auf der Registerkarte " **[!UICONTROL Erweiterte Optionen]** "die Option "Ergänzung **** erstellen"und füllen Sie die Felder **[!UICONTROL Übergangseinschrift]** und **[!UICONTROL Segmentcode]** aus.

   ![](assets/wkf_control-segment-advanced.png)

1. Wählen Sie **[!UICONTROL Bestätigen]** aus.

Die detaillierten Schritte zum Erstellen einer Segmentierungsaktivität werden im Abschnitt [Segmentierung](../../automating/using/segmentation.md) beschrieben.

## Creating an Email activity {#creating-an-email-activity}

1. In **[!UICONTROL Activities]** &gt; **[!UICONTROL Channels]**, drag and drop an **[!UICONTROL Email Delivery]** after the main target segment.
1. Click the activity and select ![](assets/edit_darkgrey-24px.png) to edit it.
1. Wählen Sie **[!UICONTROL Einmalige E-Mail]** und danach **[!UICONTROL Weiter]** aus.
1. Wählen Sie eine E-Mail-Vorlage und dann **[!UICONTROL Weiter]** aus.
1. Geben Sie die E-Mail-Eigenschaften ein und wählen Sie **[!UICONTROL Weiter]** aus.
1. To create the layout of your email, click on **[!UICONTROL Use the Email Designer]**.
1. Bearbeiten und speichern Sie Ihre Inhalte.
1. Deaktivieren Sie im Bereich **[!UICONTROL Plan]** des Nachrichten-Dashboards die Option **[!UICONTROL-Anforderungsbestätigung vor dem Senden von Nachrichten}** .

Die detaillierten Schritte zum Erstellen einer E-Mail-Aktivität finden Sie im Abschnitt [E-Mail-Zustellung](../../automating/using/email-delivery.md) .

## Erstellen einer Datenaktivität zum Aktualisieren {#creating-update-data-activity}

1. Ziehen Sie eine **[!UICONTROL Aktualisierungsdatenaktivität]** nach dem Kontrollgruppensegment und legen Sie es ab.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der ![](assets/edit_darkgrey-24px.png)-Schaltfläche aus den angezeigten Quick Actions.
1. Wählen Sie auf der Registerkarte " **[!UICONTROL Allgemein]** "in der Dropdownliste " **[!UICONTROL Vorgangstyp]** "die Option **[!UICONTROL Aktualisieren]** .
1. Wählen Sie auf der Registerkarte **[!UICONTROL Identifikation]** die Option **[!UICONTROL Direkt mit der Targeting-Dimension]** .
1. Wählen Sie die **[!UICONTROL Profilressource]** aus, die Sie zuvor als zu aktualisierende Dimension erweitert haben.

   ![](assets/wkf_control-update-identification.png)

1. Wählen Sie auf der Registerkarte " **[!UICONTROL Zu aktualisierende]** Felder"das Kontrollgruppenfeld aus, das Sie der **[!UICONTROL Profilressource]** als **[!UICONTROL Ziel]** hinzugefügt haben, und geben Sie als Bedingung true ein.

   ![](assets/wkf_control-update-fields-to-update.png)

1. Wählen Sie **[!UICONTROL Bestätigen]** aus.

Die ausführlichen Schritte zum Erstellen einer Aktualisierungsdatenaktivität werden im Abschnitt [Daten](../../automating/using/update-data.md) aktualisieren beschrieben.

## Workflow ausführen {#running-the-workflow}

Click **[!UICONTROL Start]** to run the workflow.

Nach Ausführung des Workflows wird die Population der Kontrollgruppe ausgeschlossen und die Nachricht wird an das verbleibende Hauptziel gesendet.

Die **[!UICONTROL Profil]** -Ressource wird wie folgt aktualisiert: Wenn sich ein Profil in der Kontrollgruppe befand, wird das entsprechende Feld markiert.

![](assets/wkf_control-group-profile-checked.png)

Sie können nun vergleichen, wie die Empfänger der Nachricht reagieren, im Vergleich zu der kleinen Gruppe, die von der Nachricht ausgeschlossen wurde und sie nicht erhalten hat.

## Wiederverwenden derselben Kontrollgruppe {#reusing-same-control-group}

Das obige Beispiel ermöglicht die Erstellung einer globalen Kontrollgruppe, da diese unabhängig von den Auslieferungen als Profilattribut gespeichert wird. Tatsächlich wird das neue Feld "Kontrollgruppe", das als Teil der **[!UICONTROL Profil]** -Ressourcenerweiterung erstellt wurde, aktualisiert, nachdem der Workflow oben ausgeführt wurde.

Wenn Sie demzufolge das nächste Mal dieselbe Kontrollgruppe verwenden möchten, können Sie das Segment im neuen Feld "Kontrollgruppe"durchführen, anstatt eine zufällige Segmentierung durchzuführen.

Gehen Sie wie folgt vor:
1. Wählen Sie beim Erstellen der **[!UICONTROL Segmentierungsaktivität]** das zu bearbeitende Segment auf der Registerkarte " **[!UICONTROL Segmente]** "aus.
1. Stellen Sie sicher, dass Sie auf der Registerkarte **[!UICONTROL Konfiguration]** dieses Segments nicht die Option Population dieses Segments **** beschränken auswählen.
1. Ziehen Sie auf der Registerkarte " **[!UICONTROL Filtern]** "die **[!UICONTROL Profile (Attribute)]** in den Hauptarbeitsbereich.

   ![](assets/wkf_control-group-segment-profiles-attributes.png)

1. Wählen Sie im Fenster "Regel **[!UICONTROL hinzufügen - Profile (Attribute)]** "die Option "Kontrollgruppe"(das Feld, das Sie der **[!UICONTROL Profilressource]** hinzugefügt haben) und dann **[!UICONTROL Ja]** als Filterbedingung.

   ![](assets/wkf_control-group-segment-profiles-attributes-field.png)
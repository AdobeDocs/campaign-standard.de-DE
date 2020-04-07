---
title: Warnungen bei Zustellproblemen erhalten
description: Hier erfahren Sie, wie Versandwarnungen verwendet werden.
page-status-flag: never-activated
uuid: a3ab733a-e3db-4adc-b930-cd4064b6dc1c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: monitoring-messages
discoiquuid: 0766bd57-c5f1-4f56-ac84-e5a04d3819ec
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 155ed7e50e207e4c4dc0569e5e96b24e712e4be8

---


# Warnungen bei Zustellproblemen erhalten{#receiving-alerts-when-failures-happen}

## Über Versandwarnungen {#about-delivery-alerting}

Bei der Funktion **Versandwarnungen** handelt es sich um ein Warnungsmanagementsystem, über das eine Benutzergruppe automatisch Benachrichtigungen zu ihren Sendungen erhält.

Die gesendeten Benachrichtigungen beinhalten einen Bericht, der standardmäßig auf den folgenden Bedingungen basiert:

* Fehlgeschlagene Sendungen
* Sendungen mit fehlgeschlagener Vorbereitung
* Sendungen mit zu hoher Softbounce-Fehlerrate
* Sendungen mit zu hoher Hardbounce-Fehlerrate
* Sendungen mit dem Status &quot;Ausstehend&quot;, die länger als üblich dauern
* Sendungen mit geringem Durchsatz
* Gestartete Sendungen

Die Empfänger der Warnungen können die von Adobe Campaign verarbeiteten Sendungen überwachen und entsprechende Maßnahmen treffen, wenn bei der Durchführung Fehler auftreten.

Diese Warnungen können entsprechend den Warnungsbedingungen angepasst werden, die über ein Dashboard in Adobe Campaign definiert werden.

>[!NOTE]
>
>Die Warnungen werden nur per E-Mail zugestellt.

Die gesendeten Benachrichtigungen enthalten folgende Elemente:

* A **[!UICONTROL Summary]** displaying the number of deliveries meeting the criteria that you defined and the label/color that you chose for each criterion.
* den Bereich **[!UICONTROL Details]**, in dem alle für das entsprechende Dashboard definierten Versandbedingungen sowie alle Sendungen für jede Bedingung aufgeführt werden.

![](assets/delivery-alerting_notification.png)

## Versandwarnungs-Dashboards {#delivery-alerting-dashboards}

### Über Versandwarnungs-Dashboards {#about-delivery-alerting-dashboards}

Dashboards werden verwendet, um die Empfänger der Benachrichtigungen zu verwalten, die Warnungsbedingungen zu definieren und auf den Verlauf der Warnungen zuzugreifen.

>[!NOTE]
>
>Um Dashboards und Warnungsbedingungen öffnen und konfigurieren zu können, müssen Sie über Administratorrechte verfügen oder der Sicherheitsgruppe **Versand-Supervisoren** angehören. Standardbenutzer können nicht auf Dashboards in Adobe Campaign zugreifen, sondern haben nur die Möglichkeit, Warnnachrichten zu empfangen. Weiterführende Informationen zu Benutzern und zur Sicherheit in Adobe Campaign finden Sie in den Abschnitten [Typen von Benutzern](../../administration/using/users-management.md) und [Über Sicherheitsgruppen](../../administration/using/managing-groups-and-users.md#about-security-groups).

In der Adobe Campaign-Benutzeroberfläche haben Sie folgende Möglichkeiten:

* Versandwarnungs-Dashboards erstellen und verwalten. Siehe [Versandwarnungs-Dashboard erstellen](#creating-a-delivery-alerting-dashboard).
* Versandwarnungsbedingungen für jedes Dashboard definieren und verwalten. Beispielsweise können Sie Warnungen für Sendungen mit fehlgeschlagener Vorbereitung oder Sendungen mit geringem Durchsatz erstellen. Siehe [Über Warnungsbedingungen](#about-alerting-criteria).
* Die Bedingungsparameter für jedes Dashboard ändern. Siehe [Bedingungsparameter](#criteria-parameters).
* Für jedes Dashboard eine Empfängergruppe definieren.

   Beispiel: Sie möchten die Benutzer mit Administratorrechten nur über fehlgeschlagene Sendungen informieren. Sie möchten aber auch, dass Mitarbeiter der Marketingabteilung von den Sendungen mit zu hoher Softbounce-Fehlerrate informiert werden. Sie müssen daher zwei unterschiedliche Dashboards erstellen und die Bedingungen für jede Empfängergruppe definieren.

* Öffnen Sie den Verlauf aller gesendeten Warnungen für jedes Dashboard.

   Bei der Auswahl eines Dashboards wird standardmäßig die zuletzt gesendete Warnung für dieses Dashboard angezeigt. Alle gesendeten Warnungen sind auf der linken Bildschirmseite aufgelistet. Click an item in the **[!UICONTROL History]** list to access the corresponding alerts.

![](assets/delivery-alerting_dashboard.png)

### Versandwarnungs-Dashboard erstellen {#creating-a-delivery-alerting-dashboard}

Wenn Sie Benachrichtigungen, die auf bestimmten Bedingungen basieren, an unterschiedliche Benutzergruppen senden möchten, benötigen Sie mehrere Dashboards. Gehen Sie wie folgt vor, um ein neues Dashboard zu erstellen:

1. Go to **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Delivery alerting]**.
1. Wählen Sie **[!UICONTROL Delivery alerting dashboards]** und klicken Sie auf **[!UICONTROL Create]**.
1. Check the **[!UICONTROL Enabled]** box to activate the current dashboard.

   Ist diese Option deaktiviert, werden mit diesem Dashboard verknüpfte Benachrichtigungen nicht mehr gesendet. Standardmäßig ist diese Option deaktiviert.

   ![](assets/delivery-alerting_dashboard_general.png)

1. Select the group of recipients that you want to notify from the **[!UICONTROL Alert group]** drop-down list. Zum Ändern oder Erstellen einer Gruppe lesen Sie den Abschnitt [Sicherheitsgruppe erstellen und Benutzer zuordnen](../../administration/using/managing-groups-and-users.md#creating-a-security-group-and-assigning-users).
1. Klicken Sie im **[!UICONTROL Delivery alerting criteria]** Abschnitt auf , **[!UICONTROL Create element]** um Kriterien hinzuzufügen. Siehe [Über Warnungsbedingungen](#about-alerting-criteria).
1. Select the **[!UICONTROL Edit properties]** button. In the **[!UICONTROL Criteria parameters]** tab, define how the criteria will be applied. Siehe [Bedingungsparameter](#criteria-parameters).
1. Click **[!UICONTROL Create]** to save the dashboard.

Immer wenn jetzt ein Versand die von Ihnen in diesem Dashboard definierten Bedingungen erfüllt, wird eine Warnung an die angegebene Benutzergruppe gesendet.

## Versandwarnungsbedingungen  {#delivery-alerting-criteria}

### Über Warnungsbedingungen {#about-alerting-criteria}

Um auf die Versand-Warnkriterien zuzugreifen, gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Delivery alerting]** und wählen Sie **[!UICONTROL Delivery alerting criteria]**.

![](assets/delivery-alerting_criteria.png)

Die folgenden Bedingungen stehen in den Versandwarnungs-Dashboards zur Verfügung:

* **[!UICONTROL Deliveries failed]**: Jeder Versand, der innerhalb eines definierten Bereichs geplant ist, mit einem fehlerhaften Status.
* **[!UICONTROL Deliveries with preparation failed]**: Jeder Versand, der innerhalb eines definierten Bereichs geändert wurde und für den der Vorbereitungsschritt (Zielgruppe und Inhaltsgenerierung) fehlgeschlagen ist. Weiterführende Informationen dazu finden Sie im Abschnitt [Versandvorbereitung](../../sending/using/preparing-the-send.md).
* **[!UICONTROL Delivery with bad error ratio for soft bounces]**: Jeder Versand, der innerhalb eines definierten Bereichs geplant ist, mit einem Status von mindestens **[!UICONTROL In progress]** einem Soft-Absprungfehler-Verhältnis von mehr als einem definierten Prozentwert.
* **[!UICONTROL Delivery with bad error ratio for hard bounces]**: Jeder Versand, der innerhalb eines definierten Bereichs geplant ist, mit einem Status von mindestens **[!UICONTROL In progress]** einem festen Absprungfehler-Verhältnis, der größer als ein definierter Prozentwert ist.
* **[!UICONTROL Deliveries with long start pending]**: Jeder Versand, der innerhalb eines definierten Bereichs mit einem **[!UICONTROL Start pending]** Status von mehr als einer definierten Dauer geplant ist, d. h., **[!UICONTROL Start pending]** die Meldungen wurden noch nicht vom System berücksichtigt.
* **[!UICONTROL Deliveries with low throughput]**: Jeder Versand, der länger als eine definierte Dauer mit weniger als einem definierten Prozentwert der verarbeiteten Nachrichten gestartet wurde, hat einen geringeren Durchsatz als ein definierter Wert.
* **[!UICONTROL Deliveries in progress]**: Jeder Versand, der innerhalb eines definierten Bereichs mit dem **[!UICONTROL In progress]** Status geplant ist.

>[!NOTE]
>
>Alle Parameter, die für die oben aufgeführten Bedingungen gelten, weisen Standardwerte auf. These values can be changed in the **[!UICONTROL Criteria parameters]** tab of the delivery alerting dashboards. Siehe [Bedingungsparameter](#criteria-parameters).

You can select any item from the **[!UICONTROL Delivery alerting criteria]** list to access its details.

![](assets/delivery-alerting_criteria_definition.png)

Für jede Bedingung können Sie folgende Einstellungen festlegen:

* **[!UICONTROL Indicators to add in alerts]**, d. h. die Spalten, die im **[!UICONTROL Details]** Benachrichtigungsabschnitt für die Versände angezeigt werden, die dem ausgewählten Kriterium entsprechen.

   ![](assets/delivery-alerting_notification_colums.png)

* **[!UICONTROL Alert type]**, d. h. das Etikett und die Farbe, die neben dem Versand-Kriterium in der Zusammenfassung der Anmeldung angezeigt werden.

   ![](assets/delivery-alerting_notification_labels.png)

* **[!UICONTROL Criteria frequency]**: Wird ein Kriterium für einen Versand erfüllt, wird es in jeder innerhalb des Überwachungszeitraums übermittelten Meldung wiederholt. Ansonsten wird für einen Versand nur eine einzige Warnung pro Tag und Art der Warnung (beim ersten Auftreten) gemäß der Warnungsbedingung gesendet.

   Standardmäßig ist diese Option für alle Bedingungen auf einmal täglich festgelegt.

**Verwandte Themen:**

* [Versandlogs](../../sending/using/monitoring-a-delivery.md#sending-logs)
* [Häufigkeit der Versandwarnungen](#alerting-frequency)
* [Symbole und Status von Marketingaktivitäten](../../start/using/marketing-activities.md#marketing-activity-icons-and-statuses)

### Versandwarnungsbedingung erstellen  {#creating-a-delivery-alerting-criterion}

Sie können nach Bedarf neue Versandwarnungsbedingungen erstellen.

For example, you can create a new criterion enabling to send a notification listing all deliveries with a **[!UICONTROL Finished]** status.

To do this, you first need to extend the **Delivery** resource and add a new filter allowing you to select only the deliveries with a **[!UICONTROL Finished]** status.

1. Go to **Adobe Campaign** > **Administration** > **Development** > **Custom resources** and click **[!UICONTROL Create]**.
1. Wählen Sie **[!UICONTROL Extend an existing resource]** die **[!UICONTROL Delivery]** Ressource aus der Dropdown-Liste und klicken Sie auf **[!UICONTROL Create]** , um sie zu bearbeiten.

   ![](assets/delivery-alerting_extend-delivery-cus.png)

   Weiterführende Informationen zu einer bestehenden Ressource finden Sie im Abschnitt [Ressource definieren](../../developing/using/creating-or-extending-the-resource.md).

1. Wechseln Sie in der **[!UICONTROL Delivery]** Ressource zur **[!UICONTROL Filter definition]** Registerkarte und klicken Sie auf , **[!UICONTROL Add an element]** um einen Filter zu erstellen.

   ![](assets/delivery-alerting_new-filter.png)

1. Edit the new filter definition: in the **[!UICONTROL Filter definition]** window, drag and drop the **[!UICONTROL Status]** item into the workspace and select **[!UICONTROL Finished]** as the filter condition.

   ![](assets/delivery-alerting_filter-status.png)

   Weiterführende Informationen zur Erstellung und Bearbeitung von benutzerdefinierten Filtern finden Sie im Abschnitt [Filter definieren](../../developing/using/configuring-filter-definition.md).

1. Speichern Sie Ihre Änderungen und publizieren Sie die Ressourcen. Weiterführende Informationen dazu finden Sie unter [Benutzerdefinierte Ressource publizieren](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).

   Der Filter wird erstellt und kann jetzt in einer neuen Versandwarnungsbedingung ausgewählt werden.

1. Gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Delivery alerting]**, wählen Sie **[!UICONTROL Delivery alerting criteria]** und klicken Sie auf **[!UICONTROL Create]**.
1. Wählen Sie in der **[!UICONTROL Delivery filter applied by this criterion]** Dropdown-Liste den soeben erstellten Filter aus.

   ![](assets/delivery-alerting_cus-filter.png)

   Die Einstellungen Ihrer Bedingung können auf dieselbe Weise definiert werden wie die der Standardbedingungen. Siehe [Über Warnungsbedingungen](#about-alerting-criteria).

Nach der Erstellung können diese Bedingungen zu einem Versandwarnungs-Dashboard sowie zu anderen Bedingungen hinzugefügt werden. Siehe [Über Versandwarnungs-Dashboards](#about-delivery-alerting-dashboards).

![](assets/delivery-alerting_new-criterion.png)

**Verwandtes Thema:**

[Ressource hinzufügen oder erweitern](../../developing/using/key-steps-to-add-a-resource.md)

## Versandwarnungsparameter  {#delivery-alerting-parameters}

### Bedingungsparameter {#criteria-parameters}

In the **[!UICONTROL Criteria parameters]** tab of a [delivery alerting dashboard](#creating-a-delivery-alerting-dashboard), you can define the settings that apply to the criteria selected in this dashboard.

![](assets/delivery-alerting_dashboard_criteria-parameters.png)

* **[!UICONTROL Delivery target minimum size]**: Wenn Sie beispielsweise 100 in dieses Feld eingeben, wird eine Benachrichtigung nur für Versand mit einer Zielgruppe von 100 Empfängern oder mehr gesendet. Dieser Parameter gilt für alle Bedingungen.
* **[!UICONTROL Monitoring period before and after the contact date (in hours)]**: Anzahl der Stunden vor und nach dem aktuellen Zeitpunkt. Nur Sendungen mit Kontaktdatum in diesem Zeitraum werden berücksichtigt. Dieser Parameter gilt für alle Bedingungen. Standardmäßig ist der Wert dieses Feldes mit 24 Stunden festgelegt.

   Weiterführende Informationen zum Kontaktdatum finden Sie in Abschnitt [Über die Versandplanung](../../sending/using/about-scheduling-messages.md).

* **[!UICONTROL Maximum ratio of soft bounce errors]**: Eine Benachrichtigung wird für alle Versand gesendet, deren Soft-Absprungfehlerquote größer als der angegebene Wert ist. Der Standardwert für dieses Feld ist 0,05 (5 %).

   Weiterführende Informationen zu Softbounce-Fehlern finden Sie in den Abschnitten [Bounce-Message-Qualifizierung](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification) und [Liste der Versandfehlertypen](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons).

* **[!UICONTROL Maximum ratio of hard bounce errors]**: Eine Benachrichtigung wird für alle Versand gesendet, deren Fehlerquote höher als der angegebene Wert ist. Der Standardwert für dieses Feld ist 0,05 (5 %).

   Weiterführende Informationen zu Hardbounce-Fehlern finden Sie in den Abschnitten [Bounce-Message-Qualifizierung](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification) und [Liste der Versandfehlertypen](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons).

* **[!UICONTROL Minimum time threshold for delivery in 'Start pending' status (in minutes)]**: Für alle Versand mit einem **[!UICONTROL Start pending]** Status, der länger als in diesem Feld angegeben ist, wird eine Benachrichtigung gesendet. Dies bedeutet, **[!UICONTROL Start pending]** dass die Meldungen noch nicht vom System berücksichtigt wurden.
* **[!UICONTROL Minimum time required for the computation of the throughput (in minutes)]**: Für das Kriterium werden nur Versand berücksichtigt, die (mit **[!UICONTROL In progress]** Status) länger als die angegebene Dauer **[!UICONTROL Deliveries with low throughput]** beginnen.
* **[!UICONTROL Maximum percentage of processed messages for the computation of the throughput]**: Nur Versand, deren Prozentsatz der verarbeiteten Nachrichten unter dem angegebenen Prozentsatz liegt, werden für das **[!UICONTROL Deliveries with low throughput]** Kriterium berücksichtigt.
* **[!UICONTROL Minimum expected throughput (in sent messages per hour)]**: Für das **[!UICONTROL Deliveries with low throughput]** Kriterium werden nur Versand berücksichtigt, deren Durchsatz unter dem angegebenen Wert liegt.
* **[!UICONTROL Minimum processed ratio required for 'Deliveries in progress' criterion]**: Es werden nur Versand berücksichtigt, deren Prozentsatz der verarbeiteten Nachrichten über dem angegebenen Prozentsatz liegt.

### Häufigkeit der Versandwarnungen {#alerting-frequency}

Die **[!UICONTROL Frequency of delivery alerting]** Option ermöglicht die Definition der Verzögerung zwischen zwei Warnungssendungen. Standardmäßig ist dieser Zeitraum auf 10 Minuten festgelegt.

Sie können diese Einstellung über das Menü **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** > **[!UICONTROL Options]** ändern.

>[!NOTE]
>
>Diese Option gilt für alle in Adobe Campaign definierten Dashboards. Es ist nicht möglich, für jedes Dashboard eine eigene Häufigkeit festzulegen.

## Gründe für Versandwarnungen  {#delivery-alerting-reasons}

Mit der Funktion **Versandwarnung** von Adobe Campaign sind alle Benutzer von Adobe Campaign automatisch über den Ausführungsstatus des Versands über E-Mails und Dashboards informiert.

Hier sind einige Tipps, was Sie tun können, wenn Sie eine Benachrichtigung zu Versandwarnungen erhalten.

Prüfen Sie zuerst den Tab **Protokoll** des Versands, um alle mit dem Versand und den Testsendungen verbundenen Informationen anzuzeigen. Eventuelle Fehler oder Warnmeldungen werden durch rote und gelbe Symbole hervorgehoben. Ein rotes Symbol weist auf einen kritischen Fehler hin, der den Start des Versands verhindert.

To view the history of every occurrence of a delivery, select the **[!UICONTROL Sending logs]** tab. Hier finden Sie die Liste der gesendeten Nachrichten sowie deren Status. There you can check the delivery status for each recipient ( **[!UICONTROL Sent]**, **[!UICONTROL Pending]**, **[!UICONTROL Failed]**, etc.). Lesen Sie diesbezüglich auch den Abschnitt [Versandlogs](../../sending/using/monitoring-a-delivery.md#sending-logs).

Hier sind einige mögliche Gründe für den Erhalt von Warnungsbenachrichtigungen in Bezug auf die für einen Versand erfüllten Bedingungen.

* **[!UICONTROL Deliveries failed]**: Dieses Kriterium informiert Sie über alle Versand mit einem fehlerhaften Status. Die möglichen Gründe:

   * Ein Problem mit dem Versand-Server (MTA, Message Transfer Agent)
   * Eine Zeitüberschreitung bei der Verbindung zwischen dem Versand-Server von Adobe Campaign und dem Empfangs-Server
   * Ein Problem bei der Zustellbarkeit
   * Ein fehlerhafter Workflow
   Wenn der Versand durch einen Workflow ausgelöst wird, prüfen Sie, ob der Workflow korrekt gestartet wurde. Weiterführende Informationen dazu finden Sie unter [Workflow ausführen](../../automating/using/executing-a-workflow.md). Sollten die Probleme fortbestehen, wenden Sie sich an Ihren Adobe-Campaign-Administrator.

* **[!UICONTROL Deliveries with preparation failed]**: In den folgenden Fällen kann während der Vorbereitung des Versands ein Fehler auftreten:

   * Im Versand fehlt der Betreff.
   * Die Personalisierungsfelder enthalten falsche Syntax.
   * Die Zielgruppe fehlt.
   * Der Versand übersteigt das Größenlimit.
   Weiterführende Informationen dazu finden Sie im Abschnitt [Versandvorbereitung](../../sending/using/preparing-the-send.md). Diese Fehler werden jedoch normalerweise während der Nachrichtenanalyse erkannt. Näheres dazu finden Sie unter [Kontrollregeln](../../sending/using/control-rules.md).

* Mögliche Ursachen für eine **[!UICONTROL Delivery with bad error ratio for soft bounces]** Warnung sind:

   * Der Server des Empfängers ist ausgefallen.
   * Das Postfach des Empfängers ist voll.
   Weitere Informationen finden Sie auf den Registerkarten **[!UICONTROL Exclusion logs]** und **[!UICONTROL Exclusion causes]** auf den Versandlogs. Siehe [Ausschlusslogs](../../sending/using/monitoring-a-delivery.md#exclusion-logs).

   Mögliche Ursachen für eine **[!UICONTROL Delivery with bad error ratio for hard bounces]** Warnung sind:

   * Der Empfänger steht auf der Blacklist, was bedeutet, dass er nicht mehr kontaktiert werden möchte.
   * Die E-Mail-Adresse des Empfängers existiert nicht.
   * Die Domain des Empfängers existiert nicht.
   * Der Server des Empfängers blockiert die Zustellung.
   Um Soft- und Hardbounce-Fehler zu vermeiden, folgen Sie den unten stehenden Empfehlungen:

   * Erstellen Sie Filter-Typologieregeln, um einen Teil der Zielgruppe während der Versandanalyse auszuschließen, wie etwa Empfänger in Quarantäne. Näheres dazu finden Sie unter [Filterregel erstellen](../../sending/using/filtering-rules.md).
   * Aktualisieren Sie regelmäßig Ihre Kundendatenbank, um eine gute Quarantäneverwaltung zu gewährleisten. Näheres dazu erfahren Sie unter [Über Quarantänen](../../sending/using/understanding-quarantine-management.md#about-quarantines).
   * Im Allgemeinen sollten Sie versuchen, die Zustellbarkeit möglichst zu verbessern. Näheres dazu finden Sie in der Dokumentation von Adobe Campaign im Abschnitt [Zustellbarkeit](../../sending/using/about-deliverability.md). Wenden Sie sich außerdem an Ihren Adobe Campaign-Administrator um Hilfe.



* **[!UICONTROL Deliveries with long start pending]**: Normalerweise bedeutet dies, dass es ein Problem auf der MTA-Ebene (Message Transfer Agent) gibt. Der Prozess wartet auf die Verfügbarkeit von Ressourcen. Möglicherweise wurde der MTA noch nicht gestartet.

   **[!UICONTROL Deliveries with low throughput]**: Auch hier handelt es sich um eine Frage der Lieferbarkeit, was bedeutet, dass die MTA zu langsam ist.

   Wenden Sie sich an Ihren Adobe-Campaign-Administrator, um Näheres dazu zu erfahren.

**Verwandte Themen:**

* [Ursachen von fehlgeschlagenen Sendungen](../../sending/using/understanding-delivery-failures.md)
* [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md)
* [Blacklists in Campaign verwenden](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)


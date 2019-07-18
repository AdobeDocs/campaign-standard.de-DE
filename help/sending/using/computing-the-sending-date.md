---
title: Versanddatum berechnen
seo-title: Versanddatum berechnen
description: Versanddatum berechnen
seo-description: Hier erfahren Sie, wie Sie eine Nachricht an einem bestimmten Datum und zu einer bestimmten Uhrzeit senden.
page-status-flag: nie aktiviert
uuid: fbbb 37 a 0-7257-4407-a 4 c 9-f 76 bf 44460 d 4
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird gesendet
content-type: Referenz
topic-tags: sheduling-messages
discoiquuid: 02 a 87 cc 6-c 40 c -44 fe-bb 4 e-b 88870 a 4859 b
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 28abc1e8aa31f3e0c7f09926f34a977d4c491fd8

---


# Versanddatum berechnen{#computing-the-sending-date}

Sie können eine Formel definieren, um die Nachricht an jeden Empfänger an einem bestimmten Datum und zu einer bestimmten Uhrzeit zu senden.

## Datumsformel anpassen {#customizing-date-formula}

Die Optimierung des Versandzeitpunkts ist beispielsweise während der Anlaufphase Ihrer Marketingaktivitäten nützlich.

Wenn E-Mails über eine neue Plattform versendet werden, sind ISPs normalerweise misstrauisch gegenüber den neuen IP-Adressen. Das plötzliche Versenden großer Mengen an E-Mails veranlasst ISPs oft dazu, sie als Spam zu qualifizieren.

Um dies zu verhindern, können Sie das Datenvolumen schrittweise erhöhen, indem Sie den Versand von großen Mengen von E-Mails auf mehrere Zeitpunkte aufteilen. Dies gewährleistet eine reibungslose Anlaufphase, da die Gesamtrate ungültiger Adressen verringert wird.

Sie können Ihre Ziel-Audience beliebig aufteilen und Ihren Versand beispielsweise in fünf Teilsendungen versenden. So können Sie die erste Teilsendung von 10 % Ihrer Ziel-Audience am 1. Juni um 10 Uhr durchführen, die zweite Teilsendung von 15 % der Audience 24 Stunden später und so weiter.

Diese Abfolge kann mit einem Workflow terminiert werden.

![](assets/send-time_opt_workflow1.png)

1. Gehen Sie in die Liste der Marketingaktivitäten und erstellen Sie einen neuen Workflow. Lesen Sie diesbezüglich auch den Abschnitt [Workflows erstellen](../../automating/using/building-a-workflow.md#creating-a-workflow).
1. Ziehen Sie eine **Abfrage** in den Workflow-Arbeitsbereich und öffnen Sie sie. Siehe den Abschnitt [Abfrage](../../automating/using/query.md).
1. Wählen Sie eine Audience aus, z. B. alle Ihre Gold-Kunden und klicken Sie auf **[!UICONTROL Bestätigen], um die Abfrage zu speichern.**
1. Ziehen Sie eine **Segmentierung** in den Workflow-Arbeitsbereich und öffnen Sie sie. Siehe den Abschnitt [Segmentierung](../../automating/using/segmentation.md).
1. Definieren Sie fünf Segmente. Gehen Sie für jedes Segment folgendermaßen vor:

   * Füllen Sie das Feld **[!UICONTROL Segmentcode]aus: Geben Sie manuell den gewünschten Zeitpunkt für den Versand der Nachricht ein.**

      Beispiel: Sie möchten den ersten Teilversand am 1. Juni um 10 Uhr (GMT+1) durchführen. Verwenden Sie dazu das folgende Format: **JJJJ-MM-TT hh:mm:ss+tz**.

      ![](assets/send-time_opt_segment_configuration.png)

      Um die nächste Teilsendung am nächsten Tag durchzuführen, geben Sie **2017-06-02 10:00:00+01** ein.

      Definieren Sie die nächsten Teilsendungen für die restlichen Segmente folgendermaßen:

      * **2017-06-03 10:00:00+01**
      * **2017-06-04 10:00:00+01**
      * **05.06.2017 10:00:00+01**
   * Wählen Sie die Option **[!UICONTROL Segmentpopulation begrenzen]aus.**

      Wählen Sie im Tab **[!UICONTROL Begrenzung]** die Option **Zufällige Auswahl]aus und geben Sie für jedes Segment den gewünschten Prozentsatz ein: 10 für die erste Teilsendung, 15 für die zweite etc.[!UICONTROL **

      ![](assets/send-time_opt_segment_limitation.png)


1. Wählen Sie **[!UICONTROL Alle Segmente in derselben Transition erzeugen]** aus und danach **[!UICONTROL Bestätigen]**.

   ![](assets/send-time_opt_segment_dates.png)

1. Ziehen Sie einen **E-Mail-Versand** in den Workflow-Arbeitsbereich und öffnen Sie ihn. Siehe den Abschnitt [E-Mail-Versand](../../automating/using/email-delivery.md).
1. Click the **[!UICONTROL Schedule]** section in the email dashboard and select **[!UICONTROL Messages to be sent automatically on the date specified below]**.
1. Definieren Sie im Feld **[!UICONTROL Versandstart am]ein Kontaktdatum.**
1. Wählen Sie aus der Sedezeitoptimierungs-Dropdown-Liste **[!UICONTROL Versand zu einem durch eine Formel festgelegten Zeitpunkt aus]**.
1. Wählen Sie die Schaltfläche **[!UICONTROL Ausdruck bearbeiten]** im Feld **Benutzerdefinierte Datumsformel]aus.[!UICONTROL **

   ![](assets/send-time_opt_formula_define.png)

1. Erstellen Sie mit der Funktion **[!UICONTROL ToDateTime]** und dem Feld **Segmentcode]den folgenden Ausdruck.[!UICONTROL ** Sie können den Ausdruck auch direkt eingeben, aber achten Sie darauf, korrekte Syntax und Rechtschreibung zu verwenden.

   ```
   ToDateTime([targetData/@segmentCode])
   ```

   Die Funktion **[!UICONTROL ToDateTime]wandelt den Segmentcode von einem Textstring in einen Datums- und Uhrzeit-Wert um.**

   Bestätigen Sie den Ausdruck, um zum vorherigen Bildschirm zurückzukehren.

   ![](assets/send-time_opt_formula_define_segment.png)

   Im Fenster **[!UICONTROL Planung]wird die benutzerdefinierte Datumsformel folgendermaßen dargestellt:**

   ```
   ToDateTime([targetData/@segmentCode])
   ```

   ![](assets/send-time_opt_custom_formula.png)

1. Validieren Sie die Planung, speichern Sie den Versand und starten Sie den Workflow.

Der Versand wird auf fünf Tage verteilt an alle Empfänger gesendet.

>[!NOTE]
>
>Achten Sie bei der Validierung des Versands darauf, dass alle Daten in der Zukunft liegen. Ansonsten werden die Nachrichten unmittelbar nach der Validierung gesendet.

## Ausdruck verwenden {#using-an-expression}

Die Versandzeitoptimierung ist auch für Callcenter-Kampagnen hilfreich. Damit können Sie gewährleisten, dass nicht alle Nachrichten zur selben Zeit beim Empfänger eintreffen. Dadurch kann Ihr Unternehmen die Anzahl der Anrufe entsprechend seiner Kapazität steuern.

Beispiel: Sie laden in einer E-Mail Ihre Kunden ein, das Callcenter zu kontaktieren, um ein Werbeangebot einzulösen. Damit das Callcenter nicht mit Anrufen überflutet wird, segmentieren Sie Ihre Ziel-Audience zufällig und senden Ihre E-Mails in vier Teilsendungen.

Diese Abfolge kann mit einem Workflow terminiert werden.

![](assets/send-time_opt_workflow2.png)

1. Gehen Sie in die Liste der Marketingaktivitäten und erstellen Sie einen neuen Workflow. Lesen Sie diesbezüglich auch den Abschnitt [Workflows erstellen](../../automating/using/building-a-workflow.md#creating-a-workflow).
1. Ziehen Sie eine **Abfrage** in den Workflow-Arbeitsbereich und öffnen Sie sie. Siehe den Abschnitt [Abfrage](../../automating/using/query.md).
1. Wählen Sie eine Audience aus, z. B. 35 Profile, und klicken Sie auf **[!UICONTROL Bestätigen], um die Abfrage zu speichern.**
1. Ziehen Sie eine **Segmentierung** in den Workflow-Arbeitsbereich und öffnen Sie sie. Siehe den Abschnitt [Segmentierung](../../automating/using/segmentation.md).
1. Definieren Sie vier Segmente. Gehen Sie für jedes Segment folgendermaßen vor:

   * Definieren Sie die Segmentcodes:

      * 8:00 AM - 10:00 AM: **0**. Die Nachricht wird an das erste Viertel der Zielpopulation um 8 Uhr gesendet (Kontaktdatum).
      * 10:00 AM - 12:00 AM: **2**. Die Nachricht wird an das zweite Viertel der Zielpopulation um 10 Uhr gesendet (Kontaktdatum + 2 Stunden).
      * 14:00 AM - 16:00 AM: **6**. Da das Callcenter zwischen 12 und 14 Uhr geschlossen ist, wird die Nachricht an das dritte Viertel der Zielpopulation um 14 Uhr gesendet (Kontaktdatum + 6 Stunden).
      * 16:00 AM - 18:00 AM: **8**. Die Nachricht wird an das letzte Viertel der Zielpopulation um 16 Uhr gesendet (Kontaktdatum + 8 Stunden).
      >[!NOTE]
      >
      >Das Kontaktdatum wird später im Workflow in der E-Mail-Versand-Aktivität definiert.

   * Wählen Sie die Option **[!UICONTROL Segmentpopulation begrenzen]aus.**
   * Wählen Sie im Tab **[!UICONTROL Begrenzung]** die Option **[!UICONTROL Zufällige Auswahl]aus und geben Sie für jedes Segment den gewünschten Prozentsatz ein:** 25 **.**


1. Wählen Sie **[!UICONTROL Alle Segmente in derselben Transition erzeugen]** aus und danach **[!UICONTROL Bestätigen]**.

   ![](assets/send-time_opt_segment.png)

1. Ziehen Sie einen **E-Mail-Versand** in den Workflow-Arbeitsbereich und öffnen Sie ihn. Siehe den Abschnitt [E-Mail-Versand](../../automating/using/email-delivery.md).
1. Wählen Sie im E-Mail-Dashboard den Bereich **[!UICONTROL Planung]aus.**
1. Wählen Sie **[!UICONTROL Nachrichtenversand am unten angegebenen Datum aus]**.
1. Definieren Sie im Feld **[!UICONTROL Versandstart am]ein Kontaktdatum.**

   Wählen Sie für dieses Beispiel den 25. Mai, 8 Uhr aus.

1. Wählen Sie aus der Sedezeitoptimierungs-Dropdown-Liste **[!UICONTROL Versand zu einem durch eine Formel festgelegten Zeitpunkt]** aus und klicken Sie auf die Schaltfläche **Ausdruck bearbeiten[!UICONTROL .]**

   ![](assets/send-time_opt_formula_expression.png)

1. In the **[!UICONTROL Expression editor]**, set the date and the segment codes to compute the data for each customer.

   Wählen Sie in der Funktionsliste die Option **[!UICONTROL AddHours aus]**.

   ![](assets/send-time_opt_formula_expression_addhours.png)

   In the available fields, select **[!UICONTROL Current delivery]** &gt; **[!UICONTROL Delivery scheduling]** &gt; **[!UICONTROL Contact date]**.

   ![](assets/send-time_opt_formula_expression_contact_date.png)

   Dadurch können Sie das im Feld **[!UICONTROL Versandstart am]spezifizierte Datum und die Uhrzeit abrufen.**

   Wählen Sie in der Funktionsliste die Option **[!UICONTROL ToInteger aus]**. In the available fields, select **[!UICONTROL Additional data]** &gt; **[!UICONTROL Segment code]**.

   ![](assets/send-time_opt_formula_expression_segment_code.png)

   Dadurch können Sie die in den Segmentcodes spezifizierten Zahlen abrufen.

   Sie erhalten die folgende Formel:

   ```
   AddHours([currentDelivery/scheduling/@contactDate], ToInteger([targetData/@segmentCode]))
   ```

1. Validieren Sie Ihren Ausdruck, um ihn zu speichern. Validieren Sie die Planung, speichern Sie den Versand und starten Sie den Workflow.

* Das erste Segment erhält die Nachricht am Kontaktdatum (25. Mai, 8 Uhr).
* Das zweite Segment erhält die Nachricht zwei Stunden später (25. Mai, 10 Uhr).
* Das dritte Segment erhält die Nachricht sechs Stunden später (25. Mai, 14 Uhr).
* Das vierte Segment erhält die Nachricht acht Stunden später (25. Mai, 16 Uhr).


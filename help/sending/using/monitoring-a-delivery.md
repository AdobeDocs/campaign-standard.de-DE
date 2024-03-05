---
title: Sendungen in Adobe Campaign Standard überwachen
description: Erfahren Sie, wie Sie Sendungen in Adobe Campaign Standard überwachen.
audience: sending
content-type: reference
topic-tags: monitoring-messages
context-tags: delivery,main
feature: Performance Monitoring
role: User
level: Beginner
exl-id: ddc92077-df73-411d-a161-3263581e6945
source-git-commit: ed60bde4785da9a8cc5a6cc0efcdb24e2c1f65e3
workflow-type: ht
source-wordcount: '527'
ht-degree: 100%

---

# Sendungen überwachen{#monitoring-a-delivery}

Es gibt mehrere Möglichkeiten, einen Versand zu überwachen und seine Wirkung zu messen. Als funktionaler Administrator können Sie auf Nachrichtenprotokolle und Versandlogs zugreifen.

>[!IMPORTANT]
>
>Nur funktionale [Administratoren](../../administration/using/users-management.md#functional-administrators) mit **[!UICONTROL Administratorrolle]** und Zugriff auf **alle** Einheiten können auf Versandlogs, Nachrichtenprotokolle, Trackinglogs, Ausschluss-Logs oder Abonnenten-Logs zugreifen. Ein Benutzer ohne Administratorrechte kann diese Protokolle ansprechen, muss aber mit einer verknüpften Tabelle (Profile, Versand) beginnen.

* **Nachrichtenprotokolle**: Diese Protokolle können Sie direkt vom Nachrichten-Dashboard aus abrufen. In ihnen werden Details zum Versand dargestellt und Sie erfahren, welche Zielgruppe warum ausgeschlossen wurde sowie Tracking-Informationen wie z. B. Öffnungen und Klicks.

  Der Zugriff auf die Nachrichtenprotokolle ist über die Schaltfläche unten rechts in der Kachel **[!UICONTROL Bereitstellung]** möglich.

  Die verschiedenen Tabs zeigen (wenn vorhanden) Informationen zu **[!UICONTROL Versandlogs]**, **[!UICONTROL Ausschlusslogs]**, **[!UICONTROL Ausschlussgründen]**, **[!UICONTROL Trackinglogs]** und **[!UICONTROL getrackten URLs]**. Siehe [Versandlogs](#delivery-logs).

  ![](assets/sending_delivery1.png)

  Das Protokoll enthält alle auf den Versand und auf Testsendungen bezogenen Logs. Eventuelle Fehler oder Warnmeldungen werden durch spezifische Symbole hervorgehoben. Lesen Sie diesbezüglich auch den Abschnitt [Nachrichten validieren](../../sending/using/previewing-messages.md).

  Mithilfe der Schaltfläche **[!UICONTROL Liste exportieren]** kann das Protokoll exportiert werden.

  ![](assets/sending_delivery2.png)

* **Auftragsprotokolle**: Eine Liste der durch den Versand ausgelösten Batch-Aufträge kann vom Nachrichten-Dashboard aus aufgerufen werden, indem Sie **[!UICONTROL Auftragsverlauf]** aus der Dropdown-Liste **[!UICONTROL Zusammenfassung]** auswählen.

  Wählen Sie einen beliebigen Auftrag aus der Liste aus, um die Details des ausgewählten **[!UICONTROL Batch-Auftrags]** anzuzeigen.

  ![](assets/sending_delivery8.png)

* **Versandwarnungen**: Um Erfolge und Fehlschläge beim Versand zu verfolgen, ist Adobe Campaign mit einem E-Mail-Warnsystem ausgestattet, über das Benutzer Benachrichtigungen zu wichtigen Systemaktivitäten erhalten.
* **Berichte**: Im Nachrichten-Dashboard können Sie für diese Nachricht mehrere Berichte aufrufen. Zusätzlich ist über das Menü **[!UICONTROL Berichte]** eine vollständige Liste integrierter oder benutzerdefinierter Berichte mit Metriken zu Ihrer Nachricht oder Kampagne abrufbar.
* Administratoren können Logs auch in einer separaten Datei exportieren, die dann in eigenen Berichterstellungs- oder Business Intelligence Tools verarbeitet werden können. Lesen Sie diesbezüglich auch den Abschnitt [Logs exportieren](../../automating/using/exporting-logs.md).

**Verwandte Themen:**

* [Warnungen bei Zustellproblemen erhalten](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Berichte](../../reporting/using/about-dynamic-reports.md)

## Versandlogs {#delivery-logs}

### Versandlogs {#sending-logs}

Der Tab **[!UICONTROL Versandlogs]** zeigt die Liste der einzelnen Nachrichten eines Versands. Hier wird die Liste der gesendeten Nachrichten und deren Status gespeichert. Für jeden einzelnen Empfänger können Sie anhand des Status das Ergebnis des Versands verfolgen.

Für jedes Profil mit dem Status **[!UICONTROL Gesendet]** wird in der Spalte **[!UICONTROL Datum]** der Versandzeitpunkt der Nachricht angezeigt.

![](assets/sending_delivery3.png)

Klicken Sie auf das Stiftsymbol rechts neben der entsprechenden Zeile, um auf die Details eines bestimmten Versandprotokolls zuzugreifen.

![](assets/sending_access-sending-log.png)

Alle Details zum Versandprotokoll sind schreibgeschützt. Sie können auch eine Vorschau der Mirrorseite anzeigen.

![](assets/sending_sending-log.png)

>[!NOTE]
>
>Um das Rendering der Mirrorseite in der Campaign-Benutzeroberfläche anzuzeigen, muss die Server-URL der Mirrorseite sicher sein. Verwenden Sie in diesem Fall https:// anstelle von http://, um diese URL beim [Konfigurieren Ihrer Marke](../../administration/using/branding.md#configuring-and-using-brands) einzurichten.

### Ausschlusslogs {#exclusion-logs}

Der Tab **[!UICONTROL Ausschlusslogs]** zeigt die Liste der vom Versand ausgeschlossenen Empfänger und den jeweiligen Ausschlussgrund an.

![](assets/sending_delivery4.png)

### Ausschlussgründe {#exclusion-causes}

Der Tab **[!UICONTROL Ausschlussgründe]** zeigt die Anzahl an ausgeschlossenen Empfängern pro Ausschlussgrund an.

![](assets/sending_delivery5.png)

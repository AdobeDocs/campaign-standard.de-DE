---
title: Sendungen beobachten
seo-title: Sendungen beobachten
description: Sendungen beobachten
seo-description: Hier erfahren Sie, wie Sie einen Versand nachverfolgen können.
page-status-flag: nie aktiviert
uuid: 7772 c 607-debd -40 fd -8322-4 d 49119979 b 4
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird gesendet
content-type: Referenz
topic-tags: monitoring-messages
discoiquuid: eb 9 fa 216-4568-423 a -9396-8 f 7 b 82181 ae 9
context-tags: delivery, main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: cb6396228e42f99f7e184a82e6c894b09a164cd9

---


# Sendungen beobachten{#monitoring-a-delivery}

Es gibt mehrere Möglichkeiten, einen Versand zu beobachten und seine Wirkung zu messen:

* **Nachrichtenprotokolle**: Diese Protokolle können Sie direkt vom Nachrichten-Dashboard aus abrufen. In ihnen werden Details zum Versand dargestellt und Sie erfahren, welche Zielgruppe warum ausgeschlossen wurde sowie Tracking-Informationen wie z. B. Öffnungen und Klicks.

   Der Zugriff auf die Nachrichtenprotokolle ist über die Schaltfläche rechts unten in der **[!UICONTROL Freigabe]-Kachel möglich.**

   Several tabs contain information (if it exists) regarding the **[!UICONTROL Sending logs]**, **[!UICONTROL Exclusion logs]**, **[!UICONTROL Exclusion causes]**, **[!UICONTROL Tracking logs]** and **[!UICONTROL Tracked URLs]**. Siehe [Versandlogs](../../sending/using/monitoring-a-delivery.md#delivery-logs).

   ![](assets/sending_delivery1.png)

   Das Protokoll enthält alle auf den Versand und auf Testsendungen bezogenen Logs. Eventuelle Fehler oder Warnmeldungen werden durch spezifische Symbole hervorgehoben. Lesen Sie diesbezüglich auch den Abschnitt [Nachrichten validieren](../../sending/using/previewing-messages.md).

   Mithilfe der Schaltfläche **[!UICONTROL Liste exportieren]kann das Protokoll exportiert werden.**

   ![](assets/sending_delivery2.png)

* **Versandwarnungen**: Um Erfolge und Fehlschläge beim Versand zu verfolgen, ist Adobe Campaign mit einem E-Mail-Warnsystem ausgestattet, über das Benutzer Benachrichtigungen zu wichtigen Systemaktivitäten erhalten.
* **Berichte**: Im Nachrichten-Dashboard können Sie für diese Nachricht mehrere Berichte aufrufen. Zusätzlich ist über ein **[!UICONTROL Berichte]-Menü eine vollständige Liste integrierter oder benutzerdefinierter Berichte mit Messwerten zu Ihrer Nachricht oder Kampagne abrufbar.**
* Administratoren können Logs auch in einer separaten Datei exportieren, die dann in eigenen Berichterstellungs- oder Business Intelligence Tools verarbeitet werden können. Lesen Sie diesbezüglich auch den Abschnitt [Logs exportieren](../../automating/using/exporting-logs.md).

**Verwandte Themen:**

* [Warnungen bei Zustellproblemen erhalten](../../sending/using/receiving-alerts-when-failures-happen.md)
* [Berichte](../../reporting/using/about-dynamic-reports.md)

## Versandlogs {#delivery-logs}

### Versandlogs {#sending-logs}

Der **[!UICONTROL Versandlogs]-Tab zeigt die Liste der einzelnen Nachrichten eines Versands** sowie deren Status an. Für jeden einzelnen Empfänger können Sie anhand des Status das Ergebnis des Versands verfolgen.

Für jedes Profil mit dem Status **[!UICONTROL Gesendet]** wird in der Spalte **Datum]der Versandzeitpunkt der Nachricht angezeigt.[!UICONTROL **

![](assets/sending_delivery3.png)

### Ausschlusslogs {#exclusion-logs}

Der **[!UICONTROL Ausschlusslogs]-Tab zeigt die Liste der vom Versand ausgeschlossenen Empfänger und den jeweiligen Ausschlussgrund an.**

![](assets/sending_delivery4.png)

### Ausschlussgründe {#exclusion-causes}

Der **[!UICONTROL Ausschlussgründe]-Tab zeigt die Anzahl an ausgeschlossenen Empfängern pro Ausschlussgrund an.**

![](assets/sending_delivery5.png)


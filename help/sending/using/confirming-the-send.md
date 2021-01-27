---
solution: Campaign Standard
product: campaign
title: Versand bestätigen
description: Hier erfahren Sie, wie die Nachrichtenvorbereitung abgeschlossen wird.
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages
context-tags: delivery,deployment,back
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 100%

---


# Versand bestätigen{#confirming-the-send}

Nach erfolgreicher Vorbereitung und Validierung Ihrer Nachrichten können Sie den Versandstart bestätigen. Weiterführende Informationen zur Nachrichtenvorbereitung finden Sie im Abschnitt [Versandvorbereitung](../../sending/using/preparing-the-send.md).

Nur Benutzer mit der Benutzerrolle **[!UICONTROL Sendungen starten]** können den Versand bestätigen. Lesen Sie diesbezüglich auch den Abschnitt [Liste der Rollen](../../administration/using/list-of-roles.md).

Benutzern, die nicht diese Benutzerrolle besitzen, wird diese Nachricht angezeigt:

![](assets/confirm_delivery_2.png)

Verwenden Sie die Schaltfläche **[!UICONTROL Versand bestätigen]**, um die Nachrichten abzusenden.

![](assets/confirm_delivery.png)

Valdieren Sie über die Schaltfläche **[!UICONTROL OK]**.

![](assets/confirm_delivery1.png)

Die Versandverarbeitung ist in Gang.

>[!NOTE]
>
>Wenn die Nachricht terminiert wurde, wird sie gesendet, sobald der Zeitpunkt erreicht wurde. Weiterführende Informationen zum Terminieren von Nachrichten finden Sie in [diesem Abschnitt](../../sending/using/about-scheduling-messages.md).

Wenn Sie einen wiederkehrenden Versand ohne Aggregat-Zeitraum verwenden, können Sie vor dem Senden der Nachrichten eine Bestätigung anfordern. Öffnen Sie dazu im Versand-Dashboard die Kachel **[!UICONTROL Planung]** und aktivieren Sie die entsprechende Option.

![](assets/confirmation_recurring_deliveries.png)

Die Kachel **[!UICONTROL Freigabe]** zeigt den Verarbeitungsfortschritt an.

Nach Abschluss des Versands an die Kontakte zeigt die **[!UICONTROL Freigabe]**-Kachel Ihre KPI-Daten (Key Performance Indicators) an:

* Anzahl zu sendender Nachrichten
* Anzahl gesendeter Nachrichten
* Anteil zugestellter Nachrichten,
* Anteil von Bounces und Fehlern
* Anteil offener Nachrichten
* Anteil an Nachrichten, in denen geklickt wurde (im Fall von E-Mails).

   >[!NOTE]
   >
   >Die **[!UICONTROL Öffnungsrate]** und die **[!UICONTROL Clickthrough-Rate]** werden stündlich aktualisiert.

![](assets/sending_delivery.png)

Wenn es zu lange dauert, bis die KPIs aktualisiert sind oder die Ergebnisse in den Versandlogs nicht berücksichtigt werden, wählen Sie die Schaltfläche **[!UICONTROL Statistiken berechnen]** im Fenster **[!UICONTROL Freigabe]** aus.

![](assets/sending_delivery7.png)

Die Nachricht erscheint außerdem im Verlauf der in der Audience enthaltenen Profile. Näheres wird in Abschnitt [Integriertes Kundenprofil](../../audiences/using/integrated-customer-profile.md) beschrieben.

Nach dem Versand einer Nachricht können Sie das Verhalten des Empfängers nachverfolgen und beobachten, um die Wirkung der Nachricht zu messen. Lesen Sie diesbezüglich auch diese Abschnitte:

* [Nachrichten tracken](../../sending/using/tracking-messages.md)
* [Sendungen beobachten](../../sending/using/monitoring-a-delivery.md)


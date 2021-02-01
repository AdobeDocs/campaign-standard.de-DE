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
source-git-commit: b48e246ee515d2f250d866ed72d5765bf1ccb326
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 21%

---


# Versand bestätigen{#confirming-the-send}

Nach erfolgreicher Vorbereitung und Validierung Ihrer Nachrichten können Sie den Versandstart bestätigen. Weiterführende Informationen zur Nachrichtenvorbereitung finden Sie im Abschnitt [Versandvorbereitung](../../sending/using/preparing-the-send.md).

Nur Benutzer mit der Benutzerrolle **[!UICONTROL Sendungen starten]** können den Versand bestätigen. Lesen Sie diesbezüglich auch den Abschnitt [Liste der Rollen](../../administration/using/list-of-roles.md).

<!--Users without this role will see the following message: 

![](assets/confirm_delivery_2.png)-->

## Nachricht senden {#sending-message}

Nachdem die Vorbereitung abgeschlossen ist, befolgen Sie die folgenden Schritte, um Ihre Nachricht zu senden.

1. Klicken Sie auf die Schaltfläche **[!UICONTROL Senden]** bestätigen in der Aktionsleiste der Nachricht.

   ![](assets/confirm_delivery.png)

1. Schließen Sie den Senden ab, indem Sie auf die Schaltfläche **[!UICONTROL OK]** klicken.

   ![](assets/confirm_delivery1.png)

1. Warten Sie, während die Nachricht gesendet wird. Die Kachel **[!UICONTROL Freigabe]** zeigt den Verarbeitungsfortschritt an.

>[!NOTE]
>
>Wenn die Nachricht terminiert wurde, wird sie gesendet, sobald der Zeitpunkt erreicht wurde. Weiterführende Informationen zum Terminieren von Nachrichten finden Sie in [diesem Abschnitt](../../sending/using/about-scheduling-messages.md).

Wenn Sie einen wiederkehrenden Versand ohne Aggregat-Zeitraum verwenden, können Sie vor dem Senden der Nachrichten eine Bestätigung anfordern. Öffnen Sie dazu beim Konfigurieren der Nachricht den Block **[!UICONTROL Plan]** des Versand-Dashboards und aktivieren Sie die dedizierte Option.

![](assets/confirmation_recurring_deliveries.png)

## Die Meldungsindikatoren {#message-indicators}

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

Wenn die KPIs zu lange aktualisiert werden oder die Ergebnisse aus den sendenden Protokollen nicht berücksichtigt werden, klicken Sie im Fenster **[!UICONTROL Bereitstellung]** auf die Schaltfläche **[!UICONTROL Statistik berechnen]**.

![](assets/sending_delivery7.png)

Die Nachricht kann im Verlauf eines der zielgerichteten Profil angezeigt werden. Näheres wird in Abschnitt [Integriertes Kundenprofil](../../audiences/using/integrated-customer-profile.md) beschrieben.

Nachdem eine Nachricht gesendet wurde, können Sie das Verhalten der Empfänger verfolgen und sie überwachen, um die Auswirkungen zu messen. Lesen Sie diesbezüglich auch diese Abschnitte:

* [Nachrichten tracken](../../sending/using/tracking-messages.md)
* [Sendungen beobachten](../../sending/using/monitoring-a-delivery.md)

### Versand-Erfolgserfolg-Berichte {#delivered-status-report}

>[!NOTE]
>
>Dieser Abschnitt gilt nur für E-Mail-Kanal.

In der **[!UICONTROL Zusammenfassung]**-Ansicht jeder E-Mail werden die **[!UICONTROL Ausgelieferten]**-prozentualen Beginn zu 100 % und dann im gesamten Versand [die Gültigkeitsdauer](../../administration/using/configuring-email-channel.md#validity-period-parameters) schrittweise verringert, während die weichen und festen Absprünge zurückgemeldet werden<!--from the Enhanced MTA to Campaign-->.

Tatsächlich werden alle Meldungen in den [Versandprotokollen](../../sending/using/monitoring-a-delivery.md#sending-logs) als **[!UICONTROL Gesendet]** angezeigt, sobald sie erfolgreich von der Kampagne an den Enhanced MTA (Message Transfer Agent) weitergeleitet werden. Sie bleiben in diesem Status, es sei denn, oder bis ein [bounce](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons) für diese Meldung von der erweiterten MTA an die Kampagne zurückgesendet wird.

Wenn Meldungen mit festem Absprung von der erweiterten MTA zurückgesendet werden, ändert sich ihr Status von **[!UICONTROL Gesendet]** in **[!UICONTROL Fehlgeschlagen]** und der **[!UICONTROL Ausgelieferte]**-Prozentsatz wird entsprechend verringert.

Wenn Meldungen mit weichem Zeilensprung aus der erweiterten MTA zurückgegeben werden, werden sie weiterhin als **[!UICONTROL Gesendet]** angezeigt und der **[!UICONTROL Ausgelieferte]**-Prozentsatz wird noch nicht aktualisiert. Soft-bouncing-Meldungen werden dann [erneut versucht](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure) während der Gültigkeitsdauer des Versands:

* Wenn ein erneuter Versuch vor Ende der Gültigkeitsdauer erfolgreich war, bleibt der Meldungsstatus weiterhin **[!UICONTROL Gesendet]** und der **[!UICONTROL Ausgelieferte]**-Prozentsatz bleibt unverändert.

* Andernfalls ändert sich der Status in **[!UICONTROL Fehlgeschlagen]** und der **[!UICONTROL Ausgelieferte]**-Prozentsatz wird entsprechend verringert.

<!--Soft-bouncing messages increment an error counter. When the error counter reaches the limit threshold or when the validity period is over, their status changes to **[!UICONTROL Failed]**.-->

<!--For more on retries after a delivery temporary failure, see [this section](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).-->

Daher sollten Sie bis zum Ende der Gültigkeitsdauer warten, um die finale **[!UICONTROL Ausgelieferte]** Prozentzahl und die endgültige Anzahl der tatsächlich gesendeten **[!UICONTROL und**[!UICONTROL  Fehlgeschlagenen ]**Meldungen anzuzeigen.]**

### Email Feedback Service (Beta) {#email-feedback-service}

>[!NOTE]
>
>Dieser Abschnitt gilt nur für E-Mail-Kanal.

Mit der EFS-Funktion (Email Feedback Service) wird der Status jeder E-Mail genau gemeldet, da Feedback direkt vom Enhanced MTA (Message Transfer Agent) erfasst wird.

>[!IMPORTANT]
>
>Der E-Mail-Feedback-Dienst ist derzeit als Betafunktion verfügbar.

Nachdem der Versand gestartet wurde, ändert sich der Prozentsatz für **[!UICONTROL Ausgeliefert]** nicht mehr, wenn die Nachricht erfolgreich von der Kampagne auf die erweiterte MTA übertragen wurde.

![](assets/efs-sending.png)

Die Versandlogs zeigen den Status **[!UICONTROL Ausstehend]** für jede Zieladresse an.

![](assets/efs-pending.png)

Wenn die Nachricht tatsächlich an die zielgerichteten Profil gesendet wird und diese Informationen in Echtzeit aus dem erweiterten MTA gemeldet werden, zeigen die Versandlogs den Status **[!UICONTROL Gesendet]** für jede Adresse an, die die Nachricht erfolgreich erhalten hat. Der Prozentsatz **[!UICONTROL Ausgeliefert]** wird mit jedem erfolgreichen Versand entsprechend erhöht.

Wenn Meldungen mit festem Absprung aus der erweiterten MTA zurückgegeben werden, ändert sich ihr Protokollstatus von **[!UICONTROL Ausstehend]** in **[!UICONTROL Fehlgeschlagen]** und der Prozentsatz **[!UICONTROL Absprünge + Fehler]** wird entsprechend erhöht.

Wenn Meldungen mit weichem Absprung aus dem erweiterten MTA zurückgegeben werden, ändert sich auch ihr Protokollstatus von **[!UICONTROL Ausstehend]** in **[!UICONTROL Fehlgeschlagen]** und der Prozentsatz **[!UICONTROL Absprünge + Fehler]** wird entsprechend erhöht. Der Prozentsatz **[!UICONTROL Ausgeliefert]** bleibt unverändert. Soft-bouncing-Meldungen werden dann während des gesamten Versands [Gültigkeitsdauer](../../administration/using/configuring-email-channel.md#validity-period-parameters) erneut versucht:

* Wenn ein erneuter Versuch vor Ende der Gültigkeitsdauer erfolgreich war, wird der Status der Nachricht auf **[!UICONTROL Gesendet]** und der **[!UICONTROL Ausgeliefert]**-Prozentsatz entsprechend erhöht.

* Andernfalls bleibt der Status **[!UICONTROL Fehlgeschlagen]**. Die Prozentsätze **[!UICONTROL Ausgeliefert]** und **[!UICONTROL Absprünge + Fehler]** bleiben unverändert.

>[!NOTE]
>
>Weitere Informationen zu harten und weichen Absprüngen finden Sie in [diesem Abschnitt](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons).
>
>Weitere Informationen zu weiteren Zustellversuchen nach einem temporären Fehler eines Versands finden Sie in [diesem Abschnitt](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure).

<!--Soft-bouncing messages increment an error counter. When the error counter reaches the limit threshold or when the validity period is over, the address goes into quarantine and the status remains as **[!UICONTROL Failed]**. For more on conditions for sending an address to quarantine, see [this section](../../help/sending/using/understanding-quarantine-management.md#conditions-for-sending-an-address-to-quarantine).-->

### Von EFS {#changes-introduced-by-efs} eingeführte Änderungen

Die nachstehende Tabelle zeigt die Änderungen bei KPIs und dem Senden von Protokollstatus, die durch die EFS-Funktion eingeführt wurden.

| Schritt in den sendenden Prozess<br> | KPI-Zusammenfassung<br>OHNE EFS | Protokollstatus senden<br>OHNE EFS | KPI-Zusammenfassung<br>MIT EFS | Protokollstatus<br>MIT EFS senden |
|--- |--- |--- | --- | --- |
| Nachricht wird erfolgreich von der Kampagne auf die erweiterte MTA weitergeleitet | <ul><li>**[!UICONTROL Ausgelieferte]** prozentuale Beginn zu 100 %</li><li>**[!UICONTROL Absprünge +]** Verursacher-Beginn bei 0 %</li></ul> | Gesendet | <ul><li>**[!UICONTROL Ausgelieferte]** prozentuale Beginn zu 0 %</li><li>**[!UICONTROL Absprünge +]** Verursacher-Beginn bei 0 %</li></ul> | Ausstehend |
| Hartabschneidende Nachrichten werden aus der erweiterten MTA zurückgemeldet. | <ul><li>**[!UICONTROL Der]** gelieferte Prozentsatz wird entsprechend verringert</li><li>**[!UICONTROL Bounces +]** errorspercentage wird entsprechend erhöht</li></ul> | Fehlgeschlagen | <ul><li>Keine Änderung des Prozentsatzes **[!UICONTROL Ausgeliefert]**</li><li>**[!UICONTROL Bounces +]** errorspercentage wird entsprechend erhöht</li></ul> | Fehlgeschlagen |
| Soft-bouncing-Meldungen werden aus der erweiterten MTA zurückgemeldet | <ul><li>Keine Änderung des Prozentsatzes **[!UICONTROL Ausgeliefert]**</li><li>Keine Änderung des Prozentsatzes **[!UICONTROL Absprünge + Fehler]**</li></ul> | Gesendet | <ul><li>Keine Änderung des Prozentsatzes **[!UICONTROL Ausgeliefert]**</li><li>**[!UICONTROL Bounces +]** errorspercentage wird entsprechend erhöht</li></ul> | Fehlgeschlagen |
| Absprüngliche Meldungen: weitere Zustellversuche sind erfolgreich | <ul><li>Keine Änderung des Prozentsatzes **[!UICONTROL Ausgeliefert]**</li><li>Keine Änderung des Prozentsatzes **[!UICONTROL Absprünge + Fehler]**</li></ul> | Gesendet | <ul><li>**[!UICONTROL Der]** gelieferte Prozentsatz wird entsprechend erhöht</li><li>**[!UICONTROL Absprünge +]** Errorspercentage werden entsprechend verringert</li></ul> | Gesendet |
| Weitere Zustellversuche mit Soft-Bouncing-Meldungen schlagen fehl | <ul><li>**[!UICONTROL Der]** gelieferte Prozentsatz wird entsprechend verringert</li><li>**[!UICONTROL Bounces +]** errorspercentage wird entsprechend erhöht</li></ul> | Fehlgeschlagen | <ul><li> Keine Änderung des Prozentsatzes **[!UICONTROL Ausgeliefert]** </li><li> Keine Änderung des Prozentsatzes **[!UICONTROL Absprünge + Fehler]** </li></ul> | Fehlgeschlagen |

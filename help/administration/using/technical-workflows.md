---
title: Technische Workflows
description: Erfahren Sie mehr über technische Workflows
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: da3a3af5-207a-4289-bd07-00a8c5d1cf57
TQID: https://experienceleague.adobe.com/imU-lsjNUEb2VZ-hLLAobuJ0UFlFqygQD-KE80hRpG0
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
subfeature_v2: id: ca3c1dd6-bdd2-41a9-bc5a-e35f5cca9e63
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: beb7a3c1-66ab-4786-b879-7621375b3c40id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 803
ht-degree: 79%

---

# Technische Workflows{#technical-workflows}

Die technischen Workflows sind standardmäßig in Adobe Campaign enthalten. Technische Workflows dienen der programmierten periodischen Ausführung von Server-Aufträgen.

Hierbei kann es sich beispielsweise um die Wartung der Datenbank, den Abruf von Trackinginformationen oder die Einrichtung von geplanten Versandvorgängen handeln. Der Zugriff auf technische Workflows erfolgt über das Adobe-Campaign-Logo oben links im Bildschirm.

Funktionale Administratoren können auf technische Workflows über das Menü **[!UICONTROL Administration > Anwendungskonfiguration > Workflows]** zugreifen.

>[!NOTE]
>
>Als funktionaler Administrator können Sie technische Workflows aussetzen oder neu starten und ihre Eigenschaften und Struktur ändern.

![](assets/technical_workflows.png)

## Liste der technischen Workflows {#list-of-technical-workflows}

Technische Workflows dienen der Verwaltung automatischer Hintergrundprozesse und technischer Verfahren in Adobe Campaign.

<table> 
 <tbody> 
  <tr> 
   <td> <strong>Titel</strong><br /> </td> 
   <td> <strong>Kennung</strong><br /> </td> 
   <td> <strong>Beschreibung</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">A/B-Test</span> <br /> </td> 
   <td> <span class="uicontrol">abTesting</span> <br /> </td> 
   <td> Dieser Workflow analysiert die Tracking-Protokolle der einzelnen Varianten. Am Ende der Testphase des A/B-Tests berechnet er automatisch die Gewinnervariante. Er wird standardmäßig täglich gestartet.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Fakturierung</span> <br /> </td> 
   <td> <span class="uicontrol">billing</span> <br /> </td> 
   <td> Dieser Workflow übermittelt per E-Mail den Aktivitätsbericht des Systems an den fakturierungsverantwortlichen Benutzer ('billing'). Er wird standardmäßig automatisch täglich um 1 Uhr gestartet.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Header aus Versandvorlagen kopieren</span> <br /> </td> 
   <td> <span class="uicontrol">smtpHeaderupdate</span> <br /> </td> 
   <td> Dieser Workflow kopiert die für E-Mail-Versandvorlagen festgelegten SMTP-Header in die entsprechenden untergeordneten Sendungen ohne Vorlagen. Von diesem Workflow werden nur E-Mail-Marketing-Sendungen erfasst. SMTP-Header werden nicht in Transaktions- und Testsendungen kopiert. <br> Dieser Workflow wird nicht regelmäßig ausgeführt. Sie muss vom Benutzer pro Verwendung gestartet werden. <!--So it'not really a technical workflow like all workflows on this page, because it's not run automatically - TBC--> <br> Wenn Ihre Instanz eine große Versandmenge aufweist, können Sie die Option NmsCleanup_DeliveryPurgeDelay in den <strong>Anwendungseinstellungen</strong> aktualisieren. Wenn Sie die SMTP-Header einer Vorlage ändern, müssen Sie den Workflow nach der Änderung erneut ausführen, damit die korrigierten Header in Sendungen ohne Vorlagen kopiert werden.<a href="data-retention.md#deliveries">Weitere Informationen</a>
   <br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Datenbankbereinigung</span> <br /> </td> 
   <td> <span class="uicontrol">cleanup</span> <br /> </td> 
   <td> Dieser Workflow dient der Datenbankwartung. Er berechnet diverse Statistiken und Vorgänge und bereinigt obsolete Daten gemäß den definierten Parametern. Er wird standardmäßig täglich um 4 Uhr gestartet.<br /> </td> 
  </tr>
  <tr> 
   <td> <span class="uicontrol">Freigegebene Zielgruppe importieren</span> <br /> </td> 
   <td> <span class="uicontrol">importSharedAudience</span> <br /> </td> 
   <td> Dieser Workflow synchronisiert die Daten von aus Adobe Experience Cloud in Adobe Campaign importierten Zielgruppen. Er wird standardmäßig stündlich gestartet.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Sofortige Berichtfreigabe</span> <br /> </td> 
   <td> <span class="uicontrol">reportSendingNow</span> <br /> </td> 
   <td> Dieser Workflow startet, unmittelbar nachdem der Versandzeitpunkt eines Bericht definiert wurde. Ihr Bericht wird dann in eine PDF-Datei umgewandelt, die per E-Mail an die Empfänger gesendet wird.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">KPI-Abstimmung mit Adobe Analytics</span> <br /> </td> 
   <td> <span class="uicontrol">kpiReconciliation</span> <br /> </td> 
   <td> Dieser Workflow ruft die KPI-Daten einmal täglich vom Reporting-Dienst ab und stimmt sie mit den Daten in Adobe Analytics ab. Danach wird die Differenz bei Bedarf übertragen. Er wird standardmäßig täglich um 4.20 Uhr gestartet.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Message Center Lokale Archivierung</span> <br /> </td> 
   <td> <span class="uicontrol">mcSynch_local</span> <br /> </td> 
   <td> Dieser Workflow archiviert die Echtzeit-Ereignisse in einer Verlaufstabelle. Er wird standardmäßig stündlich gestartet.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Bericht-Aggregate</span> <br /> </td> 
   <td> <span class="uicontrol">reportingAggregates</span> <br /> </td> 
   <td> Dieser Workflow aktualisiert die in Berichten verwendeten Aggregate. Er wird standardmäßig täglich um 2 Uhr gestartet.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">KPIs mit Adobe Analytics teilen</span> <br /> </td> 
   <td> <span class="uicontrol">kpiSharing</span> <br /> </td> 
   <td> Dieser Workflow überträgt alle 15 Minuten KPI-Daten von Adobe Campaign Standard zu Adobe Analytics.<br /> </td> 
  </tr> 
    </tr> 
   <tr> 
   <td> <span class="uicontrol">Mit Launch synchronisieren </span> <br /> </td> 
   <td> <span class="uicontrol">SyncWithLaunch</span> <br /> </td> 
   <td> Dieser Workflow synchronisiert die Tag-Eigenschaften für Mobilgeräte, die in Adobe Campaign Standard importiert wurden. Er wird alle 15 Minuten gestartet.<br /> </td> 
  </tr>
  <tr> 
   <td> <span class="uicontrol">Trackinglog-Wiederherstellung</span> <br /> </td> 
   <td> <span class="uicontrol">SyncWithLaunch</span> <br /> </td> 
   <td> Dieser Workflow synchronisiert die Tag-Eigenschaften für Mobilgeräte, die in Adobe Campaign Standard importiert wurden. Er wird alle 15 Minuten gestartet.<br /> </td> 
  </tr>
  <tr> 
   <td> <span class="uicontrol">Trackinglogs wiederherstellen</span> <br /> </td> 
   <td> <span class="uicontrol">trackingLogRecovery</span> <br /> </td> 
   <td> Dieser Workflow stellt verlorene Trackinglogs wieder her. Beachten Sie, dass dieser technische Workflow nur in bestimmten Kontexten verwendet wird und auf die interne Verwendung in Adobe beschränkt ist. <br> Er wird standardmäßig alle zehn Minuten gestartet.<br /> </td> 
  </tr>
  <tr> 
   <td> <span class="uicontrol">Update der Versandausführung</span> <br/> </td> 
   <td> <span class="uicontrol">updateDeliveryExecInfo</span> <br/> </td> 
   <td> Dieser Workflow kopiert die Broadlogs und Trackinglogs in die lokale Datenbank. Er wird standardmäßig alle zehn Minuten gestartet.<br/> </td> 
  </tr>
  <tr> 
   <td> <span class="uicontrol">Aktualisierung der Versandindikatoren</span> <br /> </td> 
   <td> <span class="uicontrol">updateDeliveryIndicators</span> <br /> </td> 
   <td> Dieser Workflow aktualisiert die Versand-KPIs (Key Performance Indicators). Er wird standardmäßig stündlich gestartet.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Update des Ereignisstatus</span> <br /> </td> 
   <td> <span class="uicontrol">updateEventsStatus</span> <br /> </td> 
   <td> Dieser Workflow ordnet Ereignissen einen Status zu. Folgende Status sind möglich:<br /> <strong>Ausstehend</strong>: Das Ereignis befindet sich in der Warteschlange. Ihr wurde noch keine Nachrichtenvorlage zugewiesen.<br /> <span class="uicontrol">Versand ausstehend</span> : Das Ereignis befindet sich in der Warteschlange, wurde einer Nachrichtenvorlage zugeordnet und wird vom Versand verarbeitet.<br /> <strong>Gesendet</strong>: Dieser Status wird aus den Versandlogs kopiert. Das bedeutet, dass der Versand durchgeführt wurde.<br /> <strong>Vom Versand ignoriert</strong> Dieser Status wird aus den Versandlogs kopiert. Das bedeutet, dass der Versand ignoriert wurde.<br /> <strong>Versand fehlgeschlagen</strong>: Dieser Status wird aus den Versandlogs übernommen. Dies bedeutet, dass der Versand fehlgeschlagen ist.<br /> <span class="uicontrol">Ereignis wurde nicht berücksichtigt</span> : Das Ereignis konnte keiner Nachrichtenvorlage zugeordnet werden. Es erfolgt kein weiterer Versuch der Ereignisverarbeitung.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Zustellbarkeit</span> <br /> </td> 
   <td> <span class="uicontrol">deliverabilityUpdate</span> <br /> </td> 
   <td> Dieser Workflow erstellt die Liste der Qualifizierungsregeln für Bounce Messages sowie die Domain- und MX-Liste der Plattform. Der Workflow wird nur bei geöffnetem HTTPS-Port ausgeführt. Er wird standardmäßig täglich um 2 Uhr gestartet.<br /> </td> 
  </tr> 
 </tbody> 
</table>

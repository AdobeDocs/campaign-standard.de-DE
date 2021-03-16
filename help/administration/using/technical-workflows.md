---
solution: Campaign Standard
product: campaign
title: Technische Workflows
description: Technische Workflows sind vordefinierte Workflows für im Hintergrund ablaufende technische Prozesse in Adobe Campaign. Sie gewährleisten das korrekte Funktionieren der Plattform.
audience: administration
content-type: reference
topic-tags: application-settings
feature: Instanzeinstellungen
role: Administrator
level: Erfahren
translation-type: tm+mt
source-git-commit: a7a1aa2841410674597264927325c073fef4ce26
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 99%

---


# Technische Workflows{#technical-workflows}

Die technischen Workflows sind standardmäßig in Adobe Campaign enthalten. Technische Workflows dienen der programmierten periodischen Ausführung von Server-Vorgängen.

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
   <td> <span class="uicontrol">Datenbankbereinigung</span> <br /> </td> 
   <td> <span class="uicontrol">cleanup</span> <br /> </td> 
   <td> Dieser Workflow dient der Datenbankwartung. Er berechnet diverse Statistiken und Vorgänge und bereinigt obsolete Daten gemäß den definierten Parametern. Er wird standardmäßig täglich um 4 Uhr gestartet.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Planungen</span> <br /> </td> 
   <td> <span class="uicontrol">forecasting</span> <br /> </td> 
   <td> Dieser Workflow analysiert die im Planungskalender verzeichneten Sendungen (Erstellung von Planungslogs). Er wird standardmäßig täglich um 1 Uhr gestartet. <br /> </td> 
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
   <td> Dieser Workflow synchronisiert die Adobe Launch-Eigenschaften für Mobilgeräte, die in Adobe Campaign Standard importiert wurden. Er wird alle 15 Minuten gestartet.<br /> </td> 
  </tr>
  <tr> 
   <td> <span class="uicontrol">Update der Versandausführung</span> <br /> </td> 
   <td> <span class="uicontrol">updateDeliveryExecInfo</span> <br /> </td> 
   <td> Dieser Workflow aktualisiert die Tracking-Indikatoren des Versands. Er wird standardmäßig alle zehn Minuten gestartet.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Aktualisierung der Versandindikatoren</span> <br /> </td> 
   <td> <span class="uicontrol">updateDeliveryIndicators</span> <br /> </td> 
   <td> Dieser Workflow aktualisiert die Versand-KPIs (Key Performance Indicators). Er wird standardmäßig stündlich gestartet.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Update des Ereignisstatus</span> <br /> </td> 
   <td> <span class="uicontrol">updateEventsStatus</span> <br /> </td> 
   <td> Dieser Workflow ordnet Ereignissen einen Status zu. Folgende Status sind möglich:<br /> <strong>Ausstehend</strong>: Das Ereignis befindet sich in der Warteschlange. Es wurde noch keine Nachrichtenvorlage zugeordnet.<br /> <span class="uicontrol">Versand ausstehend</span>: Das Ereignis befindet sich in der Warteschlange, eine Nachrichtenvorlage wurde zugeordnet und die Verarbeitung durch den Versand hat begonnen.<br /> <strong>Gesendet</strong>: Dieser Status wird aus den Versandlogs übernommen. Er bedeutet, dass die Nachrichten versendet wurden.<br /> <strong>Vom Versand ignoriert</strong>: Dieser Status wird aus den Versandlogs übernommen. Er bedeutet, dass kein Versand vorgenommen bzw. die Sendung ignoriert/nicht berücksichtigt wurde.<br /> <strong>Versandfehler</strong>: Dieser Status wird aus den Versandlogs übernommen. Er bedeutet, dass der Versand fehlgeschlagen ist.<br /> <span class="uicontrol">Ereignis wurde nicht übernommen</span>: Dem Ereignis konnte keine Nachrichtenvorlage zugeordnet werden. Es erfolgt kein weiterer Versuch der Ereignisverarbeitung.<br /> </td> 
  </tr> 
  <tr> 
   <td> <span class="uicontrol">Zustellbarkeit</span> <br /> </td> 
   <td> <span class="uicontrol">deliverabilityUpdate</span> <br /> </td> 
   <td> Dieser Workflow erstellt die Liste der Qualifizierungsregeln für Bounce Messages sowie die Domain- und MX-Liste der Plattform. Der Workflow wird nur bei geöffnetem HTTPS-Port ausgeführt. Er wird standardmäßig täglich um 2 Uhr gestartet.<br /> </td> 
  </tr> 
 </tbody> 
</table>


---
title: Indikatorberechnung
description: Hier erhalten Sie Informationen über die Ergebnisse Ihrer Berichte mit einer Liste mit Metrik-Formeln.
page-status-flag: never-activated
uuid: dfbc9d7e-62db-4e77-bb8e-0ac826ec7333
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: about-reporting
discoiquuid: 45b11631-6b32-4074-8c8d-affd06407810
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 100%

---


# Indikatorberechnung{#indicator-calculation}

>[!NOTE]
>
>Um große Volumen und Echtzeitanalysen besser verarbeiten und verwalten zu können, legt die dynamische Berichterstellung für die Zählung unterschiedlicher Werte approximierte Aggregationen zugrunde. Approximierte Aggregationen halten die Speichernutzung in Grenzen und sind häufig schneller als die Berechnung exakter Werte.

In den Tabellen unten finden Sie nach Versandtyp geordnet die Liste der Indikatoren, die in Berichten verwendet werden, sowie ihre Berechnungsformeln.

## E-Mail-Versand        {#email-delivery}

<table> 
 <thead> 
  <tr> 
   <th> <strong>Titel</strong> <br /> </th> 
   <th> <strong>Feldname</strong> <br /> </th> 
   <th> <strong>Formel zur Indikatorberechnung</strong> <br /> </th> 
   <th> <strong>Erklärung</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Konto deaktiviert<br /> </td> 
   <td> @disabled<br /> </td> 
   <td> count(@failureReason=4)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Auf Blockierungsliste<br /> </td> 
   <td> @blacklisted<br /> </td> 
   <td> count(@failureReason=8, @failureType=2)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Blockierungslistenrate<br /> </td> 
   <td> @rateBlacklisted<br /> </td> 
   <td> @blacklisted/@sent<br /> </td> 
   <td> Der Denominator für die Berechnung der Rate basiert auf der Anzahl der gesendeten Nachrichten (Zugestellt + Bounces).<br /> </td> 
  </tr> 
  <tr> 
   <td> Bounces + Fehler<br /> </td> 
   <td> @bounces<br /> </td> 
   <td> count(@status=2)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Bounce- + Fehlerrate<br /> </td> 
   <td> @rateBounces<br /> </td> 
   <td> @bounces/@sent<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Klicks<br /> </td> 
   <td> @clicks<br /> </td> 
   <td> count(@trackingUrlType=1 oder 10 oder 11)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Durchklickrate<br /> </td> 
   <td> @clickthrough<br /> </td> 
   <td> @uniqueclicks/@delivered<br /> </td> 
   <td> Der Denominator für die Berechnung der Rate basiert nur auf der Anzahl der zugestellten Nachrichten.<br /> </td> 
  </tr> 
  <tr> 
   <td> Zugestellt<br /> </td> 
   <td> @delivered<br /> </td> 
   <td> count(@status=1)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Zustellrate<br /> </td> 
   <td> @rateDelivered<br /> </td> 
   <td> @delivered/@sent<br /> </td> 
   <td> Der Denominator für die Berechnung der Rate basiert auf der Anzahl der gesendeten Nachrichten (Zugestellt + Bounces).<br /> </td> 
  </tr> 
  <tr> 
   <td> Hardbounces<br /> </td> 
   <td> @hardBounces<br /> </td> 
   <td> count(@failureType=2 AND @failureReason=8)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Hardbounce-Rate<br /> </td> 
   <td> @rateHardBounces<br /> </td> 
   <td> @hardBounces/@sent<br /> </td> 
   <td> Der Denominator für die Berechnung der Rate basiert auf der Anzahl der gesendeten Nachrichten (Zugestellt + Bounces).<br /> </td> 
  </tr> 
  <tr> 
   <td> Ungültige Domain<br /> </td> 
   <td> @invalidDomain<br /> </td> 
   <td> count(@failureReason=2)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Postfach voll<br /> </td> 
   <td> @mailBoxFull<br /> </td> 
   <td> count(@failureReason=5)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Mirrorseite<br /> </td> 
   <td> @mirrorPage<br /> </td> 
   <td> count(@trackingUrlType=6)<br /> </td> 
   <td> Der Denominator für die Berechnung der Rate basiert nur auf der Anzahl der zugestellten Nachrichten.<br /> </td> 
  </tr> 
  <tr> 
   <td> Mirrorseitenrate<br /> </td> 
   <td> @rateMirrorPage<br /> </td> 
   <td> @mirrorPage/@delivered<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Nicht angemeldet<br /> </td> 
   <td> @notConnected<br /> </td> 
   <td> count(@failureReason=6)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Öffnungen<br /> </td> 
   <td> @uniqueOpens<br /> </td> 
   <td> count(@trackingUrlType=2 + unique(@trackingUrlType=1,2,3,6,10,11) - unique(@trackingUrlType=2))<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Öffnungsrate<br /> </td> 
   <td> @rateOpens<br /> </td> 
   <td> @opens/@delivered<br /> </td> 
   <td> Der Denominator für die Berechnung der Rate basiert nur auf der Anzahl der zugestellten Nachrichten.<br /> </td> 
  </tr> 
  <tr> 
   <td> Quarantäne<br /> </td> 
   <td> @quarantine<br /> </td> 
   <td> isQuarantine=true<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Quarantänerate<br /> </td> 
   <td> @rateQuarantine<br /> </td> 
   <td> @quarantine/@sent<br /> </td> 
   <td> Der Denominator für die Berechnung der Rate basiert auf der Anzahl der gesendeten Nachrichten (Zugestellt + Bounces).<br /> </td> 
  </tr>
  <tr> 
   <td> Zurückgewiesen<br /> </td> 
   <td> @rejected<br /> </td> 
   <td> count(@failureReason=20, @failureType=2)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Zurückweisungsrate<br /> </td> 
   <td> @rateRejected<br /> </td> 
   <td> @rejected/@sent<br /> </td> 
   <td> Der Denominator für die Berechnung der Rate basiert auf der Anzahl der gesendeten Nachrichten (Zugestellt + Bounces).<br /> </td> 
  </tr> 
  <tr> 
   <td> Verarbeitet/gesendet<br /> </td> 
   <td> @sent<br /> </td> 
   <td> @delivered + @bounces<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Softbounces<br /> </td> 
   <td> @softBounces<br /> </td> 
   <td> count(@failureType=1)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Softbounce-Rate<br /> </td> 
   <td> @rateSoftBounces<br /> </td> 
   <td> @softBounces/@sent<br /> </td> 
   <td> Der Denominator für die Berechnung der Rate basiert auf der Anzahl der gesendeten Nachrichten (Zugestellt + Bounces).<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelklicks<br /> </td> 
   <td> @uniqueclicks<br /> </td> 
   <td> Einzelklicks werden anhand von ThetaSketch-Konzepten berechnet. Weiterführende Informationen hierzu finden Sie in diesem <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard/using/reporting/about-reporting/troubleshooting.html#unique-open-clicks-no-match">Beispiel</a>.<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Einzelöffnungen<br /> </td> 
   <td> @uniqueopens<br /> </td> 
   <td> unique(@trackingUrlType=1,2,3,6,10,11)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Unerreichbar <br /> </td> 
   <td> @unreachable<br /> </td> 
   <td> count(@failureReason=3)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Abgemeldet<br /> </td> 
   <td> @unsubscribes<br /> </td> 
   <td> count(@trackingUrlType=3)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Abmelderate<br /> </td> 
   <td> @rateUnsubscribes<br /> </td> 
   <td> @unsubscribes/@delivered<br /> </td> 
   <td> Der Denominator für die Berechnung der Rate basiert nur auf der Anzahl der zugestellten Nachrichten.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unbekannter Nutzer<br /> </td> 
   <td> @unknownUser<br /> </td> 
   <td> count(@failureReason=1)<br /> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

## Push-Benachrichtigungsversand        {#push-notification-delivery}

<table> 
 <thead> 
  <tr> 
   <th> <strong>Titel</strong> <br /> </th> 
   <th> <strong>Feldname</strong> <br /> </th> 
   <th> <strong>Formel zur Indikatorberechnung</strong> <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Verarbeitet/gesendet<br /> </td> 
   <td> @sent<br /> </td> 
   <td> @count(status=sent)<br /> </td> 
  </tr> 
  <tr> 
   <td> Zugestellt<br /> </td> 
   <td> @delivered<br /> </td> 
   <td> @count(status=delivered)<br /> </td> 
  </tr> 
  <tr> 
   <td> Zustellrate<br /> </td> 
   <td> @rateDelivered<br /> </td> 
   <td> (@delivered/@sent)*100<br /> </td> 
  </tr> 
  <tr> 
   <td> Bounce- + Fehlerrate<br /> </td> 
   <td> @rateBounces<br /> </td> 
   <td> (@delivered/@sent)*100<br /> </td> 
  </tr> 
  <tr> 
   <td> Öffnungen<br /> </td> 
   <td> @opens<br /> </td> 
   <td> @count(status=open)<br /> </td> 
  </tr> 
  <tr> 
   <td> Öffnungsrate<br /> </td> 
   <td> @rateOpens<br /> </td> 
   <td> (@opens/@delivered)*100<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelöffnungen<br /> </td> 
   <td> @uniqueopens<br /> </td> 
   <td> Einzelöffnungen werden anhand von ThetaSketch-Konzepten von einzelnen Empfänger-IDs berechnet. Weiterführende Informationen hierzu finden Sie in diesem <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard/using/reporting/about-reporting/troubleshooting.html#unique-open-clicks-no-match">Beispiel</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Impressionen<br /> </td> 
   <td> @impressions<br /> </td> 
   <td> @count(status=delivered)<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelimpressionen<br /> </td> 
   <td> @uniqueimpressions<br /> </td> 
   <td> @unique(@count(status=view))<br /> </td> 
  </tr> 
  <tr> 
   <td> Klicks<br /> </td> 
   <td> @clicks<br /> </td> 
   <td> @count(status=interact)<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelklicks<br /> </td> 
   <td> @uniqueclicks<br /> </td> 
   <td> Einzelklicks werden anhand von ThetaSketch-Konzepten berechnet. Weiterführende Informationen hierzu finden Sie in diesem <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard/using/reporting/about-reporting/troubleshooting.html#unique-open-clicks-no-match">Beispiel</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Durchklickrate<br /> </td> 
   <td> @clickthrough<br /> </td> 
   <td> (@interact/@delivered)*100<br /> </td> 
  </tr> 
 </tbody> 
</table>

## In-App-Versand        {#in-app-delivery}

<table> 
 <thead> 
  <tr> 
   <th> <strong>Titel</strong> <br /> </th> 
   <th> <strong>Feldname</strong> <br /> </th> 
   <th> <strong>Formel zur Indikatorberechnung</strong> <br /> </th> 
   <th> <strong>Erklärung</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Verarbeitet/gesendet<br /> </td> 
   <td> @sent<br /> </td> 
   <td> @count(status=sent)<br /> </td> 
   <td> sent=delivered<br /> </td> 
  </tr> 
  <tr> 
   <td> Zugestellt<br /> </td> 
   <td> @delivered<br /> </td> 
   <td> @count(status=delivered)<br /> </td> 
   <td> delivered=sent<br /> </td> 
  </tr> 
  <tr> 
   <td> Impressionen<br /> </td> 
   <td> @impressions<br /> </td> 
   <td> @count(status=view) oder @count(status=button 1 click + button 2 click + dismissals)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Einzelimpressionen<br /> </td> 
   <td> @uniqueimpressions<br /> </td> 
   <td> @unique(@count(status=view))<br /> </td> 
   <td> Für die Vorlage <span class="uicontrol">Nutzer auf Basis ihres Campaign-Profils in die Zielgruppe aufnehmen (inAppProfile)</span> ist Benutzer = Empfänger-ID.<br />Für die Vorlagen <span class="uicontrol">Alle Nutzer einer Mobile App in die Zielgruppe aufnehmen (inAppBroadcast)</span> und <span class="uicontrol">Nutzer auf Basis ihres Mobile-Profils in die Zielgruppe aufnehmen (inApp)</span> ist Benutzer = MC-ID oder eine andere Kennung, die eine eindeutige Kombination aus Benutzer, Mobile App und Gerät darstellt.<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App-Klicks <br /> </td> 
   <td> @inappclicks<br /> </td> 
   <td> @count (status=click)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Einzelne In-App-Klicks<br /> </td> 
   <td> @uniqueinapp<br /> </td> 
   <td> @unique(@count (status=clicks))<br /> </td> 
   <td> Für die Vorlage <span class="uicontrol">Nutzer auf Basis ihres Campaign-Profils in die Zielgruppe aufnehmen (inAppProfile)</span> ist Benutzer = Empfänger-ID.<br />Für die Vorlagen <span class="uicontrol">Alle Nutzer einer Mobile App in die Zielgruppe aufnehmen (inAppBroadcast)</span> und <span class="uicontrol">Nutzer auf Basis ihres Mobile-Profils in die Zielgruppe aufnehmen (inApp)</span> ist Benutzer = MC-ID oder eine andere Kennung, die eine eindeutige Kombination aus Benutzer, Mobile App und Gerät darstellt.<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App-Klickrate<br /> </td> 
   <td> @inappclickthrough<br /> </td> 
   <td> Gesamtklicks auf Schaltfläche 1 oder Schaltfläche 2/Gesamtzahl der Impressionen * 100<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> In-App-Abweisung<br /> </td> 
   <td> @dismissal<br /> </td> 
   <td> @count (status=close)<br /> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> Einzelne In-App-Abweisungen<br /> </td> 
   <td> @uniquedismissal<br /> </td> 
   <td> @unique(@count (status=close))<br /> </td> 
   <td> Für die Vorlage <span class="uicontrol">Nutzer auf Basis ihres Campaign-Profils in die Zielgruppe aufnehmen (inAppProfile)</span> ist Benutzer = Empfänger-ID.<br />Für die Vorlagen <span class="uicontrol">Alle Nutzer einer Mobile App in die Zielgruppe aufnehmen (inAppBroadcast)</span> und <span class="uicontrol">Nutzer auf Basis ihres Mobile-Profils in die Zielgruppe aufnehmen (inApp)</span> ist Benutzer = MC-ID oder eine andere Kennung, die eine eindeutige Kombination aus Benutzer, Mobile App und Gerät darstellt.<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App-Abweisungsrate<br /> </td> 
   <td> @dismissalrate<br /> </td> 
   <td> Gesamtzahl der Schließungen/Gesamtimpressionen * 100<br /> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>


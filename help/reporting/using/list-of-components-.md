---
title: Liste von Komponenten
description: Hier finden Sie die Liste der in dynamischen Berichten enthaltenen Komponenten sowie ihre Definitionen.
audience: reporting
content-type: reference
topic-tags: about-reporting
feature: Reporting
role: Leader
level: Beginner
exl-id: 8980bf05-60a8-4360-a354-445e1faeb5b2
source-git-commit: 6530ca1726a2aff18c5be9566d8008c317918e64
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 100%

---

# Liste von Komponenten {#list-of-components}

Weiterführende Informationen zur Kompatibilität zwischen Dimensionen und Metriken finden Sie in dieser [Tabelle](/help/reporting/using/assets/dynamic_report_compatibility.pdf). Wenn zwei Komponenten nicht kompatibel sind, zeigt die Zelle den Wert **Kein** an.

[![Bild](assets/dynamic_report_compatibility.png)](https://experienceleague.adobe.com/docs/campaign-standard/assets/dynamic_report_compatibility.pdf)

## Dimensionen {#dimensions}

In der Tabelle unten finden Sie die Liste der Dimensionen, die in Berichten verwendet werden, sowie ihre Definitionen.

<table> 
 <thead> 
  <tr> 
   <th> Dimension<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Browser<br /> </td> 
   <td> Browser, in dem die Nachricht geöffnet oder angeklickt wurde<br /> </td> 
  </tr> 
  <tr> 
   <td> Kampagne<br /> </td> 
   <td> Titel und Kennung Ihrer Kampagne<br /> </td> 
  </tr> 
  <tr> 
   <td> Ort<br /> </td> 
   <td> Der im Empfängerprofil gespeicherte Ort<br /> </td> 
  </tr> 
  <tr> 
   <td> Land/Region<br /> </td> 
   <td> Das im Empfängerprofil gespeicherte Land<br /> </td> 
  </tr> 
  <tr> 
   <td> Versand<br /> </td> 
   <td> Titel und Kennung des Versands<br /> </td> 
  </tr> 
  <tr> 
   <td> Gerät<br /> </td> 
   <td> Gerät, auf dem die E-Mail/SMS/Push-Benachrichtigung geöffnet/angesehen/angeklickt wurde.<br /> </td> 
  </tr> 
  <tr> 
   <td> Grund des Fehlschlagens<br /> </td> 
   <td> Fehlertypen, die bei jedem Versand zu Bounces führten, z. B. unbekannte Nutzer, ungültige Domain oder Postfach voll.<br /> </td> 
  </tr> 
  <tr> 
   <td> Geschlecht<br /> </td> 
   <td> Geschlecht der Empfänger, also männlich oder weiblich. Wenn dieses Feld im Empfängerprofil leer ist, ist der Wert unbestimmt.<br /> </td> 
  </tr> 
  <tr> 
   <td> Aktionen bei In-App-Nachrichten<br /> </td> 
   <td> Aktionen bei gesendeten In-App-Nachrichten, z. B. Aktionen auf Schaltfläche 1 oder 2 oder Verwerfungen.<br /> </td> 
  </tr> 
  <tr> 
   <td> Nachrichtentyp<br /> </td> 
   <td> Der für den Versand verwendete Kanal, beispielsweise E-Mail, SMS, Push-Benachrichtigung oder In-App-Nachricht<br /> </td> 
  </tr> 
  <tr> 
   <td> Name der Mobile App<br /> </td> 
   <td> Name der Mobile App<br /> </td> 
  </tr> 
  <tr> 
   <td> Plattform<br /> </td> 
   <td> Plattform des Geräts, auf dem die Nachricht geöffnet/angesehen/angeklickt wurde<br /> </td> 
  </tr> 
  <tr> 
   <td> Profil<br /> </td> 
   <td> Fasst native und benutzerdefinierte Profilfelder zusammen, die während der Erweiterung der Profilressource erstellt wurden. Weiterführende Informationen dazu finden Sie auf dieser <a href="../../developing/using/key-steps-to-add-a-resource.md">Seite</a> und in diesem <a href="../../reporting/using/creating-a-custom-profile-dimension.md">Beispiel</a>.<br /> Beachten Sie, dass Daten für diese Dimension abgerufen werden, sobald die mit dem Profilfeld verknüpfte benutzerdefinierte Ressource veröffentlicht wird.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push-Plattform<br /> </td> 
   <td> Plattform des Geräts, auf dem die Push-Benachrichtigung geöffnet wurde, wie iOS oder Android<br /> </td> 
  </tr> 
  <tr> 
   <td> Empfänger-Domain<br /> </td> 
   <td> Die zum Öffnen der E-Mail verwendete Domain<br /> </td> 
  </tr> 
  <tr> 
   <td> Wiederkehrender Versand<br /> </td> 
   <td> Titel und Kennung des wiederkehrenden Versands<br /> </td> 
  </tr> 
  <tr> 
   <td> Absender-Domain<br /> </td> 
   <td> Die zum Senden der E-Mail verwendete Domain<br /> </td> 
  </tr> 
  <tr> 
   <td> Absender-IP<br /> </td> 
   <td> Die zum Senden der E-Mail verwendete IP<br /> </td> 
  </tr> 
  <tr> 
   <td> Bundesland/Kanton<br /> </td> 
   <td> Das im Empfängerprofil gespeicherte Bundesland<br /> </td> 
  </tr> 
  <tr> 
   <td> Tracking-URL<br /> </td> 
   <td> URL, die der Benutzer in der Nachricht angeklickt hat<br /> </td> 
  </tr> 
  <tr> 
   <td> Kategorie des URL-Trackings<br /> </td> 
   <td> Die der Tracking-URL zugewiesene Kategorie<br /> </td> 
  </tr> 
  <tr> 
   <td> Titel des URL-Trackings<br /> </td> 
   <td> Der an die URL vergebene Titel, wie "Mirrorseite", "Kontakt" oder "Öffnung".<br /> </td> 
  </tr> 
  <tr> 
   <td> Versand von Transaktionsnachrichten<br /> </td> 
   <td> Titel und Kennung des Transaktionsnachrichtenversands<br /> </td> 
  </tr> 
  <tr> 
   <td> Variante<br /> </td> 
   <td> Variante der E-Mail im Fall von A/B-Tests<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Metriken             {#metrics}

In den Tabellen unten finden Sie nach Versandtyp geordnet die Liste der Metriken, die in Berichten verwendet werden, sowie ihre Definitionen.

### Metriken zu E-Mail und SMS             {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrik<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Auf Blockierungsliste<br /> </td> 
   <td> Anzahl der Empfänger, die eine E-Mail als Spam oder Junk gekennzeichnet haben<br /> </td> 
  </tr> 
  <tr> 
   <td> Blockierungslistenrate<br /> </td> 
   <td> Prozentsatz der Sendungen, die auf einer Blockierungsliste markiert sind.<br /> </td> 
  </tr> 
  <tr> 
   <td> Bounces + Fehler<br /> </td> 
   <td> Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler und der automatischen Bounce-Verarbeitung in Bezug auf die Gesamtzahl der gesendeten Nachrichten<br /> </td> 
  </tr> 
  <tr> 
   <td> Bounce- + Fehlerrate<br /> </td> 
   <td> Prozentsatz der Bounce-E-Mails in Bezug auf die gesendeten E-Mails<br /> </td> 
  </tr> 
  <tr> 
   <td> Klicks<br /> </td> 
   <td> Die Anzahl der Klicks auf einen Inhalt in einem Versand.<br /> </td> 
  </tr> 
  <tr> 
   <td> Durchklickrate<br /> </td> 
   <td> Prozentsatz der Klicks in einem Versand<br /> </td> 
  </tr> 
  <tr> 
   <td> Zugestellt<br /> </td> 
   <td> Anzahl der erfolgreich gesendeten Nachrichten in Bezug auf die Gesamtzahl der gesendeten Nachrichten<br /> </td> 
  </tr> 
  <tr> 
   <td> Zustellrate<br /> </td> 
   <td> Prozentsatz der erfolgreich gesendeten Nachrichten<br /> </td> 
  </tr> 
  <tr> 
   <td> Hardbounce<br /> </td> 
   <td> Gesamtzahl der permanenten Fehler, beispielsweise einer falschen E-Mail-Adresse<br /> </td> 
  </tr> 
  <tr> 
   <td> Hardbounce-Rate<br /> </td> 
   <td> Prozentsatz der Sendungen, die permanent fehlgeschlagen sind<br /> </td> 
  </tr> 
  <tr> 
   <td> Mirrorseite<br /> </td> 
   <td> Die Anzahl der Empfänger, die den Mirrorseiten-Link angeklickt haben<br /> </td> 
  </tr> 
  <tr> 
   <td> Mirrorseitenrate<br /> </td> 
   <td> Prozentsatz der Klicks auf den Mirrorseiten-Link in Bezug auf die Gesamtzahl der Sendungen<br /> </td> 
  </tr> 
  <tr> 
   <td> Klicks auf Angebot<br /> </td> 
   <td> Die Anzahl der Klicks auf ein Angebot in einem Versand.<br /> </td> 
  </tr> 
  <tr> 
   <td> Klickrate des Angebots<br /> </td> 
   <td> Prozentsatz der Klicks auf ein Angebot.<br /> </td> 
  </tr> 
  <tr> 
   <td> Öffnungen<br /> </td> 
   <td> Anzahl der Öffnungen einer Nachricht in einem Versand.<br /> </td> 
  </tr> 
  <tr> 
   <td> Öffnungsrate<br /> </td> 
   <td> Prozentsatz der geöffneten Nachrichten<br /> </td> 
  </tr> 
  <tr> 
   <td> Verarbeitet/gesendet<br /> </td> 
   <td> Gesamtzahl der gesendeten Nachrichten<br /> </td> 
  </tr> 
  <tr> 
   <td> Quarantäne<br /> </td> 
   <td> Anzahl der Bounce-Nachrichten, aufgrund derer eine Adresse unter Quarantäne gestellt wurde<br /> </td> 
  </tr> 
  <tr> 
   <td> Quarantänerate<br /> </td> 
   <td> Prozentsatz der Quarantänen in Bezug auf die gesendeten Nachrichten<br /> </td> 
  </tr> 
  <tr> 
   <td> Zurückgewiesen<br /> </td> 
   <td> Anzahl der Sendungen, die von SMTP-Servern als Spam gekennzeichnet wurden<br /> </td> 
  </tr> 
  <tr> 
   <td> Zurückweisungsrate<br /> </td> 
   <td> Prozentsatz der Nachrichten, die als abgelehnt gekennzeichnet wurden<br /> </td> 
  </tr> 
  <tr> 
   <td> Softbounce<br /> </td> 
   <td> Gesamtzahl der temporären Fehler, beispielsweise einer vollen Inbox<br /> </td> 
  </tr> 
  <tr> 
   <td> Softbounce-Rate<br /> </td> 
   <td> Prozentsatz der Sendungen, die vorläufig fehlgeschlagen sind<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelklicks<br /> </td> 
   <td> Anzahl der Empfänger, die einen Inhalt in einem Versand angeklickt haben<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelöffnungen<br /> </td> 
   <td> Anzahl der Empfänger, die den Versand geöffnet haben<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelabmeldungen<br /> </td> 
   <td> Die Anzahl der Empfänger, die den Abmelde-Link angeklickt haben.<br /> </td> 
  </tr> 
  <tr> 
   <td> Abmelderate<br /> </td> 
   <td> Anzahl der Einzelabmeldungen im Vergleich zu den zugestellten Nachrichten.<br /> </td> 
  </tr> 
  <tr> 
   <td> Abgemeldet<br /> </td> 
   <td> Gesamtanzahl der Klicks auf den Abmelde-Link.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Metriken zu Push-Benachrichtigungen             {#push-notification-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrik<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Bounces + Fehler<br /> </td> 
   <td> Gesamtzahl der über alle Sendungen hinweg kumulierten Fehler im Vergleich zur Gesamtzahl aller gesendeten Nachrichten, z. B. Fehler durch MCPNS oder Provider.<br /> </td> 
  </tr> 
  <tr> 
   <td> Bounce- + Fehlerrate<br /> </td> 
   <td> Prozentsatz der Bounce-Push-Benachrichtigungen in Bezug auf die gesendeten Push-Benachrichtigungen.<br /> </td> 
  </tr> 
  <tr> 
   <td> Klicks<br /> </td> 
   <td> Gibt an, wie oft eine Push-Benachrichtigung an das Gerät geschickt und vom Benutzer angeklickt wurde. Der Benutzer hat die Benachrichtigung entweder angesehen oder verworfen. Wenn er sie angesehen hat, wird sie beim Push-Öffnungstracking berücksichtigt.<br /> </td> 
  </tr> 
  <tr> 
   <td> Durchklickrate<br /> </td> 
   <td> Prozentsatz der Benutzer, die mit der Push-Benachrichtigung interagiert haben.<br /> </td> 
  </tr> 
  <tr> 
   <td> Zugestellt<br /> </td> 
   <td> Anzahl der erfolgreich gesendeten Push-Benachrichtigungen in Bezug auf die Gesamtzahl der gesendeten Push-Benachrichtigungen.<br /> </td> 
  </tr> 
  <tr> 
   <td> Zustellrate<br /> </td> 
   <td> Anzahl der erfolgreich gesendeten Push-Benachrichtigungen.<br /> </td> 
  </tr> 
  <tr> 
   <td> Impressionen<br /> </td> 
   <td> Gibt an, wie oft eine Push-Benachrichtigung an das Gerät gesendet und in der Benachrichtigungszentrale unverändert gelassen wurde. In den meisten Fällen sollte die Anzahl der Impressionen in etwa der Anzahl der Sendungen entsprechen. Dadurch wird sichergestellt, dass das Gerät die Nachricht erhalten und diese Informationen an den Server zurückgegeben hat.<br /> </td> 
  </tr> 
  <tr> 
   <td> Verarbeitet/gesendet<br /> </td> 
   <td> Gesamtzahl der gesendeten Push-Benachrichtigungen.<br /> </td> 
  </tr> 
  <tr> 
   <td> Öffnungen<br /> </td> 
   <td> Gesamtzahl der Push-Benachrichtigungen, die an das Gerät gesendet und vom Benutzer angeklickt wurden, sodass die App geöffnet wurde. Dies ist ähnlich der Klick-Kategorie mit dem Unterschied, dass keine Push-Öffnung ausgelöst wird, wenn die Benachrichtigung verworfen wird.<br /> </td> 
  </tr> 
  <tr> 
   <td> Öffnungsrate<br /> </td> 
   <td> Prozentsatz der geöffneten Push-Benachrichtigungen.<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelklicks<br /> </td> 
   <td> Anzahl der Interaktionen eindeutiger Benutzer mit der Push-Benachrichtigung, z. B. Klicks auf die Benachrichtigung oder die Schaltfläche.<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelimpressionen<br /> </td> 
   <td> Anzahl der Impressionen durch einen Empfänger.<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelöffnungen<br /> </td> 
   <td> Anzahl der Empfänger, die den Versand geöffnet haben<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Metriken zu In-App-Nachrichten             {#in-app-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrik<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Zugestellt<br /> </td> 
   <td> Gesamtzahl der In-App-Nachrichten, die vom Service Provider an das Gerät gesendet wurden.<br /> </td> 
  </tr> 
  <tr> 
   <td> Impressionen<br /> </td> 
   <td> Gesamtzahl der In-App-Nachrichten, die von den Empfängern gesehen wurden abhängig davon, ob die Trigger-Bedingung erfüllt worden ist.<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App-Klicks <br /> </td> 
   <td> Gesamtzahl der Empfänger, die auf Schaltfläche 1 oder Schaltfläche 2 geklickt haben.<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App-Klickrate<br /> </td> 
   <td> Prozentsatz der Benutzer, die auf Schaltfläche 1 oder Schaltfläche 2 geklickt haben, verglichen mit den Benutzern, die die Nachricht gesehen haben.<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App-Abweisung<br /> </td> 
   <td> Gesamtzahl der Nachrichten, die von Benutzern verworfen wurden, indem diese entweder die Schließen-Schaltfläche oder die automatische Funktion zum Entfernen der Nachricht verwendet haben.<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App-Abweisungsrate<br /> </td> 
   <td> Prozentsatz der In-App-Nachrichten, die von Empfängern verworfen wurden.<br /> </td> 
  </tr> 
  <tr> 
   <td> Verarbeitet/gesendet<br /> </td> 
   <td> Gesamtzahl der In-App-Nachrichten, die von Adobe Campaign als Teil des Versandvorgangs gesendet wurden.<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelimpressionen<br /> </td> 
   <td> Anzahl der Impressionen durch einen einzelnen Empfänger<br /> </td> 
  </tr> 
  <tr> 
   <td> In-App-Einzelklicks<br /> </td> 
   <td> Anzahl der Klicks auf Schaltfläche 1 oder Schaltfläche 2 durch Empfänger.<br /> </td> 
  </tr> 
  <tr> 
   <td> Einzelne In-App-Abweisungen<br /> </td> 
   <td> Anzahl der verworfenen In-App-Nachrichten durch Empfänger.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Segmente {#segments}

In der Tabelle unten finden Sie die Liste der Segmente, die in Berichten verwendet werden, sowie ihre Definitionen.

<table> 
 <thead> 
  <tr> 
   <th> Segment<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Alter: Boomers 1<br /> </td> 
   <td> Empfänger mit Geburtsjahr 1946 bis 1954<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: Boomers 2<br /> </td> 
   <td> Empfänger mit Geburtsjahr 1955 bis 1965<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: von 18 bis 25<br /> </td> 
   <td> Empfänger im Alter von 18 bis 25 Jahren<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: von 26 bis 30<br /> </td> 
   <td> Empfänger im Alter von 26 bis 30 Jahren<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: von 31 bis 40<br /> </td> 
   <td> Empfänger im Alter von 31 bis 40 Jahren<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: von 41 bis 50<br /> </td> 
   <td> Empfänger im Alter von 41 bis 50 Jahren<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: Generation X<br /> </td> 
   <td> Empfänger mit Geburtsjahr 1966 bis 1976<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: Generation Y (Millennials)<br /> </td> 
   <td> Empfänger mit Geburtsjahr 1977 bis 1994<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: Generation Z<br /> </td> 
   <td> Empfänger mit Geburtsjahrgang 1995 bis heute<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: über 50<br /> </td> 
   <td> Empfänger im Alter von über 50 Jahren<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: unter 25<br /> </td> 
   <td> Empfänger im Alter von unter 25 Jahren<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: unter 30<br /> </td> 
   <td> Empfänger im Alter von unter 30 Jahren<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: unter 40<br /> </td> 
   <td> Empfänger im Alter von unter 40 Jahren<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: unter 50<br /> </td> 
   <td> Empfänger im Alter von unter 50 Jahren<br /> </td> 
  </tr> 
  <tr> 
   <td> Alter: Stille Generation<br /> </td> 
   <td> Empfänger mit Geburtsjahr 1945 oder früher<br /> </td> 
  </tr> 
  <tr> 
   <td> Alle Besuche<br /> </td> 
   <td> Jeder Empfänger<br /> </td> 
  </tr>
 </tbody> 
</table>

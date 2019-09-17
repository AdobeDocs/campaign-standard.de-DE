---
title: Versionshinweise 2015–2016
seo-title: Versionshinweise 2015–2016
description: Versionshinweise 2015–2016
seo-description: Auf dieser Seite werden alle Versionen von Adobe Campaign Standard von 2015 und 2016 aufgelistet.
page-status-flag: never-activated
uuid: d5a0f6cc-0bed-46cf-8dff-1717fb624f8f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: a3ce6b80-1858-49d1-8880-3543181127f4
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ea825afe573959d95d0f7f3f6e79dd38ac5a678a

---


# Versionshinweise 2015–2016{#release-notes}

Suchen Sie eine bestimmte Version von Adobe Campaign Standard aus dem Jahr 2015 oder 2016?

Mit jeder Version werden neue Funktionen und Korrekturen veröffentlicht. Klicken Sie auf eine Version, um sich den Inhalt anzusehen.

Sehen Sie sich [Dokumentationsaktualisierungen](../../rn/using/documentation-updates.md) für Adobe Campaign Standard an. Neuere Versionshinweise finden Sie auf dieser [Seite](../../rn/using/release-notes.md).

## 16.11 - Version November 2016  {#release-16-11---november-2016}

### Neue Funktionen {#new-capabilities}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Ausschlussregeln für Zustellbarkeit<br /> </td> 
   <td> In der Zustellbarkeitsinstanz wird nun eine verschlüsselte globale Unterdrückungsliste verwaltet, um Blacklisting aufgrund von schädlichen Aktivitäten zu vermeiden. Dies betrifft insbesondere die Verwendung von Spamtraps.<br /> Bei jedem E-Mail-Versand vergleichen zwei Typologieregeln die E-Mail-Adresse des Empfängers mit den unzulässigen Adressen oder Domain-Namen aus der Liste. Wenn eine Übereinstimmung festgestellt wird, wird der Empfänger aus der Zielpopulation ausgeschlossen.<br /> Lesen Sie für weiterführende Informationen das <a href="../../administration/using/filtering-rules.md#default-deliverability-exclusion-rules">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Allgemeine Optimierung<br /> </td> 
   <td> Dieses Update umfasst zahlreiche Änderungen und Korrekturen zur Behebung von Problemen, die bei unseren Kunden aufgetreten sind. Auch die allgemeine Leistung der Plattform wurde verbessert. <br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches}

#### Allgemein {#general}

* Fehlerkorrektur – diverse Sicherheitsprobleme wurden behoben.
* Verschiedene Probleme im Zusammenhang mit leeren oder doppelten Feldern in der REST-API wurden behoben.
* SMS-Nachrichten und Push-Benachrichtigungen können nun direkt über die Startseite der Anwendung erstellt werden.

#### E-Mails und SMS-Nachrichten  {#emails-and-sms-messages}

* Fehlerkorrektur – ZIP-Dateien können nun im Inhaltseditor hochgeladen werden.
* Fehlerkorrektur – ein bereits gesendeter Testversand kann nun geöffnet werden.
* Fehlerkorrektur – der Zugriff auf den Bericht **[!UICONTROL Klicks]** für eine A/B-Test-E-Mail erzeugt nun keine Fehlermeldung mehr.
* Fehlerkorrektur – Änderungen, die im Modus **[!UICONTROL Quelle anzeigen]** vorgenommen wurden, können nun angewendet werden.
* Fehlerkorrektur – XML-Modelldateien für die prädiktive Betreffzeile lassen sich nun importieren.
* Unter **[!UICONTROL Administration &gt; Kanäle &gt; E-Mails &gt; Prädiktive Betreffzeile]** steht nun ein neuer Bildschirm zum Importieren von Daten für das trainierte Betreffzeilenmodell zur Verfügung.
* Fehlerkorrektur – Benutzer ohne Administratorberechtigungen können nun die zulässigen Masken im E-Mail-Konfigurationsbildschirm nicht mehr bearbeiten.

#### Push-Benachrichtigungen {#push-notifications}

* Fehlerkorrektur – nach Versand von Push-Benachrichtigungen unter Verwendung der Vorlage **[!UICONTROL Push-Benachrichtigung für Profile senden]** werden nun die Versand- und Ereignislogs der Empfänger angezeigt.
* Fehlerkorrektur – kein Problem bei der Erstellung neure Mobile-Apps mehr.

#### Workflows  {#workflows}

* Fehlerkorrektur – bei Verwendung der **[!UICONTROL Abonnement]**-Aktivität tritt nun kein Leistungsproblem mehr auf.
* Fehlerkorrektur – Workflows, deren interner Name ein Leerzeichen enthält, arbeiten nun problemlos.

#### Integrationen  {#integrations}

* Fehlerkorrektur – bei Verwendung der Option **Freigegebenes Bild der Adobe Marketing Cloud** in E-Mails wird kein Fehler mehr ausgelöst.

#### Benutzerdefinierte Ressourcen {#custom-resources}

* Die API-Protokollvorschau zwischen zwei Publikationen von erweiterten API-Feldern wurde verbessert.
* Fehlerkorrektur – eine benutzerdefinierte Ressource kann nun vor der Veröffentlichung gelöscht werden.
* Fehlerkorrektur – kein Fehler mehr bei der Profilerweiterung und der Definition von Kennungsschlüsseln mit dynamischen Feldern.
* Fehlerkorrektur – das Hinzufügen von Links zu einer benutzerdefinierten Ressource löst keine Probleme mehr aus.

## 16.10 - Version Oktober 2016  {#release-16-10---october-2016}

### Neue Funktionen {#new-capabilities-1}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Prädiktive E-Mail-Betreffzeile<br /> </td> 
   <td> Beim Bearbeiten von E-Mails bietet Ihnen eine neue Option die Möglichkeit, verschiedene Betreffzeilen auszuprobieren und dabei eine jeweilige Einschätzung der Öffnungsrate zu erhalten, bevor Sie die E-Mail senden. Dies wird durch das Training Ihres eigenen lernfähigen Modells, das sich an Ihren bisherigen Versanddaten orientiert, oder durch die Verwendung eines speziell auf Ihre Branche abgestimmten, vordefinierten Modells ermöglicht. Diese Funktion ist ausschließlich für E-Mail-Nachrichten und Datenbanken mit englischen Inhalten verfügbar. <br /> Weiterführende Informationen zur Aktivierung und Verwendung dieser Funktion finden Sie im <a href="../../designing/using/subject-line.md#predictive-subject-line">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transaktionsnachrichtenversand per SMS<br /> </td> 
   <td> Adobe Campaigns Transaktionsnachrichtenversandkapazitäten wurden um den SMS-Kanal erweitert. Von nun an werden zwei Kanäle für Transaktionsnachrichten unterstützt: E-Mail und SMS.<br /> Lesen Sie für weiterführende Informationen das <a href="../../administration/using/configuring-transactional-messaging.md#creating-an-event">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Folgenachrichten für den Transaktionsnachrichtenversand<br /> </td> 
   <td> Es können nun Workflows erstellt werden, die auf ein Ereignis abzielen. Das bedeutet, dass Sie Folgenachrichten an Kunden senden können, die zuvor eine Transaktionsnachricht erhalten haben. Sie können die Zielgruppe nach Ereignistyp, Ereignis-Broadlogs und Trackinglogs filtern. In die Folgenachricht können Sie den Ereignisinhalt übernehmen (payload). <br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/follow-up-messages.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Erweiterte Profiles &amp; Services API<br /> </td> 
   <td> In der Profiles &amp; Services API können nun erweiterte Felder angezeigt werden. Der Publikationsmechanismus ermöglicht den API ein Mapping von erweiterten Feldern der benutzerdefinierten Ressourcen Profile oder Dienste. Damit das funktioniert, wurde die Benutzerrolle <strong>DATA MODEL</strong> hinzugefügt. Dank dieser neuen Benutzerrolle können Benutzer eine Reihe von Administratoren konfigurieren, die Zugriff auf das Datenmodell haben.<br /> Lesen Sie für weiterführende Informationen das <a href="../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-1}

#### Allgemein {#general-1}

* Fehlerkorrektur – diverse Sicherheitsprobleme wurden behoben.

#### E-Mails und SMS-Nachrichten {#emails-and-sms-messages-1}

* Der Konfigurationsbildschirm für externe SMS-Konten (**[!UICONTROL Administration &gt; Kanäle &gt; SMS &gt; SMS-Konten]**) wurde verbessert. Im Bereich **[!UICONTROL SMSC-Besonderheiten]** wurden mehrere Parameter hinzugefügt, damit im "Text"-Feld Fehlercodes unterstützt werden.

#### Push-Benachrichtigungen {#push-notifications-1}

* Fehlerkorrektur – die Anzeige von vordefinierten Filtern wird nicht länger behindert, wenn die Audience einer Push-Benachrichtigung mithilfe der Vorlage **[!UICONTROL Push-Benachrichtigungs-Versand]** (mobileApp) bearbeitet wird.
* Im Konfigurationsbildschirm von Mobile Apps (**[!UICONTROL Administration &gt; Kanäle &gt; Push-Benachrichtigung &gt; Mobile Apps]**) wird nun eine Nachricht angezeigt, die darüber informiert, dass die iOS- bzw. Android-Plattform erfolgreich erstellt wurde.

#### Landingpages {#landing-pages}

* Fehlerkorrektur – diverse Probleme wurden behoben, sodass der Versand von Bestätigungs-E-Mails nach der Unterbreitung eines Landingpage-Formulars nicht länger verhindert wird.

#### Audiences und Abfragen  {#audiences-and-queries}

* Fehlerkorrektur – diverse Probleme wurden behoben, sodass Profile nun problemlos im Abfrageeditor ausgewählt werden können.

#### Transaktionsnachrichten {#transactional-messages}

* Fehlerkorrektur – die Depublikation von Transaktionsvorlagen funktioniert nun fehlerfrei.
* Fehlerkorrektur – Trigger-Ereignisse werden nicht länger in der Liste der Ereignisse angezeigt.

#### Integrationen  {#integrations-1}

* Fehlerkorrektur – freigegebene Zielgruppen können nun ungehindert in Sendungen verwendet werden, nachdem sie aktualisiert wurden.
* Fehlerkorrektur – freigegebene Assets (Option **[!UICONTROL Freigegebenes Bild der Adobe Marketing Cloud]**) können nun problemlos in Landingpages verwendet werden.
* Fehlerkorrektur – diverse Probleme wurden behoben, sodass freigegebene Zielgruppen aus Adobe Audience Manager nach dem Import nun ungehindert bearbeitet werden können.

## 16.9 - Version September 2016  {#release-16-9---september-2016}

### Neue Funktionen {#new-capabilities-2}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Remarketing-Trigger<br /> </td> 
   <td> Durch die Integration von Adobe Campaign mit dem Core Service <span class="uicontrol">Triggers</span> können Sie Ihren Kunden personalisierte E-Mails senden, die auf bestimmte Verhaltensweisen abgestimmt sind, die auf Ihrer Webseite mithilfe von Adobe Analytics (innerhalb von 15 Minuten) ermittelt wurden.<br /> In Adobe Marketing Cloud werden die verschiedenen Trigger definiert, also jene Verhaltensweisen von Kunden, die Sie verfolgen möchten. Dabei kann es sich beispielsweise um Kunden handeln, die ihren Warenkorb stehen gelassen, einen Artikel daraus entfernt haben oder deren Sitzung abgelaufen ist. Bei der Erstellung von Triggern bestimmen Sie die Trigger-Bedingung sowie die Daten, die im Falle der Auslösung des Ereignisses an Adobe Campaign gesendet werden (pload). <br /> In Adobe Campaign werden der zuvor erstellte Trigger ausgewählt, die Ereignisdaten mit Datamart-Daten angereichert und eine mit diesem Trigger verknüpfte Transaktionsnachrichtenvorlage definiert. Lässt zum Beispiel ein Kunde seinen Warenkorb stehen, wird ein Ereignis an Adobe Campaign gesendet, das dort zur Erstellung einer Remarketing-E-Mail führt, die innerhalb von 15 Minuten an den Kunden gesendet wird.<br /> Lesen Sie für weiterführende Informationen das <a href="../../integrating/using/about-adobe-experience-cloud-triggers.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transaktionsnachrichten: Aussetzen/Depublizieren<br /> </td> 
   <td> Es besteht nun die Möglichkeit, die Publikation einer Transaktionsvorlage zur Aktualisierung ihres Inhalts auszusetzen. Dabei werden die entsprechenden Nachrichten nicht länger gesendet, sondern in der Datenbank gespeichert. Bei der Wiederaufnahme der Publikation werden die Nachrichten in der Warteschlange verarbeitet und sie werden gesendet, sofern ihre Gültigkeit nicht abgelaufen ist.<br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/event-transactional-messages.md#suspending-a-transactional-message-publication">entsprechende Handbuch</a>.<br /> Außerdem haben Sie fortan die Möglichkeit, Ereignisse und Transaktionsvorlagen zu löschen. Dadurch werden die entsprechenden Nachrichten nicht länger gesendet und nicht in der Datenbank gespeichert.<br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/event-transactional-messages.md#unpublishing-a-transactional-message">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Markenvielfalt (Multibranding)<br /> </td> 
   <td> Kunden mit mehreren Marken können diese künftig in ein und derselben Instanz verwalten. Die Erstellung bzw. Konfiguration von Marken ist eine dem Administrator Ihrer Adobe Campaign-Instanz vorbehaltene Funktion, mithilfe derer Sie zentral alle eine Marke betreffenden Parameter innerhalb von Adobe Campaign konfigurieren können. Sie umfasst Elemente, die vom Logo bis zu technischeren Parametern wie Tracking-URLs, Web Analytics, Server-URL, Domain-Name etc. reichen.<br /> Lesen Sie für weiterführende Informationen das <a href="../../administration/using/branding.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Responsive Email Design als Vorschau<br /> </td> 
   <td> Mithilfe dieser Funktion lässt sich testen, wie Ihre E-Mail auf verschiedenen Geräten angezeigt wird. Hierzu wurde innerhalb der E-Mail-Vorschau ein Raster hinzugefügt, das die Darstellung der E-Mail auf verschiedenen Bildschirmgrößen simuliert.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push-Benachrichtigungen<br /> </td> 
   <td> Es wurde ein neuer Kanal hinzugefügt, der es Marketern ermöglicht, personalisierte und zielgruppenspezifische Push-Benachrichtigungen an iOS- und Android-Mobilgeräte zu versenden. Nachrichten können entweder im Rahmen eines Einzelversands oder einer Workflow-Aktivität gesendet werden. Die Kompatibilität mit der Transaktionsnachrichten-Funktion wird in zukünftigen Versionen gegeben sein. Dieser Kanal bedient sich des Mobile-Core-Service-SDKs (<a href="https://marketing.adobe.com/developer/gallery/marketing-cloud-mobile-libraries">hier</a> verfügbar).<br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/about-push-notifications.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-2}

#### Allgemein {#general-2}

* Mit dieser Version werden in der Benutzeroberfläche neue Filter- und Suchoptionen in Listen verfügbar. Diese neue Funktion ist beispielsweise in Logs (Versand, Tracking), Diensten (Abonnement, Abonnementverlauf), Audiences und Workflow-Transitionen verfügbar.
* Fehlerkorrektur – diverse auf die Touchpoints-Anzahl in Kundenprofilen bezogene Anzeigeprobleme wurden behoben.
* Fehlerkorrektur – diverse Typologieprobleme wurden behoben.

#### E-Mails und SMS-Nachrichten  {#emails-and-sms-messages-2}

* Fehlerkorrektur – fehlerhafte Testsendungen können nicht länger bearbeitet werden. Sie sind nun schreibgeschützt.
* Fehlerkorrektur – Empfänger laufen bei zu langen oder Kodierungsprobleme aufweisenden SMS-Nachrichten nicht länger Gefahr, auf die Blacklist gesetzt zu werden.

#### Benutzerdefinierte Ressourcen {#custom-resources-1}

* Fehlerkorrektur – bei der Verwendung erweiterter Filter einer benutzerdefinierten Ressource werden nun alle Ergebnisse angezeigt.

#### Transaktionsnachrichten {#transactional-messages-1}

* Der Kennung einer neuen Ereignisdefinition wird nun automatisch ein Präfix hinzugefügt.
* In der Benutzeroberfläche wurde das Symbol für Transaktionsnachrichten geändert.

#### Integrationen  {#integrations-2}

* Fehlerkorrektur – beim Einfügen von Bildern mit hoher Auflösung unter Verwendung der Option **Dynamisches Bild von Adobe Target** kommt es nicht länger zu Anzeigefehlern.
* Fehlerkorrektur – eine freigegebene Zielgruppe kann künftig nicht mehr gespeichert werden, wenn in AMC Data Source keine Destination ID angegeben wurde.

## 16.7 - Version Juli 2016  {#release-16-7---july-2016}

### Neue Funktionen {#new-capabilities-3}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Angereicherte Transaktionsnachrichten<br /> </td> 
   <td> Es ist künftig möglich, Transaktionsvorlagen mit der Adobe Campaign-Datenbank zu verknüpfen, um mithilfe von auf diese Weise abgerufenen Informationen den Inhalt von Transaktionsnachrichten anzureichern.<br /> Lesen Sie für weiterführende Informationen das <a href="../../administration/using/configuring-transactional-messaging.md#enriching-the-transactional-message-content">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dynamische URLs für Bilder<br /> </td> 
   <td> Diese neue Funktion dient der Bildquellen-Personalisierung durch Einfügung von Inhaltsbausteinen und dynamischen Texten für Tracking- und Personalisierungszwecke.<br /> Zum Beispiel ist es künftig möglich, Parameter in Bild-URLs zu verwenden, um von den Dynamic-Media-Funktionen in AEM Asset (S7) zu profitieren. So können Sie beispielsweise eine E-Mail mit personalisierten Bildern senden und dazu entweder "Hallo Alexander, hier kommen die neuesten Events für Berlin" oder "Hallo Frank, hier kommen die neuesten Events für New York" einblenden.<br /> Lesen Sie für weiterführende Informationen das <a href="../../designing/using/personalization.md#personalizing-urls">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integration mit People Core Service<br /> </td> 
   <td> Bei der Integration von Adobe Campaign mit People Core Service (Profiles &amp; Audiences) werden nun Adobe-Marketing-Cloud-Kennungen vom Typ <strong>Declared ID</strong> berücksichtigt.<br /> Auf diese Weise lassen sich Segmente importieren und aus <strong>Besucherkennungen</strong> oder <strong>Declared IDs</strong><br /> bestehende Audiences exportieren. Weiterführende Informationen dazu finden Sie im <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Versandlogs<br /> </td> 
   <td> MTA-Logs (Versandserver) zeigen künftig den vollständigen Verlauf jeder Nachricht an, insbesondere alle Versandversuche einschließlich des dazugehörigen Fehlerstatus. Die Leistungen der Anwendung werden hiervon nicht beeinflusst.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-3}

#### Allgemein {#general-3}

* Fehlerkorrektur – anstelle irrelevanter Felder werden nun die Felder angezeigt, die ausgefüllt werden müssen. Irrelevante Felder wurden bisher angezeigt, nachdem bei der Bearbeitung einer Bedingung in einer Abfrage mehrmals der Vergleichsoperator geändert wurde.
* Fehlerkorrektur – bei der Definition einer relativen, auf ein Datumsfeld bezogenen Filterbedingung wurde das Verhalten der Option **[!UICONTROL Letzten X Tage/Monate/Quartale/Jahre]** korrigiert. Der Zeitraum wird künftig gleitend im Bezug auf Datum und Uhrzeit des Servers und nicht im Bezug auf ein Kalenderdatum berechnet.

#### Workflows  {#workflows-1}

* Fehlerkorrektur – in den Eigenschaften von **[!UICONTROL Abfrage]**-Aktivitäten wird im Bildschirm zur Auswahl der Zielgruppendimension nun die richtige Werteliste ausgegeben.
* Fehlerkorrektur – in **[!UICONTROL Abfrage]**-Aktivitäten wird bei Hinzufügung eines auf Kollektionselemente bezogenen Aggregats vom Typ Durchschnitt oder Zählung die Auswahl des **existiert**-Operators nicht mehr erzwungen.

#### Inhaltsbearbeitung {#content-editing}

* Fehlerkorrektur – beim Import von HTML-Inhalten treten keine Anzeigeprobleme im Bezug auf das "Responsive Design" mehr auf.
* Die Stilattribute werden beim ersten Öffnen des Inhalts nach dem Import nicht mehr überschrieben.
* Fehlerkorrektur – das Hinzufügen einer Bedingung zu einer dynamischen Inhaltsvariante löst keinen Fehler mehr aus. Fehlerkorrektur – das Hinzufügen einer Checkbox zum Inhalt einer Landingpage löst keinen Fehler mehr aus. Die Checkbox kann nun verwendet werden.
* Fehlerkorrektur – das Löschen von Text in einem Block löst auch dann keinen Fehler mehr aus, wenn der Cursor am Anfang des entsprechenden Blocks platziert ist.

#### Transaktionsnachrichten {#transactional-messages-2}

* Bei der Integration in eine Webseite ist es künftig möglich, für ein gegebenes Ereignis ein Ablaufdatum zu definieren. Nach Überschreiten dieses Datums kann die dem Ereignis entsprechende Nachricht nicht mehr gesendet werden.

## 16.6 - Version Juni 2016  {#release-16-6---june-2016}

### Neue Funktionen {#new-capabilities-4}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Profile-und-Dienste-API<br /> </td> 
   <td> Die Adobe Campaign-API <span class="uicontrol">Profile und Dienste</span> steht nun im <a href="https://www.adobe.io/products/campaign">adobe.io</a>-Portal zur Verfügung. Sie bietet die Möglichkeit, Profile in Adobe Campaign mithilfe von REST-Calls zu aktualisieren, einzufügen und zu löschen sowie sie für Dienste an- bzw. abzumelden.<br /> Weiterführende Informationen finden Sie in der <a href="https://docs.campaign.adobe.com/doc/standard/en/adobeio.html">detaillierten Beschreibung der API</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-4}

#### Allgemein {#general-4}

* Tooltips sind fortan auf Mobilgeräten deaktiviert, um die Lesbarkeit der angezeigten Informationen zu gewährleisten.
* Fehlerkorrektur – der Inhalt bestimmter Bildschirmbereiche auf dem iPad kann nun problemlos gescrollt werden.
* Fehlerkorrektur – bei Verwendung von Internet Explorer 11 treten bei der Bearbeitung von Inhalten keine Kompatibilitätsfehler mehr auf.
* Fehlerkorrektur – beim ersten Fehlschlag eines Datenimports kann nun ungehindert auf die detaillierten Protokolle zugegriffen werden.
* Fehlerkorrektur – Filter vom Typ Intervall können nun problemlos gespeichert werden.
* Fehlerkorrektur – bei der Konfiguration der Anzeige von Listen werden die Elemente einer Ressource nun korrekt angezeigt.
* Fehlerkorrektur – im Explorer des Abfrageeditors werden mittels des Suchfelds ausgegebene Ergebnisse nicht im Suchverlauf beibehalten, sodass sie bei einer erneuten Suche nicht weiterhin angezeigt werden.

#### E-Mails und SMS-Nachrichten  {#emails-and-sms-messages-3}

* Fehlerkorrektur – die auf Bounces bezogenen Informationen in Versandprotokollen können nun problemlos abgerufen werden.
* Fehlerkorrektur – auf den Kontext von dynamischen Inhaltsbausteinen in Transaktionsnachrichten kann nun problemlos zugegriffen werden.
* Fehlerkorrektur – in E-Mail-Inhalten lassen sich dynamische Texte nun problemlos mit URL-Links belegen.
* Fehlerkorrektur – die Anzeige der Titelleiste des Erstellungsassistenten eines Versands wurde korrigiert.
* Der Primärschlüssel eines Versands kann nicht länger als Personalisierungsfeld verwendet werden.

#### Workflows  {#workflows-2}

* Die Transitionen zwischen zwei Workflow-Aktivitäten zeigen nun die Anzahl der berechneten und von einer Aktivität zur anderen übertragenen Elemente an.
* Beim Hinzufügen von Zusatzdaten in einer **[!UICONTROL Abfrage]**-Aktivität sind die inkompatiblen Felder nun ausgeblendet.
* Das beim Hinzufügen von Zusatzdaten angezeigte Fenster zur Aggregatdefinition wurde insofern verbessert, als nur noch kompatible Optionen vorgeschlagen werden (z. B.: Ein Durchschnitt lässt sich ausschließlich unter Verwendung numerischer Daten berechnen).
* Start oder Neustart nativer technischer Workflows lassen sich nun nur noch von Benutzern mit Administratorrechten ausführen.

#### Landingpages  {#landing-pages-1}

* Fehlerkorrektur – in den Eigenschaften von Landingpages kommt es nicht länger zur Beschädigung von Schlüsseln mit AES-32-Bit-Verschlüsselung.
* Fehlerkorrektur – bei der Definition von Sichtbarkeitsbedingungen oder dem Hinzufügen von dynamischen Inhalten in Landingpages wird der Abfrageeditor nun korrekt angezeigt.

#### Benutzerdefinierte Ressourcen {#custom-resources-2}

* Die Option **[!UICONTROL In den Parametermodus wechseln]** ist nun bei der Definition eines auf die Dienstanmeldungen eines Profils bezogenen Filters ausgeblendet.
* Fehlerkorrektur – bei der Konfiguration einer 0:1-Relation in einer benutzerdefinierten Ressource wird kein Fehler mehr erzeugt.
* Fehlerkorrektur – der beim Hinzufügen eines Felds vom Typ **Datum und Uhrzeit** in einer benutzerdefinierten Ressource definierte **Konstante Standardwert** kann nun bei Bedarf problemlos bearbeitet werden.

## 16.5 - Version Mai 2016  {#release-16-5---may-2016}

### Neue Funktionen {#new-capabilities-5}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Vordefinierte Filter<br /> </td> 
   <td> Administratoren haben künftig die Möglichkeit, erweiterte Filter zu erstellen, die im Abfrageeditor als vorkonfigurierte Regeln erscheinen. Durch Auswahl dieser Filter haben es Benutzer leichter, komplexe Konfigurationen in einer vereinfachten Benutzeroberfläche zu erstellen, z. B. bei der Audience-Bestimmung.<br /> Lesen Sie für weiterführende Informationen das <a href="../../developing/using/configuring-filter-definition.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: An-/Abmeldedienst<br /> </td> 
   <td> Eine neue <span class="uicontrol">An-/Abmeldedienst</span>-Aktivität macht es möglich, mehrere Profile mittels einer einzigen Aktion für Dienste an- bzw. abzumelden.<br /> Sie können diese Aktivität im Anschluss an eine Zielgruppenbestimmung oder den Import einer Datei mit identifizierten Daten verwenden.<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/subscription-services.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Anreicherung von Daten<br /> </td> 
   <td> In <span class="uicontrol">Abfrage</span>-Aktivitäten ist nun der Tab <span class="uicontrol">Zusatzdaten</span> verfügbar. Mithilfe dieser Funktion lassen sich durch die Abfrage ermittelte Daten anreichern und an die Folgeaktivitäten des Workflows übertragen, wo sie weiter verwendet werden können.<br /> Nach dem Hinzufügen von Zusatzdaten können Sie ein zusätzliches Filterniveau auf die ursprünglich abgefragten Daten anwenden, indem Sie Bedingungen erstellen, die sich auf die definierten Zusatzdaten beziehen.<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/query.md#enriching-data">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Kontextuelle Hilfe<br /> </td> 
   <td> In den verschiedenen Adobe Campaign-Bildschirmen steht künftig eine kontextuelle Hilfe zur Verfügung. Dadurch können Sie mit einem einzigen Klick direkt auf die Dokumentation über die aktuell von Ihnen verwendete Funktion zugreifen. Verwenden Sie zur Anzeige der kontextuellen Hilfe das '?'-Symbol oben rechts im Bildschirm, wie unten dargestellt.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-5}

#### Allgemein {#general-5}

* Die Benutzeroberfläche wurde in vielerlei Hinsicht und entsprechend den Marketing-Cloud-Standards verbessert.
* Die verschiedenen Typen von Dropdown-Listen wurden vereinheitlicht.

#### E-Mails und SMS-Nachrichten  {#emails-and-sms-messages-4}

* Fehlerkorrektur – E-Mails können nun auch dann problemlos gesendet werden, wenn die Fehleradressenmaske ausgefüllt ist.
* Für den Versand von E-Mails wird künftig das TLS-Protokoll unterstützt. Mithilfe einer neuen Spalte in der MX-Verwaltung lässt sich künftig für jede Domain das gewünschte TLS-Verhalten definieren.
* Die Benutzeroberfläche von SMS wurde verbessert.

#### Workflows  {#workflows-3}

* Diverse Verbesserungen der Workflow-Benutzeroberfläche.
* Fehlerkorrektur – die Quick Actions werden nun korrekt angezeigt.
* Fehlerkorrektur – Workflows schlagen nicht länger fehl, wenn Aktivitäten des Typs **[!UICONTROL Segmentierung]** verwendet werden, die eine 1:n-Relation enthalten.
* Fehlerkorrektur – Workflow-Transitionen lassen sich nun auch ungehindert auf hybriden Geräten öffnen.
* Fehlerkorrektur – die 'Aussetzen'-Schaltfläche wird nun auch beim ersten Start eines Workflows angezeigt.

#### Inhaltseditor  {#content-editor}

* Mit dem Inhaltseditor lassen sich jetzt jegliche URLs in E-Mails oder Landingpages personalisieren. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../designing/using/personalization.md#personalizing-urls).
* Fehlerkorrektur – Bilder gehen nicht länger verloren, wenn sie im Erstellungsassistenten des Versands hinzugefügt und der Inhalt in der Folge geändert wurde.

#### Benutzerdefinierte Ressourcen {#custom-resources-3}

* Fehlerkorrektur – das Hinzufügen eines personalisierten Links vom Typ 1:n im Konfigurationsbildschirm einer benutzerdefinierten Ressource löst keinen Fehler mehr aus.
* Die Fortschrittsanzeige bei der Vorbereitung und Publikation von benutzerdefinierten Ressourcen wurde verbessert.
* Fehlerkorrektur – die Anzeige der Liste der Relationen einer benutzerdefinierten Ressource erfolgt nun fehlerfrei.

#### Transaktionsnachrichten {#transactional-messages-3}

* Die Benutzerfreundlichkeit der Oberfläche sowie die Leistungsfähigkeit und Robustheit der Transaktionsnachrichten-Engine wurden optimiert.
* Es besteht künftig die Möglichkeit, die Publikation von Transaktionsnachrichtenvorlagen vorübergehend auszusetzen. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../channels/using/event-transactional-messages.md#suspending-a-transactional-message-publication).
* Fehlerkorrektur – in Transaktionsnachrichtenvorlagen können nicht länger Inhaltsbausteine mit inkompatibler Zielgruppendimension hinzugefügt werden.
* Fehlerkorrektur – die Anzeige der API-Vorschau im Konfigurationsbildschirm eines Ereignisses wird nicht länger behindert.

#### Audiences und Abfragen  {#audiences-and-queries-1}

* Verschiedene auf die Datumsangabe im Abfrageeditor bezogene Korrekturen. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../automating/using/editing-queries.md#creating-queries).

#### Administration  {#administration}

* Fehlerkorrektur – ein auf den Namen der Sicherheitsgruppe "Standardbenutzer" bezogener Fehler hindert Benutzer nicht länger daran, sich einzuloggen.

## 16.3 - Version März 2016  {#release-16-3---march-2016}

### Neue Funktionen {#new-capabilities-6}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Benutzeroberfläche und Navigation<br /> </td> 
   <td> Die Adobe Campaign-Benutzeroberfläche wurde verbessert, um Navigation und Prozesse einfacher und intuitiver zu gestalten.<br /> Die Navigationsleiste befindet sich nun im oberen Bereich der Anwendung. Auf erweiterte Menüs kann über das <strong>Adobe Campaign</strong>-Logo zugegriffen werden.<br /> Lesen Sie für weiterführende Informationen das <a href="../../start/using/interface-description.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Audience-Speicherung<br /> </td> 
   <td> In der <span class="uicontrol">Audience-Speicherung</span>-Aktivität ist nun die neue Option <span class="uicontrol">Neue Audience erstellen und aktualisieren</span> verfügbar. Bei Verwendung dieser Option wird der Audience-Titel manuell eingeben. Wenn der eingegebene Titel einer bereits existierenden Audience entspricht, wird diese aktualisiert. Sollte die Audience noch nicht existieren, wird sie erstellt.<br />Des Weiteren wird die Audience bei jeder weiteren Workflow-Ausführung aktualisiert.<br /> Sie haben weiterhin die Möglichkeit, den Aktualisierungsmodus für Audiences auszuwählen: d. h., die Audience mit neuen Daten anzureichern oder die Gesamtheit der Daten der Audience bei jeder Ausführung zu ersetzen.<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/save-audience.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Segmentierung<br /> </td> 
   <td> Mithilfe der <span class="uicontrol">Segmentierung</span>-Aktivität lassen sich nun Daten von temporären Ressourcen segmentieren. Zum Beispiel: Daten einer importierten Datei.<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/segmentation.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-6}

#### Allgemein {#general-6}

* Fehlerkorrektur – bei der Sortierung von Listen tritt kein Anzeigefehler mehr auf: Der die Sortierreihenfolge anzeigende Pfeil zeigt nun für alle Datentypen in die richtige Richtung.
* Fehlerkorrektur – bei der Hinzufügung einer Regel in einer Abfrage wird die Anzahl der in einem Dropdown-Menü angezeigten Elemente nicht mehr begrenzt.

#### E-Mails und SMS-Nachrichten  {#emails-and-sms-messages-5}

* Fehlerkorrektur – der Zugriff auf den E-Mail-Rendering-Bericht erfolgt nun fehlerfrei.
* Bei der Versandvorbereitung wird nun ein Fehler ausgegeben, wenn keine Absenderadresse angegeben wurde.

#### Workflows  {#workflows-4}

* Bei der Extraktion von Dateien im CSV-Format wurden gewisse Optionen zur Dateiformatierung angezeigt, ohne berücksichtigt zu werden. Diese Optionen werden künftig nicht mehr angezeigt.
* Fehlerkorrektur – bei der Übertragung einer **[!UICONTROL SFTP]**-Datei tritt kein Fehler mehr auf, wenn die Option **[!UICONTROL Quelldateien nach der Übertragung löschen]** angekreuzt ist.
* Fehlerkorrektur – die Anzeige der Zählung und Datenvorschau einer **[!UICONTROL Abfrage]** ist nun auch nach der Aktualisierung der Seite fehlerfrei möglich.
* Fehlerkorrektur – das Öffnen bestimmter Transitionen, insbesondere derer, die aus Versandaktivitäten oder Abfragen mit unterschiedlicher Zielgruppen- und Filterdimension ausgehen, löst keinen Fehler mehr aus.
* Fehlerkorrektur – Personalisierungsfelder können nun auch dann problemlos in eine Versandaktivität eingefügt werden, wenn der Workflow nach dem Hinzufügen der Aktivität nicht erneut gespeichert wurde.
* Fehlerkorrektur – die Zielgruppendimension ausgehender Transitionen einer E-Mail-Versandaktivität wird nun fehlerfrei angezeigt.

#### Landingpages  {#landing-pages-2}

* Fehlerkorrektur – Personalisierungsfelder funktionieren nun auch in lokalisierbaren Inhaltsbausteinen von Landingpages.

#### Benutzerdefinierte Ressourcen {#custom-resources-4}

* Fehlerkorrektur – eine benutzerdefinierte Ressource kann nun auch dann fehlerfrei durchsucht werden, wenn in der Bildschirmdefinition der Ressource die Option **[!UICONTROL Felder zur Suche hinzufügen]** angekreuzt ist und in der **[!UICONTROL Zusammenstellung des Filterbereichs]** mehrere Felder ausgewählt sind.

## 16.2 - Version Februar 2016 {#release-16-2---february-2016}

### Neue Funktionen {#new-capabilities-7}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> A/B-Test für E-Mails<br /> </td> 
   <td> Sie haben künftig die Möglichkeit, A/B-Tests zu Inhalt, Betreff oder Absendername von E-Mails durchzuführen. Mit dieser neuen Funktion lassen sich bis zu drei Varianten eines Elements testen.<br /> Bei Verwendung einer der A/B-Test-spezifischen Vorlagen zur E-Mail-Erstellung ermöglicht eine neue Etappe im Erstellungsassistenten die Definition der Testparameter.<br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/designing-an-a-b-test-email.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Verwaltung von Marken<br /> </td> 
   <td> Sie haben künftig die Möglichkeit, eine oder mehrere Marken zu definieren und auf die Identität der jeweiligen Marken bezogene Parameter zentral anzugeben. Des Weiteren können diese Marken verschiedenen Versand- oder Landingpage-Vorlagen zugeordnet werden.<br /> Lesen Sie für weiterführende Informationen das <a href="../../administration/using/branding.md#assigning-a-brand-to-an-email">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Inkrementelle Abfrage<br /> </td> 
   <td> Die neue Workflow-Aktivität <span class="uicontrol">Inkrementelle Abfrage</span> ermöglicht Ihnen die Durchführung von Abfragen, die bei jeder Ausführung lediglich auf neue Ergebnisse abzielen. Dabei werden die Ergebnisse früherer Ausführungen automatisch ausgeschlossen. In Verbindung mit einer <span class="uicontrol">Planung</span> lässt sich der Ausführungsrhythmus der <span class="uicontrol">Inkrementellen Abfrage</span> bestimmen .<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/incremental-query.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transaktionsnachrichten<br /> </td> 
   <td> Die Benutzerfreundlichkeit der Oberfläche zur Verwaltung von Transaktionsnachrichten hat sich verbessert. Alle Business-Prozesse in Bezug auf Transaktionsnachrichten werden jetzt zentral im Menü <span class="uicontrol">Marketingpläne</span> &gt; <span class="uicontrol">Transaktionsnachrichten</span> verwaltet. Außerdem wurde die Ereigniskonfiguration verbessert. Ereignisse werden nun unabhängig von benutzerdefinierten Ressourcen verwaltet.<br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/about-transactional-messaging.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-7}

#### Allgemein {#general-7}

* Fehlerkorrektur – die Anzeige in Berichten, Listen und Abfragen erfolgt nun fehlerfrei.
* Fehlerkorrektur – bei mobilen Geräten kommt es nicht mehr zu Kompatibilitäts- und Anzeigeproblemen.

#### E-Mails und SMS-Nachrichten  {#emails-and-sms-messages-6}

* Fehlerkorrektur – bei der Erstellung von Nachrichten (E-Mail oder SMS) wird die Anzeige der Schaltfläche zum Einfügen von Personalisierungsfeldern nicht mehr behindert.
* Fehlerkorrektur – über Mblox gesendete SMS werden nun korrekt übertragen.

#### Audiences und Abfragen  {#audiences-and-queries-2}

* Fehlerkorrektur – beim Hinzufügen einer zusätzlichen Bedingung in einer Abfrage wird auch dann kein die Zählung betreffender Fehler mehr erzeugt, wenn zuvor die Filterdimension geändert wurde.
* Fehlerkorrektur – bei der Vorschau von Abfrageergebnissen kommt es nicht länger zu einem falschen Seitenumbruch.

#### Inhaltsbearbeitung  {#content-editing-1}

* Fehlerkorrektur – bei der Verwendung benutzerdefinierter Auflistungen wird die Konfiguration eines dynamischen Inhalts nun korrekt berücksichtigt.

#### Workflows  {#workflows-5}

* Fehlerkorrektur – das Vorhandensein einer leeren Zeile im Tab **[!UICONTROL Zu aktualisierende Felder]** einer **[!UICONTROL Daten-Update]**-Aktivität verhindert nicht länger die Ausführung aller Aktivitäten in einem Workflow.
* Fehlerkorrektur – der Import von Daten, die Informationen zu geografischen Einheiten und Organisationseinheiten enthalten, ist nun fehlerfrei möglich.
* Fehlerkorrektur – das Hinzufügen einer **[!UICONTROL Ausschluss]**-Regel vom Typ **[!UICONTROL Achsenänderung]** löst keinen Fehler mehr aus.
* Fehlerkorrektur – die Manipulation einer aus einer **[!UICONTROL Segmentierung]**-Aktivität ausgehenden Transition führt nicht länger zur Erstellung eines unerwünschten zusätzlichen Segments.
* Fehlerkorrektur – das Laden einer Datei in einer Workflow-Vorlage erzeugt keinen Fehler mehr.
* Fehlerkorrektur – Leerzeichen können nun ungehindert als Spaltentrennzeichen in der **[!UICONTROL Datei-laden]**-Aktivität verwendet werden.

#### Benutzerdefinierte Ressourcen {#custom-resources-5}

* Fehlerkorrektur – der Status einer benutzerdefinierten Ressource lässt sich nach einem Package-Import nun auch dann zurücksetzen, wenn die Ressource zum Zeitpunkt des Exports bereits publiziert war.

#### Packages  {#packages}

* Fehlerkorrektur – Packages können nun auch dann exportiert werden, wenn sie einen Workflow enthalten.
* Fehlerkorrektur – die Auswahl mehrerer Elemente derselben Ressource wird nicht länger behindert.

## 16.1 - Version Januar 2016  {#release-16-1---january-2016}

### Neue Funktionen {#new-capabilities-8}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Berichte<br /> </td> 
   <td> Folgende auf E-Mail-Sendungen bezogene Berichte stehen nun zur Verfügung: <span class="uicontrol">Beschwerden</span>, <span class="uicontrol">Öffnungen</span> und <span class="uicontrol">Abmeldungen</span> .<br /> Folgende Berichte wurden verbessert: <span class="uicontrol">Versandzusammenfassung</span>, <span class="uicontrol">Bounces</span>, <span class="uicontrol">Versanddurchsatz</span> und <span class="uicontrol">Trackingindikatoren</span> .<br /> Lesen Sie für weiterführende Informationen das <a href="../../reporting/using/defining-the-report-period.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Abfragenbearbeitung<br /> </td> 
   <td> Das Abfragetool wurde verbessert und ermöglicht nun die Suche in <strong>1:N</strong>-Relationen.<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/editing-queries.md#creating-queries">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Inhaltspersonalisierung<br /> </td> 
   <td> Im Zusammenhang mit der Bearbeitung von E-Mails und Landingpages wurde die Bedieneroberfläche zur Angabe der Anzeigebedingungen von Inhaltsbausteinen verbessert.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Spaltendefinition beim Import<br /> </td> 
   <td> In der Aktivität <span class="uicontrol">Datei laden</span> können die Spalten einer importierten Datei in Zukunft detailliert konfiguriert werden: erwarteter Datentyp, Format von Datum und Uhrzeit, Umgang mit leeren Werten und Fehlern sowie Neukodifizierung von Werten.<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/load-file.md#column-format">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> SMS-Kodierungs-Mapping<br /> </td> 
   <td> Es ist künftig möglich, benutzerdefinierte Mappings zur SMS-Kodierung für Anbieter zu definieren, die nicht die Standardkodierung verwenden. Die Konfiguration benutzerdefinierter Mappings erfolgt durch Administratoren, welche darüber hinaus eine Rangordnung für die Berücksichtigung der Mappings definieren.<br /> Lesen Sie für weiterführende Informationen das <a href="../../administration/using/configuring-sms-channel.md#smsc-specifics">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-8}

#### Allgemein {#general-8}

* Verbesserung der Kompatibilität mit Internet Explorer und Chrome bei Hybrid- und Touch-Geräten.
* Fehlerkorrektur – kein Datenverlust mehr, wenn bei der Erstellung eines neuen Benutzers/Profils/Testprofils die E-Mail-Adresse eine fehlerhafte Syntax aufweist.

#### E-Mails und SMS-Nachrichten  {#emails-and-sms-messages-7}

* Fehlerkorrektur – die Miniaturansicht des Inhalts kann nun auch aus der E-Mail-Vorschau korrekt erzeugt werden.
* Fehlerkorrektur – der Roh-Inhalt von E-Mails oder SMS wird nun auch im Vorschaubildschirm korrekt angezeigt.

#### Audiences und Abfragen  {#audiences-and-queries-3}

* Fehlerkorrektur – die Erstellung von **Abfrage**-Audiences ist nun auch in Bezug auf die **Dienst**-Ressource möglich.
* Fehlerkorrektur – in Abfragen wird die Funktionsliste nun auch bei der Bearbeitung einer Bedingung im erweiterten Modus korrekt angezeigt.
* Fehlerkorrektur – die Erstellung von **Abfrage**-Audiences ist nun auch mit auf Kollektionen basierenden Kriterien möglich.
* Fehlerkorrektur – die Erstellung von Abfragen ist nun auch dann möglich, wenn darin auf Versand-KPIs zielende Filter enthalten sind.
* Fehlerkorrektur – die Vorschau von in Workflows erstellten Audience-Inhalten wird nun korrekt erzeugt.

#### Benutzerdefinierte Ressourcen {#custom-resources-6}

* Fehlerkorrektur – kein Serverabsturz mehr bei benutzerdefinierten Ressourcen mit Feldern, die einen dynamischen Standardwert aufweisen.
* Fehlerkorrektur – bei der Bildschirmdefinition für benutzerdefinierte Ressourcen löst das Verschieben und anschließende Löschen von Elementen im Bereich **[!UICONTROL Konfiguration des Detailbildschirms]** keinen Fehler mehr aus.
* Fehlerkorrektur – kein Fehler mehr bei der Definition eines Standardwerts in Listen vom Typ **Integer**, die nicht **0** als möglichen Wert enthalten.
* Fehlerkorrektur – in benutzerdefinierten Ressourcen ist bei der Konfiguration des Detailbildschirms das Hinzufügen eines Elements nun auch nach einer Zurücksetzung möglich.

#### Workflows  {#workflows-6}

* Fehlerkorrektur – es werden nicht mehr die Protokolle aller Aktivitäten, sondern nur die der markierten Aktivität angezeigt.
* Fehlerkorrektur in Zusammenhang mit der Aktivität **[!UICONTROL Planung]**. Die Option **[!UICONTROL Tag des Monats]** wird nun korrekt berücksichtigt und nicht mehr durch **[!UICONTROL Tag der Woche]** ersetzt.
* Fehlerkorrektur – die Aktivität **[!UICONTROL Planung]** arbeitet nun auch dann korrekt, wenn der Ablaufmodus mit **[!UICONTROL Nach einer bestimmten Anzahl an Ausführungen]** angegeben ist.
* Fehlerkorrektur in Zusammenhang mit dem Datenexport mittels der Aktivität **[!UICONTROL Dateiextraktion]**. Die in der Exportdatei enthaltene Anzahl an Zeilen stimmt nun mit der Anzahl an tatsächlich exportierten Elementen überein.
* Fehlerkorrektur – kein Fehler mehr bei der Auswahl von Dateien in der Aktivität **[!UICONTROL Datei laden]**.
* Fehlerkorrektur – in der Aktivität **[!UICONTROL Daten-Update]** ist es nun möglich, zu aktualisierende Felder zu löschen.
* Fehlerkorrektur – Änderungen eines Workflows können nun auch dann gespeichert werden, wenn zuvor die Ausführungsprotokolle geöffnet wurden.
* Fehlerkorrektur – die Aktivität **[!UICONTROL Datei laden]** wird nun auch dann nicht mehr doppelt ausgeführt, wenn ihre Konfiguration die Verwendung der Datei der eingehenden Transition vorsieht und diese über eine **[!UICONTROL Dateiübertragung]** geladen wurde.
* Fehlerkorrektur – temporäre Entitäten werden nun von **Ausschluss**-Aktivitäten korrekt verarbeitet.
* Fehlerkorrektur – **[!UICONTROL Abfrage]**-Aktivitäten werden nun auch dann korrekt ausgeführt, wenn die in der Aktivität konfigurierten Zielgruppen- und Filterdimensionen verschieden sind.
* Fehlerkorrektur – bei **[!UICONTROL Verzweigung]**-Aktivitäten wird das Speichern des Workflows nicht mehr durch die automatische Benennung von ausgehenden Transitionen, die zur besagten Aktivität hinzugefügt werden, verhindert.

#### Inhaltsbearbeitung {#content-editing-2}

* Fehlerkorrektur – bei der Inhaltsbearbeitung werden keine ungewünschten Symbole oder Suchmenüs mehr angezeigt.

#### Landingpages  {#landing-pages-3}

* Fehlerkorrektur – Landingpages können nun mittels eines Package-Imports importiert werden.

#### Transaktionsnachrichten {#transactional-messages-4}

* Im Benutzer "Message Center Push Agent" können künftig verlässliche IP-Adressen in den Sicherheitsparametern angegeben werden.
* Fehlerkorrektur – die Erstellung von neuen Ereignistypen wird nicht mehr behindert.

## 15.11 - Version November 2015  {#release-15-11---november-2015}

### Neue Funktionen {#new-capabilities-9}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> SMS-Kanal<br /> </td> 
   <td> Es ist nun möglich, in Adobe Campaign SMS-Nachrichten zu senden.<br /> Wie auch E-Mails können Sie SMS-Sendungen in Kampagnen oder ausgehend von der Liste der Marketingaktivitäten erstellen. In Workflows lassen sich ebenfalls SMS-Sendungen zum einmaligen oder zum wiederkehrenden Versand erstellen.<br /> Diese SMS-Sendungen basieren auf Vorlagen, deren Konfiguration über die Versandvorlagenliste erfolgt. Eine Vorlage ist standardmäßig enthalten.<br /> SMS-Sendungen unterstützen SMPP 3.4, das von der Mehrzahl der SMS-Router verwendet wird.<br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/about-sms-messages.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Analyse von Transitionen<br /> </td> 
   <td> Es ist nun möglich, Daten und deren Struktur in der letzten Transition eines Workflows zu analysieren. Auf diese Weise können Sie prüfen, ob die ausgeführten Aktivitäten die gewünschten Ergebnisse erzielen.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dateibezogene Vorab-Bearbeitung und Anschlussvorgänge in Workflows<br /> </td> 
   <td> Beim Import und Export von Dateien mithilfe der <span class="uicontrol">Datei laden</span>- und <span class="uicontrol">Dateiextraktion</span>-Aktivitäten können künftig weitere Bearbeitungsschritte hinzugefügt werden.<br /> Standardmäßig bieten diese Aktivitäten die Möglichkeit der Komprimierung und Dekomprimierung von Dateien im GZIP-Format.<br /> Weiterführende Informationen finden Sie in den Kapiteln <a href="../../automating/using/load-file.md">Datei laden</a> und <a href="../../automating/using/extract-file.md">Dateiextraktion</a> des Workflow-Handbuchs.<br /> </td> 
  </tr> 
  <tr> 
   <td> Zustellberichte<br /> </td> 
   <td> Ein E-Mail-Rendering-Bericht steht künftig zur Verfügung. Dieser Bericht zeigt die verschiedenen Renderings einer Nachricht in Abhängigkeit von Medium und E-Mail-Client, auf dem sie angezeigt wird.<br /> Die Zusammenfassung des Berichts zeigt darüber hinaus die Anzahl an empfangenen, als Spam gekennzeichneten und nicht empfangenen Nachrichten sowie die Anzahl an Nachrichten, deren Empfang ausstehend ist.<br /> Lesen Sie für weiterführende Informationen das <a href="../../sending/using/email-rendering.md#email-rendering-report-description">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Packageverwaltung<br /> </td> 
   <td> Es ist in Packages künftig möglich, Bilder zu importieren und zu exportieren.<br /> </td> 
  </tr> 
  <tr> 
   <td> Quick Actions<br /> </td> 
   <td> Wird die Maus über ein Element in einer Liste oder einem Workflow bewegt oder dieses ausgewählt, werden bestimmte Aktionen angezeigt. Manche dieser Aktionen werden jetzt als Symbole rund um die betreffenden Elemente angezeigt, um den Zugriff zu erleichtern. Diese sogenannten Quick Actions ermöglichen das rasche Duplizieren, Löschen, Öffnen etc. von Elementen.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-9}

#### Allgemein {#general-9}

* Fehlerkorrektur – der Zugriff auf allgemeine Instanzparameter ist nun auch mit Benutzerkonten vom Typ Administrator möglich.
* Der Datentyp **float** wird in benutzerdefinierten Ressourcen nun korrekt unterstützt.
* Fehlerkorrektur – die Statusänderung der Vorlage eines vereinfachten Imports löst in der Liste der ausgeführten Importe keinen Anzeigefehler mehr aus.

#### Landingpages  {#landing-pages-4}

* Fehlerkorrektur – Landingpage-Vorlagen werden in englischsprachigen Instanzen nicht mehr teilweise in französischer Sprache angezeigt.

#### Audiences  {#audiences}

* Fehlerkorrektur – aus Adobe Marketing Cloud importierte Audiences werden nun in der Audience-Liste angezeigt.
* Fehlerkorrektur – bei der Abfragedefinition wird die Option "Groß-/Kleinschreibung beachten" nicht mehr ungewollt aktiviert.
* Fehlerkorrektur – bei der Abfragedefinition wird die Filterung von Audiences nicht mehr verhindert.
* Fehlerkorrektur – in Audiences wird der Abbruch von Aktionen nicht mehr verhindert.

#### Workflows  {#workflows-7}

* Fehlerkorrektur – in **[!UICONTROL Daten-Update]**-Aktivitäten können die zu aktualisierenden Felder nun auch manuell konfiguriert werden.
* Fehlerkorrektur – kein endloses Laden beim Öffnen einer **[!UICONTROL Abfrage]**-Aktivität mehr, wenn der Workflow nach der Platzierung der Aktivität im Diagramm nicht gespeichert wurde.
* Fehlerkorrektur – in Workflow-**[!UICONTROL Abfragen]** ausgewählte Audiences lösen bei der Zählung und der Vorschau keinen Serverausfall mehr aus.
* Fehlerkorrektur – beim Öffnen von Workflow-Aktivitäten erscheint keine unnötige Fehlernachricht mehr.
* Fehlerkorrektur – die Konfiguration von **[!UICONTROL Planung]**-Aktivitäten zur wiederholten Ausführung eines Workflows am selben Tag wird nicht mehr verhindert.
* Fehlerkorrektur – in Workflow-Aktivitäten werden keine Felder mehr angezeigt, die in Abfragen nicht berücksichtigt werden können.
* Fehlerkorrektur – in ausgehenden Transitionen werden in **[!UICONTROL Abfragen]** bezüglich Sendungen hinzugefügte KPIs nun korrekt wiedergegeben.
* Fehlerkorrektur – in Workflows wird die Erstellung von Audiences vom Typ Datei nach dem Dateiimport nicht mehr verhindert.
* Fehlerkorrektur – Profildaten werden nun auch dann korrekt aktualisiert, wenn das Feld **location/address3** der Ressource verwendet wird.
* Fehlerkorrektur – heterogene Aktivitäts-Kollektionen können in Workflows nun dupliziert werden.
* Fehlerkorrektur – in Workflows werden bei wiederkehrenden Sendungen die der Fehlerdiagnose dienenden SQL-Scripts nun korrekt angezeigt.

#### Inhaltseditor  {#content-editor-1}

* Fehlerkorrektur – das Suchen im Quellcode von Landingpages und E-Mails ist nun möglich.

#### Packages  {#packages-1}

* Fehlerkorrektur – Korrektur diverser Fehler, die den Export bestimmter Elementtypen (insbesondere Landingpages, Workflows) in Packages verhinderten.
* Fehlerkorrektur – geänderte Titel von Package-Importen werden nun korrekt anstelle der alten Titel angezeigt.
* Fehlerkorrektur – inkompatible Ressourcen werden nicht mehr in der Liste der exportierbaren Ressourcen angezeigt.

## 15.10 - Version Oktober 2015  {#release-15-10---october-2015-}

### Neue Funktionen {#new-capabilities-10}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Workflows: Aktivität "Deduplizierung"<br /> </td> 
   <td> Die Workflow-Aktivitäten wurden um die Deduplizierung erweitert. Diese Aktivität ermöglicht das Auffinden von Dubletten in Zielgruppen anhand von Kriterien, die Sie selbst festlegen.<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/deduplication.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: verbessertes Diagramm<br /> </td> 
   <td> Im Workflow-Arbeitsbereich können künftig Tastenkombinationen zum Auswählen, Öffnen und Löschen von Aktivitäten verwendet werden.<br /> Darüber hinaus wurde die Ausrichtung der Aktivitäten verbessert, um eine bessere visuelle Organisation von Workflows zu ermöglichen.<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/workflow-interface.md#workspace">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Aktivität "Dateiextraktion"<br /> </td> 
   <td> Der Name von mithilfe der <span class="uicontrol">Dateiextraktion</span> exportierten Dateien wird künftig automatisch mit dem Datum und der Uhrzeit der Erstellung ergänzt, um seine Eindeutigkeit zu gewährleisten.<br /> </td> 
  </tr> 
  <tr> 
   <td> Vereinfachter Datenimport<br /> </td> 
   <td> Der Name der Vorlage, die für einen vereinfachten Import verwendet wurde, ist künftig standardmäßig in der Importliste und in der Detailansicht eines jeden Imports sichtbar.<br /> </td> 
  </tr> 
  <tr> 
   <td> Benutzerdefinierte Ressourcen<br /> </td> 
   <td> Die Verwaltung und Erstellung von Relationen für benutzerdefinierte Ressourcen wurde verbessert und erweitert.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-10}

#### E-Mail {#email}

* Fehlerkorrektur – Abmelde-Links arbeiten nun auch ausgehend von Mirrorseiten korrekt.
* Fehlerkorrektur – der Titel von E-Mail-Sendungen wird nun in der Bearbeitungsseite der E-Mail korrekt angezeigt.
* Fehlerkorrektur – externe **[!UICONTROL Routing]**-Konten können nun auch in duplizierten Versandvorlagen ausgewählt werden.

#### Audiences {#audiences-1}

* Fehlerkorrektur – bei der Audience-Zählung tritt kein Fehler mehr auf, wenn in der Abfrage eine 1:N-Relation verwendet wird.
* Fehlerkorrektur – die Profilauswahl in E-Mail-Audiences ist nun ohne Probleme möglich.

#### Workflows  {#workflows-8}

* Fehlerkorrektur – bei der Konfiguration eines E-Mail-Versands in Workflows treten keine Anzeigeprobleme mehr auf.
* Fehlerkorrektur – die Aktivität **[!UICONTROL Datei laden]** funktioniert nun fehlerfrei. Zuvor wurde eine leere Fehlermeldung angezeigt.
* Fehlerkorrektur – die Aktivität **[!UICONTROL Dateiübertragung]** funktioniert nun fehlerfrei. Zugriffsberechtigungen wurden nicht immer korrekt gehandhabt.
* Fehlerkorrektur – in Workflows mit einer **[!UICONTROL E-Mail zum wiederkehrenden Versand können Dateien nun korrekt exportiert werden]** .
* Fehlerkorrektur – in Workflows können nun E-Mail-Sendungen korrekt erstellt werden und sowohl Betreff als auch Inhalt werden korrekt berücksichtigt.
* Fehlerkorrektur – im Zuge der Konfiguration von Workflows für Vorlagen des vereinfachten Imports ist in der **[!UICONTROL Daten-Update]**-Aktivität nun die Auswahl von Abstimmschlüsseln ohne Probleme möglich.
* Fehlerkorrektur – die Speicherung von Workflows ist nun auch dann korrekt möglich, wenn zuvor eine Aktivität gelöscht wurde.

#### Plattform {#platform}

* Fehlerkorrektur – ein neues Element kann nun auch dann erstellt werden, wenn eine benutzerdefinierte Ressource eine Relation zum Ressourcentyp des besagten Elements enthält.
* Fehlerkorrektur – das Schreiben von gewissen Protokollen nimmt nun nicht mehr bis zu 15 Minuten in Anspruch.
* Fehlerkorrektur – die Liste der Marketingaktivitäten wird nun auch bei Sortierung nach **[!UICONTROL Datum]** oder **[!UICONTROL Indikatoren]** korrekt angezeigt.

#### Landingpages {#landing-pages-5}

* Fehlerkorrektur – die Auswahl eines Testprofils für die Landingpage-Vorschau löst keinen Fehler mehr aus.

#### Transaktionsnachrichten {#transactional-messages-5}

* Fehlerkorrektur – das Löschen eines Testprofil-Ereignisses löst keinen Absturz der Anwendung mehr aus.

#### Berichte {#reports}

* Fehlerkorrektur – in den Berichten **[!UICONTROL deliveryThroughputReport]** und **[!UICONTROL deliveryTrackingReport]** werden nun die richtigen Daten erzeugt.

#### Inhaltseditor {#content-editor-2}

* Fehlerkorrektur – HTML-Tags werden nun bei der Verarbeitung von dynamischen Inhaltsbausteinen korrekt verwaltet.

## 15.8 - Version August 2015  {#release-15-8---august-2015}

### Neue Funktionen {#new-capabilities-11}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Vereinfachter Datenimport<br /> </td> 
   <td> Adobe Campaign bietet künftig eine vereinfachte Methode zum Import von Daten.<br /> Benutzer können Vorlagen nutzen, welche nur das Laden der die gewünschten Daten enthaltenden Datei erfordern. Diese Vorlagen sind zuvor von einem Administrator zu definieren. Ein in der Vorlage definierter Workflow wird – für den Benutzer transparent – ausgeführt. Letzterer kann direkt auf das Ergebnis sowie eine die Zurückweisungen enthaltende Datei zugreifen.<br /> Die Daten dieser Dateien können zur Datenbank hinzugefügt oder direkt zur Erstellung einer Audience verwendet werden.<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/about-data-import-and-export.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Erstellung von Programmen und Kampagnen<br /> </td> 
   <td> Bei der Erstellung von Programmen und Kampagnen wird als Startdatum künftig automatisch das aktuelle Tagesdatum verwendet.<br /> Das Enddatum wird in Abhängigkeit vom Startdatum wie folgt berechnet:<br /> 
    <ul> 
     <li> Startdatum + 186 Tage bei Programmen, </li> 
     <li> Startdatum + 61 Tage bei Kampagnen. </li> 
    </ul> Lesen Sie für weiterführende Informationen das <a href="../../start/using/programs-and-campaigns.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> E-Mail<br /> </td> 
   <td> Die Liste der getrackten URLs ist künftig schreibgeschützt.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transaktionsnachrichten<br /> </td> 
   <td> Es ist künftig möglich, den Versand personalisierter Transaktionsnachrichten (Kennwortänderung, Registrierungsbestätigung etc.) zu automatisieren.<br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/about-transactional-messaging.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Benutzerdefinierte Ressourcen<br /> </td> 
   <td> Verschiedene neue Funktionen stehen künftig zur Verfügung: Erweiterung der Testprofil-Ressource, Verwaltung nach Status und Löschen von Ressourcen.<br /> Lesen Sie für weiterführende Informationen das <a href="../../developing/using/resource-statuses.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-11}

#### Anzeige {#display}

* Fehlerkorrektur – im Abfragetool werden unter Safari Felder nicht mehr überlappend angezeigt.

#### Inhaltseditor  {#content-editor-3}

* Fehlerkorrektur – im E-Mail-Betreff können künftig die Zeichen '&lt;', '&amp;' und '&gt;' verwendet werden.

#### E-Mail {#email-1}

* Fehlerkorrektur – das Hinzufügen von Text im Anschluss an einen dynamischen Text ist nun möglich.

#### Listen  {#lists}

* Fehlerkorrektur – beim Export der Ausführungslogs eines Workflows wird die Spalte **Nachricht** nun korrekt exportiert.

#### Profile und Audiences  {#profiles-and-audiences}

* Fehlerkorrektur – Duplizieren und Löschen von Elementen lösen keine doppelte Bestätigungsaufforderung mehr aus **(betraf nur Hybridgeräte unter Internet Explorer 11)**.

#### Workflows  {#workflows-9}

* Fehlerkorrektur – E-Mails werden nun auch im Zuge von Workflow-Ausführungen korrekt versendet.
* Fehlerkorrektur – Workflows können jetzt ausgeführt werden, wenn in einer **[!UICONTROL Datei laden]**-Aktivität der Name der Zurückweisungsdatei nicht angegeben wird.
* Fehlerkorrektur – Workflows können jetzt ausgeführt werden, wenn in einer **[!UICONTROL Planung]**-Aktivität die **[!UICONTROL Ausführungshäufigkeit]** mit **[!UICONTROL Täglich]** angegeben wird .

#### Plattform {#platform-1}

* Fehlerkorrektur – Miniaturansichten werden nun auch bei Verwendung von Lastverteilungsservern korrekt erzeugt.

## 15.7 - Version Juli 2015  {#release-15-7---july-2015}

### Neue Funktionen {#new-capabilities-12}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Listenexport<br /> </td> 
   <td> Adobe Campaign bietet künftig die Möglichkeit, Inhalte von Listen in eine Datei im CSV-Format zu exportieren. Zugriff auf diese Funktion besteht bei allen Bildschirmen, die eine <strong>Listen</strong>-Ansicht aufweisen (beispielsweise die Profilliste).<br /> Exportiert werden die Daten der Spalten, die zum Zeitpunkt des Exports in der Liste angezeigt werden. Durch Anpassung der Listenkonfiguration können so die zu exportierenden Daten ausgewählt werden.<br /> Weiterführende Informationen finden Sie im <a href="../../automating/using/exporting-lists.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integration mit Adobe Profiles &amp; Audiences<br /> </td> 
   <td> Es ist künftig möglich, freigegebene Zielgruppen der Adobe Marketing Cloud in Adobe Campaign zu nutzen und Audiences aus Adobe Campaign für die Nutzung in der Marketing Cloud freizugeben:<br /> 
    <ul> 
     <li> Export: Bei der Speicherung einer aus Profilen bestehenden Audience im Rahmen eines Workflows bietet die Option <span class="uicontrol">In der Adobe Marketing Cloud freigeben</span> nun die Möglichkeit, die Profile einer existierenden Zielgruppe hinzuzufügen oder eine neue Zielgruppe zu erstellen. </li> 
     <li> Import: Im Bildschirm zur Audience-Verwaltung ist es bei der Erstellung einer Audience vom Typ <strong>Liste</strong> nun möglich, diese als <span class="uicontrol">Zielgruppe der Adobe Marketing Cloud</span> zu kennzeichnen . Dies ermöglicht die Auswahl einer existierenden freigegebenen Zielgruppe und deren Import in Adobe Campaign. </li> 
    </ul> Weiterführende Informationen zur Konfiguration und Verwendung dieser Funktion finden Sie im <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Digital Content Editor - Dynamische Inhalte<br /> </td> 
   <td> Die Bedieneroberfläche zur Verwaltung dynamischer Inhalte wurde verbessert. Pfeile ermöglichen es nun, direkt im Nachrichtenkörper von einem dynamischen Inhalt zum nächsten zu wechseln.<br /> Weiterführende Informationen finden Sie im <a href="../../channels/using/defining-dynamic-content-in-a-landing-page.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Digital Content Editor - Dynamische Texte<br /> </td> 
   <td> Mithilfe des Inhaltseditors ist es nun möglich, dynamische Texte für E-Mails in verschiedenen Kontexten zu definieren:<br /> 
    <ul> 
     <li> im Betreff einer E-Mail, </li> 
     <li> im HTML-Modus, </li> 
     <li> im Textmodus. </li> 
    </ul> Weiterführende Informationen finden Sie im <a href="../../channels/using/defining-dynamic-text.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Programme und Kampagnen - Berichte<br /> </td> 
   <td> Die Bedieneroberfläche und die grafische Darstellung der Berichte wurden verbessert.<br /> Weiterführende Informationen finden Sie im <a href="../../reporting/using/defining-the-report-period.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-12}

#### Installation {#installation}

* Namen von Adobe Campaign-Instanzen sind nun auf 32 Zeichen begrenzt.

#### Workflows  {#workflows-10}

* Fehlerkorrektur – in Workflows schlägt bei der Bearbeitung von Abfragen die Zielgruppenbestimmung bei Verwendung von Ressourcen vom Typ 'delivery' nicht mehr fehl.
* Fehlerkorrektur – in Workflow-Abfragen werden verknüpfte Ressourcen nun korrekt verarbeitet.
* Fehlerkorrektur – das Bearbeiten der Aktivität **Wiederkehrender Versand** ist nun auch dann problemlos möglich, wenn ein Workflow bereits ausgeführt wurde.

#### E-Mails  {#emails}

* Fehlerkorrektur – vor dem E-Mail-Versand ist die Überprüfung der JavaScript-Syntax nun auch bei E-Mails möglich, für die ein dynamischer Inhalt mithilfe des Ausdruckseditors definiert wurde.

#### Landingpages  {#landing-pages-6}

* Fehlerkorrektur – das Bearbeiten von Landingpages ist nun auch auf Tablets problemlos möglich.

#### Assets Core Service  {#assets-core-service}

* Bei der Auswahl von freigegebenen Assets im Rahmen der E-Mail- oder Landingpage-Bearbeitung wird die Liste der verfügbaren Assets nun für Adobe Campaign gefiltert.

## 15.6 - Version Juni 2015  {#release-15-6---june-2015}

### Neue Funktionen {#new-capabilities-13}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Workflows: Aktivität "Abstimmung"<br /> </td> 
   <td> Im Rahmen eines Workflows lässt sich mithilfe der Aktivität <strong>Abstimmung</strong> eine Verbindung zwischen z. B. nicht-identifizierten Daten aus einem Dateiimport und bereits existierenden Ressourcen herstellen.<br /> Diese Aktivität wird vor allem für Daten-Management-Zwecke verwendet. Die Aktivität dient hauptsächlich der Datenverwaltung und wird zwei bestimmten Anwendungskontexten gerecht:<br /> 
    <ul> 
     <li> <strong>Hinzufügung von Relationen</strong>: Mithilfe des Tabs <strong>Relationen</strong> lassen sich Beziehungen zwischen eingehenden Daten und mehreren Dimensionen der Adobe Campaign-Datenbank hinzufügen. </li> 
     <li> <strong>Identifizierung der Daten</strong>: Mithilfe des Tabs <strong>Identifizierung</strong> lassen sich eingehende Daten den Spalten einer bereits in der Adobe Campaign-Datenbank existierenden Dimension zuordnen. Die aus der Aktivität ausgehenden Daten werden so als der bestimmten Dimension zugehörig identifiziert. </li> 
    </ul> Weiterführende Informationen finden Sie im <a href="../../automating/using/reconciliation.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Aktivität "Dateiextraktion"<br /> </td> 
   <td> Im Rahmen eines Workflows erlaubt die neue Aktivität <strong>Dateiextraktion</strong> den Export von in Adobe Campaign enthaltenen Daten in Form von externen Dateien. <br /> Einschränkung: Es ist zum jetzigen Zeitpunkt nicht möglich, dynamische Namen für Ausgabedateien zu verwenden.<br /> Weiterführende Informationen finden Sie im <a href="../../automating/using/extract-file.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Aktivität "Planung"<br /> </td> 
   <td> Verbesserung des Widgets zur Auswahl des Ausführungszeitpunkts in der Workflow-Aktivität <strong>Planung</strong>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Aktivität "Dateiübertragung"<br /> </td> 
   <td> SFTP wird nun unterstützt.<br /> </td> 
  </tr> 
  <tr> 
   <td> Benutzerdefinierte Ressourcen<br /> </td> 
   <td> Im Menü <span class="uicontrol">Entwicklung</span> haben Benutzer mit Administratorrechten nun die Möglichkeit, das zur Verfügung gestellte Datenmodell durch benutzerdefinierte Ressourcen zu ergänzen, also beispielsweise Tabellen mit Verkaufs- oder Produktdaten zu erstellen. <br /> Darüber hinaus können native Anwendungsressourcen erweitert werden, um neue Felder hinzuzufügen.<br /> Des Weiteren ist nun die Navigation in Bildschirmen, die neuen oder erweiterten benutzerdefinierten Ressourcen entsprechen, konfigurierbar.<br /> Weiterführende Informationen finden Sie im <a href="../../developing/using/data-model-concepts.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Testprofile<br /> </td> 
   <td> Bei Testprofilen ist nun im Zuge der Testprofillisten-Konfiguration die Auswahl des <strong>Zweiten Vornamens</strong> und der <strong>Anrede</strong> möglich.<br /> </td> 
  </tr> 
  <tr> 
   <td> Inhaltseditor: dynamische Inhalte<br /> </td> 
   <td> Es besteht die Möglichkeit, multiple Inhalte zu erstellen, die in Abhängigkeit von mithilfe des Ausdruckseditors definierten Bedingungen den Benutzern dynamisch angezeigt werden.<br /> Weiterführende Informationen finden Sie im <a href="../../channels/using/defining-dynamic-content-in-a-landing-page.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> E-Mail<br /> </td> 
   <td> Die E-Mail-Versandlogs weisen nun eine <strong>Testprofil</strong>-Spalte auf.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-13}

#### Listen {#lists-1}

* Das Löschen eines Listenelements zieht nun eine automatische Aktualisierung der Liste nach sich.
* Fehlerkorrektur – Listenelemente können nun auch ausgewählt werden, wenn die Liste nur eine Spalte enthält.
* Fehlerkorrektur – Seitenaktualisierung löst keinen Verlust von Änderungen der Listenanzeige mehr aus.
* In der Testprofilliste können nun der zweite Vorname und die Anrede der Profile angezeigt werden.
* Fehlerkorrektur – in Mozilla Firefox löst die Auswahl von Checkboxen in einer Liste keinen Fehler mehr aus.

#### Audiences  {#audiences-2}

* Fehlerkorrektur – im Audience-Bildschirm ist nun die Verwendung der **[!UICONTROL Hinzufügen]**-Schaltfläche möglich.

#### E-Mails {#emails-1}

* Fehlerkorrektur – Korrektur des JavaScript-Fehlers, der bei der E-Mail-Bearbeitung die wiederholte Verwendung der Vorschau verhinderte.
* Fehlerkorrektur – auf Microsoft Surface Pro3 Tablets unter Internet Explorer 11 ist nun die Verwendung der Schaltflächen **[!UICONTROL Eigenschaften bearbeiten]** und **[!UICONTROL Testsendungen anzeigen]** möglich.
* Fehlerkorrektur – E-Mail-Versandlogs werden nun korrekt angezeigt.

#### Landingpages  {#landing-pages-7}

* Fehlerkorrektur – in Landingpages ist bei der Inhaltsbearbeitung nun die Verwendung des Inhaltsbausteins **Markenlogo** möglich.
* Fehlerkorrektur – Landingpages werden nun auch dann in der Liste der Marketingaktivitäten angezeigt, wenn in der Landingpage ein Gültigkeitsdatum angegeben ist.

#### Workflows  {#workflows-11}

* Fehlerkorrektur – bei der Konfiguration von **Segmentierungsaktivitäten** können Segmente im Gruppierungsmodus nun korrekt begrenzt werden.
* Fehlerkorrektur – die Auswahl von Transitionen ist nun auch nach der Konfiguration von **Segmentierungsaktivitäten** korrekt möglich.
* Fehlerkorrektur – das Löschen von Transitionen ist nun auch nach der Konfiguration von **Segmentierungsaktivitäten** korrekt möglich.
* Fehlerkorrektur – in **Segmentierungsaktivitäten** arbeiten Populationszählung und -vorschau nun korrekt.
* Fehlerkorrektur – das Löschen von wiederkehrenden E-Mails wird nun effektiv durchgeführt.
* Fehlerkorrektur – nach dem Löschen einer Aktivität vom Typ **Dateiübertragung** werden die darin enthaltenen Daten nicht mehr in einer neuen **Dateiübertragung** angezeigt.
* Fehlerkorrektur – in **Ausschlussaktivitäten** werden Ausschlussregeln nun korrekt berücksichtigt.
* Fehlerkorrektur – Beim Löschen einer E-Mail-Versand-Aktivität in einem Workflow tritt kein Fehler mehr auf. Die entsprechenden Sendungen werden jetzt auch aus der Liste der Marketingaktivitäten entfernt.

#### Navigation  {#navigation}

* Die fortlaufende Navigation von einem Feld zum nächsten auf ein und derselben Seite ist nun mithilfe der Tabulatortaste möglich.

## 15.4 - Version April 2015  {#release-15-4---april-2015}

### Neue Funktionen {#new-capabilities-14}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Package-Import und -Export<br /> </td> 
   <td> Im Menü <strong>Freigabe</strong> können Benutzer mit Administratorrechten nun mithilfe des Package-Imports und -Exports Ressourcen zwischen verschiedenen Adobe Campaign-Instanzen austauschen.<br /> Weiterführende Informationen finden Sie im <a href="../../automating/using/managing-packages.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Berichte<br /> </td> 
   <td> Alle Berichte (außer <strong>Klicks</strong>) stehen nun auch auf Programmniveau zur Verfügung. Hierbei handelt es sich um folgende Berichte:<br /> 
    <ul> 
     <li> Versanddurchsatz bezogen auf das Programm </li> 
     <li> Trackingindikatoren bezogen auf das Programm </li> 
     <li> Verteilung nach Domain bezogen auf das Programm </li> 
     <li> Fehler und Bounces bezogen auf das Programm </li> 
     <li> URLs und Clickstreams bezogen auf das Programm </li> 
    </ul> Die Berichte können für bestimmte Zeiträume abgerufen werden (z. B. drei Monate, sechs Monate etc.). Kampagnenberichte können auf die gleiche Weise gefiltert werden.<br /> Weiterführende Informationen finden Sie im <a href="../../reporting/using/about-dynamic-reports.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Aktivität <strong>E-Mail-Versand</strong><br /> </td> 
   <td> Die <strong>E-Mail-Versand</strong>-Aktivität wurde verbessert. Über diese Aktivität erstellte E-Mails, wiederkehrende E-Mails sowie Ausführungen wiederkehrender E-Mails können nun über die Marketingaktivitätenliste der Anwendung abgerufen werden.<br /> Weiterführende Informationen finden Sie im <a href="../../automating/using/email-delivery.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Aktivität <strong>Segmentierung</strong><br /> </td> 
   <td> Die Workflow-Aktivitäten wurden um die <strong>Segmentierung</strong> erweitert. Diese Aktivität ermöglicht ausgehend von in vorgeschalteten Workflow-Aktivitäten ermittelten Populationen die Erstellung von Segmenten und die Zuordnung von Segmentcodes. Die auf diese Weise definierten Segmente können im Anschluss an die Aktivität in einer gemeinsamen oder in unterschiedlichen Transitionen weiterverwendet werden. Jetzt sind Optionen verfügbar, mit denen Sie die Population filtern und die Größe eines jeden Segments begrenzen und damit die Personalisierung optimieren können. So können Sie beispielsweise beliebig Profile auswählen, die bestimmten Kriterien entsprechen.<br /> Weiterführende Informationen finden Sie im <a href="../../automating/using/segmentation.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integrationen: <strong>Assets Core Service</strong><br /> </td> 
   <td> Es ist nun möglich, im Inhalt von E-Mails und Landingpages freigegebene Ressourcen aus <strong>Assets Core Service</strong> zu verwenden. Diese können direkt in der Adobe Marketing Cloud verwaltet werden.<br /> Weiterführende Informationen finden Sie im <a href="../../integrating/using/working-with-campaign-and-assets-core-service.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integrationen: <strong>Adobe Target</strong><br /> </td> 
   <td> Es ist nun möglich, von <strong>Adobe Target</strong> dynamisch berechnete Bilder in Adobe Campaign-E-Mails zu verwenden. Auf diese Weise können Sie den Inhalt in Abhängigkeit von in Adobe-Target-Segmenten definierten Kriterien personalisieren und den Empfängern jeweils den bestmöglichen Inhalt präsentieren.<br /> Weiterführende Informationen finden Sie im <a href="../../integrating/using/about-campaign-target-integration.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Digital Content Editor: <strong>Blockmarkierung</strong><br /> </td> 
   <td> Bei der Markierung von Blöcken im HTML-Inhaltseditor wird nun im unteren Abschnitt des Arbeitsbereichs eine Breadcrumb-Leiste angezeigt, welche die präzise Auswahl bestimmter Elemente erleichtert.<br /> Weiterführende Informationen finden Sie im <a href="../../channels/using/managing-landing-page-structure-and-style.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## 15.3 - Version März 2015  {#release-15-3---march-2015}

### Neue Funktionen {#new-capabilities-15}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Berichte<br /> </td> 
   <td> Der Zugang zu Berichten ist künftig direkt über ein Programm oder eine Kampagne möglich. In Bezug auf Programme ist der Bericht <strong>Versandzusammenfassung</strong> hinzugefügt worden.<br /> Weiterführende Informationen finden Sie im <a href="../../reporting/using/delivery-summary.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Daten aktualisieren<br /> </td> 
   <td> In den Workflows bietet die <strong>Daten-Update</strong>-Aktivität künftig eine Funktion zur automatischen Zuordnung der eingehenden Felder zu Feldern eines Anwendungsschemas. Dies erleichtert die Auswahl der zu aktualisierenden Felder.<br /> Weiterführende Informationen finden Sie im <a href="../../automating/using/update-data.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> E-Mail-Versand<br /> </td> 
   <td> In den Workflows sind die erweiterten Optionen der <strong>E-Mail-Versand</strong>-Aktivität künftig mittels einer speziellen Schaltfläche in der Symbolleiste abrufbar. Diese Schaltfläche ist nur dann verfügbar, wenn eine <strong>E-Mail-Versand</strong>-Aktivität ausgewählt ist. Sie dient vor allem dazu, der Aktivität eine ausgehende Transition hinzuzufügen und den im Workflow angezeigten Namen der Aktivität zu ändern.<br /> Weiterführende Informationen finden Sie im <a href="../../automating/using/email-delivery.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

### Korrekturen  {#patches-14}

#### Allgemein {#general-10}

* Fehlerkorrektur – bei der Erstellung eines Versands wird die Anzeige des Empfängers nicht länger gestört.
* Fehlerkorrektur – Verwendung einer auf der 'Haben geöffnet'-Bedingung basierenden Audience ist nun möglich.
* Fehlerkorrektur – das Löschen eines leeren Profils ist nun erlaubt.
* Fehlerkorrektur – bei der Versandvorschau wird kein Fehler mehr erzeugt.
* Fehlerkorrektur – das Duplizieren einer Marketingaktivität funktioniert nun fehlerfrei.
* Fehlerkorrektur – das Löschen einer Kampagne erzeugt keinen Fehler mehr.


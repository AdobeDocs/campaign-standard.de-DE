---
title: 'Versionshinweise  '
seo-title: 'Versionshinweise  '
description: Versionshinweise
seo-description: Auf dieser Seite werden die zuletzt veröffentlichten Versionen von Adobe Campaign Standard aufgelistet.
page-status-flag: nie aktiviert
uuid: 1 cf 2 e 40 c-beca -43 db -8261-a 1820 ee 86 ad 3
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: rn
content-type: Referenz
topic-tags: campaign-standard-releases
discoiquuid: 5 c 7 bfb 74-4002-4 ffe -87 e 8-bddb 41 d 34 b 41
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f6ac14bf13433444e71d58cf677681b30f4b620f

---


# Versionshinweise  {#release-notes}

Suchen Sie eine bestimmte Version von Adobe Campaign Standard aus dem Jahr 

Mit jeder Version werden neue Funktionen und Korrekturen veröffentlicht. Klicken Sie auf eine Version, um sich den Inhalt anzusehen. In der [Releaseplanung](https://helpx.adobe.com/campaign/kb/acs-release-planning.html) können Sie sehen, wann die nächste Version veröffentlicht wird.

Sehen Sie sich [Dokumentationsaktualisierungen](../../rn/using/documentation-updates.md) für Adobe Campaign Standard an. Ältere Versionshinweise finden Sie auf diesen Seiten: [Versionshinweise 2018](../../rn/using/release-notes-2018.md), [Versionshinweise 2017](../../rn/using/release-notes-2017.md), [Versionshinweise 2015–2016](../../rn/using/release-notes-2015-2016.md). Sehen Sie sich auch die Liste der [eingestellten und entfernten Funktionen](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html) an.

## 19.3 - Version Juli 2019 {#release-19-3---july-2019}

### Neue Funktionen? {#what-s-new-3}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> External API Activity (Public Beta)<br /> </td> 
   <td> <p>Zur tieferen Personalisierung ermöglicht die externe API-Aktivität Ihnen, Daten aus externen Systemen über einen REST-API-Aufruf in einen Workflow zu übertragen. Die REST-Endpunkte können ein Kundenverwaltungssystem, Adobe I/O Runtime oder Adobe Experience Cloud REST Endpunkt (z. B. Datenplattform, Target, Analytics, Kampagne) sein.</p><p>Diese Funktion befindet sich derzeit in öffentlicher Hand.</p><p>For more information, refer to the <a href="../../automating/using/external-api.md">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/managing-processes-and-data/data-management-activities/external-api-activity.html">how-to video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Report on workflow segment<br /> </td> 
   <td> <p>Mit dieser Funktion können Marketingexperten ihre Bereitstellungsleistung nach Segmentcode aufschlüsseln. Wenn Sie einen Workflow erstellen und eine Segmentierungsaktivität verwenden, um der Auslieferungspopulation Segmente zuzuweisen, können diese Segmente nun dieselbe Auslieferung durchführen. Auf diese Weise können Sie die Statistiken zum Öffnen/Klicken auf Grundlage mehrerer Segmente innerhalb einer einzelnen Auslieferung anzeigen.</p><p>For more information, refer to the <a href="../../reporting/using/creating-a-report-workflow-segment.md">detailed documentation</a> and the <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/reporting/report-on-workflow-segments.html">how-to video</a>.</p></td>
  </tr> 
 </tbody> 
</table>

### Verbesserungen bei der Sicherheit {#security-enhancements-2}

* Es wurde ein Sicherheitsproblem behoben, durch das DOS-Angriffe (DOS) auf ungültige Anforderungen zum Abrufen von Bildern verhindert wurden. (CAMP-33454)

### Verbesserungen bei Email Designer {#email-designer-enhancements-3}

* Es wurde ein Problem behoben, durch das einer HTML-Vorlage jedes Mal, wenn eine Komponente hinzugefügt wurde, zusätzliche HTML-Stiltags hinzugefügt wurden. Dies konnte die Größe der Vorlage drastisch erhöhen. (CAMP-34694)
* Es wurde ein Problem behoben, durch das einige rechts obere Symbolleistenmenüoptionen nicht verfügbar waren. (CAMP-34577)
* Es wurde ein Problem behoben, das auftrat, wenn der Inhaltsblock der Mirror Page in einen E-Email-Inhalt eingefügt wurde. (CAMP-34779)
* Es wurde ein Problem behoben, das bei der Verwendung von JSPP-Code in einer E-Email auftrat und es schwierig machte, den Inhalt zu bearbeiten. (CAMP-34574)
* Es wurde ein Problem behoben, durch das Bilder oben abgeschnitten wurden, wenn ein Hyperlink hinzugefügt wurde. (CAMP-34382)
* Es wurde ein Problem beim Anzeigen des E-Mail-Designers mit Firefox behoben. (CAMP-34364)
* Es wurden verschiedene Probleme behoben, die beim Definieren dynamischer Inhalte in einer E-Email im erweiterten Modus aufgetreten sind. (CAMP -34351, CAMP -34333, CAMP -34331)
* Es wurden verschiedene Probleme behoben, die beim Regeleditor für dynamische Inhalte aufgetreten sind (CAMP -44304, CAMP -34303).
* Es wurde ein Problem behoben, durch das das Link-Feld nicht im Bereich "E-Mail-Designer-Einstellungen" angezeigt wurde (CAMP -33749).
* Es wurde ein Problem mit dem youtube-Symbol behoben, das in E-Emails übergrößen wurde. (CAMP-33726)
* Es wurde ein Sicherheitsproblem behoben, durch das der bearbeitbare Seiteninhalt bearbeitbar war. (CAMP-33691)
* Es wurde ein Problem behoben, durch das die HTML-Ausgabe bei Verwendung des Größer-als-Zeichen in dynamischen Inhalten abgeschnitten wurde. (CAMP-33688)
* Es wurde ein Problem behoben, das beim Bearbeiten der Option "Rückgängig" beim Bearbeiten von Text im E-Mail-Designer auftrat. (CAMP-32565)
* Es wurde ein Problem behoben, durch das zusätzliche Tags beim Rückgängigmachen der Stile statt beim Entfernen von Stilen erstellt wurden. (CAMP-32359)
* Sie können jetzt definieren, ob jede Komponente, die in einer E-Mail verwendet wird, nur auf Desktopgeräten oder nur auf Mobilgeräten angezeigt wird.
* Sie können nun die Breite und Höhe einer Social-Content-Komponente festlegen.
* Es wurde ein Fehler behoben, der verhinderte, dass dynamische Inhalte nach dem Löschen dieser dynamischen Inhalte entfernt wurden.
* Es wurde ein Fehler behoben, der dazu führte, dass der Betreff einer E-Mail nach der Änderung nicht aktualisiert wurde.
* Ein Problem wurde behoben, das eine n: n Spaltenstruktur wird einmal ausgewählt, sobald sie in der Arbeitsfläche abgelegt wurde.
* Es wurde ein Problem behoben, durch das die Miniaturansicht der Nachricht im E-Mail-Dashboard verschwommen angezeigt wurde.
* Es wurde ein Problem behoben, durch das der Hintergrund für E-Emails, die in Outlook empfangen wurden, nicht richtig angezeigt wurde.
* Es wurden einige Sortierungsprobleme auf der Homepage von E-Mail Designer behoben.
* Es wurde ein Problem behoben, das beim Duplizieren von Varianten bei Verwendung dynamischer Inhalte auftrat.
* Einige unerwünschte Felder wurden aus dem Bereich "E-Mail-Designer-Einstellungen" entfernt.

### Sonstige Verbesserungen {#other-improvements-3}

* Durch die Integration mit Adobe Experience Platform Location Services ist Adobe Campaign jetzt kompatibel, um standortbasierte Marketingmeldungen über das Experience Platform SDK an die Abonnenten Ihrer mobilen Anwendung zu senden. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md).
* Die Berichterstellungsfunktion wurde verbessert. Um diese Funktion nutzen zu können, müssen Sie die Vereinbarung zur Nutzungsnutzung für dynamische Berichte akzeptieren. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).
* In Workflows wurde eine neue Option hinzugefügt, um die nächsten zehn Ausführungen eines Arbeitsablaufs in der Vorschau anzuzeigen. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../automating/using/scheduler.md).
* In der Planer-Aktivität können Sie mit einer neuen Option einen bestimmten Tag einer bestimmten Woche für monatliche Auslieferungen auswählen. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../automating/using/scheduler.md).
* Beim Erstellen wiederkehrender Lieferungen ohne Aggregationszeitraum ermöglicht das Bereitstellungs-Dashboard jetzt die Bestätigung der Bestätigung, bevor die Auslieferung gesendet wird. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../sending/using/confirming-the-send.md).
* Sie können jetzt die Beschriftung einer Auslieferung mit Ereignisvariablen personalisieren, die in der externen Signalaktivität des Workflows deklariert wurden. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../automating/using/calling-a-workflow-with-external-parameters.md).
* Die GDPR-Löschabfrage wurde verbessert, um eine bessere Leistung zu erzielen. (CAMP-33504)
* Die Option "ftp" wurde aus der Konfigurationsoberfläche für die externe Kontokonfiguration entfernt. (CAMP-34472)
* Sie können jetzt die Option "SMTP-Testmodus" für jede E-Email aktivieren und deaktivieren. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../administration/using/configuring-email-channel.md#smtp-test-mode). (CAMP-34602)

### Sonstige Änderungen {#other-changes-2}

* In der Benutzeroberfläche der Auslieferungseigenschaften wurde eine Warnung hinzugefügt. Es gibt an, dass die Lieferungen auf der Grundlage ihres Aggregationszeitraums vorbereitet und gelöst werden, um den Arbeitsablauf mehrmals pro Tag aufzurufen. Sie sollten sicherstellen, dass sie keinen Punkt haben. (CAMP-34393)
* In benutzerdefinierten Ressourcenkonfigurationsbildschirmen wurde eine Warnung hinzugefügt. Es wird empfohlen, für benutzerdefinierte Ressourcen-IDs maximal 30 Zeichen zu verwenden. Dies gilt auch für benutzerdefinierte Ressourcenfelder, Schlüssel, Indizes und Links.
* Beim Versuch, eine Transaktionsnachricht zu löschen, die von einer Einstiegsseite als Bestätigungsmeldung verwendet wird, wird nun eine Nachricht angezeigt.
* In Workflows wird jetzt eine Warnung angezeigt, wenn eine Aktivität länger als 6 Stunden ausgeführt wurde. Dies gilt nicht für Push-Benachrichtigungen, Bereitstellung, Signal-, Start-, Ende-, Fork-, UND-, Zeitplan- und Wait-Aktivitäten.
* In Workflows wird jetzt eine Warnung angezeigt, wenn Sie die maximale Anzahl von Workflows erreichen, die gleichzeitig ausgeführt werden.
* Arbeitsabläufe, die für mehr als sieben Tage in Pause oder Fehlgeschlagen waren, werden nun gestoppt, um weniger Speicherplatz zu belegen. Die Bereinigungsaufgabe wird in den Workflow-Protokollen angezeigt.
* Bei Verwendung einer "Übertragungsdatei" -Aktivität wird jetzt ein Fehler protokolliert, wenn die Dateigröße den verfügbaren Speicherplatz überschreitet.
* Die Aktion "Zur Ziel-URL umleiten" kann nicht mehr für die sekundäre Schaltfläche in-App-Nachrichten ausgewählt werden.

### Korrekturen {#patches-3}

* Es wurde ein Fehler behoben, der dazu führte, dass GDPR-Zugriffsanforderungen fehlschlugen.
* Es wurde ein Problem behoben, durch das Auslöser verworfen werden konnten, wenn mehrere Auslöser für ein eindeutiges Profil empfangen wurden.
* Es wurde ein Problem behoben, das zu einer fehlerhaften Fehlermeldung zur benutzerdefinierten Ressourcenveröffentlichung nach der Anmeldung führen konnte.
* Es wurde ein Problem behoben, durch das beim Erstellen oder Erweitern einer benutzerdefinierten Ressource eine leere Seite angezeigt wurde.
* Es wurde ein Problem behoben, durch das eine Zielgruppe mit appsubscriptionrcp nicht als Targeting-Dimension für das Targeting bei einer mobilen Bereitstellung verfügbar war.
* Es wurde ein Fehler behoben, der verhinderte, dass keine E-Mail-Adressen der harten Absprünge in Quarantäne gestellt wurden. (CAMP-24587)
* Es wurde ein Problem behoben, das auftrat, wenn eine Typologie hinzugefügt und anschließend gelöscht wurde, bevor die Typologie gespeichert wurde. (CAMP-32789)
* Es wurde ein Problem behoben, durch das Einstiegsseiteninhalte beim Deaktivieren dynamischer Inhalte nicht angezeigt wurden. (CAMP-32924)
* Es wurde ein Problem mit wiederkehrenden Auslieferungen behoben, das bei der Verwendung der Personalisierung für die Attribute einer Master-Auslieferung auftrat. (CAMP-32983)
* Es wurde ein Problem in Workflows behoben, durch das Ergebnisse aus einem Übergang mit eingehenden SMS-Nachrichtendaten nicht gelesen werden konnten. (CAMP-33134)
* Es wurde ein Problem in Workflows behoben, das beim Kombinieren von Gabeseiten und Ausschlussaktivitäten zur Erstellung von Zielgruppen auftrat. (CAMP-33401)
* Es wurde ein Fehler behoben, der dazu führte, dass Seiteninhalte nicht angezeigt wurden und keine Bestätigungen für wiederkehrende Lieferungen gesendet wurden. (CAMP-33413)
* Es wurde ein Fehler behoben, der zu einem Fehler führte, wenn eine Union-Aktivität zwischen Profilen und Zielgruppen verwendet wurde. Dieses Problem wurde durch eine Inkompatibilität der Identifizierungsschlüssel in Eingabeübergängen verursacht. (CAMP-33713)
* Es wurde ein Fehler in den Test-Aktivitäten behoben, der verhinderte, dass der Ausdruck "reccount" die korrekte Syntax beim Doppelklick verwendet. (CAMP-33756)
* Es wurde ein Problem behoben, das zu einer Fehlermeldung führte, wenn beim Öffnen des technischen Arbeitsablaufs für die Rechnungsstellung eine Fehlermeldung geöffnet wurde. (CAMP-34313)
* Es wurde ein Problem in Einstiegsseiten behoben, das beim Konfigurieren von Kontrollkästchen-Feldern mit Abonnements auftrat. (CAMP-34369)
* Es wurde ein Problem behoben, das auftrat, wenn eine Liste konfiguriert und das Symbol "Symbol" hinzugefügt wurde. (CAMP-34585)
* Es wurde ein Problem behoben, durch das die Verwendung des|" und " %"-Symbole als Datums- oder Uhrzeittrennzeichen in den Aktivitäten des Ladens von Datei-Workflows. (CAMP-34706)
* Es wurde ein Problem behoben, das bei der Verwendung von Sichtbarkeitsbedingungen mit Kontrollkästchen in Einstiegsseiten auftrat. (CAMP-34802)
* Es wurde ein Fehler in der Anreicherungsaktivität behoben, der verhinderte, dass Felder auf der Registerkarte "Zusätzliche Daten" angezeigt wurden, wenn die Filterdimension auf Tracking-Protokolle und die Zieldimension auf Profil eingestellt war.
* Es wurde ein Fehler behoben, der zu einer Fehlermeldung führte, wenn eine Ressource "workflowtemplate" exportiert wurde.
* Es wurde ein Problem beim Erstellen eines neuen Profils behoben, das verhinderte, dass das Feld "Land/Region" gespeichert wurde, wenn es im Dialogfeld ausgewählt wurde.
* Es wurden verschiedene Probleme behoben, die bei Verwendung der Direct Mail-Importvorlage (updatequarantinesdeliverylogsdirectmail) auftraten.
* Es wurde ein Problem mit der Integration von Assets on Demand behoben.
* Es wurde ein Problem behoben, das beim Einzoomen in der Zeitschienenansicht auftrat. (CAMP-33628)
* Es wurde ein Problem behoben, durch das Proofs nicht sofort für E-Mail-Nachrichten mit geplanten Datum und Uhrzeit gesendet werden konnten. (CAMP-33723)
* Es wurde ein Fehler im Zusammenhang mit Transaktionsmessaging behoben, der Fehlerprotokolle verursachte, wenn ein Benutzer abgemeldet wurde. (CAMP-31698)
* Es wurde ein Fehler behoben, der beim Planen einer E-Mail in bestimmten Umgebungen auftrat.
* Es wurde ein Fehler behoben, der dazu führte, dass der Arbeitsablauf für die Bereitstellung von Bereitstellungen aktualisieren fehlschlug.
* Es wurde ein Sicherheitsproblem behoben, das den E-Mail-Inhalt beschädigte, wenn der Betreff mehrere Zeilen enthielt.


## 19.2.7 - Version Juli 2019 {#release-19-2-7---july-2019}

### Neuheiten {#improvements-2}

* Die GDPR-Löschabfrage wurde verbessert, um eine bessere Leistung zu erzielen.
* Es wurde ein Problem behoben, durch das nach dem Upgrade 19.2 ein Web-Absturz verursacht wurde. (CAMP-34862)
* Es wurde ein Problem behoben, durch das Nicht-Administratoren Berichte speichern oder planen konnten. (CAMP-31133)
* Korrektur eines Problems bei der Verwendung von "|" als Datumstrennzeichen in der Workflow-Arbeitsablaufaktivität. (CAMP-34706)

## 19.2.4 - Version Juni 2019 {#release-19-2-4---june-2019}

### Email Designer {#email-designer-2}

* Es wurde ein Problem behoben, durch das Benutzer keine Fragmente bearbeiten konnten, wenn leere style-Tags im HTML-Code verwendet wurden. Dies ist eine Folgekorrektur von CAMP-33778 in Version 19.2.3.

## 19.2.3 - Version Juni 2019 {#release-19-2-3---june-2019}

### Email Designer {#email-designer-1}

Eine Reihe von Verbesserungen und Korrekturen wurde implementiert, um die Verwendung von Fragmenten in Version 19.2 zu optimieren. Neu erstellte Fragmente funktionieren fehlerlos. Früher erstellte Fragmente werden grau dargestellt und müssen in das neue Format migriert werden. Klicken Sie dazu auf jedes Fragment und bestätigen Sie seine Migration in das neue Format. Wir empfehlen Ihnen, einige Fragmente zu testen, bevor Sie alle migrieren.

* Fehlerkorrektur – Fragmente können jetzt bearbeitet werden, nachdem sie entsperrt wurden. Dieses Problem bestand bei vorhandenen Fragmenten bei der Aktualisierung auf Version 19.2. (CAMP-33778)
* Fehlerkorrektur – Die Verwendung von dynamischen Inhalten funktioniert jetzt einwandfrei. Zum HTML-Code wurden zusätzliche Leerzeichen hinzugefügt.

### Sonstige Verbesserungen {#other-improvements-2}

* Fehlerkorrektur – Der SMS-Versand kann jetzt fortgesetzt werden, nachdem die Verbindung des SMS-Connectors unterbrochen wurde.
* Fehlerkorrektur – SMPP-Verbindungen werden jetzt nicht mehr geschlossen, wenn TLS aktiviert ist.
* Fehlerkorrektur – SMPP-Verbindungen werden jetzt nicht mehr geschlossen, wenn TLS aktiviert ist.
* In Campaign wurde die Option "Launch_URL_Campaign" hinzugefügt, um Eigenschaften von Apps zu verwalten, die mit dem Mobile SDK von Adobe Experience Platform erstellt wurden.
* Fehlerkorrektur – Die Sandbox-Umgebungs-Option wird nicht mehr deaktiviert, wenn das Zertifikat einer neu erstellten mobilen Eigenschaft hochgeladen und die Eigenschaftenseite der App geschlossen wird.
* Fehlerkorrektur – Der Inhalt einer Transaktionsnachricht kann jetzt mit Daten aus der Dienst-Ressource angereichert werden. (CAMP-33707)
* Fehlerkorrektur – Landingpages werden jetzt nicht mehr auf die Blacklist gesetzt, wenn Profile von einem Dienst abgemeldet werden.

## 19.2 - Version Mai 2019 {#release-19-2---may-2019}

### Neue Funktionen? {#what-s-new-}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Control Panel<br /> </td> 
   <td> <p>Mit dem Control Panel können Sie Administratoraufgaben effizienter erledigen. So ermöglicht es Ihnen, die Serverkapazität zu überwachen und die Einstellungen der Instanzen zu verwalten (u. a. der SFTP-Server).</p><p>For more information, refer to the <a href="https://helpx.adobe.com/campaign/kb/control-panel.html">detailed documentation</a> and the <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-control-panel-video-use.html">how-to video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Lokale Benachrichtigungen<br /> </td> 
   <td> <p>Mit lokalen Benachrichtigungen können Sie Benutzer informieren, wenn neue Daten in deren Apps verfügbar sind, selbst wenn kein Internetzugang vorhanden oder die App nicht aktiv ist. Ausgelöst werden lokale Benachrichtigungen von einer App. Der Auslöser erfolgt zu einem bestimmten Zeitpunkt durch ein bestimmtes Ereignis.</p><p>Lesen Sie für weiterführende Informationen das <a href="../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type">entsprechende Handbuch</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Verbesserung bei Workflows – Hinzufügen einer Payload zur Aktivität "Externes Signal"<br /> </td> 
   <td> <p>Starten Sie Workflows nun mit Payloads, wenn zuvor definierte Bedingungen eines anderen Workflows oder eines REST-API-Aufrufs erfüllt sind. Letzteres ermöglicht Ihnen die Integration mit Ihren externen Systemen. Gleichzeitig stellen wir die neue <strong>Test</strong>-Aktivität zur Verfügung, mit der diese Funktion getestet werden kann.</p><p>For more information, refer to the <a href="../../automating/using/calling-a-workflow-with-external-parameters.md">detailed documentation</a> and the <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-external-signal-activity-feature-video-use.html">how-to video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Verbesserung bei Landingpages – Google reCAPTCHA<br /> </td> 
   <td> <p>Mit Google reCAPTCHA können Sie Spam auf Ihren Landingpages vermeiden, ohne dass Sie Ihre Kunden zu entsprechenden Handlungen auffordern müssen.</p><p>Lesen Sie für weiterführende Informationen das <a href="../../channels/using/designing-a-landing-page.md#setting-google-recaptcha">entsprechende Handbuch</a>.</p></td> 
  </tr> 
 </tbody> 
</table>

### Verbesserungen bei der Sicherheit {#security-enhancements}

* Fehlerkorrektur – Ein potenzielles Sicherheitsproblem mit Clickjacking im Reporting-Arbeitsbereich wurde behoben.

### Verbesserungen bei Email Designer {#email-designer-enhancements}

* Fehlerkorrektur – Bei der Verwendung duplizierter Fragmente im Email Designer tritt kein Fehler mehr auf. (CAMP-33193)
* Fehlerkorrektur – Jetzt werden bei der Verwendung von Inline-Elementen in der Email Designer-Benutzeroberfläche keine unerwünschten Leerzeichen mehr erzeugt. (CAMP-32163)
* Fehlerkorrektur – Zusätzliche HTML-Tag-Attribute, die vom Benutzer nach dem Speichern von E-Mail-Inhalten im Email Designer hinzugefügt wurden, werden jetzt nicht mehr gelöscht. (CAMP-32162)
* Fehlerkorrektur – Jetzt wird im Email Designer im HTML-Modus kein Microsoft-Office-Tag mehr angezeigt, nachdem es entfernt wurde. (CAMP-32141)
* Wenn Sie eine E-Mail in einer veralteten Version von Email Designer erstellt haben, werden Sie jetzt beim Öffnen dieses E-Mail-Inhalts aufgefordert, ein Update auf die aktuelle Version durchzuführen. (CAMP-31529)
* Fehlerkorrektur – Bilder in einer mit Email Designer erstellten E-Mail werden jetzt nicht mehr verzerrt dargestellt, wenn sie an gewisse Messaging Clients gesendet werden. (CAMP-31407)
* Fehlerkorrektur – Elemente wie Listen und Schaltflächen werden jetzt im Nur-Text-Modus korrekt dargestellt, wenn sie im HTML-Modus erstellt wurden. (CAMP-32582, CAMP-32542)
* Fehlerkorrektur – Jetzt können mehr als 50 Organisationseinheiten in einer Inhaltsvorlage oder in Fragmenteigenschaften dargestellt werden. (CAMP-32932)
* Fehlerkorrektur – Beim Empfang in Outlook einer mit Email Designer erstellten E-Mail tritt jetzt kein Fehler mehr mit der Viewport-Hintergrundfarbe auf. (CAMP-31402)
* Fehlerkorrektur – Mit Email Designer erstellte E-Mail-Inhalte sind jetzt responsiv, wenn sie in Outlook geöffnet werden. (CAMP-31400)
* Fehlerkorrektur – Dynamische Inhalte im Betreff einer E-Mail funktionieren jetzt fehlerfrei. (CAMP-32837)
* Fehlerkorrektur – Jetzt tritt kein durch inkorrekte Escape-Sequenzen bedingter Fehler mehr mit E-Mail-Betreffs auf.
* Fehlerkorrektur – Fragmente können jetzt im Email Designer in die linke Palette geladen werden.
* Fehlerkorrektur – Fragmente, die während der Inhaltsbearbeitung von E-Mails erstellt wurden, werden jetzt nach der Aktualisierung der Fragmentliste im Email Designer in der linken Palette dargestellt.
* Fehlerkorrektur – Bei der Verwendung von dynamischen Inhalten in einer E-Mail treten jetzt keine Fehler mehr auf.
* Fehlerkorrektur – Farben mit RGB-Werten können jetzt in der Farbauswahl definiert werden.
* Fehlerkorrektur – Die Mirrorseite ist jetzt responsiv, wenn die E-Mail auf einem Mobiltelefon empfangen wird.

### Verbesserungen bei Transaktionsnachrichten {#transactional-messaging-enhancements}

Am Transaktionsnachrichten-Kanal wurden mehrere Verbesserungen durchgeführt, um seine Funktionsweise und Leistung zu optimieren.

* Die Dauer von Transaktionsnachrichten wurde verlängert, damit alle Nachrichten gesendet werden können, bevor sie ihre Gültigkeit verlieren, insbesondere wenn der Vorgang wiederholt wird.
* Die Leistung von Transaktionsnachrichten wurde erhöht, indem die Last auf unterschiedliche Versand-Threads aufgeteilt wurde.
* Der Versand von Transaktionsnachrichten wurde optimiert, damit gleichzeitig mehrere Analysen derselben Nachricht durchgeführt werden können.
* Fehlerkorrektur – Durchsatz und Latenz bei Transaktions-Push-Benachrichtigungen sind jetzt einheitlich.
* Fehlerkorrektur – Beim Versand von Transaktionsnachrichten wird jetzt die korrekte Zielgruppe angezeigt.
* Fehlerkorrektur – Beim Import eines Packages mit einer Ereigniskonfiguration und der zugehörigen Transaktionsnachricht tritt jetzt kein Fehler mehr auf. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../channels/using/about-transactional-messaging.md#exporting-and-importing-transactional-messages).
* Fehlerkorrektur – Jetzt werden keine Kollektionsdaten mehr aus den Testprofilen gelöscht, die für eine Transaktionsnachricht mit Produktlisten erstellt wurden.

### Sonstige Änderungen {#other-changes}

* Zum externen SMS-Konto wurde eine neue Option hinzugefügt. Hiermit kann die maximale Anzahl der für den SMS-Versand verantwortlichen MTA-Prozesse beschränkt werden, um die Anzahl der parallelen Verbindungen besser steuern zu können. Weiterführende Informationen dazu finden Sie in der Technote zum [SMS-Schnittstellenprotokoll und dessen Konfiguration](https://helpx.adobe.com/campaign/kb/sms-connector-protocol-and-settings.html).
* Wird jetzt eine Ressource mit einer API-Erweiterung publiziert, deren API zuvor bereits publiziert wurde, wird diese API jedes Mal automatisch aktualisiert, wenn sie erneut publiziert wird. Früher musste diese Aktion manuell durchgeführt werden. Wurde die API nicht aktualisiert, konnte ein Fehler in den Profil- oder Service-Ressourcen dieser API auftreten. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension).
* In dynamischen Berichten wurde die Postleitzahl-Dimension entfernt. Verwenden Sie stattdessen die Dimensionen "Stadt", "Land" und "Bundesland".
* Der Lebenszyklus-Ereignistrigger "Erster Start" für In-App-Nachrichten wurde entfernt.
* Wird ein Package mit Sicherheitsgruppen exportiert, enthält es jetzt die den Gruppen zugewiesenen Rollen. (CAMP-32960)
* Eine neue Option ermöglicht Ihnen, in der Aktivität "Datei laden" zu prüfen, ob die Spalten der zu ladenden Datei zur Spaltendefinition passen. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../automating/using/load-file.md). (CAMP-32229)
* Workflows können jetzt mit einer Payload gestartet werden, wodurch externe Parameter für mehrere Aktivitäten innerhalb eines Workflows gemeinsam verwendet werden können. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../automating/using/calling-a-workflow-with-external-parameters.md). (CAMP-29412 &amp; CAMP-29413)
* Campaign Standard-APIs ermöglichen Ihnen jetzt, die geografischen und Organisationseinheiten von Profilen mithilfe einer Payload zu aktualisieren. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html).
* Die Fehlernachrichten, die angezeigt werden, wenn der Zugriff auf ein Datenbankobjekt nicht möglich ist, sind jetzt besser verständlich.
* In der Dateiextraktionsaktivität wurden die Javascript-Funktionen zur Definition des Namens einer zu exportierenden Datei aktualisiert. Im Ausgabefeld ist jetzt nur die formatDate-Funktion verfügbar. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../automating/using/extract-file.md).
* Der Mechanismus zur Kennungserzeugung für benutzerdefinierte Ressourcen wurde verbessert. Primärschlüssel für neue benutzerdefinierte Ressourcen sind jetzt standardmäßig 64 Bit lang.
* Der Testmodus für die Publikation von benutzerdefinierten Ressourcen wurde verbessert. Jetzt wird Benutzern eine Warnung angezeigt, wenn die letzte Publikation einer benutzerdefinierten Ressource fehlgeschlagen ist und noch nicht korrigiert wurde. Wenn die Publikation einer benutzerdefinierten Ressource fehlschlägt, können Sie zur letzten funktionierenden Version zurückkehren. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).
* Zur Dateiübertragungsaktivität wurde eine neue Option hinzugefügt. Damit können Sie im SFTP-Modus bei der Verwendung des Dateidownloads die Dateien sortieren. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../automating/using/transfer-file.md). (CAMP-33109)

### Korrekturen {#patches}

* Fehlerkorrektur – Jetzt tritt beim MTA kein Speicherleck mehr auf, wenn SMS-Einstellungen neu geladen werden.
* Fehlerkorrektur – Datenbankaktualisierungen können jetzt im Reparaturmodus publiziert werden.
* Fehlerkorrektur – Jetzt treten zwischen Berichten in Adobe Analytics und dynamischen Berichten in Adobe Campaign keine Abweichungen mehr auf. (CAMP-25393)
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr im Berichtfreigabe-Workflow auf.
* Fehlerkorrektur – Benutzer können jetzt In-App-Nachrichten mit einer Medien-URL senden.
* Fehlerkorrektur – Jetzt werden Apps nur mehr dann angezeigt, wenn ihr Zertifikat zur Instanz hochgeladen wurde.
* Fehlerkorrektur – Jetzt funktionieren Personalisierungsfelder, wenn die Vorlage **Alle Nutzer einer Mobile App auswählen** verwendet wird.
* Neue Campaign Standard-Instanzen wurden bereitgestellt. (CAMP-32635 &amp; CAMP-32344)
* Fehlerkorrektur – Die Datumsformel in einem Workflow kann jetzt angepasst werden. (CAMP-30336)
* Fehlerkorrektur – Bei der Definition einer benutzerdefinierten Datumsformel sind in der Dropdown-Liste jetzt die Felder "Zusatzdaten" und "Segmentcode" verfügbar. (CAMP-32383)
* Fehlerkorrektur – Verschlüsselte zurückgewiesene Datensätze können jetzt mit den Aktivitäten "Dateiübertragung" und "Dateiextraktion" gefunden werden. (CAMP-32377)
* Fehlerkorrektur – In APIs zeigen jetzt die lineCount-Filter die exakte Gesamtzahl an. (CAMP-31424)
* Fehlerkorrektur – In Landingpages wird in Eingabefeldern jetzt der aktualisierte Wert angezeigt, nachdem dieser geändert wurde. (CAMP-31401)
* Fehlerkorrektur – Jetzt wird die Signalaktivität nicht mehr unerwartet aktiviert.
* Fehlerkorrektur – Die E-Mail-Vorschau wird jetzt auch dann angezeigt, wenn die Zielgruppe leer ist.
* Fehlerkorrektur – In der Aktivität "Dateiextraktion" wird jetzt keine Datei mehr erstellt, wenn die Option "Keine Datei erstellen, wenn die eingehende Transition leer ist" aktiviert ist.
* Fehlerkorrektur – Der Zustellbarkeits-Workflow wird jetzt nicht mehr deaktiviert, wenn er nicht erfolgreich beendet wurde.
* Fehlerkorrektur – Benutzer können jetzt Berichte speichern und planen. (CAMP-31133)

## 19.1.3 - Version März 2019 {#release-19-1-3---march-2019}

### Verbesserungen bei Email Designer {#email-designer-enhancements-1}

* Fehlerkorrektur – Eine Vorlage kann jetzt auch nach dem Speichern verändert werden.
* Fehlerkorrektur – Jetzt treten keine Fehler mehr auf, wenn eine zuvor erstellte Vorlage in einer E-Mail verwendet wird.
* Fehlerkorrektur – Komponenten können jetzt in importierten Vorlagen verborgen werden.

### Sonstige Verbesserungen {#other-improvements}

* Fehlerkorrektur – Bei der Ansicht von Typologieregeln tritt jetzt kein Fehler mehr auf. (CAMP-32059 &amp; CAMP-31849)
* Fehlerkorrektur – Typologieregeln können jetzt bearbeitet werden. (CAMP-31750)
* Fehlerkorrektur – Der inMail-Vorgang hält jetzt nicht mehr unerwartet an. (CAMP-31238)

## 19.1 - Version Februar 2019 {#release-19-1---february-2019}

### Neue Funktionen? {#what-s-new--1}

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Verbesserungen bei Push-Kanal-Berichten<br /> </td> 
   <td> <p>Bei Berichten für den Push-Kanal wurden mehrere Verbesserungen vorgenommen, damit die Benutzerinteraktion intuitiver gemessen werden kann. In dieser Version werden drei unterschiedliche Metriken für Push-Kanäle eingeführt: Impressionen, Klicks, Öffnungen (App-Öffnungen). Damit können Benutzerinteraktion mit Push-Benachrichtigungen effizienter gemessen und analysiert werden. Gleichzeitig wurden auch die Definition und Implementierung dieser Metriken standardisiert. Darüber hinaus wurde der Bericht zu Push-Benachrichtigungen durch visuelle Darstellungen und Metriken verbessert.</p><p> Lesen Sie für weiterführende Informationen das <a href="../../reporting/using/push-notification-report.md">entsprechende Handbuch</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Launch-Integration für Mobile App<br /> </td> 
   <td> <p>Diese Version beinhaltet die Integration von Adobe Campaign mit den allgemein verfügbaren Versionen von Android- und iOS-Erweiterungen für Adobe Campaign Standard in Adobe Experience Platform Launch und Mobile SDKs. Diese Erweiterungen unterstützen Push-Benachrichtigungen, In-App-Benachrichtigungen und Mobile-App-Profilaktualisierungen.</p><p> Lesen Sie für weiterführende Informationen das <a href="../../administration/using/about-typology-rules.md#typology-rules">entsprechende Handbuch</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Mobile In-App-Nachrichtenversand<br /> </td> 
   <td> <p>Diese Version enthält die allgemein verfügbare Version der In-App-Kanal-Option in Campaign. Die wichtigsten neuen Funktionen gegenüber der Beta-Version sind dynamische Berichte für den In-App-Kanal und der sichere Handshake zwischen Mobile SDK und MCIAS (Marketing Cloud In-App Messaging Service, der die In-App-Regeln zum SDK weiterleitet). Der sichere Handshake gewährleistet, dass die personenbezogenen Daten Ihrer Benutzer nicht in betrügerische Hände gelangen können. Außerdem können Sie damit Benutzerdaten auf einem gemeinsam genutzten Gerät schützen, da der Nachrichten-Cache jedes Mal geleert wird, wenn sich der Benutzer abmeldet.</p><p>Weiterführende Informationen finden Sie im <a href="../../channels/using/about-in-app-messaging.md">entsprechenden Handbuch</a> und im <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-in-app-message-tutorial.html">In-App-Tutorial</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Workflow-Verbesserungen<br /> </td> 
   <td> <p>Die folgenden Workflow-Funktionen wurden hinzugefügt:</p> 
    <ul> 
     <li> Jetzt ist es möglich, Aktivitäten innerhalb eines Workflows oder in einen anderen Workflow in derselben Campaign-Instanz per Copy &amp; Paste zu verschieben. Auf diese Weise können Sie einfach einen ganzen Workflow oder einzelne Aktivitäten duplizieren, während Sie die ursprünglich definierten Einstellungen beibehalten. Lesen Sie für weiterführende Informationen das <a href="../../automating/using/workflow-interface.md#duplicating-workflow-activities">entsprechende Handbuch</a>. (CAMP-20014) </li> 
     <li> Bei der Verwendung der Aktivität <strong>Datei laden</strong> können Sie jetzt einen Zeitstempel zum Namen der Datei hinzufügen, die die zurückgewiesenen Datensätze enthält. Lesen Sie für weiterführende Informationen das <a href="../../automating/using/load-file.md#configuration">entsprechende Handbuch</a>. </li> 
     <li> Bei den Aktivitäten <strong>Abfrage</strong> und <strong>Segmentierung</strong> kann jetzt eine ausgehende Transition erzeugt werden, wenn durch die Aktivitäten keine Daten abgerufen werden. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Verbesserungen bei der Sicherheit {#security-enhancements-1}

* Der erzeugte Landingpage-HTML-Code wurde aktualisiert, sodass er jetzt die Indexierung durch Suchmaschinen verhindert.

### Verbesserungen bei Email Designer {#email-designer-enhancements-2}

* Es wurden vier von Behance Künstlern designte, responsive E-Mail-Vorlagen hinzugefügt.

   Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../start/using/about-templates.md#content-templates).

* Unser neues On-Boarding ermöglicht Ihnen eine raschere E-Mail-Erstellung und einfacheren Zugriff auf Handbücher und Tutorials.

   Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../designing/using/about-email-content-design.md#email-designer-home-page).

* Jetzt können Sie die Anzahl und Breite von Spalten nach Belieben konfigurieren.

   Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../designing/using/defining-the-email-structure.md#editing-the-email-structure).

* Wenn Sie in der Mobile-Ansicht arbeiten, können Sie nun bestimmte Komponenten für diese Ansicht verbergen, um so den Platz optimal zu nutzen.

   Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../designing/using/about-email-content-design.md#switching-to-mobile-view).

* Sie können jetzt zusätzlich zu den bereits verfügbaren Kanälen auch benutzerdefinierte Social-Media-Kanäle zu Ihrer E-Mail-Vorlage hinzufügen.
* Fehlerkorrektur – Jetzt können Sie im Strukturmenü hinunterscrollen, wenn mehr als 18 Strukturen verwendet werden. (CAMP-31173)
* Fehlerkorrektur – Der Preheader wird nicht mehr oberhalb des Inhalts angezeigt, wenn eine mit Adobe Campaign gesendete E-Mail, die einen Preheader enthält, weitergeleitet wird. (CAMP-30736)
* Fehlerkorrektur – Die Betreffzeile kann jetzt aktualisiert werden, wenn die Option zum **Aktualisieren von AEM-Inhalt** ausgewählt wird, nachdem der Betreff in Adobe Experience Manager geändert wurde. (CAMP-29984)
* Fehlerkorrektur – Dynamische Bilder von Adobe Target können jetzt verwendet werden.
* Fehlerkorrektur – Die Vorschau wird jetzt in der Vorbereitungsphase korrekt aktualisiert, auch wenn der abgerufene Inhalt zuvor über eine URL importiert wurde.
* Zur Inhaltskomponente **Social** wurde das YouTube-Symbol hinzugefügt.
* Inhaltskomponenten und Fragmente können jetzt in der Email-Designer-Palette als **Liste** angezeigt werden.

### Sonstige Verbesserungen {#other-improvements-1}

* Adobe Campaign ist jetzt im Zusammenhang mit sowohl SDK-V4- als auch AEP-SDK-Apps vollständig FCM-konform.
* Adobe Campaign unterstützt Push-Benachrichtigungen unter Wear OS von Android sowie watchOS von Apple.
* Warn- und Fehlermeldungen, die bei der Navigation in der Benutzeroberfläche auftreten können, wurden verständlicher gestaltet.
* Jetzt können zur Profilliste Spalten für Opt-in und Opt-out hinzugefügt werden (Felder für "Kontaktieren Sie mich nicht mehr…").
* Die Zeitzonen-Dropdown-Liste auf dem Profilerstellungs-Bildschirm wurde aus dem Adressbereich in den oberen Bereich des Bildschirms verschoben.
* Jetzt können bei der Konfiguration von benutzerdefinierten Ressourcen-Bildschirmen Trennlinien hinzugefügt werden, sodass Felder in Kategorien zusammengefasst werden können.

   Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../developing/using/configuring-the-screen-definition.md#defining-the-detail-screen-configuration).

### Sonstige Änderungen {#other-changes-1}

* Adobe Campaign und Adobe Experience Cloud stellen mit Campaign Standard Release 19.2 (Frühling 2019) den Support für Microsoft Internet Explorer 11 ein. Bitte wechseln Sie zu Microsoft Edge oder einem anderen unterstützten Browser. Näheres dazu finden Sie auf der Seite der [eingestellten und entfernten Funktionen](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html).
* Das Feld **Ländercode** in der Profilressource wurde in **Länder-/Regionscode** umbenannt.

### Korrekturen {#patches-1}

* Fehlerkorrektur – Eine Nachricht kann jetzt auch dann gesendet werden, wenn ein Testprofil zu einer E-Mail-Transaktionsnachricht hinzugefügt wird. (CAMP-29854)
* Fehlerkorrektur – Der Nachrichtenversand auf anderen Kanälen ist jetzt nicht mehr verlangsamt, wenn der Versand in allen Kanälen gleichzeitig gestartet wird und auf einem Kanal langsam ist.
* Fehlerkorrektur – Der MTA beginnt jetzt nicht mehr mit dem Versand von SMS-Nachrichten, wenn die externe Kontoverbindung noch nicht aufgebaut wurde.
* Fehlerkorrektur – Bei der Ausführungsfrequenz und der Startzeit der Planungsaktivität tritt jetzt kein Fehler mehr auf. (CAMP-30745)
* Fehlerkorrektur – Bei der Verwendung von erweiterten Profilressourcen tritt bei der PKEY-Erstellung jetzt kein Fehler mehr auf. (CAMP-30285)
* Fehlerkorrektur – Bei auf Kalendertagen basierenden Ermüdungsregeln tritt jetzt kein Fehler mehr auf. (CAMP-30136)
* Fehlerkorrektur – Beim Zugriff auf benutzerdefinierte Ressourcen mit Namen, die auf "Base" enden, tritt jetzt kein Fehler mehr auf. (CAMP-30109)
* Fehlerkorrektur – Jetzt kann ein PATCH-Aufruf verwendet werden, um ein Profil für einen Dienst anzumelden. (CAMP-29728)
* Fehlerkorrektur – Der Import einer XML-Datei mit der Datei-laden-Aktivität führt jetzt nicht mehr zu Fehlern im Workflow. (CAMP-29208 und CAMP-28205)
* Fehlerkorrektur – Beim Verknüpfen von benutzerdefinierten Ressourcen können jetzt Relationen mit umgekehrter Kardinalität erstellt werden. (CAMP-30476)
* Fehlerkorrektur – Jetzt können Versandlogs erweitert werden, auch wenn Segmentcodes verwendet werden.
* Fehlerkorrektur – Bei der Verwendung der Dateitransfer-Aktivität in Workflows werden keine Zeilen mehr dupliziert.
* Fehlerkorrektur – Terminierte Berichte können jetzt zum geplanten Zeitpunkt versendet werden.
* Fehlerkorrektur – Jetzt treten keine Abweichungen mehr zwischen den KPI "Zu senden" und "Gesendet" eines In-App-Versands in einem Workflow auf.
* Fehlerkorrektur – Tracking funktioniert jetzt für In-App-Nachrichten, die in benutzerdefiniertem HTML-Code erstellt wurden.
* Fehlerkorrektur – In-App-Nachrichteninhalte, die in einem Workflow verwendet werden, können jetzt gespeichert werden.
* Fehlerkorrektur – Mobile Apps sind jetzt auch für Administratoren sichtbar.
* Fehlerkorrektur – jetzt tritt kein Fehler mehr beim technischen Zustellbarkeits-Workflow auf. (CAMP-26387)
* Fehlerkorrektur – Jetzt treten keine Abweichungen mehr zwischen den für einen In-App-Versand ausgewählten Profilen und den im Versand-Dashboard dargestellten Profilen auf. (CAMP-28722)
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr bei der Integration von Campaign mit Assets Core Service auf, sodass ein freigegebenes Asset in einer E-Mail ausgewählt werden kann.

## 19.0 - Version Januar 2019 {#release-19-0---january-2019}

### Neue Funktionen? {#what-s-new--2}

<table> 
 <colgroup><col style="width: 30%"><col style="width: 70%"></colgroup>
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Allgemeine Verfügbarkeit von Email Designer<br /> </td> 
   <td> <p>Der neue, intuitive Email Designer (zuvor Creative Designer genannt) ist jetzt allgemein verfügbar. Er unterstützt jetzt alle Funktionen des bisherigen Inhaltseditors, wie:</p> 
    <ul> 
     <li> Die Verwendung von <a href="../../integrating/using/adding-target-dynamic-content.md">dynamischen Bildern von Adobe Target</a> </li> 
     <li> Die Möglichkeit, <a href="../../designing/using/importing-content-from-a-url.md#retrieving-content-from-a-url-automatically-at-preparation-time">in der Vorbereitungsphase Inhalt von einer URL automatisch abzurufen</a> </li> 
     <li> Vollständig kompatible <a href="../../start/using/about-templates.md#content-templates">native Inhaltsvorlagen</a>. </li> 
    </ul> 
    <p>For more information, refer to the <a href="../../designing/using/about-email-content-design.md">detailed documentation</a> and the <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-email-designer-tutorial.html">how-to video</a>. Unten finden Sie alle Verbesserungen und Fehlerkorrekturen.</p><p>Aus diesem Grund wird der bisherige E-Mail-Inhaltseditor eingestellt. Weiterführende Informationen dazu finden Sie auf dieser <a href="https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html">Seite</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Produktlisten in Transaktions-E-Mails<br /> </td> 
   <td> <p>Sie können jetzt in einer Transaktions-E-Mail eine oder mehrere Produktlisten referenzieren. So können Sie beispielsweise im Anschluss an einen stehen gelassenen Warenkorb automatisch eine E-Mail versenden, in der alle im Warenkorb befindlichen Produkte samt Bild, Preis und Link zum Produkt aufgelistet werden.</p><p>For more information, refer to the <a href="../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message">detailed documentation</a> and the <a href="https://helpx.adobe.com/campaign/kt/acs/using/acs-product-listings-in-transactional-emails-feature-video-setup.html">how-to video</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Mobile-Ansicht in Email Designer<br /> </td> 
   <td> <p>Bei der Bearbeitung von E-Mail-Inhalten können Sie jetzt zu einer Mobile-Ansicht wechseln. Dort können Sie das responsive Design einer E-Mail anpassen, indem Sie alle Stiloptionen für die Anzeige auf Mobilgeräten einzeln bearbeiten, z. B. Spannen, Schriftgrad, Hintergrundfarbe usw.</p><p> Lesen Sie für weiterführende Informationen das <a href="../../designing/using/about-email-content-design.md#switching-to-mobile-view">entsprechende Handbuch</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Verbesserungen der Betaversion von In-App Messaging<br /> </td> 
   <td> <p>Die Betafunktion In-App Messaging wurde folgendermaßen verbessert:</p> 
    <ul> 
     <li> Der In-App-Betakanal entspricht der DSGVO. </li> 
     <li> Integration mit Analytics-APIs, um Triggers-Dropdown-Listen mit Daten zu befüllen </li> 
     <li> Intuitive Optik und Beschreibung von Versandvorlagen </li> 
     <li> Verbesserte Bedienbarkeit der Authoring-Benutzeroberfläche </li> 
    </ul> <p>Lesen Sie für weiterführende Informationen das <a href="../../channels/using/about-in-app-messaging.md">entsprechende Handbuch</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Neuheiten {#improvements}

* Durch eine neue Option in der Datenladeaktivität können Sie eine Anschlussvorgangsetappe auf die Datei anwenden, die zurückgewiesene Datensätze enthält (z. B. Komprimierung im ZIP-Format). (CAMP-24521)
* Eine neue Option in der Daten-Update-Aktivität ermöglicht jetzt die Konfiguration der maximalen Batch-Größe für hochzuladende Daten. (CAMP-28400)
* Verbesserte Auswahlmöglichkeit des Landes einer Profiladresse. Bei der Auswahl eines Landes wird die Dropdown-Liste "Bundesland/-staat" jetzt automatisch mit den relevanten Bundesland-Werten aktualisiert. (CAMP-28874)
* Eine neue Option in der Dateiextraktionsaktivität verhindert jetzt die Erstellung einer Datei, wenn die eingehende Transition leer ist. Dadurch wird verhindert, dass leere Dateien zu SFTP-Servern hochgeladen werden.
* Der Versandzusammenfassungs-Bericht wurde verbessert.
* Die Liste der verfügbaren Länder bei der Definition einer Profiladresse wurde erweitert. (CAMP-26707)
* Jetzt wird eine Fehlernachricht angezeigt, wenn versucht wird, einen integrierten Workflow zu importieren.

### Email Designer {#email-designer}

* Fehlerkorrektur – Jetzt wird die Funktion für die geografische Einheit auf einer E-Mail-Vorlage oder in einem Inhaltsfragment, die mit Email Designer erstellt wurden, nicht mehr aktiviert, obwohl diese Funktion in Adobe Campaign deaktiviert wurde. Zuvor war die Vorlage oder das Fragment nicht mehr verfügbar, wenn versucht wurde, nochmals auf sie zuzugreifen. (CAMP-28174)
* Fehlerkorrektur – Jetzt können Bedingungen für dynamische Inhalte während der Bearbeitung von Inhalt mit Email Designer gespeichert werden. (CAMP-27905)
* Fehlerkorrektur – Die HTML-Version wird jetzt nicht mehr aus dem E-Mail-Inhalt entfernt, nachdem die Textversion einer Nachricht bearbeitet und die HTML-Synchronisation in Email Designer aufgehoben wurde. (CAMP-28507)
* Fehlerkorrektur – Die Benutzeroberfläche von Email Designer kann jetzt bei der Verwendung von Internet Explorer 11 geöffnet werden. (CAMP-28273)
* Fehlerkorrektur – Die mit Email Designer auf Schaltflächen angewendeten Einstellungen werden jetzt auch in Microsoft Outlook korrekt dargestellt.
* Fehlerkorrektur – URLs in einem in einer E-Mail verwendeten Inhaltsfragment sind in Email Designer jetzt nicht mehr bearbeitbar. Dies war zuvor möglich, obwohl das Fragment standardmäßig gesperrt war.
* Fehlerkorrektur – Jetzt wird die Divisor-Komponente von Email Designer in Microsoft Office angezeigt.
* Fehlerkorrektur – Jetzt frieren in manchen Browsern keine Seiten mehr ein, wenn Inhalt angesehen wird, der mithilfe des bisherigen E-Mail-Inhaltseditors aus AEM synchronisiert wurde. (CAMP-29068)
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr auf, wenn unter Verwendung des bisherigen E-Mail-Inhaltseditors auf ein Bild in einer E-Mail geklickt wird. (CAMP-30424)
* Fehlerkorrektur – Jetzt ist es möglich, bei der Bearbeitung einer E-Mail mit Email Designer neu erstellte Fragmente anzuzeigen. (CAMP-29928)
* Fehlerkorrektur – Jetzt wird Schaltflächentext ordnungsgemäß in E-Mails angezeigt, die mit Email Designer erstellt und im Outlook Webmail Client empfangen wurden.
* Jetzt ist es möglich, mit Email Designer Profil-Transaktionsnachrichten zu erstellen. (CAMP-28900)
* Fehlerkorrektur – Jetzt ist Inhalt in Email Designer gesperrt, wenn er während der Vorbereitung automatisch von einer URL abgerufen wird. Zuvor konnte der Inhalt bearbeitet werden.

### Korrekturen {#patches-2}

* Fehlerkorrektur – In dynamischen Berichten werden jetzt korrekte Versandlogs angezeigt. (CAMP-23446)
* Fehlerkorrektur – Die Zahlen im Bounce-Zusammenfassungsbericht werden jetzt korrekt angezeigt (CAMP-28703).
* Fehlerkorrektur – Bei der Integration von Campaign mit Assets Core Service tritt jetzt kein Fehler mehr auf, sodass Assets immer angezeigt werden, wenn in einer E-Mail **[!UICONTROL Freigegebenes Bild von Adobe Experience Cloud]ausgewählt wird (CAMP-28732).**
* Fehlerkorrektur – Jetzt können SMS-Nachrichten, die den Buchstaben "œ" enthalten, gesendet werden. Zuvor war dies nicht möglich, selbst wenn die Transliteration im externen SMPP-Konto zugelassen wurde. (CAMP-29041)
* Fehlerkorrektur – Bei der Verwendung einer Segmentierungsaktivität in Workflows werden Datensätze nicht mehr doppelt angezeigt. (CAMP-28743)
* Fehlerkorrektur – In Workflow-Aktivitäten können Werte-Mappings im Bereich Neukodifizierung der Werte jetzt gelöscht werden. (CAMP-28708)
* Fehlerkorrektur – Bei der Verwendung von Platzhaltern in der Option "Existenztest einer Datei" tritt in der Dateitransferaktivität kein Fehler mehr auf. (CAMP-28977)
* Fehlerkorrektur – Bei der Aktualisierung der Einstellungen externer Konten tritt in der Dateitransferaktivität kein Fehler mehr auf. (CAMP-28894)
* Fehlerkorrektur – Bei der Verwendung der Bedingung "E-Mail ist nicht leer" tritt bei benutzerdefinierten Filtern im Abfrageeditor kein Fehler mehr auf. (CAMP-28741)
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr auf, wenn benutzerdefinierte Ressourcentabellen mit über 100.000 Datensätzen exportiert werden. (CAMP-28150)
* Fehlerkorrektur – Mit Triggers verknüpfte Transaktionsnachrichten können jetzt gelöscht werden. (CAMP-28385)
* Passwörter, die in manchen SMS-Logs angezeigt wurden und daher ein Sicherheitsrisiko darstellten, wurden entfernt.
* Fehlerkorrektur – Jetzt werden die Verbindungen zum SMPP Simulator nicht mehr unterbrochen. Das war der Fall, wenn von Adobe Campaign ein leeres Passwort gesendet wurde.
* Fehlerkorrektur – Jetzt können Kampagnen versendet werden, wenn SMS-Verbindungen instabil sind.
* Fehlerkorrektur – Gelöschte Sendungen werden jetzt nicht mehr in dynamischen Berichten angezeigt.
* Fehlerkorrektur – Zusatzdaten können jetzt aus Versandlogs, Trackinglogs und Ausschlusslog-Tabellen abgerufen werden, wenn in einem Workflow eine Anreicherungsaktivität verwendet wird.
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr bei DSGVO-Löschanfragen auf, wenn der Relationstyp "Kollektionsrelation mit Kardinalität N" und die Option "Das Löschen des Zieldatensatzes zieht das Löschen der durch die Relation referenzierten Datensätze nach sich" verwendet wird.
* Fehlerkorrektur – Bei der Berichtfreigabe tritt jetzt kein Fehler mehr auf.
* Fehlerkorrektur – Beim Versand von Push-Benachrichtigungen treten jetzt keine Durchsatzprobleme mehr auf.
* Fehlerkorrektur – In Briefpost-Ausgabedateien fehlen jetzt keine Felder mehr.
* Fehlerkorrektur – Benutzer können jetzt keine integrierten Workflows mehr ändern.
* Fehlerkorrektur – Bei der Erstellung einer Kampagne mit einer Kampagnenvorlage, die einen Workflow mit einer konfigurierten Dateiextraktionsaktivität enthält, tritt jetzt kein Fehler mehr auf (CAMP-29198)
* Fehlerkorrektur – Bei der Dateiextraktionsaktivität kann jetzt derselbe Ausdruck für mehrere Elemente verwendet werden. (CAMP-29182)
* Fehlerkorrektur – Jetzt tritt im Abfrageeditor bei der Join-Bedingung zwischen Broadlog und Trackinglog für rtEvent kein Fehler mehr auf. (CAMP-28780)
* Fehlerkorrektur – Jetzt können Änderungen an der Landingpage "Spezifische Aktionen" gespeichert werden. (CAMP-29422)
* Fehlerkorrektur – Jetzt kann die Payload eines Ereignisses in einem Workflow exportiert werden. (CAMP-29029)
* Fehlerkorrektur – Auf der Blacklist stehende SMS-Nummern können jetzt von einer SMS-Nachricht ausgeschlossen werden. (CAMP-28898)
* Fehlerkorrektur – SMPP-Anbieter können jetzt im Fall eines Fehlers bei der Verarbeitung eingehender Nachrichten benachrichtigt werden. (CAMP-29804)
* Fehlerkorrektur – Externe Konten mit damit verbundenen Sendungen können jetzt nicht mehr gelöscht werden. (CAMP-29738)
* Der Versanddurchsatz für SMS-Nachrichten wurde verbessert und ist jetzt stabiler.
* Fehlerkorrektur – Das Zeichen "~" kann jetzt in SMS-Nachrichten verwendet werden. (CAMP-29172)
* Fehlerkorrektur – Bei der Option zur Versandzeitoptimierung tritt bei Sendungen kein Fehler mehr auf. (CAMP-29231)


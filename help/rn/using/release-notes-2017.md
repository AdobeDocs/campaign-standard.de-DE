---
title: Versionshinweise 2017
description: Auf dieser Seite werden alle Versionen von Adobe Campaign Standard von 2017 und aufgelistet.
page-status-flag: never-activated
uuid: d73f8186-e309-441b-969d-71d0a1c33cf4
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: 1cfd9b3b-9b3e-4587-9c46-b6fb02131654
internal: n
snippet: y
translation-type: ht
source-git-commit: 1f15e28bed22e3defb29f16875fcf4c07f4af5a3
workflow-type: ht
source-wordcount: '4688'
ht-degree: 100%

---


# Versionshinweise 2017{#release-notes}

Suchen Sie eine bestimmte Version von Adobe Campaign Standard aus dem Jahr 2017?

Mit jeder Version werden neue Funktionen und Korrekturen veröffentlicht. Klicken Sie auf eine Version, um sich den Inhalt anzusehen.

Sehen Sie sich [Dokumentationsaktualisierungen](../../rn/using/documentation-updates.md) für Adobe Campaign Standard an. Neuere Versionshinweise finden Sie auf dieser [Seite](../../rn/using/release-notes.md).

## Version 17.10 - Oktober 2017         {#release-17-10---october-2017}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Ermüdungsverwaltung<br /> </td> 
   <td> Mit der Ermüdungsverwaltung können Sie Ermüdungsregeln erstellen, um zu verhindern, dass Profile zu oft angesprochen werden. Ermüdungsregeln können einfach erstellt werden und sind dabei extrem flexibel durch Funktionen wie die kanalübergreifende Zählung von Nachrichten (einschließlich Transaktionsnachrichten), die Zählung von bestimmten Sendungen oder die Anwendung von Regeln auf bestimmte Profile.<br /> Lesen Sie für weiterführende Informationen das <a href="../../sending/using/fatigue-rules.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Inhaltserstellung: Import aus einer URL<br /> </td> 
   <td> Durch den Import aus einer URL können Sie rasch auf Kreativinhalte auf einer Website zugreifen, um E-Mails zu erstellen. Zusätzlich können Sie Ihre Kreativprozesse optimieren, indem Sie Dritten ermöglichen, Inhalte direkt über eine URL zu teilen. Importierte Inhalte können flexibel als Teil eines Einzelversands oder auf Vorlagenebene verwendet werden, was eine konsistente Präsentation der Marke in allen Kampagnen ermöglicht, egal ob es sich um auf Workflows basierte Nachrichten oder um Transaktionsnachrichten handelt oder ob sie A/B-Tests oder multivariate Tests beinhalten. Beim Import aus einer URL werden alle Links automatisch umgewandelt und getrackt, damit die E-Mail-Leistung mithilfe dynamischer Berichte überwacht werden kann.<br /> Lesen Sie für weiterführende Informationen das <a href="../../designing/using/using-existing-content.md#importing-content-from-a-url">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**Korrekturen**

_Plattform_

* Fehlerkorrektur – große, komprimierte Dateien werden jetzt richtig dekomprimiert.
* Die Sicherheit bei der Verwaltung von Marken wurde verbessert. Die Änderung eines Markennamens und der Adresse des Absenders ist jetzt den technischen Administratoren von Adobe vorbehalten.
* Um die Sicherheit zu erhöhen, können vom Benutzer erstellte Inhalte (Bilder, Mirrorseiten, Landingpages etc.) nicht mehr von der Domain adobe.com ausgegeben werden. Jetzt müssen diese Ressourcen über eine eigene Domain im Branding-Bereich konfiguriert werden.
* Fehlerkorrektur – jetzt tritt bei der Darstellung und Filterung von Marketing-Aktivitäten kein Fehler mehr auf.
* Fehlerkorrektur – Felder mit dem Abonnement-Datum werden jetzt mit einem POST-Rest-API-Aufruf aktualisiert.

_E-Mails, SMS und Briefpost_

* Fehlerkorrektur – eine Audience vom Typ Liste kann jetzt in einer Nachricht ausgewählt werden, ohne dass die Vorbereitung fehlschlägt.
* In der mehrsprachigen E-Mail-Versandfunktion wurden fehlende Sprachen hinzugefügt.
* Die Im Versand-Dashboard dargestellte Inhalts-Miniaturansicht wird jetzt automatisch aktualisiert, wenn der Inhalt geändert und gespeichert wird.
* Fehlerkorrektur – in Verbindung mit der Zeitzone tritt jetzt kein Fehler mehr auf und Sendungen können geöffnet werden.

_Push-Benachrichtigungen_

* Bei der Konfiguration des Push-Benachrichtigungskanals sollte die Push-Provider-Plattform für iOS **apns** und für Android **gcm** sein.
* Fehlerkorrektur – in der Adobe Campaign-Benutzeroberfläche können jetzt iOS Mobile Apps korrekt hinzugefügt werden.
* Push-Benachrichtigungen werden jetzt unter Android sowohl auf GCM-fähigen als auch auf FCM-fähigen Mobile Apps unterstützt.
* Fehlerkorrektur – Inhalt kann jetzt gespeichert werden, wenn eine Vorlage einer Push-Benachrichtigung dupliziert wird.
* Jetzt kann ein Profil aus der Adobe Campaign-Datenbank erstellt oder aktualisiert werden, indem die Benutzerdaten von Mobile Apps abgestimmt werden.
* Adobe Campaign priorisiert jetzt die Verarbeitung von Transaktions-Push-Benachrichtigungen gegenüber Standard-Push-Benachrichtigungen.

_Berichte_

* Fehlerkorrektur – der Prozentsatz der Klicks wird jetzt im E-Mail-Inhalt angezeigt.
* Fehlerkorrektur – die Blockierungslisten-Metrik wird jetzt als Bounce und nicht mehr als Hardbounce gezählt.
* Fehlerkorrektur – in der Zusammenfassung werden jetzt keine negativen Zählungen mehr angezeigt.
* Fehlerkorrektur – Profile werden jetzt nicht mehr in der falschen Altersgruppe gezählt.
* Die Formeln für Softbounces und Hardbounces wurden geändert.

_Workflows_

* Fehlerkorrektur – in der Aktivität **[!UICONTROL Datei laden]** tritt kein Fehler mehr auf, nachdem in der Aktivität manuell Spalten hinzugefügt und entfernt wurden.
* Der technische Workflow **[!UICONTROL deliverabilityUpdate]** ist jetzt so festgelegt, dass er um 2 Uhr Serverzeit durchgeführt wird.
* Fehlerkorrektur – aus Sicherheitsgründen kann jetzt kein Listenexport mehr durchgeführt werden, wenn der Benutzer nicht über die Export-Benutzerrolle verfügt.
* Fehlerkorrektur – Bei der Aktivität **[!UICONTROL Abstimmung]** tritt kein Fehler mehr auf.
* Fehlerkorrektur – bei der Verwendung von Platzhaltern in der Aktivität **[!UICONTROL Dateiübertragung]** tritt kein Fehler mehr auf.

_Profile und Audiences_

* Fehlerkorrektur – jetzt werden die Bedingungen von Abfragen immer berücksichtigt, sodass kein falsches Ergebnis mehr auftritt.
* Fehlerkorrektur – auf Profile kann jetzt auch dann zugegriffen werden, wenn sie in der Zielgruppe einer Nachricht waren, die zwar vorbereitet, aber nie gesendet wurde und abgelaufen ist.

_Integrationen_

* Fehlerkorrektur – Datenquellen, die für Trigger erstellt wurden, können jetzt richtig angezeigt und ausgewählt werden.

_Benutzerdefinierte Ressourcen_

* Fehlerkorrektur – in Bildschirmen des Typs Liste werden jetzt keine Zeilen für benutzerdefinierte Ressourcen mehr angezeigt, die keine Daten enthalten.
* Fehlerkorrektur – boolesche Felder mit dem Wert &#39;False&#39; werden jetzt in benutzerdefinierten Ressourcen angezeigt.

## Version 17.9 - September 2017         {#release-17-9---september-2017}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Bibliothek für E-Mail-Vorlagen<br /> </td> 
   <td> Neu: 18 neue responsive Vorlagen in zwei attraktiven Motiven namens Astro und Feather. Diese anpassbaren Vorlagen sind branchenunabhängig und können sofort verwendet werden. Die Vorlagen enthalten Inhalte für eine Vielzahl von Nutzungsszenarien und ermöglichen Ihnen damit, E-Mail-Marketingkampagnen rascher, effizienter und attraktiver zu konzipieren und durchzuführen.<br /> Lesen Sie für weiterführende Informationen das <a href="../../designing/using/using-reusable-content.md#content-templates">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dynamische Berichterstellung mit Profildaten<br /> </td> 
   <td> Die dynamische Berichterstellung ermöglicht vollständig anpassbare und in Echtzeit aktualisierte Berichte. Neu in dieser Version ist eine deutliche Verbesserung der dynamischen Berichterstellung, durch die auf Profildaten zugegriffen werden kann. Dies ermöglicht die demografische Analyse nach Profildimensionen wie Geschlecht, Stadt, Postleitzahl und Alter sowie nach Daten von E-Mail-Kampagnen wie Öffnungen und Klicks. Durch die gewohnte, benutzerfreundliche Benutzeroberfläche mit Drag &amp; Drop-Funktionalität ist es jetzt einfacher denn je festzustellen, wie Ihre E-Mail-Kampagne bei Ihrem wichtigsten Kundensegment angekommen ist.<br /> Lesen Sie für weiterführende Informationen das <a href="../../reporting/using/about-dynamic-reports.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Gesammelte Anmeldung mit Ursprung &amp; Datum<br /> </td> 
   <td> Mit dieser verbesserten Funktion der gesammelten Anmeldung können Sie jetzt in einem Workflow über die Aktivität "An/Abmeldedienst" Anmeldeinformationen (Ursprung und Datum) direkt in der Adobe Campaign Standard-Datenbank speichern.<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/subscription-services.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**Korrekturen**

_Plattform_

* Kunden, die keinen eindeutigen Schlüssel zur Identifizierung ihrer eigenen Datensätze verwenden, müssen in der Lage sein, eine Kennung von Adobe Campaign Standard abzurufen. Diese Kennung (**ACS ID**) kann einerseits exportiert, andererseits aber auch als Abstimmschlüssel bei der Datenaktualisierung verwendet werden. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources).
* Das FTP-Protokoll wird nicht weiterverwendet. Verwenden Sie stattdessen SFTP. Damit vorhandene Implementierungen nicht blockiert werden, funktionieren Konfigurationen auf FTP wie bisher, doch für neue Aktivitäten wird die Option nicht mehr angezeigt.

_E-Mails, SMS und Briefpost_

* Jetzt ist es möglich, neue Warnungsbedingungen für Benachrichtigungen zu Versandwarnungen zu erstellen. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-criterion).
* Die Benachrichtigungen zu Versandwarnungen haben ein neues Design und das Versandwarnungs-Dashboard wurde verbessert.
* Wenn jetzt ein externes Routing-Konto deaktiviert ist, wird in den betroffenen Sendungen (E-Mail, SMS und Push-Benachrichtigungen) ein Warnhinweis angezeigt. Gleichzeitig ist die Schaltfläche **Vorschau** verborgen.
* Fehlerkorrektur – In der Vorschau von A/B-Tests zum E-Mail-Inhalt tritt kein Fehler mehr auf, wenn dynamischer Text in der Betreffzeile aktiviert ist.

_Transaktionsnachrichten_

* Jetzt ist es möglich den Zeitpunkt einer Folgenachricht festzulegen, z. B. drei Tage nach einer Transaktionsnachricht. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../channels/using/follow-up-messages.md#sending-a-follow-up-message).
* Jetzt ist es möglich, das Datum festzulegen, ab dem die mit einem Ereignis verknüpfte Transaktionsnachricht gesendet werden soll.
* Fehlerkorrektur – Jetzt tritt kein SQL-Fehler mehr auf, wenn ein Workflow, der eine Folgenachricht enthält, ausgeführt wird, nachdem mit empfangenen und verarbeiteten Ereignissen verknüpfte Profile gelöscht werden.
* Fehlerkorrektur – Mit einem Ereignis verknüpfte Profile können jetzt gelöscht werden.
* Fehlerkorrektur – Jetzt tritt bei der Weiterleitung getrackter Links kein Fehler mehr auf.
* Fehlerkorrektur – Jetzt kann das Tracking gewisser Links in einer E-Mail oder SMS deaktiviert werden.

_Berichte_

* Der **Klicks**-Bericht wurde verbessert. Außerdem ist es jetzt möglich, Klicks für jeden in einem Versand definierten bedingten Inhalt sowie für jeden wiederkehrenden Versand oder für Transaktionsnachrichten anzuzeigen. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../sending/using/receiving-alerts-when-failures-happen.md#creating-a-delivery-alerting-criterion).
* Fehlerkorrektur – Mit der Quarantänemetrik können jetzt korrekte Daten abgerufen werden.
* Ein neuer vordefinierter Zeitrahmen wurde zum Kalender-Widget hinzugefügt.
* Die [Metriken für dynamische Berichte](../../reporting/using/indicator-calculation.md) und die [Kampagnen-KPIs](../../sending/using/confirming-the-send.md) (dargestellt im Dashboard gesendeter Nachrichten) wurden für größere Kohärenz angepasst.
* Fehlerkorrektur – Pipelines stürzen auf Debian 7 jetzt nicht mehr ab.

_Workflows_

* Fehlerkorrektur – Jetzt tritt bei der Aufbewahrung von importierten Dateien kein Fehler mehr auf.

_Integrationen_

* eVars und Ereignisse werden jetzt bei der Integration von Analytics und Campaign unterstützt.
* Wenn eine E-Mail mit dem Inhalt des stehengelassenen Warenkorbs gesendet wird, ist der Payload-Parameter für die aus dem Warenkorb entfernten Elemente jetzt optional.

_Profile und Audiences_

* Adobe Campaign erstellt jetzt einen Bericht, in dem die Anzahl der aktiven Profile angegeben wird. Dieser Bericht hat nur informativen Charakter und keine direkte Auswirkung auf die Rechnungsstellung. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../audiences/using/active-profiles.md).
* Fehlerkorrektur – Profile können jetzt über die API &quot;Profile und Dienste&quot; einen Dienst abonnieren.

## Version 17.7 - Juli 2017         {#release-17-7---july-2017}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Mehrsprachige E-Mail- und SMS-Sendungen<br /> </td> 
   <td> Definition und Ausführung mehrsprachiger E-Mail- und SMS-Sendungen im Rahmen eines einzigen Versands in der bevorzugten Sprache Ihrer automatisch segmentierten Kunden. Zusätzlich können Sie Leistungsberichte zu jedem Versand aufgeschlüsselt nach Sprachen und Personen erstellen.<br /> Immer mehr Unternehmen stehen vor dem Problem, im Zuge ihrer internationalen Expansion mehrsprachige Inhalte versenden zu müssen. Deshalb ist der optimierte Versand lokalisierter Nachrichten ein wesentlicher Teil einer effektiven Kundenkommunikationsstrategie für multinationale Unternehmen, Unternehmen in Ländern mit mehreren Sprachen und Unternehmen, die ihre Inhalte unabhängig vom Wohnort ihrer Kunden auf sprachlicher Ebene weiter personalisieren möchten. Lesen Sie für weiterführende Informationen das <a href="../../channels/using/creating-a-multilingual-email.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Adobe Campaign-Benachrichtigungen<br /> </td> 
   <td> Empfang von Benachrichtigungen zu wichtigen Systemaktivitäten direkt in Adobe Campaign Standard. So werden Sie beispielsweise vom Fortschritt Ihrer aktuellen Sendungen benachrichtigt oder über einen fehlerhaften Workflow informiert.<br /> Echtzeit-Benachrichtigungen informieren die jeweiligen Interessengruppen und ermöglichen es Benutzern, unverzüglich und direkt auf Aktivitätsbenachrichtigungen innerhalb der Anwendung zu reagieren. Teams profitieren dadurch von verbesserter Agilität und Effizienz sowie von einer reibungslosen Ausführung der Kampagnen. Lesen Sie für weiterführende Informationen das <a href="../../administration/using/sending-internal-notifications.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Versandwarnungen<br /> </td> 
   <td> Zusätzlich zur Ansicht von Benachrichtigungen direkt in Adobe Campaign Standard bietet Adobe Campaign jetzt auch ein E-Mail-Warnsystem, bei dem Benutzern oder externen Interessengruppen E-Mail-Warnungen zu wichtigen Systemaktivitäten gesendet werden. Erstellen, Verwalten und Empfangen von benutzerdefinierten Warnungen und Dashboards, um über erfolgreiche oder fehlerhafte Sendungen auf dem Laufenden zu bleiben.<br /> Die Versandwarnung von Adobe Campaign erhöht die Effizienz, indem alle Benutzer von Adobe Campaign in einem Unternehmen automatisch über den Ausführungsstatus des Versands über E-Mails und Dashboards informiert werden. Lesen Sie für weiterführende Informationen das <a href="../../sending/using/receiving-alerts-when-failures-happen.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Verschlüsselte Declared ID in Datenquellen<br /> </td> 
   <td> Versand von E-Mail- und SMS-Triggern, ohne dass in Campaign ein Profil vorhanden sein muss, indem verschlüsselte Kontaktinformationen (E-Mail-Adresse oder Telefonnummer) als Declared ID verwendet werden. Verschlüsselte Declared IDs können von Adobe Campaign Standard dekodiert werden, weshalb jetzt neue vermarktbare Profile erstellt werden können, wenn Audiences mit zuvor unbekannten Kontakten von anderen Experience Cloud-Lösungen übermittelt werden.<br /> Ermöglicht das Ansprechen von Kunden und unbekannten potenziellen Kunden in Echtzeit mithilfe von E-Mail und SMS, um die Loyalität der bestehenden Kundenbasis zu stärken und neue Kunden zu gewinnen. Nutzen Sie Ihre Cookie-Daten aus erster Hand (von Adobe Audience Manager*) optimal, wenn potenzielle Kunden diese Einblicke in Adobe Campaign authentifizieren und nutzen. <br /> *Adobe Audience Manager ist erforderlich. Lesen Sie für weiterführende Informationen das <a href="../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> KPI-Freigabe von Campaign für Analytics<br /> </td> 
   <td> Gemeinsame Nutzung von Kampagnendaten mit Adobe Analytics, um E-Mail-Marketingmetriken in Campaign gemeinsam mit anderen Marketing- und Werbeaktivitäten anhand von Konversionen zu messen, wodurch Sie sich einen Überblick über das Kundenverhalten vor und nach dem Anklicken verschaffen können.<br /> Direktes Verfolgen der Gesamtleistung und Erkennen von Synergien mit externen Programmen in Analytics. Lassen Sie die Erkenntnisse aus dieser kombinierten Ansicht wiederum in Ihre Kampagnen einfließen. Damit können Sie schließlich die Öffnungs-, Klick- und Konversionsraten steigern und die Einnahmen sowie die Gesamtleistung der Kampagne verbessern. <br /> Hierzu ist Adobe Analytics erforderlich. Lesen Sie für weiterführende Informationen das <a href="../../integrating/using/about-campaign-analytics-integration.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Briefpost-Kanal - Rücksendungen an den Absender<br /> </td> 
   <td> Der Austausch einfach strukturierter Dateien, die Rücksendeinformation enthalten, mit Briefpost-Dienstleistern wird jetzt unterstützt. Durch diese Verbesserung des Briefpost-Kanals können entsprechende Anschriften von der künftigen Kommunikation ausgeschlossen werden.<br /> Zusätzlich können Marketer sich über fehlerhafte Adressen informieren lassen und mit dem Kunden über andere Kanäle in Kontakt treten oder ihn auffordern, seine Anschrift zu aktualisieren. Dadurch sparen Marketer auch Marketingausgaben, da keine Mails mehr an falsche Adressen gesendet werden. <br /> Briefpost ist als zusätzlicher Kanal verfügbar. Lesen Sie für weiterführende Informationen das <a href="../../channels/using/return-to-sender.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**Korrekturen**

_Allgemein_

* Fehlerkorrektur – jetzt ist der Export von Listen nur mehr durch bestimmte Benutzer möglich. Nur Benutzer mit der Rolle **[!UICONTROL Export]** sind dazu berechtigt.

_E-Mails, SMS und Briefpost_

* Fehlerkorrektur – im Workflow **updateDeliveryExecInfo** wird der Indikator **Zu senden** bei SMS-Sendungen nicht mehr auf 0 gestellt.
* In der Option **Erweiterte Parameter** der Versandvorlagen-Eigenschaften werden in der Dropdown-Liste **Routing** nur externe Konten angezeigt, die dem Nachrichtentyp der Vorlage entsprechen. Beispielsweise werden in einer E-Mail-Versandvorlage nur externe E-Mail-Konten angezeigt.
* Fehlerkorrektur – in Testprofilen ist es nun möglich, **[!UICONTROL Text]** als bevorzugtes E-Mail-Format auszuwählen.
* Fehlerkorrektur – bei der Auswahl der Standardzeitzone im Planungsbildschirm eines Versands tritt kein Javascript-Fehler mehr auf.
* Fehlerkorrektur – Fallen werden jetzt in den Versandlogs angezeigt.
* Im Bildschirm für die Vorlagenauswahl des Versanderstellungsassistenten werden jetzt Vorlagen für Folgenachrichten und A/B-Tests standardmäßig verborgen. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../channels/using/creating-an-email.md).
* Fehlerkorrektur – jetzt ist der Versand von Nachrichten nur mehr durch bestimmte Benutzer möglich. Nur Benutzer mit der Rolle **[!UICONTROL Sendungen starten]** sind dazu berechtigt. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../sending/using/confirming-the-send.md).

_Push-Benachrichtigungen_

* Fehlerkorrektur – Reporting mit der URL **Campaign-Tracking-Endpunkt** ist jetzt möglich.
* Fehlerkorrektur – Der Titel der Push-Benachrichtigung wird jetzt auf Android-Geräten angezeigt.
* Fehlerkorrektur – Push-Benachrichtigungen werden jetzt auf iOS-Geräten angezeigt, wenn die Push-Benachrichtigung nur einen Titel (und nichts im Nachrichten-Textkörper) enthält.
* Fehlerkorrektur – URLs von Medienanhängen in einem Versand werden jetzt nicht mehr getrackt. Dies verhinderte die Integration von Videos und Bildern in den Versand. Das Tracking von URLs des Typs mediaAttachmentURL ist jetzt für Push-Benachrichtigungen standardmäßig deaktiviert.

_Berichte_

* Fehlerkorrektur – Werte werden jetzt in Grafiken und Tabellen nicht mehr unterschiedlich angezeigt.
* Fehlerkorrektur – Push-Benachrichtigungswerte werden nicht mehr als E-Mail-Werte angezeigt.
* Fehlerkorrektur – Werte werden jetzt nicht mehr als unbekannt angezeigt, wenn ein Versand außerhalb einer Kampagne erstellt wurde.
* Fehlerkorrektur – SMS-Berichtsdaten werden nicht mehr als Mobile App-Daten angezeigt.

_Workflows_

* Workflow-Logs können jetzt gefiltert werden (Zeitraum und Textsuche). Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../automating/using/monitoring-workflow-execution.md).
* Im Versand-Workflow ist jetzt eine Option verfügbar, mit der die Bestätigung vor dem Senden deaktiviert werden kann.
* Fehlerkorrektur – Im Erstellungsassistenten eines wiederkehrenden Versands kann jetzt eine Outbound-Transition eingestellt werden.
* Fehlerkorrektur – jetzt kann eine Workflow-Abfrageaktivität auf der Basis eines benutzerdefinierten Ressourcenfeldes mit einer Auflistung verwendet werden, die zahlreiche Werte aufweist.

## Version 17.5 - Mai 2017         {#release-17-5---may-2017}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Briefpost<br /> </td> 
   <td> Durchbrechen Sie die digitale Barriere und stellen Sie mit Briefpost, dem ersten Offline-Kanal von Adobe Campaign Standard, eine Verbindung zur echten Welt her. Diese Funktion ermöglicht die Personalisierung und Erstellung einer Datei, die von Briefpost-Dienstleistern als Teil Ihrer Cross-Channel-Kampagnen benötigt wird. Mit Briefpost können Sie Kunden ansprechen oder das Kundenerlebnis durch einen attraktiven taktilen Kontaktpunkt verbessern und Kunden zu Ihrer App, Ihrer Website oder in den Verkaufsraum führen.<br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/about-direct-mail.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> E-Mail-BCC<br /> </td> 
   <td> E-Mail-BCC ermöglicht die Archivierung jeder einzelnen an Empfänger gesendeten E-Mails. Durch das Hinzufügen einer BCC-E-Mail-Adresse zu allen E-Mails können Kunden von Adobe Campaign Standard eine exakte Kopie einer jeden E-Mail aufbewahren. Dies ist eine häufige rechtliche Anforderung insbesondere im Finanzdienstleistung-Sektor und hilft Kundendienstzentralen in Echtzeit bei der Konfliktlösung.<br /> Lesen Sie für weiterführende Informationen das <a href="../../sending/using/archiving.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**Korrekturen**

_Aktualisierung der Benutzeroberfläche_

* In der Navigationsleiste wurde der Link **[!UICONTROL Planung]** entfernt und durch den Link **[!UICONTROL Programme &amp; Kampagnen]** ersetzt.

_E-Mails und SMS-Nachrichten_

* Fehlerkorrektur – der Versandstatus **[!UICONTROL Weitere Zustellversuche in Gang]** wird nun in der richtigen Farbe, blau und nicht grau, angezeigt. Die Farbe war grau statt blau.

_Workflows_

* Fehlerkorrektur - jetzt tritt kein Fehler mehr auf, wenn die in der Aktivität **[!UICONTROL Dateiübertragung]** auszuführende Aktion geändert wird.

_Berichte_

* Die Indikatorberechnungen für **[!UICONTROL Spam]** und **[!UICONTROL Spam-Rate]** wurden geändert.
* Die **[!UICONTROL Bounce]**-Metriken wurden verbessert und liefern jetzt genauere Ergebnisse.

_Push-Benachrichtigungen_

* Fehlerkorrektur – jetzt kann ein Push-Ereignis im Marketingverlauf eines Profils ausgewählt werden.
* Die Verwendung von Push-Benachrichtigungen in Workflows wurde verbessert.

## Version 17.4 - April 2017         {#release-17-4---april-2017}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Verbesserte Bildbearbeitungsfunktionen mit Creative SDK<br /> </td> 
   <td> Sie können jetzt Bilder mit den zahlreichen Funktionen des Adobe Creative SDK direkt im Inhaltseditor während der Bearbeitung von E-Mails oder Landingpages bearbeiten.<br /> Für diese Funktion ist kein Kauf zusätzlicher Creative-Cloud-Lösungen erforderlich.<br /> Weitere Informationen finden Sie im <a href="../../designing/using/images.md#modifying-images-with-the-adobe-creative-sdk">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push-Benachrichtigungen für Transaktionen<br /> </td> 
   <td> Die Kapazitäten des Transaktionsnachrichtenversands von Adobe Campaign wurden um den Mobile-App-Kanal erweitert. Transaktionsnachrichten werden jetzt von drei Kanälen unterstützt: E-Mail, SMS und Push-Benachrichtigungen.<br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/transactional-push-notifications.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Wiederkehrende Push-Benachrichtigungen<br /> </td> 
   <td> Sie können jetzt wiederkehrende Push-Benachrichtigungen in einem Workflow konfigurieren. Mit wiederkehrenden Push-Benachrichtigungen können Sie Ihren Kunden regelmäßige Aktualisierungen wie beispielsweise wöchentliche Informationen oder Angebote senden.<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/push-notification-delivery.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Amazon Simple Storage Service (S3) Connector<br /> </td> 
   <td> Jetzt kann der Amazon-Simple-Storage-Service-Connector (S3) für den Import oder Export von Daten in und aus Adobe Campaign verwendet werden. Er kann in einer Workflow-Aktivität eingerichtet werden. Die Konfiguration erfolgt in einem externen Konto.<br /> Lesen Sie für weiterführende Informationen das <a href="../../administration/using/external-accounts.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integration von Dreamweaver verfügbar<br /> </td> 
   <td> Die Integration zwischen Adobe Campaign und Dreamweaver ist jetzt verfügbar. Sie funktioniert mit der aktuellsten Version von Dreamweaver (17.0.2).<br /> Dies erfordert die Integrationserweiterung von Adobe Campaign, die hier heruntergeladen werden kann: <a href="https://adobe.ly/acdw_addon">https://adobe.ly/acdw_addon</a><br />. Weiterführende Informationen finden Sie in diesem <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/designing-content/email-designer/dreamweaver-integration.html">Video</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**Korrekturen**

_Plattform_

* Fehlerkorrektur – ein Problem bezüglich des Speicherbedarfs wurde beseitigt.

_E-Mails und SMS-Nachrichten_

* Fehlerkorrektur – Inhalt kann jetzt ordnungsgemäß mit den letzten Änderungen bei der Vorschau einer Nachricht synchronisiert werden.
* Fehlerkorrektur – eine MX- oder Domain-E-Mail-Verarbeitungsregel kann jetzt erstellt oder gelöscht werden.
* Fehlerkorrektur – E-Mails mit mehreren Aliassen können jetzt gesendet werden.
* Fehlerkorrektur – Fallen-Versandlogs werden jetzt in den Versandlogs angezeigt.
* Fehlerkorrektur – jetzt tritt kein Fehler mehr auf, wenn die getrackten URLs eines Versands angezeigt werden sollen, aber keine URLs im Inhalt vorhanden sind.
* Fehlerkorrektur – die Größenattribute eines Bildes werden jetzt korrekt in der gesendeten Nachricht angewendet.

_Transaktionsnachrichten_

* Das rtEventHistoId-Feld wird in einer Transaktionsnachrichtenvorlage nicht mehr als Personalisierungsfeld angezeigt.

_Landingpages_

* Der Filter **[!UICONTROL Nach E-Mail]** in Landingpages wurde optimiert, um neue Abonnenten mit Datenbankprofilen abzustimmen.
* Fehlerkorrektur – jetzt werden nicht mehr freie Texteingaben anstelle von Kontrollkästchen angezeigt, wenn booleschen Felder zur Konfiguration eines Formulars verwendet werden.
* Fehlerkorrektur – jetzt kann eine Miniaturansicht von Landingpages erstellt werden.

_Workflows_

* Fehlerkorrektur – bei der Bearbeitung der Aktivitäten **[!UICONTROL Ende]** oder **[!UICONTROL Externes Signal]** tritt kein Anzeigefehler mehr auf (Fehler betraf nur Safari).
* Die Fehlermeldung bei der Bearbeitung der Aktivität **[!UICONTROL Audience lesen]** mit einer fehlerhaften Audience wurde verbessert.
* Fehlerkorrektur – jetzt entsteht kein SQL-Fehler mehr, wenn eine Abonnementaktivität ausgeführt wird.

_Integrationen_

* POI-Daten: Fehlerkorrektur – bei der Zählung von Standortabonnenten tritt kein Fehler mehr auf.

_Audiences und Abfragen_

* Fehlerkorrektur – Summen- und Durchschnitts-Aggregate für eine Kollektion können jetzt im Abfrageeditor verwendet werden.
* Fehlerkorrektur – der Abfrageeditor kann jetzt nach der Änderung der Filterressource erneut geladen werden.

_Berichte_

* Fehlerkorrektur – die Metriken zur Öffnungsrate werden jetzt korrekt berechnet, wenn in einer Tabelle mehrere Zeilen ausgewählt werden.
* Fehlerkorrektur – jetzt werden Metriken nicht mehr nur als ganze Zahlen dargestellt. Sie können auch als Dezimalzahlen dargestellt werden.

_Push-Benachrichtigungen_

* Fehlerkorrektur – jetzt wird eine Fehlermeldung angezeigt, wenn eine Android-Anwendung mit einer Mobile App verknüpft wird, die nicht auf MCPNS erstellt wurde.
* Fehlerkorrektur – Benutzer können jetzt stillen Benachrichtigungen keine Töne mehr hinzufügen.

## Version 17.2 - März 2017         {#release-17-2---march-2017}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Dynamische Berichterstellung<br /> </td> 
   <td> Die dynamische Berichterstellung ermöglicht neuartige, vollständig anpassbare und in Echtzeit aktualisierte Berichte. Diese Funktion basiert auf anpassbaren Pivot-Tabellen und Grafiken. Per Drag &amp; Drop können Sie darin Variablen und Dimensionen verschieben und so die Effizienz und Wirksamkeit Ihrer Marketingkampagnen analysieren. Mit der dynamischen Berichterstattung können Sie Berichte individuell erstellen und speichern.<br /> Lesen Sie für weiterführende Informationen das <a href="../../reporting/using/about-dynamic-reports.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integration von Dreamweaver (Labs)<br /> </td> 
   <td> Durch die Integration von Adobe Campaign und Dreamweaver steht Ihnen jetzt ein umfassendes Verfahren zur Erstellung von E-Mail-Kampagnen mit Adobe-Lösungen bereit.<br /> Sie können Adobe Campaign-E-Mails in Dreamweaver bearbeiten und den Inhalt zwischen diesen beiden Lösungen synchronisieren.<br /> In der ersten Release ist die Integration als "Labs"-Funktion verfügbar, die nur mit der Betaversion von Dreamweaver (Pre Release) funktioniert. Wenn Sie sie aktivieren möchten, kontaktieren Sie bitte AC-DW-integration@adobe.com.<br /> Weiterführende Informationen finden Sie in diesem <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/designing-content/email-designer/dreamweaver-integration.html">Video</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Manuell Versandzeitpunkt optimieren<br /> </td> 
   <td> Sie können jetzt manuell für jeden Empfänger einen Versandzeitpunkt festlegen – auf Versandebene oder mit einem Workflow. <br /> Dazu sind zwei neue Optionen verfügbar: <br /> 
    <ul> 
     <li> Alle Empfänger erhalten die Nachricht unter Berücksichtigung ihrer jeweiligen Zeitzone. </li> 
     <li> Jeder Empfänger erhält die Nachricht zu einem in einer Formel festgelegten berechneten Zeitpunkt. </li> 
    </ul> Lesen Sie für weiterführende Informationen das <a href="../../sending/using/optimizing-the-sending-time.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Neue Funktionen bei Push-Benachrichtigungen<br /> </td> 
   <td> Der Push-Benachrichtigungs-Kanal wurde folgendermaßen verbessert:<br /> 
    <ul> 
     <li> Neue Authoring-Benutzeroberfläche </li> 
     <li> Stille Benachrichtigungen (Silent Push) </li> 
     <li> Interactive Push </li> 
     <li> Unterstützung von Rich-Inhalten </li> 
     <li> Berechnung der Nutzdatengröße </li> 
    </ul> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/about-push-notifications.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: Neue Signal-Aktivität<br /> </td> 
   <td> Mit der neuen <span class="uicontrol">Signal</span>-Aktivität können Sie in einem Workflow einen anderen Workflow auslösen.<br /> Durch die Fähigkeit, einen Workflow durch einen anderen zu starten, können Sie jetzt komplexere Customer Journeys unterstützen. Sie können die Customer Journeys besser überwachen und beim Auftreten von Problemen reagieren.<br /> Mehrere Workflow-Aktivitäten wurden aktualisiert:<br /> 
    <ul> 
     <li> <span class="uicontrol">Ende</span>-Aktivität: In einem neuen Tab können Sie festlegen, welcher Workflow ausgelöst werden soll, nachdem eine Aktivität abgeschlossen ist. </li> 
     <li> <span class="uicontrol">Daten-Update</span>-Aktivität: Über die neue leere ausgehende Transition kann eine <strong>Ende</strong>-Aktivität hinzugefügt werden, die einen weiteren Workflow auslöst. Leere ausgehende Transitionen enthalten keine Daten und belegen auch keinen Speicherplatz im System. </li> 
    </ul> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/external-signal.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Workflows: neue Audience-lesen-Aktivität<br /> </td> 
   <td> Beginnen Sie Ihre Zielgruppenbestimmung mit einer bestehenden Audience, die Sie in einer einzigen Aktivität einfach auswählen und eingrenzen können.<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/read-audience.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> POI-Daten (Points of Interest)<br /> </td> 
   <td> Die POI-Funktion basiert auf der Integration von Adobe Campaign mit Adobe Analytics for Mobile. Wenn Benutzer die App eines Unternehmens öffnen, können Standortdaten vom Mobilgerät des Benutzers erfasst werden, <strong>Points of Interest</strong> genannt. Dadurch kann das Unternehmen mithilfe von Adobe Campaign-Workflows personalisierte Nachrichten basierend auf dem Standort des Benutzers senden. Dieser Kanal bedient sich des Mobile-Core-Service-SDKs.<br /> Bitte beachten Sie, dass diese Funktion Analytics for Mobile, eine zahlungspflichtige Lösung, voraussetzt.<br /> Lesen Sie für weiterführende Informationen das <a href="../../integrating/using/about-campaign-points-of-interest-data-integration.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> REST APIs<br /> </td> 
   <td> In der API können Sie jetzt auf Ressourcen zugreifen, sofern diese mit einer Ressource vom Typ "Profiles and Services" verknüpt sind.<br /> Lesen Sie für weiterführende Informationen das <a href="../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**Korrekturen**

_Allgemein_

* Jetzt können beim Export von Versandlogs Profildaten hinzugefügt werden.

_E-Mails und SMS-Nachrichten_

* Fehlerkorrektur – jetzt kann die Option **[!UICONTROL Vor dem Nachrichtenversand Bestätigung einholen]** deaktiviert werden, wenn die Markierung entfernt und der Versand gespeichert wird.
* Fehlerkorrektur – die Depublikation von Transaktions-E-Mails wird nicht mehr verhindert.
* Fehlerkorrektur – Inhalt kann jetzt ordnungsgemäß mit den letzten Änderungen vor der Vorschau eines Versands synchronisiert werden.

_Landingpages_

* Fehlerkorrektur – ein Benutzer kann jetzt Bearbeitungen durchführen, wenn er in den Inhaltsbereich einer Landingpage klickt.

_Workflows_

* Fehlerkorrektur – der Inhalt der Zurückweisungs-Transition der Aktivität **[!UICONTROL Datei laden]** kann jetzt gelesen werden.
* Fehlerkorrektur – vertauschte Spalten werden jetzt bei der Konfiguration der Aktivität **[!UICONTROL Datei laden]** berücksichtigt.

## Version 17.1 - Januar 2017 {#release-17-1---january-2017}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Protokollexport für externe Berichterstattung<br /> </td> 
   <td> Exportieren Sie Logs, wie zum Beispiel Versandlogs und Trackinglogs, um sie in Ihren eigenen Berichterstattungs- oder Business Intelligence Tools zu verarbeiten. Mithilfe von Workflows mit inkrementellen Abfragen können Sie automatisch regelmäßige Exporte neuer Logs durchführen.<br /> Zusätzlich zur Verfügbarkeit der Log-Ressourcen im Ressourcen-Picker wurden auch Verbesserungen an den Aktivitäten <a href="../../automating/using/incremental-query.md">Inkrementelle Abfrage</a> und <a href="../../automating/using/extract-file.md">Dateiextraktion</a> vorgenommen:<br /> 
    <ul> 
     <li> Mit der Option <span class="uicontrol">Inkrementelle Abfrage</span> können Sie neue oder aktualisierte Daten nun über ein Datumsfeld abrufen. Zuvor waren alle Ergebnisse früherer Ausführungen automatisch ausgeschlossen, selbst wenn sie seit der letzten Ausführung aktualisiert worden waren. </li> 
     <li> Mit der Option <span class="uicontrol">Dateiextraktion</span> können jetzt Titel anstelle von Kennungen für Auflistungswerte exportiert werden. </li> 
    </ul> Diese Aktivitäten stehen Administratoren zur Verfügung, die Zugriff auf alle geografischen und Unternehmenseinheiten besitzen.<br /> Weiterführende Informationen zum Exportieren von Logs finden Sie im <a href="../../automating/using/exporting-logs.md">entsprechenden Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Marketing-Funktionen für Transaktionsnachrichten<br /> </td> 
   <td> Sie können nun Transaktionsnachrichten basierend auf Kunden-Marketing-Profilen versenden. Damit haben Sie folgende Möglichkeiten:<br /> 
    <ul> 
     <li> Marketing-Typologieregeln wie <span class="uicontrol">Auf die Blockierungsliste gesetzte Adresse</span> anwenden </li> 
     <li> einen Abmelde-Link in die Nachricht einfügen </li> 
     <li> die Transaktionsnachrichten zur allgemeinen Versandberichterstattung hinzufügen </li> 
     <li> Die Transaktionsnachrichten für die Customer Journey nutzen </li> 
    </ul> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/profile-transactional-messages.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transaktionsnachrichten-API<br /> </td> 
   <td> Die Transaktionsnachrichten-API ist jetzt über <a href="https://docs.campaign.adobe.com/doc/standard/en/adobeio.html">adobe.io</a> verfügbar, wodurch die Verwendung und Überwachung vereinfacht wird:<br /> 
    <ul> 
     <li> Sie profitieren von den Berichterstellungs- und Überwachungsfunktionen der Plattform adobe.io. </li> 
     <li> Die Authentifizierung erfolgt nun über einen adobe.io-Token anstatt über die IP-Zulassungsauflistung, wodurch das Sicherheitsverfahren vereinfacht wird. </li> 
     <li> Alle APIs sind jetzt auf einer einzigen Plattform integriert. Damit wird es einfacher, Ihrer Integration Funktionen für Transaktionsnachrichten hinzuzufügen, wenn Sie bereits die Profiles &amp; Services API unterstützen. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

**Korrekturen**

_Allgemein_

* Die Optionen zur **[!UICONTROL Zugriffsberechtigung]** sind jetzt wieder in den Eigenschaften der Landingpage verfügbar.
* Fehlerkorrektur – kein altes Bild wird mehr anstelle des gewünschten Bildes gerendert. Dieser Fehler ist aufgetreten, wenn das Ausgangsbild in der Inhaltserstellung eines Versands oder einer Landingpage aktualisiert worden war.
* Fehlerkorrektur – in einem bestehenden externen SFTP-Konto können jetzt alle Felder bearbeitet werden.
* Fehlerkorrektur – mehrere Probleme mit der Benutzeroberfläche wurden behoben. Beispielsweise können jetzt problemlos Profilattribute bearbeitet und Änderungen gespeichert werden.

_E-Mails und SMS-Nachrichten_

* Fehlerkorrektur – bei Versandvorlagen mit HTML-Inhalt, der ein Tag enthält,

_Push-Benachrichtigungen_

* Fehlerkorrektur – von Anwendungen können jetzt Postbacks an den Adobe Campaign-Server gesendet werden.
* Fehlerkorrektur – für Android sind jetzt die Funktionen **[!UICONTROL Ton abspielen]** und **[!UICONTROL Benutzerdefinierte Felder]** verfügbar.
* Fehlerkorrektur – jetzt wird kein zusätzliches Maskierungszeichen mehr an für Emojis verwendete Unicode-Zeichen angefügt.
* Wenn der Anmeldetoken eines Abonnenten auf die Blockierungsliste gesetzt wird, wird der entsprechende Status in der Abonnentenliste der Anwendung in Adobe Campaign jetzt unverzüglich aktualisiert.

_Workflows_

* Fehlerkorrektur – die Vorschau auf Abfragen bezüglich Ereignisressourcen (z. B. rtEvent) ist jetzt möglich.
* Die von einer **[!UICONTROL Datei-laden]**-Aktivität erstellte Zurückweisungsdatei kann jetzt in ihrer ausgehenden Transition abgerufen und in der nächsten Aktivität verarbeitet werden. Beispielsweise kann die Zurückweisungsdatei über einen SFTP-Server mit **[!UICONTROL Dateiübertragung]** hochgeladen werden.
* Fehlerkorrektur – die Population eines Segments kann jetzt eingeschränkt werden, wenn **[!UICONTROL Temporäre Ressource]** im Tab **[!UICONTROL Allgemein]** im Bereich **[!UICONTROL Segmentierung]** ausgewählt ist.
* **[!UICONTROL Die Aktivitäten von Planung]** können jetzt nicht mehr so eingestellt werden, dass ein Workflow häufiger als einmal alle 10 Minuten ausgelöst wird.
* Fehlerkorrektur – jetzt funktioniert **[!UICONTROL Nur gemeinsame Zusatzdaten verwenden]** in der Aktivität **[!UICONTROL Vereinigung]** einwandfrei.

_Integrationen_

* Fehlerkorrektur – bei der Freigabe einer Ereignisauslösung in Adobe Campaign kommt es zu keinen Problemen mehr. Dieser Fehler trat auf, wenn die Metadaten &quot;Wahrscheinlichkeit eines erneuten Besuchs innerhalb von 30 Tagen&quot; zur Abbruchsauslösung in Adobe Experience Cloud hinzugefügt wurden.
* Fehlerkorrektur – der technische Workflow löscht jetzt nicht mehr das Zieldimensionsfeld, wenn Audiences von People Core Service importiert werden. Darauf folgende Abfragen konnten keine importierten Audiences abrufen.
* Fehlerkorrektur – durch die Aktivität **[!UICONTROL Audience-Speicherung]** eines Workflows wird kein Fehler mehr erzeugt, wenn die Option **[!UICONTROL In der Adobe Experience Cloud freigeben]** aktiviert ist.


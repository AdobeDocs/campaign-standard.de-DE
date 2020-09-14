---
title: Versionshinweise 2019
description: Auf dieser Seite werden alle Versionen von Adobe Campaign Standard von 2019 aufgelistet.
page-status-flag: never-activated
uuid: 99f92a54-4b3d-48b9-b08d-e98b24e75f62
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: e54f8305-7e32-4193-8e5a-b5d87b03038c
internal: n
snippet: y
translation-type: ht
source-git-commit: 1f15e28bed22e3defb29f16875fcf4c07f4af5a3
workflow-type: ht
source-wordcount: '7628'
ht-degree: 100%

---


# Versionshinweise 2019{#release-notes-2019}

[Versionsplanung](https://helpx.adobe.com/de/campaign/kb/acs-release-planning.html) | [Control Panel-Versionen](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html) | [Aktualisierungen der Dokumentation](../../rn/using/documentation-updates.md) | [Neueste Versionshinweise](../../rn/using/release-notes.md) | [Eingestellte Funktionen](https://helpx.adobe.com/de/campaign/kb/acs-deprecated-and-removed-features.html)

## Version 19.4 – Dezember 2019 {#release-19-4---october-2019}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> <strong>California Consumer Privacy Act (CCPA)</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Der CCPA ist das neue Datenschutzgesetz des US-Bundesstaates Kalifornien, das am 01. Januar 2020 in Kraft tritt und in dem die Anforderungen an den Datenschutz harmonisiert und neu geregelt werden. Der CCPA gilt für Adobe Campaign-Kunden, die Daten von Personen ("Datensubjekten") erfassen, die in Kalifornien wohnhaft sind.</p>
   <p>Zusätzlich zu den bereits in Adobe Campaign verfügbaren Datenschutzoptionen (Einverständnisverwaltung, Einstellungen für die Datenbeibehaltung und Benutzerrollen etc.) stellen wir daher weitere Funktionen bereit, mit deren Hilfe Sie CCPA-konformes Verhalten sicherstellen können:</p>
   <ul>
    <li>Recht auf Zugriff und Recht auf Löschung: Dazu nutzen wir die Funktionen, die wir analog dazu für die DSGVO ergänzt haben – <a href="https://helpx.adobe.com/content/help/de/campaign/kb/acs-privacy.html#righttoaccess">mehr dazu</a> </li>
    <li><p>Bei der Erstellung einer Datenschutzanfrage steht nun eine Auswahl für den Regulierungstyp (DSGVO oder CCPA) im Privacy Core Service zur Verfügung. Diese Methode sollten Sie für Anfragen auf Datenzugriff bzw. -löschung verwenden. Die Campaign-API und -Schnittstelle für Zugriffs- und Löschanfragen wurde eingestellt.  Weitere Informationen dazu finden Sie im Artikel <a href="https://helpx.adobe.com/de/campaign/kb/acs-deprecated-and-removed-features.html">Eingestellte und entfernte Funktionen</a>.</p></li>
    <li>Ein Feld für die <strong>Abmeldung gemäß CCPA</strong> wurde zur Profilressource hinzugefügt, über das Adobe Campaign-Benutzer nachverfolgen können, ob ein Kunde die Weitergabe seiner personenbezogenen Daten untersagt hat. <a href="https://helpx.adobe.com/content/help/de/campaign/kb/acs-privacy.html#ccpa">Mehr dazu</a>.</li>
  </ul>
    <p>Weitere Informationen finden Sie in <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/privacy/privacy-overview.html">diesem Video</a>.</p>
</td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Integration mit Microsoft Dynamics 365 (GA)</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> 
    <p>Die Integration von Adobe Campaign Standard mit Microsoft Dynamics 365 ist ab sofort verfügbar. Sie können nun die Datensätze Ihrer Kontakte und benutzerdefinierten Entitäten von Dynamics 365 auf Campaign übertragen und E-Mail-Ereignisdaten von Campaign zurück an Dynamics 365 übermitteln, um eine bessere Abstimmung von Vertrieb und Marketing zu erzielen.</p>
    <p>Weitere Informationen dazu, wie Sie diese Integration einrichten, finden Sie im <a href="../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md">entsprechenden Handbuch</a> und in <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard/using/integrating-with-adobe-cloud/campaign-and-microsoft-dynamics-365/working-with-campaign-standard-and-microsoft-dynamics-365.html">diesem Video</a>.</p>
  </td>
  </tr> 
 </tbody> 
</table>

**Verbesserungen**

* Das Popup-Fenster für die Zustimmung zur Nutzung dynamischer Berichte wurde aktualisiert und beinhaltet jetzt die Integration von Adobe Campaign Standard mit Microsoft Dynamics 365. Durch Akzeptieren der Bedingungen werden für die Integration von Adobe Campaign Standard mit Microsoft Dynamics 365 und für die Erstellung dynamischer Berichte Profildaten mit einbezogen – [mehr dazu](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement) (CAMP-29766)
* Fehlerkorrektur – Beim Empfang von Versandwarnungen werden nun keine falschen Kontaktdaten mehr angezeigt.
* Wenn ein Transaktionsnachrichtenereignis mit einem unbekannten Kontextparameter gesendet wird, gibt Campaign jetzt die Fehlermeldung &quot;400&quot; anstelle von &quot;500&quot; aus. (CAMP-28632)
* In dynamischen Berichten wurde für das **Ausschließen des Testversands** ein neues Segment hinzugefügt. Zum Filtern Ihrer Berichte ist dieses Segment jetzt standardmäßig ausgewählt – [mehr dazu](../../reporting/using/list-of-components-.md#segments)
* Zu Push-Benachrichtigungen wurde eine Option zum Festlegen der **Ablauffrist einer Nachricht** hinzugefügt. Damit können Sie ein Ablaufdatum angeben, an dem die Nachricht nicht mehr von Apple (APNS) bzw. Android (FCM) gesendet wird – [mehr dazu](../../channels/using/customizing-a-push-notification.md#add-expiration-date)
* Die Aktivität **Datei laden** wurde dahingehend verbessert, dass Workflow-Logs nun klarer und detaillierter über den Fehler informieren, der auftritt, wenn das Laden einer Datei fehlgeschlagen ist. Die durch Aktivieren der Option **Zurückweisungen in einer Datei speichern** generierte ausgehende Transition wurde in **Zurückweisungen** umbenannt – [mehr dazu](../../automating/using/load-file.md)
* Zu den Versandlogs wurden Logs mit Bezug auf mehrsprachige Nachrichten hinzugefügt, anhand derer besser nachvollzogen werden kann, warum Sendungen aufgrund von fehlenden Sprachen in den hochgeladenen CSV-Dateien fehlgeschlagen sind.

**Verbesserungen bei der Sicherheit**

* Fehlerkorrektur – Beim Löschen der Informationen eines in Quarantäne gesetzten Profils mittels Datenschutzanfrage werden nun alle Daten einschließlich der E-Mail-Adresse entfernt.
* Die Absicherung gegen Injektionen in E-Mail-Kopfzeilen wurde verbessert.
* Der Schutz vor SSRF-Angriffen unter Verwendung von xtk-Ausdrücken (E-Mail-HTML, Textinhalte und Betreff, SMS und Inhalte von Push-Benachrichtigungen) wurde verbessert.

**Verbesserungen bei Email Designer**

* Fehlerkorrektur – Links für Abmeldung, Anmeldung und Landingpage, die in eine E-Mail eingefügt werden, lassen sich nun verfolgen. (CAMP-37809)
* Fehlerkorrektur – Beim Erstellen einer neuen E-Mail und Auswählen einer Vorlage treten nun keine Fehler mehr auf. (CAMP-38000)
* Für Link-Bearbeitungen mit Email Designer können Sie jetzt die Option **Unterstrichener Link** verwenden. Außerdem wurde eine **Target**-Eigenschaft hinzugefügt, deren Standardwert auf **Ohne** festgelegt ist. [mehr dazu](../../designing/using/styles.md#about-styling-links)
* Fehlerkorrektur – Für Links in Textkomponenten im Textkörper einer E-Mail wird nun die korrekte Farbe verwendet. (CAMP-37330)
* Fehlerkorrektur – Beim Löschen eines Bildes werden nun auch zugeordnete Links entfernt. (CAMP-37234)
* Fehlerkorrektur – Änderungen in den Einstellungen für die **Prioritätsstufe** dynamischer Inhalte in einer Bedingung können jetzt gespeichert werden. (CAMP-36883)
* Fehlerkorrektur – Das Durchsuchen von Landingpages funktioniert jetzt ordnungsgemäß. Die Suche wurde von den 50 zuerst erstellten auf alle in der Datenbank vorhandenen erweitert. (CAMP-36839)
* Fehlerkorrektur – Änderungen des E-Mail-Absenders im Feld **Von: Name** können jetzt gespeichert werden. (CAMP-36606)
* Die Warnung zur Kompatibilität von Karussellkomponenten wurde angepasst und informiert jetzt über unterstützte E-Mail-Clients.
* Ein Problem mit der Anzeige auf Mobilgeräten wurde behoben. Wird einer E-Mail ein neues Bild hinzugefügt oder zu ihr hochgeladen, ist das Höhenattribut jetzt immer auf &quot;Höhe: Auto&quot; festgelegt. (CAMP-35497)
* Fehlerkorrektur – Im HTML-Code werden Stil- und Meta-Tags jetzt nicht mehr beibehalten, wenn ein Fragment aus einer Strukturkomponente gelöscht wird. (CAMP-35390)
* Fehlerkorrektur – Beim Aktualisieren wiederverwendbarer Inhalte tritt kein Problem mehr mit Fragmenten auf. (CAMP-35186)
* Fehlerkorrektur – Nur für Mobilgeräte bestimmte bedingte Inhalte in E-Mails werden jetzt korrekt angezeigt. (CAMP-35155)
* Fehlerkorrektur – Das Problem mit zuweilen angezeigten geschützten Leerzeichen mit Nullbreite wurde behoben. (CAMP-35116)
* Fehlerkorrektur – Die Schaltflächen im Dialogfeld **Als Fragment speichern** befinden sich nun an der korrekten Position.
* Fehlerkorrektur – Nach dem Hinzufügen eines HTML-Tags zu einem Bild oder zu Alternativtext tritt nun kein Problem mit der Vorschau mehr auf.
* Fehlerkorrektur – Beim Bearbeiten in E-Mail-Designer tritt nun kein Problem mehr mit Links in E-Mails auf, die mit dem früheren Editor erstellt wurden.
* Fehlerkorrektur – Im Content verbleiben nun keine Dubletten von Stil-Tags mehr.
* Fehlerkorrektur – Beim Einfügen eines Personalisierungsfelds in eine E-Mail wird nun das korrekte Datumsformat verwendet.
* Fehlerkorrektur – Beim Wechseln zwischen HTML- und Nur-Text-Modus tritt beim Speichern nun kein Problem mehr auf.
* Fehlerkorrektur – Beim Klicken auf die Option zum Sperren und Entsperren werden dem Bereich für Inline-Stil-Eigenschaften nun keine Randwerte mehr hinzugefügt.
* Fehlerkorrektur – Die Größe der Mobilgeräte-Echtzeitansicht wurde angepasst, um ein besseres Rendering zu ermöglichen.
* Fehlerkorrektur – Problematische Größen von Schaltflächen in Vorlagen und Fragmenten wurden angepasst.
* Fehlerkorrektur – Beim Einfügen von Bildern in Schaltflächenkomponenten tritt nun kein Problem mehr mit der Bildgröße auf.

**Sonstige Änderungen**

* Der standardmäßig für die Anzeige von Versand-KPIs verwendete Zeitraum auf der Seite &quot;Dynamische Berichte&quot; wurde so angepasst, dass keine Diskrepanzen in den Berichtsergebnissen mehr auftreten. (CAMP-35148)
* Logs enthalten im Falle eines abgelaufenen Anwendungszertifikats nun eine entsprechende Fehlermeldung.
* Die Vorschau für die Payload-Berechnung enthält nun benutzerdefinierte Feldgrößen, wodurch verhindert wird, dass der Versand von Push-Benachrichtigungen fehlschlägt. (CAMP-35303)
* Der Name der **Datei mit den Zurückweisungen** in der Aktivität **Datei laden** kann jetzt genauso personalisiert werden wie die **Datenexport-Aktivität**.
* Alle benutzerdefinierten Entitäten, die nicht mit einer vordefinierten Entität verknüpft sind, können nun über die API aufgerufen werden.
* Die Datenbankleistung wurde bei der Verarbeitung großer Ressourcen verbessert.
* Die Beschreibungen für einige beim Versand von SMS-Nachrichten auftretende Fehler wurden klarer formuliert. (CAMP-36558)
* Beim Ausführen der Aktivität **Planung** in einem Workflow, bei dem diese entweder direkt oder über verschiedene Aktivitäten mit sich selbst verbunden ist, wird jetzt eine Fehlermeldung angezeigt, da dies dazu führen könnte, dass sich der Workflow-Server aufhängt.
* Verschiedene Verbesserungen wurden vorgenommen, um die Behebung von Fehlern bei Transaktionsnachrichten zu erleichtern: Der Link &quot;Daten&quot; wurde im Bildschirm zur Ereigniskonfiguration in &quot;Letzte Transaktionsereignisse&quot; umbenannt und listet die empfangenen Ereignisse nun in absteigender Reihenfolge auf. Außerdem wurde ein neuer Transaktionsstatus namens &quot;targetingFailed&quot; erstellt. Kann das Transaktionsnachrichtenmodul eine Verknüpfung, die für die Zielgruppenbestimmung von Nachrichten verwendet wird, nicht anreichern, erhält das Transaktionsereignis nun diesen neuen Status (anstelle des Status &quot;routingFailed&quot;).
* An der Oberfläche wurden verschiedene Verbesserungen im Hinblick auf die Einschränkungen des Zugriffs auf Landingpages durch bestimmte geografische oder Organisationseinheiten vorgenommen. Damit soll darauf hingewiesen werden, dass die Landingpage bestimmten Sichtbarkeitsbedingungen unterliegt: Die Auswahl der geografischen und Organisationseinheit ist für die Erstellung einer Landingpage nun obligatorisch. Sobald eine Einheit ausgewählt wurde, wird ein Banner mit den zugehörigen Informationen angezeigt. Die Fehlermeldung, die beim Testen der Landingpage angezeigt wird, wurde klarer formuliert.
* In Campaign Standard-APIs können benutzerdefinierte Schlüssel nicht mithilfe eines PATCH-Vorgangs geändert werden, wenn der Schlüsselwert vom ursprünglichen Schlüssel abweicht oder wenn Sie einen eigenen Schlüssel als URI anstelle des von Adobe bereitgestellten verwenden.
* Die Sprache &quot;Albanisch – Mazedonien&quot; wurde zur Dropdown-Liste bevorzugter Sprachen hinzugefügt. (CAMP-35396)

**Korrekturen**

* Fehlerkorrektur – Terminierte Berichte können nun sortiert oder durchsucht werden.
* Fehlerkorrektur – Die UND- und ODER-Regeln für Auslöser werden nun nicht mehr miteinander vertauscht.
* Fehlerkorrektur – Die Eigenschaft für Mobilgeräte wird nun nicht mehr fälschlicherweise als &quot;In Launch gelöscht&quot; angezeigt. (CAMP-35382)
* Fehlerkorrektur – Die Eigenschaften für Mobilgeräte von Adobe Launch können nun mit Adobe Campaign synchronisiert werden. (CAMP-35411, CAMP-35089, CAMP-35014, CAMP-35487)
* Fehlerkorrektur – Push-Transaktionsnachrichten schlagen nun nicht mehr fehl, wenn Ereignisse mit Profildaten angereichert wurden. (CAMP-34385)
* Fehlerkorrektur – Eigenschaften für Mobilgeräte lassen sich nun über mehrere Umgebungen hinweg synchronisieren. (CAMP-37060)
* Fehlerkorrektur – Beim Auswählen einer Vorlage für eine Push-Benachrichtigung, die eine Formel für ein Kontaktdatum verwendet, tritt nun kein Fehler mehr auf. (CAMP-35300)
* Fehlerkorrektur – Ein Problem, das den Nachrichtenversand-Dienst zum Absturz bringen konnte, wurde behoben. (CAMP-35287)
* Fehlerkorrektur – Bei der wiederkehrenden Briefpost wird nun nicht mehr für alle Elemente das erste Ereignisdatum festgelegt. (CAMP-35139)
* Fehlerkorrektur – Die jüngst erweiterten benutzerdefinierten Ressourcen für **Profile** sind nun für Abfragen verfügbar. (CAMP-35119)
* Fehlerkorrektur – Der Modus **Struktur der Datenbank reparieren** für Instanzen mit aktivierter Sharding-Konfiguration funktioniert jetzt ordnungsgemäß. (CAMP-35118)
* Fehlerkorrektur – Beim Hinzufügen von Aggregat-Daten zu Broadlogs tritt nun kein SQL-Log-Fehler mehr auf. (CAMP-35034)
* Fehlerkorrektur – Beim Erstellen einer Aktivität vom Typ **Segmentierung** tritt nun kein Fehler mehr mit Transitionen auf. (CAMP-35033)
* Fehlerkorrektur – Bei der Aktivität **Abfrage** tritt nun kein Fehler mehr auf, der verhindert, dass über die Funktion **cryp_aescbcDecrypt** die Funktion **crypt_aescbcEncrypt** entschlüsselt wird. (CAMP-34952)
* Fehlerkorrektur – Für Sendungen werden nun die **Trackinglogs** angezeigt. (CAMP-34855)
* Fehlerkorrektur – Bei Verwendung einer benutzerdefinierten Datumsformel für die **Sendezeit-Optimierung** wird der Versand von Push-Benachrichtigungen nun nicht mehr durch Fehler mit den Zusatzdaten des Workflows verhindert. (CAMP-30336)
* Fehlerkorrektur – Ein Problem, das in bestimmten Fällen die Veröffentlichung benutzerdefinierter Ressourcen verhinderte, wurde behoben. (CAMP-37425)
* Fehlerkorrektur – Package-Importe können nun durch Administratoren geändert werden.  (CAMP-37176)
* Fehlerkorrektur – Der Versand von Testsendungen ist nun möglich, was bislang durch ein Problem in Workflows verhindert wurde, wenn die Bereitstellungsaktivität mit einer leeren Aktivität vom Typ **Audience lesen** verbunden war. (CAMP-37164)
* Fehlerkorrektur – Benutzerdefinierte Ressourcen können nun in eine neue Umgebung importiert werden. (CAMP-36506)
* Fehlerkorrektur – Bei Klick-Berichten kommt es nun nicht mehr vor, dass Prozentangaben von Bildern verdeckt werden. (CAMP-36407)
* Fehlerkorrektur – Beim Exportieren eines Versandbeschreibungsfelds tritt nun kein Problem mehr auf. (CAMP-35467)
* Fehlerkorrektur – Es kommt nun nicht mehr vor, dass ein Versand in &quot;Start ausstehend&quot; verbleibt, obwohl der Versand bereits abgeschlossen wurde. (CAMP-35355)
* Fehlerkorrektur – Workflow-Logs werden nun auch dann angezeigt, wenn SQL-Logs aktiviert und dann deaktiviert wurden.

## Version 19.3 - Juli 2019 {#release-19-3---july-2019}

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
   <td> Externe API-Aktivität (öffentliche Beta-Version)<br /> </td> 
   <td> <p>Zur umfassenderen Personalisierung ermöglicht die externe API-Aktivität, Daten aus externen Systemen über einen REST-API-Aufruf in einen Workflow zu übertragen. Bei den REST-Endpunkten kann es sich um ein Customer Management System, Adobe I/O Runtime oder einen REST-Endpunkt von Adobe Experience Cloud (z. B. Data Platform, Target, Analytics, Campaign) handeln.</p><p>Diese Funktion ist derzeit in einer öffentlichen Beta-Version verfügbar.</p><p>Weiterführende Informationen finden Sie in der <a href="../../automating/using/external-api.md">ausführlichen Dokumentation</a> und in <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/managing-processes-and-data/data-management-activities/external-api-activity.html">diesem Video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Bericht zu Workflow-Segmenten<br /> </td> 
   <td> <p>Mit dieser Funktion können Marketingexperten die Leistung ihres Versands nach Segmentcode aufschlüsseln. Wenn Sie einen Workflow erstellen und eine Segmentierungsaktivität verwenden, um der Versandpopulation Segmente zuzuweisen, können diese Segmente nun demselben Versand zugeordnet werden. Auf diese Weise können Sie die Öffnungs- und Klickstatistiken in mehreren Segmenten desselben Versands anzeigen.</p><p>Weiterführende Informationen finden Sie in der <a href="../../reporting/using/creating-a-report-workflow-segment.md">ausführlichen Dokumentation</a> und in <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/reporting/report-on-workflow-segments.html">diesem Video</a>.</p></td>
  </tr> 
 </tbody> 
</table>

**Verbesserungen bei der Sicherheit**

* Fehlerkorrektur – Jetzt besteht keine Sicherheitslücke mehr, durch die DOS-Angriffe (Denial of Service) auf ungültige Anforderungen zum Abrufen von Bildern durchgeführt werden können. (CAMP-33454)

**Verbesserungen bei Email Designer**

* Fehlerkorrektur – Jetzt erhält eine HTML-Vorlage nicht mehr jedes Mal, wenn eine Komponente hinzugefügt wird, zusätzliche HTML-Style-Tags, sodass sich die Vorlagengröße nicht mehr erheblich erhöht. (CAMP-34694)
* Fehlerkorrektur – Alle Optionen in der rechten oberen Symbolleiste sind jetzt jederzeit verfügbar. (CAMP-34577)
* Fehlerkorrektur – Der Inhaltsbaustein der Mirrorseiten-URL kann jetzt problemlos in E-Mail-Inhalt eingefügt werden. (CAMP-34779)
* Fehlerkorrektur – E-Mail-Inhalt kann jetzt problemlos bearbeitet werden, wenn JSPP-Code in der E-Mail verwendet wird. (CAMP-34574)
* Fehlerkorrektur – Bilder werden jetzt nicht mehr am oberen Rand abgeschnitten, wenn ein Hyperlink hinzugefügt wird. (CAMP-34382)
* Fehlerkorrektur – Bei der Verwendung von E-Mail-Designer mit Firefox tritt kein Anzeigeproblem mehr auf. (CAMP-34364)
* Fehlerkorrektur – Im erweiterten Modus kann jetzt dynamischer Inhalt in einer E-Mail problemlos definiert werden. (CAMP-34351, CAMP-34333, CAMP-34331)
* Fehlerkorrektur – Beim Regel-Editor für dynamischen Inhalt treten jetzt keine Fehler mehr auf (CAMP-34304, CAMP-34303).
* Fehlerkorrektur – Das Link-Feld kann jetzt im Einstellungsfenster von E-Mail-Designer angezeigt werden (CAMP-33749).
* Fehlerkorrektur – Das YouTube-Symbol wird in gesendeten E-Mails nicht mehr zu groß dargestellt. (CAMP-33726)
* Fehlerkorrektur – Ein Sicherheitsproblem wurde behoben, sodass der Inhalt der Mirrorseite nicht mehr bearbeitbar ist. (CAMP-33691)
* Fehlerkorrektur – Bei der Verwendung des Größer-als-Symbols in dynamischem Inhalt tritt kein Fehler mehr in der HTML-Ausgabe auf. (CAMP-33688)
* Fehlerkorrektur – Beim Bearbeiten von Text in E-Mail-Designer kann jetzt die Rückgängig-Option problemlos verwendet werden. (CAMP-32565)
* Fehlerkorrektur – Beim Rückgängigmachen von Stilen werden jetzt zusätzliche Tags entfernt und nicht mehr hinzugefügt. (CAMP-32359)
* Sie können jetzt definieren, ob eine in einer E-Mail verwendete Komponente nur auf Desktop-Geräten oder nur auf Mobilgeräten angezeigt wird.
* Sie können nun die Breite und Höhe einer Inhaltskomponente für Social Media festlegen.
* Fehlerkorrektur – Alter Quellcode von dynamischem Inhalt wird jetzt nach dem Löschen des entsprechenden Inhalts entfernt.
* Fehlerkorrektur – Der Betreff einer E-Mail kann jetzt aktualisiert werden, nachdem er geändert wurde.
* Fehlerkorrektur – Eine n: n-Spaltenstruktur kann jetzt ausgewählt werden, nachdem sie im Arbeitsbereich abgelegt wurde.
* Fehlerkorrektur – Die Miniaturansicht einer Nachricht wird im E-Mail-Dashboard nicht mehr verschwommen angezeigt.
* Fehlerkorrektur – Der Hintergrund für E-Mails, die in Outlook empfangen werden, wird jetzt korrekt angezeigt.
* Fehlerkorrektur – Die Sortierung auf der Startseite von E-Mail-Designer funktioniert jetzt einwandfrei.
* Fehlerkorrektur – Varianten können jetzt bei der Verwendung von dynamischem Inhalt dupliziert werden.
* Einige unerwünschte Felder wurden aus dem Einstellungsfenster von E-Mail-Designer entfernt.

**Sonstige Verbesserungen**

* Durch die Integration mit Adobe Experience Platform Location Services ist Adobe Campaign jetzt in der Lage, standortbasierte Marketingnachrichten über das Experience Platform SDK an die Abonnenten einer Mobile App zu senden. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../integrating/using/configuring-campaign-points-of-interest-data-integration.md).
* Die Berichterstellungsfunktion wurde verbessert. Um diese Funktion nutzen zu können, müssen Sie die Nutzungsvereinbarung zur dynamischen Berichterstattung akzeptieren. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).
* In Workflows wurde eine neue Option hinzugefügt, um die nächsten zehn Ausführungen eines Workflows in der Vorschau anzuzeigen. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../automating/using/scheduler.md).
* In der Planungsaktivität gibt es eine neue Option, mit der Sie einen bestimmten Tag einer bestimmten Woche für monatliche Sendungen auswählen können. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../automating/using/scheduler.md).
* Beim Erstellen eines wiederkehrenden Versands ohne Aggregat-Zeitraum ermöglicht das Versand-Dashboard jetzt die Anforderung einer Bestätigung, bevor die Nachrichten gesendet werden. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../sending/using/confirming-the-send.md).
* Sie können jetzt den Versandtitel mit Ereignisvariablen personalisieren, die in der Aktivität &quot;Externes Signal&quot; des Workflows deklariert wurden. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../automating/using/calling-a-workflow-with-external-parameters.md).
* Die DSGVO-Löschabfrage wurde verbessert, um eine bessere Leistung zu erzielen. (CAMP-33504)
* Die &quot;ftp&quot;-Option wurde aus der Konfigurationsoberfläche für externe Konten entfernt. (CAMP-34472)
* Sie können jetzt die SMTP-Testmodus-Option für jede E-Mail aktivieren und deaktivieren. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../administration/using/configuring-email-channel.md#smtp-test-mode). (CAMP-34602)

**Sonstige Änderungen**

* In der Benutzeroberfläche für Versandeigenschaften wurde ein Warnhinweis hinzugefügt. Er weist darauf hin, dass die Sendungen auf der Grundlage ihres Aggregat-Zeitraums vorbereitet werden und kein Zeitraum angegeben werden darf, wenn der Workflow mehrmals täglich aufgerufen werden soll. (CAMP-34393)
* In Konfigurationsfenstern benutzerdefinierter Ressourcen wurde ein Warnhinweis hinzugefügt. Es wird empfohlen, für die Kennung benutzerdefinierter Ressourcen maximal 30 Zeichen zu verwenden. Dies gilt auch für Felder, Schlüssel, Indizes und Links benutzerdefinierter Ressourcen.
* Wenn versucht wird, eine Transaktionsnachricht zu löschen, die von einer Landingpage als Bestätigungsnachricht verwendet wird, wird nun eine Nachricht angezeigt.
* In Workflow-Protokollen wird jetzt ein Warnhinweis angezeigt, wenn eine Aktivität länger als 6 Stunden ausgeführt wird. Dies gilt nicht für Aktivitäten vom Typ Push-Benachrichtigung, Versand, Signal, Start, Ende, Verzweigung, Und-Verknüpfung, Planung und Warten.
* In Workflow-Protokollen wird jetzt ein Warnhinweis angezeigt, wenn Sie die maximale Anzahl von gleichzeitig ausgeführten Workflows erreicht haben.
* Workflows, die länger als sieben Tage im Pausen- oder Fehler-Status sind, werden nun gestoppt, um Speicherplatz zu sparen. Die Bereinigungsaufgabe wird in den Workflow-Protokollen angezeigt.
* Bei Verwendung der Aktivität &quot;Datei übertragen&quot; wird jetzt ein Fehler protokolliert, wenn die Dateigröße den verfügbaren Speicherplatz überschreitet.
* Die Aktion &quot;Zu Ziel-URL umleiten&quot; kann nicht mehr für die sekundäre Schaltfläche in In-App-Nachrichten ausgewählt werden.

**Korrekturen**

* Fehlerkorrektur – DSGVO-Zugriffsanforderungen schlagen jetzt nicht mehr fehl.
* Fehlerkorrektur – Beim Empfang mehrerer Triggers für ein einziges Profil werden diese jetzt nicht mehr verworfen.
* Fehlerkorrektur – Jetzt wird nicht mehr fälschlicherweise nach dem Anmelden eine Fehlermeldung über die Publikation einer benutzerdefinierten Ressource angezeigt.
* Fehlerkorrektur – Wenn eine benutzerdefinierte Ressource erstellt oder erweitert wird, wird keine leere Seite mehr angezeigt.
* Fehlerkorrektur – Eine Audience mit appSubscriptionrcp ist jetzt in einem Mobile-Versand als Zielgruppendimension zum Targeting verfügbar.
* Fehlerkorrektur – E-Mail-Adressen von Hardbounces werden jetzt in die Quarantäne aufgenommen. (CAMP-24587)
* Fehlerkorrektur – Jetzt kann eine Typologieregel hinzugefügt und anschließend gelöscht werden, bevor die Typologie gespeichert wird. (CAMP-32789)
* Fehlerkorrektur – Der Inhalt einer Landingpage kann jetzt auch dann angezeigt werden, wenn dynamischer Inhalt deaktiviert ist. (CAMP-32924)
* Fehlerkorrektur – Beim wiederkehrenden Versand tritt kein Fehler mehr auf, wenn die Attribute des primären Versands personalisiert werden. (CAMP-32983)
* Fehlerkorrektur – In Workflows können einer Transition jetzt Ergebnisse entnommen werden, wenn die Transition Daten eingehender SMS-Nachrichten enthält. (CAMP-33134)
* Fehlerkorrektur – Verzweigungs- und Ausschlussaktivitäten können jetzt in Workflows zur Erstellung von Audiences verwendet werden. (CAMP-33401)
* Fehlerkorrektur – Jetzt ist es möglich, bei wiederkehrenden Sendungen den Inhalt von Mirrorseiten anzuzeigen und einen Testversand durchzuführen. (CAMP-33413)
* Fehlerkorrektur – Zwischen Profilen und Audiences kann jetzt eine Vereinigungsaktivität verwendet werden. Dieses Problem wurde durch eine Inkompatibilität der Identifizierungsschlüssel in Eingangstransitionen verursacht. (CAMP-33713)
* Fehlerkorrektur – In Testaktivitäten verwendet der Ausdruck &quot;recCount&quot; jetzt beim Doppelklicken die korrekte Syntax. (CAMP-33756)
* Fehlerkorrektur – Beim Öffnen der Protokolle des technischen Workflows &quot;Rechnungsstellung&quot; wird keine Fehlermeldung mehr angezeigt. (CAMP-34313)
* Fehlerkorrektur – Felder von Abonnement-Checkboxes in Landingpages können jetzt problemlos konfiguriert werden. (CAMP-34369)
* Fehlerkorrektur – In Listen kann jetzt beim Konfigurieren das Feld &quot;Symbol&quot; eingefügt werden. (CAMP-34585)
* Fehlerkorrektur – &quot;|&quot; und &quot;%&quot; können jetzt in der Workflow-Aktivität &quot;Datei laden&quot; als Separatoren für das Datum oder die Uhrzeit verwendet werden. (CAMP-34706)
* Fehlerkorrektur – In Landingpages können jetzt Sichtbarkeitsbedingungen mit Checkboxes verwendet werden. (CAMP-34802)
* Fehlerkorrektur – In der Anreicherungsaktivität werden jetzt im Tab &quot;Zusatzdaten&quot; Felder angezeigt, wenn die Filterdimension auf Trackinglogs und die Zielgruppendimension auf Profil eingestellt ist.
* Fehlerkorrektur – Beim Export der Ressource &quot;Workflow-Vorlage&quot; wird kein Warnhinweis mehr angezeigt.
* Fehlerkorrektur – Beim Erstellen eines neuen Profils kann das Feld &quot;Code für Land/Region&quot; jetzt gespeichert werden, nachdem es im Dialogfeld ausgewählt wurde.
* Fehlerkorrektur – Bei der Verwendung der Briefpost-Importvorlage (updateQuarantinesDeliveryLogsDirectMail) treten jetzt keine Fehler mehr auf.
* Fehlerkorrektur – Bei der Integration von Assets on Demand tritt kein Fehler mehr auf.
* Fehlerkorrektur – Die Timeline-Ansicht kann jetzt problemlos vergrößert werden. (CAMP-33628)
* Fehlerkorrektur – Testsendungen für E-Mail-Nachrichten mit geplantem Datum und Uhrzeit können jetzt unmittelbar durchgeführt werden. (CAMP-33723)
* Fehlerkorrektur – Transaktionsnachrichten erzeugen jetzt keine Fehlerprotokolle mehr, wenn sich ein Benutzer abmeldet. (CAMP-31698)
* Fehlerkorrektur – Die Planung von E-Mail-Nachrichten ist jetzt in allen Umgebungen fehlerfrei möglich.
* Fehlerkorrektur – Der Workflow &quot;Update der Versandausführung&quot; funktioniert jetzt problemlos.
* Fehlerkorrektur – Der E-Mail-Inhalt ist jetzt nicht mehr fehlerhaft, wenn der Betreff mehrere Zeilen lang ist.


## Version 19.2.7 - Juli 2019 {#release-19-2-7---july-2019}

**Verbesserungen**

* Die DSGVO-Löschabfrage wurde verbessert, um eine bessere Leistung zu erzielen.
* Fehlerkorrektur – Nach dem Upgrade 19.2 stürzt die Website nicht mehr ab. (CAMP-34862)
* Fehlerkorrektur – Jetzt können auch andere Benutzer als Admin-Benutzer Berichte speichern und planen. (CAMP-31133)
* Fehlerkorrektur – Bei der Verwendung von &quot;|&quot; als Datumstrennzeichen in der Workflow-Aktivität &quot;Datei laden&quot; tritt kein Problem mehr auf. (CAMP-34706)

## Version 19.2.4 - Juni 2019 {#release-19-2-4---june-2019}

**Email Designer**

* Fehlerkorrektur – Benutzer können jetzt auch Fragmente bearbeiten, wenn im HTML-Code leere Style-Tags verwendet wurden. Dies ist eine Folgekorrektur von CAMP-33778 in Version 19.2.3.

## Version 19.2.3 - Juni 2019 {#release-19-2-3---june-2019}

**Email Designer**

Eine Reihe von Verbesserungen und Korrekturen wurde implementiert, um die Verwendung von Fragmenten in Version 19.2 zu optimieren. Neu erstellte Fragmente funktionieren fehlerlos. Früher erstellte Fragmente werden grau dargestellt und müssen in das neue Format migriert werden. Klicken Sie dazu auf jedes Fragment und bestätigen Sie seine Migration in das neue Format. Wir empfehlen Ihnen, einige Fragmente zu testen, bevor Sie alle migrieren.

* Fehlerkorrektur – Fragmente können jetzt bearbeitet werden, nachdem sie entsperrt wurden. Dieses Problem bestand bei vorhandenen Fragmenten bei der Aktualisierung auf Version 19.2. (CAMP-33778)
* Fehlerkorrektur – Die Verwendung von dynamischen Inhalten funktioniert jetzt einwandfrei. Zum HTML-Code wurden zusätzliche Leerzeichen hinzugefügt.

**Sonstige Verbesserungen**

* Fehlerkorrektur – Der SMS-Versand kann jetzt fortgesetzt werden, nachdem die Verbindung des SMS-Connectors unterbrochen wurde.
* Fehlerkorrektur – SMPP-Verbindungen werden jetzt nicht mehr geschlossen, wenn TLS aktiviert ist.
* Fehlerkorrektur – SMPP-Verbindungen werden jetzt nicht mehr geschlossen, wenn TLS aktiviert ist.
* In Campaign wurde die Option &quot;Launch_URL_Campaign&quot; hinzugefügt, um Eigenschaften von Apps zu verwalten, die mit dem Mobile SDK von Adobe Experience Platform erstellt wurden.
* Fehlerkorrektur – Die Sandbox-Umgebungs-Option wird nicht mehr deaktiviert, wenn das Zertifikat einer neu erstellten mobilen Eigenschaft hochgeladen und die Eigenschaftenseite der App geschlossen wird.
* Fehlerkorrektur – Der Inhalt einer Transaktionsnachricht kann jetzt mit Daten aus der Dienst-Ressource angereichert werden. (CAMP-33707)
* Fehlerkorrektur – Landingpages werden jetzt nicht mehr auf die Blockierungsliste gesetzt, wenn Profile von einem Dienst abgemeldet werden.

## Version 19.2 - Mai 2019 {#release-19-2---may-2019}

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
   <td> Control Panel<br /> </td> 
   <td> <p>Mit dem Control Panel können Sie Administratoraufgaben effizienter erledigen. So ermöglicht es Ihnen, die Serverkapazität zu überwachen und die Einstellungen der Instanzen zu verwalten (u. a. der SFTP-Server).</p><p>Weiterführende Informationen finden Sie im <a href="https://docs.adobe.com/content/help/de-DE/control-panel/using/control-panel-home.html">ausführlichen Handbuch</a> und in <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/administrating/control-panel/control-panel-overview.html">diesem Video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Lokale Benachrichtigungen<br /> </td> 
   <td> <p>Mit lokalen Benachrichtigungen können Sie Benutzer informieren, wenn neue Daten in deren Apps verfügbar sind, selbst wenn kein Internetzugang vorhanden oder die App nicht aktiv ist. Ausgelöst werden lokale Benachrichtigungen von einer App. Der Auslöser erfolgt zu einem bestimmten Zeitpunkt durch ein bestimmtes Ereignis.</p><p>Lesen Sie für weiterführende Informationen das <a href="../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type">entsprechende Handbuch</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Verbesserung bei Workflows – Hinzufügen einer Payload zur Aktivität "Externes Signal"<br /> </td> 
   <td> <p>Starten Sie Workflows nun mit Payloads, wenn zuvor definierte Bedingungen eines anderen Workflows oder eines REST-API-Aufrufs erfüllt sind. Letzteres ermöglicht Ihnen die Integration mit Ihren externen Systemen. Gleichzeitig stellen wir die neue <strong>Test</strong>-Aktivität zur Verfügung, mit der diese Funktion getestet werden kann.</p><p>Weiterführende Informationen finden Sie in der <a href="../../automating/using/calling-a-workflow-with-external-parameters.md">ausführlichen Dokumentation</a> und in <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/managing-processes-and-data/execution-activities/external-signal-activity.html">diesem Video</a>.</p></td> 
  </tr> 
  <tr> 
   <td> Verbesserung bei Landingpages – Google reCAPTCHA<br /> </td> 
   <td> <p>Mit Google reCAPTCHA können Sie Spam auf Ihren Landingpages vermeiden, ohne dass Sie Ihre Kunden zu entsprechenden Handlungen auffordern müssen.</p><p>Weitere Informationen finden Sie im <a href="../../channels/using/configuring-landing-page.md#setting-google-recaptcha">entsprechenden Handbuch</a>.</p></td> 
  </tr> 
 </tbody> 
</table>

**Verbesserungen bei der Sicherheit**

* Fehlerkorrektur – Ein potenzielles Sicherheitsproblem mit Clickjacking im Reporting-Arbeitsbereich wurde behoben.

**Verbesserungen bei Email Designer**

* Fehlerkorrektur – Bei der Verwendung duplizierter Fragmente in E-Mail-Designer tritt kein Fehler mehr auf. (CAMP-33193)
* Fehlerkorrektur – Jetzt werden bei der Verwendung von Inline-Elementen in der E-Mail-Designer-Benutzeroberfläche keine unerwünschten Leerzeichen mehr erzeugt. (CAMP-32163)
* Fehlerkorrektur – Zusätzliche HTML-Tag-Attribute, die vom Benutzer nach dem Speichern von E-Mail-Inhalten in E-Mail-Designer hinzugefügt wurden, werden jetzt nicht mehr gelöscht. (CAMP-32162)
* Fehlerkorrektur – Jetzt wird in E-Mail-Designer im HTML-Modus kein Microsoft-Office-Tag mehr angezeigt, nachdem es entfernt wurde. (CAMP-32141)
* Wenn Sie eine E-Mail in einer veralteten Version von E-Mail-Designer erstellt haben, werden Sie jetzt beim Öffnen dieses E-Mail-Inhalts aufgefordert, ein Update auf die aktuelle Version durchzuführen. (CAMP-31529)
* Fehlerkorrektur – Bilder in einer mit E-Mail-Designer erstellten E-Mail werden jetzt nicht mehr verzerrt dargestellt, wenn sie an gewisse Messaging Clients gesendet werden. (CAMP-31407)
* Fehlerkorrektur – Elemente wie Listen und Schaltflächen werden jetzt im Nur-Text-Modus korrekt dargestellt, wenn sie im HTML-Modus erstellt wurden. (CAMP-32582, CAMP-32542)
* Fehlerkorrektur – Jetzt können mehr als 50 Organisationseinheiten in einer Inhaltsvorlage oder in Fragmenteigenschaften dargestellt werden. (CAMP-32932)
* Fehlerkorrektur – Beim Empfang in Outlook einer mit E-Mail-Designer erstellten E-Mail tritt jetzt kein Fehler mehr mit der Viewport-Hintergrundfarbe auf. (CAMP-31402)
* Fehlerkorrektur – Mit E-Mail-Designer erstellte E-Mail-Inhalte sind jetzt responsiv, wenn sie in Outlook geöffnet werden. (CAMP-31400)
* Fehlerkorrektur – Dynamische Inhalte im Betreff einer E-Mail funktionieren jetzt fehlerfrei. (CAMP-32837)
* Fehlerkorrektur – Jetzt tritt kein durch inkorrekte Escape-Sequenzen bedingter Fehler mehr mit E-Mail-Betreffs auf.
* Fehlerkorrektur – Fragmente können jetzt in E-Mail-Designer in die linke Palette geladen werden.
* Fehlerkorrektur – Fragmente, die während der Inhaltsbearbeitung von E-Mails erstellt wurden, werden jetzt nach der Aktualisierung der Fragmentliste in E-Mail-Designer in der linken Palette dargestellt.
* Fehlerkorrektur – Bei der Verwendung von dynamischen Inhalten in einer E-Mail treten jetzt keine Fehler mehr auf.
* Fehlerkorrektur – Farben mit RGB-Werten können jetzt in der Farbauswahl definiert werden.
* Fehlerkorrektur – Die Mirrorseite ist jetzt responsiv, wenn die E-Mail auf einem Mobiltelefon empfangen wird.

**Verbesserungen bei Transaktionsnachrichten**

Am Transaktionsnachrichten-Kanal wurden mehrere Verbesserungen durchgeführt, um seine Funktionsweise und Leistung zu optimieren.

* Die Dauer von Transaktionsnachrichten wurde verlängert, damit alle Nachrichten gesendet werden können, bevor sie ihre Gültigkeit verlieren, insbesondere wenn der Vorgang wiederholt wird.
* Die Leistung von Transaktionsnachrichten wurde erhöht, indem die Last auf unterschiedliche Versand-Threads aufgeteilt wurde.
* Der Versand von Transaktionsnachrichten wurde optimiert, damit gleichzeitig mehrere Analysen derselben Nachricht durchgeführt werden können.
* Fehlerkorrektur – Durchsatz und Latenz bei Transaktions-Push-Benachrichtigungen sind jetzt einheitlich.
* Fehlerkorrektur – Beim Versand von Transaktionsnachrichten wird jetzt die korrekte Zielgruppe angezeigt.
* Fehlerkorrektur – Beim Import eines Packages mit einer Ereigniskonfiguration und der zugehörigen Transaktionsnachricht tritt jetzt kein Fehler mehr auf. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../channels/using/getting-started-with-transactional-msg.md#exporting-and-importing-transactional-messages).
* Fehlerkorrektur – Jetzt werden keine Kollektionsdaten mehr aus den Testprofilen gelöscht, die für eine Transaktionsnachricht mit Produktlisten erstellt wurden.

**Sonstige Änderungen**

* Zum externen SMS-Konto wurde eine neue Option hinzugefügt. Hiermit kann die maximale Anzahl der für den SMS-Versand verantwortlichen MTA-Prozesse beschränkt werden, um die Anzahl der parallelen Verbindungen besser steuern zu können. Weiterführende Informationen dazu finden Sie in der Technote zum [SMS-Schnittstellenprotokoll und dessen Konfiguration](https://helpx.adobe.com/de/campaign/kb/sms-connector-protocol-and-settings.html).
* Wird jetzt eine Ressource mit einer API-Erweiterung publiziert, deren API zuvor bereits publiziert wurde, wird diese API jedes Mal automatisch aktualisiert, wenn sie erneut publiziert wird. Früher musste diese Aktion manuell durchgeführt werden. Wurde die API nicht aktualisiert, konnte ein Fehler in den Profil- oder Service-Ressourcen dieser API auftreten. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension).
* In dynamischen Berichten wurde die Postleitzahl-Dimension entfernt. Verwenden Sie stattdessen die Dimensionen &quot;Stadt&quot;, &quot;Land&quot; und &quot;Bundesland&quot;.
* Der Lebenszyklus-Ereignistrigger &quot;Erster Start&quot; für In-App-Nachrichten wurde entfernt.
* Wird ein Package mit Sicherheitsgruppen exportiert, enthält es jetzt die den Gruppen zugewiesenen Rollen. (CAMP-32960)
* Eine neue Option ermöglicht Ihnen, in der Aktivität &quot;Datei laden&quot; zu prüfen, ob die Spalten der zu ladenden Datei zur Spaltendefinition passen. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../automating/using/load-file.md). (CAMP-32229)
* Workflows können jetzt mit einer Payload gestartet werden, wodurch externe Parameter für mehrere Aktivitäten innerhalb eines Workflows gemeinsam verwendet werden können. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../automating/using/calling-a-workflow-with-external-parameters.md). (CAMP-29412 &amp; CAMP-29413)
* Campaign Standard-APIs ermöglichen Ihnen jetzt, die geografischen und Organisationseinheiten von Profilen mithilfe einer Payload zu aktualisieren. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../api/using/get-started-apis.md).
* Die Fehlernachrichten, die angezeigt werden, wenn der Zugriff auf ein Datenbankobjekt nicht möglich ist, sind jetzt besser verständlich.
* In der Dateiextraktionsaktivität wurden die Javascript-Funktionen zur Definition des Namens einer zu exportierenden Datei aktualisiert. Im Ausgabefeld ist jetzt nur die formatDate-Funktion verfügbar. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../automating/using/extract-file.md).
* Der Mechanismus zur Kennungserzeugung für benutzerdefinierte Ressourcen wurde verbessert. Primärschlüssel für neue benutzerdefinierte Ressourcen sind jetzt standardmäßig 64 Bit lang.
* Der Testmodus für die Publikation von benutzerdefinierten Ressourcen wurde verbessert. Jetzt wird Benutzern eine Warnung angezeigt, wenn die letzte Publikation einer benutzerdefinierten Ressource fehlgeschlagen ist und noch nicht korrigiert wurde. Wenn die Publikation einer benutzerdefinierten Ressource fehlschlägt, können Sie zur letzten funktionierenden Version zurückkehren. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).
* Zur Dateiübertragungsaktivität wurde eine neue Option hinzugefügt. Damit können Sie im SFTP-Modus bei der Verwendung des Dateidownloads die Dateien sortieren. Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../automating/using/transfer-file.md). (CAMP-33109)

**Korrekturen**

* Fehlerkorrektur – Jetzt tritt beim MTA kein Speicherleck mehr auf, wenn SMS-Einstellungen neu geladen werden.
* Fehlerkorrektur – Datenbankaktualisierungen können jetzt im Reparaturmodus publiziert werden.
* Fehlerkorrektur – Jetzt treten zwischen Berichten in Adobe Analytics und dynamischen Berichten in Adobe Campaign keine Abweichungen mehr auf. (CAMP-25393)
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr im Berichtfreigabe-Workflow auf.
* Fehlerkorrektur – Benutzer können jetzt In-App-Nachrichten mit einer Medien-URL senden.
* Fehlerkorrektur – Jetzt werden Apps nur mehr dann angezeigt, wenn ihr Zertifikat zur Instanz hochgeladen wurde.
* Fehlerkorrektur – Jetzt funktionieren Personalisierungsfelder, wenn die Vorlage **Alle Nutzer einer Mobile App auswählen** verwendet wird.
* Neue Campaign Standard-Instanzen wurden bereitgestellt. (CAMP-32635 &amp; CAMP-32344)
* Fehlerkorrektur – Die Datumsformel in einem Workflow kann jetzt angepasst werden. (CAMP-30336)
* Fehlerkorrektur – Bei der Definition einer benutzerdefinierten Datumsformel sind in der Dropdown-Liste jetzt die Felder &quot;Zusatzdaten&quot; und &quot;Segmentcode&quot; verfügbar. (CAMP-32383)
* Fehlerkorrektur – Verschlüsselte zurückgewiesene Datensätze können jetzt mit den Aktivitäten &quot;Dateiübertragung&quot; und &quot;Dateiextraktion&quot; gefunden werden. (CAMP-32377)
* Fehlerkorrektur – In APIs zeigen jetzt die lineCount-Filter die exakte Gesamtzahl an. (CAMP-31424)
* Fehlerkorrektur – In Landingpages wird in Eingabefeldern jetzt der aktualisierte Wert angezeigt, nachdem dieser geändert wurde. (CAMP-31401)
* Fehlerkorrektur – Jetzt wird die Signalaktivität nicht mehr unerwartet aktiviert.
* Fehlerkorrektur – Die E-Mail-Vorschau wird jetzt auch dann angezeigt, wenn die Zielgruppe leer ist.
* Fehlerkorrektur – In der Aktivität &quot;Dateiextraktion&quot; wird jetzt keine Datei mehr erstellt, wenn die Option &quot;Keine Datei erstellen, wenn die eingehende Transition leer ist&quot; aktiviert ist.
* Fehlerkorrektur – Der Zustellbarkeits-Workflow wird jetzt nicht mehr deaktiviert, wenn er nicht erfolgreich beendet wurde.
* Fehlerkorrektur – Benutzer können jetzt Berichte speichern und planen. (CAMP-31133)

## Version 19.1.3 - März 2019         {#release-19-1-3---march-2019}

**Verbesserungen bei Email Designer**

* Fehlerkorrektur – Eine Vorlage kann jetzt auch nach dem Speichern verändert werden.
* Fehlerkorrektur – Jetzt treten keine Fehler mehr auf, wenn eine zuvor erstellte Vorlage in einer E-Mail verwendet wird.
* Fehlerkorrektur – Komponenten können jetzt in importierten Vorlagen verborgen werden.

**Sonstige Verbesserungen**

* Fehlerkorrektur – Bei der Ansicht von Typologieregeln tritt jetzt kein Fehler mehr auf. (CAMP-32059 &amp; CAMP-31849)
* Fehlerkorrektur – Typologieregeln können jetzt bearbeitet werden. (CAMP-31750)
* Fehlerkorrektur – Der inMail-Vorgang hält jetzt nicht mehr unerwartet an. (CAMP-31238)

## Version 19.1 – Februar 2019 {#release-19-1---february-2019}

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
   <td> Verbesserungen bei Push-Kanal-Berichten<br /> </td> 
   <td> <p>Bei Berichten für den Push-Kanal wurden mehrere Verbesserungen vorgenommen, damit die Benutzerinteraktion intuitiver gemessen werden kann. In dieser Version werden drei unterschiedliche Metriken für Push-Kanäle eingeführt: Impressionen, Klicks, Öffnungen (App-Öffnungen). Damit können Benutzerinteraktion mit Push-Benachrichtigungen effizienter gemessen und analysiert werden. Gleichzeitig wurden auch die Definition und Implementierung dieser Metriken standardisiert. Darüber hinaus wurde der Bericht zu Push-Benachrichtigungen durch visuelle Darstellungen und Metriken verbessert.</p><p> Lesen Sie für weiterführende Informationen das <a href="../../reporting/using/push-notification-report.md">entsprechende Handbuch</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Launch-Integration für Mobile App<br /> </td> 
   <td> <p>Diese Version beinhaltet die Integration von Adobe Campaign mit den allgemein verfügbaren Versionen von Android- und iOS-Erweiterungen für Adobe Campaign Standard in Adobe Experience Platform Launch und Mobile SDKs. Diese Erweiterungen unterstützen Push-Benachrichtigungen, In-App-Benachrichtigungen und Mobile-App-Profilaktualisierungen.</p><p> Lesen Sie für weiterführende Informationen das <a href="https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html">entsprechende Handbuch</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Mobile In-App-Nachrichtenversand<br /> </td> 
   <td> <p>Diese Version enthält die allgemein verfügbare Version der In-App-Kanal-Option in Campaign. Die wichtigsten neuen Funktionen gegenüber der Beta-Version sind dynamische Berichte für den In-App-Kanal und der sichere Handshake zwischen Mobile SDK und MCIAS (Experience Cloud In-App Messaging Service, der die In-App-Regeln zum SDK weiterleitet). Der sichere Handshake gewährleistet, dass die personenbezogenen Daten Ihrer Benutzer nicht in betrügerische Hände gelangen können. Außerdem können Sie damit Benutzerdaten auf einem gemeinsam genutzten Gerät schützen, da der Nachrichten-Cache jedes Mal geleert wird, wenn sich der Benutzer abmeldet.</p><p>Weiterführende Informationen finden Sie im <a href="../../channels/using/about-in-app-messaging.md">entsprechenden Handbuch</a> und im <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/communication-channels/mobile/in-app/in-app-message-overview.html">In-App-Tutorial</a>.</p> </td> 
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

**Verbesserungen bei der Sicherheit**

* Der erzeugte Landingpage-HTML-Code wurde aktualisiert, sodass er jetzt die Indexierung durch Suchmaschinen verhindert.

**Verbesserungen bei Email Designer**

* Es wurden vier von Behance Künstlern designte, responsive E-Mail-Vorlagen hinzugefügt.

   Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../designing/using/using-reusable-content.md#content-templates).

* Unser neues On-Boarding ermöglicht Ihnen eine raschere E-Mail-Erstellung und einfacheren Zugriff auf Handbücher und Tutorials.

   Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-home-page).

* Jetzt können Sie die Anzahl und Breite von Spalten nach Belieben konfigurieren.

   Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../designing/using/designing-from-scratch.md#defining-the-email-structure).

* Wenn Sie in der Mobile-Ansicht arbeiten, können Sie nun bestimmte Komponenten für diese Ansicht verbergen, um so den Platz optimal zu nutzen.

   Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../designing/using/plain-text-html-modes.md#switching-to-mobile-view).

* Sie können jetzt zusätzlich zu den bereits verfügbaren Kanälen auch benutzerdefinierte Social-Media-Kanäle zu Ihrer E-Mail-Vorlage hinzufügen.
* Fehlerkorrektur – Jetzt können Sie im Strukturmenü hinunterscrollen, wenn mehr als 18 Strukturen verwendet werden. (CAMP-31173)
* Fehlerkorrektur – Der Preheader wird nicht mehr oberhalb des Inhalts angezeigt, wenn eine mit Adobe Campaign gesendete E-Mail, die einen Preheader enthält, weitergeleitet wird. (CAMP-30736)
* Fehlerkorrektur – Die Betreffzeile kann jetzt aktualisiert werden, wenn die Option zum **Aktualisieren von AEM-Inhalt** ausgewählt wird, nachdem der Betreff in Adobe Experience Manager geändert wurde. (CAMP-29984)
* Fehlerkorrektur – Dynamische Bilder von Adobe Target können jetzt verwendet werden.
* Fehlerkorrektur – Die Vorschau wird jetzt in der Vorbereitungsphase korrekt aktualisiert, auch wenn der abgerufene Inhalt zuvor über eine URL importiert wurde.
* Zur Inhaltskomponente **Social** wurde das YouTube-Symbol hinzugefügt.
* Inhaltskomponenten und Fragmente können jetzt in der Email-Designer-Palette als **Liste** angezeigt werden.

**Sonstige Verbesserungen**

* Adobe Campaign ist jetzt im Zusammenhang mit sowohl SDK-V4- als auch AEP-SDK-Apps vollständig FCM-konform.
* Adobe Campaign unterstützt Push-Benachrichtigungen unter Wear OS von Android sowie watchOS von Apple.
* Warn- und Fehlermeldungen, die bei der Navigation in der Benutzeroberfläche auftreten können, wurden verständlicher gestaltet.
* Jetzt können zur Profilliste Spalten für Opt-in und Opt-out hinzugefügt werden (Felder für &quot;Kontaktieren Sie mich nicht mehr…&quot;).
* Die Zeitzonen-Dropdown-Liste auf dem Profilerstellungs-Bildschirm wurde aus dem Adressbereich in den oberen Bereich des Bildschirms verschoben.
* Jetzt können bei der Konfiguration von benutzerdefinierten Ressourcen-Bildschirmen Trennlinien hinzugefügt werden, sodass Felder in Kategorien zusammengefasst werden können.

   Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](../../developing/using/configuring-the-screen-definition.md#defining-the-detail-screen-configuration).

**Sonstige Änderungen**

* Adobe Campaign und Adobe Experience Cloud stellen mit Campaign Standard Release 19.2 (Frühling 2019) den Support für Microsoft Internet Explorer 11 ein. Bitte wechseln Sie zu Microsoft Edge oder einem anderen unterstützten Browser. Näheres dazu finden Sie auf der Seite der [eingestellten und entfernten Funktionen](https://helpx.adobe.com/de/campaign/kb/acs-deprecated-and-removed-features.html).
* Das Feld **Ländercode** in der Profilressource wurde in **Länder-/Regionscode** umbenannt.

**Korrekturen**

* Fehlerkorrektur – Eine Nachricht kann jetzt auch dann gesendet werden, wenn ein Testprofil zu einer E-Mail-Transaktionsnachricht hinzugefügt wird. (CAMP-29854)
* Fehlerkorrektur – Der Nachrichtenversand auf anderen Kanälen ist jetzt nicht mehr verlangsamt, wenn der Versand in allen Kanälen gleichzeitig gestartet wird und auf einem Kanal langsam ist.
* Fehlerkorrektur – Der MTA beginnt jetzt nicht mehr mit dem Versand von SMS-Nachrichten, wenn die externe Kontoverbindung noch nicht aufgebaut wurde.
* Fehlerkorrektur – Bei der Ausführungsfrequenz und der Startzeit der Planungsaktivität tritt jetzt kein Fehler mehr auf. (CAMP-30745)
* Fehlerkorrektur – Bei der Verwendung von erweiterten Profilressourcen tritt bei der PKEY-Erstellung jetzt kein Fehler mehr auf. (CAMP-30285)
* Fehlerkorrektur – Bei auf Kalendertagen basierenden Ermüdungsregeln tritt jetzt kein Fehler mehr auf. (CAMP-30136)
* Fehlerkorrektur – Beim Zugriff auf benutzerdefinierte Ressourcen mit Namen, die auf &quot;Base&quot; enden, tritt jetzt kein Fehler mehr auf. (CAMP-30109)
* Fehlerkorrektur – Jetzt kann ein PATCH-Aufruf verwendet werden, um ein Profil für einen Dienst anzumelden. (CAMP-29728)
* Fehlerkorrektur – Der Import einer XML-Datei mit der Datei-laden-Aktivität führt jetzt nicht mehr zu Fehlern im Workflow. (CAMP-29208 und CAMP-28205)
* Fehlerkorrektur – Beim Verknüpfen von benutzerdefinierten Ressourcen können jetzt Relationen mit umgekehrter Kardinalität erstellt werden. (CAMP-30476)
* Fehlerkorrektur – Jetzt können Versandlogs erweitert werden, auch wenn Segmentcodes verwendet werden.
* Fehlerkorrektur – Bei der Verwendung der Dateitransfer-Aktivität in Workflows werden keine Zeilen mehr dupliziert.
* Fehlerkorrektur – Terminierte Berichte können jetzt zum geplanten Zeitpunkt versendet werden.
* Fehlerkorrektur – Jetzt treten keine Abweichungen mehr zwischen den KPI &quot;Zu senden&quot; und &quot;Gesendet&quot; eines In-App-Versands in einem Workflow auf.
* Fehlerkorrektur – Tracking funktioniert jetzt für In-App-Nachrichten, die in benutzerdefiniertem HTML-Code erstellt wurden.
* Fehlerkorrektur – In-App-Nachrichteninhalte, die in einem Workflow verwendet werden, können jetzt gespeichert werden.
* Fehlerkorrektur – Mobile Apps sind jetzt auch für Administratoren sichtbar.
* Fehlerkorrektur – jetzt tritt kein Fehler mehr beim technischen Zustellbarkeits-Workflow auf. (CAMP-26387)
* Fehlerkorrektur – Jetzt treten keine Abweichungen mehr zwischen den für einen In-App-Versand ausgewählten Profilen und den im Versand-Dashboard dargestellten Profilen auf. (CAMP-28722)
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr bei der Integration von Campaign mit Assets Core Service auf, sodass ein freigegebenes Asset in einer E-Mail ausgewählt werden kann.

## Version 19.0 - Januar 2019 {#release-19-0---january-2019}

**Neue Funktionen**

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
   <td> Allgemeine Verfügbarkeit von E-Mail-Designer<br /> </td> 
   <td> <p>Der neue, intuitive E-Mail-Designer (zuvor Creative Designer genannt) ist jetzt allgemein verfügbar. Er unterstützt jetzt alle Funktionen des bisherigen Inhaltseditors, wie:</p> 
    <ul> 
     <li> Die Verwendung von <a href="../../integrating/using/adding-target-dynamic-content.md">dynamischen Bildern von Adobe Target</a> </li> 
     <li> Die Möglichkeit, <a href="../../designing/using/using-existing-content.md#retrieving-content-from-a-url-automatically-at-preparation-time">in der Vorbereitungsphase Inhalt von einer URL automatisch abzurufen</a> </li> 
     <li> Vollständig kompatible <a href="../../designing/using/using-reusable-content.md#content-templates">native Inhaltsvorlagen</a>. </li> 
    </ul> 
    <p>Weiterführende Informationen finden Sie in der <a href="../../designing/using/designing-content-in-adobe-campaign.md">ausführlichen Dokumentation</a> und in <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/designing-content/email-designer/email-designer-overview.html">diesem Video</a>. Unten finden Sie alle Verbesserungen und Fehlerkorrekturen.</p><p>Aus diesem Grund wird der bisherige E-Mail-Inhaltseditor eingestellt. Weiterführende Informationen dazu finden Sie auf dieser <a href="https://helpx.adobe.com/de/campaign/kb/acs-deprecated-and-removed-features.html">Seite</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Produktlisten in Transaktions-E-Mails<br /> </td> 
   <td> <p>Sie können jetzt in einer Transaktions-E-Mail eine oder mehrere Produktlisten referenzieren. So können Sie beispielsweise im Anschluss an einen stehen gelassenen Warenkorb automatisch eine E-Mail versenden, in der alle im Warenkorb befindlichen Produkte samt Bild, Preis und Link zum Produkt aufgelistet werden.</p><p>Weiterführende Informationen finden Sie in der <a href="../../channels/using/event-transactional-messages.md#using-product-listings-in-a-transactional-message">ausführlichen Dokumentation</a> und in <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/designing-content/product-listings-in-transactional-email.html">diesem Video</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Mobile-Ansicht in E-Mail-Designer<br /> </td> 
   <td> <p>Bei der Bearbeitung von E-Mail-Inhalten können Sie jetzt zu einer Mobile-Ansicht wechseln. Dort können Sie das responsive Design einer E-Mail anpassen, indem Sie alle Stiloptionen für die Anzeige auf Mobilgeräten einzeln bearbeiten, z. B. Spannen, Schriftgrad, Hintergrundfarbe usw.</p><p> Lesen Sie für weiterführende Informationen das <a href="../../designing/using/plain-text-html-modes.md#switching-to-mobile-view">entsprechende Handbuch</a>.</p> </td> 
  </tr> 
  <tr> 
   <td> Verbesserungen der Betaversion von In-App Messaging<br /> </td> 
   <td> <p>Die Betafunktion In-App Messaging wurde folgendermaßen verbessert:</p> 
    <ul> 
     <li> Der In-App-Betakanal entspricht der DSGVO. </li> 
     <li> Integration mit Analytics-APIs, um Triggers-Dropdown-Listen mit Daten zu befüllen </li> 
     <li> Intuitive Optik und Beschreibung von Versandvorlagen </li> 
     <li> Verbesserte Bedienbarkeit der Authoring-Benutzeroberfläche </li> 
    </ul> <p>Weitere Informationen finden Sie im <a href="../../channels/using/about-in-app-messaging.md">entsprechenden Handbuch</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

**Verbesserungen**

* Durch eine neue Option in der Datenladeaktivität können Sie eine Anschlussvorgangsetappe auf die Datei anwenden, die zurückgewiesene Datensätze enthält (z. B. Komprimierung im ZIP-Format). (CAMP-24521)
* Eine neue Option in der Daten-Update-Aktivität ermöglicht jetzt die Konfiguration der maximalen Batch-Größe für hochzuladende Daten. (CAMP-28400)
* Verbesserte Auswahlmöglichkeit des Landes einer Profiladresse. Bei der Auswahl eines Landes wird die Dropdown-Liste &quot;Bundesland/-staat&quot; jetzt automatisch mit den relevanten Bundesland-Werten aktualisiert. (CAMP-28874)
* Eine neue Option in der Dateiextraktionsaktivität verhindert jetzt die Erstellung einer Datei, wenn die eingehende Transition leer ist. Dadurch wird verhindert, dass leere Dateien zu SFTP-Servern hochgeladen werden.
* Der Versandzusammenfassungs-Bericht wurde verbessert.
* Die Liste der verfügbaren Länder bei der Definition einer Profiladresse wurde erweitert. (CAMP-26707)
* Jetzt wird eine Fehlernachricht angezeigt, wenn versucht wird, einen integrierten Workflow zu importieren.

**Email Designer**

* Fehlerkorrektur – Jetzt wird die Funktion für die geografische Einheit auf einer E-Mail-Vorlage oder in einem Inhaltsfragment, die mit E-Mail-Designer erstellt wurden, nicht mehr aktiviert, obwohl diese Funktion in Adobe Campaign deaktiviert wurde. Zuvor war die Vorlage oder das Fragment nicht mehr verfügbar, wenn versucht wurde, nochmals auf sie zuzugreifen. (CAMP-28174)
* Fehlerkorrektur – Jetzt können Bedingungen für dynamische Inhalte während der Bearbeitung von Inhalt mit E-Mail-Designer gespeichert werden. (CAMP-27905)
* Fehlerkorrektur – Die HTML-Version wird jetzt nicht mehr aus dem E-Mail-Inhalt entfernt, nachdem die Textversion einer Nachricht bearbeitet und die HTML-Synchronisation in E-Mail-Designer aufgehoben wurde. (CAMP-28507)
* Fehlerkorrektur – Die Benutzeroberfläche von E-Mail-Designer kann jetzt bei der Verwendung von Internet Explorer 11 geöffnet werden. (CAMP-28273)
* Fehlerkorrektur – Die mit E-Mail-Designer auf Schaltflächen angewendeten Einstellungen werden jetzt auch in Microsoft Outlook korrekt dargestellt.
* Fehlerkorrektur – URLs in einem in einer E-Mail verwendeten Inhaltsfragment sind in E-Mail-Designer jetzt nicht mehr bearbeitbar. Dies war zuvor möglich, obwohl das Fragment standardmäßig gesperrt war.
* Fehlerkorrektur – Jetzt wird die Divisor-Komponente von E-Mail-Designer in Microsoft Office angezeigt.
* Fehlerkorrektur – Jetzt frieren in manchen Browsern keine Seiten mehr ein, wenn Inhalt angesehen wird, der mithilfe des bisherigen E-Mail-Inhaltseditors aus AEM synchronisiert wurde. (CAMP-29068)
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr auf, wenn unter Verwendung des bisherigen E-Mail-Inhaltseditors auf ein Bild in einer E-Mail geklickt wird. (CAMP-30424)
* Fehlerkorrektur – Jetzt ist es möglich, bei der Bearbeitung einer E-Mail mit E-Mail-Designer neu erstellte Fragmente anzuzeigen. (CAMP-29928)
* Fehlerkorrektur – Jetzt wird Schaltflächentext ordnungsgemäß in E-Mails angezeigt, die mit E-Mail-Designer erstellt und im Outlook Webmail Client empfangen wurden.
* Jetzt ist es möglich, mit E-Mail-Designer Profil-Transaktionsnachrichten zu erstellen. (CAMP-28900)
* Fehlerkorrektur – Jetzt ist Inhalt in E-Mail-Designer gesperrt, wenn er während der Vorbereitung automatisch von einer URL abgerufen wird. Zuvor konnte der Inhalt bearbeitet werden.

**Korrekturen**

* Fehlerkorrektur – In dynamischen Berichten werden jetzt korrekte Versandlogs angezeigt. (CAMP-23446)
* Fehlerkorrektur – Die Zahlen im Bounce-Zusammenfassungsbericht werden jetzt korrekt angezeigt (CAMP-28703).
* Fehlerkorrektur – Bei der Integration von Campaign mit Assets Core Service tritt jetzt kein Fehler mehr auf, sodass Assets immer angezeigt werden, wenn in einer E-Mail **[!UICONTROL Freigegebenes Bild von Adobe Experience Cloud]** ausgewählt wird (CAMP-28732).
* Fehlerkorrektur – Jetzt können SMS-Nachrichten, die den Buchstaben &quot;œ&quot; enthalten, gesendet werden. Zuvor war dies nicht möglich, selbst wenn die Transliteration im externen SMPP-Konto zugelassen wurde. (CAMP-29041)
* Fehlerkorrektur – Bei der Verwendung einer Segmentierungsaktivität in Workflows werden Datensätze nicht mehr doppelt angezeigt. (CAMP-28743)
* Fehlerkorrektur – In Workflow-Aktivitäten können Werte-Mappings im Bereich Neukodifizierung der Werte jetzt gelöscht werden. (CAMP-28708)
* Fehlerkorrektur – Bei der Verwendung von Platzhaltern in der Option &quot;Existenztest einer Datei&quot; tritt in der Dateitransferaktivität kein Fehler mehr auf. (CAMP-28977)
* Fehlerkorrektur – Bei der Aktualisierung der Einstellungen externer Konten tritt in der Dateitransferaktivität kein Fehler mehr auf. (CAMP-28894)
* Fehlerkorrektur – Bei der Verwendung der Bedingung &quot;E-Mail ist nicht leer&quot; tritt bei benutzerdefinierten Filtern im Abfrageeditor kein Fehler mehr auf. (CAMP-28741)
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr auf, wenn benutzerdefinierte Ressourcentabellen mit über 100.000 Datensätzen exportiert werden. (CAMP-28150)
* Fehlerkorrektur – Mit Triggers verknüpfte Transaktionsnachrichten können jetzt gelöscht werden. (CAMP-28385)
* Passwörter, die in manchen SMS-Logs angezeigt wurden und daher ein Sicherheitsrisiko darstellten, wurden entfernt.
* Fehlerkorrektur – Jetzt werden die Verbindungen zum SMPP Simulator nicht mehr unterbrochen. Das war der Fall, wenn von Adobe Campaign ein leeres Passwort gesendet wurde.
* Fehlerkorrektur – Jetzt können Kampagnen versendet werden, wenn SMS-Verbindungen instabil sind.
* Fehlerkorrektur – Gelöschte Sendungen werden jetzt nicht mehr in dynamischen Berichten angezeigt.
* Fehlerkorrektur – Zusatzdaten können jetzt aus Versandlogs, Trackinglogs und Ausschlusslog-Tabellen abgerufen werden, wenn in einem Workflow eine Anreicherungsaktivität verwendet wird.
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr bei DSGVO-Löschanfragen auf, wenn der Relationstyp &quot;Kollektionsrelation mit Kardinalität N&quot; und die Option &quot;Das Löschen des Zieldatensatzes zieht das Löschen der durch die Relation referenzierten Datensätze nach sich&quot; verwendet wird.
* Fehlerkorrektur – Bei der Berichtfreigabe tritt jetzt kein Fehler mehr auf.
* Fehlerkorrektur – Beim Versand von Push-Benachrichtigungen treten jetzt keine Durchsatzprobleme mehr auf.
* Fehlerkorrektur – In Briefpost-Ausgabedateien fehlen jetzt keine Felder mehr.
* Fehlerkorrektur – Benutzer können jetzt keine integrierten Workflows mehr ändern.
* Fehlerkorrektur – Bei der Erstellung einer Kampagne mit einer Kampagnenvorlage, die einen Workflow mit einer konfigurierten Dateiextraktionsaktivität enthält, tritt jetzt kein Fehler mehr auf (CAMP-29198)
* Fehlerkorrektur – Bei der Dateiextraktionsaktivität kann jetzt derselbe Ausdruck für mehrere Elemente verwendet werden. (CAMP-29182)
* Fehlerkorrektur – Jetzt tritt im Abfrageeditor bei der Join-Bedingung zwischen Broadlog und Trackinglog für rtEvent kein Fehler mehr auf. (CAMP-28780)
* Fehlerkorrektur – Jetzt können Änderungen an der Landingpage &quot;Spezifische Aktionen&quot; gespeichert werden. (CAMP-29422)
* Fehlerkorrektur – Jetzt kann die Payload eines Ereignisses in einem Workflow exportiert werden. (CAMP-29029)
* Fehlerkorrektur – Auf der Blockierungsliste stehende SMS-Nummern können jetzt von einer SMS-Nachricht ausgeschlossen werden. (CAMP-28898)
* Fehlerkorrektur – SMPP-Anbieter können jetzt im Fall eines Fehlers bei der Verarbeitung eingehender Nachrichten benachrichtigt werden. (CAMP-29804)
* Fehlerkorrektur – Externe Konten mit damit verbundenen Sendungen können jetzt nicht mehr gelöscht werden. (CAMP-29738)
* Der Versanddurchsatz für SMS-Nachrichten wurde verbessert und ist jetzt stabiler.
* Fehlerkorrektur – Das Zeichen &quot;~&quot; kann jetzt in SMS-Nachrichten verwendet werden. (CAMP-29172)
* Fehlerkorrektur – Bei der Option zur Versandzeitoptimierung tritt bei Sendungen kein Fehler mehr auf. (CAMP-29231)


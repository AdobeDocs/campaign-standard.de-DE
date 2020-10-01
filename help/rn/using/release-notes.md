---
title: Neueste Version
description: Auf dieser Seite finden Sie Informationen zum Inhalt der neuesten Version von Campaign Standard.
page-status-flag: never-activated
uuid: 1cf2e40c-beca-43db-8261-a1820ee86ad3
contentOwner: vignes
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: 5c7bfb74-4002-4ffe-87e8-bddb41d34b41
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7168162baa26c960475d8c9c613989d0338f95c2
workflow-type: tm+mt
source-wordcount: '2387'
ht-degree: 99%

---


# Neueste Version{#latest-release}

[Versionsplanung](../../rn/using/release-planning.md) | [Control Panel-Versionen](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html) | [Aktualisierungen der Dokumentation](../../rn/using/documentation-updates.md) | [Frühere Versionshinweise](../../rn/using/release-notes-2020.md) | [Eingestellte Funktionen](../../rn/using/deprecated-features.md)

## Version 20.4 – Oktober 2020 {#release-20-4---october-2020}

**Neue Funktionen**

<table> 
<thead> 
<tr> 
<th> <strong>Kontrollgruppen</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>Sie können jetzt <strong>Kontrollgruppen</strong> verwenden, um die Wirkung Ihrer Kampagnen zu messen, indem Sie einen Teil ihrer Audience ausschließen. Sie können dann das Verhalten der Zielpopulation, die die Nachricht erhalten hat, mit dem Verhalten der Kontakte vergleichen, die nicht in der Zielpopulation enthalten waren. Anhand der Versandlogs können Sie auch eine Kontrollgruppe in zukünftigen Kampagnen auswählen.
</p>
<p>Weiterführende Informationen finden Sie im <a href="../../sending/using/control-group.md">entsprechenden Handbuch</a> und im <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/communication-channels/email/control-groups.html">Anleitungsvideo</a>.
</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Externe API – OAuth-Unterstützung</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>Adobe Campaign unterstützt jetzt OAuth zur Authentifizierung in der Workflow-Aktivität <strong>Externe API</strong>. Diese neue Funktion ermöglicht es dieser Aktivität, mit Systemen zu kommunizieren, die OAuth-Unterstützung benötigen.
</p>
<p>Weitere Informationen finden Sie im <a href="../../automating/using/external-api.md">entsprechenden Handbuch</a>.
</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Integration von Journey AI</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>Wir freuen uns, Journey AI für alle Kunden von Adobe Campaign Standard anzukündigen.</p>
  <p>Journey AI nutzt fortschrittliches maschinelles Lernen (ML), um es Unternehmen zu ermöglichen, die Gestaltung und Bereitstellung von Customer Journeys zu optimieren, indem sie die Interaktionsvorlieben jedes Einzelnen vorhersagen.</p>
  <P>Journey AI besteht aus zwei ML-Funktionen:</p>
<ul> 
     <li> <strong>Prädiktive Interaktionsbewertung</strong>: Identifiziert auf intelligente Weise den bevorzugten Grad der Interaktion der Kunden, um Nachrichten besser auszurichten und zu personalisieren und so die Konversionen und die Kundenbindung zu erhöhen. Sehen Sie sich das <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/communication-channels/email/journey-ai/predictive-engagement-scoring.html">Anleitungsvideo</a> an.</li> 
     <li> <strong>Prädiktive Sendezeitoptimierung</strong> – Prognostiziert den bestmöglichen Zeitpunkt zum Senden von E-Mails an jede Einzelperson in einer Kampagne, um die Interaktionsraten zu maximieren und den ROI der E-Mail-Kampagne zu verbessern. Sehen Sie sich das <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/communication-channels/email/journey-ai/predictive-send-time-optimization.html">Anleitungsvideo</a> an.</li>
    </ul>
  <p>Wenn Sie erfahren möchten, wie Sie mit Journey AI beginnen, lesen Sie bitte das <a href="../../sending/using/predictive.md">entsprechende Handbuch</a> und wenden Sie sich an Ihren Kundenbetreuer. Beachten Sie, dass Journey AI für Bestandskunden von Campaign kostenlos erhältlich ist, die Implementierungskosten jedoch ca. 50 Stunden betragen.</p>
    </td> 
</tr> 
</tbody> 
</table>

**Verbesserungen**

* **Datenschutzverwaltung**: Das **CCPA-Opt-out**-Feld, das über die Campaign-Benutzeroberfläche und die API verfügbar war, wird jetzt auch über den Privacy Core Service unterstützt. In diesem Feld können Adobe Campaign-Benutzer verfolgen, ob ein Verbraucher sich vom Verkauf persönlicher Informationen abgemeldet hat. [Mehr dazu](https://helpx.adobe.com/content/help/de/campaign/kb/acs-privacy.html#ccpa)
* **Verbesserungen bei der Workflow-Ausführung** (Beta): Im Rahmen einer globalen Initiative für Workflows wurden einige wichtige Verbesserungen entwickelt, um die Speicherverwaltung zu stabilisieren, die Latenz zu verringern und den von Workflows während der Ausführung verbrauchten Speicher zu optimieren. Diese Verbesserungen befinden sich derzeit in der Beta-Phase und stehen nur einer Reihe von Kunden zur Verfügung. Die allgemeine Verfügbarkeit ist für Anfang 2021 geplant.
* Um die Sicherheit zu verbessern, verwendet Campaign jetzt einen **Signaturmechanismus** zum Verfolgen von Links in E-Mails.
* Die Konfiguration mobiler Apps wurde durch **klarere Fehlermeldungen** beim Hochladen von iOS-Zertifikaten oder Android-Schlüsseln verbessert.
* **Die Verwaltung von SMS- Fehlern** wurde verbessert, um zu verhindern, dass zu viele Profile zur Quarantäne-Liste hinzugefügt werden. Standardmäßig werden SMS-Fehler jetzt als Softbounces anstelle von Hardbounces konfiguriert. Mehr dazu erfahren Sie auf [dieser Seite](https://helpx.adobe.com/de/campaign/kb/sms-connector-protocol-and-settings.html).

**Verbesserungen bei Email Designer**

* Wir haben das Benutzererlebnis in Email Designer mit der **neuen dynamischen kontextbezogenen Hilfe** verbessert, die Benutzeroberfläche und Dokumentation vollständig miteinander verbindet und einen einfachen Zugriff auf die neuesten Hilfeinhalte bietet.
* Fehlerkorrektur – Zeilenumbrüche in einer Nachricht werden beim Bearbeiten der Textversion nicht mehr entfernt. (CAMP-44483)
* Fehlerkorrektur – Die Textversion einer HTML-Vorlage wird jetzt automatisch generiert und synchronisiert. (CAMP-44195)
* Fehlerkorrektur – Das Ändern der Bildgröße funktioniert jetzt richtig. Nach dem Senden der Nachrichten wurden die Bilder in Microsoft Outlook nicht richtig angezeigt. (CAMP-44656)
* Fehlerkorrektur – Das Einfügen einer Schaltfläche und Festlegen ihrer Breite auf &quot;Auto&quot; funktioniert jetzt richtig. Nach dem Senden der Nachricht wurde der Inhalt der Schaltfläche nicht vollständig angezeigt. (CAMP-44560)
* Fehlerkorrektur – Das Hochladen von Inhalten aus einer angehängten HTML-Datei funktioniert jetzt richtig. Nachdem die Nachricht an eine Gmail-Adresse gesendet wurde, wurde das CSS nicht angewendet, was zu einem Rendering-Problem führte. (CAMP-44085)
* Fehlerkorrektur – Zuvor in einer Nachricht verwendete Inhaltsfragmente werden jetzt aktualisiert, wenn sie direkt in der Inhaltsvorlage geändert werden. (CAMP-43973)
* Fehlerkorrektur – Die Suchleiste **Fragmente** funktioniert jetzt richtig. Bei der Suche nach einem vorhandenen Fragment wurde in der Suchleiste kein Ergebnis angezeigt. (CAMP-44223)
* Fehlerkorrektur – Die Suchleisten **Inhaltsbausteine** und **Fragmente** funktionieren jetzt richtig. Bei Verwendung einer der Suchleisten wurden die Ergebnisse nur angezeigt, wenn Sie **Weitere Ergebnisse anzeigen...** geklickt haben. (CAMP-44205)
* Fehlerkorrektur – Der Abstand zwischen Text und Bildern in Microsoft Outlook kann jetzt korrekt angewendet werden. (CAMP-45370)
* Fehlerkorrektur – Das Duplizieren eines Fragments funktioniert jetzt richtig. Nach dem Duplizieren des Fragments fehlten im ursprünglichen Fragment HTML-Zeilen. (CAMP-45207)
* Fehlerkorrektur – Rendering ist jetzt in Microsoft Outlook ohne Probleme möglich. (CAMP-44749)
* Fehlerkorrektur – Der Abstand einer **Strukturkomponente** kann jetzt in einer Versandvorlage richtig geändert werden. CSS-Tags übernahmen keine am Abstand vorgenommenen Änderungen, was zu einem Rendering-Problem führte. (CAMP-45381)
* Fehlerkorrektur – Das Hochladen eines Fragments funktioniert jetzt richtig. Die Höhe des Bilds wurde automatisch auf 0 eingestellt, wodurch ein Rendering-Problem auftrat. (CAMP-45366)

**Sonstige Änderungen**

* Es wurden Wiederholungsmechanismen für den Fall eines Fehlers beim Versuch hinzugefügt, eine Experience Platform-Audience mit der Aktivität **Audience lesen** zu importieren. (CAMP-43947, CAMP-43366)
* Organisationseinheiten werden jetzt automatisch auf die Organisationseinheit des Benutzers eingestellt, der das Profil oder die Entität erstellt. Organisationseinheiten können nicht mehr entfernt und leer gelassen werden.
* Beim Publizieren einer benutzerdefinierten Ressource wird jetzt nach der Vorbereitung ein Bestätigungs-Popup angezeigt.
* Die Popup-Meldung, die angezeigt wird, wenn eine benutzerdefinierte Ressource fehlschlägt, wurde verbessert.
* Der Ausdruckseditor in Workflows wurde verbessert, um Ausführungsfehler zu vermeiden.  Es stehen [neue Funktionen](../../automating/using/customizing-workflow-external-parameters.md) zur Verfügung: Sie können in allen Aktivitäten verwendet werden, die die Verwendung von Ereignisvariablen nach dem Aufruf eines Workflows mit externen Parametern ermöglichen. Zusätzlich wird jetzt im Ausdruckseditor eine QuickInfo mit der Funktionsbeschreibung angezeigt.
* [Zur Liste der Transaktionsereignisse wurden neue Filter hinzugefügt. ](../../administration/using/configuring-transactional-messaging.md#searching-transactional-events) Mit ihnen können Sie die Ereigniskonfigurationen nach ihrem Status sowie nach dem letzten Empfang eines Ereignisses filtern.
* Die Protokolle, die beim Exportieren von Packages angezeigt werden, wurden im Fehlerfall spezifischer und detaillierter hinsichtlich der aufgetretenen Fehler gestaltet.
* Nach dem Senden einer Nachricht können Sie jetzt die Liste der [getrackten URLs](../../sending/using/tracking-messages.md) durchsuchen, filtern und exportieren.
* Die automatische [Synchronisation zwischen Launch und Campaign](../../administration/using/configuring-a-mobile-application.md#aepsdk-workflow) ist jetzt allgemein verfügbar und standardmäßig aktiviert.
* Die Größe der Workflow-Export-Packages wurde optimiert, indem der Testversand-Export entfernt wurde.
* Es wurde eine neue Meldung hinzugefügt, um die Größe der heruntergeladenen Datei in der Aktivität **Dateiübertragung** anzuzeigen.
* Die Fehlermeldungen für ungültige Sitzungs-Token wurden verbessert.
* Ein neuer Mechanismus verhindert jetzt, dass Tracking-Ereignisse von Proxys zu Trackinglogs und Berichten hinzugefügt werden.
* Es wurde eine neue Warnmeldung hinzugefügt, die das Debugging von Datenverwaltungsaktivitäten unterstützt, die mit einer Versandaktivität verbunden sind.
* Die Beschriftungen im Reporting-Arbeitsbereich wurden verbessert.
* Es wurde ein neuer Validierungsschritt hinzugefügt, um das Löschen von technischen Objekten in Transaktionsnachrichten zu verhindern.
* Auf der Registerkarte **Liste der Ausführungen** einer Transaktionsnachricht wurde ein neuer Filter zum Versandstatus hinzugefügt, um die Fehlerbehebung zu verbessern.
* Um die Leistung zu verbessern und die Ausführungszeit zu optimieren, wurden unbenutzte Indizes entfernt, basierend auf den Nutzungsstatistiken von Tabellen, die in einer vorläufigen Analyse für mehr als 350 Kunden identifiziert wurden. Die betroffenen Tabellen sind: nmsaddressStatus, nmscampaign, nmsdelivery, nmslandingpage, nmsprogram, nmsempfänger, nmsseedmember, nmsservice, nmssubhistorcp, nmsaudience, xtkworkflow.

**Korrekturen**

* Fehlerkorrektur – Ziel-Links können jetzt für Push-Benachrichtigungen oder In-App-Nachrichten verwendet werden, wenn Tracking aktiviert ist.
* Es wurde ein Problem behoben, bei dem hohe Priorität in Transaktionsnachrichten nicht berücksichtigt wurde, wenn ein signifikanter Versand als Massenspeicher auftrat.
* Fehlerkorrektur – Marken können jetzt Transaktions-E-Mails zugewiesen werden. Während des Publikationsschritts konnten mehrere Fehlermeldungen angezeigt werden. (CAMP-44988)
* Fehlerkorrektur –Es können jetzt Informationen in Feldern in der Workflow-Benutzeroberfläche gespeichert werden, die numerische Werte erfordern. (CAMP-44025)
* Fehlerkorrektur – Beim Verwenden einer **Testaktivität** in einem Workflow für Importvorlagen wird keine Fehlermeldung mehr angezeigt. (CAMP-42910)
* Fehlerkorrektur – Es ist jetzt möglich, eine **Audience lesen**-Aktivität mit einem Auflistungstypfeld und in Verbindung mit den Aktivitäten **Vereinigung** und **Anreicherung** erfolgreich zu verwenden. (CAMP-42795)
* Fehlerkorrektur – In dynamische Berichten können jetzt native Segmente zum Filtern von Daten in Berichten problemlos verwendet werden. (CAMP-42627)
* Fehlerkorrektur – **Planungsaktivitäten** können jetzt auf 0 Uhr festlegt werden. (CAMP-42674)
* Fehlerkorrektur – SMS-Nachrichten können jetzt ohne Unterbrechung gesendet werden, wenn die SMPP-Verbindung instabil ist. (CAMP-42789)
* Fehlerkorrektur – Die Schaltfläche **Vorbereitung stoppen** wird jetzt nach dem Aktualisieren der Seite angezeigt. (CAMP-42721)
* Fehlerkorrektur – Die Prozentwerte für Klicks-Berichte werden jetzt angezeigt, wenn Inhalte aus einer URL importiert werden. (CAMP-44468)
* Fehlerkorrektur – Beim Auswählen eines Profils, das im Zusammenhang mit der Profilersetzung verwendet werden sollte, wird kein Timeout-Fehler mehr angezeigt. (CAMP-44746)
* Fehlerkorrektur – Instanzen funktionieren jetzt nach der Bereitstellung von benutzerdefinierten Ressourcen, die falsche Link-Definitionen enthalten. (CAMP-44406)
* Fehlerkorrektur – Es werden keine leeren verknüpften Entitäten (Typologien, Marken usw.) nach dem Kopieren und Einfügen eines Versands in eine Kampagnenvorlage erstellt. (CAMP-44765)
* Fehlerkorrektur – Im Falle eines Datenbankabsturzes oder eines einfachen Datenbankneustarts unter Azure werden Testsendungen nicht mehr aufgrund einer fehlerhaften Handhabung von Versandvorbereitungstabellen verhindert.
* Fehlerkorrektur – Es können jetzt Links mit Experience Manager-Inhalten in einem Versand mit mehrsprachigen Inhalten gelöscht werden. (CAMP-44029)
* Fehlerkorrektur – In dynamischen Berichten können Dimensionen jetzt gefiltert werden, ohne dass eine Fehlermeldung angezeigt wird. (CAMP-43097)
* Fehlerkorrektur – Beim Zugriff auf ein Profil in einer Instanz, die mit benutzerdefinierten Ressourcen konfiguriert ist, die bestimmte Linkdefinitionen enthalten, wird kein leerer Bildschirm mehr angezeigt. (CAMP-41009)
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr in Workflows auf, wenn eine Aktivität vom Typ **Anreicherung** mit zwei Eingabeaktivitäten verwendet wird, bei denen beide Zielgruppenressourcen verknüpft sind. (CAMP-42133)
* Fehlerkorrektur – Import-Workflows werden bei Verwendung der Aktivität **Dateiübertragung** nicht mehr wiederholt. (CAMP-43754)
* Fehlerkorrektur – Dubletten werden beim Erstellen eines Profils mit exportierten Logs jetzt berücksichtigt. (CAMP-45031)
* Fehlerkorrektur – Berichte in Adobe Campaign und in PDF-Dateien exportierte Berichte weisen keine Diskrepanzen mehr auf. (CAMP-43010)
* Fehlerkorrektur – Briefpostversand-Workflows funktionieren jetzt richtig, wenn bestehende Datenfelder in Funktionen verwendet werden. (CAMP-42737)
* Fehlerkorrektur – Der Import von Packages mit Transaktionsereignissen und Transaktionsnachrichten-Vorlagen funktioniert jetzt richtig. Der Importvorgang wurde bei 5 % angehalten. (CAMP-42544)
* Fehlerkorrektur – Nach dem Ändern der Aktivität **Anreicherung** und dem Hinzufügen zusätzlicher Daten in einem Workflow treten keine Fehler (Uncaught TypeError – nicht abgefangener Typfehler) mehr auf. (CAMP-41877)
* Fehlerkorrektur – Workflows können jetzt gelöscht werden. Die Logs mussten bereinigt werden, um den Workflow zu löschen. (CAMP-44144)
* Fehlerkorrektur – Landingpages mit HTML-Code können jetzt problemlos erstellt werden. Obligatorische Kontrollkästchen wurden in Campaign nicht erkannt und waren auf der publizierten Landingpage nicht verfügbar. (CAMP-44181)
* Fehlerkorrektur – Workflows werden bei Verwendung der Aktivität **Warten** nicht mehr wiederholt. (CAMP-43981)
* Fehlerkorrektur – Beim Senden von Transaktionsnachrichten kommt es nicht mehr vor, dass mehrere E-Mail-Adressen in einem Versand mehrmals als Ziel ausgewählt werden. (CAMP-44202)
* Fehlerkorrektur – Bei der Verwendung der Profilersetzung mit targetData-Personalisierung treten keine Fehler mehr auf. (CAMP-44996)
* Fehlerkorrektur – Die Versandvorschau kann beim Exportieren einer Versandvorlage in einem Package problemlos angezeigt werden. (CAMP-44084)
* Fehlerkorrektur – Testsendungen können jetzt an Testprofile gesendet werden, wenn benutzerdefinierte Zielgruppen-Mappings verwendet werden. (CAMP-43701)
* Fehlerkorrektur – In einem Workflow kann jetzt die Aktivität **Audience lesen** mit einer Audience mit einer anderen Zielgruppendimension als **Profil** verwendet werden. (CAMP-41885)
* Fehlerkorrektur – Wenn der technische Workflow **updateEventsStatus** zum Abrufen des Ereignisverlaufs zu lange benötigt (wenn der Workflow angehalten wird), treten keine Fehler mehr auf. Das nicht verwendete Aggregatfeld &quot;sumQueueTime&quot; wurde aus dem Workflow entfernt, um das Problem zu lösen. (CAMP-43920)
* Fehlerkorrektur – Bei der Bereitstellung benutzerdefinierter Ressourcen treten keine Speicherprobleme mehr auf. (CAMP-42909)
* Fehlerkorrektur – Wenn Attribute in Kollektionen fehlen, treten in Transaktionsnachrichten keine Fehler mehr auf. Jetzt werden alle fehlenden Attribute mit einem Standardwert definiert und in die Payload aufgenommen. (CAMP-42882)
* Fehlerkorrektur – Die Leistung bei Abfragen von Versandlogs der Echtzeit-Ereignisse wird nicht mehr beeinträchtigt. (CAMP-42759)
* Fehlerkorrektur – Dateierweiterungen in Großbuchstaben können jetzt mit freigegebenen Assets verwendet werden. (CAMP-44159)
* Fehlerkorrektur – Die Verbindung zu einem externen Konto kann nicht mehr vor dessen Erstellung getestet werden. Die Schaltfläche **Verbindung testen** wird jetzt erst nach Erstellung des externen Kontos angezeigt.
* Fehlerkorrektur – Nach dem Neustart des erweiterten MTA bei Instanzen mit Sharding-Konfiguration werden Nachrichten nicht mehr als ausstehend angezeigt.
* Fehlerkorrektur – Die Anzahl der aktiven Profile stimmt jetzt mit der tatsächlichen Anzahl der ausgeführten Sendungen überein.
* Fehlerkorrektur – Beim Suchen nach Ressourcen in einem Workflow im Abfrageeditor treten keine Latenzzeiten mehr auf.
* Fehlerkorrektur – Bei der Auswahl der Option **Bei der Textsuche berücksichtigte Felder definieren** in einer benutzerdefinierten Ressource treten kein Fehler mehr auf. Wenn die Liste des Felds leer gelassen wurde, schlug die Publikation der benutzerdefinierten Ressource fehl.
* Fehlerkorrektur – Beim Anzeigen der Übersicht über benutzerdefinierte Ressourcen mit einem großen Datenvolumen treten keine Leistungsprobleme mehr auf.
* Fehlerkorrektur – Es ist jetzt möglich, einen Versand mit Profilersetzungen zu importieren.
* Fehlerkorrektur – Wenn die Profilersetzung verwendet wird, können jetzt Testsendungen sofort ausgeführt werden, wenn der Versand geplant ist.
* Fehlerkorrektur – Beim Hochladen eines Android-Schlüssels für eine mobile App wurde ein Fehler behoben. In der Meldung, die nach dem erfolgreichen Hochladen des Schlüssels angezeigt wurde, wurde der Wert des vorherigen Schlüssels angezeigt.
* Fehlerkorrektur – Es können jetzt Testprofile von Transaktionsnachrichten erstellt werden, nachdem eine Ereigniskonfiguration mit einer Kollektion ohne Attribute erstellt wurde.
* Fehlerkorrektur – Benutzerdefinierte Ressourcen können jetzt publiziert werden, nachdem ein neuer Filter mit einem Aggregat erstellt wurde.
* Fehlerkorrektur – Die Öffnungsrate für Gmail-Empfänger wird jetzt korrekt getrackt. Dieser Fehler wurde durch den Gmail Image Proxy verursacht.
* Fehlerkorrektur – Beim Importieren von Packages treten keine Fehler wegen zu wenig Arbeitsspeicher mehr auf.
* Fehlerkorrektur – Die Aktion zum Aufheben der Verknüpfung von Experience Manager funktioniert jetzt, wenn der Experience Manager-Inhalt einen Pfad mit dem Zeichen &quot;%20&quot;enthält.
* Fehlerkorrektur –Beim Duplizieren von Workflow-Aktivitäten sind die Beschriftungen jetzt korrekt.
* Fehlerkorrektur – Auf einer Landingpage können jetzt Transaktionsnachrichten problemlos ausgewählt werden, wenn die Option **Absendung einer Nachricht auslösen** aktiviert ist.
* Fehlerkorrektur – Der Versandstatus wird jetzt bei Transaktionsnachrichten und beim wiederkehrenden Versand mit dem richtigen Standardwert initialisiert. Die Fehlerprotokolle wurden ebenfalls verbessert.
* Fehlerkorrektur – Das Schema **App-Abonnements** (appSubscriptionRcp) kann jetzt mit einem Profil-Link unter Verwendung eines benutzerdefinierten Felds erweitert werden. Der Index wurde nicht automatisch erstellt, was sich auf die Push-Sendezeit auswirken konnte. (CAMP-41120)


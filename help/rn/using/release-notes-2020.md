---
title: Versionshinweise 2020
description: Auf dieser Seite werden alle Versionen von Adobe Campaign Standard von 2020 aufgelistet.
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
feature: Overview
role: User
level: Beginner
hidefromtoc: true
exl-id: b6cf7152-2200-43d7-8d0a-d65752bb2c9b
source-git-commit: 1d8baca669235be10d373d985ea62f6f014c16f8
workflow-type: tm+mt
source-wordcount: '5272'
ht-degree: 100%

---

# Versionshinweise 2020{#release-notes-2020}

![](assets/do-not-localize/cp-icon.png) **Neue Control Panel-Version im Juni** mit der Überwachung aktiver Profile, der Prüfung der Subdomain-Zustellbarkeit und der GPG-Schlüsselverwaltung. [Weitere Informationen](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html?lang=de).

![](assets/do-not-localize/cp-icon.png) **Neue Control Panel-Version vom Oktober** mit Domain-Konfiguration unter Verwendung von CNAMEs und neuen Funktionen zur Datenbanküberwachung. [Weitere Informationen](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html?lang=de).

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
<p>Weiterführende Informationen finden Sie im <a href="../../sending/using/control-group.md">entsprechenden Handbuch</a> und im <a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/email/control-groups.html">Anleitungsvideo</a>.
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
<th> <strong>Integration von Journey-KI</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>Wir freuen uns, Journey-KI für alle Kunden von Adobe Campaign Standard anzukündigen.</p>
  <p>Journey-KI nutzt fortschrittliches maschinelles Lernen (ML), um es Unternehmen zu ermöglichen, die Gestaltung und den Versand von Customer Journeys zu optimieren, indem sie die Interaktionsvorlieben jeder und jedes Einzelnen vorhersagen.</p>
  <P>Journey-KI besteht aus zwei ML-Funktionen:</p>
<ul> 
     <li> <strong>Prädiktive Interaktionsbewertung</strong>: Identifiziert auf intelligente Weise den bevorzugten Grad der Interaktion der Kunden, um Nachrichten besser auszurichten und zu personalisieren und so die Konversionen und die Kundenbindung zu erhöhen. Sehen Sie sich das <a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/email/journey-ai/predictive-engagement-scoring.html?lang=de">Anleitungsvideo</a> an.</li> 
     <li> <strong>Prädiktive Sendezeitoptimierung</strong> – Prognostiziert den bestmöglichen Zeitpunkt zum Senden von E-Mails an jede Einzelperson in einer Kampagne, um die Interaktionsraten zu maximieren und den ROI der E-Mail-Kampagne zu verbessern. Sehen Sie sich das <a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/email/journey-ai/predictive-send-time-optimization.html?lang=de">Anleitungsvideo</a> an.</li>
    </ul>
  <p>Wenn Sie erfahren möchten, wie Sie mit Journey-KI beginnen, lesen Sie bitte das <a href="../../sending/using/predictive.md">entsprechende Handbuch</a> und wenden Sie sich an Ihren Kundenbetreuer. Beachten Sie, dass Journey-KI für Bestandskunden von Campaign kostenlos erhältlich ist, die Implementierungskosten jedoch ca. 50 Stunden betragen.</p>
    </td> 
</tr> 
</tbody> 
</table>

**Verbesserungen**

* **Datenschutzverwaltung**: Das **CCPA-Opt-out**-Feld, das über die Campaign-Benutzeroberfläche und die API verfügbar war, wird jetzt auch über den Privacy Core Service unterstützt. In diesem Feld können Adobe Campaign-Benutzer verfolgen, ob ein Verbraucher sich vom Verkauf personenbezogener Informationen abgemeldet hat. [Mehr dazu](https://helpx.adobe.com/content/help/de/campaign/kb/acs-privacy.html#ccpa)
* **Verbesserungen bei der Workflow-Ausführung** (Beta): Im Rahmen einer globalen Initiative für Workflows wurden einige wichtige Verbesserungen entwickelt, um die Speicherverwaltung zu stabilisieren, die Latenz zu verringern und den von Workflows während der Ausführung verbrauchten Speicher zu optimieren. Diese Verbesserungen befinden sich derzeit in der Betaversion und stehen nur einer Reihe von Kunden zur Verfügung. Die allgemeine Verfügbarkeit ist für Anfang 2021 geplant.
* Um die Sicherheit zu verbessern, verwendet Campaign jetzt einen **Signaturmechanismus** zum Verfolgen von Links in E-Mails.
* Die Konfiguration mobiler Apps wurde durch **klarere Fehlermeldungen** beim Hochladen von iOS-Zertifikaten oder Android-Schlüsseln verbessert.
* **Die Verwaltung von SMS- Fehlern** wurde verbessert, um zu verhindern, dass zu viele Profile zur Quarantäne-Liste hinzugefügt werden. Standardmäßig werden SMS-Fehler jetzt als Softbounces anstelle von Hardbounces konfiguriert. Mehr dazu erfahren Sie auf [dieser Seite](https://helpx.adobe.com/de/campaign/kb/sms-connector-protocol-and-settings.html).

**Verbesserungen bei Email Designer**

* Wir haben das Benutzererlebnis in Email Designer mit der **neuen dynamischen kontextuellen Hilfe** verbessert, die Benutzeroberfläche und Dokumentation vollständig miteinander verbindet und einen einfachen Zugriff auf die neuesten Hilfeinhalte bietet.
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
* Beim Veröffentlichen einer benutzerdefinierten Ressource wird jetzt nach der Vorbereitung ein Bestätigungs-Popup angezeigt.
* Die Popup-Meldung, die angezeigt wird, wenn eine benutzerdefinierte Ressource fehlschlägt, wurde verbessert.
* Der Ausdruckseditor in Workflows wurde verbessert, um Ausführungsfehler zu vermeiden.  Es stehen [neue Funktionen](../../automating/using/customizing-workflow-external-parameters.md) zur Verfügung: Sie können in allen Aktivitäten verwendet werden, die die Verwendung von Ereignisvariablen nach dem Aufruf eines Workflows mit externen Parametern ermöglichen. Zusätzlich wird jetzt im Ausdruckseditor eine QuickInfo mit der Funktionsbeschreibung angezeigt.
* [Zur Liste der Transaktionsereignisse wurden neue Filter hinzugefügt. ](../../channels/using/configuring-transactional-event.md#searching-transactional-events) Mit ihnen können Sie die Ereigniskonfigurationen nach ihrem Status sowie nach dem letzten Empfang eines Ereignisses filtern.
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
* Um die Performance zu verbessern und die Ausführungszeit zu optimieren, wurden unbenutzte Indizes entfernt, basierend auf den Nutzungsstatistiken von Tabellen, die in einer vorläufigen Analyse für mehr als 350 Kunden identifiziert wurden. Die betroffenen Tabellen sind: nmsaddressStatus, nmscampaign, nmsdelivery, nmslandingpage, nmsprogram, nmsempfänger, nmsseedmember, nmsservice, nmssubhistorcp, nmsaudience, xtkworkflow.

**Korrekturen**

* Fehlerkorrektur – Ziel-Links können jetzt für Push-Benachrichtigungen oder In-App-Nachrichten verwendet werden, wenn Tracking aktiviert ist.
* Fehlerkorrektur – Bei einem gebündelten Versand mit hoher Priorität wird diese jetzt in Transaktionsnachrichten berücksichtigt.
* Fehlerkorrektur – Marken können jetzt Transaktions-E-Mails zugewiesen werden. Während des Veröffentlichungsschritts konnten mehrere Fehlermeldungen angezeigt werden. (CAMP-44988)
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
* Fehlerkorrektur – Landingpages mit HTML-Code können jetzt problemlos erstellt werden. Obligatorische Kontrollkästchen wurden in Campaign nicht erkannt und waren auf der veröffentlichten Landingpage nicht verfügbar. (CAMP-44181)
* Fehlerkorrektur – Workflows werden bei Verwendung der Aktivität **Warten** nicht mehr wiederholt. (CAMP-43981)
* Fehlerkorrektur – Beim Senden von Transaktionsnachrichten kommt es nicht mehr vor, dass mehrere E-Mail-Adressen in einem Versand mehrmals als Ziel ausgewählt werden. (CAMP-44202)
* Fehlerkorrektur – Bei der Verwendung der Profilersetzung mit targetData-Personalisierung treten keine Fehler mehr auf. (CAMP-44996)
* Fehlerkorrektur – Die Versandvorschau kann beim Exportieren einer Versandvorlage in einem Package problemlos angezeigt werden. (CAMP-44084)
* Fehlerkorrektur – Testsendungen können jetzt an Testprofile gesendet werden, wenn benutzerdefinierte Zielgruppen-Mappings verwendet werden. (CAMP-43701)
* Fehlerkorrektur – In einem Workflow kann jetzt die Aktivität **Audience lesen** mit einer Audience mit einer anderen Zielgruppendimension als **Profil** verwendet werden. (CAMP-41885)
* Fehlerkorrektur – Wenn der technische Workflow **updateEventsStatus** zum Abrufen des Ereignisverlaufs zu lange benötigt (wenn der Workflow angehalten wird), treten keine Fehler mehr auf. Das nicht verwendete Aggregatfeld &quot;sumQueueTime&quot; wurde aus dem Workflow entfernt, um das Problem zu lösen. (CAMP-43920)
* Fehlerkorrektur – Bei der Bereitstellung benutzerdefinierter Ressourcen treten keine Speicherprobleme mehr auf. (CAMP-42909)
* Fehlerkorrektur – Wenn Attribute in Sammlungen fehlen, treten in Transaktionsnachrichten keine Fehler mehr auf. Jetzt werden alle fehlenden Attribute mit einem Standardwert definiert und in die Payload aufgenommen. (CAMP-42882)
* Fehlerkorrektur – die Performance bei Abfragen von Versandlogs der Echtzeit-Ereignisse wird nicht mehr beeinträchtigt. (CAMP-42759)
* Fehlerkorrektur – Dateierweiterungen in Großbuchstaben können jetzt mit freigegebenen Assets verwendet werden. (CAMP-44159)
* Fehlerkorrektur – Die Verbindung zu einem externen Konto kann nicht mehr vor dessen Erstellung getestet werden. Die Schaltfläche **Verbindung testen** wird jetzt erst nach Erstellung des externen Kontos angezeigt.
* Fehlerkorrektur – Nach dem Neustart des erweiterten MTA bei Instanzen mit Sharding-Konfiguration werden Nachrichten nicht mehr als ausstehend angezeigt.
* Fehlerkorrektur – Die Anzahl der aktiven Profile stimmt jetzt mit der tatsächlichen Anzahl der ausgeführten Sendungen überein.
* Fehlerkorrektur – Beim Suchen nach Ressourcen in einem Workflow im Abfrageeditor treten keine Latenzen mehr auf.
* Fehlerkorrektur – Bei der Auswahl der Option **Bei der Textsuche berücksichtigte Felder definieren** in einer benutzerdefinierten Ressource treten kein Fehler mehr auf. Wenn die Liste des Felds leer gelassen wurde, schlug die Veröffentlichung der benutzerdefinierten Ressource fehl.
* Fehlerkorrektur – Beim Anzeigen der Übersicht über benutzerdefinierte Ressourcen mit einem großen Datenvolumen treten keine Performance-Probleme mehr auf.
* Fehlerkorrektur – Es ist jetzt möglich, einen Versand mit Profilersetzungen zu importieren.
* Fehlerkorrektur – Wenn die Profilersetzung verwendet wird, können jetzt Testsendungen sofort ausgeführt werden, wenn der Versand geplant ist.
* Fehlerkorrektur – Beim Hochladen eines Android-Schlüssels für eine mobile App wurde ein Fehler behoben. In der Meldung, die nach dem erfolgreichen Hochladen des Schlüssels angezeigt wurde, wurde der Wert des vorherigen Schlüssels angezeigt.
* Fehlerkorrektur – Es können jetzt Testprofile von Transaktionsnachrichten erstellt werden, nachdem eine Ereigniskonfiguration mit einer Sammlung ohne Attribute erstellt wurde.
* Fehlerkorrektur – Benutzerdefinierte Ressourcen können jetzt veröffentlicht werden, nachdem ein neuer Filter mit einem Aggregat erstellt wurde.
* Fehlerkorrektur – Die Öffnungsrate für Gmail-Empfänger wird jetzt korrekt getrackt. Dieser Fehler wurde durch den Gmail Image Proxy verursacht.
* Fehlerkorrektur – Beim Importieren von Packages treten keine Fehler wegen zu wenig Arbeitsspeicher mehr auf.
* Fehlerkorrektur – Die Aktion zum Aufheben der Verknüpfung von Experience Manager funktioniert jetzt, wenn der Experience Manager-Inhalt einen Pfad mit dem Zeichen &quot;%20&quot;enthält.
* Fehlerkorrektur –Beim Duplizieren von Workflow-Aktivitäten sind die Beschriftungen jetzt korrekt.
* Fehlerkorrektur – Auf einer Landingpage können jetzt Transaktionsnachrichten problemlos ausgewählt werden, wenn die Option **Absendung einer Nachricht auslösen** aktiviert ist.
* Fehlerkorrektur – Der Versandstatus wird jetzt bei Transaktionsnachrichten und beim wiederkehrenden Versand mit dem richtigen Standardwert initialisiert. Die Fehlerprotokolle wurden ebenfalls verbessert.
* Fehlerkorrektur – Das Schema **App-Abonnements** (appSubscriptionRcp) kann jetzt mit einem Profil-Link unter Verwendung eines benutzerdefinierten Felds erweitert werden. Der Index wurde nicht automatisch erstellt, was sich auf die Push-Sendezeit auswirken konnte. (CAMP-41120)



## Version 20.3 – Mai 2020 {#release-20-3---may-2020}

**Neue Funktionen**

<table> 
<thead> 
<tr> 
<th> <strong>Thailändisches Datenschutzgesetz (PDPA)</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td> <p>Das thailändische Datenschutzgesetz (PDPA) ist ein neues Datenschutzgesetz, mit dem die Datenschutzanforderungen für Thailand harmonisiert und modernisiert werden. Diese Verordnung gilt für Adobe Campaign-Kunden, die Daten von Personen erfassen, die in diesem Land wohnhaft sind.</p>
<p>Zusätzlich zu den bereits in Adobe Campaign verfügbaren Datenschutzoptionen (Einverständnisverwaltung, Einstellungen für die Datenbeibehaltung und Benutzerrollen usw.) werden daher weitere Funktionen bereitgestellt, mit deren Hilfe PDPA-konformes Verhalten sichergestellt werden kann:</p>
<ul>
<li>Recht auf Zugriff und Recht auf Löschung: Hierfür werden die Funktionen genutzt, die für die DSGVO und PPDA hinzugefügt wurden – <a href="https://helpx.adobe.com/content/help/de/campaign/kb/acs-privacy.html#righttoaccess">mehr dazu</a> </li>
<li><p>Bei der Erstellung einer Datenschutzanfrage steht im Privacy Core Service nun eine Auswahl für die PDPA-Verordnung zur Verfügung. Diese Methode sollten Sie für Anfragen auf Datenzugriff bzw. -löschung verwenden. Die Campaign-API und -Schnittstelle für Zugriffs- und Löschanfragen wurde eingestellt.  Weitere Informationen dazu finden Sie im Artikel <a href="../../rn/using/deprecated-features.md">Eingestellte und entfernte Funktionen</a>.</p></li>
</ul>
<p>Weitere Informationen finden Sie in <a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/privacy/privacy-overview.html?lang=de">diesem Video</a>.</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Externe API-Aktivität (allgemeine Verfügbarkeit)</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>Die <strong>externe API-Aktivität </strong> wechselt von der Betaversion in die allgemeine Verfügbarkeit. Diese Version bietet zusätzliche Flexibilität für das Parsen des Textes von JSON-Antworten. Sie können jetzt:</p>
<ul>
<li>eine verschachtelte JSON mit einer maximalen Tiefe von zehn Ebenen analysieren; </li>
<li>ausgewählte Eigenschaften als Blattknoten aus einer JSON analysieren und auf eine Tabellenzeile abflachen;</li>
<li>ein Array-Objekt aus einer JSON auswählen und verwenden, ohne die "Objektdaten" benennen zu müssen oder ohne dass sie sich auf der obersten Ebene befinden müssen.</li>
</ul>
<p><strong>Vorsicht:</strong> Kunden müssen in ihren Workflows alle externen API-Aktivitäten der Betaphase <strong>durch externe API-Aktivitäten der allgemeinen Verfügbarkeit</strong> ersetzen.  Workflows, die die Betaversion der externen API verwenden, funktionieren in 20.3 nicht mehr.</p>
<p>Weiterführende Informationen finden Sie im <a href="../../automating/using/external-api.md">entsprechenden Handbuch</a> und in <a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/managing-processes-and-data/data-management-activities/external-api-activity.html?lang=de">diesem Video</a>.</p>
</td> 
</tr> 
</tbody> 
</table>

**Zusätzliche Funktionen** (ab 13. Juli)

* **KI-gestützte Sendezeitoptimierung und Profilbewertung**: Sie können jetzt Design und Versand von Customer Journeys optimieren, um die Interaktionsvorlieben jedes Einzelnen vorherzusagen. Mit Journey-KI kann Adobe Campaign Öffnungsraten, optimale Sendezeiten und wahrscheinliche Abwanderungszahlen anhand historischer Interaktionsmetriken analysieren und vorhersagen. [Mehr dazu](../../sending/using/predictive.md)
* **Brasiliens neue Datenschutzverordnung**: Zusätzlich zu den bereits in Campaign verfügbaren Datenschutzfunktionen hilft Ihnen Adobe, LGPD-konformes Verhalten (LGPD: brasilianische Datenschutzverordnung Lei Geral de Proteção de Datos) sicherzustellen. Bei der Erstellung einer Datenschutzanfrage wurde dem Privacy Core Service die LGPD-Verordnung hinzugefügt. [Mehr dazu](https://helpx.adobe.com/de/campaign/kb/campaign-privacy-overview.html)

**Verbesserungen**

* Die Anzahl der Zeichen, die im Feld **Präfix** zum [Testen von Nachrichten mit Zielgruppenprofilen](../../sending/using/testing-messages-using-target.md) verwendet werden können, wurde von 32 auf 500 Zeichen erhöht.
* Die maximale Anzahl von Echtzeit-Ereignissen, die in einer Instanz veröffentlicht werden können, wurde von 350 auf 2.000 erhöht. (CAMP-41608)
* Die Synchronisation zwischen Adobe Launch und Campaign Standard wurde mithilfe des technischen Workflows syncWithLaunch verbessert. Dieser Workflow ermöglicht den automatischen Import aller Adobe Launch-Eigenschaften für Mobilgeräte in Adobe Campaign Standard. Weiterführende Informationen dazu finden Sie auf dieser [Seite](../../administration/using/technical-workflows.md).

  Sie müssen ein Ticket an die Adobe-Kundenunterstützung senden (entweder direkt oder über Ihren Adobe-Ansprechpartner), damit der technische Workflow syncWithLaunch in Ihrer Campaign-Instanz aktiviert wird. (CAMP-40082)

**Verbesserungen bei Email Designer**

* Email Designer kann jetzt eine flexiblere HTML-Formatierung als das strikte W3C-Format handhaben. (CAMP-42529)
* Bei [klickbaren Bildern](../../designing/using/links.md#inserting-a-link) werden jetzt in Inhaltsbausteinen neben dem Bild keine Links mehr angezeigt. (CAMP-41586)
* Die Weiterleitung zu einer Landingpage ist jetzt möglich, wenn der [getrackten URL](../../designing/using/links.md#about-tracked-urls) in der Vorlage eine Kategorie hinzugefügt wurde. (CAMP-41537)
* Mit dem Abstand von Schaltflächen in Outlook besteht jetzt kein Problem mehr.
* HTML-Tags werden jetzt nicht mehr im Klartext angezeigt.
* Bei der Suche nach Inhaltsbausteinen werden jetzt die Suchergebnisse des Servers sowie vorab geladene Ergebnisse angezeigt. (CAMP-41870)

**Sonstige Änderungen**

* Die Benutzeroberfläche für die Veröffentlichung benutzerdefinierter Ressourcen wurde mit klareren Fehlermeldungen ausgestattet.
* Nicht verwendete Versand-Mappings wurden aus der Benutzeroberfläche entfernt.
* Unnötige Administratorrollen wurden aus der Benutzeroberfläche entfernt.
* Checkboxes können in einer Landingpage jetzt zu Pflichtfeldern gemacht werden.
* Beim Herunterladen der CSV-Datei eines dynamischen Berichts wurde das Limit von 200 Zeilen entfernt. Sie können jetzt jede Zeile Ihres Berichts einschließen. (CAMP-40810)
* Die Sprache ES-US wurde der Liste nativer Sprachen für mehrsprachige E-Mails hinzugefügt. (CAMP-42279)
* Dateien, die mit einer Dateiübertragungs-Aktivität heruntergeladen wurden, werden nun nach X Tagen gelöscht, wobei X durch das Feld **Verlauf in Tagen** unter dem Menü **Ausführung** in den Workflow-Eigenschaften bestimmt wird. [Mehr dazu](../../automating/using/managing-execution-options.md)

**Experience Platform-Integrationen**

* Die Aktivierung von Adobe Experience Platform-Zielgruppen über die Aktivität **Zielgruppe lesen** wurde verbessert, um eine höhere Performance und Stabilität zu erzielen. Darüber hinaus wurden Workflow-Logs in Bezug auf Aktivierungsvorgänge klarer und detaillierter gestaltet, was eine einfachere Überwachung und Fehlerbehebung beim Lesen von Adobe Experience Platform-Audiences ermöglicht.

**Patches**

* Während des Veröffentlichungsvorgangs einer benutzerdefinierten Ressource wird keine Geisterressource mehr erstellt.
* Die Anzeige des Marketing-Verlaufs von Profilen wird nicht mehr verhindert, wenn die Profilressource mit einer benutzerdefinierten Ressource erweitert wird. (CAMP-41009)
* Der Inhalt von nativen Landingpage-Vorlagen wird beim Öffnen des Editors nicht mehr in französischer Sprache angezeigt. (CAMP-41639)
* In Push-Benachrichtigungen mit dynamischem Inhalt wird nicht mehr Anzeige von Emojis verhindert. (CAMP-40715)
* In der Aktivität **Deduplizierung** wird einer der ausgehenden komplementären Transitionen kein falscher Segment-Code mehr zugewiesen. (CAMP-41400)
* Das Löschen geplanter Berichte wird jetzt nicht mehr verhindert. (CAMP-41302)
* Zwischen dem Versand-Dashboard und dem Bericht **Versandzusammenfassung** bestehen keine Abweichungen mehr. (CAMP-41145)
* In heruntergeladenen Berichten tritt jetzt kein Anzeigeproblem mit Zeichenüberschneidungen mehr auf.
* Bei Testversandersetzungen funktioniert jetzt die Vorschau eines Versands.
* Beim Löschen benutzerdefinierter Felder einer lokalen In-App-Benachrichtigung tritt jetzt kein Fehler mehr auf.
* Die Funktion &quot;charIndex&quot; funktioniert jetzt in einem Workflow mit einer **Ende**- oder **Dateiübertragungs**-Aktivität.
* Jetzt tritt kein Fehler mehr in Workflows auf, wenn eine Aktivität vom Typ **Anreicherung** mit zwei Eingabeaktivitäten verwendet wurde, einschließlich Zielgruppenressourcen, die eine Relation zueinander aufweisen. (CAMP-42133)
* Die Ausführung eines Workflows bei Verwendung unbekannter Funktionen ist jetzt möglich. (CAMP-41873)
* Beim Erstellen von Zielgruppen mithilfe mehrerer Aktivitäten vom Typ **Zielgruppe speichern** mit komplementären ausgehenden Transitionen tritt jetzt kein Problem mehr auf. (CAMP-39992)
* Bei der Verwendung von Personalisierung in Transaktions-E-Mails treten jetzt keine Datenabweichungen mehr auf. (CAMP-41842)
* Beim Löschen von benutzerdefinierten Feldern in Sendungen mit Push-Benachrichtigungen tritt jetzt kein Problem mehr auf. (CAMP-37586)
* Benutzer können jetzt Änderungen an Berichten vornehmen. (CAMP-42505)


![](assets/do-not-localize/cp-icon.png) **Neue Control Panel-Version im Mai** mit Zertifikatsverlängerung für CNAME-Subdomains. [Mehr dazu](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html?lang=de).

## Version 20.2 – April 2020 {#release-20-2---april-2020}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> <strong>Azure Blob-Integration</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Der Azure Blob Storage-Connector kann jetzt mithilfe einer Workflow-Aktivität vom Typ <strong>Dateiübertragung</strong> zum Importieren oder Exportieren von Daten in Adobe Campaign verwendet werden. </p>
    <p>Weitere Informationen finden Sie im <a href="../../administration/using/external-accounts.md#microsoft-azure-external-account">entsprechenden Handbuch</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Testen von E-Mails mit Zielgruppenprofilen</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Zusätzlich zu Testprofilen können Sie Ihre E-Mails jetzt mit echten Zielgruppenprofilen testen. So können Sie eine genaue Darstellung der Nachricht erhalten, die das Profil empfangen wird: benutzerdefinierte Felder, dynamische und personalisierte Informationen, einschließlich zusätzlicher Daten aus Workflows usw. </p>
    <p>Weiterführende Informationen finden Sie im <a href="../../sending/using/testing-messages-using-target.md">entsprechenden Handbuch</a> und in diesem <a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/communication-channels/email/profile-substitution.html?lang=de">Tutorial-Video</a>. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Im April werden im Control Panel von Campaign neue Funktionen veröffentlicht, einschließlich der Google TXT-Datensatzverwaltung, der Überwachung der Datenbankkapazität und eines E-Mail-Warnsystems. Weiterführende Informationen zu diesen Funktionen finden Sie im [Versionshinweis zum Control Panel](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html?lang=de).

**Verbesserungen**

* Das Anwendererlebnis beim Transaktionsnachrichtenversand wurde verbessert; zudem wurde die Konsistenz der Benutzeroberfläche erhöht. [mehr dazu](../../channels/using/getting-started-with-transactional-msg.md)
* Campaign Standard ermöglicht es Ihnen jetzt, mithilfe zusätzlicher Daten aus Workflows Testsendungen an Testprofile vorzunehmen.
* Schutzmaßnahmen für die externe API-Aktivität wurden aktualisiert. [Mehr dazu](../../automating/using/external-api.md)

**Verbesserungen bei Email Designer**

* Jetzt tritt kein Fehler mehr beim Escapen auf, wenn ein personalisiertes Bild mehrmals angeklickt wird.
* Beim Duplizieren dynamischer Textkomponenten wird nicht mehr die falsche Zeile dupliziert. (CAMP-41249)
* Beim Abstand in Outlook tritt jetzt kein Fehler mehr auf, wenn der Abstand auf Tabellenebene anstatt auf div-Ebene definiert wird.
* Die Breite eines Bilds ändert sich beim Wechsel in den HTML-Modus nicht mehr. (CAMP-41116)
* Auf die Social-Media-Komponente kann jetzt auch dann zugegriffen werden, wenn Alternativtext für die Symbole angegeben wird. (CAMP-41345)
* Beim Kopieren und Einfügen in Email Designer werden jetzt keine sichtbaren `<br>`-Tags mehr angezeigt.
* HTML-Tags werden jetzt nicht mehr in der E-Mail angezeigt, wenn von HTML-Inhalten auf Nur-Text umgestellt wird. (CAMP-41138)
* Das Rendering von Schaltflächen ist jetzt auch mit nur einem definierten Rand möglich.
* Beim HTML-Einzug wird jetzt die Fußzeile von E-Mails in Microsoft Outlook nicht mehr nach links verschoben. (CAMP-40987)
* Personalisierungsfelder, die ein in HTML definiertes Sammlungsattribut verwenden, werden jetzt beim Wechsel zum Nur-Text-Modus nicht mehr in den Nur-Text-Inhalt kopiert. (CAMP-40365)
* Links können jetzt in ein ausgewähltes Textsegment eingefügt wurden. (CAMP-41406)
* Beim Auswählen einer Zeitzone im Abfrageeditor wird jetzt das Datum geändert. (CAMP-38277)

**Sonstige Änderungen**

* Der native Workflow **KPI-Abstimmung mit Adobe Analytics** wird jetzt bis zum aktuellen Datum anstatt nur einen Tag lang ausgeführt.
* Das Hinzufügen von sowohl APNS als auch APNS-SANDBOX als Plattformen in einer App wird von MCPNS nicht unterstützt. Nachdem Sie das Zertifikat in Adobe Campaign Standard erfolgreich hinzugefügt haben, können Sie Ihre Einstellungen jetzt nicht mehr ändern, da der MCPNS-App nur eine APNS-Plattform (Produktion oder Sandbox) hinzugefügt werden kann.

**Experience Platform-Integrationen**

>[!NOTE]
>
>Adobe Experience Platform-Funktionen in Campaign Standard befinden sich derzeit in der Betaversion und können daher häufig ohne Vorankündigung aktualisiert werden. Weiterführende Informationen finden Sie im entsprechenden Handbuch: Experience Platform-Daten-Connector, Zielgruppen-Ziele

* In den Workflow-Protokollen zeigt Campaign nun alle zehn Minuten die Anzahl der Datensätze an, die vom derzeit ausgeführten Auftrag bereits verarbeitet wurden.
* Ein Adobe Experience Platform-Profil, das aus der Datenbank gelöscht worden war, kann jetzt problemlos importiert werden.
* In Workflow-Protokollen wird jetzt für die Gesamtzahl der importierten Datensätze kein falsches Ergebnis mehr angezeigt.

**Korrekturen**

* Bei der Workflow-Aktivität **Anreicherung** wird beim Hinzufügen von Leerzeichen im Feld **Alias** kein neues Zeilenelement mehr erstellt. (CAMP-39229)
* Bei der Durchführung eines Testversands kann jetzt nicht mehr jedes beliebige Testprofil als Zielgruppe ausgewählt werden.
* Nach der Aufhebung der Veröffentlichung und Löschung einer Ereigniskonfiguration tritt jetzt kein Fehler mehr auf. [Mehr dazu](../../channels/using/publishing-transactional-event.md#deleting-an-event)
* Die Schaltfläche **Speichern** verschwindet jetzt nicht mehr, wenn Änderungen an Workflows vorgenommen werden.
* Beim manuellen Löschen einer Datenschutzanfrage in Campaign können nach deren Verarbeitung die mit der Anfrage verknüpften Daten auch nach der Bereinigung gelöscht werden.
* Beim Anzeigen einer Vorschau oder beim Senden von Nachrichten mit Sonderzeichen aus Adobe Experience Manager tritt jetzt kein Fehler mehr auf.
* Jetzt kann in Workflows eine Aktivität mit mehreren eingehenden Transitionen problemlos ausgeführt werden.
* Standardbenutzer können &quot;Abonnements für eine Anwendung&quot; jetzt als Zieldimension in einer Workflow-Abfrage oder einem Versand verwenden. (CAMP-37618)

## Version 20.1.4 – Februar 2020 {#release-20-1-4---february-2020}

* Beim Öffnen der Aktivität **Audience lesen** in vorhandenen Workflows tritt jetzt kein Problem mehr auf. (CAMP-41002)

## Version 20.1.3 – Februar 2020 {#release-20-1-3---february-2020}

* Jetzt tritt kein Regressionsproblem mehr auf, das in 20.1 von CAMP-39273 für Kunden eingeführt wurde, die diese Lücke nutzten. CAMP-39273 wurde zurückgesetzt.

## Version 20.1.2 – Februar 2020 {#release-20-1-2---february-2020}

**Verbesserungen bei Email Designer**

* Jetzt wird kein HTML-Tag-Element mehr in einem veralteten Fragment hinzugefügt, wenn es gepatcht und der Inhalt dann gespeichert wird. (CAMP-40685)
* Bei Verwendung dynamischer Inhalte wird jetzt kein Leerzeichen mehr hinzugefügt. (CAMP-40605)
* Beim Konfigurieren einer Transaktions-E-Mail-Vorlage tritt jetzt kein Problem mehr auf. (CAMP-40604)

## Version 20.1 – Februar 2020 {#release-20-1---february-2020}

**Neue Funktionen**


<table> 
 <thead> 
  <tr> 
   <th> <strong>Adobe Experience Platform Data Connector (Betaversion)</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Adobe Experience Platform Data Connector ist jetzt in Adobe Campaign Standard integriert. Sie können Ihre Campaign-Daten in Adobe Experience Platform bereitstellen, indem Sie XTK-Daten (in Campaign aufgenommene Daten) auf das Adobe Experience Platform-Datenmodell (XDM) abbilden. </p>
    <p>Bitte beachten Sie, dass diese Funktion nur für Kundinnen und Kunden verfügbar ist, die auf Azure gehostet werden.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Audience Destinations (Betaversion) </strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Mit Audience Destinations können Sie Segmente von Adobe Experience Platform für Adobe Campaign freigeben.</p>
    <p>Bitte beachten Sie, dass diese Funktion nur für Kundinnen und Kunden verfügbar ist, die auf Azure gehostet werden.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

**Verbesserungen**

* Globale Verfügbarkeit des erweiterten MTA: Nachrichten (einschließlich Transaktionsnachrichten) werden jetzt vom erweiterten MTA von Adobe Campaign gesendet, der eine aktualisierte Versandinfrastruktur bereitstellt, die besseren Durchsatz sowie verbesserte Zustellbarkeit und Bounce-Handhabung ermöglicht – [mehr dazu](https://helpx.adobe.com/de/campaign/kb/campaign-enhanced-mta.html)

* Die Zeitzonenverwaltung wurde verbessert. Sie können jetzt eine [bestimmte Zeitzone](../../automating/using/building-a-workflow.md) für einen gesamten Workflow definieren. Die ausgewählte Zeitzone gilt für alle Aktivitäten des Workflows. Informationen zur Zeitzone, die für den Benutzer oder Server konfiguriert wurde, werden jetzt in der Benutzeroberfläche angezeigt (in Protokollen nach Auswahl einer Zeitzone). (CAMP-37672)

* Campaign Standard-APIs ermöglichen es Ihnen jetzt, bei Verwendung großer Tabellen eine Paginierung durchzuführen, indem Sie den Parameter `_forcePagination=true` zu Ihrer Aufruf-URL hinzufügen – [mehr dazu](../../api/using/pagination.md)

* Die Versandlog-ID (eine eindeutige ID für jedes Protokoll) ist jetzt in den Ressourcen Versandlogs und in den Trackinglogs für alle Zielgruppendimensionen verfügbar. Dadurch können beispielsweise beim Export Versand- oder Trackinglogs identifiziert werden – [mehr dazu](../../automating/using/exporting-logs.md)

**Verbesserungen bei Email Designer**

* Fehlende Textanweisungen beim Erstellen einer Audience wurden hinzugefügt.
* Beim Klicken auf die Schaltfläche **Inhalt ändern** im Assistenten des alten E-Mail-Editors tritt jetzt kein Problem mehr auf.
* Die Header können jetzt mit dem Inhalt des Dienstzusammenfassungsberichts abgeglichen werden. (CAMP-38103)
* Dynamische Inhaltsvarianten können jetzt gelöscht wurden, ohne dass die restliche Betreffzeile beeinträchtigt wird. (CAMP-40096)
* Bei Verwendung der B-Variante im Betreff tritt jetzt kein Fehler mehr beim A/B-Test auf. (CAMP-40327)
* Dateien können jetzt per Drag-and-Drop verschoben werden, wenn die Import-Funktion zum Hochladen von HTML verwendet wird. (CAMP-39326)
* Text kann jetzt aus einem Texteditor kopiert und eingefügt werden. (CAMP-39028)
* Wortvorschläge werden jetzt angezeigt. (CAMP-38970)
* Fragmente können jetzt durch Benutzer gespeichert werden. (ATU-2447)
* Die Duplizierung dynamischer Strukturen ist jetzt möglich. (CAMP-38367)
* Bedingungen für dynamische Inhalte werden jetzt bei der Duplizierung beibehalten. (CAMP-39051)

**Sonstige Änderungen**

* Der Filter „Sendungen mit fehlgeschlagener Vorbereitung“ berücksichtigt jetzt das Erstellungsdatum der Sendungen und nicht das letzte Änderungsdatum.
* Die organisatorische Einheit der Sicherheitsgruppe „Administratoren“ kann nicht mehr geändert werden.
* Beim Erstellen eines Profils muss jetzt das Feld für die Organisationseinheit ausgefüllt werden.
* Ein Experience Cloud Trigger kann jetzt nur gelöscht werden, wenn sowohl das Ereignis als auch die mit ihm verknüpfte Transaktionsvorlage gelöscht werden.
* [!DNL Adobe Creative SDK] wurde eingestellt. Es wird jetzt in Campaign Standard nicht mehr unterstützt. Näheres dazu finden Sie auf der Seite [Veraltete und bereits entfernte Funktionen](../../rn/using/deprecated-features.md).


**Korrekturen**

* Beim Durchführen einer Datenschutzanfrage zum Löschen von Benutzerdaten werden Benutzerdaten jetzt auch in Ausschlusslogs gelöscht. (CAMP-39003)
* Jetzt bestehen keine Zugriffsprobleme mehr, wenn die Textgröße in einem Container-Element geändert wird.
* Das Kalender-Popup, das beim Bewegen des Mauszeigers in Marketing-Aktivitäten angezeigt wird, kann jetzt geschlossen werden.
* In der Aktivität **[!UICONTROL Externe API]** tritt jetzt kein Problem mehr auf, bei dem die Schaltfläche **[!UICONTROL Bestätigen]** angezeigt wurde, selbst wenn keine Daten geändert wurden.
* Bei der Verwendung der Aktivität **[!UICONTROL Vereinigung]** tritt bei Abfragen mit unterschiedlichen Zieldimensionen kein Problem mehr auf. Die Transitionsdaten zeigten nur Datensätze aus der Zielgruppendimension des Hauptsatzes an. (CAMP-36831)
* Bei der Verwendung der Aktivität **[!UICONTROL Abstimmung]** tritt in bestimmten Kontexten kein Problem mehr auf, z. B. wenn eine von zwei eingehenden Aktivitäten eine Ausschlussaktivität ist. (CAMP-37490)
* Beim Auswählen und Aktualisieren von Testprofilen tritt kein Fehler mehr auf. (CAMP-37976)
* Beim Anmelden oder Abmelden über Landingpages werden keine Fehlerseiten mehr angezeigt. (CAMP-37771)
* Beim Hochladen von Inhalten im Zip-Format tritt jetzt kein Fehler mehr auf, bei dem PNG-Dateien im HTML-Code mit ihrer Erweiterung in Großbuchstaben referenziert wurden. (CAMP-37913)
* In-App-Nachrichten können jetzt gesendet werden, wenn dem Versand ein Testprofil hinzugefügt wird.
* Bei der Workflow-Aktivität „Externe API“ wurde ein Fehler behoben, durch den bei der Verknüpfung mit Anreicherungsaktivitäten die Aktivität fehlschlug.
* Der Status von SMS-Nachrichten wird jetzt korrekt angezeigt.
* Bei benutzerdefinierten Ressourcen tritt jetzt kein Fehler mehr auf, sodass unter unterschiedlichen API-Endpunkten keine doppelten Einträge mehr angezeigt werden.
* Landingpages sind jetzt nach dem Veröffentlichen verfügbar. (CAMP-38695)
* Beim Anzeigen von Daten aus einer Schnittmengentransition aus zwei verschiedenen Ressourcen tritt jetzt kein Fehler mehr auf. (CAMP-38974)
* Der Auflistungswert in einer Versandvorlage kann jetzt korrekt definiert werden. (CAMP-38388)
* Bei E-Mail-Massensendungen tritt jetzt kein Fehler mehr auf, bei dem der Versandstatus als „Ausstehend“ und der Gesendet-Status als „Fertig“ angezeigt wurde. (CAMP-35355)
* Die Absender-Domain wird in der dynamischen Berichterstellung jetzt korrekt angezeigt. (CAMP-33123)
* Bei den Abmeldezahlen in der dynamischen Berichterstellung treten jetzt keine Unstimmigkeiten mehr auf. (CAMP-39949)
* Beim Senden von In-App-Nachrichten können jetzt Adressen im Bildschirm „Versandlogs“ angezeigt wurden.
* SMS-Versandlogs werden jetzt mit der richtigen Anzahl von Bounces aktualisiert. (CAMP-38395)
* Die Push-Benachrichtigungstoken werden jetzt nicht mehr durch Post-Aufrufe von App-Abonnements aktualisiert. (CAMP-39273)

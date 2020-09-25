---
title: Neueste Version
description: Auf dieser Seite finden Sie Informationen zum Inhalt der aktuellen Version des Campaign Standards
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
source-git-commit: 8d55a92deeccabcb6970de6cce4b5e297bc431d8
workflow-type: tm+mt
source-wordcount: '2441'
ht-degree: 4%

---


# Neueste Version{#latest-release}

[Versionsplanung](../../rn/using/release-planning.md) | [Control Panel-Versionen](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html) | [Aktualisierungen der Dokumentation](../../rn/using/documentation-updates.md) | [Frühere Versionshinweise](../../rn/using/release-notes-2020.md) | [Eingestellte Funktionen](../../rn/using/deprecated-features.md)

## Version 20.4 - Oktober 2020            {#release-20-4---october-2020}

**Neue Funktionen**

<table> 
<thead> 
<tr> 
<th> <strong>Kontrollgruppen</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>Sie können jetzt <strong>Kontrollgruppen</strong> verwenden, um die Auswirkungen Ihrer Kampagnen zu messen, indem Sie einen Teil ihrer Audience ausschließen. Sie können dann das Verhalten der Zielgruppe, die die Nachricht erhalten hat, mit dem Verhalten der nicht zielgerichteten Kontakte vergleichen. Auf der Grundlage der gesendeten Protokolle können Sie auch eine Kontrollgruppe in zukünftigen Kampagnen Zielgruppe werden.
</p>
<p>For more information refer to the <a href="../../sending/using/control-group.md">detailed documentation</a> and <a href="https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/control-groups.html">how-to video</a>.
</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Externe API - OAuth-Unterstützung</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>Adobe Campaign unterstützt jetzt OAuth zur Authentifizierung in der Aktivität des <strong>externen API</strong> -Workflows. Diese neue Funktion ermöglicht es dieser Aktivität, mit Systemen zu kommunizieren, die OAuth unterstützen.
</p>
<p>For more information refer to the <a href="../../automating/using/external-api.md">detailed documentation</a>.
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
  <td> <p>Wir freuen uns, die Journey AI für alle Adobe Campaign Standard-Kunden bekannt geben zu können.</p>
  <p>Die Journey AI nutzt fortschrittliches maschinelles Lernen (ML), um Firmen in die Lage zu versetzen, die Gestaltung und den Versand von Kundenreisen zu optimieren, indem sie die Interaktionsvorlieben jedes Einzelnen vorhersagen.</p>
  <P>Die Journey-KI besteht aus zwei ML-Funktionen:</p>
<ul> 
     <li> <strong>Predictive Interaktionsbewertung</strong> - Intelligentes Identifizieren Sie die bevorzugte Interaktionsstufe der Kunden, um die Zielgruppe zu verbessern und Nachrichten zu personalisieren, um Konversionen und Bindung zu erhöhen. Sehen Sie sich das <a href="https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/journey-ai/predictive-engagement-scoring.html">Anleitungsvideo</a>an.</li> 
     <li> <strong>Predictive Send Time Optimization</strong> - Prognostiziert den bestmöglichen Zeitpunkt zum Senden von E-Mails an jede Einzelperson in einer Kampagne, um die Interaktionsraten zu maximieren und den ROI bei der E-Mail-Kampagne zu erhöhen. Sehen Sie sich das <a href="https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/journey-ai/predictive-send-time-optimization.html">Anleitungsvideo</a>an.</li>
    </ul>
  <p>Wenn Sie wissen möchten, wie Sie mit Journey AI beginnen können, lesen Sie bitte die <a href="../../sending/using/predictive.md">ausführliche Dokumentation</a> und wenden Sie sich an Ihren Kundenbetreuer. Beachten Sie, dass die Journey-KI zwar für Bestandskunden kostenlos erhältlich ist, die Implementierungskosten jedoch rund 50 Stunden betragen.</p>
    </td> 
</tr> 
</tbody> 
</table>

**Verbesserungen**

* **Datenschutzverwaltung**: Das **CCPA Opt-Out** -Feld, das über die Benutzeroberfläche und API zur Verfügung stand, wird jetzt auch über den Privacy Core Service unterstützt. In diesem Feld können Adobe Campaign-Nutzer nachverfolgen, ob ein Verbraucher sich für den Verkauf von persönlichen Informationen entschieden hat. [mehr dazu](https://helpx.adobe.com/content/help/de/campaign/kb/acs-privacy.html#ccpa)
* **Verbesserungen** der Workflow-Ausführung (Beta): Im Rahmen einer globalen Initiative um Workflows wurden einige wichtige Verbesserungen entwickelt, um das Speichermanagement zu stabilisieren, die Latenz zu reduzieren und den Speicher zu optimieren, der während der Ausführung von Workflows belegt wird. Diese Verbesserungen befinden sich derzeit in der Betaphase und stehen nur einer Reihe von Kunden zur Verfügung. Die allgemeine Verfügbarkeit ist für Anfang 2021 geplant.
* Zur Verbesserung der Sicherheit verwendet Kampagne jetzt einen **Signaturmechanismus** zur Verfolgung von Links in E-Mails.
* Die Konfiguration der mobilen App wurde durch **klarere Fehlermeldungen** beim Hochladen von iOS-Zertifikaten oder Android-Schlüsseln verbessert.
* Für transaktionale Push-Nachrichten-Targeting-Profil ist jetzt eine **neue Zuordnung** von Versänden verfügbar (mapRtEventAppSubRcp). Versand, Ausschluss und Trackinglogs für diese Versand stehen nun in den Tabellen &quot;wideLogAppSubRcp&quot;, &quot;excludeLogAppSubRcp&quot;und &quot;trackingLogAppSubRcp&quot;zur Verfügung. Dadurch wird ein Fehler behoben, der dazu führte, dass die Analyse des Versands beim Senden einer transaktionalen Push-Nachricht mit der Dimension &quot; **Profil** -Zielgruppe&quot;fehlschlug.
* **Das SMS-Fehlermanagement** wurde verbessert, um zu verhindern, dass zu viele Profil zur Quarantäne-Liste hinzugefügt werden. Standardmäßig werden SMS-Fehler jetzt als weiche Fehler und nicht als schwere Fehler konfiguriert. Refer to [this page](https://helpx.adobe.com/de/campaign/kb/sms-connector-protocol-and-settings.html).

**Verbesserungen bei Email Designer**

* Mit der **neuen dynamischen Kontexthilfe** , die die Benutzeroberfläche und Dokumentation vollständig miteinander verbindet, haben wir die Benutzerfreundlichkeit im E-Mail-Designer verbessert und einen einfachen Zugriff auf die neuesten Hilfeinhalte ermöglicht.
* Es wurde ein Problem behoben, durch das Zeilenumbrüche in einer Meldung beim Bearbeiten der Textversion entfernt wurden. (CAMP-44483)
* Es wurde ein Fehler behoben, der verhinderte, dass die Nur-Text-Version einer HTML-Vorlage automatisch generiert und synchronisiert wurde. (CAMP-44195)
* Es wurde ein Problem behoben, das beim Ändern der Bildgröße auftreten konnte. Nachdem die Nachrichten gesendet wurden, wurden die Bilder in Microsoft Outlook nicht korrekt angezeigt. (CAMP-44656)
* Es wurde ein Problem behoben, das beim Einfügen einer Schaltfläche und dem Festlegen ihrer Breite auf &quot;auto&quot;aufgetreten ist. Nach dem Senden der Nachricht wurde der Inhalt der Schaltfläche nicht vollständig angezeigt. (CAMP-44560)
* Es wurde ein Problem behoben, das beim Hochladen von Inhalten aus einer angehängten HTML-Datei aufgetreten ist. Nachdem die Nachricht an eine Gmail-Adresse gesendet wurde, wurde das CSS nicht angewendet, was zu einem Renderingproblem führte. (CAMP-44085)
* Es wurde ein Problem behoben, bei dem Inhaltsfragmente, die zuvor in einer Nachricht verwendet wurden, nicht aktualisiert wurden, wenn sie direkt in der Inhaltsvorlage geändert wurden. (CAMP-43973)
* Es wurde ein Problem mit der **Suchleiste &quot;Fragmente** &quot;behoben. Bei der Suche nach einem vorhandenen Fragment wurde in der Suchleiste kein Ergebnis angezeigt. (CAMP-44223)
* Es wurde ein Problem mit den Suchleisten **Inhaltsblöcke** und **Fragmente** behoben. Bei Verwendung einer der Suchleisten wurden die Ergebnisse nur angezeigt, wenn Sie auf Mehr Ergebnisse **anzeigen geklickt haben...**. (CAMP-44205)
* Es wurde ein Problem behoben, bei dem die Umrandung zwischen Text und Bildern in Microsoft Outlook nicht möglich war. (CAMP-45370)
* Es wurde ein Problem beim Duplizieren eines Fragments behoben. Nach dem Duplizieren des Fragments fehlten im ursprünglichen Fragment HTML-Zeilen. (CAMP-45207)
* Es wurde ein Fehler behoben, der zu Renderingproblemen in Microsoft Outlook führte. (CAMP-44749)
* Es wurde ein Fehler behoben, der beim Ändern der Auffüllung der **Strukturkomponente** in einer Versandvorlage auftrat. CSS-Tags haben keine an der Umrandung vorgenommenen Änderungen übernommen, was zu einem Renderingproblem geführt hat. (CAMP-45381)
* Es wurde ein Problem beim Hochladen eines Bildes behoben. Die Höhe des Bilds wurde automatisch auf 0 eingestellt, wodurch ein Renderingproblem aufgetreten ist. (CAMP-45366)

**Sonstige Änderungen**

* Wiederholungsmechanismen wurden hinzugefügt, wenn beim Versuch, eine Experience Platform-Audience mit einer **Read-Audience** -Aktivität zu importieren, ein Fehler auftritt. (CAMP-43947, CAMP-43366)
* Organisatorische Einheiten werden jetzt automatisch auf die Organisationseinheit des Benutzers eingestellt, der das Profil oder die Entität erstellt. Organisatorische Einheiten können nicht mehr entfernt und leer gelassen werden.
* Beim Veröffentlichen einer benutzerdefinierten Ressource wird jetzt nach der Vorbereitung ein Bestätigungs-Popup angezeigt.
* Die Popup-Meldung, die angezeigt wird, wenn eine benutzerdefinierte Ressource fehlschlägt, wurde aus Gründen der Übersichtlichkeit verbessert.
* Der Ausdruck-Editor in Workflows wurde verbessert, um Ausführungsfehler zu vermeiden. [Es stehen neue Funktionen](../../automating/using/customizing-workflow-external-parameters.md) zur Verfügung: Sie können in allen Aktivitäten verwendet werden, die die Verwendung von Ereignis-Variablen nach dem Aufruf eines Workflows mit externen Parametern ermöglichen. Darüber hinaus wird jetzt eine QuickInfo mit der Funktionsbeschreibung im Ausdruck-Editor angezeigt.
* [Neue Filter](../../administration/using/configuring-transactional-messaging.md#searching-transactional-events) wurden zur Liste der transaktionalen Ereignis hinzugefügt. Sie ermöglichen es Ihnen, die Ereignis-Konfigurationen nach ihrem Status sowie nach dem letzten Empfang eines Ereignisses zu filtern.
* Die Protokolle, die beim Exportieren von Paketen angezeigt werden, wurden spezieller und detaillierter zu den aufgetretenen Fehlern im Fehlerfall gemacht.
* Nach dem Senden einer Nachricht können Sie jetzt die Liste der [verfolgten URLs](../../sending/using/tracking-messages.md)suchen, filtern und exportieren.
* Die automatische [Synchronisierung zwischen Start und Kampagne](../../administration/using/configuring-a-mobile-application.md#aepsdk-workflow) ist jetzt GA und ist standardmäßig aktiviert.
* Transaktionsnachrichten können mit hoher Priorität gesendet werden, auch wenn der Versand erheblich belastet ist.
* Die Größe der Workflow-Exportpakete wurde optimiert, indem der sendende Testversand-Export entfernt wurde.
* Es wurde eine neue Meldung hinzugefügt, um die Größe der heruntergeladenen Datei in der Aktivität **Dateiübertragung** anzuzeigen.
* Fehlermeldungen für ungültige Sitzungstoken wurden verbessert.
* Ein neuer Mechanismus verhindert nun, dass Verfolgungsdaten von Stellvertretern zu Trackinglogs und Berichten hinzugefügt werden.
* Es wurde eine neue Warnmeldung hinzugefügt, die das Debugging von Data Management-Aktivitäten unterstützt, die mit einer Versand-Aktivität verbunden sind.
* Die Beschriftungen im Arbeitsbereich &quot;Berichte&quot;wurden verbessert.
* Ein neuer Validierungsschritt wurde hinzugefügt, um das Löschen von technischen Gegenständen in Transaktionsnachrichten zu verhindern.
* Auf der Registerkarte &quot; **Execution Liste** &quot;einer Transaktionsnachricht wurde ein neuer Filter zum Status des Versands hinzugefügt, um die Fehlerbehebung zu verbessern.
* Zur Leistungsverbesserung und zur Optimierung der Ausführungszeit wurden nicht verwendete Indizes entfernt, basierend auf den Nutzungsstatistiken von Tabellen, die in der vorläufigen Analyse für mehr als 350 Kunden ermittelt wurden. Die betroffenen Tabellen sind: nmsaddressStatus, nmscampaign, nmsdelivery, nmslandingpage, nmsprogram, nmsempfänger, nmsseedmember, nmsservice, nmssubhistorcp, nmsaudience, xtkworkflow

**Korrekturen**

* Es wurde ein Fehler behoben, der verhinderte, dass Sie einen Ziellink für Push-Benachrichtigungen oder In-App-Nachrichten verwenden konnten, wenn die Verfolgung aktiviert war.
* Es wurde ein Problem behoben, durch das verhindert werden konnte, dass Sie einer transaktionalen E-Mail Marken zuweisen. Während des Veröffentlichungsschritts können mehrere Fehlermeldungen angezeigt werden. (CAMP-44988)
* Es wurde ein Fehler in der Workflow-Benutzeroberfläche behoben, der verhinderte, dass Informationen in Feldern gespeichert wurden, die numerische Werte anfordern. (CAMP-44025)
* Es wurde ein Problem behoben, durch das eine Fehlermeldung angezeigt werden konnte, wenn eine **Test** -Aktivität in einem Arbeitsablauf für Importvorlagen verwendet wurde. (CAMP-42910)
* Es wurde ein Problem behoben, das bei der Verwendung einer **Read-Audience** -Aktivität mit einem Auflistung-Typ-Feld und einer Verbindung zu **Vereinigung** - oder **Anreicherung** -Aktivitäten auftrat. (CAMP-42795)
* Es wurde ein Problem in dynamischen Berichten behoben, das beim Einsatz der vordefinierten Segmente zum Filtern von Daten in Berichten auftrat. (CAMP-42627)
* Es wurde ein Problem behoben, durch das Sie keine Aktivität für die **Planung** auf 12 Uhr festlegen konnten. (CAMP-42674)
* Es wurde ein Problem behoben, das das Senden von SMS-Nachrichten unterbrechen konnte, wenn die SMPP-Verbindung instabil war. (CAMP-42789)
* Es wurde ein Fehler behoben, der verhinderte, dass die Schaltfläche zum **Anhalten der Vorbereitung** nach dem Aktualisieren der Seite angezeigt wurde. (CAMP-42721)
* Es wurde ein Fehler behoben, der verhinderte, dass Prozentwerte für Hotclick-Berichte angezeigt wurden, wenn Inhalte aus einer URL importiert wurden. (CAMP-44468)
* Es wurde ein Fehler behoben, der einen Timeout-Fehler anzeigen konnte, wenn ein Profil ausgewählt wurde, das im Kontext der Ersetzung des Profils verwendet werden sollte. (CAMP-44746)
* Es wurde ein Fehler behoben, der dazu führte, dass Instanzen nach der Bereitstellung von benutzerdefinierten Ressourcen, die falsche Linkdefinitionen enthielten, nicht funktionierten. (CAMP-44406)
* Es wurde ein Problem behoben, durch das leere verknüpfte Entitäten (Typologien, Marken usw.) erstellt wurden. nach dem Kopieren und Einfügen eines Versands in eine Kampagnenvorlage. (CAMP-44765)
* Es wurde ein Fehler behoben, der verhinderte, dass Testversand aufgrund einer fehlerhaften Handhabung von Versand-Vorbereitungstabellen bei einem Datenbankabsturz oder einem einfachen Datenbankneustart in Azurblaus gesendet wurden.
* Es wurde ein Problem behoben, das das Löschen von Links mit Experience Manager-Inhalten in einem Versand mit mehrsprachigen Inhalten verhinderte. (CAMP-44029)
* Es wurde ein Problem in dynamischen Berichten behoben, durch das beim Versuch, Dimensionen zu filtern, eine Fehlermeldung angezeigt werden konnte.  (CAMP-43097)
* Es wurde ein Problem behoben, durch das ein leerer Bildschirm angezeigt werden konnte, wenn versucht wurde, auf Profil in einer Instanz zuzugreifen, die mit benutzerdefinierten Ressourcen, die bestimmte Linkdefinitionen enthielten, konfiguriert wurde. (CAMP-41009)
* Es wurde ein Problem in Workflows behoben, das bei der Verwendung einer **Anreicherung** -Aktivität mit zwei Eingaberessourcen auftrat, die beide Zielgruppen miteinander verknüpft haben. (CAMP-42133)
* Es wurde ein Fehler behoben, der dazu führte, dass Workflows bei Verwendung einer Aktivität zur **Dateiübertragung** in eine Schleife umgewandelt wurden. (CAMP-43754)
* Es wurde ein Fehler behoben, der dazu führte, dass Duplikat beim Erstellen eines Profils mit exportierten Protokollen nicht berücksichtigt wurden. (CAMP-45031)
* Es wurde ein Fehler behoben, der zu Datendiskrepanzen zwischen Berichten in Adobe Campaign und in PDF-Dateien exportierten Berichten führte. (CAMP-43010)
* Es wurde ein Fehler behoben, der dazu führte, dass der Arbeitsablauf für Direct Mail-Versand fehlschlug, wenn bestehende Datenfelder in Funktionen verwendet wurden. (CAMP-42737)
* Es wurde ein Fehler behoben, der beim Importieren von Paketen mit transaktionalen Ereignissen und Meldungsvorlagen auftrat. Der Importvorgang wurde mit 5 % beendet. (CAMP-42544)
* Es wurde ein Fehler behoben, der nach dem Ändern der Aktivität für die **Anreicherung** und dem Hinzufügen zusätzlicher Daten in einem Workflow zu einem Fehler (Uncatch TypeError) führte. (CAMP-41877)
* Es wurde ein Fehler behoben, der das Löschen des Workflows verhinderte. Protokolle mussten bereinigt werden, um den Workflow zu löschen. (CAMP-44144)
* Es wurde ein Fehler beim Erstellen einer Landingpage mit HTML-Code behoben. Obligatorische Kontrollkästchen wurden in der Kampagne nicht erkannt und waren in der veröffentlichten Landingpage nicht verfügbar. (CAMP-44181)
* Es wurde ein Fehler behoben, der dazu führte, dass Workflows bei der Verwendung der Aktivität **Warten** wiederholt wurden. (CAMP-43981)
* Es wurde ein Problem beim Senden von Transaktionsnachrichten behoben, das dazu führte, dass mehrere E-Mail-Adressen in einem Versand mehrmals als Ziel ausgewählt wurden. (CAMP-44202)
* Es wurde ein Fehler behoben, der bei Verwendung der Ersetzung von Profilen durch die Personalisierung von targetData auftrat. (CAMP-44996)
* Es wurde ein Fehler behoben, der dazu führte, dass die Vorschau des Versands beim Exportieren einer Versandvorlage in einem Paket fehlschlug. (CAMP-44084)
* Es wurde ein Fehler behoben, der verhinderte, dass Testversand bei der Verwendung benutzerdefinierter Zielgruppen-Mapping an Profil gesendet wurden. (CAMP-43701)
* Es wurde ein Fehler behoben, der in Workflows auftrat, wenn die Aktivität **Audience** lesen verwendet und eine Audience mit einer anderen Zielgruppendimension als **Profil** als Ziel verwendet wurde.  (CAMP-41885)
* Es wurde ein Fehler behoben, der zu Fehlern führte, wenn der technische Arbeitsablauf **updateEventsStatus** zu lange dauerte, bis der Ereignis-Verlauf abgerufen wurde (wenn der Workflow beendet wurde). Das nicht verwendete Aggregat &quot;sumQueueTime&quot;wurde aus dem Workflow entfernt, um das Problem zu lösen. (CAMP-43920)
* Es wurde ein Speicherproblem bei der Bereitstellung benutzerdefinierter Ressourcen behoben. (CAMP-42909)
* Es wurde ein Fehler in der Transaktionsnachricht behoben, der auftrat, wenn Attribute in Sammlungen fehlten. Jetzt werden alle fehlenden Attribute mit einem Standardwert definiert und in die Nutzlast aufgenommen. (CAMP-42882)
* Es wurde ein Problem behoben, das die Leistung bei der Abfrage von Echtzeit-Ereignis-Versandlogs beeinträchtigen konnte. (CAMP-42759)
* Es wurde ein Fehler behoben, der bei der Verwendung von Dateierweiterungen in Großbuchstaben mit freigegebenen Assets auftrat. (CAMP-44159)
* Es wurde ein Fehler behoben, der beim Testen der Verbindung zu einem Externe Konto vor dessen Erstellung eine Fehlermeldung anzeigte. Die Schaltfläche **Verbindung** testen wird jetzt erst nach Erstellung des Externen Kontos angezeigt.
* Es wurde ein Fehler behoben, der dazu führte, dass Meldungen nach dem Neustart der erweiterten MTA bei mit der Freigabe konfigurierten Instanzen als ausstehend angezeigt wurden.
* Es wurde ein Fehler behoben, der dazu führte, dass die Anzahl der aktiven Profil nicht mit der tatsächlichen Anzahl der gesendeten Versand übereinstimmte.
* Es wurde ein Problem behoben, das zu Latenzzeiten führen konnte, wenn im Abfragen-Editor in einem Workflow nach Ressourcen gesucht wurde.
* Es wurde ein Fehler behoben, der bei der Auswahl der Option **Geben Sie die Felder an, die in der Textsuchoption** in einer benutzerdefinierten Ressource berücksichtigt werden sollen, auftrat. Wenn die Liste des Felds leer gelassen wurde, ist die Veröffentlichung der benutzerdefinierten Ressource fehlgeschlagen.
* Es wurde ein Leistungsproblem behoben, das beim Anzeigen der Übersicht über benutzerdefinierte Ressourcen mit einem großen Datenvolumen auftrat.
* Es wurde ein Fehler behoben, der verhinderte, dass Sie einen Versand mit Profil-Ersatzteilen importieren konnten.
* Es wurde ein Fehler behoben, der dazu führte, dass Testversand nicht sofort gesendet wurden, wenn der Versand geplant war, wenn Profil ersetzt wurde.
* Es wurde ein Problem behoben, das beim Hochladen eines Android-Schlüssels für eine Mobilanwendung aufgetreten ist. In der Meldung, die nach dem erfolgreichen Hochladen des Schlüssels angezeigt wurde, wurde der Wert des vorherigen Schlüssels angezeigt.
* Es wurde ein Fehler behoben, der verhinderte, dass Testelemente aus Transaktionsnachrichten erstellt werden konnten, nachdem eine Ereignis-Konfiguration mit einer Sammlung ohne Attribut erstellt wurde.
* Es wurde ein Fehler behoben, der dazu führte, dass benutzerdefinierte Ressourcen nach dem Erstellen eines neuen Filters mit einem Aggregat nicht veröffentlicht werden konnten.
* Es wurde ein Fehler behoben, der dazu führte, dass eine falsche Tracking-Offline-Rate für Gmail-Empfänger vom Gmail-Image-Proxy verursacht wurde.
* Es wurde ein Problem behoben, das beim Importieren eines Pakets Fehler wegen zu wenig Arbeitsspeicher verursachte.
* Es wurde ein Fehler behoben, der dazu führte, dass die Aktion zum Aufheben der Verknüpfung des Experience Managers fehlschlug, wenn der Inhalt des Experience Managers einen Pfad mit dem Zeichen &quot;%20&quot;enthielt.
* Es wurde ein Fehler bei Beschriftungen behoben, der beim Duplizieren von Workflow-Aktivitäten auftrat.
* Es wurde ein Problem mit der Transaktionsnachricht-Auswahl in einer Landingpage behoben, das auftrat, wenn die Option **Beginn zum Senden der Nachricht** ausgewählt wurde.
* Es wurde ein Problem mit Transaktionsnachrichten oder wiederkehrenden Versänden behoben, bei denen der Versand-Status nicht mit dem richtigen Standardwert initialisiert werden konnte. Die Fehlerprotokolle wurden ebenfalls verbessert.
* Es wurde ein Fehler behoben, der beim Erweitern des **Abonnements auf ein Anwendungsfeld** (appSubscriptionRcp) mit einem Profil-Link mithilfe eines benutzerdefinierten Felds auftrat. Der Index wurde nicht automatisch erstellt, was sich auf die Push-Sendezeit auswirken könnte. (CAMP-41120)


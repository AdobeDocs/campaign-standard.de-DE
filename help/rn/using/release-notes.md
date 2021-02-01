---
solution: Campaign Standard
product: campaign
title: Neueste Version
description: Auf dieser Seite finden Sie Informationen zum Inhalt der neuesten Version von Campaign Standard.
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
translation-type: tm+mt
source-git-commit: 41f2280c72a2f6bee3e4e972fab17a7ac94b966c
workflow-type: tm+mt
source-wordcount: '2610'
ht-degree: 73%

---


# Neueste Version{#latest-release}

[Versionsplanung](../../rn/using/release-planning.md) | [Control Panel-Versionen](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html) | [Aktualisierungen der Dokumentation](../../rn/using/documentation-updates.md) | [Frühere Versionshinweise](../../rn/using/release-notes-2020.md) | [Eingestellte Funktionen](../../rn/using/deprecated-features.md)

## Version 21.1 - Februar 2021                  {#release-21-1---february-2021}

**Neue Funktionen**

<table> 
<thead> 
<tr> 
<th> <strong>Email Feedback Service</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Email Feedback Service (EFS) ist ein skalierbarer Dienst, der das Feedback direkt vom erweiterten MTA erfasst und damit die Reporting-Genauigkeit verbessert. Diese Funktion wird als private Beta veröffentlicht und wird in zukünftigen Versionen nach und nach allen Kunden zur Verfügung stehen.</p>
<ul>
<li>Alle Kategorien von Feedback werden nun für einen vollständigen und präzisen Berichte erfasst.</li>
<li>Die Berechnung des Indikators <b>Ausgeliefert</b> basiert nun auf Echtzeitrückmeldungen der erweiterten MTA für eine verbesserte Genauigkeit und Reaktivität.</li>
<li>EFS löst das Problem der Verzögerungen mit synchronem Soft Bounces-Berichte.</li>
</ul>
<p>Weitere Informationen finden Sie im <a href="../../sending/using/confirming-the-send.md#email-feedback-service">entsprechenden Handbuch</a>.
</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Verbesserungen der Adobe Experience Manager-Integration</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Die Integration der Kampagne mit Adobe Experience Manager wurde verbessert: Sie können jetzt mehrsprachige Inhalte einfacher aus Adobe Experience Manager importieren. <p>
<p>Adobe Campaign Standard erkennt jetzt automatisch Sprachvarianten von Adobe Experience Manager-Inhalten und ermöglicht den Import und die Erstellung von Varianten in großer Zahl. Dadurch wird die Anzahl der Schritte, die ein Anwender ausführen muss, um eine mehrsprachige Kampagne auf der Grundlage von Adobe Experience Manager-Inhalten zu erstellen, erheblich verkürzt.</p>
<p>Weitere Informationen finden Sie im <a href="../../integrating/using/creating-multilingual-email-aem.md">entsprechenden Handbuch</a>.
</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Einheitliche Experience Cloud-Benutzeroberfläche</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Die Kopfzeile von Adobe Campaign wurde geändert, um das Erlebnis über alle Experience Cloud-Produkte und -Services hinweg zu vereinheitlichen und zu verbessern. Diese Änderungen sollen Ihnen die Nutzung erleichtern, unter anderem durch folgende Verbesserungen:</p>
<ul>
<li>Einfacherer Wechsel zwischen Ihren Organisationen oder zu einer anderen Anwendung.</li>
<li>Verbesserte Benutzerhilfe – Durch die Einbindung von Experience League in das Produkt liefert die Suche auch Ergebnisse aus Community-Foren und mehr Videoinhalte, sodass Sie einfacheren Zugriff auf zusätzliche Inhalte haben und die Anwendung optimal nutzen können. Wir haben auch einen Feedback-Mechanismus direkt im Hilfemenü hinzugefügt, der es einfacher macht, Probleme zu melden oder Ideen zu teilen.</li>
<li>Verbesserte Benachrichtigungen – Das Dropdown-Menü "Benachrichtigungen" enthält jetzt zwei Registerkarten: eine für Ihre eigenen Produktbenachrichtigungen und eine für mehr globale Produktankündigungen.</li>
</ul>
<p>Weitere Informationen finden Sie im <a href="../../start/using/interface-description.md#top-bar">entsprechenden Handbuch</a>.
</p>
</td> 
</tr> 
</tbody> 
</table>

**Verbesserungen**

* **Die Integration von Microsoft Dynamics 365 wurde durch ein spezielles Self-Service-Integrationsprogramm und einen verbesserten Implementierungsprozess verbessert.** [Mehr dazu](../../integrating/using/d365-acs-get-started.md)

* Es wurde eine Verbesserung vorgenommen, um die Fehlerbehebung bei Problemen mit dem Transaktionsnachrichtenprozess zu erleichtern. Technische Adobe-Administratoren können nun die Rückverfolgung für jeden Prozess verwenden, ohne ihn neu zu starten.

* Mit der Liste **Profil** können Sie jetzt nach Datensätzen suchen, die auf einem der folgenden Felder basieren: E-Mail-, Vor-, Nachname- oder benutzerdefinierte Felder, die beim Erweitern der Profil-Ressource in der erweiterten Filterung hinzugefügt wurden. Diese Funktion ist auch in Campaign Standard-APIs verfügbar, die den Parameter &quot;filterType&quot; verwenden. [Mehr dazu](../../audiences/using/integrated-customer-profile.md)

* Ein Parameter wurde an die Anzahl der Container angepasst, die den Datenbank-Pooling-Prozess für Transaktionsnachrichten ausführen. Dadurch kann die Last gleichmäßig auf alle verwendeten Container verteilt und eine optimale Leistung erzielt werden.

* Eine neue Funktion **GetOption** ist jetzt in Aktivitäten verfügbar, die Ereignis-Variablen verwenden, nachdem ein Workflow mit externen Parametern aufgerufen wurde. Damit können Sie den Wert einer angegebenen Funktion zurückgeben. [Mehr dazu](../../automating/using/customizing-workflow-external-parameters.md)

* Eine neue Option ermöglicht es dem Campaign Standard, die Verfügbarkeit des physischen Speichers **auf Ihrem System zu überprüfen, bevor ein Workflow gestartet wird.** Steht zu wenig Speicher zur Verfügung, wird die Ausführung des Workflows verzögert, bis der Systemspeicher diesen Schwellenwert erreicht. Dadurch wird eine weitere Leistungsminderung vermieden und das Risiko eines Ausfalls verringert. Der Arbeitsablauf wird automatisch fortgesetzt, sobald die Belastung des Servers nachlässt und der Arbeitsspeicher zunimmt. Beachten Sie, dass diese Option schreibgeschützt ist und nicht geändert werden kann. [Mehr dazu](../../automating/using/best-practices-workflows.md#execution)

* In Adobe Campaign Standard ist ein neuer Prozess verfügbar, mit dem Sie einfacher von der älteren SDK v4-Mobilanwendung zu **Adobe Experience Platform Mobile SDK** migrieren können. Mehr dazu erfahren Sie auf [dieser Seite](../../administration/using/sdkv4-migration.md).

**Sonstige Änderungen**

* Es wurde ein Fehler in eine Warnung bei der Nachrichtenvorbereitung geändert, wenn die Begrenzung von 100 Inhalts-Downloads pro rollierender Stunde erreicht wird. Beim Erreichen des Grenzwerts wird nun eine Warnung angezeigt, wodurch der weitere Versand ermöglicht wird.

* Beim Anreichern des Transaktionsnachrichteninhalts werden die Links beim Abrufen von Daten aus der Profiltabelle nicht mehr abgefragt. Dies reduziert die Latenz bei der Nachrichtenvorbereitung und vermeidet leere Profildaten aufgrund einer fehlerhaften Relation, die für die Profiltabelle definiert ist.

* Die technische Konfiguration der Instanz wurde zur Gewährleistung von Stabilität optimiert. (CAMP-45681)

* Die Sitzungsverwaltung wurde verbessert, um den Speicher zu optimieren. (CAMP-45901, CAMP-46767)

* Die Aktivität **Dateiübertragung** generiert jetzt eine zusätzliche Variable (filesCount), die die Anzahl der hochgeladenen oder heruntergeladenen Dateien enthält. (CAMP-45842) [Mehr dazu](../../automating/using/transfer-file.md#output-variables)

* Der SMS-Connector kann jetzt mit jeder Nachricht mehrere optionale Parameter senden. [Mehr dazu](../../administration/using/sms-protocol.md)

* Benutzer mit der Rolle &quot;DATAMODEL&quot;können jetzt Versand-Protokollerweiterungen veröffentlichen. (CAMP-46604)

* Die Fehlermeldung, die beim Versuch angezeigt wurde, eine Ressource zu veröffentlichen, die auf eine nicht mehr vorhandene benutzerdefinierte Ressource ausgerichtet ist, wurde klarer formuliert. (CAMP-46893)

* Die folgenden Sprachen wurden der Liste **Bevorzugte Sprache** hinzugefügt: Indonesisch - Indonesien (in-id), Englisch - Schweden (en-se), Englisch - Asiatisch-Pazifischer Raum (en-ap), Englisch - Japan (en-jp), Spanisch - Lateinamerika (es-la). (CAMP-46351)

* Die Profilauswahl beim Testen einer Landingpage verwendet nun die Ressource &quot;profilBase&quot; anstelle von &quot;profile&quot;, um Zeitüberschreitungen zu vermeiden.

* Das SMPP-Protokollformat wurde verbessert.

* Den JS-Funktionen &quot;cryptString&quot; und &quot;decryptString&quot; wurden optionale Parameter zur Angleichung an die Adobe Campaign Classic-API hinzugefügt.

* Verbesserte Warn- und Fehlermeldungen in den Versandvorbereitungslogs.

* Verbesserte Fehlerprotokolle beim Versuch, eine Verbindung mit Adobe Identity Management Service (IMS) herzustellen.

* Sie können jetzt die Dimensionen **Versand** und **Kampagne** mithilfe der Suchleiste im dynamischen Berichte weiter filtern.

* Das Gültigkeitsdatum der SMS-Transaktionsnachricht kann jetzt durch den für den Ablaufparameter in der Transaktionsnachrichten-API festgelegten Wert definiert werden. (CAMP-36600)

* Beim dynamischen Reporting zeigte der integrierte Bericht **Versandzusammenfassung** falsche Daten für die Metrik der Abmelderate an. Eine neue Metrik mit dem Namen **Eindeutige Abmeldung** wurde hinzugefügt, um dies zu beheben. (CAMP-46445)

**Korrekturen**

* Es wurde ein Problem behoben, das dazu führte, dass der Versand aufgrund bestimmter Prozesse sehr langsam ausgeführt wurde. Dies lag daran, dass für mehrere Parameter falsche Einheiten definiert waren (z. B. Millisekunden statt Sekunden).

* Es wurde ein Problem behoben, bei dem das Mobile SDK eine offene Tracking-Anfrage basierend auf der Bedingung sendete, dass deliveryId/MessageID nicht null ist. Dies führte bei Sendungen mit deaktiviertem Tracking zu 404-Fehlern. Eine zusätzliche Variable (acsDeliveryTracking) mit Informationen zum Tracking-Status des Versands wird jetzt in der Payload gesendet. Diese Variable kann je nach eingestelltem Tracking-Status zwei Werte haben: ein oder aus. [Mehr dazu](../../administration/using/push-tracking.md).

* Es wurde ein Problem in Workflows behoben, das beim Kopieren und Einfügen einer **Deduplizierungs**-Aktivität auftrat, die einmal ausgeführt worden war und eine temporäre Ressource nutzte. Nach der Duplizierung wurde die Ressource der Aktivität automatisch auf &quot;Leer&quot; eingestellt, was zu Problemen bei anderen Aktivitäten des Workflows führte. Nach dem Einfügen bleibt die Ressource der Aktivität die gleiche, damit der Fehler so schnell wie möglich und nicht später im Workflow ausgelöst wird. (CAMP-46903)

* Es wurde ein Fehler behoben, der dazu führte, dass die Analyse des Versands beim Senden eines transaktionalen Push-Nachrichten-Targeting-Profils fehlschlug, indem ein neues [Zielgruppen-Mapping](../../administration/using/target-mappings-in-campaign.md) eingeführt wurde: **Profil - Echtzeit-Ereignis für Push** (*mapRtEventAppSubRcp*). Versand, Ausschluss und Trackinglogs für [transaktionale Push-Benachrichtigungen, die auf ein Profil](../../channels/using/transactional-push-notifications.md#transactional-push-notifications-targeting-a-profile) abzielen, werden jetzt in *wideLogAppSubRcp*, *excludeLogAppSubRcp* und *trackingLogAppSubRcp* gespeichert. Tabellen.
* Fehlerkorrektur – Versandberichte werden jetzt ausgeführt, wenn 5.000 Zeilen angezeigt werden.
* Fehlerkorrektur – A/B-Tests funktionieren jetzt einwandfrei. Der Inhalt von Variante B kann jetzt aktualisiert werden, nachdem die Versandvorlage geändert wurde. (CAMP-45235)
* Fehlerkorrektur – Der Transaktionsnachrichtenprozess wird jetzt nicht mehr blockiert, sodass Nachrichten problemlos gesendet werden können.
* Fehlerkorrektur – Das Anklicken eines internen Links führt jetzt nicht mehr zu Navigationsproblemen (z. B. beim Zugriff auf den übergeordneten Versand über einen Bildschirm mit einer Testversand-Zusammenfassung).
* Fehlerkorrektur – Beim Erstellen eines Versands werden jetzt alle verfügbaren Experience Manager-Inhaltsvorlagen angezeigt. (CAMP-45990)
* Fehlerkorrektur – In Workflows werden jetzt Fehlermeldungen angezeigt, nachdem die Spalte **Grund** zur Registerkarte &quot;Zusatzdaten&quot; in den Versandlogs hinzugefügt wurde. (CAMP-45139)
* Fehlerkorrektur – Jetzt tritt kein Problem mehr auf, wenn zwei Anwendungsabonnement-Aufrufe dieselbe Marketing Cloud-ID haben (Fehler &quot;Duplizierte Schlüsselwerte verletzen die Eindeutigkeitsbeschränkung&quot;).
* Fehlerkorrektur – Es tritt kein Problem mehr mit verlangsamter Geschwindigkeit auf, wenn Aktivitäten per Drag-and-drop in einen Workflow gezogen wurden, der eine große Anzahl von **Abfrage**- und **Audience lesen**-Aktivitäten enthält. (CAMP-44511)
* Fehlerkorrektur – Jetzt tritt am Ende der Vorbereitung der Transaktionsnachricht kein Fehler mehr auf, sodass Weiterleitungsinformationen auf die Tracking-Server geladen werden können.
* Fehlerkorrektur – Beim Versuch, Importvorlagen oder frühere Importvorgänge nach dem Anpassen der Workflow-Ressource zu öffnen, werden keine Fehlermeldungen mehr angezeigt. (CAMP-46183)
* Fehlerkorrektur – Die Ausführung der Aktivität **Audience lesen** wird jetzt nicht mehr verhindert, wenn diese mit einem dynamischen Audience-Namen konfiguriert wurde. (CAMP-46047)
* Fehlerkorrektur – Die Schaltfläche **Liste exportieren** wird jetzt angezeigt.
* Fehlerkorrektur – Der Workflow **Bericht-Aggregate** schlägt jetzt nicht mehr fehl. (CAMP-45979)
* Fehlerkorrektur – Beim Erstellen einer benutzerdefinierten Ressource mit einem benutzerdefinierten zusammengesetzten Schlüssel (dynamischer Text-/Datumsinhalt) tritt jetzt kein Problem mehr auf.
* Fehlerkorrektur – Die Anzeige von Abfragetransitionsdaten wird jetzt nicht mehr verhindert. (CAMP-45669)
* Fehlerkorrektur – Bei der Veröffentlichung benutzerdefinierter Ressourcen tritt jetzt kein Problem mehr mit dem Speicherverbrauch auf.
* Fehlerkorrektur – Beim Konfigurieren eines Versands für die Durchführung an einem bestimmten Datum tritt jetzt kein Problem mehr auf. Wurde der Versand so eingestellt, dass er nach der Bestätigung sofort ausgeführt wird, schlug die Versandvorbereitung fehl und das ursprünglich angegebene Datum wurde weiterhin verwendet. (CAMP-44107)
* Fehlerkorrektur – Transaktionsvorlagen können jetzt problemlos geöffnet werden. (CAMP-47181)
* Fehlerkorrektur – Im Veröffentlichungsprozess von Transaktionsnachrichten tritt jetzt kein Problem mehr auf, das zu duplizierten Typologien und Typologieregeln mit Namen führen kann, die die zulässige Zeichenfolgenlänge überschreiten. (CAMP-47104)
* Fehlerkorrektur – In der Aktivität **Externe API** tritt jetzt kein Problem mehr auf, wenn ein Eingabeparameter einen nicht vorhandenen Datensatz zurückgibt. (CAMP-47023)
* Fehlerkorrektur – Das erneute Verbinden des SMPP-Connectors wird jetzt nicht mehr verhindert.
* Fehlerkorrektur – Jetzt tritt kein Problem mehr bei der Aktivität **Dateiübertragung** auf, wenn eine Datei mit einem Punkt im Namen heruntergeladen wird. Zuvor wurden die Zeichen nach dem Punkt als Dateierweiterung betrachtet. (CAMP-46624)
* Fehlerkorrektur – Das Datenbank-Pooling wird jetzt nicht mehr verhindert, sodass keine Transaktionsnachrichten mehr in der Router-Warteschlange hängen bleiben.
* Fehlerkorrektur – Abgebrochene Versandlogs werden jetzt nicht mehr gesendet.
* Fehlerkorrektur – Workflows schlagen bei Verwendung der Aktivität **Und-Verknüpfung** nicht mehr fehl. Die Aktivität änderte die Hauptmenge automatisch auf die letzte Transition, die mit ihr verbunden war, selbst wenn in ihr die erste verbundene Transition angezeigt wurde. (CAMP-46900)
* Fehlerkorrektur – Bei Adressen, die erfolgreich unter Quarantäne gestellt wurden, wird der Status nicht mehr fälschlicherweise auf &quot;Gültig&quot; gesetzt. Zuvor wurden solche Adressen wieder aus der Quarantäne entfernt.
* Fehlerkorrektur – Personalisierte Felder können jetzt angezeigt werden, wenn sie Sonderzeichen enthalten. (CAMP-46805)
* Fehlerkorrektur – Eine spezifische detaillierte Ansicht eines Profils kann jetzt angezeigt werden. Hierbei trat ein Problem auf, wenn die Profilressource mit benutzerdefinierten Feldern erweitert worden war und die Option **Abschnitt mit Personalisierungsfeldern hinzufügen** aktiviert war.
* Fehlerkorrektur – Beim Senden von Transaktionsereignissen wird nicht mehr der Fehlercode 500 zurückgegeben. (CAMP-46811)
* Fehlerkorrektur – Jetzt werden geplante E-Mail-Berichte zugestellt. (CAMP-46891)
* Fehlerkorrektur – Jetzt kann eine benutzerdefinierte Ressource mit der Profilressource mit einer einfachen Relation mit Kardinalität 1 problemlos verknüpft werden. Beim Zugriff auf ein Profil mit einem leeren Feld für die benutzerdefinierte Ressource wird jetzt eine Fehlermeldung anstelle einer leeren Liste angezeigt.
* Fehlerkorrektur – Wenn in einem Workflow die Profilersetzung verwendet wird, kann die Seite jetzt die Versandprofile laden, wenn das zu ersetzende Profil ausgewählt wird. (CAMP-46522)
* Fehlerkorrektur – Es wurde eine Regression behoben, bei der der technische Workflow **Datenbankbereinigung** versucht hat, abgelaufene Versandarbeitstabellen abzulegen, was zu folgenden Fehlern führte: (CAMP-46536).

```
   PGS-220000 PostgreSQL error: ERROR: table ""wkdlv_24439460_data"" does not exist and WDB-200001 SQL statement 'DROP TABLE wkdlv_24448131_data' could not be executed.
```

* Fehlerkorrektur – In einigen Fällen trat bei der Verwendung des benutzerdefinierten Filters für benutzerdefinierte Ressourcen der folgende Fehler auf: (CAMP-46509).

```
   The 'profile/xxxx' field used in the filter 'xxxxx' does not exist in custom resource 'xxx'
```

* Es wurde ein Problem behoben, bei dem die Vorbereitung der Push-Benachrichtigung **zu lange dauerte, bis sie abgeschlossen war.** Dies wurde durch einen fehlenden Index in den transienten Arbeitstabellen verursacht.
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr auf, wenn die Option **Dimension zur Abstimmung** in einer **Abstimmungs**-Aktivität in einem Workflow verwendet wird und bereits eine Relation zwischen einer benutzerdefinierten Ressource und einer Profilressource definiert ist.
* Fehlerkorrektur – Beim Hinzufügen von Links über die Aktivität **Abstimmung** oder **Anreicherung** tritt kein Fehler mehr auf. Zuvor wurden ausgewählte Links nicht in der Ausgabetransition angezeigt.
* Fehlerkorrektur – Beim Verwenden der Aktivität **Segmentierung** bei wiederkehrenden Sendungen in einem Workflow werden die Nachrichten nicht mehr an die falsche Audience gesendet. (CAMP-46275, CAMP-46470)
* Fehlerkorrektur – Die Veröffentlichung von benutzerdefinierten Ressourcen schlägt jetzt nicht mehr fehl, wenn man die Profilressource zu erweitern versucht, um benutzerdefinierte Profildimensionen für das dynamische Reporting zu erstellen. (CAMP-46266)
* Fehlerkorrektur – Beim Hinzufügen eines Links zu einer Dateiimporttabelle tritt jetzt kein Fehler mehr auf. Nach dem Hinzufügen einer **Anreicherungs**-Aktivität zur **Dateiimport**-Aktivität verschwand der zuvor konfigurierte Link. (CAMP-46557)
* Es wurde ein Fehler behoben, der bei der Verwendung benutzerdefinierter Ressourcen, die mit Profil-Daten verknüpft sind, dazu führte, dass die Anzeigereihenfolge im Konfigurationsbildschirm **Details** beim Speichern geändert wurde. (CAMP-46312)
* Es wurde ein Problem behoben, das die Anzeige von Daten im dynamischen Berichte aufgrund von Versänden, die auf einer benutzerdefinierten Versand-Zuordnung basieren, verhindern konnte.
* Es wurde ein Fehler behoben, der dazu führte, dass Sie eine Sammlung mit einer falschen Ressourcendatei in einer Aktivität **Abfrage** nicht auswählen konnten.
* Fehlerkorrektur – Der InMail-Prozess validiert die Hardbounces jetzt richtig.
* Fehlerkorrektur – Jetzt tritt beim Öffnen eines Profilbildschirms aufgrund eines Link-Fehlers kein Problem mehr auf.
* Fehlerkorrektur – Das Löschen von DSGVO-Daten aus dem Bereinigungs-Workflow wird jetzt nicht mehr verhindert.
* Es wurde ein Fehler behoben, der auftrat, wenn die Planungskonfiguration manuell mit der Tastatur in den E-Mail-Versand-Planparametern aktualisiert wurde.
* Fehlerkorrektur – Profile können jetzt bearbeitet werden, wenn die Parameter in der Organisationseinheit falsch sind.
* Es wurde ein Fehler behoben, der dazu führte, dass das Erweiterungsfeld **Dienst** leer war und in den **E-Mail-Eigenschaften** nicht eingestellt werden konnte, selbst wenn es in der Versandvorlage festgelegt wurde.
* Fehlerkorrektur – Jetzt dauert die Verarbeitung von Testsendungen nicht mehr längere Zeit. (CAMP-45048)
* Fehlerkorrektur – Das Sortieren von Spalten in einem Profilübersichtsbildschirm funktioniert jetzt fehlerfrei.
* Fehlerkorrektur – Die Erstellung der Miniaturansicht auf Azure funktioniert jetzt bei E-Mail-Varianten, die chinesische Zeichen enthalten, einwandfrei. (CAMP-47152)
* Es wurde ein Regressionsfehler behoben, der in Kampagne 20.4 eingeführt wurde und aufgrund der Filterung von Ereignissen, die von Gmail-Konten empfangen wurden, zu fehlerhaften Open Rate für Gmail führen konnte. (CAMP-46504)
* Fehlerkorrektur – HTML-Inhalt kann jetzt in eine Transaktionsnachrichtenvorlage importiert werden. (CAMP-47318)
* Es wurde ein Problem behoben, durch das die Anzeige der Renderings im **Bericht zum E-Mail-Rendering** verlangsamt werden konnte. (CAMP-46226)
* Fehlerkorrektur – Benutzerdefinierte Ressourcen, die mit einem Element vom Typ &quot;Liste&quot; konfiguriert werden, können jetzt in der Bildschirmdefinition veröffentlicht werden. (CAMP-47217)
* Es wurde ein Fehler im E-Mail-Designer behoben, der verhinderte, dass Zeilenunterteilungen in **Microsoft Outlook** korrekt dargestellt wurden, wenn sie oben im E-Mail-Inhalt platziert wurden. (CAMP-46294)
* Es wurde ein Fehler behoben, der dazu führte, dass die KPIs-Abstimmung mit dem technischen Arbeitsablauf **Adobe Analytics** blockiert wurde. (CAMP-46576)
* Es wurde ein Problem im **E-Mail-Designer** behoben, das verhindert hat, dass Fragmente automatisch in Suchfeldern angezeigt wurden, wenn Inhaltsblöcke eingefügt wurden. (CAMP-44205)
* Es wurde ein Problem im **E-Mail-Designer** behoben, bei dem unerwünschte Zeichen in gesendeten E-Mails angezeigt wurden, wenn Emojis in Fragmenten verwendet wurde. (CAMP-46621)
* Korrektur der Regression, die in 20.4 im **E-Mail-Designer** eingeführt wurde und die Trennzeichenkomponente beeinträchtigte, was zu zusätzlichen Zeilenhöhen und Bildverzerrungen im Inhalt führte. (CAMP-46663)
* Es wurde ein Fehler behoben, der dazu führte, dass die vordefinierten Schaltflächen beim Senden der Nachricht an ein Outlook-Postfach zentriert blieben, obwohl diese Schaltflächen in **E-Mail-Designer** rechts oder links ausgerichtet waren. (CAMP-46466)
* Es wurde ein Fehler behoben, der verhinderte, dass die Liste der Testelemente aktualisiert wurde, wenn Profil in der Vorschau **E-Mail-Designer** gesucht wurden. (CAMP-45265)
* Es wurde ein Fehler behoben, der verhinderte, dass benutzerspezifische Profil bei der Suche nach Profilen in der Vorschau **E-Mail-Designer** in der Liste angezeigt wurden. (CAMP-45589)
* Es wurde ein Fehler behoben, der dazu führte, dass beim Generieren von Trendgrafiken aus dem **Zusammenfassungsbericht für Versand** falsche Datumsangaben angezeigt wurden. (CAMP-45521)

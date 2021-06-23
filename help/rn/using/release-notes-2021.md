---
solution: Campaign Standard
product: campaign
title: Versionshinweise 2021
description: Auf dieser Seite werden alle Versionen von Adobe Campaign Standard von 2021 aufgelistet.
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
feature: Übersicht
role: Business Practitioner
level: Beginner
exl-id: b6cf7152-2200-43d7-8d0a-d65752bb2c9b
source-git-commit: 4a8dfc0b8f321447e0ebc23a9f5bbef337454d9f
workflow-type: ht
source-wordcount: '2535'
ht-degree: 100%

---

# Versionshinweise 2021{#release-notes-2021}

[Versionsplanung](../../rn/using/release-planning.md) | [Control Panel-Versionen](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html?lang=de) | [Aktualisierungen der Dokumentation](../../rn/using/documentation-updates.md) | [Frühere Versionshinweise](../../rn/using/release-notes-2020.md) | [Eingestellte Funktionen](../../rn/using/deprecated-features.md)

## Version 21.1 – Februar 2021 {#release-21-1---february-2021}

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
<p>Email Feedback Service (EFS) ist ein skalierbarer Dienst, der das Feedback direkt vom erweiterten MTA erfasst und damit die Reporting-Genauigkeit verbessert. Diese Funktion wird als private Betaversion veröffentlicht und wird in zukünftigen Versionen nach und nach allen Kunden zur Verfügung stehen.</p>
<ul>
<li>Alle Kategorien von Feedback werden jetzt für vollständiges und genaues Reporting erfasst.</li>
<li>Die Berechnung des <b>Zugestellt</b>-Indikators basiert nun auf Echtzeit-Feedback des erweiterten MTA, um Genauigkeit und Reaktivität zu verbessern.</li>
<li>EFS löst das Problem der Verzögerungen beim Reporting zu synchronen Bounces.</li>
</ul>
<p>Weitere Informationen finden Sie im <a href="../../sending/using/confirming-the-send.md">entsprechenden Handbuch</a>.
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
<p>Die Campaign-Integration mit Adobe Experience Manager wurde verbessert: Sie können jetzt mehrsprachige Inhalte einfacher aus Adobe Experience Manager importieren. <p>
<p>Adobe Campaign Standard erkennt jetzt automatisch Sprachvarianten von Adobe Experience Manager-Inhalten und ermöglicht den Import und die Erstellung von Varianten in großer Zahl. Dadurch wird die Anzahl der Schritte, die ein Anwender ausführen muss, um eine mehrsprachige Kampagne auf der Grundlage von Adobe Experience Manager-Inhalten zu erstellen, erheblich verkürzt.</p>
<p>Weitere Informationen finden Sie im <a href="../../integrating/using/creating-multilingual-email-aem.md">entsprechenden Handbuch</a>.
</p>
</td> 
</tr> 
</tbody> 
</table>

<!--
<table> 
<thead> 
<tr> 
<th> <strong>Unified Experience Cloud interface</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Adobe Campaign header bar has been changed to unify and improve your experience across all Experience Cloud products and services. These changes are designed to make your life easier, including:</p>
<ul>
<li>Easier switching between your organizations or to a different application.</li>
<li>Improved User Help – Bringing the Experience League into the product, search results also include results from community forums and more video content, giving you easier access to more content to help get the most out of the application. We've also added a feedback mechanism right in the Help menu, making it easier to report issues or share your ideas.</li>
<li>Improved Notifications – Notifications drop-down now has two tabs: one for your own product notifications, and one for more global product announcements.</li>
</ul>
<p>For more information refer to the <a href="../../start/using/interface-description.md#top-bar">detailed documentation</a>.
</p>
<p>NOTE: This change will be progressively rolled out to all customer environments between Feb 10 and March 1st.
</p>
</td> 
</tr> 
</tbody> 
</table>
-->

**Verbesserungen**

* **Die Integration von Microsoft Dynamics 365 wurde durch ein spezielles Self-Service-Integrationsprogramm und einen verbesserten Implementierungsprozess verbessert.** [Mehr dazu](../../integrating/using/d365-acs-get-started.md)

* Es wurde eine Verbesserung vorgenommen, um die Fehlerbehebung bei Problemen mit dem Transaktionsnachrichtenprozess zu erleichtern. Technische Adobe-Administratoren können nun die Rückverfolgung für jeden Prozess verwenden, ohne ihn neu zu starten.

* In der Liste **Profile** können Sie jetzt nach Datensätzen suchen, die auf einem dieser Felder basieren: E-Mail, Vorname, Nachname oder benutzerdefinierte Felder, die den erweiterten Filtern beim Erweitern der Profilressource hinzugefügt wurden. Diese Funktion ist auch in Campaign Standard-APIs verfügbar, die den Parameter &quot;filterType&quot; verwenden. [Mehr dazu](../../audiences/using/integrated-customer-profile.md)

* Ein Parameter wurde an die Anzahl der Container angepasst, die den Datenbank-Pooling-Prozess für Transaktionsnachrichten ausführen. Dadurch kann die Last gleichmäßig auf alle verwendeten Container verteilt und eine optimale Leistung erzielt werden.

* Eine neue **GetOption**-Funktion ist jetzt in Aktivitäten verfügbar, für die nach dem Aufruf eines Workflows mit externen Parametern Ereignisvariablen verwendet werden. Damit können Sie den Wert einer angegebenen Funktion zurückgeben. [Mehr dazu](../../automating/using/customizing-workflow-external-parameters.md)

* Eine neue Option ermöglicht es Campaign Standard, die Verfügbarkeit von **physischem Speicher** auf Ihrem System zu überprüfen, bevor ein Workflow gestartet wird. Steht zu wenig Speicher zur Verfügung, wird die Ausführung des Workflows verzögert, bis der Systemspeicher diesen Schwellenwert erreicht. Dadurch wird eine weitere Leistungsverschlechterung vermieden und das Risiko eines Ausfalls verringert. Der Workflow wird automatisch fortgesetzt, sobald die Auslastung des Servers abnimmt und der Speicher zunimmt. Beachten Sie, dass diese Option schreibgeschützt ist und nicht geändert werden kann. [Mehr dazu](../../automating/using/best-practices-workflows.md#execution)

* In Adobe Campaign Standard ist ein neuer Prozess verfügbar, der eine einfachere Migration von der älteren SDK v4-Mobile App auf das **Adobe Experience Platform Mobile SDK** ermöglicht. Mehr dazu erfahren Sie auf [dieser Seite](../../administration/using/sdkv4-migration.md).

**Sonstige Änderungen**

* Es wurde ein Fehler in eine Warnung bei der Nachrichtenvorbereitung geändert, wenn die Begrenzung von 100 Inhalts-Downloads pro rollierender Stunde erreicht wird. Beim Erreichen des Grenzwerts wird nun eine Warnung angezeigt, wodurch der weitere Versand ermöglicht wird.

* Beim Anreichern des Transaktionsnachrichteninhalts werden die Links beim Abrufen von Daten aus der Profiltabelle nicht mehr abgefragt. Dies reduziert die Latenz bei der Nachrichtenvorbereitung und vermeidet leere Profildaten aufgrund einer fehlerhaften Relation, die für die Profiltabelle definiert ist.

* Die technische Konfiguration der Instanz wurde zur Gewährleistung von Stabilität optimiert. (CAMP-45681)

* Die Sitzungsverwaltung wurde verbessert, um den Speicher zu optimieren. (CAMP-45901, CAMP-46767)

* Die Aktivität **Dateiübertragung** generiert jetzt eine zusätzliche Variable (filesCount), die die Anzahl der hochgeladenen oder heruntergeladenen Dateien enthält. (CAMP-45842) [Mehr dazu](../../automating/using/transfer-file.md#output-variables)

* Der SMS-Connector kann jetzt mit jeder Nachricht mehrere optionale Parameter senden. [Mehr dazu](../../administration/using/sms-protocol.md)

* Benutzer mit der Rolle &quot;DATAMODEL&quot; können jetzt Erweiterungen für Versandlogs veröffentlichen. (CAMP-46604)

* Die Fehlermeldung, die beim Veröffentlichen einer Ressource angezeigt wurde, für die eine nicht mehr vorhandene benutzerdefinierte Ressource als Zielgruppe festgelegt war, wurde klarer formuliert. (CAMP-46893)

* Die folgenden Sprachen wurden zur Liste der **bevorzugten Sprachen** hinzugefügt: Indonesisch – Indonesien (in-id), Englisch – Schweden (en-se), Englisch – Asien-Pazifik (en-ap), Englisch – Japan (en-jp), Spanisch – Lateinamerika (es-la). (CAMP-46351)

* Die Profilauswahl beim Testen einer Landingpage verwendet nun die Ressource &quot;profilBase&quot; anstelle von &quot;profile&quot;, um Zeitüberschreitungen zu vermeiden.

* Das SMPP-Protokollformat wurde verbessert.

* Den JS-Funktionen &quot;cryptString&quot; und &quot;decryptString&quot; wurden optionale Parameter zur Angleichung an die Adobe Campaign Classic-API hinzugefügt.

* Verbesserte Warn- und Fehlermeldungen in den Versandvorbereitungslogs.

* Verbesserte Fehlerprotokolle beim Versuch, eine Verbindung zum Adobe Identity Management Service (IMS) herzustellen.

* Sie können jetzt die Dimensionen für **Versand** und **Kampagne** weiter filtern, indem Sie die Suchleiste im dynamischen Reporting verwenden.

* Das Gültigkeitsdatum der SMS-Transaktionsnachricht kann jetzt durch den für den Ablaufparameter in der Transaktionsnachrichten-API festgelegten Wert definiert werden. (CAMP-36600)

* Beim dynamischen Reporting zeigte der integrierte Bericht **Versandzusammenfassung** falsche Daten für die Metrik der Abmelderate an. Eine neue Metrik mit dem Namen **Eindeutige Abmeldung** wurde hinzugefügt, um dies zu beheben. (CAMP-46445)

**Korrekturen**

* Es wurde ein Problem behoben, das dazu führte, dass Sendungen aufgrund bestimmter Prozesse sehr langsam ausgeführt wurden. Dies lag daran, dass für mehrere Parameter falsche Einheiten definiert waren (z. B. Millisekunden statt Sekunden).

* Es wurde ein Problem behoben, bei dem das Mobile SDK eine offene Tracking-Anfrage basierend auf der Bedingung sendete, dass deliveryId/MessageID nicht null ist. Dies führte bei Sendungen mit deaktiviertem Tracking zu 404-Fehlern. Eine zusätzliche Variable (acsDeliveryTracking) mit Informationen zum Tracking-Status des Versands wird jetzt in der Payload gesendet. Diese Variable kann je nach eingestelltem Tracking-Status zwei Werte haben: ein oder aus. [Mehr dazu](../../administration/using/push-tracking.md).

* Es wurde ein Problem in Workflows behoben, das beim Kopieren und Einfügen einer **Deduplizierungs**-Aktivität auftrat, die einmal ausgeführt worden war und eine temporäre Ressource nutzte. Nach der Duplizierung wurde die Ressource der Aktivität automatisch auf &quot;Leer&quot; eingestellt, was zu Problemen bei anderen Aktivitäten des Workflows führte. Nach dem Einfügen bleibt die Ressource der Aktivität die gleiche, damit der Fehler so schnell wie möglich und nicht später im Workflow ausgelöst wird. (CAMP-46903)

* Es wurden Probleme behoben, die dazu führten, dass die Versandanalyse beim Senden einer Transaktions-Push-Benachrichtigung an Profile fehlschlug, indem ein neues [Zielgruppen-Mapping](../../administration/using/target-mappings-in-campaign.md) eingeführt wurde: **Profil – Echtzeitereignis für Push** (*mapRtEventAppSubRcp*). Die Versand-, Ausschluss- und Trackinglogs für [profilbasierte Transaktions-Push-Benachrichtigungen](../../channels/using/transactional-push-notifications.md#transactional-push-notifications-targeting-a-profile) werden jetzt in den Tabellen *broadLogAppSubRcp*, *excludeLogAppSubRcp* und *trackingLogAppSubRcp* gespeichert.

   >[!IMPORTANT]
   >
   >Aufgrund dieser Änderung wird empfohlen, das Zielgruppen-Mapping zu aktualisieren und die Nachricht erneut zu veröffentlichen, wenn Sie eine vorhandene profilbasierte Transaktions-Push-Benachrichtigung verwenden (die vor dem Upgrade auf Adobe Campaign 21.1 erstellt wurde). Eine detaillierte Anleitung dazu finden Sie [hier](../../channels/using/transactional-push-notifications.md#change-target-mapping). Die Verwendung des früheren Zielgruppen-Mappings **Profil – Echtzeitereignis** (*mapRtEventRcp*) kann zu längeren Versandvorbereitungszeiten und Leistungseinbußen führen.

* Fehlerkorrektur – Versandberichte werden jetzt ausgeführt, wenn 5.000 Zeilen angezeigt werden.
* Fehlerkorrektur – A/B-Tests funktionieren jetzt einwandfrei. Der Inhalt von Variante B kann jetzt aktualisiert werden, nachdem die Versandvorlage geändert wurde. (CAMP-45235)
* Fehlerkorrektur – Der Transaktionsnachrichtenprozess wird jetzt nicht mehr blockiert, sodass Nachrichten problemlos gesendet werden können.
* Fehlerkorrektur – Das Anklicken eines internen Links führt jetzt nicht mehr zu Navigationsproblemen (z. B. beim Zugriff auf den übergeordneten Versand über einen Bildschirm mit einer Testversand-Zusammenfassung).
* Fehlerkorrektur – Beim Erstellen eines Versands werden jetzt alle verfügbaren Experience Manager-Inhaltsvorlagen angezeigt. (CAMP-45990)
* Fehlerkorrektur – In Workflows werden jetzt Fehlermeldungen angezeigt, nachdem die Spalte **Grund** zur Registerkarte &quot;Zusatzdaten&quot; in den Versandlogs hinzugefügt wurde. (CAMP-45139)
* Fehlerkorrektur – Jetzt tritt kein Problem mehr auf, wenn zwei Anwendungsabonnement-Aufrufe dieselbe Marketing Cloud-ID haben (Fehler &quot;Duplizierte Schlüsselwerte verletzen die Eindeutigkeitsbeschränkung&quot;).
* Fehlerkorrektur – Es tritt kein Problem mehr mit verlangsamter Geschwindigkeit auf, wenn Aktivitäten per Drag-and-Drop in einen Workflow gezogen wurden, der eine große Anzahl von **Abfrage**- und **Audience lesen**-Aktivitäten enthält. (CAMP-44511)
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

* Fehlerkorrektur – Der Abschluss der **Vorbereitung von Push-Benachrichtigungen** nimmt jetzt nicht mehr zu viel Zeit in Anspruch. Dies wurde durch einen fehlenden Index in den transienten Arbeitstabellen verursacht.
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr auf, wenn die Option **Dimension zur Abstimmung** in einer **Abstimmungs**-Aktivität in einem Workflow verwendet wird und bereits eine Relation zwischen einer benutzerdefinierten Ressource und einer Profilressource definiert ist.
* Fehlerkorrektur – Beim Hinzufügen von Links über die Aktivität **Abstimmung** oder **Anreicherung** tritt kein Fehler mehr auf. Zuvor wurden ausgewählte Links nicht in der Ausgabetransition angezeigt.
* Fehlerkorrektur – Beim Verwenden der Aktivität **Segmentierung** bei wiederkehrenden Sendungen in einem Workflow werden die Nachrichten nicht mehr an die falsche Audience gesendet. (CAMP-46275, CAMP-46470)
* Fehlerkorrektur – Die Veröffentlichung von benutzerdefinierten Ressourcen schlägt jetzt nicht mehr fehl, wenn man die Profilressource zu erweitern versucht, um benutzerdefinierte Profildimensionen für das dynamische Reporting zu erstellen. (CAMP-46266)
* Fehlerkorrektur – Beim Hinzufügen eines Links zu einer Dateiimporttabelle tritt jetzt kein Fehler mehr auf. Nach dem Hinzufügen einer **Anreicherungs**-Aktivität zur **Dateiimport**-Aktivität verschwand der zuvor konfigurierte Link. (CAMP-46557)
* Fehlerkorrektur – Die Verwendung benutzerdefinierter Ressourcen, die mit Profildaten verknüpft sind, führt jetzt nicht mehr dazu, dass die Anzeigereihenfolge auf dem **Detailkonfigurationsbildschirm** beim Speichern geändert wird. (CAMP-46312)
* Fehlerkorrektur – Im dynamischen Reporting werden jetzt auch dann Daten angezeigt, wenn Sendungen vorhanden sind, die auf einem benutzerdefinierten Versand-Mapping basieren.
* Fehlerkorrektur – Jetzt ist es möglich, eine Sammlung mit einem falschen Ressourcenziel in einer Workflow-**Abfrageaktivität** auszuwählen.
* Fehlerkorrektur – Der InMail-Prozess validiert die Hardbounces jetzt richtig.
* Fehlerkorrektur – Jetzt tritt beim Öffnen eines Profilbildschirms aufgrund eines Link-Fehlers kein Problem mehr auf.
* Fehlerkorrektur – Das Löschen von DSGVO-Daten aus dem Bereinigungs-Workflow wird jetzt nicht mehr verhindert.
* Fehlerkorrektur – Jetzt kann die Planungskonfiguration in den E-Mail-Versandzeitplan-Parametern manuell mit der Tastatur aktualisiert werden.
* Fehlerkorrektur – Profile können jetzt bearbeitet werden, wenn die Parameter in der Organisationseinheit falsch sind.
* Fehlerkorrektur – Jetzt bleibt das **Diensterweiterungsfeld** nicht mehr leer und kann in den **E-Mail-Eigenschaften** angepasst werden. Zuvor war dies nicht möglich, selbst wenn es in der Versandvorlage angepasst wurde.
* Fehlerkorrektur – Jetzt dauert die Verarbeitung von Testsendungen nicht mehr längere Zeit. (CAMP-45048)
* Fehlerkorrektur – Das Sortieren von Spalten in einem Profilübersichtsbildschirm funktioniert jetzt fehlerfrei.
* Fehlerkorrektur – Die Erstellung der Miniaturansicht auf Azure funktioniert jetzt bei E-Mail-Varianten, die chinesische Zeichen enthalten, einwandfrei. (CAMP-47152)
* Fehlerkorrektur – Es wurde eine in Campaign-Version 20.4 eingeführte Regression behoben, die aufgrund des Filterns von Tracking-Ereignissen, die von Gmail-Konten empfangen wurden, zu falschen Öffnungsraten für Gmail führen konnte. (CAMP-46504)
* Fehlerkorrektur – HTML-Inhalt kann jetzt in eine Transaktionsnachrichtenvorlage importiert werden. (CAMP-47318)
* Fehlerkorrektur – Die Anzeige der Renderings im **E-Mail-Rendering-Bericht** ist nicht mehr verlangsamt. (CAMP-46226)
* Fehlerkorrektur – Benutzerdefinierte Ressourcen, die mit einem Element vom Typ &quot;Liste&quot; konfiguriert werden, können jetzt in der Bildschirmdefinition veröffentlicht werden. (CAMP-47217)
* Fehlerkorrektur – In Email Designer werden jetzt Zeilentrennlinien in **Microsoft Outlook** korrekt dargestellt, wenn sie am oberen Rand des E-Mail-Inhalts platziert werden. (CAMP-46294)
* Fehlerkorrektur – Der technische Workflow der KPI-Abstimmung mit **Adobe Analytics** wird jetzt nicht mehr blockiert. (CAMP-46576)
* Fehlerkorrektur – In **Email Designer** werden jetzt Fragmente beim Einfügen von Inhaltsbausteinen automatisch in Suchfeldern angezeigt. (CAMP-44205)
* Fehlerkorrektur – In **Email Designer** werden jetzt bei der Verwendung von Emojis in Fragmenten keine unerwünschten Zeichen mehr in gesendeten E-Mails angezeigt. (CAMP-46621)
* Fehlerkorrektur – Eine in Version 20.4 eingeführte Regression in **Email Designer** wurde behoben, die sich auf die Trennlinienkomponente auswirkte und zu zusätzlichen Zeilenhöhen und Bildverzerrungen im Inhalt führte. (CAMP-46663)
* Fehlerkorrektur – Die vordefinierten Schaltflächen beim Senden einer Nachricht an ein Outlook-Postfach bleiben jetzt nicht mehr zentriert, obwohl diese Schaltflächen in **Email Designer** rechts oder links ausgerichtet werden. (CAMP-46466)
* Fehlerkorrektur – Die Liste der Testprofile wird jetzt beim Suchen nach Profilen in der **Email Designer**-Vorschau aktualisiert. (CAMP-45265)
* Fehlerkorrektur – Beim Suchen nach Profilen in der **Email Designer**-Vorschau werden jetzt benutzerdefinierte Testprofile in der Liste angezeigt. (CAMP-45589)
* Fehlerkorrektur – Beim Erstellen von Trendgrafiken aus dem **Versandzusammenfassungsbericht** werden jetzt übereinstimmende Datumsangaben angezeigt. (CAMP-45521)

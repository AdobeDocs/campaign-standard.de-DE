---
solution: Campaign Standard
product: campaign
title: Frühere Versionshinweise
description: Frühere Versionshinweise
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
hide: true
hidefromtoc: true
translation-type: tm+mt
source-git-commit: 1bf35c654b9c526330a70f7647ec7d9fd87e2335
workflow-type: tm+mt
source-wordcount: '2586'
ht-degree: 4%

---


# Neue Version {#new-release}

[Versionsplanung](../../rn/using/release-planning.md) | [Control Panel-Versionen](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html) | [Aktualisierungen der Dokumentation](../../rn/using/documentation-updates.md) | [Neueste Versionshinweise](../../rn/using/release-notes.md) | [Eingestellte Funktionen](../../rn/using/deprecated-features.md)

Diese Seite beschreibt neue Funktionen, Verbesserungen und Fehlerbehebungen, die in der nächsten Campaign Standard-Version enthalten sind.

>[!CAUTION]
>
> Dieser Inhalt kann ohne vorherige Ankündigung geändert werden, bis das Upgrade-Datum für die Stage-Umgebung abgeschlossen ist. Weitere Informationen finden Sie auf der Seite [Versionsplanung](../../rn/using/release-planning.md).


## Version 21.1 - Februar 2021 {#release-21-1---febuary-2021}

**Neue Funktionen**

<table> 
<thead> 
<tr> 
<th> <strong>E-Mail-Feedback-Dienst</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Email Feedback Service (EFS) ist ein skalierbarer Dienst, der die Genauigkeit der Berichte verbessert, indem E-Mail-Feedback direkt aus der erweiterten MTA erfasst werden.</p>
<ul>
<li>Alle Kategorien von Ereignissen werden erfasst: Verzögerungen, Auslieferung, Senden, Abbestellen (Link, Liste), Feedback (Spam-Beschwerden, asynchrone Ereignis).</li>
<li>Die Berechnung von Sent/Delivered-Indikatoren basiert nun auf Echtzeitrückmeldungen der erweiterten MTA, um Genauigkeit und Reaktivität zu verbessern.</li>
<li>EFS löst das Problem der zeitgleichen Absprünge des Berichte und nimmt 80% des Ladevorgangs vom InMail-Prozess ab.</li>
</ul>
<p>Diese Funktion wird als <strong>private Beta</strong> veröffentlicht und steht allen Kunden in zukünftigen Versionen schrittweise zur Verfügung.</p>
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
<p>Adobe Campaign Standard erkennt jetzt automatisch Sprachvarianten von Adobe Experience Manager-Inhalten und ermöglicht den Import und die Erstellung von Massenvarianten. Dadurch wird die Anzahl der Schritte, die ein Anwender ausführen muss, um eine mehrsprachige Kampagne auf der Grundlage von Adobe Experience Manager-Inhalten zu erstellen, erheblich vereinfacht.</p>
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
<p>Die Kopfzeilenleiste des Adobe Campaigns wurde geändert, um Ihr Erlebnis für alle Experience Cloud-Produkte und -Dienste zu vereinheitlichen und zu verbessern. Diese Änderungen sollen Ihnen das Leben erleichtern, unter anderem:</p>
<ul>
<li>Einfacherer Wechsel zwischen Ihren Organisationen oder zu einer anderen Anwendung.</li>
<li>Verbesserte Benutzerhilfe - Die Suchergebnisse beinhalten auch Ergebnisse aus Community-Foren und weitere Videoinhalte, sodass Sie leichter auf weitere Inhalte zugreifen können, um die Anwendung optimal nutzen zu können. Wir haben auch einen Feedback-Mechanismus direkt im Menü Hilfe hinzugefügt, der es einfacher macht, Probleme zu melden oder Ideen auszutauschen.</li>
<li>Verbesserte Benachrichtigungen - Die Dropdownliste Benachrichtigungen enthält jetzt zwei Registerkarten: eine für Ihre eigenen Produktbenachrichtigungen und eine für weitere globale Produktankündigungen.</li>
</ul>
</td> 
</tr> 
</tbody> 
</table>

**Verbesserungen**

* **Die Microsoft Dynamics 365** -Integration wurde durch eine eigens entwickelte Self-Service-Integrations-App und einen verbesserten Implementierungsprozess verbessert. [Mehr dazu](../../integrating/using/d365-acs-get-started.md)

* Es wurde eine Verbesserung vorgenommen, um die Fehlerbehebung zu erleichtern, wenn Probleme mit dem **Transactional Messaging-Prozess** auftreten. Technische Administratoren der Adobe können nun die Ablaufverfolgung für jeden Prozess verwenden, ohne ihn neu zu starten.

* Mit der Liste **Profil** können Sie jetzt nach Datensätzen suchen, die auf einem der folgenden Felder basieren: E-Mail-, Vor-, Nachname- oder benutzerdefinierte Felder, die beim Erweitern der Profil-Ressource in der erweiterten Filterung hinzugefügt wurden. Diese Funktion ist auch in Campaign Standard-APIs verfügbar, die den Parameter filterType verwenden.

* Ein Parameter wurde an die Anzahl der Container angepasst, die den Datenbankpooling-Prozess **Transaktionsnachrichten** ausführen. Dadurch kann die Last gleichmäßig auf alle verwendeten Container verteilt werden und eine optimale Leistung erzielen.

* Eine neue Funktion **GetOption** ist jetzt in Aktivitäten verfügbar, die Ereignis-Variablen verwenden, nachdem ein Workflow mit externen Parametern aufgerufen wurde. Damit können Sie den Wert einer bestimmten Funktion zurückgeben.

* Eine neue Option ermöglicht es dem Campaign Standard, die Verfügbarkeit von **physischem Speicher** auf Ihrem System zu überprüfen, bevor ein Workflow gestartet wird. Ist der Arbeitsspeicher zu niedrig, wird die Ausführung des Arbeitsablaufs verzögert, bis der Systemspeicher diesen Schwellenwert erreicht. Dadurch wird eine weitere Leistungsminderung vermieden und das Risiko eines Ausfalls verringert. Der Arbeitsablauf wird automatisch fortgesetzt, sobald die Belastung des Servers nachlässt und der Arbeitsspeicher zunimmt. Beachten Sie, dass diese Option schreibgeschützt ist und nicht geändert werden kann.


**Sonstige Änderungen**

* Es wurde ein Fehler in eine Warnung bei der Nachrichtenvorbereitung geändert, wenn die Beschränkung von 100 Inhaltsdownloads pro rollierender Stunde erreicht wurde. Beim Erreichen des Grenzwerts wird nun eine Warnung angezeigt, die den weiteren Versand ermöglicht.

* Beim Anreichern von Transaktionsnachrichten-Inhalten werden die Links beim Abrufen von Daten aus der Profil-Tabelle nicht mehr abgerufen. Dadurch wird die Latenz bei der Nachrichtenvorbereitung verringert und aufgrund einer fehlerhaften Beziehung, die mit der Profil-Tabelle definiert wurde, werden leere Profil-Daten vermieden.

* Die technische Konfiguration der Instanz wurde zur Gewährleistung der Stabilität optimiert. (CAMP-45681)

* Die Sitzungsverwaltung wurde verbessert, um den Arbeitsspeicher zu optimieren. (CAMP-45901, CAMP-46767)

* Die Aktivität **Übertragungsdatei** generiert jetzt eine zusätzliche Variable (filesCount), die die Anzahl der hochgeladenen oder heruntergeladenen Dateien enthält. (CAMP-45842)

* Der **SMS-Connector** kann jetzt mit jeder Nachricht mehrere optionale Parameter senden.

* Benutzer mit der Rolle &quot;DATAMODEL&quot;können jetzt Versand-Protokollerweiterungen veröffentlichen. (CAMP-46604)

* Die Fehlermeldung, die beim Versuch angezeigt wird, eine Ressource zu veröffentlichen, die auf eine benutzerdefinierte Ressource ausgerichtet ist, die nicht mehr vorhanden ist, wurde klarer formuliert. (CAMP-46893)

* Die folgenden Sprachen wurden der Liste **Bevorzugte Sprache** hinzugefügt: Indonesisch - Indonesien (in-id), Englisch - Schweden (en-se), Englisch - Asiatisch-Pazifischer Raum (en-ap), Englisch - Japan (en-jp), Spanisch - Lateinamerika (es-la). (CAMP-46351)

* Die Auswahl für Profil beim Testen einer Landingpage verwendet jetzt die profileBase-Ressource anstelle von Profil, um Zeitüberschreitungen zu verhindern.

* Das SMPP-Protokollformat wurde verbessert.

* Optionale Parameter für die Funktionen cryptString und decryptString JS wurden hinzugefügt, um sie mit den Adobe Campaign Classic APIs abzugleichen.

* Verbesserte Warn- und Fehlermeldungen in den Versand-Vorbereitungsprotokollen.

* Verbesserte Fehlerprotokolle beim Versuch, eine Verbindung mit Adobe Identity Management Service (IMS) herzustellen.

* Sie können jetzt die Dimensionen für Versand und Kampagne weiter filtern, indem Sie die Suchleiste in **Dynamischer Berichte** verwenden.

* Das Gültigkeitsdatum der transaktionalen SMS-Nachricht kann nun durch den für den Ablaufparameter in der **Transaktionsnachrichten-API** festgelegten Wert definiert werden. (CAMP-36600)

* Im dynamischen Berichte zeigte der integrierte Bericht **Versand-Zusammenfassung** falsche Daten für die Metrik für die Abmeldung an. Eine neue Metrik mit dem Namen **Eindeutige Abmeldung** wurde hinzugefügt, um dies zu beheben. (CAMP-46445)

**Korrekturen**

* Es wurde ein Fehler behoben, der dazu führte, dass Versand aufgrund bestimmter Prozesse sehr langsam ausgeführt wurden. Dies war auf fehlerhafte Einheiten zurückzuführen, die für mehrere Parameter definiert wurden (z. B. Millisekunden anstelle von Sekunden).
* Es wurde ein Problem in Workflows behoben, das beim Kopieren und Einfügen einer **Deduplizierung-Duplikate**-Aktivität auftrat, die einmal ausgeführt wurde und eine temporäre Ressource nutzte. Nach der Duplizierung wurde die Ressource der Aktivität automatisch auf &quot;Leer&quot;eingestellt, was zu Problemen in anderen Aktivitäten des Workflows führte. Nach dem Einfügen bleibt die Ressource der Aktivität gleich, damit der Fehler so schnell wie möglich und nicht später im Workflow ausgelöst wird. (CAMP-46903)
* Es wurde ein Fehler behoben, der auftrat, wenn das Mobile SDK eine offene Verfolgungsanfrage basierend auf der Bedingung gesendet hat, dass deliveryID/MessageID nicht null ist. Dies führt bei Versänden mit deaktivierter Verfolgung zu 404 Fehlern. Eine zusätzliche Variable (acsDeliveryTracking) mit Informationen zum Verfolgungsstatus des Versands wird jetzt in der Nutzlast gesendet. Diese Variable kann je nach dem festgelegten Verfolgungsstatus zwei Werte ein- oder ausblenden.
* Es wurde ein Fehler behoben, der verhinderte, dass Versandberichte ausgeführt wurden, wenn 5000 Zeilen angezeigt wurden.
* Es wurde ein Problem mit A/B-Tests behoben, durch das verhindert wurde, dass der Inhalt der Variante B aktualisiert wurde, nachdem die Versandvorlage geändert wurde. (CAMP-45235)
* Es wurde ein Fehler behoben, der dazu führte, dass der Transaktionsnachrichtenprozess blockiert wurde und das Senden von Nachrichten verhindert wurde.
* Es wurde ein Fehler behoben, der dazu führte, dass die Analyse des Versands fehlschlug, wenn eine transaktionale Push-Nachricht mit der Dimension &quot;Profil-Zielgruppe&quot;gesendet wurde. Für Push-Transaktionsnachrichten, die auf Profile abzielen, ist jetzt ein neues Versand-Mapping (mapRtEventAppSubRcp) verfügbar. Die Versand-, Ausschluss- und Trackinglogs für diese Sendungen stehen nun in den Tabellen &quot;broadLogAppSubRcp&quot;, &quot;excludeLogAppSubRcp&quot; und &quot;trackingLogAppSubRcp&quot; zur Verfügung.
* Es wurde ein Problem behoben, das zu Navigationsproblemen führen konnte, wenn auf einen internen Link geklickt wurde (z. B. beim Zugriff auf den übergeordneten Versand über einen Testversand-Zusammenfassungsbildschirm).
* Es wurde ein Fehler behoben, der verhinderte, dass beim Erstellen eines Versands alle verfügbaren Inhaltsvorlagen für Experience Manager angezeigt wurden. (CAMP-45990)
* Es wurde ein Fehler in Workflows behoben, der dazu führte, dass Fehlermeldungen nach dem Hinzufügen der Spalte **Grund** zur zusätzlichen Registerkarte &quot;Daten&quot;nicht in den Versandlogs angezeigt wurden. (CAMP-45139)
* Es wurde ein Problem behoben, das auftrat, wenn zwei App-Abonnement-Aufrufe dieselbe Marketing Cloud-ID hatten (&quot;Duplikat-Schlüsselwert verletzt den Fehler &quot;eindeutige Einschränkung&quot;).
* Es wurde ein Problem behoben, das zu Langsamkeit-Problemen führen konnte, wenn Aktivitäten per Drag &amp; Drop in einen Workflow mit einer großen Anzahl von Aktivitäten **Abfrage** und **Read-Audience** gezogen wurden. (CAMP-44511)
* Es wurde ein Fehler behoben, der am Ende der Vorbereitung der Transaktionsnachricht auftrat und das Hochladen von Weiterleitungsinformationen auf die Tracking-Server verhinderte.
* Es wurde ein Problem behoben, durch das Fehlermeldungen angezeigt werden konnten, wenn versucht wurde, Importvorlagen zu öffnen oder Importaufträge zu vergehen, nachdem die Workflow-Ressource angepasst wurde. (CAMP-46183)
* Es wurde ein Fehler behoben, der die Ausführung einer Aktivität **Lesen** verhinderte, wenn diese mit einem dynamischen Audiencen-Namen konfiguriert wurde. (CAMP-46047)
* Es wurde ein Problem behoben, bei dem die Schaltfläche **Liste exportieren** nicht angezeigt wurde.
* Es wurde ein Problem behoben, das zum Fehlschlagen des **Berichte-Aggregats**-Workflows führen konnte. (CAMP-45979)
* Es wurde ein Problem behoben, das beim Erstellen einer benutzerdefinierten Ressource mit einem benutzerdefinierten zusammengesetzten Schlüssel (dynamischer Text/Datum) auftrat.
* Es wurde ein Problem behoben, das die Anzeige von Daten zur Transition der Abfrage verhindern konnte. (CAMP-45669)
* Korrektur von Problemen beim Speicherverbrauch im Zusammenhang mit der benutzerdefinierten Ressourcenveröffentlichung.
* Es wurde ein Problem behoben, das beim Konfigurieren eines Versands für das Senden an ein bestimmtes Datum aufgetreten ist. Wurde der Versand dann so eingestellt, dass er sofort nach der Bestätigung versandt wird, ist die Vorbereitung des Versands fehlgeschlagen und das ursprünglich angegebene Datum wurde weiterhin berücksichtigt. (CAMP-44107)
* Es wurde ein Problem behoben, das das Öffnen von Transaktionsvorlagen verhinderte. (CAMP-47181)
* Es wurde ein Fehler im Veröffentlichungsprozess der Transaktionsnachricht behoben, der dazu führte, dass Duplikat-Typologien und Typologieregeln mit Namen, die die zulässige Zeichenfolgengröße überschreiten, angezeigt wurden. (CAMP-47104)
* Es wurde ein Fehler in der Aktivität **Externe API** behoben, der auftrat, wenn ein Eingabeparameter einen nicht vorhandenen Datensatz zurückgab. (CAMP-47023)
* Es wurde ein Problem behoben, das die erneute Verbindung des SMPP-Connectors verhindern konnte.
* Es wurde ein Problem behoben, das in der Aktivität **Dateiübertragung** beim Herunterladen einer Datei mit einem Punkt in ihrem Namen auftrat. Die Zeichen nach dem Punkt wurden als Dateierweiterung betrachtet. (CAMP-46624)
* Es wurde ein Fehler behoben, der dazu führte, dass Datenbankpooling nicht durchgeführt werden konnten, wodurch Transaktionsnachrichten in der Router-Warteschlange hängen blieben.
* Es wurde ein Fehler behoben, der nicht verhinderte, dass die abgebrochenen Versandlogs gesendet wurden.
* Es wurde ein Fehler behoben, der dazu führte, dass ein Workflow bei Verwendung einer **AND-join**-Aktivität fehlschlug. Die Aktivität änderte den Primär-Satz automatisch auf die letzte Transition, die mit ihr verbunden war, selbst wenn sie die erste verkabelte Transition anzeigte. (CAMP-46900)
* Es wurde ein Fehler behoben, der dazu führte, dass Adressen, die erfolgreich unter Quarantäne gestellt wurden, ihren Status nicht korrekt auf &quot;Gültig&quot;festgelegt hatten, wodurch sie aus der Quarantäne entfernt wurden.
* Es wurde ein Problem behoben, das die Anzeige personalisierter Felder verhinderte, wenn diese Sonderzeichen enthielten. (CAMP-46805)
* Es wurde ein Problem behoben, das die Anzeige einer bestimmten detaillierten Ansicht für ein Profil verhinderte. Dies trat auf, wenn die Profil-Ressource mit benutzerdefinierten Feldern erweitert wurde und die Option **Hinzufügen einen personalisierten Feldabschnitt** aktiviert war.
* Es wurde ein Fehler behoben, der beim Senden von transaktionalen Ereignissen den Fehlercode 500 zurückgeben konnte. (CAMP-46811)
* Es wurde ein Problem behoben, durch das verhindert werden konnte, dass geplante E-Mail-Berichte empfangen werden. (CAMP-46891)
* Es wurde ein Problem behoben, das beim Verknüpfen einer benutzerspezifischen Ressource mit der Profil-Ressource mit einem einfachen Link zur 1-Kardinalität auftrat. Beim Zugriff auf ein Profil mit leerem Feld für die benutzerdefinierte Ressource wird jetzt eine Fehlermeldung anstelle einer leeren Liste angezeigt.
* Es wurde ein Fehler behoben, der bei der Verwendung der Ersetzung von Profilen in einem Workflow auftrat, bei dem die Seite die Versand-Profil nicht geladen hat, wenn das zu ersetzende Profil ausgewählt wurde. (CAMP-46522)
* Es wurde eine Regression behoben, bei der der technische Arbeitsablauf **Datenbankbereinigung** versucht hat, abgelaufene Versand-Tabellen abzulegen, was zu folgenden Fehlern führte: (CAMP-46536)

```
   PGS-220000 PostgreSQL error: ERROR: table ""wkdlv_24439460_data"" does not exist and WDB-200001 SQL statement 'DROP TABLE wkdlv_24448131_data' could not be executed.
```

* Es wurde der folgende Fehler behoben, der in einigen Fällen bei der Verwendung des benutzerspezifischen Filters für benutzerdefinierte Ressourcen auftrat: (CAMP-46509)

```
   The 'profile/xxxx' field used in the filter 'xxxxx' does not exist in custom resource 'xxx'
```

* Es wurde ein Problem behoben, bei dem die Vorbereitung der Push-Benachrichtigung zu lange dauerte, bis sie abgeschlossen war. Dies wurde durch einen fehlenden Index an den transienten Arbeitstabellen verursacht.
* Es wurde ein Fehler behoben, der auftrat, wenn die Option **Dimension zum Abgleich** in einer **Versöhnung**-Aktivität in einem Workflow verwendet wurde, wenn bereits eine Beziehung zwischen einer benutzerspezifischen Ressource und einer Profil-Ressource definiert war.
* Es wurde ein Problem behoben, das beim Hinzufügen von Links über eine **Versöhnung**- oder **Anreicherung**-Aktivität auftrat. Ausgewählte Links wurden nicht in der Transition &quot;Ausgabe&quot;angezeigt.
* Es wurde ein Fehler behoben, der beim Verwenden einer **Segmentierung**-Aktivität mit wiederkehrenden Versänden in einem Workflow dazu führte, dass der Versand an die falsche Audience gesendet wurde. (CAMP-46275, CAMP-46470)
* Es wurde ein Fehler behoben, bei dem die Veröffentlichung benutzerdefinierter Ressourcen fehlschlug, wenn versucht wurde, die Profil-Ressource zu erweitern, um benutzerdefinierte Profil-Dimensionen für den dynamischen Berichte zu erstellen. (CAMP-46266)
* Es wurde ein Fehler behoben, der beim Hinzufügen eines Links zu einer Datei-Importtabelle auftrat. Nachdem Sie der Aktivität **Dateiimport** eine **Anreicherung**-Aktivität hinzugefügt haben, verschwand der zuvor konfigurierte Link. (CAMP-46557)
* Es wurde ein Fehler behoben, der bei der Verwendung benutzerdefinierter Ressourcen, die mit Profil-Daten verknüpft sind, dazu führte, dass die Anzeigereihenfolge im Anzeigebereich &quot;Detailkonfiguration&quot;beim Speichern geändert wurde. (CAMP-46312)
* Es wurde ein Problem behoben, durch das Sie aufgrund von Versänden, die auf einer benutzerdefinierten Versand-Zuordnung basieren, keine Daten im dynamischen Berichte anzeigen konnten.
* Es wurde ein Fehler behoben, der dazu führte, dass Sie eine Sammlung mit einer falschen Ressourcenausführung in einer Workflow-Abfrage-Aktivität nicht auswählen konnten.
* Es wurde ein Fehler behoben, der dazu führen konnte, dass der InMail-Prozess die Absprünge falsch validierte.
* Es wurde ein Fehler behoben, der beim Öffnen eines Profil-Bildschirms aufgrund eines Link-Fehlers auftrat.
* Es wurde ein Problem behoben, das das Löschen von GDPR-Daten aus dem Bereinigungsarbeitsablauf verhinderte.
* Es wurde ein Fehler behoben, der auftrat, wenn die Planungskonfiguration manuell mit der Tastatur in den E-Mail-Versand-Planparametern aktualisiert wurde.
* Es wurde ein Problem behoben, durch das Sie möglicherweise ein Profil aufgrund falscher Parameter in der Einheit &quot;Unternehmen&quot;nicht bearbeiten konnten.
* Es wurde ein Fehler behoben, der dazu führte, dass das Feld für die Diensterweiterung leer war und in den E-Mail-Eigenschaften nicht eingestellt werden konnte, selbst wenn es in der Versandvorlage festgelegt wurde.
* Es wurde ein Fehler behoben, der dazu führte, dass Testversand länger verarbeitet werden konnten. (CAMP-45048)
* Es wurde ein Problem behoben, das das Sortieren von Spalten in einem Profil-Übersichtsbildschirm verhinderte.
* Es wurde ein Problem bei der Erstellung von Miniaturbildern behoben, das in Azurblauen in E-Mail-Varianten mit chinesischen Zeichen auftreten konnte. (CAMP-47152)
* Es wurde eine Regression behoben, die in 20.4 eingeführt wurde und aufgrund der Filterung von Ereignissen, die von Gmail-Konten empfangen wurden, zu fehlerhaften Open Rate für Gmail führen konnte. (CAMP-46504)
* Es wurde ein Problem behoben, durch das HTML-Inhalte nicht in eine Transaktionsnachrichtenvorlage importiert werden konnten. (CAMP-47318)
* Es wurde ein Problem behoben, durch das die Anzeige der Renderings im Bericht zur E-Mail-Wiedergabe verlangsamt werden konnte. (CAMP-46226)
* Es wurde ein Fehler behoben, der dazu führte, dass benutzerdefinierte Ressourcen, die mit einem Liste-Typ-Element in der Bildschirmdefinition konfiguriert wurden, nicht veröffentlicht werden konnten. (CAMP-47217)
* Es wurde ein Fehler im E-Mail-Designer behoben, der verhinderte, dass Zeilenunterteilungen in Microsoft Outlook korrekt dargestellt wurden, wenn sie oben im E-Mail-Inhalt platziert wurden. (CAMP-46294)
* Es wurde ein Fehler behoben, der dazu führte, dass die KPIs-Abstimmung mit dem technischen Arbeitsablauf von Adobe Analytics blockiert wurde. (CAMP-46576)
* Es wurde ein Fehler im E-Mail-Designer behoben, der dazu führte, dass Fragmente nicht automatisch in Suchfeldern angezeigt wurden, wenn Inhaltsblöcke eingefügt wurden. (CAMP-44205)
* Es wurde ein Fehler im E-Mail-Designer behoben, der dazu führte, dass unerwünschte Zeichen in gesendeten E-Mails angezeigt wurden, wenn Emojis in Fragmenten verwendet wurde. (CAMP-46621)
* Korrektur der Regression, die in Version 20.4 des E-Mail-Designers eingeführt wurde und sich auf die Trennzeichenkomponente auswirkte, was zu zusätzlichen Zeilenhöhen und Bildverzerrungen im Inhalt führte. (CAMP-46663)
* Es wurde ein Fehler behoben, der dazu führte, dass die vordefinierten Schaltflächen beim Senden der Nachricht an ein Outlook-Postfach zentriert blieben, obwohl diese Schaltflächen im E-Mail-Designer rechts oder links ausgerichtet waren. (CAMP-46466)
* Es wurde ein Fehler behoben, der verhinderte, dass die Liste der Testelemente aktualisiert wurde, wenn Profil in der Vorschau E-Mail-Designer durchsucht wurden. (CAMP-45265)
* Es wurde ein Fehler behoben, der verhinderte, dass benutzerdefinierte Testelemente in der Liste angezeigt wurden, wenn Profil in der Vorschau E-Mail-Designer durchsucht wurden. (CAMP-45589)
* Es wurde ein Fehler behoben, der dazu führte, dass beim Generieren von Trendgrafiken aus dem Zusammenfassungsbericht des Versands falsche Datumsangaben angezeigt wurden. (CAMP-45521)

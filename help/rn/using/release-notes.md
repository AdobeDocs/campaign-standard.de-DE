---
title: Aktuelle Version
description: Auf dieser Seite finden Sie Informationen zum Inhalt der aktuellen Version von Campaign Standard.
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: 7066cf1d8454ffdefa29bff5092ba2c3e1bac705
workflow-type: tm+mt
source-wordcount: '1766'
ht-degree: 99%

---


# Aktuelle Version{#latest-release}

## Version 22.1 – Februar 2022 {#feb-2022}

**Neue Funktionen**

<table> 
<thead> 
<tr> 
<th> <strong>Sicherheitsupdate für Sicherheitslücken in Apache Log4j</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Apache Log4j hat die gemeldeten Sicherheitslücken in Apache Log4j v2.17.1 behoben. Adobe Campaign Standard verwendet Apache Log4j und diese Campaign-Version enthält die neueste Version, Apache Log4j v2.17.1 </p>
</td> 
</tr> 
</tbody> 
</table>

**Sicherheitskorrekturen**

* Neuer URL-Signaturmechanismus für Tracking in dieser Version. Der frühere Mechanismus wurde deaktiviert, um ein Problem zu vermeiden, das dazu führte, dass einige gültige, signierte Tracking-Links fälschlicherweise blockiert wurden, nachdem sie durch Sicherheits-Tools von Drittanbietern geändert worden waren. (CAMP-48983)

**Verbesserungen**

* Die Verarbeitung von Berichtsdaten wurde verbessert, um zu vermeiden, dass das System überlastet wird. (CAMP-47578)
* Nach dem Versand Ihrer In-App-Nachrichten können Sie jetzt Ihren Versand deaktivieren. Auf diese Weise können Sie Ihren Versand löschen, ohne Berichtsdaten zu verlieren. (CAMP-48469)
* Um Probleme zu vermeiden, können Benutzer für eine benutzerdefinierte Tabellenspalte nicht mehr denselben Namen wie für den automatischen Primärschlüssel in der Datenbank verwenden. `"<dataType><resourceName>Id"`. (CAMP-49358)
* Sie können jetzt Ihren Versand überwachen und die Vorgangslogs über das neue Dropdown-Menü **Vorgangsverlauf** im Dashboard Ihrer Nachrichten verfolgen. (CAMP-49840)
* Die Stabilität und Datenbanksicherheit wurde durch Reduzierung von toten Tupeln verbessert. Diese treten auf, wenn im Laufe der Zeit eine große Anzahl von Nachrichten über alle Kanäle gesendet wird. (CAMP-49755, CAMP-49792, CAMP-49849)
* Im Mail Transfer Agent (MTA) von Campaign wurden Verbesserungen implementiert, um sicherzustellen, dass Datenbankverbindungen im Fall eines Datenbankabsturzes oder eines erneuten Starts automatisch aktualisiert werden. (CAMP-48063)


**Patches**

* Es wurde ein Problem mit der Option **Bericht jetzt senden** in dynamischen Berichten behoben: Die PDF-Generierungsvorgänge schlugen bei Sendungen mit Mehrfachvarianten fehl. (CAMP-49120)
* Es wurde ein Problem behoben, durch das Benutzer Inhalte aus Adobe Experience Manager (AEM) nicht in ihren Sendungen mit Adobe Campaign Standard aktualisieren oder deren Verknüpfung aufheben konnten, wenn duplizierte Inhalte in AEM denselben Schlüssel (cq:uuid) hatten. (CAMP-49161)
* Fehlerkorrektur – Der Zugriff auf eine Instanz, in der Seiten nicht geladen, Sendungen nicht geöffnet oder ausstehende Änderungen nicht gespeichert werden konnten, funktioniert nun fehlerfrei. (CAMP-50195)
* Fehlerkorrektur – Das Kriterium für die Versandwarnung kann jetzt geöffnet werden, wenn das Feld **Zustellungsfilter**, das von diesem Kriterium verwendet wird, ausgefüllt ist. (CAMP-49093)
* Fehlerkorrektur – Beim Bearbeiten der Schaltfläche **Sekundär** in In-App-Sendungen werden Änderungen jetzt berücksichtigt. (CAMP-50250)
* Fehlerkorrektur – In japanischen Instanzen können Benutzer jetzt als **Ausführungsfrequenz** in der **Planungsaktivität** „Mehrmals am Tag“ auswählen. (CAMP-50247)
* Fehlerkorrektur – Bei der Arbeit mit einer japanischen Benutzeroberfläche wird jetzt bei der Auswahl einer Uhrzeit in einer Planungsaktivität keine Fehlermeldung mehr angezeigt. (CAMP-49289)
* Fehlerkorrektur – in Push-Benachrichtigungsberichten werden verworfene Push-Benachrichtigungen jetzt nicht mehr als **Offen**, sondern als **Impression** angezeigt. (CAMP-45980)
* Fehlerkorrektur – Beim Öffnen eines Berichts tritt jetzt kein Fehler mehr auf. (CAMP-49222)
* Fehlerkorrektur – Die E-Mail-Vorbereitung schlägt jetzt nicht mehr fehl, nachdem ein Link zu AEM-Inhalten gelöscht wurde. (CAMP-49877)
* Um verschiedene Probleme zu lösen, wurde der Wiederholungsmechanismus für Sendungen, einschließlich aus einer URL importierter Inhalte, verbessert. [Weitere Infos](../../designing/using/using-existing-content.md#retrieving-content-from-a-url-automatically-at-preparation-time) (CAMP-48888)
* Fehlerkorrektur – jetzt tritt kein Fehler mehr auf, nachdem ein neuer Filter in einer benutzerdefinierten Ressource erstellt und als Abstimmschlüssel in einer Landingpage verwendet wurde. Wenn die benutzerdefinierte Ressource erneut veröffentlicht wurde, wurde der Filter aus der Liste der verfügbaren Abstimmschlüssel für die Landingpage entfernt. (CAMP-49516)
* Fehlerkorrektur – Auf Landingpages tritt jetzt kein Fehler mehr auf, wenn dynamische Bedingungen mit Kontrollkästchen verwendet werden. (CAMP-48604)
* Es wurde ein Problem behoben, das in einer **Abfrage**-Aktivität bei Verwendung der Filterbedingung &quot;In oder vor Oktober&quot; auftrat. Bei der Arbeit in einer auf eine europäische Zeitzone festgelegten Instanz wurde als ausgewählter Monat für den Filter September anstelle Oktober angezeigt, da beim Konvertieren der Zeitzone ein Problem aufgetreten war. (CAMP-48602)
* Um die Zustellbarkeit zu optimieren, sendet Adobe Campaign jetzt E-Mails mit 7-Bit-Codierung anstelle von 8-Bit-Codierung. Dadurch wird verhindert, dass Zwischenrelais die DKIM-Signatur ungültig machen, was sich auf die Authentizität der Nachrichten auswirken könnte. (CAMP-49016)
* Die Leistung beim Duplizieren von Audiences wurde verbessert, um Probleme beim Arbeiten mit großen Audiences zu vermeiden. (CAMP-49639)
* Fehlerkorrektur – Benutzerdefinierte Filter zeigen jetzt die richtigen Ergebnisse an, wenn sie in einer **Abfrage**-Aktivität verwendet werden. (CAMP-49417)
* Fehlerkorrektur – bei der Verwendung eines Fragments in einem Versand, dessen Name ein Komma enthält, wird jetzt keine Fehlermeldung mehr angezeigt. Das Problem wurde behoben. Kommas können jetzt in Fragmentnamen verwendet werden. (CAMP-49216)


## Version 21.3 – September 2021 {#release-21-3---sept-2021}

Im Folgenden finden Sie die in der neuesten Campaign Standard-Version enthaltenen neuen Funktionen, Verbesserungen und Fehlerbehebungen.

**Neue Funktionen**

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

<table> 
<thead> 
<tr> 
<th> <strong>Audit-Protokoll</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Die neue Audit-Protokoll-Funktionalität erfasst eine umfassende Liste von in Adobe Campaign auftretenden Aktionen und Ereignissen in Echtzeit. Sie beinhaltet eine Self-Service-Option für den Zugriff auf einen Datenverlauf, damit sich zum Beispiel folgende Fragen beantworten lassen:</p>
<ul>
<li>Was ist mit diesem Workflow passiert und wer hat ihn zuletzt aktualisiert?</li>
<li>Wer hat die letzten Änderungen vorgenommen?</li>
<li>Wie war der vorherige Status?</li>
</ul>
<p>Adobe Campaign führt nun Prüfungen für Erstellungs-, Bearbeitungs- und Löschaktionen für Workflows, Optionen und benutzerdefinierte Ressourcen durch. Änderungen dieser Elemente werden ebenfalls verfolgt.</p>
<p>Weitere Informationen finden Sie im <a href="../../administration/using/audit.md">entsprechenden Handbuch</a>.</p>
</td> 
</tr> 
</tbody> 
</table>


<table> 
<thead> 
<tr> 
<th> <strong>Workflow-Diagnosemodus</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Sie können Campaign-Workflows jetzt im Diagnosemodus ausführen. In diesem Modus werden Informationen protokolliert, die bei der Fehlerbehebung von Problemen bei der Ausführung helfen. Wenn eine Workflow-Abfrage mehr als eine Minute dauert, wird standardmäßig der gesamte Ausführungsplan protokolliert.</p>
<p>Weitere Informationen finden Sie im <a href="../../automating/using/managing-execution-options.md">entsprechenden Handbuch</a>.</p>
</td> 
</tr> 
</tbody> 
</table>

**Verbesserungen bezüglich der Sicherheit**

* Die Sicherheit wurde zum Schutz vor SSRF-Angriffen verbessert. (CAMP-47836)
* Die Liste der Benutzer ist jetzt auf Administratoren beschränkt. (CAMP-47260)
* Umgebungsvariablen können nicht mehr als Teil der Parametererweiterung in einer URL verwendet werden. (CAMP-47268)

**Verbesserungen**

* Beim Erstellen eines wiederkehrenden Versands in einem Workflow, der mit einem Adobe Experience Manager-Inhalt verknüpft ist, wird der Status der Inhaltsvalidierung nun vor dem Versenden überprüft.
* Die Beschränkung der Datenbankverbindung ist jetzt mit dem Campaign-Package abgestimmt, um Verbindungsfehler zu vermeiden.
* Eine neue Konsistenzprüfung bei der Veröffentlichung benutzerdefinierter Ressourcen verhindert, dass Benutzer doppelte Indizes erstellen, wodurch die Veröffentlichung fehlschlägt. Eine verbesserte Fehlermeldung fordert den Benutzer auf, den Index bei Bedarf umzubenennen. [Weitere Informationen](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource)

**Sonstige Änderungen**

* Der Adobe Experience Platform Data Connector- und Audience Destinations-Service wird jetzt von Campaign Standard nicht mehr unterstützt. Wenn Sie diese Funktionen verwenden, müssen Sie zu Adobe-Quellen und -Zielen wechseln und Ihre Implementierung anpassen. [Weitere Informationen](../../integrating/using/get-started-sources-destinations.md)   
* Veraltete und entfernte Funktionen sind auf [dieser Seite](deprecated-features.md) aufgeführt.
* Die neue Aggregatfunktion &quot;StringAgg&quot; wurde eingeführt, um die Werte einer Spalte vom Typ Zeichenfolge zu verketten. (CAMP-47077) [Mehr dazu](../../automating/using/list-of-functions.md#aggregates)
* Der technische Workflow **Aktualisierung der Versandindikatoren** (updateDeliveryIndicators) wurde verbessert, um die Leistung zu steigern.
* In-App-Messaging-Vorlagen sind jetzt für alle in Campaign Standard unterstützten Sprachen verfügbar.
* Die Versandvorbereitungszeit wurde für Transaktionsnachrichten optimiert, indem die Anzahl der Aufrufe an den Tracking-Server während der Versandanalyse reduziert wurde.
* Eine neue Warnmeldung informiert Benutzer über eine hohe Absprungrate.
* Protokollfehlermeldungen und -warnungen wurden verbessert, um die Fehlerbehebung zu vereinfachen, wenn die Trackinglogs nicht ordnungsgemäß abgerufen werden können. (CAMP-48939, CAMP-47360)
* Sie können jetzt URLs, einschließlich des Domain-Namens, vollständig personalisieren. [Weitere Infos](../../designing/using/personalization.md#personalizing-urls)

**Korrekturen**

* Fehlerkorrektur – Der Zeitüberschreitungsfehler beim Import von E-Mail-Inhalten aus einer URL wurde behoben. (CAMP-49054)
* Fehlerkorrektur – Der Zugriff auf eine mit Lesezeichen versehene URL oder das Aktualisieren einer Seite im Browser führt nicht mehr zum Sitzungsende und zu einem Fehler (-69). (CAMP-49003, CAMP-48930, CAMP-48894)
* Fehlerkorrektur – Regeln werden jetzt vom alten Zustellbarkeits-Server auf den neuen fehlerfrei synchronisiert. (CAMP-48923)
* Fehlerkorrektur – E-Mail-Vorlagen mit HTML-Tags werden in Email Designer jetzt fehlerfrei geladen. (CAMP-48243)
* Fehlerkorrektur – Adobe Experience Manager-Inhalt wird jetzt beim Erstellen von Transaktionsnachrichten mit Email Designer geladen. (CAMP-49075)
* Fehlerkorrektur – In der Benutzeroberfläche wird zwischen der oberen Leiste und dem Inhalt nicht mehr zu viel Abstand hinzugefügt.
* Fehlerkorrektur – Bei Transaktionsnachrichten tritt jetzt kein Veröffentlichungsfehler mehr auf, wenn Campaign-Inhaltsbausteine in Adobe Experience Manager-Inhalten verwendet werden. (CAMP-49233)
* Fehlerkorrektur – Jetzt wird keine Fehlermeldung mehr angezeigt, wenn die Authentifizierung fehlschlägt. Der Benutzer wird nun zur Anmeldeseite weitergeleitet.
* Fehlerkorrektur – In der Token-Anzeige tritt kein Fehler mehr auf, der Benutzer daran hindert, einen Bericht zu bearbeiten oder freizugeben.
* Fehlerkorrektur – Die Veröffentlichung einer benutzerdefinierten Ressource mit einem Filterausdruck mit 1:n-Tabellenbeziehungen funktioniert jetzt problemlos. (CAMP-48740)
* Fehlerkorrektur – Jetzt kann in Workflow-Transitionen das Versandkontaktdatum abgerufen werden. (CAMP-48871)
* Fehlerkorrektur – Jetzt können Versandlogs während der Erstellung einer benutzerdefinierten Profildimension problemlos erweitert werden.
* Fehlerkorrektur – Sendungen mit mehreren Sprachvarianten schlagen jetzt nicht mehr fehl. Wenn ein Benutzer die Standardsprache löscht, muss ab jetzt eine andere Sprachvariante als Standard festgelegt werden, bevor Sprachkopien erstellt werden. (CAMP-48235)
* Fehlerkorrektur – E-Mail-Nachrichten zeigen in Outlook keine zusätzlichen Leerzeichen mehr an, wenn der Benutzer beim Entwerfen der Nachricht die Option **Nur auf Mobilgeräten anzeigen** ausgewählt hat. (CAMP-48902)
* Fehlerkorrektur – Das Feld &quot;Letzter Ausführungstag der inkrementellen Abfrageaktivität&quot; fehlt jetzt nicht mehr in der Registerkarte **Verarbeitete Daten**, nachdem der inkrementelle Abfrage-Workflow ausgeführt wurde. (CAMP-48879)
* Fehlerkorrektur – in der Workflow-Aktivität **Segmentierung** können Sie jetzt einen dynamischen Segment-Code ordnungsgemäß definieren. (CAMP-48727)
* Fehlerkorrektur – Das Speichern eines Workflows nach dessen Bearbeitung erfolgt nun zuverlässig und fehlerfrei. (CAMP-48695)
* Fehlerkorrektur – Jetzt können benutzerdefinierte Ressourcen problemlos veröffentlicht werden, da das Datenschema eines Triggers nach dem Löschen des Triggers nicht mehr beibehalten wird. (CAMP-48523)
* Fehlerkorrektur – Feedback-Schleifenanfragen werden jetzt berücksichtigt, da der InMail-Prozess die zu aktualisierenden Versandlogs jetzt zuverlässig abrufen kann. (CAMP-48705)
* Fehlerkorrektur – Die Ausschlussoptionen in der Workflow-Aktivität **Ausschluss** können jetzt ordnungsgemäß definiert werden.(CAMP-48355)
* Fehlerkorrektur – Jetzt tritt kein Fehler mehr auf, wenn Anreicherungsaktivitäten in Workflows Anmeldungen zu oder Abmeldungen von einem Dienst beinhalten. Dieses Problem führte zum Absturz.
* Fehlerkorrektur – Workflows können jetzt zuverlässig ausgeführt werden.
* Fehlerkorrektur – Benutzer können jetzt native Sicherheitsgruppen in der Benutzeroberfläche umbenennen oder löschen.
* Fehlerkorrektur – Benutzer können jetzt einen unvollständigen Ereignisveröffentlichungsvorgang löschen.
* Fehlerkorrektur – Der Datenbankbereinigungs-Workflow kann jetzt fehlerfrei ausgeführt werden. (CAMP-49097)

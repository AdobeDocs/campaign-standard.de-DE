---
title: Vorzeitige Versionshinweise
description: Vorzeitige Versionshinweise
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 43%

---

# Vorzeitige Versionshinweise {#new-release}

Auf dieser Seite werden neue Funktionen, Verbesserungen und Fehlerbehebungen beschrieben, die in der nächsten Campaign Standard-Version enthalten sind.

>[!CAUTION]
>
> Dieser Inhalt kann ohne vorherige Ankündigung bis zum Aktualisierungsdatum der Staging-Umgebung geändert werden. Weitere Informationen finden Sie auf der [Seite mit der Versionsplanung](../../rn/using/release-planning.md).

## Version 21.3 – September 2021 {#release-21-3---sept-2021}

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
* Die Liste der Benutzer ist jetzt nur noch auf Administratoren beschränkt. (CAMP-47260)
* Umgebungsvariablen können nicht mehr als Teil der Parametererweiterung in einer URL verwendet werden. (CAMP-47268)

**Verbesserungen**

* Beim Erstellen eines wiederkehrenden Versands in einem Workflow, der mit einem Adobe Experience Manager-Inhalt verknüpft ist, wird der Status der Inhaltsvalidierung nun vor dem Versenden überprüft.
* Die Beschränkung der Datenbankverbindung ist jetzt mit dem Campaign-Package abgestimmt, um Verbindungsfehler zu vermeiden.
* Es wurde eine Konsistenzprüfung beim Erstellen von Indizes in benutzerdefinierten Ressourcen hinzugefügt und die Fehlermeldungen wurden verbessert.

**Sonstige Änderungen**

* Der Adobe Experience Platform Data Connector- und Audience Destinations-Dienst wird jetzt mit Campaign Standard nicht mehr unterstützt. Wenn Sie diese Funktionen verwenden, müssen Sie zu Adobe-Quellen und -Zielen wechseln und Ihre Implementierung anpassen. [Weitere Informationen](../../integrating/using/get-started-sources-destinations.md)   
* Veraltete und entfernte Funktionen sind auf [dieser Seite](deprecated-features.md) aufgeführt.
* Die neue Aggregatfunktion &quot;StringAgg&quot; wurde eingeführt, um die Werte einer Spalte vom Typ Zeichenfolge zu verketten. (CAMP-47077)
* Der technische Workflow **Aktualisierung der Versandindikatoren** (updateDeliveryIndicators) wurde verbessert, um die Leistung zu verbessern.
* In-App-Messaging-Vorlagen sind jetzt für alle in Campaign Standard unterstützten Sprachen verfügbar.
* Die Versandvorbereitungszeit wurde für Transaktionsnachrichten optimiert, indem die Anzahl der Aufrufe an den Tracking-Server während der Versandanalyse reduziert wurde.
* Eine neue Warnmeldung informiert Benutzer über eine hohe Absprungrate.
* Verbesserte Protokollfehlermeldungen und -warnungen, um das Debugging zu vereinfachen, wenn die Trackinglogs nicht ordnungsgemäß abgerufen werden konnten. (CAMP-48939, CAMP-47360)
* Sie können jetzt URLs, einschließlich des Domänennamens, vollständig personalisieren. [Weitere Infos](../../designing/using/personalization.md#personalizing-urls)

**Korrekturen**

* Fehlerkorrektur – Der Zeitüberschreitungsfehler beim Import von E-Mail-Inhalten aus einer URL wurde behoben. (CAMP-49054)
* Es wurde ein Fehler (-69) behoben, der durch ein Ende der Sitzung verursacht wurde, wenn auf eine mit Lesezeichen versehene URL zugegriffen oder eine Seite über den Browser aktualisiert wurde. (CAMP-49003, CAMP-48930, CAMP-48894)
* Fehlerkorrektur – Regeln werden jetzt vom alten Zustellbarkeits-Server auf den neuen fehlerfrei synchronisiert. (CAMP-48923)
* Fehlerkorrektur – E-Mail-Vorlagen mit HTML-Tags werden in Email Designer jetzt fehlerfrei geladen. (CAMP-48243)
* Fehlerkorrektur - Adobe Experience Manager-Inhalt wird jetzt beim Erstellen von Transaktionsnachrichten mit Email Designer geladen. (CAMP-49075)
* Es wurde ein Problem in der Benutzeroberfläche behoben, bei dem zwischen der oberen Leiste und dem Inhalt zu viel Abstand hinzugefügt wurde.
* Fehlerkorrektur - Bei Transaktionsnachrichten tritt jetzt kein Veröffentlichungsfehler mehr auf, wenn Campaign-Inhaltsbausteine in Adobe Experience Manager-Inhalten verwendet werden. (CAMP-49233)
* Fehlerkorrektur - jetzt wird keine Fehlermeldung mehr angezeigt, wenn die Authentifizierung fehlschlägt. Der Benutzer wird nun zur Anmeldeseite weitergeleitet.
* Es wurde ein Problem mit der Token-Anzeige behoben, das Benutzer daran hinderte, einen Bericht zu bearbeiten oder freizugeben.
* Fehlerkorrektur - Es wurde ein Problem bei der Veröffentlichung einer benutzerdefinierten Ressource mit einem Filterausdruck mit 1:n-Tabellenbeziehungen behoben. (CAMP-48740)
* Fehlerkorrektur - jetzt können in Workflow-Transitionen Versandkontaktdaten abgerufen werden. (CAMP-48871)
* Fehlerkorrektur - jetzt kann die Erweiterung von Versandlogs während der Erstellung einer benutzerdefinierten Profildimension aktiviert werden.
* Fehlerkorrektur - Sendungen mit mehreren Sprachvarianten schlagen jetzt nicht mehr fehl. Wenn ein Benutzer die Standardsprache löscht, muss ab jetzt eine andere Sprachvariante als Standard festgelegt werden, bevor Sprachkopien erstellt werden. (CAMP-48235)
* Es wurde ein Problem behoben, bei dem E-Mail-Nachrichten in Outlook zusätzliche Leerzeichen anzeigten, wenn der Benutzer beim Entwerfen der Nachricht die Option **Nur auf Mobilgeräten anzeigen** ausgewählt hatte. (CAMP-48902)
* Fehlerkorrektur - Das letzte Ausführungsdatum des Felds für die inkrementelle Abfrageaktivität fehlt jetzt im Tab **Verarbeitete Daten** , nachdem der inkrementelle Abfrage-Workflow ausgeführt wurde. (CAMP-48879)
* Fehlerkorrektur - in der Workflow-Aktivität **Segmentierung** können Sie jetzt einen dynamischen Segmentcode ordnungsgemäß definieren. (CAMP-48727)
* Fehlerkorrektur - der Speichern eines Workflows nach dessen Bearbeitung erfolgt nun fehlerfrei und zufällig. (CAMP-48695)
* Fehlerkorrektur - Jetzt können benutzerdefinierte Ressourcen veröffentlicht werden, da das Datenschema eines Triggers auch nach dem Löschen des Triggers beibehalten wird. (CAMP-48523)
* Fehlerkorrektur - Feedback-Schleifenanfragen werden jetzt berücksichtigt, da der InMail-Prozess die zu aktualisierenden Versandlogs nicht abrufen konnte. (CAMP-48705)
* Fehlerkorrektur - Die Ausschlussoptionen in der Workflow-Aktivität **Ausschluss** können jetzt ordnungsgemäß definiert werden.(CAMP-48355)
* Fehlerkorrektur - Jetzt tritt kein Fehler mehr auf, wenn Anreicherungsaktivitäten in Workflows Abonnements oder Abmeldungen von einem Dienst erfordern. Dieses Problem führte zum Absturz.
* Fehlerkorrektur - Workflows können jetzt ausgeführt werden.
* Fehlerkorrektur - Benutzer können jetzt vordefinierte Sicherheitsgruppen in der Benutzeroberfläche umbenennen oder löschen.
* Fehlerkorrektur - Benutzer können jetzt einen unvollständigen Ereignisveröffentlichungsauftrag löschen.
* Fehlerkorrektur - Der Datenbankbereinigungs-Workflow schlägt jetzt nicht mehr mit einem Fehler fehl. (CAMP-49097)

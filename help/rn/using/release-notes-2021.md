---
title: Versionshinweise 2021
description: Auf dieser Seite werden alle Versionen von Adobe Campaign Standard von 2021 aufgelistet.
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
feature: Overview
role: User
level: Beginner
exl-id: 225c65cc-2964-4b71-84a9-30fcd22d75bf
source-git-commit: afb988281f00dc17b484872259d44f51864d55f1
workflow-type: tm+mt
source-wordcount: '4695'
ht-degree: 99%

---

# Versionshinweise 2021{#release-notes-2021}

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
* Der technische Workflow **Aktualisierung der Versandindikatoren** (updateDeliveryIndicators) wurde verbessert, um die Performance zu steigern.
* In-App-Messaging-Vorlagen sind jetzt für alle in Campaign Standard unterstützten Sprachen verfügbar.
* Die Versandvorbereitungszeit wurde für Transaktionsnachrichten optimiert, indem die Anzahl der Aufrufe an den Tracking-Server während der Versandanalyse reduziert wurde.
* Eine neue Warnmeldung informiert Benutzer über eine hohe Absprungrate.
* Protokollfehlermeldungen und -warnungen wurden verbessert, um die Fehlerbehebung zu vereinfachen, wenn die Trackinglogs nicht ordnungsgemäß abgerufen werden können. (CAMP-48939, CAMP-47360)
* Sie können jetzt URLs, einschließlich des Domain-Namens, vollständig personalisieren. [Weitere Informationen](../../designing/using/personalization.md#personalizing-urls)
* Testversand- und Trap-Profile wurden jetzt in dynamischen Berichten aus der dynamischen Berechnung der Versand-Performance ausgeschlossen. (CAMP-47338)

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


## Version 21.2 – Juni 2021 {#release-21-2---june-2021}

Im Folgenden finden Sie die in der kommenden Campaign Standard-Version enthaltenen neuen Funktionen, Verbesserungen und Fehlerbehebungen. Im Folgenden finden Sie die in dieser Campaign Standard-Version enthaltenen neuen Funktionen, Verbesserungen und Fehlerbehebungen.

**Verbesserungen**

* Beim Erstellen einer Landingpage können Sie jetzt eine obligatorische Checkbox hinzufügen, die die Profile vor dem Absenden des Formulars markieren müssen. Weitere Informationen finden Sie im [entsprechenden Handbuch](../../channels/using/managing-landing-page-form-data.md#agreement-checkbox).

* Für die Integration von Triggers wurde die Fehlermeldung verbessert, die angezeigt wird, wenn in der Trigger-Payload keine Abstimmdaten eingehen: &quot;In der Payload fehlen Alias-Daten&quot;.

* die Performance beim Abrufen von Push-Benachrichtigungen aus der Warteschlange wurde verbessert.

**Sonstige Änderungen**

* Der URL-Signaturmechanismus für Tracking-Links wurde deaktiviert, um zu verhindern, dass einige gültige, signierte Tracking-Links nach der Änderung durch Sicherheits-Tools von Drittanbietern fälschlicherweise blockiert werden.

* In Sendungen mit mehreren Varianten können Benutzer keine Sprachkopien mehr erstellen, wenn die Standardvariante gelöscht wurde. Bei der Erstellung einer Sprachkopie wird nun eine Meldung angezeigt. (CAMP-48235)

* Der zweistufige Prozess zum Löschen von Profilen (eingestellt ab Campaign-Version 19.4) ist jetzt standardmäßig deaktiviert. Zuvor musste der Prozess vor der Verwendung von Privacy Core Service manuell über die Campaign-Benutzeroberfläche deaktiviert werden. Andernfalls verblieben Löschanfragen im Status &quot;Ausstehend&quot;, ohne abgeschlossen zu werden.

* In dynamischen Berichten wurde das Segment **Testversand ausschließen** entfernt. (CAMP-46161)

* Es wurde eine neue Warnmeldung hinzugefügt, die den Benutzer darüber informiert, wenn ein iOS-Zertifikat ohne den Wert &quot;platformPrincipal&quot; in das Campaign-Programm hochgeladen wird.

* Die maximale Größe einer E-Mail ist jetzt standardmäßig mit 100 MB festgelegt. Mit dieser Begrenzung können Fehler verhindert werden, durch die die Größe einer E-Mail unbegrenzt erhöht werden kann, was zu einem Systemabsturz führen könnte. (CAMP-47445) [Mehr dazu](../../sending/using/design-and-personalize.md#email-size)

* Die Integration von Asset Core Service mit Email Designer kann jetzt von Standardbenutzern verwendet werden.

* Es wurde eine neue Meldung hinzugefügt, die bestätigt, dass die Migration von einer v4-Push-Benachrichtigungs-App zu einer v5-Push-Benachrichtigungs-App erfolgreich war.

* Während der Erstellung von JSON Web Token zur Authentifizierung bei der Campaign Standard-API werden die Produktprofile jetzt **berücksichtigt**. Das bedeutet, dass die der Sicherheitsgruppe (die dem Produktprofil in Adobe I/O entspricht) zugewiesenen Organisationseinheiten und -rollen auf das für Campaign Standard REST-API-Aufrufe erforderliche technische IMS-Konto angewendet werden. (CAMP-47479)

**Korrekturen**

* Fehlerkorrektur – Die Gültigkeitsoption für die Protokolltabelle (**xtkjoblog**) der Batch-Verarbeitung kann jetzt angewendet werden. Zuvor konnte die Tabelle nicht korrekt bereinigt werden.

* Fehlerkorrektur – Die Reihenfolge der Filter in einer **Segmentierungs**-Workflow-Aktivität kann jetzt geändert werden. (CAMP-48357)

* Fehlerkorrektur – Sendungen schlagen nicht mehr mit einem Nullwertfehler fehl, da eine Regression von 20.4 behoben wurde. (CAMP-48591)

* Fehlerkorrektur – Das Senden eines Berichts über das Menü **Freigeben** > **Bericht jetzt senden** oder **Bericht planmäßig senden** ist jetzt möglich. (CAMP-47798)

* Fehlerkorrektur – Eine Regression wurde korrigiert, die zu falschen Öffnungsraten für Gmail geführt hatte, da von Gmail-Konten empfangene Tracking-Events gefiltert wurden. (CAMP-46504)

* Fehlerkorrektur – Zwischen Berichten in Adobe Campaign Standard und Berichten in Adobe Analytics gibt es jetzt keine Diskrepanzen mehr. (CAMP-47671, CAMP-47296)

* Fehlerkorrektur – Der Zugriff auf die Versandlogs ist jetzt auch möglich, wenn die Vorbereitung fehlgeschlagen ist. (CAMP-48296)

* Fehlerkorrektur – Beim Versuch, einen benutzerdefinierten Bericht zu bearbeiten, zu löschen oder zu senden, wird keine Fehlermeldung mehr angezeigt. (CAMP-47789, CAMP-47798)

* Fehlerkorrektur – Die API-Aufrufe beim Erstellen einer neuen benutzerdefinierten Ressource und beim Aktivieren der Option **Nicht synchronisieren** funktionieren jetzt fehlerfrei. (CAMP-48014)

* Fehlerkorrektur – Benutzerdefinierte Ressourcen mit der aktivierten Option **Nicht synchronisieren** verweisen nicht mehr auf ein Schema, das neu entworfen oder gelöscht wurde. Dieses Problem verursachte einen Fehler beim Veröffentlichen der benutzerdefinierten Ressourcen.

* Fehlerkorrektur – Bei der Verwendung mehrerer Kurzwahlnummern im selben externen Konto tritt kein SMS-Opt-out-Fehler mehr auf.

* Fehlerkorrektur – Der Zugriff auf eine neue Versandwarnungsbedingung ist jetzt nach der Veröffentlichung der Datenbank möglich. Zuvor wurde die Nachricht &quot;Die Ressource, auf die Sie zuzugreifen versuchen, ist nicht erreichbar&quot; angezeigt. (CAMP-48221)

* Fehlerkorrektur – In Campaign-Instanzen mit dynamischem Reporting sind jetzt alle Trackinglogs vorhanden. Es wurde ein neuer [technischer Workflow](../../administration/using/technical-workflows.md) hinzugefügt, um die fehlenden Trackinglogs bereitzustellen. (CAMP-47885)

* Fehlerkorrektur – In dynamischen Berichten werden Versanddaten jetzt angezeigt. Berichte wurden auf 0 gesetzt. (CAMP-47480)

* Fehlerkorrektur – Der Server-JavaScript-HTTP-Client kann sich jetzt mit einer externen URL verbinden.

* Fehlerkorrektur – Wenn der interne Name des Workflows geändert wird, wird die Aktivität **Inkrementelle Abfrage** nicht mehr zurückgesetzt. Dies trat auf, wenn ein Datumsfeld als inkrementeller Modus verwendet wurde. (CAMP-47674)

* Fehlerkorrektur – Wenn eine mehrsprachige E-Mail mit der Adobe Experience Manager-Integration erstellt wird, wird jetzt die Vorschau-Miniaturansicht in der Versandzusammenfassung angezeigt. Zuvor trat ein Problem, wenn die Schaltfläche **Erstellung von Sprachkopien** verwendet wurde, um die E-Mail-Varianten zu erstellen. (CAMP-47810)

* Fehlerkorrektur – Benutzer können jetzt vom untergeordneten E-Mail- oder SMS-Versand aus auf den übergeordneten Versand zugreifen. (CAMP-47986)

* Fehlerkorrektur – Beim Senden von Transaktionsnachrichten über die REST-API mit einem fehlenden benutzerdefinierten Ereignis werden CPU und Speicher nicht mehr übermäßig belastet. (CAMP-47147)

* Fehlerkorrektur – Das Senden von Echtzeitnachrichten mit der Transaktionsnachricht-API funktioniert jetzt reibungslos.

* Fehlerkorrektur – Nach Verwendung der Option **Bericht planmäßig senden** werden Berichte jetzt in jedem Fall empfangen. (CAMP-48583, CAMP-47786)

* Fehlerkorrektur – Nach Verwendung der Option **Bericht jetzt senden** werden Berichte jetzt vollständig und alle Daten enthaltend empfangen. (CAMP-48583)

* Fehlerkorrektur – Beim Hochladen eines Bildes mit Email Designer behalten Bilder ihre ursprünglichen Abmessungen. (CAMP-47017)

* Fehlerkorrektur – Jetzt werden alle verfügbaren Experience Manager-Vorlagen angezeigt, wenn ein Versand erstellt wird. (CAMP-48132)

* Fehlerkorrektur – Der Campaign-Link auf der Zusammenfassungsseite eines durchgeführten Versands leitet die Benutzer jetzt zuverlässig zu der zugehörigen Kampagne weiter. (CAMP-48012)

* Fehlerkorrektur – In Email Designer funktioniert jetzt die Integration von Asset Core Service, wenn ein Asset ausgewählt wird. (CAMP-47446)

* Fehlerkorrektur – Journey Orchestration-Sendungen werden jetzt nicht mehr blockiert. Zuvor unterstützte Campaign keine Zeitstempel mit einem exakten Wert (d. h. endend auf 00), die von Ereignissen in Journey Orchestration gesendet wurden.

## Version 21.1 – Februar 2021 {#release-21-1---february-2021}

**Neue Funktionen**

<table> 
<thead> 
<tr> 
<th> <strong>E-Mail-Feedback-Service</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>E-Mail-Feedback-Service (EFS) ist ein skalierbarer Dienst, der das Feedback direkt vom erweiterten MTA erfasst und damit die Reporting-Genauigkeit verbessert. Diese Funktion wird als private Betaversion veröffentlicht und wird in zukünftigen Versionen nach und nach allen Kunden zur Verfügung stehen.</p>
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

* Ein Parameter wurde an die Anzahl der Container angepasst, die den Datenbank-Pooling-Prozess für Transaktionsnachrichten ausführen. Dadurch kann die Last gleichmäßig auf alle verwendeten Container verteilt und eine optimale Performance erzielt werden.

* Eine neue **GetOption**-Funktion ist jetzt in Aktivitäten verfügbar, für die nach dem Aufruf eines Workflows mit externen Parametern Ereignisvariablen verwendet werden. Damit können Sie den Wert einer angegebenen Funktion zurückgeben. [Mehr dazu](../../automating/using/customizing-workflow-external-parameters.md)

* Eine neue Option ermöglicht es Campaign Standard, die Verfügbarkeit von **physischem Speicher** auf Ihrem System zu überprüfen, bevor ein Workflow gestartet wird. Steht zu wenig Speicher zur Verfügung, wird die Ausführung des Workflows verzögert, bis der Systemspeicher diesen Schwellenwert erreicht. Dadurch wird eine weitere Performance-Verschlechterung vermieden und das Risiko eines Ausfalls verringert. Der Workflow wird automatisch fortgesetzt, sobald die Auslastung des Servers abnimmt und der Speicher zunimmt. Beachten Sie, dass diese Option schreibgeschützt ist und nicht geändert werden kann. [Mehr dazu](../../automating/using/best-practices-workflows.md#execution)

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

* Es wurden optionale Parameter zu den JS-Funktionen &quot;cryptString&quot;und &quot;decryptString&quot;hinzugefügt, die mit den Adobe Campaign Standard-APIs übereinstimmen.

* Verbesserte Warn- und Fehlermeldungen in den Versandvorbereitungslogs.

* Verbesserte Fehlerprotokolle beim Versuch, eine Verbindung zum Adobe Identity Management Service (IMS) herzustellen.

* Sie können jetzt die Dimensionen für **Versand** und **Kampagne** weiter filtern, indem Sie die Suchleiste im dynamischen Reporting verwenden.

* Das Gültigkeitsdatum der SMS-Transaktionsnachricht kann jetzt durch den für den Ablaufparameter in der Transaktionsnachrichten-API festgelegten Wert definiert werden. (CAMP-36600)

* Beim dynamischen Reporting zeigte der integrierte Bericht **Versandzusammenfassung** falsche Daten für die Metrik der Abmelderate an. Eine neue Metrik mit dem Namen **Eindeutige Abmeldung** wurde hinzugefügt, um dies zu beheben. (CAMP-46445)

**Korrekturen**

* Es wurde ein Problem behoben, das dazu führte, dass Sendungen aufgrund bestimmter Prozesse sehr langsam ausgeführt wurden. Dies lag daran, dass für mehrere Parameter falsche Einheiten definiert waren (z. B. Millisekunden statt Sekunden).

* Es wurde ein Problem behoben, bei dem das Mobile SDK eine offene Tracking-Anfrage basierend auf der Bedingung sendete, dass deliveryId/MessageID nicht null ist. Dies führte bei Sendungen mit deaktiviertem Tracking zu 404-Fehlern. Eine zusätzliche Variable (acsDeliveryTracking) mit Informationen zum Tracking-Status des Versands wird jetzt in der Payload gesendet. Diese Variable kann je nach eingestelltem Tracking-Status zwei Werte haben: ein oder aus. [Weitere Informationen](../../administration/using/push-tracking.md).

* Es wurde ein Problem in Workflows behoben, das beim Kopieren und Einfügen einer **Deduplizierungs**-Aktivität auftrat, die einmal ausgeführt worden war und eine temporäre Ressource nutzte. Nach der Duplizierung wurde die Ressource der Aktivität automatisch auf &quot;Leer&quot; eingestellt, was zu Problemen bei anderen Aktivitäten des Workflows führte. Nach dem Einfügen bleibt die Ressource der Aktivität die gleiche, damit der Fehler so schnell wie möglich und nicht später im Workflow ausgelöst wird. (CAMP-46903)

* Es wurden Probleme behoben, die dazu führten, dass die Versandanalyse beim Senden einer Transaktions-Push-Benachrichtigung an Profile fehlschlug, indem ein neues [Zielgruppen-Mapping](../../administration/using/target-mappings-in-campaign.md) eingeführt wurde: **Profil – Echtzeitereignis für Push** (*mapRtEventAppSubRcp*). Die Versand-, Ausschluss- und Trackinglogs für [profilbasierte Transaktions-Push-Benachrichtigungen](../../channels/using/transactional-push-notifications.md#transactional-push-notifications-targeting-a-profile) werden jetzt in den Tabellen *broadLogAppSubRcp*, *excludeLogAppSubRcp* und *trackingLogAppSubRcp* gespeichert.

  >[!IMPORTANT]
  >
  >Aufgrund dieser Änderung wird empfohlen, das Zielgruppen-Mapping zu aktualisieren und die Nachricht erneut zu veröffentlichen, wenn Sie eine vorhandene profilbasierte Transaktions-Push-Benachrichtigung verwenden (die vor dem Upgrade auf Adobe Campaign 21.1 erstellt wurde). Eine detaillierte Anleitung dazu finden Sie [hier](../../channels/using/transactional-push-notifications.md#change-target-mapping). Die Verwendung des früheren Zielgruppen-Mappings **Profil – Echtzeitereignis** (*mapRtEventRcp*) kann zu längeren Versandvorbereitungszeiten und Performance-Einbußen führen.

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

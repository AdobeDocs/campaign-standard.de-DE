---
title: Versionshinweise 2022
description: Auf dieser Seite werden alle Versionen von Adobe Campaign Standard von 2022 aufgelistet.
feature: Overview
role: User
level: Beginner
exl-id: 8c722084-988d-47bd-98ad-9f5a422980a0
source-git-commit: e7c9c79a72b9f1ce36d0c60464b36be7d36a50a6
workflow-type: ht
source-wordcount: '1201'
ht-degree: 100%

---

# Versionshinweise 2022{#release-notes-2022}

## Version 22.3.2 {#feb-23}

### Sicherheits-Update{#rn-security2}

Diese Version umfasst die folgende Sicherheitsaktualisierung: Debian wurde auf v11.0 aktualisiert.

## Version 22.3 – Herbst/Winter 2022 {#sept-22}

### Sicherheits-Update{#rn-security}

Diese Version umfasst die folgende Sicherheitsaktualisierung: Apache Tomcat wurde von v7.0 auf v8.0 aktualisiert.

### Fehlerbehebungen{#rn-fixes}

* Fehlerkorrektur – Terminierte Berichte werden jetzt nicht mehr eine Stunde vor dem geplanten Zeitpunkt ausgelöst. (CAMP-51502)
* Fehlerkorrektur – Die Versandindikatoren im Versand-Dashboard stimmen jetzt mit den Versandlogs überein (nms:broadLogRcp). (CAMP-51127)
* Fehlerkorrektur – Die Erweiterung benutzerdefinierter Ressourcen mit dem ACS-Connector (Prime-Angebot) ist jetzt möglich. (CAMP-51033)
* Der Veröffentlichungsprozess für Antworten auf Datenschutzanfragen wurde verbessert, um Verzögerungen zu vermeiden. (CAMP-50613)

## Version 22.2 – Juni 2022 {#june-2022}

**Verbesserungen**

* **Adobe Notification Service** - Campaign wird mit dem Adobe Notification Service geliefert, der es Experience Cloud-Lösungen ermöglicht, Nutzer/innen in der gesamten Experience Cloud über Aktivitäten zu informieren, die für sie wichtig sind. Ab Version 22.2 wurde das Nutzererlebnis verbessert: Benachrichtigungen werden priorisiert und produkterzeugte Benachrichtigungen werden von Adobe-Statusmeldungen getrennt. Wenn sich die Benachrichtigung auf einen bestimmten Workflow bezieht, kannst du jetzt auch direkt aus der E-Mail oder der produktinternen Benachrichtigung auf den entsprechenden Workflow zugreifen.  Weiterführende Informationen zu Adobe Campaign-Benachrichtigungen finden Sie in Abschnitt [Benachrichtigungen in Adobe Campaign](../../administration/using/sending-internal-notifications.md).

<!--
* **Optimization in Workflow startup** - Adobe has added a new capability which can tune the number of workflows that start around the same time. This would help prevent CPU spikes that could have led to service interruptions or downtime. Adobe would enable it after 22.2 release. There is no further action item on customer regarding the same.
-->

* **Barrierefreiheit** – Adobe hat viele Fehlerbehebungen bei der Barrierefreiheit vorgenommen, um die Benutzerfreundlichkeit der Anwendung zu erhöhen. Diese Funktionen sind derzeit nur für einige frühzeitige Benutzende verfügbar und werden in zukünftigen Versionen allen Kunden und Kundinnen zur Verfügung stehen. Beispiele für Verbesserungen bei der Barrierefreiheit:

   * Sicherstellen, dass auf jedem Bildschirm eine sichtbare Fokusanzeige für fokussierbare Elemente vorhanden ist
   * Erstellen von Seitenmarkierungen für eine einfachere Navigation
   * Hinzufügen von Name, Rolle, Wert und Status für viele Steuerelemente
   * Beheben von Problemen mit der dynamischen Fokusreihenfolge auf Hauptbildschirmen


**Patches**

* Fehlerkorrektur: Der technische Workflow für die Rechnungsstellung funktioniert jetzt einwandfrei. (CAMP-51029)
* Fehlerkorrektur: Die fehlende Microsoft Edge-Browser-Kategorie wurde in Tracking-Berichten hinzugefügt. Sie wurde zuvor mit Microsoft Chrome-Öffnungen kategorisiert. (CAMP-51165)
* Fehlerkorrektur: Es wurde ein Problem mit DSGVO-Anfragen behoben, bei dem Daten aus untergeordneten Tabellen nicht gelöscht wurden. (CAMP-48276)
* Fehlerkorrektur: Die Sichtbarkeitsbedingung eines Fragments in einer Transaktionsnachrichtenvorlage wird jetzt in E-Mail-Designer gespeichert. (CAMP-50338)
* Fehlerkorrektur: Es wurde ein Fehler in Campaign-Berichten behoben, der dazu führte, dass der Datumsbereich nicht berücksichtigt wurde. (CAMP-50991)
* Fehlerkorrektur: Geplante E-Mails schlagen nun nicht mehr fehl. Zuvor konnte die Versandanalyse nicht gestartet werden, da der Versand noch den Status &quot;Erneuter Versuch steht aus&quot; aufwies. (CAMP-50302)
* Fehlerkorrektur: In E-Mail-Designer tritt jetzt kein Fehler mehr auf, wenn eine E-Mail mit einer Profilersetzung in der Vorschau angezeigt wird. (CAMP-49312)
* Fehlerkorrektur: Es wurde ein Problem mit einem leerem Wert in benutzerdefinierten Auflistungen behoben: Wenn Sie eine benutzerdefinierte Ressource mit einem Feld erstellen, das eine Textauflistung darstellt und nur einen Wert enthält, wird dieser Wert jetzt standardmäßig festgelegt, sodass Sie eine Abfrage für dieses Feld als einfache Anfrage erstellen können. (CAMP-50606)


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
* Sie können jetzt Ihren Versand überwachen und die Vorgangslogs über das neue Dropdown-Menü **Vorgangsverlauf** im Dashboard Ihrer Nachrichten verfolgen. [Weitere Informationen](../../sending/using/monitoring-a-delivery.md) (CAMP-49840)
* Die Stabilität und Datenbanksicherheit wurde durch Reduzierung von toten Tupeln verbessert. Diese treten auf, wenn im Laufe der Zeit eine große Anzahl von Nachrichten über alle Kanäle gesendet wird. (CAMP-49755, CAMP-49792, CAMP-49849)
* Im Mail Transfer Agent (MTA) von Campaign wurden Verbesserungen implementiert, um sicherzustellen, dass Datenbankverbindungen im Fall eines Datenbankabsturzes oder eines erneuten Starts automatisch aktualisiert werden. (CAMP-48063)
* Die neue Tracking-Option **Tracking-Pixel oben in der E-Mail verwenden** wurde zu den E-Mail-Eigenschaften hinzugefügt. Damit können Sie das Tracking-Pixel an den Anfang der E-Mail statt an das Ende verschieben. (CAMP-49672)

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
* Um verschiedene Probleme zu lösen, wurde der Wiederholungsmechanismus für Sendungen, einschließlich aus einer URL importierter Inhalte, verbessert. [Weitere Informationen](../../designing/using/using-existing-content.md#retrieving-content-from-a-url-automatically-at-preparation-time) (CAMP-48888)
* Fehlerkorrektur – jetzt tritt kein Fehler mehr auf, nachdem ein neuer Filter in einer benutzerdefinierten Ressource erstellt und als Abstimmschlüssel in einer Landingpage verwendet wurde. Wenn die benutzerdefinierte Ressource erneut veröffentlicht wurde, wurde der Filter aus der Liste der verfügbaren Abstimmschlüssel für die Landingpage entfernt. (CAMP-49516)
* Fehlerkorrektur – Auf Landingpages tritt jetzt kein Fehler mehr auf, wenn dynamische Bedingungen mit Kontrollkästchen verwendet werden. (CAMP-48604)
* Fehlerkorrektur – Es gibt jetzt kein Problem mehr in einer **Abfrage** Aktivität, wenn die Filterbedingung „Am oder vor Oktober“ verwendet wird. Bei der Arbeit in einer auf eine europäische Zeitzone festgelegten Instanz wurde als ausgewählter Monat für den Filter September anstelle Oktober angezeigt, da beim Konvertieren der Zeitzone ein Problem aufgetreten war. (CAMP-48602)
* Um die Zustellbarkeit zu optimieren, sendet Adobe Campaign jetzt E-Mails mit 7-Bit-Codierung anstelle von 8-Bit-Codierung. Dadurch wird verhindert, dass Zwischenrelais die DKIM-Signatur ungültig machen, was sich auf die Authentizität der Nachrichten auswirken könnte. (CAMP-49016)
* Die Leistung beim Duplizieren von Audiences wurde verbessert, um Probleme beim Arbeiten mit großen Audiences zu vermeiden. (CAMP-49639)
* Fehlerkorrektur – Benutzerdefinierte Filter zeigen jetzt die richtigen Ergebnisse an, wenn sie in einer **Abfrage**-Aktivität verwendet werden. (CAMP-49417)
* Fehlerkorrektur – bei der Verwendung eines Fragments in einem Versand, dessen Name ein Komma enthält, wird jetzt keine Fehlermeldung mehr angezeigt. Das Problem wurde behoben, und Kommas können jetzt in Fragmentnamen verwendet werden. (CAMP-49216)

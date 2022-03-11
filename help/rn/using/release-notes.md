---
title: Aktuelle Version
description: Auf dieser Seite finden Sie Informationen zum Inhalt der aktuellen Version von Campaign Standard.
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: 98aa27e4fb5eab9abbce5a9a9ba2c17d04424d70
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 97%

---


# Aktuelle Version{#latest-release}

![Control Panel](assets/do-not-localize/cp-icon.png) **Neue Control Panel-Versionen** mit Durchsätzen, Latenz und Workflow-Überwachung. [Weitere Infos](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html?lang=de){target=&quot;_blank&quot;}.

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
* Es wurde ein Problem behoben, das in einer **Abfrage**-Aktivität bei Verwendung der Filterbedingung &quot;In oder vor Oktober&quot; auftrat. Bei der Arbeit in einer auf eine europäische Zeitzone festgelegten Instanz wurde als ausgewählter Monat für den Filter September anstelle Oktober angezeigt, da beim Konvertieren der Zeitzone ein Problem aufgetreten war. (CAMP-48602)
* Um die Zustellbarkeit zu optimieren, sendet Adobe Campaign jetzt E-Mails mit 7-Bit-Codierung anstelle von 8-Bit-Codierung. Dadurch wird verhindert, dass Zwischenrelais die DKIM-Signatur ungültig machen, was sich auf die Authentizität der Nachrichten auswirken könnte. (CAMP-49016)
* Die Leistung beim Duplizieren von Audiences wurde verbessert, um Probleme beim Arbeiten mit großen Audiences zu vermeiden. (CAMP-49639)
* Fehlerkorrektur – Benutzerdefinierte Filter zeigen jetzt die richtigen Ergebnisse an, wenn sie in einer **Abfrage**-Aktivität verwendet werden. (CAMP-49417)
* Fehlerkorrektur – bei der Verwendung eines Fragments in einem Versand, dessen Name ein Komma enthält, wird jetzt keine Fehlermeldung mehr angezeigt. Das Problem wurde behoben. Kommas können jetzt in Fragmentnamen verwendet werden. (CAMP-49216)


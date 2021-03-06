---
title: Vorzeitige Versionshinweise
description: Vorzeitige Versionshinweise
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: 9ab2e49203315e4c31a1bc268cd17bd0351a5349
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 86%

---

# Vorzeitige Versionshinweise {#new-release}

Auf dieser Seite werden neue Funktionen, Verbesserungen und Fehlerbehebungen beschrieben, die in der nächsten Campaign Standard-Version enthalten sind.

>[!CAUTION]
>
> Dieser Inhalt kann ohne vorherige Ankündigung bis zum Aktualisierungsdatum der Staging-Umgebung geändert werden. Weitere Informationen finden Sie auf der [Seite mit der Versionsplanung](../../rn/using/release-planning.md).

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
<p>Nach der Aktualisierung von Apache log4j v2.17.0 im Dezember 2021, um sicherzustellen, dass unsere Kunden nicht von möglichen unbeabsichtigten Auswirkungen der Einführung weiterer Änderungen am System außerhalb unseres normalen Veröffentlichungszeitplans betroffen sind, haben wir die Aktualisierung intern vorgenommen und bereiten sie mit dieser Version auf die Bereitstellung vor.</p>
</td> 
</tr> 
</tbody> 
</table>

**Sicherheitskorrekturen**

* Neuer URL-Signaturmechanismus für Tracking in dieser Version. Der frühere Mechanismus wurde deaktiviert, um ein Problem zu vermeiden, das dazu führte, dass einige gültige, signierte Tracking-Links fälschlicherweise blockiert wurden, nachdem sie durch Sicherheits-Tools von Drittanbietern geändert worden waren. (CAMP-48983)
* Erhöhen Sie die Sicherheit für den Zugriff auf Anwendungs- und Server-Konfigurationsdateien: Die Sicherheit der APIs für den Zugriff auf JavaScript-Dateien ist jetzt auf Sandbox-Ordner beschränkt. (CAMP-49411)

**Verbesserungen**

* Die Verarbeitung von Berichtsdaten wurde verbessert, um zu vermeiden, dass das System überlastet wird. (CAMP-47578)
* Nach dem Versand Ihrer In-App-Nachrichten können Sie jetzt Ihren Versand deaktivieren. Auf diese Weise können Sie Ihren Versand löschen, ohne Berichtsdaten zu verlieren. (CAMP-48469)
* Um Probleme zu vermeiden, können Benutzer für eine benutzerdefinierte Tabellenspalte nicht mehr denselben Namen wie für den automatischen Primärschlüssel in der Datenbank verwenden. `"<dataType><resourceName>Id"`. (CAMP-49358)

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
* Um verschiedene Probleme zu lösen, wurde der Wiederholungsmechanismus für Sendungen, einschließlich aus einer URL importierter Inhalte, verbessert. (CAMP-48888)
* Fehlerkorrektur – jetzt tritt kein Fehler mehr auf, nachdem ein neuer Filter in einer benutzerdefinierten Ressource erstellt und als Abstimmschlüssel in einer Landingpage verwendet wurde. Wenn die benutzerdefinierte Ressource erneut veröffentlicht wurde, wurde der Filter aus der Liste der verfügbaren Abstimmschlüssel für die Landingpage entfernt. (CAMP-49516)
* Fehlerkorrektur – Auf Landingpages tritt jetzt kein Fehler mehr auf, wenn dynamische Bedingungen mit Kontrollkästchen verwendet werden. (CAMP-48604)
* Es wurde ein Problem behoben, das in einer **Abfrage**-Aktivität bei Verwendung der Filterbedingung &quot;In oder vor Oktober&quot; auftrat. Bei der Arbeit in einer auf eine europäische Zeitzone festgelegten Instanz wurde als ausgewählter Monat für den Filter September anstelle Oktober angezeigt, da beim Konvertieren der Zeitzone ein Problem aufgetreten war. (CAMP-48602)
* Um die Zustellbarkeit zu optimieren, werden E-Mails jetzt mit 7-Bit-Kodierung statt mit 8-Bit-Kodierung gesendet. Dadurch wird verhindert, dass Relais die DKIM-Signatur ungültig machen, wenn sie von 8 auf 7 Bit konvertieren. (CAMP-49016)
* Die Leistung beim Duplizieren von Audiences wurde verbessert, um Probleme beim Arbeiten mit großen Audiences zu vermeiden. (CAMP-49639)
* Fehlerkorrektur – Benutzerdefinierte Filter zeigen jetzt die richtigen Ergebnisse an, wenn sie in einer **Abfrage**-Aktivität verwendet werden. (CAMP-49417)
* Fehlerkorrektur – bei der Verwendung eines Fragments in einem Versand, dessen Name ein Komma enthält, wird jetzt keine Fehlermeldung mehr angezeigt. Das Problem wurde behoben. Kommas können jetzt in Fragmentnamen verwendet werden. (CAMP-49216)
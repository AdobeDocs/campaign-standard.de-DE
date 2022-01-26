---
title: Vorzeitige Versionshinweise
description: Vorzeitige Versionshinweise
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: 5435e1dbfbe08399c488322320ac5bb8e681a79d
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 10%

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
<p>Apache log4j hat die gemeldeten Sicherheitslücken in Apache log4j v2.17.1 behoben. Adobe Campaign Standard verwendet Apache log4j und in dieser Version enthält dieses neueste Apache log4j v2.17.1 </p>
</td> 
</tr> 
</tbody> 
</table>

**Sicherheitskorrekturen**

* Neuer URL-Signaturmechanismus für Tracking in dieser Version. Der vorherige Mechanismus war deaktiviert worden, um zu verhindern, dass einige gültige, signierte Tracking-Links nach der Änderung durch Sicherheitswerkzeuge von Drittanbietern fälschlicherweise blockiert wurden. (CAMP-48983)

**Verbesserungen**

* Die Verarbeitung von Berichtsdaten wurde verbessert, um zu vermeiden, dass das System überlastet wird. (CAMP-47578)
* Nach dem Versand Ihrer In-App-Nachrichten können Sie jetzt Ihren Versand deaktivieren. Auf diese Weise können Sie Ihren Versand löschen, ohne Berichtsdaten zu verlieren. (CAMP-48469)
* Um Probleme zu vermeiden, können Benutzer für eine benutzerdefinierte Tabellenspalte nicht mehr denselben Namen wie für den automatischen Primären Schlüssel in der Datenbank verwenden. `"<dataType><resourceName>Id"`. (CAMP-49358)
* Sie können jetzt Ihren Versand überwachen und die Auftragsprotokolle mit dem neuen **Auftragsverlauf** aus dem Dashboard Ihrer Nachrichten. (CAMP-49840)
* Verbesserte Stabilität und Datenbanksicherheit durch Reduzierung von toten Schläuchen, wenn im Laufe der Zeit eine große Anzahl von Nachrichten über alle Kanäle gesendet wird. (CAMP-49755, CAMP-49792, CAMP-49849)
* Um sicherzustellen, dass Datenbankverbindungen im Fall eines Datenbankabsturzes oder eines erneuten Starts automatisch aktualisiert werden, wurden im Campaign Mail Transfer Agent (MTA) Verbesserungen implementiert. (CAMP-48063)


**Patches**

* Es wurde ein Problem mit der **Bericht jetzt senden** Option in dynamischen Berichten: Die PDF-Generierungsaufträge schlugen mit Sendungen einschließlich Mehrfachvarianten fehl. (CAMP-49120)
* Es wurde ein Problem behoben, durch das Benutzer Adobe Experience Manager (AEM)-Inhalte nicht in ihren Adobe Campaign Standard-Sendungen aktualisieren oder deren Verknüpfung aufheben konnten, wenn duplizierte Inhalte in AEM gleichen Schlüssel (cq:uuid) freigegeben wurden. (CAMP-49161)
* Fehlerkorrektur - der Zugriff auf eine Instanz, in der Seiten nicht geladen werden, Sendungen nicht geöffnet werden konnten oder ausstehende Änderungen nicht gespeichert werden konnten, funktioniert nun fehlerfrei. (CAMP-50195)
* Fehlerkorrektur - Versandwarnungsbedingungen können jetzt geöffnet werden, wenn das Feld **Versandfilter** Dieses Kriterium wurde nicht erfüllt. (CAMP-49093)
* Fehlerkorrektur - Beim Bearbeiten der **Sekundär** in In-App-Sendungen, die die Berücksichtigung von Änderungen verhinderten. (CAMP-50250)
* Es wurde ein Fehler in japanischen Instanzen behoben, durch den Benutzer mehrmals am Tag als **Ausführungsfrequenz** im **Planung** Aktivität. (CAMP-50247)
* Fehlerkorrektur - Bei der Arbeit mit einer japanischen Benutzeroberfläche wird jetzt bei der Auswahl einer Uhrzeit in der Aktivität Planung keine Fehlermeldung mehr angezeigt. (CAMP-49289)
* Fehlerkorrektur - in Push-Benachrichtigungsberichten werden verworfene Push-Benachrichtigungen jetzt nicht mehr als **Öffnen** anstelle von **Impression**. (CAMP-45980)
* Fehlerkorrektur - Beim Öffnen eines Berichts treten jetzt keine Fehler mehr auf. (CAMP-49222)
* Fehlerkorrektur - Die E-Mail-Vorbereitung schlägt jetzt nicht mehr fehl, nachdem ein Link zu AEM Inhalt gelöscht wurde. (CAMP-49877)
* Um verschiedene Probleme zu lösen, wurde der Wiederholungsmechanismus für Sendungen, einschließlich aus einer URL importierter Inhalte, verbessert. (CAMP-48888)
* Fehlerkorrektur - jetzt tritt kein Fehler mehr auf, nachdem ein neuer Filter in einer benutzerdefinierten Ressource erstellt und als Abstimmschlüssel in einer Landingpage verwendet wurde. Wenn die benutzerdefinierte Ressource erneut publiziert wurde, wurde der Filter aus der Liste der verfügbaren Abstimmschlüssel für die Landingpage entfernt. (CAMP-49516)
* Fehlerkorrektur - Auf Landingpages tritt jetzt kein Fehler mehr auf, wenn dynamische Bedingungen mit Kontrollkästchen verwendet werden. (CAMP-48604)
* Es wurde ein Problem behoben, das in einem **Abfrage** -Aktivität bei Verwendung der Filterbedingung &quot;Ein oder vor Oktober&quot;. Bei der Arbeit von einer Instanz, die auf eine europäische Zeitzone festgelegt ist, wurde im ausgewählten Monat für den Filter September anstelle Oktober angezeigt, da beim Konvertieren der Zeitzone ein Problem aufgetreten ist. (CAMP-48602)
* Um die Zustellbarkeit zu optimieren, sendet Adobe Campaign jetzt E-Mails mit 7-Bit-Kodierung anstelle von 8-Bit-Kodierung. Dadurch wird verhindert, dass Zwischen-Relais die DKIM-Signatur ungültig machen, was sich auf die Authentizität der Nachrichten auswirken könnte. (CAMP-49016)
* Die Leistung beim Duplizieren von Zielgruppen wurde verbessert, um Probleme beim Arbeiten mit großen Zielgruppen zu vermeiden. (CAMP-49639)
* Fehlerkorrektur - Benutzerdefinierte Filter zeigen jetzt die richtigen Ergebnisse an, wenn sie in einer **Abfrage** Aktivität. (CAMP-49417)
* Fehlerkorrektur - bei der Verwendung eines Fragments in einem Versand mit einem Komma im Namen wird keine Fehlermeldung mehr angezeigt. Das Problem wurde behoben. Kommas können jetzt in Fragmentnamen verwendet werden. (CAMP-49216)
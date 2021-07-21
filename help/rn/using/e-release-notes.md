---
solution: Campaign Standard
product: campaign
title: Frühzeitige Versionshinweise
description: Frühzeitige Versionshinweise
feature: Übersicht
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: aeeb6b4984b3bdd974960e8c6403876fdfedd886
workflow-type: ht
source-wordcount: '1032'
ht-degree: 100%

---

# Frühere Versionshinweise {#new-release}

Auf dieser Seite werden neue Funktionen, Verbesserungen und Fehlerbehebungen beschrieben, die in der nächsten Campaign Standard-Version enthalten sind.

>[!CAUTION]
>
> Dieser Inhalt kann ohne vorherige Ankündigung bis zum Aktualisierungsdatum der Staging-Umgebung geändert werden. Weitere Informationen finden Sie auf der [Seite mit der Versionsplanung](../../rn/using/release-planning.md).


## Version 21.2 – Juni 2021 {#release-21-2---june-2021}

**Verbesserungen**

* Beim Erstellen einer Landingpage können Sie jetzt eine obligatorische Checkbox hinzufügen, die die Profile vor dem Absenden des Formulars markieren müssen.

* Für die Integration von Triggers wurde die Fehlermeldung verbessert, die angezeigt wird, wenn in der Trigger-Payload keine Abstimmdaten eingehen: &quot;In der Payload fehlen Alias-Daten&quot;.

* Die Leistung beim Abrufen von Push-Benachrichtigungen aus der Warteschlange wurde verbessert.

**Sonstige Änderungen**

* Der URL-Signaturmechanismus für Tracking-Links wurde deaktiviert, um zu verhindern, dass einige gültige, signierte Tracking-Links nach der Änderung durch Sicherheits-Tools von Drittanbietern fälschlicherweise blockiert werden.

* In Sendungen mit mehreren Varianten können Benutzer keine Sprachkopien mehr erstellen, wenn die Standardvariante gelöscht wurde. Bei der Erstellung einer Sprachkopie wird nun eine Meldung angezeigt. (CAMP-48235)

* Der zweistufige Prozess zum Löschen von Profilen (eingestellt ab Campaign-Version 19.4) ist jetzt standardmäßig deaktiviert. Zuvor musste der Prozess vor der Verwendung von Privacy Core Service manuell über die Campaign-Benutzeroberfläche deaktiviert werden. Andernfalls verblieben Löschanfragen im Status &quot;Ausstehend&quot;, ohne abgeschlossen zu werden.

* Die neue Aggregatfunktion &quot;StringAgg&quot; wurde eingeführt, um die Werte einer Spalte vom Typ Zeichenfolge zu verketten. (CAMP-47077)

* In dynamischen Berichten wurde das Segment **Testversand ausschließen** entfernt. (CAMP-46161)

* Es wurde eine neue Warnmeldung hinzugefügt, die den Benutzer darüber informiert, wenn ein iOS-Zertifikat ohne den Wert &quot;platformPrincipal&quot; in das Campaign-Programm hochgeladen wird.

* Die maximale Größe einer E-Mail ist jetzt standardmäßig mit 100 MB festgelegt. Mit dieser Begrenzung können Fehler verhindert werden, durch die die Größe einer E-Mail unbegrenzt erhöht werden kann, was zu einem Systemabsturz führen könnte. (CAMP-47445)

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

* Fehlerkorrektur – Trackinglogs sind jetzt in allen Instanzen vorhanden. Es wurde ein neuer technischer Workflow (**trackingLogRecovery**) hinzugefügt, um die fehlenden Trackinglogs bereitzustellen. Dieser Workflow sollte nur intern von Adobe verwendet werden.

* Fehlerkorrektur – In dynamischen Berichten werden Versanddaten jetzt angezeigt. Berichte wurden auf 0 gesetzt. (CAMP-47480)

* Fehlerkorrektur – Der Server-JavaScript-HTTP-Client kann sich jetzt mit einer externen URL verbinden.

* Fehlerkorrektur – Wenn der interne Name des Workflows geändert wird, wird die Aktivität **Inkrementelle Abfrage** nicht mehr zurückgesetzt. Dies trat auf, wenn ein Datumsfeld als inkrementeller Modus verwendet wurde. (CAMP-47674)

* Fehlerkorrektur – Wenn eine mehrsprachige E-Mail mit der Adobe Experience Manager-Integration erstellt wird, wird jetzt die Vorschau-Miniaturansicht in der Versandzusammenfassung angezeigt. Zuvor trat ein Problem, wenn die Schaltfläche **Erstellung von Sprachkopien** verwendet wurde, um die E-Mail-Varianten zu erstellen. (CAMP-47810)

* Fehlerkorrektur – Benutzer können jetzt vom untergeordneten E-Mail- oder SMS-Versand aus auf den übergeordneten Versand zugreifen. (CAMP-47986)

* Fehlerkorrektur – Beim Senden von Transaktionsnachrichten über die REST-API mit einem fehlenden benutzerdefinierten Ereignis werden CPU und Speicher nicht mehr übermäßig belastet. (CAMP-47147)

* Fehlerkorrektur – Das Senden von Echtzeitnachrichten mit der Transaktionsnachricht-API funktioniert jetzt reibungslos.

* Fehlerkorrektur – Nach Verwendung der Option **Bericht planmäßig senden** werden Berichte jetzt in jedem Fall empfangen. (CAMP-48583)

* Fehlerkorrektur – Nach Verwendung der Option **Bericht jetzt senden** werden Berichte jetzt vollständig und alle Daten enthaltend empfangen. (CAMP-48583)

* Fehlerkorrektur – Bei der Option **Bericht planmäßig senden** im Dynamics-Bericht wurden ein Fehler behoben, durch den der integrierte Workflow **Sofortige Berichtfreigabe** (reportSendingNow) keine Berichte erzeugen konnte. (CAMP-47786)

* Fehlerkorrektur – Beim Hochladen eines Bildes mit Email Designer behalten Bilder ihre ursprünglichen Abmessungen. (CAMP-47017)

* Fehlerkorrektur – Jetzt werden alle verfügbaren Experience Manager-Vorlagen angezeigt, wenn ein Versand erstellt wird. (CAMP-48132)

* Fehlerkorrektur – Der Campaign-Link auf der Zusammenfassungsseite eines durchgeführten Versands leitet die Benutzer jetzt zuverlässig zu der zugehörigen Kampagne weiter. (CAMP-48012)

* Fehlerkorrektur – In Email Designer funktioniert jetzt die Integration von Asset Core Service, wenn ein Asset ausgewählt wird. (CAMP-47446)

* Fehlerkorrektur – Journey Orchestration-Sendungen werden jetzt nicht mehr blockiert. Zuvor unterstützte Campaign keine Zeitstempel mit einem exakten Wert (d. h. endend auf 00), die von Ereignissen in Journey Orchestration gesendet wurden.

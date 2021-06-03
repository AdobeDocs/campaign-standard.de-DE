---
solution: Campaign Standard
product: campaign
title: Frühzeitige Versionshinweise
description: Frühzeitige Versionshinweise
feature: Übersicht
role: Business Practitioner
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: c98aa913f4004d49a897ea71e39cbfe6b3dd53c1
workflow-type: tm+mt
source-wordcount: '1008'
ht-degree: 7%

---

# Frühzeitige Versionshinweise {#new-release}

Auf dieser Seite werden neue Funktionen, Verbesserungen und Fehlerbehebungen beschrieben, die in der nächsten Campaign Standard-Version enthalten sind.

>[!CAUTION]
>
> Dieser Inhalt kann ohne vorherige Ankündigung bis zum Aktualisierungsdatum der Staging-Umgebung geändert werden. Weitere Informationen finden Sie auf der [Seite mit der Versionsplanung](../../rn/using/release-planning.md).


## Version 21.2 - Juni 2021            {#release-21-2---june-2021}

**Verbesserungen**

* Beim Erstellen einer Landingpage können Sie jetzt ein obligatorisches Kontrollkästchen hinzufügen, das Profile vor dem Senden des Formulars auswählen müssen.

* Für die Trigger-Integration wurde die Fehlermeldung, die angezeigt wird, wenn in der Trigger-Payload keine Abstimmdaten eingehen, verbessert: &quot;Alias data missing in payload&quot;.

* Die Leistung beim Abrufen von Push-Benachrichtigungen aus der Warteschlange wurde verbessert.

**Sonstige Änderungen**

* Der URL-Signaturmechanismus für Tracking-Links wurde deaktiviert, um zu verhindern, dass einige gültige, signierte Tracking-Links nach der Änderung durch Sicherheitswerkzeuge von Drittanbietern fälschlicherweise blockiert wurden.

* In Sendungen mit mehreren Varianten können Benutzer keine Sprachkopien mehr erstellen, wenn die Standardvariante gelöscht wurde. Bei der Erstellung einer Sprachkopie wird nun eine Meldung angezeigt. (CAMP-48235)

* Der zweistufige Prozess zum Löschen von Profilen (veraltet ab Campaign-Version 19.4) ist jetzt standardmäßig deaktiviert. Zuvor musste sie vor der Verwendung des Privacy Core Service manuell über die Campaign-Benutzeroberfläche deaktiviert werden. Andernfalls verbleiben Löschanfragen im Status &quot;Ausstehend&quot;, ohne abgeschlossen zu sein.

* Eine neue Aggregatfunktion &quot;StringAgg&quot; wurde eingeführt, um die Werte einer Spalte vom Typ Zeichenfolge zu verketten. (CAMP-47077)

* In dynamischen Berichten wurde das Segment **Testversand ausschließen** entfernt. (CAMP-46161)

* Es wurde eine neue Warnmeldung hinzugefügt, die den Benutzer darüber informiert, wenn ein iOS-Zertifikat ohne den Wert &quot;platformPrincipal&quot;in die Campaign-Anwendung hochgeladen wird.

* Die maximale Größe einer E-Mail ist jetzt standardmäßig auf 100 MB festgelegt. Mit dieser Begrenzung können Fehler verhindert werden, die die Größe einer E-Mail auf unbestimmte Zeit erhöhen könnten und zu einem Systemabsturz führen können. (CAMP-47445)

* Die Asset Core Service-Integration mit Email Designer kann jetzt von Standardbenutzern verwendet werden.

* Es wurde eine neue Meldung hinzugefügt, die bestätigt, dass die Migration von einer v4-Push-Anwendung zu einer v5-Push-Anwendung erfolgreich war.

**Korrekturen**

* Fehlerkorrektur - Die Ablauffunktion für die Stapelverarbeitungsprotokolltabelle (**xtkjoblog**) wird jetzt angewendet. Dadurch konnte die Tabelle nicht korrekt bereinigt werden.

* Fehlerkorrektur - Die Reihenfolge von Filtern in einer **Segmentierung** -Workflow-Aktivität kann jetzt geändert werden. (CAMP-48357)

* Fehlerkorrektur - Es wurde eine Regression von 20.4 behoben, die dazu führte, dass Sendungen mit einem Nullwertfehler fehlschlugen. (CAMP-48591)

* Es wurde ein Problem behoben, das das Senden eines Berichts über das Menü **Freigeben** > **Bericht jetzt senden** oder **Bericht planmäßig senden** verhindert hat. (CAMP-47798)

* Fehlerkorrektur - Es wurde eine Regression behoben, die aufgrund der Filterung von Tracking-Ereignissen, die von Gmail-Konten empfangen wurden, zu falschen Öffnungsraten für Gmail führen konnte. (CAMP-46504)

* Verschiedene Probleme wurden behoben, die zu Datendiskrepanzen zwischen Berichten in Adobe Campaign Standard und Berichten in Adobe Analytics führten. (CAMP-47671, CAMP-47296)

* Fehlerkorrektur - jetzt können Sie auf die Versandlogs zugreifen, nachdem die Vorbereitung fehlgeschlagen ist. (CAMP-48296)

* Fehlerkorrektur - jetzt wird keine Fehlermeldung mehr angezeigt, wenn ein benutzerdefinierter Bericht bearbeitet, gelöscht oder gesendet wird. (CAMP-47789, CAMP-47798)

* Es wurde ein Fehler behoben, der dazu führte, dass die API-Aufrufe beim Erstellen einer neuen benutzerdefinierten Ressource und Aktivieren der Option **Nicht synchronisieren** fehlschlugen. (CAMP-48014)

* Es wurde ein Problem behoben, bei dem benutzerdefinierte Ressourcen mit aktivierter Option **Nicht synchronisieren** auf ein Schema verweisen konnten, das neu entworfen oder gelöscht wurde. Dieses Problem verursachte einen Fehler beim Veröffentlichen der benutzerdefinierten Ressourcen.

* Fehlerkorrektur - Es wurde ein SMS-Abmeldefehler bei der Verwendung mehrerer Kurzwahlnummern in demselben externen Konto behoben.

* Fehlerkorrektur - Nach der Publikation der Datenbank können Sie jetzt auf eine neue Versandwarnungsbedingung (&quot;Die Ressource, auf die Sie zugreifen möchten, ist nicht erreichbar&quot;) zugreifen. (CAMP-48221)

* Es wurde ein Problem behoben, bei dem Trackinglogs in einigen Fällen fehlten. Es wurde ein neuer technischer Workflow hinzugefügt (**trackingLogRecovery**), um diese verlorenen Trackinglogs wiederherzustellen. Dieser Workflow sollte nur von der internen Adobe verwendet werden.

* Fehlerkorrektur - In dynamischen Berichten werden jetzt keine Versanddaten mehr angezeigt. Berichte wurden auf 0 gesetzt. (CAMP-47480)

* Fehlerkorrektur - Der JavaScript-HTTP-Client des Servers kann jetzt eine Verbindung zu einer externen URL herstellen.

* Fehlerkorrektur - Die Aktivität **Inkrementelle Abfrage** wird jetzt nicht mehr zurückgesetzt, nachdem der interne Name des Workflows geändert wurde. Dies trat auf, wenn ein Datumsfeld als inkrementeller Modus verwendet wurde. (CAMP-47674)

* Fehlerkorrektur - Die Miniaturansicht der Vorschau wird jetzt in der Versandzusammenfassung angezeigt, wenn eine mehrsprachige E-Mail mit der Adobe Experience Manager-Integration erstellt wird. Dieses Problem trat auf, wenn die Schaltfläche **Erstellung einer Sprachkopie** verwendet wurde, um die E-Mail-Varianten zu erstellen. (CAMP-47810)

* Fehlerkorrektur - Benutzer können jetzt über den untergeordneten E-Mail- oder SMS-Versand auf den übergeordneten Versand zugreifen. (CAMP-47986)

* Fehlerkorrektur - Beim Senden von Transaktionsnachrichten über die REST-API mit fehlendem benutzerdefiniertem Ereignis kommt es nicht mehr zu übermäßiger CPU- und Speicherbelegung. (CAMP-47147)

* Fehlerkorrektur - in der Transaktionsnachrichten-API wird der Versand von Echtzeit-Nachrichten jetzt nicht mehr verhindert.

* Es wurde ein Problem behoben, bei dem Berichte nach Verwendung der Option **Bericht nach Zeitplan senden** nicht empfangen wurden. (CAMP-48583)

* Es wurde ein Problem behoben, bei dem Berichte, die nach Verwendung der Option **Bericht jetzt senden** empfangen wurden, unvollständig waren und Daten fehlten. (CAMP-48583)

* Es wurde ein Problem mit der Option **Bericht planmäßig senden** im Dynamics-Bericht behoben, bei dem der integrierte Workflow **Instant Report Sharing** (reportSendingNow) keine Berichte generiert hat. (CAMP-47786)

* Fehlerkorrektur - In Email Designer werden die Bildabmessungen beim Hochladen eines Bildes jetzt nicht mehr eingeschränkt. (CAMP-47017)

* Fehlerkorrektur - jetzt werden alle verfügbaren Experience Manager-Vorlagen angezeigt, wenn ein Versand erstellt wird. (CAMP-48132)

* Fehlerkorrektur - der Kampagnen-Link auf der Zusammenfassungsseite eines gesendeten Versands leitet Benutzer nun zur entsprechenden Kampagne weiter. (CAMP-48012)

* Es wurde ein Problem in Email Designer behoben, bei dem die Asset-Core-Service-Integration beim Versuch, ein Asset auszuwählen, weiterhin fehlschlug. (CAMP-47446)

* Fehlerkorrektur - Es wurde ein Fehler behoben, der manche Sendungen von Journey Orchestrationen blockiert hat, da Campaign keine Zeitstempel mit einem exakten Wert (d. h. mit 00 enden) unterstützt, die von Ereignissen aus Journey Orchestration gesendet werden.

* Der technische Workflow updateDeliveryIndicators wurde optimiert. Versandkennungen mit demselben Broadlog-/Trackinglog-Schema werden nun gruppiert. Dadurch wird die Anzahl der Abfragen begrenzt und die Leistung verbessert.

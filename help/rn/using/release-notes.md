---
solution: Campaign Standard
product: campaign
title: Aktuelle Version
description: Auf dieser Seite finden Sie Informationen zum Inhalt der aktuellen Version von Campaign Standard.
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
feature: Übersicht
role: Business Practitioner
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: 847cc928c2e8ae9c9658c238fb3c8365d54af495
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 6%

---

# Aktuelle Version{#latest-release}

## Version 21.2 - Juni 2021            {#release-21-2---june-2021}

Nachfolgend finden Sie die neuen Funktionen, Verbesserungen und Fehlerbehebungen der nächsten Campaign Standard-Version.	Die in dieser Campaign Standard-Version enthaltenen neuen Funktionen, Verbesserungen und Fehlerbehebungen sind unten aufgeführt.

**Verbesserungen**

* Beim Erstellen einer Landingpage können Sie jetzt ein obligatorisches Kontrollkästchen hinzufügen, das Profile vor dem Senden des Formulars auswählen müssen. Weitere Informationen finden Sie im [entsprechenden Handbuch](../../channels/using/managing-landing-page-form-data.md#agreement-checkbox).

* Für die Trigger-Integration wurde die Fehlermeldung, die angezeigt wird, wenn in der Trigger-Payload keine Abstimmdaten eingehen, verbessert: &quot;Alias data missing in payload&quot;.

* Die Leistung beim Abrufen von Push-Benachrichtigungen aus der Warteschlange wurde verbessert.

**Sonstige Änderungen**

* Der URL-Signaturmechanismus für Tracking-Links wurde deaktiviert, um zu verhindern, dass einige gültige, signierte Tracking-Links nach der Änderung durch Sicherheitswerkzeuge von Drittanbietern fälschlicherweise blockiert wurden.

* In Sendungen mit mehreren Varianten können Benutzer keine Sprachkopien mehr erstellen, wenn die Standardvariante gelöscht wurde. Bei der Erstellung einer Sprachkopie wird nun eine Meldung angezeigt. (CAMP-48235)

* Der zweistufige Prozess zum Löschen von Profilen (veraltet ab Campaign-Version 19.4) ist jetzt standardmäßig deaktiviert. Zuvor musste sie vor der Verwendung des Privacy Core Service manuell über die Campaign-Benutzeroberfläche deaktiviert werden. Andernfalls verbleiben Löschanfragen im Status &quot;Ausstehend&quot;, ohne abgeschlossen zu sein.

* Eine neue Aggregatfunktion &quot;StringAgg&quot; wurde eingeführt, um die Werte einer Spalte vom Typ Zeichenfolge zu verketten. (CAMP-47077) [Mehr dazu](../../automating/using/list-of-functions.md#aggregates)

* In dynamischen Berichten wurde das Segment **Testversand ausschließen** entfernt. (CAMP-46161)

* Es wurde eine neue Warnmeldung hinzugefügt, die den Benutzer darüber informiert, wenn ein iOS-Zertifikat ohne den Wert &quot;platformPrincipal&quot;in die Campaign-Anwendung hochgeladen wird.

* Die maximale Größe einer E-Mail ist jetzt standardmäßig auf 100 MB festgelegt. Mit dieser Begrenzung können Fehler verhindert werden, die die Größe einer E-Mail auf unbestimmte Zeit erhöhen könnten und zu einem Systemabsturz führen können. (CAMP-47445) [Mehr dazu](../../sending/using/design-and-personalize.md#email-size)

* Die Asset Core Service-Integration mit Email Designer kann jetzt von Standardbenutzern verwendet werden.

* Es wurde eine neue Meldung hinzugefügt, die bestätigt, dass die Migration von einer v4-Push-Anwendung zu einer v5-Push-Anwendung erfolgreich war.

* Während der Erstellung von JSONWeb-Token zur Authentifizierung bei der Campaign Standard-API werden die Produktprofile jetzt **als** eingestuft. Das bedeutet, dass die der Sicherheitsgruppe zugewiesenen Organisationseinheiten und Rollen (die dem Produktprofil in Adobe I/O entsprechen) auf das für Campaign Standard Rest-API-Aufrufe erforderliche IMS-technische Konto angewendet werden. (CAMP-47479)

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

* Fehlerkorrektur - Trackinglogs fehlen jetzt in einigen Campaign-Instanzen in dynamischen Berichten. Es wurde ein neuer [technischer Workflow](../../administration/using/technical-workflows.md) hinzugefügt, um diese Trackinglogs wiederherzustellen. (CAMP-47885)

* Fehlerkorrektur - In dynamischen Berichten werden jetzt keine Versanddaten mehr angezeigt. Berichte wurden auf 0 gesetzt. (CAMP-47480)

* Fehlerkorrektur - Der JavaScript-HTTP-Client des Servers kann jetzt eine Verbindung zu einer externen URL herstellen.

* Fehlerkorrektur - Die Aktivität **Inkrementelle Abfrage** wird jetzt nicht mehr zurückgesetzt, nachdem der interne Name des Workflows geändert wurde. Dies trat auf, wenn ein Datumsfeld als inkrementeller Modus verwendet wurde. (CAMP-47674)

* Fehlerkorrektur - Die Miniaturansicht der Vorschau wird jetzt in der Versandzusammenfassung angezeigt, wenn eine mehrsprachige E-Mail mit der Adobe Experience Manager-Integration erstellt wird. Dieses Problem trat auf, wenn die Schaltfläche **Erstellung einer Sprachkopie** verwendet wurde, um die E-Mail-Varianten zu erstellen. (CAMP-47810)

* Fehlerkorrektur - Benutzer können jetzt über den untergeordneten E-Mail- oder SMS-Versand auf den übergeordneten Versand zugreifen. (CAMP-47986)

* Fehlerkorrektur - Beim Senden von Transaktionsnachrichten über die REST-API mit fehlendem benutzerdefiniertem Ereignis kommt es nicht mehr zu übermäßiger CPU- und Speicherbelegung. (CAMP-47147)

* Fehlerkorrektur - in der Transaktionsnachrichten-API wird der Versand von Echtzeit-Nachrichten jetzt nicht mehr verhindert.

* Es wurde ein Problem behoben, bei dem Berichte nach Verwendung der Option **Bericht nach Zeitplan senden** nicht empfangen wurden. (CAMP-48583, CAMP-47786)

* Es wurde ein Problem behoben, bei dem Berichte, die nach Verwendung der Option **Bericht jetzt senden** empfangen wurden, unvollständig waren und Daten fehlten. (CAMP-48583)

* Fehlerkorrektur - In Email Designer werden die Bildabmessungen beim Hochladen eines Bildes jetzt nicht mehr eingeschränkt. (CAMP-47017)

* Fehlerkorrektur - jetzt werden alle verfügbaren Experience Manager-Vorlagen angezeigt, wenn ein Versand erstellt wird. (CAMP-48132)

* Fehlerkorrektur - der Kampagnen-Link auf der Zusammenfassungsseite eines gesendeten Versands leitet Benutzer nun zur entsprechenden Kampagne weiter. (CAMP-48012)

* Es wurde ein Problem in Email Designer behoben, bei dem die Asset-Core-Service-Integration beim Versuch, ein Asset auszuwählen, weiterhin fehlschlug. (CAMP-47446)

* Fehlerkorrektur - Es wurde ein Fehler behoben, der manche Sendungen von Journey Orchestrationen blockiert hat, da Campaign keine Zeitstempel mit einem exakten Wert (d. h. mit 00 enden) unterstützt, die von Ereignissen aus Journey Orchestration gesendet werden.

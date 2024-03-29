---
title: Versionshinweise 2023
description: Auf dieser Seite werden alle Versionen von Adobe Campaign Standard von 2023 aufgelistet.
feature: Overview
role: User
level: Beginner
exl-id: 5817c4d2-4788-4695-bf9a-ec04cc042190
source-git-commit: 30e96494dd7fa3313601e48deeec8ef98dcdce85
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 100%

---

# Versionshinweise 2023 {#release-notes-2023}

## Version 23.2 – Version Herbst/Winter 2023 {#fall-23}

>[!AVAILABILITY]
>
>Diese Version ist nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie von Ihrer Adobe-Kontaktperson.

### Verbesserungen {#fall-23-rn-improvements}

* **Integration mit Adobe Experience Manager**. Bei der Erstellung einer personalisierten Versandvorlage für Transaktionsnachrichten in Adobe Experience Manager können Sie jetzt die in Campaign Standard definierten Personalisierungsfelder in einer Dropdown-Liste auswählen und verwenden. [Weitere Informationen](../../integrating/using/creating-email-experience-manager.md)

* **Cookie-Gültigkeit** – Der standardmäßige Gültigkeit von Cookies ist jetzt auf 6 Monate eingestellt und entspricht damit den Empfehlungen der französischen Datenschutzagentur (CNIL).

* **Verbesserung der Profilsuche** – Die Profilsuche wurde so optimiert, dass Zeitüberschreitungsszenarien bei Suchen reduziert werden können.

* **Lokalisierung** – Die Übersetzungen des Begriffs „audience“ bei der Bezugnahme auf eine Gruppe von Profilen, die eine Nachricht erhalten sollen, wurden für alle Digital Experience-Produkte in den folgenden Sprachen harmonisiert:

   * Deutsch: Zielgruppe
   * Brasilianisches Portugiesisch: público-alvo
   * Spanisch: público destinatario

  Diese Änderungen werden mit den nächsten Benutzeroberflächen- und Dokumentationsversionen schrittweise eingeführt.


### Sonstige Änderungen  {#fall-23-rn-other-changes}

* Transaktionsnachrichten unterstützen jetzt die Verwendung mehrerer kommagetrennter Affinitäten. [Weitere Informationen](../../sending/using/managing-typologies.md)

### Fehlerbehebungen {#fall-23-rn-fixes}

* Fehlerkorrektur – Es wurde eine Regression behoben, die bei der Verwendung großer Workflows Performance-Probleme verursachen konnte. (CAMP-53369)
* Fehlerkorrektur – Der Link in einer Workflow-E-Mail-Warnung oder -Benachrichtigung funktioniert jetzt. (CAMP-51874)

## Version 23.1 – Version Frühjahr/Sommer 2023 {#apr-23}

### Verbesserungen {#e-rn-improvements}

* Der Push-Benachrichtigungsdienst wurde modernisiert, um die Wartung zu verbessern. (CAMP-47959)
* Der SMS-Nachrichtendienst wurde modernisiert, um die Stabilität zu verbessern. (CAMP-52217)
* Adobe hat viele Fehlerbehebungen zur Barrierefreiheit vorgenommen, um die generelle Benutzerfreundlichkeit der Anwendung zu verbessern. Im Folgenden sehen Sie einige Beispiele für verbesserte Barrierefreiheit:
   * Die Barrierefreiheit der Benutzeroberfläche wurde auf vielen Bildschirmen optimiert.
   * Die Anwendung wurde für Benutzerinnen und Benutzer von Touchscreens verbessert.
   * Die Farbe mehrerer Elemente auf der Benutzeroberfläche wurde geändert, um die Sichtbarkeit zu verbessern.

### Sonstige Änderungen  {#e-rn-changes}

* Der vordefinierte **Workflow zur Erstellung von Berichtsanreicherungen** wurde hinzugefügt. Führen Sie nach dem Import eines Zielgruppen-Mappings von einer Instanz in eine andere einfach den Workflow aus, um die entsprechenden Berichtsanreicherungseinträge zu importieren. (CAMP-52452)

### Behobene Probleme{#e-rn-patches}

* Es gibt jetzt keine Timeout-Fehler mehr, wenn der Bericht zu **Klickpositionen** angezeigt wird. (CAMP-51582)
* Die Verwendung der Integration mit dem **Places**-Dienst ist jetzt wieder möglich. (CAMP-51923)
* Die Workflow-Planung funktioniert jetzt ordnungsgemäß. (CAMP-52003)
* Aufschlüsselungsdetails werden jetzt auch dann angezeigt, wenn die PDF-Version eines benutzerdefinierten dynamischen Berichts mit einer großen Datenmenge angezeigt wird. (CAMP-52178)
* Beim Zugriff auf Berichte wird jetzt keine Fehlermeldung mehr angezeigt. (CAMP-52500)
* Der Parameter **MTA-Instanzen für dieses Konto begrenzen** des SMS-Connectors wird jetzt nicht mehr auf alle Kanäle angewendet, sondern nur auf SMS. (CAMP-52640)

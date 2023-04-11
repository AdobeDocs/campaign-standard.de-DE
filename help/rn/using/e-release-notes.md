---
title: Vorzeitige Versionshinweise
description: Vorzeitige Versionshinweise
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: 485927b217fb68064897dd877c2f4a6dd208d443
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 21%

---


# Vorzeitige Versionshinweise {#e-new-release}

Auf dieser Seite werden Verbesserungen und Fehlerbehebungen beschrieben, die in der nächsten Campaign Standard-Version enthalten sind.
>[!CAUTION]
>
> Dieser Inhalt kann ohne vorherige Ankündigung bis zum Aktualisierungsdatum der Staging-Umgebung geändert werden. Weitere Informationen finden Sie auf der [Seite mit der Versionsplanung](../../rn/using/release-planning.md).

## Version 23.1 – Version Frühjahr/Sommer 2023 {#apr-23}

### Verbesserungen {#e-rn-improvements}

* Der Push-Benachrichtigungsdienst wurde modernisiert, um den Support zu verbessern. (CAMP-47959)
* Der SMS-Nachrichtendienst wurde verbessert, um eine bessere Stabilität zu erreichen. (CAMP-52217)
* Adobe hat viele Fehlerbehebungen zur Barrierefreiheit vorgenommen, um die Benutzerfreundlichkeit der Anwendung zu verbessern. Im Folgenden finden Sie einige Beispiele für Verbesserungen der Barrierefreiheit:
   * Die Barrierefreiheit der Benutzeroberfläche wurde in vielen Bildschirmen optimiert.
   * Die Anwendung wurde für Touchscreen-Benutzer verzaubert.
   * Die Farbe mehrerer Elemente auf der Benutzeroberfläche wurde geändert, um die Sichtbarkeit zu verbessern.

### Sonstige Änderungen  {#e-rn-changes}

* Die vordefinierten **Workflow zur Berichterstellung für Anreicherung** wurde hinzugefügt. Führen Sie nach dem Import eines Zielgruppen-Mappings von einer Instanz in eine andere einfach den Workflow aus, um die entsprechenden Berichterstattungseinträge zu importieren. (CAMP-52452)

### Behobene Probleme{#e-rn-patches}

* Fehlerkorrektur - Jetzt tritt kein Timeout-Fehler mehr auf, wenn die **Klickposition** Bericht. (CAMP-51582)
* Fehlerkorrektur - Die Integration mit der **Orte** Dienst. (CAMP-51923)
* Fehlerkorrektur - Die Workflow-Planung funktioniert jetzt ordnungsgemäß. (CAMP-52003)
* Fehlerkorrektur - Aufschlüsselungsdetails werden jetzt angezeigt, wenn die PDF-Version eines benutzerdefinierten dynamischen Berichts mit einer großen Datenmenge angezeigt wird. (CAMP-52178)
* Fehlerkorrektur - Beim Zugriff auf Berichte wird jetzt kein Fehler mehr angezeigt. (CAMP-52500)
* Fehlerkorrektur - Die **MTA-Instanzen für dieses Konto begrenzen** Parameter des SMS-Connectors auf alle Kanäle anwenden, anstatt nur auf SMS anzuwenden. (CAMP-52640)

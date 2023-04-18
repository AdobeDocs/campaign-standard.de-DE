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
ht-degree: 100%

---


# Vorzeitige Versionshinweise {#e-new-release}

Auf dieser Seite werden Verbesserungen und Fehlerbehebungen beschrieben, die in der nächsten Campaign Standard-Version enthalten sind.
>[!CAUTION]
>
> Dieser Inhalt kann ohne vorherige Ankündigung bis zum Aktualisierungsdatum der Staging-Umgebung geändert werden. Weitere Informationen finden Sie auf der [Seite mit der Versionsplanung](../../rn/using/release-planning.md).

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

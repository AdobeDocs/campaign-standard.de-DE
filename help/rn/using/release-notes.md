---
title: Aktuelle Version
description: Auf dieser Seite finden Sie Informationen zum Inhalt der aktuellen Version von Campaign Standard.
feature: Overview
role: User
level: Beginner
exl-id: e1f55a9b-be51-4f57-8719-fed7efc89113
source-git-commit: f9bd5901d68c09ba20d5d48d263f4818c2e1e86a
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 69%

---


# Aktuelle Version{#latest-release}

![Control Panel](assets/do-not-localize/cp-icon.png) **Neue Control Panel-Version**. [Weitere Informationen](https://experienceleague.adobe.com/docs/control-panel/using/release-notes.html?lang=de){target="_blank"}.

## Version 23.1 – Version Frühjahr/Sommer 2023 {#apr-23}

### Verbesserungen {#e-rn-improvements}

* Der Push-Benachrichtigungsdienst wurde modernisiert, um den Support zu verbessern. (CAMP-47959)
* Der SMS-Nachrichtendienst wurde verbessert, um eine bessere Stabilität zu erreichen. (CAMP-52217)
* Adobe hat viele Fehlerbehebungen zur Barrierefreiheit vorgenommen, um die Benutzerfreundlichkeit der Anwendung zu verbessern. Im Folgenden finden Sie einige Beispiele für Verbesserungen der Barrierefreiheit:
   * Die Barrierefreiheit der Benutzeroberfläche wurde in vielen Bildschirmen optimiert.
   * Die Anwendung wurde für Touchscreen-Benutzer verbessert.
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

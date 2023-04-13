---
title: Campaign Standard – Versionsplanung
description: Auf dieser Seite werden alle kommenden Versionen von Adobe Campaign Standard aufgelistet.
audience: rn
content-type: reference
topic-tags: campaign-standard-release-planning
feature: Overview
role: User
level: Beginner
exl-id: 1f48d4da-5622-4fab-af87-fcce0e40ade1
source-git-commit: 362f1f6605bc9667a80cddf2bd1bef4338cda31a
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# Versionsplanung {#release-planning}

Adobe aktualisiert laufend seine Lösungen durch neue Funktionen, Verbesserungen und Fehlerkorrekturen.

Mit jeder neuen Version werden alle Adobe Campaign Standard-Instanzen aktualisiert. Für diese Aktualisierung ist keine Maßnahme Ihrerseits erforderlich.

Aktualisierungen werden in zwei Schritten bereitgestellt. Zuerst werden Staging-Instanzen aktualisiert, damit Sie neue Funktionen testen und Ihre Konfiguration bei Bedarf anpassen können. Danach werden die Produktionsinstanzen aktualisiert.

Alle Veröffentlichungsdaten können sich ändern: Besuchen Sie diese Seite regelmäßig, um nach Updates zu suchen.

## Version 23.1 – Version Frühjahr/Sommer 2023 {#release-23-1-release}

Aktualisierungen der Umgebung erfolgen während der unten angegebenen Zeiträume in einzelnen Phasen. Details zu den Terminen werden Kunden per E-Mail mitgeteilt.

Ausführliche Informationen zu dieser Version sind in den [Versionshinweisen](release-notes.md) zu finden.

<table>
 <thead>
  <tr>
   <th> Umgebungen </th>
   <th> Daten </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>Schritt </td>
   <td>11. April 2023 – Juli 2023 </td>
  </tr>
  <tr>
   <td>Produktion </td>
   <td>18. April 2023 – Juli 2023 </td>
  </tr>
 </tbody>
</table>

Wenden Sie sich für weitere Fragen an den [Kundendienst von Adobe](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html).

## Fragen und Antworten {#questions-and-answers}

**F: Wie wirkt sich das aus?**

A: Die Änderungen sind in den [Versionshinweisen](../../rn/using/release-notes.md) aufgeführt, die auch Links zur zugehörigen Dokumentation enthalten. Adobe empfiehlt außerdem, die Seite [Eingestellte und entfernte Funktionen](../../rn/using/deprecated-features.md) zu besuchen. Diese Seiten sind für die neue Version zum Zeitpunkt der Aktualisierung der Staging-Umgebung verfügbar.

**F: Was ist der Validierungsprozess?**

A: Wenn Ihre Staging-Instanz aktualisiert wird, empfiehlt Adobe, Ihre Prozesse und Anwendungsfälle mit dieser neuen Version zu validieren und alle Probleme der [Adobe-Kundenunterstützung](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html) zu melden.

**F: Kann während des Aktualisierungsprozesses auf die Instanz zugegriffen werden?**

A: Nein. Während der Aktualisierung der Instanz ist die Datenbank möglicherweise einige Minuten lang nicht verfügbar. Alle Prozesse werden automatisch neu gestartet.

**F: Werden Nachrichten weiterhin gesendet?**

A: Nein. Für die Dauer einiger Minuten werden keine Nachrichten gesendet. Nach Abschluss der Aktualisierung werden die Prozesse automatisch neu gestartet.

**F: Werden Workflows fortgesetzt und Sendungen weiterhin durchgeführt?**

A: Nein. Während der Build-Aktualisierung werden Workflow-Server und MTA angehalten. Das bedeutet, dass Workflows und Sendungen für die Dauer einiger Minuten nicht durchgeführt werden. Es ist keine Aktion erforderlich: Die Workflows werden erneut gestartet, sobald die Instanz aktualisiert wurde.

**F: Funktionieren Tracking-Links in Nachrichten während der Aktualisierung?**

A: Ja. Während der Aktualisierung können keine neuen E-Mails gesendet werden, aber Tracking-Links, die in bereits gesendeten E-Mails enthalten sind, funktionieren.

**F: Woran ist zu erkennen, dass die Aktualisierung abgeschlossen ist?**

A: Wenn Sie sich bei Campaign anmelden, wird ein Benachrichtigungs-Popup mit der aktuellen Version angezeigt.

Wenden Sie sich bei weiteren Fragen an die [Adobe-Kundenunterstützung](https://helpx.adobe.com/de/enterprise/using/support-for-experience-cloud.html).

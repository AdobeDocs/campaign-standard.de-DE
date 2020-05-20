---
title: Campaign Standard – Versionsplanung
description: Auf dieser Seite werden alle kommenden Versionen von Adobe Campaign Standard aufgelistet.
page-status-flag: never-activated
uuid: null
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-release-planning
discoiquuid: null
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: fb865ae08a4b0db42b71e58895976a973a2ed6b7
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 99%

---


# Versionsplanung {#release-planning}

Adobe aktualisiert laufend seine Lösungen durch neue Funktionen, Verbesserungen und Fehlerkorrekturen.

Mit jeder neuen Version werden alle Adobe Campaign Standard-Instanzen aktualisiert. Für diese Aktualisierung ist keine Maßnahme Ihrerseits erforderlich.

Aktualisierungen werden in zwei Schritten bereitgestellt. Zuerst werden Staging-Instanzen aktualisiert, damit Sie neue Funktionen testen und Ihre Konfiguration bei Bedarf anpassen können. Danach werden die Produktionsinstanzen aktualisiert.

Alle Veröffentlichungsdaten können sich ändern: Wir empfehlen Ihnen, diese Seite regelmäßig zu besuchen, um nach Updates zu suchen.

**Neu!** Abonnieren Sie [Campaign Standard-Versionshinweise](http://amc-mkt-prod1-t.adobe-campaign.com/lp/LP25?service=%40rZ5cqp2DgNzrgz0alKPInakNbPSTeJYozZYnS7Wbs802u4GlISkHZX4omtK00nAU6xzZ6luEWQzr7kQ9pkCwJYumWkU), um Details zu zukünftigen Versionen direkt in Ihren Posteingang zu erhalten.

## Version 20.3.1 – Mai {#release-20-3-may-release}

Umgebungsaktualisierungen erfolgen während der unten angegebenen Zeiträume in einzelnen Phasen. Weitere Informationen über diese Version finden Sie in den [Versionshinweisen](../../rn/using/release-notes.md). Sollten Sie weitere Fragen haben, wenden Sie sich bitte an die [Kundenunterstützung von Adobe](https://support.neolane.net/webApp/extranetLogin).

<table>
 <thead>
  <tr>
   <th> Umgebung<br /> </th>
   <th> Datumsangaben<br /> </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>Staging<br /> </td>
   <td>May 26 - 27, 2020<br /> </td>
  </tr>
  <tr>
   <td> Produktion<br /> </td>
   <td>28. Mai - 1. Juni 2020<br /> </td>
  </tr>
 </tbody>
</table>



## Fragen und Antworten {#questions-and-answers}

**F: Wie wirkt sich das aus?**

A: Die Änderungen sind in den [Versionshinweisen](../../rn/using/release-notes.md) aufgeführt, die auch Links zur zugehörigen Dokumentation enthalten. Adobe empfiehlt außerdem, die Seite [Eingestellte und entfernte Funktionen](https://helpx.adobe.com/de/campaign/kb/acs-deprecated-and-removed-features.html) zu besuchen. Diese Seiten sind für die neue Version zum Zeitpunkt der Aktualisierung der Staging-Umgebung verfügbar.

**F: Was ist der Validierungsprozess?**

A: Wenn Ihre Staging-Instanz aktualisiert wird, empfiehlt Adobe, Ihre Prozesse und Anwendungsfälle mit dieser neuen Version zu validieren und alle Probleme der [Adobe-Kundenunterstützung](https://support.neolane.net/webApp/extranetLogin) zu melden.

**F: Kann während des Aktualisierungsprozesses auf die Instanz zugegriffen werden?**

A: Nein. Während der Aktualisierung der Instanz ist die Datenbank möglicherweise einige Minuten lang nicht verfügbar. Alle Prozesse werden automatisch neu gestartet.

**F: Werden Nachrichten weiterhin gesendet?**

A: Nein. Für die Dauer einiger Minuten werden keine Nachrichten gesendet. Sobald die Aktualisierung abgeschlossen ist, werden die Prozesse automatisch neu gestartet.

**F: Werden Workflows fortgesetzt und Sendungen weiterhin durchgeführt?**

A: Nein. Während der Build-Aktualisierung werden Workflow-Server und MTA angehalten. Das bedeutet, dass Workflows nicht ausgeführt und Sendungen für die Dauer einiger Minuten nicht durchgeführt werden. Es ist keine Aktion erforderlich: Die Workflows werden erneut gestartet, sobald die Instanz aktualisiert wurde.

**F: Funktionieren Tracking-Links in Nachrichten während der Aktualisierung?**

A: Ja. Während der Aktualisierung können keine neuen E-Mails gesendet werden, aber Tracking-Links, die in bereits gesendeten E-Mails enthalten sind, funktionieren.

**F: Woran ist zu erkennen, dass die Aktualisierung abgeschlossen ist?**

A: Wenn Sie sich bei Campaign anmelden, wird ein Benachrichtigungs-Popup mit der neuesten Version angezeigt.

Wenden Sie sich bei weiteren Fragen an die [Adobe-Kundenunterstützung](https://support.neolane.net/webApp/extranetLogin).

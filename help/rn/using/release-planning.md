---
title: Campaign Standard
description: Diese Seite Liste die kommenden Versionen von Adobe Campaign Standard.
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
source-git-commit: 8e614bb3e3e559a02ee5e94d9dc21e85d1b4dbd2

---


# Freigabeplanung {#release-planning}

Adobe aktualisiert laufend seine Lösungen durch neue Funktionen, Verbesserungen und Fehlerkorrekturen.

Mit jeder neuen Version werden alle Adobe Campaign Standard-Instanzen aktualisiert. Für diese Aktualisierung ist keine Maßnahme Ihrerseits erforderlich.

Aktualisierungen werden in zwei Schritten bereitgestellt. Zuerst werden Staging-Instanzen aktualisiert, damit Sie neue Funktionen testen und Ihre Konfiguration bei Bedarf anpassen können. Danach werden die Produktionsinstanzen aktualisiert.

Alle Veröffentlichungsdaten können sich ändern: Wir empfehlen Ihnen, diese Seite regelmäßig zu besuchen, um nach Updates zu suchen.

Bitte abonnieren Sie den [Erhalt von Versionshinweisen](https://www.adobe.com/subscription/priority-product-update.html) , um Informationen zu den neuesten Adobe Experience Cloud-Versionen direkt in Ihrem Posteingang zu erhalten.

## Version 20.2.1 - April {#release-20-2-april-release}

Umgebung werden in Schüben während der unten angegebenen Zeiträume aktualisiert. Ausführliche Informationen zu dieser Version finden Sie in den [Versionshinweisen](../../rn/using/release-notes.md). Wenn Sie weitere Fragen haben, wenden Sie sich bitte an den [Adobe-Kundendienst](https://support.neolane.net/webApp/extranetLogin).

<table> 
 <thead> 
  <tr> 
   <th> Umgebung<br /> </th> 
   <th> Datum-Funktionen <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Phase<br /> </td> 
   <td> March 23 - 24, 2020<br /> </td> 
  </tr> 
  <tr> 
   <td> Produktion<br /> </td> 
   <td> 31. März - 6. April 2020<br /> </td> 
  </tr> 
 </tbody> 
</table>



## Fragen und Antworten {#questions-and-answers}

**Q: Wie wirkt sich das aus?**

A: Die Änderungen sind in den [Versionshinweisen](../../rn/using/release-notes.md)aufgeführt, einschließlich Links zur zugehörigen Dokumentation. Adobe empfiehlt außerdem, die Seite &quot; [Veraltete und entfernte Funktionen&quot;aufzurufen](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html). Diese Seiten stehen zum Zeitpunkt des Upgrades auf die Stage Umgebung für die neue Version zur Verfügung.

**Q: Was ist der Validierungsprozess?**

A: Wenn Ihre Staging-Instanz aktualisiert wird, empfiehlt Adobe, Ihre Prozesse zu validieren und Anwendungsfälle mit dieser neuen Version ordnungsgemäß zu bearbeiten und alle Probleme an [Adobe Client Care](https://support.neolane.net/webApp/extranetLogin)zu melden.

**Q: Gibt es während des Aktualisierungsprozesses Zugriff auf die Instanz?**

A: Anzahl Während der Aktualisierung kann es vorkommen, dass der Zugriff auf die Datenbank innerhalb weniger Minuten nicht möglich ist. Alle Prozesse werden automatisch neu gestartet.

**Q: Werden die Nachrichten weiterhin gesendet?**

A: Anzahl Nachrichten werden nicht innerhalb weniger Minuten gesendet. Nach Abschluss der Aktualisierung werden Prozesse automatisch neu gestartet.

**Q: Wird die Workflows weiterhin laufen und die Versand senden?**

A: Anzahl Während der Buildaktualisierung werden Workflow-Server und MTA beendet. Das bedeutet, dass Workflows nicht ausgeführt werden und Versand nicht innerhalb weniger Minuten gesendet werden. Es sind keine Maßnahmen erforderlich: Workflows wird erneut Beginn, sobald die Instanz aktualisiert wurde.

**Q: Funktioniert die Nachverfolgung von Links in Nachrichten während der Aktualisierung weiterhin?**

A: Ja, sie werden funktionieren. Während der Aktualisierung können keine neuen E-Mails gesendet werden, aber Nachverfolgungslinks, die in bereits gesendeten E-Mails enthalten sind, sind funktionsfähig.

**Q: Woher weiß ich, dass die Aktualisierung abgeschlossen ist?**

A: Beim Anmelden bei Campaign wird ein Popup für die Versionshinweise mit der neuesten Version angezeigt.

Wenden Sie sich bei weiteren Fragen an den [Adobe-Kundendienst](https://support.neolane.net/webApp/extranetLogin).
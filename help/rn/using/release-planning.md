---
title: Campaign Standard Release Planning
description: Auf dieser Seite werden die kommenden Versionen von Adobe Campaign Standard aufgeführt.
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
source-git-commit: 184a878f7be573a6b45a3a2853c07029432392f0

---


# Freigabeplanung {#release-planning}

Adobe aktualisiert laufend seine Lösungen durch neue Funktionen, Verbesserungen und Fehlerkorrekturen.

Mit jeder neuen Version werden alle Adobe Campaign Standard-Instanzen aktualisiert. Für diese Aktualisierung ist keine Maßnahme Ihrerseits erforderlich.

Aktualisierungen werden in zwei Schritten bereitgestellt. Zuerst werden Staging-Instanzen aktualisiert, damit Sie neue Funktionen testen und Ihre Konfiguration bei Bedarf anpassen können. Danach werden die Produktionsinstanzen aktualisiert.

Alle Veröffentlichungsdaten können sich ändern: Wir empfehlen Ihnen, diese Seite regelmäßig zu besuchen, um nach Updates zu suchen.

Bitte abonnieren Sie den [Erhalt von Versionshinweisen](https://www.adobe.com/subscription/priority-product-update.html) , um Informationen zu den neuesten Adobe Experience Cloud-Versionen direkt in Ihrem Posteingang zu erhalten.

## Version 20.1.4 - Versionshinweise Februar {#release-20-1-4---february-release-update}

Umweltaktualisierungen erfolgen in Wellen, während der unten angegebenen Zeiträume. Ausführliche Informationen zu dieser Version finden Sie in den [Versionshinweisen](../../rn/using/release-notes.md). Wenn Sie weitere Fragen haben, wenden Sie sich bitte an den [Adobe-Kundendienst](https://support.neolane.net/webApp/extranetLogin).

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
   <td> 17.-18. Februar 2020<br /> </td> 
  </tr> 
  <tr> 
   <td> Produktion<br /> </td> 
   <td> 20. Februar - 5. März 2020<br /> </td> 
  </tr> 
 </tbody> 
</table>



## Fragen und Antworten {#questions-and-answers}

**Q: Wie wirkt sich das aus?**

A: Die Änderungen sind in den [Versionshinweisen](../../rn/using/release-notes.md)aufgeführt, einschließlich Links zur zugehörigen Dokumentation. Adobe empfiehlt außerdem, die Seite &quot; [Veraltete und entfernte Funktionen&quot;aufzurufen](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html). Diese Seiten stehen für die neue Version am Datum der Aktualisierung der Stage-Umgebung zur Verfügung.

**Q: Was ist der Validierungsprozess?**

A: Wenn Ihre Staging-Instanz aktualisiert wird, empfiehlt Adobe, Ihre Prozesse zu validieren und Anwendungsfälle mit dieser neuen Version ordnungsgemäß zu bearbeiten und alle Probleme an [Adobe Client Care](https://support.neolane.net/webApp/extranetLogin)zu melden.

**Q: Gibt es während des Aktualisierungsprozesses Zugriff auf die Instanz?**

A:Anzahl Während der Aktualisierung kann es vorkommen, dass die Datenbank einige Minuten lang nicht zugänglich ist. Alle Prozesse werden automatisch neu gestartet.

**Q: Werden die Nachrichten weiterhin gesendet?**

A:Anzahl Nachrichten werden nicht innerhalb weniger Minuten gesendet. Nach Abschluss der Aktualisierung werden Prozesse automatisch neu gestartet.

**Q: Werden die Workflows weiterhin ausgeführt und die Auslieferungen gesendet?**

A:Anzahl Während der Buildaktualisierung werden Workflow-Server und MTA beendet. Dies bedeutet, dass Workflows nicht ausgeführt werden und die Auslieferung nicht innerhalb weniger Minuten erfolgt. Es sind keine Maßnahmen erforderlich: Arbeitsabläufe starten erneut, sobald die Instanz aktualisiert wurde.

**Q: Funktioniert die Nachverfolgung von Links in Nachrichten während der Aktualisierung weiterhin?**

A: Ja, sie werden funktionieren. Während der Aktualisierung können keine neuen E-Mails gesendet werden, aber Nachverfolgungslinks in bereits gesendeten E-Mails werden verwendet.

**Q: Woher weiß ich, dass die Aktualisierung abgeschlossen ist?**

A: Wenn Sie sich bei Campaign anmelden, wird ein Popup für Versionshinweise mit der neuesten Version angezeigt.

Wenden Sie sich bei weiteren Fragen an den [Adobe-Kundendienst](https://support.neolane.net/webApp/extranetLogin).
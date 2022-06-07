---
title: Vorzeitige Versionshinweise
description: Vorzeitige Versionshinweise
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: 7767b39a48502f97e2b3af9d21a3f49b9283ab2e
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 30%

---

# Vorzeitige Versionshinweise {#new-release}

Auf dieser Seite werden neue Funktionen, Verbesserungen und Fehlerbehebungen beschrieben, die in der nächsten Campaign Standard-Version enthalten sind.

>[!CAUTION]
>
> Dieser Inhalt kann ohne vorherige Ankündigung bis zum Aktualisierungsdatum der Staging-Umgebung geändert werden. Weitere Informationen finden Sie auf der [Seite mit der Versionsplanung](../../rn/using/release-planning.md).

## Version 22.2 – Juni 2022 {#rn-2022}

**Verbesserungen**

* **Adobe Notification Service** - Campaign wird mit dem Adobe Notification Service geliefert, der es Experience Cloud-Lösungen ermöglicht, Nutzer/innen in der gesamten Experience Cloud über Aktivitäten zu informieren, die für sie wichtig sind. Ab Version 22.2 wurde das Nutzererlebnis verbessert: Benachrichtigungen werden priorisiert und produkterzeugte Benachrichtigungen werden von Adobe-Statusmeldungen getrennt. Wenn sich die Benachrichtigung auf einen bestimmten Workflow bezieht, kannst du jetzt auch direkt aus der E-Mail oder der produktinternen Benachrichtigung auf den entsprechenden Workflow zugreifen.  Weiterführende Informationen zu Adobe Campaign-Benachrichtigungen finden Sie in Abschnitt [Benachrichtigungen in Adobe Campaign](../../administration/using/sending-internal-notifications.md).

* **Optimierung beim Start des Workflows** - Adobe hat eine neue Funktion hinzugefügt, mit der die Anzahl der Workflows angepasst werden kann, die etwa zur selben Zeit beginnen. Dies würde helfen, CPU-Spitzen zu vermeiden, die zu Dienstunterbrechungen oder Ausfallzeiten geführt haben könnten. Adobe würde es nach Version 22.2 aktivieren. Es gibt kein weiteres Aktionselement für den Kunden in Bezug auf dasselbe.

* **Zugänglichkeit** - Adobe hat viele Fehlerbehebungen vorgenommen, um die Benutzerfreundlichkeit der Anwendung zu verbessern. Diese Funktionen sind derzeit nur für eine Reihe früherer Anwender verfügbar und werden in der ACS-Version 22.3 für alle Kunden eingeführt. Beispiele für Verbesserungen der Barrierefreiheit:

   * Sicherstellen, dass auf jedem Bildschirm ein sichtbarer Fokusindikator für fokussierbare Elemente vorhanden ist
   * Seitenmarkierungen für einfachere Navigation erstellen
   * Hinzufügen von Namen, Rolle, Wert und Status für viele Steuerelemente
   * Beheben von Problemen mit der dynamischen Fokusreihenfolge auf den Hauptbildschirmen

**Sicherheitsaktualisierung**

* Apache Tomcat wurde von Version 7 auf Version 8.5 aktualisiert.


**Patches**

* Fehlerkorrektur - Der technische Workflow Rechnungsstellung funktioniert jetzt einwandfrei. (CAMP-51029)
* Die fehlende Microsoft Edge-Browserkategorie wurde in Tracking-Berichten hinzugefügt. Sie wurden zuvor mit Microsoft Chrome-Öffnungen kategorisiert. (CAMP-51165)
* Es wurde ein Problem mit DSGVO-Anfragen behoben, bei denen keine Daten aus untergeordneten Tabellen gelöscht wurden. (CAMP-48276)
* Fehlerkorrektur - Die Sichtbarkeitsbedingung eines Fragments in einer Transaktionsnachrichtenvorlage wird jetzt in Email Designer gespeichert. (CAMP-50338)
* Es wurde ein Fehler in Kampagnenberichten behoben, der dazu führte, dass der Datumsbereich nicht berücksichtigt wurde. (CAMP-50991)
* Fehlerkorrektur - geplante E-Mails schlagen nun nicht mehr fehl: Die Versandanalyse konnte nicht gestartet werden, da der Versand noch den Status &quot;Erneuter Versuch steht aus&quot; aufweist. (CAMP-50302)
* Fehlerkorrektur - In Email Designer tritt jetzt kein Fehler mehr auf, wenn eine E-Mail mit einer Profilersetzung in der Vorschau angezeigt wird. (CAMP-49312)
* Es wurde ein Problem mit leerem Wert in benutzerdefinierten Auflistungen behoben: Wenn Sie eine benutzerdefinierte Ressource mit einem Feld erstellen, das eine Textauflistung ist und nur einen Wert enthält, wird dieser Wert jetzt standardmäßig festgelegt, sodass Sie eine Abfrage für dieses Feld als einfache Anforderung erstellen können. (CAMP-50606)

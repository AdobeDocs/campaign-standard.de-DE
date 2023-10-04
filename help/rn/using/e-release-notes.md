---
title: Vorzeitige Versionshinweise
description: Vorzeitige Versionshinweise
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: 46c5454ad712910c88bfda7c067fda0337b043d9
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 83%

---


# Vorzeitige Versionshinweise {#e-new-release}

Auf dieser Seite werden Verbesserungen und Fehlerbehebungen beschrieben, die in der nächsten Campaign Standard-Version enthalten sind.

>[!CAUTION]
>
> Dieser Inhalt kann ohne vorherige Ankündigung bis zum Aktualisierungsdatum der Staging-Umgebung geändert werden. Weitere Informationen finden Sie auf der [Seite mit der Versionsplanung](../../rn/using/release-planning.md).

## Version 23.2 – Version Herbst/Winter 2023 {#fall-23}

>[!AVAILABILITY]
>
>Diese Version ist nur für eine Reihe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie von Ihrer Adobe-Kontaktperson.

### Verbesserungen {#e-rn-improvements}

* **Integration mit Adobe Experience Manager**. Bei der Erstellung einer personalisierten Versandvorlage für Transaktionsnachrichten in Adobe Experience Manager können Sie jetzt die in Campaign Standard definierten Personalisierungsfelder in einer Dropdown-Liste auswählen und verwenden.

* **Cookie-Gültigkeit** – Der standardmäßige Gültigkeit von Cookies ist jetzt auf 6 Monate eingestellt und entspricht damit den Empfehlungen der französischen Datenschutzagentur (CNIL).

* **Verbesserung der Profilsuche** – Die Profilsuche wurde so optimiert, dass Zeitüberschreitungsszenarien bei Suchen reduziert werden können.

* **Lokalisierung** – Die Übersetzungen des Begriffs „audience“ bei der Bezugnahme auf eine Gruppe von Profilen, die eine Nachricht erhalten sollen, wurden für alle Digital Experience-Produkte in den folgenden Sprachen harmonisiert:

   * Deutsch: Zielgruppe
   * Brasilianisches Portugiesisch: público-alvo
   * Spanisch: público destinatario

  Diese Änderungen werden mit den nächsten Benutzeroberflächen- und Dokumentationsversionen schrittweise eingeführt.

### Sonstige Änderungen  {#e-rn-other-changes}

* Transaktionsnachrichten unterstützen jetzt die Verwendung mehrerer kommagetrennter Affinitäten.

### Fehlerbehebungen {#e-rn-fixes}

* Fehlerkorrektur - Es wurde eine Regression behoben, die bei der Verwendung großer Workflows Leistungsprobleme verursachen konnte. (CAMP-53369)
* Fehlerkorrektur - Der E-Mail-Link in einem Workflow-Warnhinweis oder einer Benachrichtigung funktioniert jetzt. (CAMP-51874)

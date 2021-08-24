---
solution: Campaign Standard
product: campaign
title: Frühzeitige Versionshinweise
description: Frühzeitige Versionshinweise
feature: Übersicht
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: fc542488cb52c4ff4e0457025a8312d2f2814cea
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 45%

---

# Frühere Versionshinweise {#new-release}

Auf dieser Seite werden neue Funktionen, Verbesserungen und Fehlerbehebungen beschrieben, die in der nächsten Campaign Standard-Version enthalten sind.

>[!CAUTION]
>
> Dieser Inhalt kann ohne vorherige Ankündigung bis zum Aktualisierungsdatum der Staging-Umgebung geändert werden. Weitere Informationen finden Sie auf der [Seite mit der Versionsplanung](../../rn/using/release-planning.md).


## Version 21.3 – September 2021 {#release-21-3---sept-2021}


**Neue Funktionen**


<table> 
<thead> 
<tr> 
<th> <strong>Einheitliche Experience Cloud-Benutzeroberfläche</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Die Kopfzeile von Adobe Campaign wurde geändert, um das Erlebnis über alle Experience Cloud-Produkte und -Services hinweg zu vereinheitlichen und zu verbessern. Diese Änderungen sollen Ihnen die Nutzung erleichtern, unter anderem durch folgende Verbesserungen:</p>
<ul>
<li>Einfacherer Wechsel zwischen Ihren Organisationen oder zu einer anderen Anwendung.</li>
<li>Verbesserte Benutzerhilfe – Durch die Einbindung von Experience League in das Produkt liefert die Suche auch Ergebnisse aus Community-Foren und mehr Videoinhalte, sodass Sie einfacheren Zugriff auf zusätzliche Inhalte haben und die Anwendung optimal nutzen können. Wir haben auch einen Feedback-Mechanismus direkt im Hilfemenü hinzugefügt, der es einfacher macht, Probleme zu melden oder Ideen zu teilen.</li>
<li>Verbesserte Benachrichtigungen – Das Dropdown-Menü "Benachrichtigungen" enthält jetzt zwei Registerkarten: eine für Ihre eigenen Produktbenachrichtigungen und eine für mehr globale Produktankündigungen.</li>
</ul>
<!--<p>For more information refer to the <a href="../../start/using/interface-description.md#top-bar">detailed documentation</a>.
</p>-->
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Audit-Protokoll</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Die neue Funktion "Audit-Protokoll"erfasst in Echtzeit eine umfassende Liste von Aktionen und Ereignissen, die in Adobe Campaign auftreten. Es bietet eine Self-Service-Möglichkeit, auf einen Datenverlauf zuzugreifen, um Fragen zu beantworten, z. B.:</p>
<ul>
<li>Was ist mit diesem Workflow passiert und wer hat ihn zuletzt aktualisiert?</li>
<li>Wer hat die letzten Änderungen vorgenommen?</li>
<li>Wie war der vorherige Status?</li>
</ul>
<p>Adobe Campaign führt nun Prüfungen für Erstellungs-, Bearbeitungs- und Löschaktionen durch: Workflows, Optionen, benutzerdefinierte Ressourcen. Änderungen dieser Elemente werden ebenfalls verfolgt.</p>
<!--<p>For more information refer to the <a href="../../administration/using/audit.md">detailed documentation</a>.
</p>-->
</td> 
</tr> 
</tbody> 
</table>


<table> 
<thead> 
<tr> 
<th> <strong>Workflow-Diagnosemodus</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td>
<p>Sie können jetzt Campaign-Workflows im diagnostischen Modus ausführen. In diesem Modus werden Informationen protokolliert, die bei der Fehlerbehebung von Ausführungsproblemen helfen. Der gesamte Ausführungsplan wird protokolliert, wenn eine Workflow-Abfrage standardmäßig mehr als eine Minute in Anspruch nimmt.</p>
<!--<p>For more information refer to the <a href="../../administration/using/audit.md">detailed documentation</a>.
</p>-->
</td> 
</tr> 
</tbody> 
</table>

**Verbesserungen**

* Beim Erstellen eines wiederkehrenden Versands in einem Workflow, der mit einem Adobe Experience Manager-Inhalt verknüpft ist, wird der Status der Inhaltsvalidierung nun vor dem Versand überprüft.
* Die Beschränkung der Datenbankverbindung ist jetzt mit dem Campaign-Package abgestimmt, um Verbindungsfehler zu vermeiden.
* Es wurde eine Konsistenzprüfung beim Erstellen von Indizes in benutzerdefinierten Ressourcen hinzugefügt und die Fehlermeldungen wurden verbessert.

**Korrekturen**

* Fehlerkorrektur - Beim Import von E-Mail-Inhalt aus einer URL tritt kein Timeout-Fehler mehr auf. (CAMP-49054)
* Es wurde ein Fehler (-69) behoben, der durch das Ende der Sitzung beim Zugriff auf eine mit Lesezeichen versehene URL oder beim Aktualisieren einer Seite über den Browser verursacht wurde. (CAMP-49003, CAMP-48930, CAMP-48894)
* Fehlerkorrektur - Regeln werden jetzt vom alten Zustellbarkeits-Server auf den neuen Zustellbarkeits-Server synchronisiert. (CAMP-48923)
* Fehlerkorrektur - Beim Laden einer E-Mail-Vorlage mit HTML-Tags in Email Designer tritt jetzt kein Fehler mehr auf. (CAMP-48243)

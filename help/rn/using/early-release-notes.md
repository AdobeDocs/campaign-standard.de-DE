---
title: Vorzeitige Versionshinweise
description: Vorzeitige Versionshinweise
feature: Overview
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 4b10eb63-3fea-438e-a1a7-25fbf7b0e5b0
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 100%

---

# Vorzeitige Versionshinweise {#new-release}

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
<p>Die neue Audit-Protokoll-Funktionalität erfasst eine umfassende Liste von in Adobe Campaign auftretenden Aktionen und Ereignissen in Echtzeit. Sie beinhaltet eine Self-Service-Option für den Zugriff auf einen Datenverlauf, damit sich zum Beispiel folgende Fragen beantworten lassen:</p>
<ul>
<li>Was ist mit diesem Workflow passiert und wer hat ihn zuletzt aktualisiert?</li>
<li>Wer hat die letzten Änderungen vorgenommen?</li>
<li>Wie war der vorherige Status?</li>
</ul>
<p>Adobe Campaign führt nun Prüfungen für Erstellungs-, Bearbeitungs- und Löschaktionen für Workflows, Optionen und benutzerdefinierte Ressourcen durch. Änderungen dieser Elemente werden ebenfalls verfolgt.</p>
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
<p>Sie können Campaign-Workflows jetzt im Diagnosemodus ausführen. In diesem Modus werden Informationen protokolliert, die bei der Fehlerbehebung von Problemen bei der Ausführung helfen. Wenn eine Workflow-Abfrage mehr als eine Minute dauert, wird standardmäßig der gesamte Ausführungsplan protokolliert.</p>
<!--<p>For more information refer to the <a href="../../administration/using/audit.md">detailed documentation</a>.
</p>-->
</td> 
</tr> 
</tbody> 
</table>

**Verbesserungen**

* Beim Erstellen eines wiederkehrenden Versands in einem Workflow, der mit einem Adobe Experience Manager-Inhalt verknüpft ist, wird der Status der Inhaltsvalidierung nun vor dem Versenden überprüft.
* Die Beschränkung der Datenbankverbindung ist jetzt mit dem Campaign-Package abgestimmt, um Verbindungsfehler zu vermeiden.
* Es wurde eine Konsistenzprüfung beim Erstellen von Indizes in benutzerdefinierten Ressourcen hinzugefügt und die Fehlermeldungen wurden verbessert.

**Korrekturen**

* Fehlerkorrektur – Der Zeitüberschreitungsfehler beim Import von E-Mail-Inhalten aus einer URL wurde behoben. (CAMP-49054)
* Fehlerkorrektur – Der Zugriff auf eine mit Lesezeichen versehene URL oder das Aktualisieren einer Seite im Browser führt nicht mehr zum Sitzungsende und zu einem Fehler (-69). (CAMP-49003, CAMP-48930, CAMP-48894)
* Fehlerkorrektur – Regeln werden jetzt vom alten Zustellbarkeits-Server auf den neuen fehlerfrei synchronisiert. (CAMP-48923)
* Fehlerkorrektur – E-Mail-Vorlagen mit HTML-Tags werden in Email Designer jetzt fehlerfrei geladen. (CAMP-48243)

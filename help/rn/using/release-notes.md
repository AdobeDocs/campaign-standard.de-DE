---
title: Neueste Version
description: Auf dieser Seite werden die zuletzt veröffentlichten Versionen von Adobe Campaign Standard aufgelistet.
page-status-flag: never-activated
uuid: 1cf2e40c-beca-43db-8261-a1820ee86ad3
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: rn
content-type: reference
topic-tags: campaign-standard-releases
discoiquuid: 5c7bfb74-4002-4ffe-87e8-bddb41d34b41
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f45985c030c3d5059bfef444287c10b842298f49
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 91%

---


# Neueste Version{#latest-release}

[Versionsplanung](../../rn/using/release-planning.md) | [Control Panel-Versionen](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html) | [Aktualisierungen der Dokumentation](../../rn/using/documentation-updates.md) | [Frühere Versionshinweise](../../rn/using/release-notes-2020.md) | [Eingestellte Funktionen](../../rn/using/deprecated-features.md)

![](assets/do-not-localize/cp-icon.png) **Neue Control Panel-Version im Juni** mit der Überwachung aktiver Profile, der Prüfung der Subdomain-Zustellbarkeit und der GPG-Schlüsselverwaltung. [Mehr dazu](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html).

## Version 20.3 – Mai 2020 {#release-20-3---may-2020}

**Neue Funktionen**

<table> 
<thead> 
<tr> 
<th> <strong>Thailändisches Datenschutzgesetz (PDPA)</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td> <p>Das thailändische Datenschutzgesetz (PDPA) ist ein neues Datenschutzgesetz, mit dem die Datenschutzanforderungen für Thailand harmonisiert und modernisiert werden. Diese Verordnung gilt für Adobe Campaign-Kunden, die Daten von Personen erfassen, die in diesem Land wohnhaft sind.</p>
<p>Zusätzlich zu den bereits in Adobe Campaign verfügbaren Datenschutzoptionen (Einverständnisverwaltung, Einstellungen für die Datenbeibehaltung und Benutzerrollen usw.) werden daher weitere Funktionen bereitgestellt, mit deren Hilfe PDPA-konformes Verhalten sichergestellt werden kann:</p>
<ul>
<li>Recht auf Zugriff und Recht auf Löschung: Hierfür werden die Funktionen genutzt, die für die DSGVO und PPDA hinzugefügt wurden – <a href="https://helpx.adobe.com/content/help/de/campaign/kb/acs-privacy.html#righttoaccess">mehr dazu</a> </li>
<li><p>Bei der Erstellung einer Datenschutzanfrage steht im Privacy Core Service nun eine Auswahl für die PDPA-Verordnung zur Verfügung. Diese Methode sollten Sie für Anfragen auf Datenzugriff bzw. -löschung verwenden. Die Campaign-API und -Schnittstelle für Zugriffs- und Löschanfragen wurde eingestellt.  Weitere Informationen dazu finden Sie im Artikel <a href="../../rn/using/deprecated-features.md">Eingestellte und entfernte Funktionen</a>.</p></li>
</ul>
<p>Weitere Informationen finden Sie in <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/privacy/privacy-overview.html">diesem Video</a>.</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Externe API-Aktivität (allgemeine Verfügbarkeit)</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>Die <strong>externe API-Aktivität </strong> wechselt von der Betaphase in die allgemeine Verfügbarkeit. Diese Version bietet zusätzliche Flexibilität für das Parsen des Textes von JSON-Antworten. Sie können jetzt:</p>
<ul>
<li>eine verschachtelte JSON mit einer maximalen Tiefe von zehn Ebenen analysieren; </li>
<li>ausgewählte Eigenschaften als Blattknoten aus einer JSON analysieren und auf eine Tabellenzeile abflachen;</li>
<li>ein Array-Objekt aus einer JSON auswählen und verwenden, ohne die "Objektdaten" benennen zu müssen oder ohne dass sie sich auf der obersten Ebene befinden müssen.</li>
</ul>
<p><strong>Vorsicht:</strong> Kunden müssen in ihren Workflows alle externen API-Aktivitäten der Betaphase <strong>durch externe API-Aktivitäten der allgemeinen Verfügbarkeit</strong> ersetzen.  Workflows, die die Betaversion der externen API verwenden, funktionieren in 20.3 nicht mehr.</p>
<p>Weiterführende Informationen finden Sie in der <a href="../../automating/using/external-api.md">ausführlichen Dokumentation</a> und in <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/managing-processes-and-data/data-management-activities/external-api-activity.html">diesem Video</a>.</p>
</td> 
</tr> 
</tbody> 
</table>

**Zusätzliche Funktionen** (ab 13. Juli)

* **AI-Powered Send Time Optimization und Profil Scoring** - Sie können jetzt Design und Versand von Kundenreisen optimieren, um die Interaktionsvorlieben jedes Einzelnen vorherzusagen. Mit der Journey-API kann Adobe Campaign offene Raten, optimale Sendezeiten und wahrscheinliche Absturzzahlen auf Basis historischer Interaktionsmetriken analysieren und vorhersagen. [Mehr dazu](../../sending/using/predictive.md)
* **Brasiliens neue Datenschutzverordnung** - Zusätzlich zu den bereits in der Kampagne verfügbaren Datenschutzfunktionen erleichtert Adobe Ihnen die Bereitschaft für Brasiliens Lei Geral de Proteçao de Datos (LGPD). Bei der Erstellung einer Datenschutzanforderung wurde die LGPD-Verordnung dem Adobe Privacy Core Service hinzugefügt. [Mehr dazu](https://helpx.adobe.com/de/campaign/kb/campaign-privacy-overview.html)

**Verbesserungen**

* Die Anzahl der Zeichen, die im Feld **Präfix** zum [Testen von Nachrichten mit Zielgruppenprofilen](../../sending/using/testing-messages-using-target.md) verwendet werden können, wurde von 32 auf 500 Zeichen erhöht.
* Die maximale Anzahl von Echtzeit-Ereignissen, die in einer Instanz veröffentlicht werden können, wurde von 350 auf 2.000 erhöht. (CAMP-41608)
* Die Synchronisation zwischen Adobe Launch und Campaign Standard wurde mithilfe des technischen Workflows syncWithLaunch verbessert. Dieser Workflow ermöglicht den automatischen Import aller Adobe Launch-Eigenschaften für Mobilgeräte in Adobe Campaign Standard. Weiterführende Informationen dazu finden Sie auf dieser [Seite](../../administration/using/technical-workflows.md).

   Sie müssen ein Ticket an die Adobe-Kundenunterstützung senden (entweder direkt oder über Ihren Adobe-Ansprechpartner), damit der technische Workflow syncWithLaunch in Ihrer Campaign-Instanz aktiviert wird. (CAMP-40082)

**Verbesserungen bei Email Designer**

* Email Designer kann jetzt eine flexiblere HTML-Formatierung als das strikte W3C-Format handhaben. (CAMP-42529)
* Bei [klickbaren Bildern](../../designing/using/links.md#inserting-a-link) werden jetzt in Inhaltsbausteinen neben dem Bild keine Links mehr angezeigt. (CAMP-41586)
* Die Weiterleitung zu einer Landingpage ist jetzt möglich, wenn der [getrackten URL](../../designing/using/links.md#about-tracked-urls) in der Vorlage eine Kategorie hinzugefügt wurde. (CAMP-41537)
* Mit dem Abstand von Schaltflächen in Outlook besteht jetzt kein Problem mehr.
* HTML-Tags werden jetzt nicht mehr im Klartext angezeigt.
* Bei der Suche nach Inhaltsbausteinen werden jetzt die Suchergebnisse des Servers sowie vorab geladene Ergebnisse angezeigt. (CAMP-41870)

**Sonstige Änderungen**

* Die Benutzeroberfläche für die Publikation benutzerdefinierter Ressourcen wurde mit klareren Fehlermeldungen ausgestattet.
* Nicht verwendete Versand-Mappings wurden aus der Benutzeroberfläche entfernt.
* Unnötige Administratorrollen wurden aus der Benutzeroberfläche entfernt.
* Checkboxes können in einer Landingpage jetzt zu Pflichtfeldern gemacht werden.
* Beim Herunterladen der CSV-Datei eines dynamischen Berichts wurde das Limit von 200 Zeilen entfernt. Sie können jetzt jede Zeile Ihres Berichts einschließen. (CAMP-40810)
* Die Sprache ES-US wurde der Liste nativer Sprachen für mehrsprachige E-Mails hinzugefügt. (CAMP-42279)
* Dateien, die mit einer Dateiübertragungs-Aktivität heruntergeladen wurden, werden nun nach X Tagen gelöscht, wobei X durch das Feld **Verlauf in Tagen** unter dem Menü **Ausführung** in den Workflow-Eigenschaften bestimmt wird – [mehr dazu](../../automating/using/managing-execution-options.md)

**Experience Platform-Integrationen**

* Die Aktivierung von Adobe [Experience Platform-Audiences](../../automating/using/aep-targeting-audiences.md) über die Aktivität **Audience lesen** wurde verbessert, um eine höhere Leistung und Stabilität zu erzielen. Darüber hinaus wurden Workflow-Logs in Bezug auf Aktivierungsvorgänge klarer und detaillierter gestaltet, was eine einfachere Überwachung und Fehlerbehebung beim Lesen von Adobe Experience Platform-Audiences ermöglicht.

**Patches**

* Während des Publikationsvorgangs einer benutzerdefinierten Ressource wird keine Geisterressource mehr erstellt.
* Die Anzeige des Marketing-Verlaufs von Profilen wird nicht mehr verhindert, wenn die Profilressource mit einer benutzerdefinierten Ressource erweitert wird. (CAMP-41009)
* Der Inhalt von nativen Landingpage-Vorlagen wird beim Öffnen des Editors nicht mehr in französischer Sprache angezeigt. (CAMP-41639)
* In Push-Benachrichtigungen mit dynamischem Inhalt wird nicht mehr Anzeige von Emojis verhindert. (CAMP-40715)
* In der Aktivität **Deduplizierung** wird einer der ausgehenden ergänzenden Transitionen kein falscher Segment-Code mehr zugewiesen. (CAMP-41400)
* Das Löschen geplanter Berichte wird jetzt nicht mehr verhindert. (CAMP-41302)
* Zwischen dem Versand-Dashboard und dem Bericht **Versandzusammenfassung** bestehen keine Abweichungen mehr. (CAMP-41145)
* In heruntergeladenen Berichten tritt jetzt kein Anzeigeproblem mit Zeichenüberschneidungen mehr auf.
* Bei Testversandersetzungen funktioniert jetzt die Vorschau eines Versands.
* Beim Löschen benutzerdefinierter Felder einer lokalen In-App-Benachrichtigung tritt jetzt kein Fehler mehr auf.
* Die Funktion &quot;charIndex&quot; funktioniert jetzt in einem Workflow mit einer **Ende**- oder **Dateiübertragungs**-Aktivität.
* Jetzt tritt kein Fehler mehr in Workflows auf, wenn eine Aktivität vom Typ **Anreicherung** mit zwei Eingabeaktivitäten verwendet wurde, einschließlich Zielgruppenressourcen, die eine Relation zueinander aufweisen. (CAMP-42133)
* Die Ausführung eines Workflows bei Verwendung unbekannter Funktionen ist jetzt möglich. (CAMP-41873)
* Beim Erstellen von Audiences mithilfe mehrerer Aktivitäten vom Typ **Audience-Speicherung** mit ergänzenden ausgehenden Transitionen tritt jetzt kein Problem mehr auf. (CAMP-39992)
* Bei der Verwendung von Personalisierung in Transaktions-E-Mails treten jetzt keine Datenabweichungen mehr auf. (CAMP-41842)
* Beim Löschen von benutzerdefinierten Feldern in Sendungen mit Push-Benachrichtigungen tritt jetzt kein Problem mehr auf. (CAMP-37586)
* Benutzer können jetzt Änderungen an Berichten vornehmen. (CAMP-42505)


![](assets/do-not-localize/cp-icon.png) **Neue Control Panel-Version im Mai** mit Zertifikatsverlängerung für CNAME-Subdomains. [Mehr dazu](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html).

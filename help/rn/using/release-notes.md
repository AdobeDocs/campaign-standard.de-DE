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
source-git-commit: b4cbc56973a57cde8af6cefa9ff89c7d29ab7b79

---


# Neueste Version{#latest-release}

[Versionsplanung](../../rn/using/release-planning.md) | [Control Panel-Versionen](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html) | [Aktualisierungen der Dokumentation](../../rn/using/documentation-updates.md) | [Frühere Versionshinweise](../../rn/using/release-notes-2020.md) | [Eingestellte Funktionen](../../rn/using/deprecated-features.md)

## Version 20.3 - Mai 2020    {#release-20-3---may-2020}

**Neue Funktionen**

<table> 
<thead> 
<tr> 
<th> <strong>Thailands Gesetz zum Schutz personenbezogener Daten (PDPA)</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
<td> <p>Der thailändische Datenschutzgesetz (PDPA) ist das neue Datenschutzgesetz, mit dem die Datenschutzanforderungen für Thailand harmonisiert und modernisiert werden. Diese Verordnung gilt für Adobe Campaign-Kunden, die Daten für in diesem Land ansässige Datensubjekte besitzen.</p>
<p>Zusätzlich zu den Datenschutzfunktionen, die bereits in Adobe Campaign verfügbar sind (einschließlich Zustimmungsverwaltung, Einstellungen zur Datenspeicherung und Benutzerrollen), nutzen wir diese Gelegenheit, um zusätzliche Funktionen einzubinden, um Ihre Bereitschaft für PDPA zu erleichtern:</p>
<ul>
<li>Recht auf Zugriff und Recht auf Löschen: nutzen wir die Funktionen, die für GDPR und CCPA hinzugefügt wurden. <a href="https://helpx.adobe.com/content/help/de/campaign/kb/acs-privacy.html#righttoaccess">mehr dazu</a> </li>
<li><p>Bei der Erstellung einer Datenschutzanforderung wurde der PDPA-Regulierungstyp in den Datenschutz-Core-Service aufgenommen. Diese Methode sollten Sie für Anfragen auf Datenzugriff bzw. -löschung verwenden. Die Campaign-API und -Schnittstelle für Zugriffs- und Löschanfragen wurde eingestellt.  Weitere Informationen dazu finden Sie im Artikel <a href="../../rn/using/deprecated-features.md">Eingestellte und entfernte Funktionen</a>.</p></li>
</ul>
<p>Weitere Informationen finden Sie in <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/privacy/privacy-overview.html">diesem Video</a>.</p>
</td> 
</tr> 
</tbody> 
</table>

<table> 
<thead> 
<tr> 
<th> <strong>Externe API-Aktivität (GA)</strong><br /> </th> 
</tr> 
</thead> 
<tbody> 
<tr> 
  <td> <p>Die <strong>externe API</strong> -Aktivität wechselt von Beta zu GA. Diese Version bietet zusätzliche Flexibilität für den JSON-Body-Parser. Sie können jetzt:</p>
<ul>
<li>analysiert eine verschachtelte JSON mit einer maximalen Tiefe von 10 Ebenen. </li>
<li>analysiert ausgewählte Eigenschaften als Blattknoten einer JSON und reduziert sie auf eine Tabellenzeile.</li>
<li>Wählen Sie ein Array-Objekt aus einem JSON aus und verwenden Sie es, ohne das Objekt "data"nennen zu müssen oder sich auf der obersten Ebene befinden zu müssen.</li>
</ul>
<p><strong>Vorsicht:</strong> Kunden müssen alle externen Beta-API-Aktivitäten <strong>durch GA-externe API-Aktivitäten in ihrer Workflows</strong> ersetzen.  Workflows, die die Betaversion der externen API verwenden, funktionieren in 20.3 nicht mehr.</p>
<p>Weiterführende Informationen finden Sie in der <a href="../../automating/using/external-api.md">ausführlichen Dokumentation</a> und in <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/managing-processes-and-data/data-management-activities/external-api-activity.html">diesem Video</a>.</p>
</td> 
</tr> 
</tbody> 
</table>

**Verbesserungen**

* Die Anzahl der Zeichen, die im Feld **Präfix** zum [Testen von Nachrichten mit zielgerichteten Profilen](../../sending/using/testing-messages-using-target.md) verwendet werden können, wurde von 32 auf 500 Zeichen erhöht.
* Die maximale Anzahl von Echtzeit-Ereignissen, die in einer Instanz veröffentlicht werden können, wurde von 350 auf 2000 erhöht. (CAMP-41608)
* Die Synchronisierung zwischen Adobe Launch und Campaign Standard wurde mithilfe des technischen Arbeitsablaufs syncWithLaunch verbessert. Dieser Arbeitsablauf ermöglicht den automatischen Import aller mobilen Adobe Launch-Eigenschaften in Adobe Campaign Standard. For more information, refer to [this page](../../administration/using/technical-workflows.md).

   Sie müssen ein Ticket an die Adobe-Kundenunterstützung senden (entweder direkt oder über Ihren Adobe-Kontakt), damit der technische Arbeitsablauf syncWithLaunch in Ihrer Kampagne aktiviert wird. (CAMP-40082)

**Verbesserungen bei Email Designer**

* Der E-Mail-Designer kann jetzt eine flexiblere HTML-Formatierung als das strikte W3C-Format handhaben. (CAMP-42529)
* Es wurde ein Problem mit [klickbaren Bildern](../../designing/using/links.md#inserting-a-link) behoben, um zu verhindern, dass Links neben dem Bild in Inhaltsblöcken angezeigt werden. (CAMP-41586)
* Es wurde ein Fehler behoben, der die Weiterleitung zu einer Landingpage verhinderte, wenn die [verfolgte URL](../../designing/using/links.md#about-tracked-urls) eine Kategorie in der Vorlage enthielt. (CAMP-41537)
* Es wurde ein Problem mit der Auffüllung von Schaltflächen in Outlook behoben.
* Es wurde ein Fehler behoben, der dazu führte, dass HTML-Tags im Klartext angezeigt wurden.
* Bei der Suche nach Inhaltsblöcken werden jetzt die Suchergebnisse des Servers sowie die Ergebnisse vorab geladen. (CAMP-41870)

**Sonstige Änderungen**

* Die Benutzeroberfläche für die Veröffentlichung benutzerdefinierter Ressourcen wurde mit klareren Fehlermeldungen verbessert.
* Nicht verwendete Versand-Zuordnungen wurden aus der Benutzeroberfläche entfernt.
* Unnötige Administratorrollen wurden aus der Oberfläche entfernt.
* Kontrollkästchen können jetzt in einer Landingpage obligatorisch sein.
* Beim Herunterladen der CSV-Datei eines dynamischen Berichts wurde der Grenzwert von 200 Zeilen entfernt. Sie können jetzt jede Zeile Ihres Berichts einschließen. (CAMP-40810)
* ES-US-Sprache in der Liste von Standardsprachen für mehrsprachige E-Mails hinzugefügt. (CAMP-42279)
* Dateien, die mit einer Aktivität für Übertragungsdateien heruntergeladen wurden, werden nun nach X Tagen gelöscht, wobei X durch das Feld **Verlauf in Tagen** unter dem Menü **Ausführung** in den Workflow-Eigenschaften bestimmt wird. [mehr dazu](../../automating/using/executing-a-workflow.md#workflow-properties)

**Experience Platform-Integrationen**

* Die Aktivierung der Adobe [Experience Platform-Audiencen](../../automating/using/aep-targeting-audiences.md) aus der Aktivität der **Read-Audience** wurde verbessert, um eine höhere Leistung und Stabilität zu erzielen. Darüber hinaus wurden Workflow-Protokolle klarer und detaillierter in Bezug auf Aktivierungen-Aufträge erstellt, was eine einfachere Überwachung und Fehlerbehebung beim Lesen von Adobe Experience Platform-Audiencen ermöglicht.

**Korrekturen**

* Es wurde ein Fehler behoben, der dazu führte, dass während des Veröffentlichungsauftrags einer benutzerdefinierten Ressource eine Geisterressource erstellt wurde.
* Es wurde ein Problem behoben, das die Anzeige des Marketingverlaufs von Profilen verhinderte, wenn die Profil-Ressource mit einer benutzerdefinierten Ressource erweitert wurde. (CAMP-41009)
* Es wurde ein Problem mit Vorlagen für vordefinierte Landingpages behoben, die ihren Inhalt beim Öffnen des Editors in französischer Sprache anzeigten. (CAMP-41639)
* Es wurde ein Problem in Push-Benachrichtigungen mit dynamischem Inhalt behoben, das die Anzeige von Emojis verhindern konnte. (CAMP-40715)
* Es wurde ein Fehler in der Aktivität **Deduplizierung-Duplikate** behoben, der dazu führte, dass einer der ausgehenden Komplementdateien ein falscher Segment-Code zugewiesen wurde. (CAMP-41400)
* Es wurde ein Fehler behoben, durch den geplante Berichte nicht gelöscht werden konnten. (CAMP-41302)
* Es wurde ein Fehler behoben, der zu Diskrepanzen zwischen dem Versand-Dashboard und dem Bericht **Versand-Zusammenfassung** führte. (CAMP-41145)
* Es wurde ein Fehler behoben, der dazu führte, dass in heruntergeladenen Berichten ein Anzeigeproblem mit Zeichenüberschneidungen auftrat.
* Es wurde ein Fehler behoben, der verhinderte, dass die Vorschau eines Versands für die Ersetzung des Testversands funktionierte.
* Es wurde ein Fehler behoben, der beim Löschen benutzerdefinierter Felder einer lokalen In-App-Benachrichtigung auftrat.
* Es wurde ein Fehler behoben, der verhinderte, dass die Funktion &quot;charIndex&quot;mit einer **End** - oder **File Transfer** -Aktivität in einem Workflow funktionierte.
* Es wurde ein Fehler in Workflows behoben, der auftrat, wenn eine Aktivität der **Anreicherung** mit zwei Eingaberessourcen verwendet wurde, einschließlich Zielgruppen-Aktivitäten, die eine Verknüpfung aufweisen. (CAMP-42133)
* Es wurde ein Problem behoben, das die Ausführung eines Workflows bei Verwendung unbekannter Funktionen verhinderte. (CAMP-41873)
* Es wurde ein Problem in Workflows behoben, das beim Erstellen von Audiencen mit mehreren Aktivitäten zum **Speichern von Audiencen** als Ergänzung zu ausgehenden Transitionen auftrat. (CAMP-39992)
* Es wurde ein Problem behoben, das zu Datendiskrepanzen bei der Verwendung der Personalisierung in transaktionalen E-Mails führte. (CAMP-41842)
* Es wurden Probleme behoben, die beim Löschen von benutzerdefinierten Feldern in Versänden mit Push-Benachrichtigungen aufgetreten sind. (CAMP-37586)
* Es wurde ein Fehler behoben, der verhinderte, dass Benutzer Änderungen an Berichten vornehmen konnten. (CAMP-42505)

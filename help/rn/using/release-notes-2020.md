---
title: Versionshinweise 2020
description: Auf dieser Seite werden alle Versionen von Adobe Campaign Standard von 2020 aufgelistet.
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
source-git-commit: 5b99fb9fbf8bdac506aeb8a35f30a7ef33aaa7e6
workflow-type: tm+mt
source-wordcount: '2953'
ht-degree: 99%

---


# Versionshinweise 2020{#release-notes-2020}

[Versionsplanung](https://helpx.adobe.com/de/campaign/kb/acs-release-planning.html) | [Control Panel-Versionen](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html) | [Aktualisierungen der Dokumentation](../../rn/using/documentation-updates.md) | [Frühere Versionshinweise](../../rn/using/release-notes-2019.md) | [Eingestellte Funktionen](https://helpx.adobe.com/de/campaign/kb/acs-deprecated-and-removed-features.html)

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
<p>Weitere Informationen finden Sie in <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/privacy/privacy-overview.html">diesem Video</a>.</p>
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
<p>Weiterführende Informationen finden Sie in der <a href="../../automating/using/external-api.md">ausführlichen Dokumentation</a> und in <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/managing-processes-and-data/data-management-activities/external-api-activity.html">diesem Video</a>.</p>
</td> 
</tr> 
</tbody> 
</table>

**Zusätzliche Funktionen** (ab 13. Juli)

* **KI-gestützte Sendezeitoptimierung und Profilbewertung**: Sie können jetzt Design und Versand von Customer Journeys optimieren, um die Interaktionsvorlieben jedes Einzelnen vorherzusagen. Mit der Journey-API kann Adobe Campaign Öffnungsraten, optimale Sendezeiten und wahrscheinliche Abwanderungszahlen anhand historischer Interaktionsmetriken analysieren und vorhersagen. [Mehr dazu](../../sending/using/predictive.md)
* **Brasiliens neue Datenschutzverordnung**: Zusätzlich zu den bereits in Campaign verfügbaren Datenschutzfunktionen hilft Ihnen Adobe, LGPD-konformes Verhalten (LGPD: brasilianische Datenschutzverordnung Lei Geral de Proteçao de Datos) sicherzustellen. Bei der Erstellung einer Datenschutzanfrage wurde dem Privacy Core Service die LGPD-Verordnung hinzugefügt. [Mehr dazu](https://helpx.adobe.com/de/campaign/kb/campaign-privacy-overview.html)

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

## Version 20.2 - April 2020 {#release-20-2---april-2020}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> <strong>Azure Blob-Integration</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Der Azure Blob Storage-Connector kann jetzt mithilfe einer Workflow-Aktivität vom Typ <strong>Dateiübertragung</strong> zum Importieren oder Exportieren von Daten in Adobe Campaign verwendet werden. </p>
    <p>Weitere Informationen finden Sie im <a href="../../administration/using/external-accounts.md#microsoft-azure-external-account">entsprechenden Handbuch</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Testen von E-Mails mit Zielgruppenprofilen</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Zusätzlich zu Testprofilen können Sie Ihre E-Mails jetzt mit echten Zielgruppenprofilen testen. So können Sie eine genaue Darstellung der Nachricht erhalten, die das Profil empfangen wird: benutzerdefinierte Felder, dynamische und personalisierte Informationen, einschließlich zusätzlicher Daten aus Workflows usw. </p>
    <p>Weiterführende Informationen finden Sie im <a href="../../sending/using/testing-messages-using-target.md">entsprechenden Handbuch</a> und in diesem <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/communication-channels/email/profile-substitution.html">Tutorial-Video</a>. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Im April werden im Control Panel von Campaign neue Funktionen veröffentlicht, einschließlich der Google TXT-Datensatzverwaltung, der Überwachung der Datenbankkapazität und eines E-Mail-Warnsystems. Weiterführende Informationen zu diesen Funktionen finden Sie im [Versionshinweis zum Control Panel](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html).

**Verbesserungen**

* Das Anwendererlebnis beim Transaktionsnachrichtenversand wurde verbessert; zudem wurde die Konsistenz der Benutzeroberfläche erhöht. [mehr dazu](../../channels/using/getting-started-with-transactional-msg.md)
* Campaign Standard ermöglicht es Ihnen jetzt, mithilfe zusätzlicher Daten aus Workflows Testsendungen an Testprofile vorzunehmen.
* Limits für die externe API-Aktivität wurden aktualisiert. [mehr dazu](../../automating/using/external-api.md)

**Verbesserungen bei Email Designer**

* Jetzt tritt kein Fehler mehr beim Escapen auf, wenn ein personalisiertes Bild mehrmals angeklickt wird.
* Beim Duplizieren dynamischer Textkomponenten wird nicht mehr die falsche Zeile dupliziert. (CAMP-41249)
* Beim Abstand in Outlook tritt jetzt kein Fehler mehr auf, wenn der Abstand auf Tabellenebene anstatt auf div-Ebene definiert wird.
* Die Breite eines Bilds ändert sich beim Wechsel in den HTML-Modus nicht mehr. (CAMP-41116)
* Auf die Social-Media-Komponente kann jetzt auch dann zugegriffen werden, wenn Alternativtext für die Symbole angegeben wird. (CAMP-41345)
* Beim Kopieren und Einfügen in Email Designer werden jetzt keine sichtbaren `<br>`-Tags mehr angezeigt.
* HTML-Tags werden jetzt nicht mehr in der E-Mail angezeigt, wenn von HTML-Inhalten auf Nur-Text umgestellt wird. (CAMP-41138)
* Das Rendering von Schaltflächen ist jetzt auch mit nur einem definierten Rand möglich.
* Beim HTML-Einzug wird jetzt die Fußzeile von E-Mails in Microsoft Outlook nicht mehr nach links verschoben. (CAMP-40987)
* Personalisierungsfelder, die ein in HTML definiertes Kollektionsattribut verwenden, werden jetzt beim Wechsel zum Nur-Text-Modus nicht mehr in den Nur-Text-Inhalt kopiert. (CAMP-40365)
* Links können jetzt in ein ausgewähltes Textsegment eingefügt wurden. (CAMP-41406)
* Beim Auswählen einer Zeitzone im Abfrageeditor wird jetzt das Datum geändert. (CAMP-38277)

**Sonstige Änderungen**

* Der native Workflow **KPI-Abstimmung mit Adobe Analytics** wird jetzt bis zum aktuellen Datum anstatt nur einen Tag lang ausgeführt.
* Das Hinzufügen von sowohl APNS als auch APNS-SANDBOX als Plattformen in einer App wird von MCPNS nicht unterstützt. Nachdem Sie das Zertifikat in Adobe Campaign Standard erfolgreich hinzugefügt haben, können Sie Ihre Einstellungen jetzt nicht mehr ändern, da der MCPNS-App nur eine APNS-Plattform (Produktion oder Sandbox) hinzugefügt werden kann.

**Experience Platform-Integrationen**

>[!NOTE]
>
>Adobe Experience Platform-Funktionen in Campaign Standard befinden sich derzeit in der Betaphase und können daher häufig ohne Vorankündigung aktualisiert werden. Weiterführende Informationen finden Sie im entsprechenden Handbuch: [Experience Platform-Connectoren ](../../developing/using/aep-about-data-connector.md), [Audience-Ziele](../../audiences/using/aep-about-audience-destinations-service.md)

* In den Workflow-Protokollen zeigt Campaign nun alle zehn Minuten die Anzahl der Datensätze an, die vom derzeit ausgeführten Auftrag bereits verarbeitet wurden.
* Ein Adobe Experience Platform-Profil, das aus der Datenbank gelöscht worden war, kann jetzt problemlos importiert werden.
* In Workflow-Protokollen wird jetzt für die Gesamtzahl der importierten Datensätze kein falsches Ergebnis mehr angezeigt.

**Korrekturen**

* Bei der Workflow-Aktivität **Anreicherung** wird beim Hinzufügen von Leerzeichen im Feld **Alias** kein neues Zeilenelement mehr erstellt. (CAMP-39229)
* Bei der Durchführung eines Testversands kann jetzt nicht mehr jedes beliebige Testprofil als Zielgruppe ausgewählt werden.
* Nach der Depublikation und Löschung einer Ereigniskonfiguration tritt jetzt kein Fehler mehr auf. [mehr dazu](../../administration/using/configuring-transactional-messaging.md#deleting-an-event)
* Die Schaltfläche **Speichern** verschwindet jetzt nicht mehr, wenn Änderungen an Workflows vorgenommen werden.
* Beim manuellen Löschen einer Datenschutzanfrage in Campaign können nach deren Verarbeitung die mit der Anfrage verknüpften Daten auch nach der Bereinigung gelöscht werden.
* Beim Anzeigen einer Vorschau oder beim Senden von Nachrichten mit Sonderzeichen aus Adobe Experience Manager tritt jetzt kein Fehler mehr auf.
* Jetzt kann in Workflows eine Aktivität mit mehreren eingehenden Transitionen problemlos ausgeführt werden.
* Standardbenutzer können &quot;Abonnements für eine Anwendung&quot; jetzt als Zieldimension in einer Workflow-Abfrage oder einem Versand verwenden. (CAMP-37618)

## Version 20.1.4 – Februar 2020 {#release-20-1-4---february-2020}

* Beim Öffnen der Aktivität **Audience lesen** in vorhandenen Workflows tritt jetzt kein Problem mehr auf. (CAMP-41002)

## Version 20.1.3 – Februar 2020 {#release-20-1-3---february-2020}

* Jetzt tritt kein Regressionsproblem mehr auf, das in 20.1 von CAMP-39273 für Kunden eingeführt wurde, die diese Lücke nutzten. CAMP-39273 wurde zurückgesetzt.

## Version 20.1.2 – Februar 2020 {#release-20-1-2---february-2020}

**Verbesserungen bei Email Designer**

* Jetzt wird kein HTML-Tag-Element mehr in einem veralteten Fragment hinzugefügt, wenn es gepatcht und der Inhalt dann gespeichert wird. (CAMP-40685)
* Bei Verwendung dynamischer Inhalte wird jetzt kein Leerzeichen mehr hinzugefügt. (CAMP-40605)
* Beim Konfigurieren einer Transaktions-E-Mail-Vorlage tritt jetzt kein Problem mehr auf. (CAMP-40604)

## Version 20.1 – Februar 2020 {#release-20-1---february-2020}

**Neue Funktionen**


<table> 
 <thead> 
  <tr> 
   <th> <strong>Adobe Experience Platform Data Connector (Beta)</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Adobe Experience Platform Data Connector ist jetzt in Adobe Campaign Standard integriert. Sie können Ihre Campaign-Daten in Adobe Experience Platform bereitstellen, indem Sie XTK-Daten (in Campaign erfasste Daten) auf das Adobe Experience Platform-Datenmodell (XDM) abbilden. </p>
    <p>Bitte beachten Sie, dass diese Funktion nur für Kunden verfügbar ist, die auf Azure gehostet werden. Weitere Informationen zu dieser Funktion und den Bedingungen für ihre Aktivierung finden Sie in der <a href="../../developing/using/aep-about-data-connector.md">ausführlichen Dokumentation</a> und im <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/administrating/adobe-experience-platform-data-connector/understanding-the-adobe-experience-platform-data-connector.translate.html">Anleitungsvideo</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Audience Destinations (Beta) </strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Mit Audience Destinations können Sie Segmente von Adobe Experience Platform für Adobe Campaign freigeben.</p>
    <p>Bitte beachten Sie, dass diese Funktion nur für Kunden verfügbar ist, die auf Azure gehostet werden. Weitere Informationen zu dieser Funktion und den Bedingungen für ihre Aktivierung finden Sie in der <a href="../../audiences/using/aep-about-audience-destinations-service.md">ausführlichen Dokumentation</a> und im <a href="https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.translate.html">Anleitungsvideo</a>. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

**Verbesserungen**

* Globale Verfügbarkeit des erweiterten MTA: Nachrichten (einschließlich Transaktionsnachrichten) werden jetzt vom erweiterten MTA von Adobe Campaign gesendet, der eine aktualisierte Versandinfrastruktur bereitstellt, die besseren Durchsatz sowie verbesserte Zustellbarkeit und Bounce-Handhabung ermöglicht – [mehr dazu](https://helpx.adobe.com/de/campaign/kb/campaign-enhanced-mta.html)

* Die Zeitzonenverwaltung wurde verbessert. Sie können jetzt eine [bestimmte Zeitzone](../../automating/using/building-a-workflow.md) für einen gesamten Workflow definieren. Die ausgewählte Zeitzone gilt für alle Aktivitäten des Workflows. Informationen zur Zeitzone, die für den Benutzer oder Server konfiguriert wurde, werden jetzt in der Benutzeroberfläche angezeigt (in Protokollen nach Auswahl einer Zeitzone). (CAMP-37672)

* Campaign Standard-APIs ermöglichen es Ihnen jetzt, bei Verwendung großer Tabellen eine Paginierung durchzuführen, indem Sie den Parameter `_forcePagination=true` zu Ihrer Aufruf-URL hinzufügen – [mehr dazu](../../api/using/pagination.md)

* Die Versandlog-ID (eine eindeutige ID für jedes Protokoll) ist jetzt in den Ressourcen Versandlogs und in den Trackinglogs für alle Zielgruppendimensionen verfügbar. Dadurch können beispielsweise beim Export Versand- oder Trackinglogs identifiziert werden – [mehr dazu](../../automating/using/exporting-logs.md)

**Verbesserungen bei Email Designer**

* Fehlende Textanweisungen beim Erstellen einer Audience wurden hinzugefügt.
* Beim Klicken auf die Schaltfläche **Inhalt ändern** im Assistenten des alten E-Mail-Editors tritt jetzt kein Problem mehr auf.
* Die Header können jetzt mit dem Inhalt des Dienstzusammenfassungsberichts abgeglichen werden. (CAMP-38103)
* Dynamische Inhaltsvarianten können jetzt gelöscht wurden, ohne dass die restliche Betreffzeile beeinträchtigt wird. (CAMP-40096)
* Bei Verwendung der B-Variante im Betreff tritt jetzt kein Fehler mehr beim A/B-Test auf. (CAMP-40327)
* Dateien können jetzt per Drag-and-Drop verschoben werden, wenn die Import-Funktion zum Hochladen von HTML verwendet wird. (CAMP-39326)
* Text kann jetzt aus einem Texteditor kopiert und eingefügt werden. (CAMP-39028)
* Wortvorschläge werden jetzt angezeigt. (CAMP-38970)
* Fragmente können jetzt durch Benutzer gespeichert werden. (ATU-2447)
* Die Duplizierung dynamischer Strukturen ist jetzt möglich. (CAMP-38367)
* Bedingungen für dynamische Inhalte werden jetzt bei der Duplizierung beibehalten. (CAMP-39051)

**Sonstige Änderungen**

* Der Filter „Sendungen mit fehlgeschlagener Vorbereitung“ berücksichtigt jetzt das Erstellungsdatum der Sendungen und nicht das letzte Änderungsdatum.
* Die organisatorische Einheit der Sicherheitsgruppe „Administratoren“ kann nicht mehr geändert werden.
* Beim Erstellen eines Profils muss jetzt das Feld für die Organisationseinheit ausgefüllt werden.
* Ein Experience Cloud Trigger kann jetzt nur gelöscht werden, wenn sowohl das Ereignis als auch die mit ihm verknüpfte Transaktionsvorlage gelöscht werden.
* [!DNL Adobe Creative SDK] wurde stillgelegt. Es wird jetzt in Campaign Standard nicht mehr unterstützt. Näheres dazu finden Sie auf der Seite [Veraltete und bereits entfernte Funktionen](https://helpx.adobe.com/de/campaign/kb/acs-deprecated-and-removed-features.html).


**Korrekturen**

* Beim Durchführen einer Datenschutzanfrage zum Löschen von Benutzerdaten werden Benutzerdaten jetzt auch in Ausschlusslogs gelöscht. (CAMP-39003)
* Jetzt bestehen keine Zugriffsprobleme mehr, wenn die Textgröße in einem Container-Element geändert wird.
* Das Kalender-Popup, das beim Bewegen des Mauszeigers in Marketing-Aktivitäten angezeigt wird, kann jetzt geschlossen werden.
* In der Aktivität **[!UICONTROL Externe API]** tritt jetzt kein Problem mehr auf, bei dem die Schaltfläche **[!UICONTROL Bestätigen]** angezeigt wurde, selbst wenn keine Daten geändert wurden.
* Bei der Verwendung der Aktivität **[!UICONTROL Vereinigung]** tritt bei Abfragen mit unterschiedlichen Zieldimensionen kein Problem mehr auf. Die Transitionsdaten zeigten nur Datensätze aus der Zielgruppendimension des Hauptsatzes an. (CAMP-36831)
* Bei der Verwendung der Aktivität **[!UICONTROL Abstimmung]** tritt in bestimmten Kontexten kein Problem mehr auf, z. B. wenn eine von zwei eingehenden Aktivitäten eine Ausschlussaktivität ist. (CAMP-37490)
* Beim Auswählen und Aktualisieren von Testprofilen tritt kein Fehler mehr auf. (CAMP-37976)
* Beim Anmelden oder Abmelden über Landingpages werden keine Fehlerseiten mehr angezeigt. (CAMP-37771)
* Beim Hochladen von Inhalten im Zip-Format tritt jetzt kein Fehler mehr auf, bei dem PNG-Dateien im HTML-Code mit ihrer Erweiterung in Großbuchstaben referenziert wurden. (CAMP-37913)
* In-App-Nachrichten können jetzt gesendet werden, wenn dem Versand ein Testprofil hinzugefügt wird.
* Bei der Workflow-Aktivität „Externe API“ wurde ein Fehler behoben, durch den bei der Verknüpfung mit Anreicherungsaktivitäten die Aktivität fehlschlug.
* Der Status von SMS-Nachrichten wird jetzt korrekt angezeigt.
* Bei benutzerdefinierten Ressourcen tritt jetzt kein Fehler mehr auf, sodass unter unterschiedlichen API-Endpunkten keine doppelten Einträge mehr angezeigt werden.
* Landingpages sind jetzt nach dem Publizieren verfügbar. (CAMP-38695)
* Beim Anzeigen von Daten aus einer Schnittmengentransition aus zwei verschiedenen Ressourcen tritt jetzt kein Fehler mehr auf. (CAMP-38974)
* Der Auflistungswert in einer Versandvorlage kann jetzt korrekt definiert werden. (CAMP-38388)
* Bei E-Mail-Massensendungen tritt jetzt kein Fehler mehr auf, bei dem der Versandstatus als „Ausstehend“ und der Gesendet-Status als „Fertig“ angezeigt wurde. (CAMP-35355)
* Die Absender-Domain wird in der dynamischen Berichterstellung jetzt korrekt angezeigt. (CAMP-33123)
* Bei den Abmeldezahlen in der dynamischen Berichterstellung treten jetzt keine Unstimmigkeiten mehr auf. (CAMP-39949)
* Beim Senden von In-App-Nachrichten können jetzt Adressen im Bildschirm „Versandlogs“ angezeigt wurden.
* SMS-Versandlogs werden jetzt mit der richtigen Anzahl von Bounces aktualisiert. (CAMP-38395)
* Die Push-Benachrichtigungstoken werden jetzt nicht mehr durch Post-Aufrufe von App-Abonnements aktualisiert. (CAMP-39273)

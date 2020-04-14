---
title: Neueste Versionshinweise 2020
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
translation-type: ht
source-git-commit: a6b0dd550dc0f6815cbf25f03fd199f4105de9c3

---


# Neueste Version{#latest-release}

[Versionsplanung](https://helpx.adobe.com/de/campaign/kb/acs-release-planning.html) | [Control Panel-Versionen](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html) | [Aktualisierungen der Dokumentation](../../rn/using/documentation-updates.md) | [Frühere Versionshinweise](../../rn/using/release-notes-2019.md) | [Eingestellte Funktionen](https://helpx.adobe.com/de/campaign/kb/acs-deprecated-and-removed-features.html)

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
    <p>Bitte beachten Sie, dass diese Funktion nur für Kunden verfügbar ist, die auf Azure gehostet werden. Weitere Informationen zu dieser Funktion und den Bedingungen für ihre Aktivierung finden Sie in der <a href="../../administration/using/aep-about-data-connector.md">ausführlichen Dokumentation</a> und im <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/adobe-experience-platform-data-connector/understanding-the-adobe-experience-platform-data-connector.html">Anleitungsvideo</a>.</p>
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
    <p>Bitte beachten Sie, dass diese Funktion nur für Kunden verfügbar ist, die auf Azure gehostet werden. Weitere Informationen zu dieser Funktion und den Bedingungen für ihre Aktivierung finden Sie in der <a href="../../audiences/using/aep-about-audience-destinations-service.md">ausführlichen Dokumentation</a> und im <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html">Anleitungsvideo</a>. </p>
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
* Adobe Creative SDK wurde eingestellt. Es wird jetzt in Campaign Standard nicht mehr unterstützt. Näheres dazu finden Sie auf der Seite [Veraltete und bereits entfernte Funktionen](https://helpx.adobe.com/de/campaign/kb/acs-deprecated-and-removed-features.html).


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

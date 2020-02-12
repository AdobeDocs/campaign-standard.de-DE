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
source-git-commit: 51408477f18725e95d3c2bd48394e776fbbe3d1d

---


# Neueste Version{#latest-release}

[Versionsplanung](https://helpx.adobe.com/campaign/kb/acs-release-planning.html) | [Control Panel-Versionen](https://docs.adobe.com/content/help/en/control-panel/using/release-notes.html) | [Aktualisierungen der Dokumentation](../../rn/using/documentation-updates.md) | [Frühere Versionshinweise](../../rn/using/release-notes-2019.md) | [Eingestellte Funktionen](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html)

## Version 20.1.2 - Februar 2020   {#release-20-1-2---february-2020}

**Verbesserungen bei Email Designer**

* Es wurde ein Problem behoben, durch das ein HTML-Tag-Element in einem veralteten Fragment hinzugefügt wurde, wenn es gepatcht und dann gespeichert wurde. (CAMP-40685)
* Es wurde ein Problem behoben, durch das bei Verwendung dynamischer Inhalte ein Leerzeichen hinzugefügt wurde. (CAMP-40605)
* Es wurde ein Problem beim Konfigurieren einer transaktionalen E-Mail-Vorlage behoben. (CAMP-40604)

## Version 20.1 - Februar 2020   {#release-20-1---february-2020}

**Neue Funktionen?**


<table> 
 <thead> 
  <tr> 
   <th> <strong>Adobe Experience Platform Data Connector (Beta)</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Der Adobe Experience Platform Data Connector ist jetzt in Adobe Campaign Standard integriert. Sie können Ihre Kampagnendaten auf Adobe Experience Platform bereitstellen, indem Sie XTK-Daten (in Campaign erfasste Daten) dem Adobe Experience Platform Data Model (XDM) zuordnen. </p>
    <p>Bitte beachten Sie, dass diese Funktion nur für Kunden verfügbar ist, die auf Azurblaus gehostet werden. Weitere Informationen zu dieser Funktion und den Bedingungen für die Aktivierung finden Sie in der <a href="../../administration/using/aep-about-data-connector.md">ausführlichen Dokumentation</a> und im <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/adobe-experience-platform-data-connector/understanding-the-adobe-experience-platform-data-connector.html">Anleitungsvideo</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>Zielgruppen-Ziele (Beta) </strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Mit Zielgruppenzielen können Sie Segmente von der Adobe Experience Platform an Adobe Campaign freigeben.</p>
    <p>Bitte beachten Sie, dass diese Funktion nur für Kunden verfügbar ist, die auf Azurblaus gehostet werden. Weitere Informationen zu dieser Funktion und den Bedingungen für die Aktivierung finden Sie in der <a href="../../audiences/using/aep-about-audience-destinations-service.md">ausführlichen Dokumentation</a> und im <a href="https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/audience-destinations/audience-destinations-overview.html">Anleitungsvideo</a>. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

**Neuheiten**

* Globale Verfügbarkeit der erweiterten MTA: Nachrichten (einschließlich Transaktionsmeldungen) werden jetzt von der Adobe Campaign Enhanced MTA gesendet, die eine aktualisierte Sendepritsche bietet, die eine verbesserte Lieferbarkeit, Durchsatz und Absprungbearbeitung ermöglicht. [mehr dazu](https://helpx.adobe.com/campaign/kb/campaign-enhanced-mta.html)

* Die Zeitzonenverwaltung wurde verbessert. Sie können jetzt eine [bestimmte Zeitzone](../../automating/using/building-a-workflow.md) für einen gesamten Workflow definieren. Die ausgewählte Zeitzone gilt für alle Aktivitäten des Workflows. Informationen zur Zeitzone, die für den Operator oder Server konfiguriert wurde, werden jetzt in der Oberfläche angezeigt (in Protokollen und nach Auswahl einer Zeitzone). (CAMP-37672)

* Kampagnen-Standard-APIs ermöglichen es Ihnen jetzt, bei Verwendung großer Tabellen Paginierung durchzuführen, indem Sie den `_forcePagination=true` Parameter zu Ihrer Aufruf-URL hinzufügen. [mehr dazu](../../api/using/pagination.md)

* Die Auslieferungsprotokoll-ID (eine eindeutige ID für jedes Protokoll) ist jetzt in den Auslieferungsprotokollen und in den Verfolgungsprotokollen für alle Targeting-Dimensionen verfügbar. Dadurch können beispielsweise beim Export Sende- oder Verfolgungsprotokolle identifiziert werden. [mehr dazu](../../automating/using/exporting-logs.md)

**Verbesserungen bei Email Designer**

* Fehlende obligatorische Textanweisungen beim Erstellen einer Zielgruppe wurden hinzugefügt.
* Es wurde ein Problem behoben, das beim Klicken auf die Schaltfläche Inhalt ****&#x200B;ändern im Assistenten des alten E-Mail-Editors auftrat.
* Es wurde ein Fehler behoben, der dazu führte, dass Kopfzeilen nicht an den Inhalt im Bericht &quot;Dienstzusammenfassung&quot;ausgerichtet wurden. (CAMP-38103)
* Es wurde ein Fehler behoben, der verhinderte, dass dynamische Inhaltsvarianten gelöscht wurden, ohne den Rest der Betreffzeile zu beeinträchtigen. (CAMP-40096)
* Korrektur eines A/B-Testfehlers bei Verwendung der B-Variante in der Betreffzeile. (CAMP-40327)
* Es wurde ein Problem behoben, das das Ziehen und Ablegen von Dateien verhinderte, wenn die Import-Funktion HTML hochladen verwendet wurde. (CAMP-39326)
* Es wurde ein Problem behoben, das das Kopieren und Einfügen von Text aus einem Texteditor verhinderte. (CAMP-39028)
* Es wurde ein Problem behoben, das die Anzeige der Wortvorschläge verhinderte. (CAMP-38970)
* Es wurde ein Problem behoben, durch das Benutzer keine Fragmente speichern konnten. (ATU-2447)

**Sonstige Änderungen**

* Der Filter &quot;Lieferungen mit fehlgeschlagener Vorbereitung&quot;berücksichtigt jetzt das Erstellungsdatum der Lieferungen und nicht das letzte Änderungsdatum.
* Die organisatorische Einheit der Sicherheitsgruppe &quot;Administratoren&quot;kann nicht mehr geändert werden.
* Beim Erstellen eines Profils muss jetzt das Feld für die Einheit des Unternehmens ausgefüllt werden.
* Ein Experience Cloud-Auslöser kann jetzt nur gelöscht werden, wenn sowohl das Ereignis als auch die mit ihm verknüpfte Transaktionsvorlage gelöscht werden.

**Korrekturen**

* Es wurde ein Fehler behoben, der beim Durchführen einer Datenschutzanforderung zum Löschen von Benutzerdaten dazu führte, dass Benutzerdaten nicht in Ausschlussprotokollen gelöscht wurden. (CAMP-39003)
* Es wurde ein Problem behoben, das zu Zugänglichkeitsproblemen führte, wenn die Größe von Text in einem Containerelement geändert wurde.
* Es wurde ein Fehler behoben, der verhinderte, dass Benutzer das Popup Kalender, das beim Bewegen des Mauszeigers in Marketingaktivitäten angezeigt wurde, nicht schließen konnten.
* Es wurde ein Problem in der **[!UICONTROL External API]** Aktivität behoben, durch das die Schaltfläche **[!UICONTROL Confirm]** angezeigt wurde, selbst wenn keine Daten geändert wurden.
* Es wurde ein Problem bei der Verwendung einer **[!UICONTROL Union]** Aktivität bei Abfragen mit unterschiedlichen Zielabmessungen behoben. Die Übergangsdaten zeigten nur Datensätze aus der Targeting-Dimension des Hauptsatzes an. (CAMP-36831)
* Es wurde ein Problem behoben, das bei der Verwendung einer **[!UICONTROL Reconciliation]** Aktivität in bestimmten Kontexten zu einem Fehler führen konnte, z. B. bei zwei eingehenden Aktivitäten, bei denen eine davon eine Ausschlussaktivität war. (CAMP-37490)
* Es wurden Leistungsprobleme behoben, die beim Auswählen und Aktualisieren von Testprofilen auftraten. (CAMP-37976)
* Es wurde ein Fehler behoben, der dazu führte, dass Fehlerseiten beim Abonnieren oder Abmelden über Einstiegsseiten angezeigt wurden. (CAMP-37771)
* Es wurde ein Problem behoben, das beim Hochladen von Inhalten im ZIP-Format auftrat und bei dem PNG-Dateien im HTML-Code mit ihrer Erweiterung in Großbuchstaben referenziert wurden. (CAMP-37913)
* Es wurde ein Fehler behoben, der verhinderte, dass In-App-Nachrichten gesendet wurden, wenn ein Testprofil zur Bereitstellung hinzugefügt wurde.
* Es wurde ein Fehler bei der Aktivität des externen API-Workflows behoben, der bei der Verknüpfung mit Anreicherungsaktivitäten fehlschlug.
* Es wurde ein Fehler behoben, der dazu führte, dass der Status von SMS-Nachrichten falsch angezeigt wurde.
* Es wurde ein Problem mit benutzerdefinierten Ressourcen behoben, bei dem doppelte Einträge unter verschiedenen API-Endpunkten angezeigt wurden.
* Es wurde ein Fehler behoben, der verhinderte, dass Einstiegsseiten nach der Veröffentlichung verfügbar waren. (CAMP-38695)
* Es wurde ein Fehler behoben, der beim Anzeigen von Daten aus einem Schnittstellenübergang aus zwei verschiedenen Ressourcen auftrat. (CAMP-38974)
* Es wurde ein Problem behoben, bei dem der Aufzählungswert in einer Bereitstellungsvorlage falsch eingestellt wurde. (CAMP-38388)
* Es wurde ein Fehler bei E-Mail-Massenlieferungen behoben, durch den der Status der Auslieferungen als Ausstehend und der Status Versendet als Fertig angezeigt wurden. (CAMP-35355)
* Es wurde ein Fehler behoben, durch den die Absenderdomäne in der dynamischen Berichterstellung falsch angezeigt wurde. (CAMP-33123)
* Es wurde ein Problem behoben, das zu Diskrepanzen bei den Abmeldezahlen in der dynamischen Berichterstellung führte. (CAMP-39949)
* Es wurde ein Fehler behoben, der verhinderte, dass beim Senden von In-App-Nachrichten Adressen im Bildschirm &quot;Senden von Protokollen&quot;angezeigt wurden.
* Es wurde ein Fehler behoben, der verhinderte, dass SMS-Senden-Protokolle mit der richtigen Anzahl von Absprüngen aktualisiert wurden. (CAMP-38395)

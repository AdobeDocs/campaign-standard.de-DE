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
source-git-commit: 66e480e957d12275d2ce5575c99b0808462588f9

---


# Neueste Version{#latest-release}

[Versionsplanung](https://helpx.adobe.com/de/campaign/kb/acs-release-planning.html) | [Control Panel-Versionen](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html) | [Aktualisierungen der Dokumentation](../../rn/using/documentation-updates.md) | [Frühere Versionshinweise](../../rn/using/release-notes-2019.md) | [Eingestellte Funktionen](https://helpx.adobe.com/de/campaign/kb/acs-deprecated-and-removed-features.html)

[Klicken Sie hier](http://amc-mkt-prod1-t.adobe-campaign.com/lp/LP25?service=%40rZ5cqp2DgNzrgz0alKPInakNbPSTeJYozZYnS7Wbs802u4GlISkHZX4omtK00nAU6xzZ6luEWQzr7kQ9pkCwJYumWkU) , um Versionshinweise zu abonnieren und Details zu den neuesten Adobe Experience Cloud-Versionen direkt in Ihrem Posteingang zu erhalten.

## Version 20.2 - April 2020     {#release-20-2---april-2020}

**Neue Funktionen?**

<table> 
 <thead> 
  <tr> 
   <th> <strong>Azurblauch-Integration</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Der Azurblauch-Datenspeicherung-Connector kann jetzt verwendet werden, um Daten mithilfe einer Workflow-Aktivität für die <strong>Übertragung von Dateien</strong> in Adobe Campaign zu importieren oder zu exportieren. </p>
    <p>Weitere Informationen finden Sie im <a href="../../administration/using/external-accounts.md#microsoft-azure-external-account">entsprechenden Handbuch</a>.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

<table> 
 <thead> 
  <tr> 
   <th> <strong>E-Mail-Tests mit zielgerichteten Profilen</strong><br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <p>Zusätzlich zu den Profilen können Sie Ihre E-Mails jetzt auch auf echten zielgerichteten Profilen testen. Dadurch können Sie eine genaue Darstellung der Nachricht erhalten, die das Profil erhalten wird: benutzerdefinierte Felder, dynamische und personalisierte Informationen, einschließlich zusätzlicher Daten aus Workflows usw. </p>
    <p>Weiterführende Informationen finden Sie in der <a href="../../sending/using/testing-messages-using-target.md">ausführlichen Dokumentation</a> und im <a href="https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/profile-substitution.html">Tutorial-Video</a>. </p>
   </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Im April werden in der Systemsteuerung der Kampagne neue Funktionen veröffentlicht, einschließlich Google TXT-Datensatzverwaltung, Datenbankraumüberwachung und E-Mail-Benachrichtigung. Weitere Informationen zu diesen Funktionen finden Sie in der Versionshinweise zur [Systemsteuerung](https://docs.adobe.com/content/help/de-DE/control-panel/using/release-notes.html).

**Neuheiten**

* Die Benutzerfreundlichkeit von Nachrichten für Transaktionsnachrichten wurde verbessert und die Konsistenz der Oberfläche wurde verbessert. [mehr dazu](../../channels/using/about-transactional-messaging.md)
* Mit Campaign Standard können Sie jetzt Testversand mit zusätzlichen Daten aus Workflows an Test-Profil senden.
* Die Richtlinien für die externe API-Aktivität wurden aktualisiert. [mehr dazu](../../automating/using/external-api.md)

**Verbesserungen bei Email Designer**

* Es wurde ein Fehler behoben, der sich auf das Ausbrechen auswirkte, wenn ein personalisiertes Bild mehrmals angeklickt wurde.
* Es wurde ein Fehler behoben, der beim Duplizieren dynamischer Textkomponenten dazu führte, dass die Zeile mit wong dupliziert wurde. (CAMP-41249)
* Es wurde ein Problem mit der Auffüllung in Outlook behoben, das beim Definieren der Auffüllung auf Tabellenebene statt auf div-Ebene auftrat.
* Es wurde ein Fehler behoben, der dazu führte, dass die Breite eines Bildes beim Wechsel zum HTML-Modus geändert wurde. (CAMP-41116)
* Es wurde ein Fehler behoben, der verhinderte, dass auf die Social-Media-Komponente zugegriffen werden konnte, wenn alternative Texte zu den Symbolen bereitgestellt wurden. (CAMP-41345)
* Es wurde ein Fehler behoben, der dazu führte, dass beim Einsatz von Kopieren und Einfügen im E-Mail-Designer sichtbare `<br>` Tags angezeigt wurden.
* Es wurde ein Fehler behoben, der dazu führte, dass HTML-Tags in der E-Mail angezeigt wurden, nachdem von HTML-Inhalten auf Text umgestellt wurde. (CAMP-41138)
* Es wurde ein Problem behoben, das die Wiedergabe von Schaltflächen mit nur einem Rand verhinderte.
* Es wurde ein Fehler im HTML-Einzug behoben, der dazu führte, dass die Fußzeile von E-Mails in Microsoft Outlook nach links verschoben wurde. (CAMP-40987)
* Es wurde ein Fehler behoben, der dazu führte, dass Personalisierungsfelder, die auf ein in HTML definiertes Sammlungsattribut abzielten, beim Wechsel zum Nur-Text-Modus in den Nur-Text-Inhalt kopiert wurden. (CAMP-40365)
* Es wurde ein Fehler behoben, der verhinderte, dass Links in ein ausgewähltes Textsegment eingefügt wurden. (CAMP-41406)
* Es wurde ein Fehler behoben, der dazu führte, dass das Datum beim Auswählen einer Zeitzone im Abfragen-Editor geändert wurde. (CAMP-38277)

**Sonstige Änderungen**

* Der Out-of-the-Box-Arbeitsablauf für die **KPIs-Abstimmung mit Adobe Analytics** wird jetzt bis zum aktuellen Datum ausgeführt, anstatt nur einen Tag lang ausgeführt zu werden.
* Das Hinzufügen von APNS und APNS-SANDBOX als Plattformen in einer App wird nicht unterstützt. Nachdem Sie das Zertifikat in Adobe Campaign Standard erfolgreich hinzugefügt haben, können Sie Ihre Einstellungen jetzt nicht mehr ändern, da der MCPNS-App nur noch eine APNS-Plattform (Produktions- oder Sandbox) hinzugefügt werden kann.

**Experience Platform-Integrationen**

>[!NOTE]
>
>Die Funktionen der Adobe Experience Platform in Campaign Standard befinden sich derzeit in der Betaphase, die möglicherweise ohne Vorankündigung häufig aktualisiert wird. Weitere Informationen finden Sie in der ausführlichen Dokumentation: Data Connector [für](../../administration/using/aep-about-data-connector.md)Experience Platform, [Audience-Ziele](../../audiences/using/aep-about-audience-destinations-service.md)

* In den Workflow-Protokollen zeigt die Kampagne nun alle 10 Minuten die Anzahl der Datensätze an, die bereits vom derzeit ausgeführten Auftrag verarbeitet wurden.
* Es wurde ein Problem behoben, das beim Importieren eines Adobe Experience Platform-Profils auftrat, das aus der Datenbank gelöscht wurde.
* Es wurde ein Problem in Workflow-Protokollen behoben, durch das ein falsches Ergebnis für die Gesamtanzahl der importierten Datensätze angezeigt werden konnte.

**Korrekturen**

* Es wurde ein Problem mit der Aktivität des Arbeitsablaufs für die **Anreicherung** behoben, das beim Hinzufügen von Leerzeichen im Feld &quot; **Alias** &quot;auftrat, das dann ein neues Zeilenelement erstellte. (CAMP-39229)
* Es wurde ein Problem behoben, bei dem jedes Profil beim Senden einer Testversand-Nachricht als Ziel ausgewählt werden konnte.
* Es wurde ein Problem behoben, das nach dem Rückgängigmachen der Veröffentlichung und Löschen einer Ereignis-Konfiguration auftrat. [mehr dazu](../../administration/using/configuring-transactional-messaging.md#deleting-an-event)
* Es wurde ein Problem behoben, bei dem die Schaltfläche **Speichern** verschwand, wenn Änderungen an Workflows vorgenommen wurden.
* Es wurde ein Problem behoben, das beim manuellen Löschen einer Datenschutzanforderung in Kampagne nach deren Verarbeitung dazu führte, dass mit der Anforderung verknüpfte Daten auch nach der Bereinigung nicht gelöscht werden konnten.
* Es wurde ein Problem behoben, das beim Anzeigen einer Vorschau oder beim Senden von Nachrichten mit Sonderzeichen aus Adobe Experience Manager auftreten konnte.
* Es wurde ein Problem behoben, das in Workflows auftreten konnte, wenn eine Aktivität mit mehreren eingehenden Transitionen ausgeführt wurde.
* Es wurde ein Fehler behoben, der dazu führte, dass Standardbenutzer die Dimension &quot;Abonnement zu einer Anwendung&quot;nicht als Zielgruppe in einer Workflow-Abfrage oder einem Versand verwenden konnten. (CAMP-37618)
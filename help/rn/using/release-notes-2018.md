---
title: Versionshinweise 2018
description: Auf dieser Seite werden alle Versionen von Adobe Campaign Standard von 2018 und aufgelistet.
feature: Overview
role: User
level: Beginner
exl-id: 17521357-14ae-4751-bd7c-aeabbcf71d07
TQID: https://experienceleague.adobe.com/BtRFMP6fh8X5Z6R1wGzc0Q07HCQlx-2-3evgAOnU3eA
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: a075b2c1-7748-4328-b7f6-343aa314616aid: b12f6872-9271-4369-85e5-86969a0b99a2id: c309ee4e-82e4-4f7e-b608-ef345678c34eid: c5474392-5419-4296-9e41-f6f4ce4f6e9bid: d5ef99fa-df0c-4153-bf94-105ad0724167
subfeature_v2: id: b1fd1501-3105-4d6b-b4d4-9af53126df75id: bf97c196-a4d1-4fa3-a151-e68a114c8ac0id: c3bf7e1e-1db5-4c72-9293-e2f0b1ab73d0id: e3988c18-3cfa-4f16-b812-ac2d2b1056faid: e5e477db-ebc7-4368-ab0f-4d8fc2aed405id: e739ee2b-6228-412e-878f-45de0791417did: eff19c99-440a-4318-b319-444edc4d8d8f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: d095671a-1355-40aa-8b5f-06c33c68080bid: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: c2422ff58487b6e8251eab2508760cd201b2eebe
workflow-type: ht
source-wordcount: 5273
ht-degree: 100%

---

# Versionshinweise 2018{#release-notes}

## Version 18.9 – September 2018 {#release-18-9-september-2018}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> In-App-Messaging (Beta-Version)<br /> </td> 
   <td> In-App-Messaging ermöglicht Ihnen, Mobile-App-Benutzer wirkungsvoller anzusprechen, da In-App-Messaging kontextuelle Interaktionen ermöglicht und Benutzer erreicht werden können, die sich von Push-Benachrichtigungen abgemeldet haben. Die Nutzung von In-App-Messaging gemeinsam mit Push-Benachrichtigungen ermöglicht ein stark personalisiertes und relevantes Benutzererlebnis. Dies wiederum sorgt für mehr Konversionen und bessere Bindung Ihrer App-Benutzenden<br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/about-in-app-messaging.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Integration von Adobe Launch für Mobile Apps (Betaversion)<br /> </td> 
   <td> Durch die Integration von Adobe Launch mit Adobe Campaign wird jetzt die Aktivierung einer App-Eigenschaft in Campaign mit dem Mobile SDK V5 vereinfacht und automatisiert<br /> Lesen Sie für weiterführende Informationen das <a href="https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**Verbesserungen**

* Adobe Campaign Standard unterstützt jetzt Version 4 der Amazon S3 API.

**Sonstige Änderungen**

* In den Broadlogs wird jetzt zwischen der maximalen Anzahl der Verbindungen und der maximalen Anzahl der Nachrichten pro Stunde unterschieden. Wenn das Limit erreicht wurde, wird jetzt der Grund für den beschränkten Durchsatz angegeben. Zuvor wurde in beiden Fällen dieselbe Meldung angezeigt (‘quota met’).
* Bei der Konfiguration einer Mobile App in Campaign ist es jetzt für den Benutzer ersichtlich, ob das iOS-Zertifikat und der Android-Server-Schlüssel erfolgreich hochgeladen wurden und wie ihr Ablaufdatum lautet.

  Weiterführende Informationen finden Sie im entsprechenden Handbuch zur Konfiguration einer Mobile App mit [SDK V4](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdkv4.html) und [SDK V5](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html).

* Benutzer einer bestimmten Mobile App können nun direkt als Zielgruppe ausgewählt werden, indem Sie die entsprechende Mobile App bei der Definition der Campaign-Eigenschaften auswählen. Diese Funktion ist für sowohl den Push- als auch den In-App-Messaging-Kanal verfügbar.

  Weitere Informationen finden Sie im [entsprechenden Handbuch](../../channels/using/preparing-and-sending-a-push-notification.md#preparing-the-notification).

* Bei der Auswahl eines Inhaltsbausteins über die Creative-Designer-Benutzeroberfläche werden jetzt alle Inhaltsbausteine auf der Liste geladen und angezeigt. (CAMP-27311)

  Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../designing/using/personalization.md#adding-a-content-block).

**Patches**

* Fehlerkorrektur – Jetzt stimmt die Loganzahl am E-Mail-Dashboard und in der E-Mail-Versandzusammenfassung für Transaktions-E-Mails überein. (CAMP-28237
* Fehlerkorrektur – In Workflows wird jetzt keine Fehlermeldung mehr angezeigt, wenn eine Datei mit einer Dateitransferaktivität importiert wird. (CAMP-27435)
* Fehlerkorrektur – Die Auswahl von Diensten wird jetzt nicht mehr im Formular aufgehoben, wenn Landingpages über 25 Dienste enthalten. (CAMP-26572)
* Fehlerkorrektur – Bei der Verwendung des Dateitransfers können jetzt in Workflows externe Konten mit einer SFTP-URL konfiguriert werden. (CAMP-26475)
* Fehlerkorrektur – Der Dienstzusammenfassungsbericht wird jetzt aktualisiert. (CAMP-26301)
* Fehlerkorrektur – In Workflows wird bei der Verwendung einer Aktivität „Anreicherung“ jetzt in benutzerdefinierten Feldern das korrekte Datum angezeigt. (CAMP-26242)
* Fehlerkorrektur – Das Datum des Abonnements eines Dienstes wird jetzt aktualisiert, wenn es über einen Dateiimport importiert wird.
* Fehlerkorrektur – Dateien werden jetzt auch dann korrekt importiert, wenn ein Workflow eine Datei-laden-Aktivität enthält (CAMP-27068).
* Fehlerkorrektur – In Dienstzusammenfassungsberichten wird jetzt nicht mehr die falsche Anzahl von Abonnements angezeigt (CAMP-25587).
* Fehlerkorrektur – Die Daten in Adobe-Analytics- und Adobe Campaign-Berichten weichen jetzt nicht mehr voneinander ab. (CAMP-25393)
* Fehlerkorrektur – Benutzer mit beschränktem Zugriff können sich jetzt anmelden. (CAMP-27381)
* Fehlerkorrektur – Die Liste der Adobe-Experience-Manager-Inhalte kann jetzt angezeigt werden, wenn eine E-Mail mit Creative Designer bearbeitet wird. (CAMP-27181)
* Fehlerkorrektur – Creative Designer kann jetzt geöffnet werden und erzeugt keinen Fehler mehr. (CAMP-27304)
* Fehlerkorrektur – Im Creative Designer funktioniert die Drag &amp; Drop-Funktion jetzt auch bei Verwendung von Internet Explorer 11 ordnungsgemäß.
* Fehlerkorrektur – Jetzt werden Bilder, die aus einer Kamera hochgeladen und im Porträtmodus aufgenommen wurden, nicht mehr in einer unerwünschten gedrehten Position dargestellt.
* Fehlerkorrektur – Bei der Verwendung der Benutzeroberfläche des Abfrage-Editors in Creative Designer werden jetzt keine unklaren Auswahlinformationen mehr angezeigt.
* Fehlerkorrektur – Bei der Verwendung der Benutzeroberfläche des Abfrage-Editors in Creative Designer werden Elemente jetzt ordnungsgemäß dupliziert.
* Fehlerkorrektur – SMS-Nachrichten werden jetzt nicht mehr an Empfänger auf der Blockierungsliste gesendet. Zuvor geschah dies weiterhin, wenn die Abmeldung über eine automatische Antwort erfolgt war. (CAMP-27128)
* Fehlerkorrektur – Jetzt wird der Fehler angezeigt, wenn der Workflow **Datenbankbereinigung** fehlschlägt. (CAMP-26876)
* Fehlerkorrektur – Jetzt können benutzerdefinierte Felder bei der Definition einer Push-Benachrichtigung gelöscht werden. (CAMP-25588)

## Version 18.7 - Juli 2018 {#release-18-7-july-2018}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Versand mit hoher Priorität für Android-Push-Benachrichtigungen<br /> </td> 
   <td> Versand mit hoher Priorität für Android: ermöglicht den Versand einer Push-Benachrichtigung mit hoher Priorität für Android-Apps, wodurch ein inaktives Gerät aktiviert wird und einige beschränkte Verarbeitungsvorgänge ausführen kann. Beachten Sie bitte, dass die Standardpriorität „Normal“ ist, was den Nachrichtenversand verzögern kann, um den Akku zu schonen.<br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/customizing-a-push-notification.md#change-the-notification-behavior-for-android">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Typologiefilter für App-Abonnentinnen und -Abonnenten<br /> </td> 
   <td> Unterstützung von Abonnements bei Typologiefiltern – Wenn Sie die Filterkriterien für eine Typologieregel angeben, können Anwendungsabonnements als Filter- und Zielgruppendimension ausgewählt werden. So können Sie nach Attributen für Benutzende mit oder ohne Profil filtern.<br /> Lesen Sie für weiterführende Informationen das <a href="../../sending/using/about-typology-rules.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Automatischer Import von Inhalten von einer URL während der Nachrichtenvorbereitung<br /> </td> 
   <td> Jetzt ist es möglich, in der Vorbereitungsphase E-Mail-Inhalt von einer URL zu importieren. Bei wiederkehrenden E-Mail-Sendungen wird bei jeder Nachrichtenvorbereitung der jeweils letzte HTML-Inhalt abgerufen, wodurch gewährleistet wird, dass der Inhalt zum Versandzeitpunkt stets aktuell ist. Mit dieser Funktion kann auch ein terminierter Versand mit Inhalt von einer URL durchgeführt werden, selbst wenn der Inhalt noch nicht verfügbar ist.<br /> Lesen Sie für weiterführende Informationen das <a href="../../designing/using/using-existing-content.md#retrieving-content-from-a-url-automatically-at-preparation-time">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Benachrichtigung bei einer neuen Version von Campaign<br /> </td> 
   <td> Jetzt wird einem Benutzer bei der Anmeldung eine Nachricht angezeigt, wenn eine Instanz auf eine neue Version aktualisiert wurde. Die Nachricht enthält die Versionsnummer und einen Link zu den Versionshinweisen. Der Benutzer kann diese Nachricht bis zur Aktualisierung auf die nächste Version verbergen. <br /> </td> 
  </tr> 
  <tr> 
   <td> Benutzerverwaltung<br /> </td> 
   <td> Ab Version 18.7 steht die Funktion der geografischen Einheiten nicht mehr für neue Campaign Standard-Instanzen sowie bestehende Instanzen zur Verfügung, für die keine geografischen Einheiten erstellt wurden.<br /> Weitere Informationen finden Sie auf dieser <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/deprecated-features.html?lang=de">Seite</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**Verbesserungen**

* Die Integration von Adobe Campaign mit Adobe Target ermöglicht jetzt die Verwendung der [Berechtigungsfunktion](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/properties-overview.html?lang=de) von Target. Beim Einfügen eines dynamischen Bildes von Adobe Target in eine E-Mail können Sie jetzt eine Target Property spezifizieren (at_property code).
* Benutzerdefinierte Ressourcen, die über eine owncopy-Relation mit der Profilressource verbunden sind, werden jetzt von DSGVO-Zugriffs- bzw. Löschanfragen berücksichtigt. Für einfache Relationen mit Kardinalität 1 und Sammlungsrelationen mit Kardinalität N muss in der benutzerdefinierten Ressource die Option &quot;Beim Löschen/Duplizieren des Ziel-Datensatzes werden auch die von der Relation referenzierten Datensätze gelöscht/dupliziert&quot; ausgewählt werden. Für einfache Relationen mit Kardinalität 0 oder 1 muss die Option &quot;Beim Löschen/Duplizieren des Datensatzes wird auch der von der Relation referenzierte Ziel-Datensatz gelöscht/dupliziert&quot; ausgewählt werden.

**Sonstige Änderungen**

* Das Zeitlimit für die Berichtfreigabe wurde von einer auf vier Minuten erhöht, um Zeitüberschreitungsfehler zu vermeiden.
* Beim Bearbeiten des Inhalts einer E-Mail wird automatisch der neue Creative Designer geöffnet. Bei Bedarf können Sie jederzeit nach dem Speichern Ihrer Änderungen zum Standard-Inhaltseditor wechseln. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../designing/using/designing-content-in-adobe-campaign.md).
* Im Creative Designer kann jetzt eine neue Inhaltskomponente – das Karussell – in eine E-Mail eingefügt werden. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../designing/using/designing-from-scratch.md#about-content-components).
* Im Klick-Bericht einer Transaktionsnachricht werden beim Anklicken der Schaltfläche **Profil wechseln** jetzt nur die Testprofile aufgelistet, die mit dem Ereignis verknüpft sind, das Sie für diese Transaktionsnachricht definiert haben.

**Patches**

* Fehlerkorrektur – bei der Verwendung des Abfragefilters &quot;Nach E-Mail&quot; werden jetzt Ergebnisse ausgegeben. (CAMP-23420)
* Fehlerkorrektur – Jetzt können keine Standardbenutzenden mehr auf bestimmte Funktionen oder Bildschirme zugreifen, die Administrierenden vorbehalten sind (/rest/head/&#42;-Endpunkte, Bildschirme für Transaktionsnachrichten sowie Profil- und Zielgruppe-Importe).
* Fehlerkorrektur – in DSGVO-Löschanfragen können jetzt benutzerdefinierte Ressourcen auch dann bearbeitet werden, wenn deren Name mit einer Zahl beginnt.
* Fehlerkorrektur – mit der Zielgruppe-speichern-Aktivität können jetzt in Adobe Experience Cloud App-Abonnenten freigegeben werden.
* Fehlerkorrektur – jetzt tritt kein Fehler mehr in der Dateiübertragungsaktivität auf, wenn der Dateiname Leerzeichen enthält. (CAMP-25936)
* Fehlerkorrektur – jetzt tritt kein Fehler mehr auf, wenn die Schaltfläche zum Aufbau einer neuen Verbindung verwendet wird, nachdem eine Sitzung abgelaufen ist. (CAMP-25560)
* Fehlerkorrektur – jetzt kommt es nicht mehr zu Ausschlüssen, wenn Sendungen mit einer Zeitzonenoptimierung in Verbindung mit Ermüdungsregeln durchgeführt werden. (CAMP-25425)
* Fehlerkorrektur – jetzt können bei der Verwendung der API-DSGVO-Funktion auch Daten mit einer 0:1-Relation gelöscht werden.
* Fehlerkorrektur – jetzt erscheint keine Fehlermeldung mehr, wenn die Bearbeitung einer Ermüdungs-Typologieregel abgebrochen wird.
* Fehlerkorrektur – jetzt tritt kein Fehler mehr auf, wenn der Nachrichteninhalt nach seiner Bearbeitung in der Vorschau angesehen wird.
* Fehlerkorrektur – jetzt tritt kein Fehler mehr auf, wenn komprimierte CSV-Dateien während der Verwendung der Dekomprimierungsoption verarbeitet werden.
* Fehlerkorrektur – jetzt werden in Creative Designer keine unerwünschten farbigen Schriften und Formatierungen mehr verursacht, wenn Text mit integrierten Stilelementen in einen Link umgewandelt oder dieser Link bearbeitet wird. (CAMP-26001)
* Fehlerkorrektur – jetzt werden im Klick-Bericht die Prozentsätze für alle Bedingungen in Sendungen angezeigt, die dynamischen Content enthalten. Zuvor wurden nur die Klicks auf die Standardvariante angezeigt.

## Version 18.6 - Juni 2018 {#release-18-6-june-2018}

**Verbesserungen**

* Die API **[!UICONTROL Verlauf]** wurde zu Adobe.IO hinzugefügt. Damit können Sie Informationen zum Marketing-Verlauf eines Profils abrufen: Anzahl der Touchpoints, gesendete Nachrichten, URL der Mirrorseite. Weitere Informationen dazu finden Sie im [dedizierten Anwendungsfall](../../api/using/interacting-with-marketing-history.md).
* Der technische Workflow **[!UICONTROL Datenbankbereinigung]** wurde optimiert, um eine bessere Performance der Datenbanksicherung zu gewährleisten.
* Creative Designer für E-Mail ist jetzt auch in Französisch und Deutsch verfügbar.

**Sonstige Änderungen**

* Bei gesendeten Nachrichten wurde im Fenster **[!UICONTROL Bereitstellung]** die Schaltfläche **[!UICONTROL Statistiken berechnen]** hinzugefügt. Damit können Sie die aktuellen KPIs abrufen, z. B. wenn die Ergebnisse des Versands zu langsam aktualisiert werden oder nicht berücksichtigt wurden. Weiterführende Informationen hierzu finden Sie in diesem [Abschnitt](../../sending/using/confirming-the-send.md).
* Funktionale Administratoren können jetzt im nativen technischen Workflow **Zustellbarkeit** die Anzahl aufeinanderfolgender Fehler definieren, die in der JavaScript-Aktivität **Regel-Update** ignoriert werden sollen. Standardmäßig beträgt der Feldwert 0, was bedeutet, dass alle Fehler ignoriert werden.
* Die SQL-Abfrage zur Verwaltung der Zugriffsbeschränkungen auf Einheiten wurde optimiert.
* Die Aktivität **[!UICONTROL Aktualisieren]** ermöglicht jetzt das Hinzufügen, Aktualisieren oder Löschen von Daten zu Abonnements (nms:appSubscriptionRcp-Tabelle).
* Der technische Workflow **[!UICONTROL Update der Versandausführung]** wurde in zwei Workflows unterteilt, um die Performance zu verbessern: **[!UICONTROL Update der Versandausführung]**: Hiermit wird das Tracking des Versands aktualisiert. Dieser Workflow wird standardmäßig alle zehn Minuten gestartet. **[!UICONTROL Aktualisierung der Versandindikatoren]**: Hiermit werden die Versand-KPIs aktualisiert. Dieser Workflow wird standardmäßig jede Stunde gestartet. Weiterführende Informationen zu technischen Workflows finden Sie in diesem [Abschnitt](../../administration/using/technical-workflows.md#list-of-technical-workflows).
* Wenn Nachrichten versendet werden, kann der Status im Bereich **[!UICONTROL Bereitstellung]** jetzt zwei Werte aufweisen: **[!UICONTROL Senden]**: Die Nachrichten werden gesendet. **[!UICONTROL Senden (erneuter Versuch)]**: Ein erneuter Versuch wird unternommen.
* Benutzer mit der Benutzerrolle **[!UICONTROL Versandvorbereitung]** können jetzt Testsendungen durchführen. (CAMP-24313)
* Die Option **TLS über SMPP aktivieren** wurde zum externen Konto **SMS-Routing durch SMPP** hinzugefügt. Weiterführende Informationen hierzu finden Sie in diesem [Abschnitt](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing).

**Patches**

* Fehlerkorrektur – E-Mails können jetzt gesendet werden, wenn sie ein dynamisches Bild von Adobe Target enthalten (CAMP-24848).
* Fehlerkorrektur – die technischen Workflows **[!UICONTROL Datenschutzanfrage/Datenlöschung]** werden jetzt abgeschlossen, wenn eine der Anfragen fehlschlägt.
* Fehlerkorrektur – Privacy Core Service erhält jetzt Anfragestatus-Aktualisierungen von Campaign.
* Fehlerkorrektur - der technische Workflow **[!UICONTROL Freigegebene Zielgruppe importieren]** funktioniert jetzt ordnungsgemäß (CAMP-25465).
* Fehlerkorrektur – Datenschutzanfragen in Campaign werden jetzt in Core Privacy Service als abgeschlossen gekennzeichnet.
* Fehlerkorrektur – die IMS-Authentifizierung bei Campaign Standard ist jetzt auch mit langen Adobe IDs möglich. (CAMP-24095)
* Fehlerkorrektur – in Creative Designer tritt jetzt kein Fehler mehr auf, wenn Inhaltsmodule entfernt werden. (CAMP-25242)
* Fehlerkorrektur – jetzt können bei Push-Benachrichtigungen auch für Abonnenten Ermüdungsregeln verwendet werden, deren Profil nicht in der Datenbank ist. (CAMP-25344)
* Fehlerkorrektur – jetzt erscheint keine Fehlermeldung mehr, wenn auf Versand-Ausschlusslogs zugegriffen wird. (CAMP-24724)
* Fehlerkorrektur – jetzt können in Instanzen mit erweiterten Versandlogs Testsendungen vorbereitet werden.
* Fehlerkorrektur – beim Veröffentlichen von benutzerdefinierten Ressourcen mit aktivierter Erweiterung der **[!UICONTROL Versandlogs]** treten jetzt keine Fehler mehr auf.
* Fehlerkorrektur – jetzt wird die Versandlaufzeit im wiederkehrenden Versand berücksichtigt.
* Fehlerkorrektur – jetzt können im Menü **[!UICONTROL Benutzerdefinierte Daten]** Daten für benutzerdefinierte Ressourcen mit über 100.000 Datensätzen sortiert werden. (CAMP-24308)
* Fehlerkorrektur – jetzt werden benutzerdefinierte Profildimensionen bei der Verwendung der Suchfunktion in dynamischen Berichten berücksichtigt.
* Fehlerkorrektur – jetzt werden internationale Daten auch in auf Kontoebene erstellten dynamischen Berichten korrekt angezeigt.
* Jetzt kann ein Dienst ohne Anmelde- oder Abmeldebestätigungsnachricht erstellt werden.

## Version 18.5 - Mai 2018 {#release-18-5-may-2018}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> DSGVO: Core Service-Integration<br /> </td> 
   <td> Durch die Integration von Privacy Core Service können Sie DSGVO-Anfragen in einer Umgebung mit mehreren Lösungen über nur einen einzigen JSON API-Aufruf automatisieren.<br /> DSGVO-Anfragen, die von Privacy Core Service an alle Experience Cloud-Lösungen gesendet werden, werden jetzt von Campaign automatisch verarbeitet<br /> Lesen Sie für weiterführende Informationen das <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy.html?lang=de">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Verbesserung bei Push-Benachrichtigungen – detailliertes Versand-Feedback<br /> </td> 
   <td> Adobe Campaign bietet jetzt die Möglichkeit, von Anbietern (APNS/GCM) per MCPNS detailliertes Feedback (Versandlogs und Ausschlusslogs) zu Push-Benachrichtigungen zu erhalten.<br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/preparing-and-sending-a-push-notification.md#sending-the-notification">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Erweiterung der Versandlogs<br /> </td> 
   <td> Ermöglicht die Erweiterung von Versandlogs mit Profildaten und Segment-Code aus Workflows. Diese Daten können dann in dynamischen Berichten verwendet werden, sodass Sie zum Versandzeitpunkt einen aktuellen Überblick über einige Daten erhalten.<br /> Es gibt zwei weitere Anwendungsfälle: <br /> 
    <ul> 
     <li> Export erweiterter Broadlogs mit „eingefrorenen“ Daten: Eine Marketing-Fachkraft möchte alle Profile exportieren, in denen der Segment-Code gleich „A“ ist (aus der Workflow-Engine abgerufen). </li> 
     <li> Segmentierung „eingefrorener“ Daten: Eine Marketing-Fachkraft möchte alle Profile, die seit dem letzten Versand 1.000 Treuepunkte gesammelt haben oder deren Segment-Code gleich „A“ war, <strong>erneut ansprechen</strong>. </li> 
    </ul> Lesen Sie für weiterführende Informationen das <a href="../../developing/using/configuring-the-resource-s-data-structure.md#defining-sending-logs-extension">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Dynamisches Reporting mit benutzerdefinierten Profildaten<br /> </td> 
   <td> Diese Funktion ermöglicht die Erstellung und Verwaltung von Berichten auf der Basis benutzerdefinierter Profildaten, die während der Profil-Ressourcenerweiterung generiert wurden. Sie können Berichte nach Profilattributen wie beispielsweise dem Treueprogramm oder dem bevorzugten Kanal aufschlüsseln.<br /> Weitere Informationen finden Sie in der <a href="../../developing/using/configuring-the-resource-s-data-structure.md#defining-sending-logs-extension">detaillierten Dokumentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**Verbesserungen**

* Speicherverbrauch und CPU-Auslastung der Anwendung wurden verbessert.

**Sonstige Änderungen**

* Die Workflow-Aktivität &quot;Audience lesen&quot; kann jetzt Experience Cloud-Audiences lesen. Zuvor konnte diese Aktivität nur Zielgruppen vom Typ Abfrage und Liste lesen. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../automating/using/read-audience.md). (CAMP-23623)
* Die Kennung der freigegebenen Standard-Datenquelle ist jetzt schreibgeschützt und kann nicht mehr geändert werden. Eine Änderung dieser Kennung könnte Probleme verursachen, wenn Zielgruppen gemeinsam mit Experience Cloud verwendet werden.
* Der Import von Audiences aus Audience Manager funktioniert jetzt mit aufgesplitteten Dateien. Zuvor wurde vom technischen Workflow importSharedAudience nur die letzte Datei des Segments importiert.
* Externe AWS-S3-Konten unterstützen jetzt Regionen und Version 4 des Authentifizierungsmechanismus. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../administration/using/external-accounts.md).
* Das Asset-Auswahlfenster lädt jetzt schneller und die Auswahl eines Assets und das Schließen des Fensters ist jetzt problemlos möglich.
* Die Eigenschaften und Struktur technischer Workflows können jetzt von Benutzern geändert werden, die Administratorrechte besitzen und den Organisations- und geografischen Einheiten &quot;Alle&quot; angehören.
* Die Benutzeroberfläche der Segmentierungsaktivität wurde bei der Erstellung neuer Segmente verbessert. Der Tab &quot;Begrenzung&quot; erscheint jetzt direkt nach dem Hinzufügen einer Begrenzung. Die Namen neuer Segmente werden jetzt mit aufsteigenden Nummern versehen (&quot;Segment 1&quot;, &quot;Segment 2&quot; etc.).
* Zur Workflow-Ressource wurde das Feld &quot;nextProcessingDate&quot; hinzugefügt. Dieses Feld ist nur über REST-API-Aufrufe sichtbar und ermöglicht die Visualisierung der Daten der nächsten Ausführungen von Workflows.
* Das Feld „sourceId“ wird jetzt in der Trackinglog-Ressource (nms:trackingLog) angezeigt.
* Die Werte der Gesamtöffnungen und der Gesamtklicks können jetzt in einer einfach strukturierten Datei mit einem Workflow exportiert werden. (CAMP-24186)
* In den Profilen ist jetzt unter den bevorzugte Sprachen &quot;Englisch - Dänemark&quot; verfügbar. (CAMP-23728)
* Bei der Verwendung einer Segmentierungsaktivität mit einem Zusatzdaten-Link (targetData) werden Sie jetzt über eine Nachricht darauf hingewiesen, dass die Daten außerhalb des Workflows nicht verfügbar sind. Diese Nachricht wird angezeigt, wenn in der Segmentierungsaktivität die Zählungs- oder Vorschau-Schaltfläche ausgewählt wird. (CAMP-23651)
* Der von Workflows verbrauchte Speicherplatz wurde optimiert: (CAMP-21979): Die von der Aktivität &quot;Datei laden&quot; verarbeiteten Dateien werden jetzt standardmäßig gelöscht. Es gibt aber auch eine Option, mit der die Speicherung bei Bedarf möglich ist. Wenn ein Workflow gelöscht wird, wird sein Ordner im Verzeichnis auf dem Server automatisch unterdrückt.

**Patches**

* Fehlerkorrektur – jetzt weisen alle Roh-Berichtereignisse damit verknüpfte Tracking-Ereignisse auf, da das Feld eventDate jetzt ordnungsgemäß befüllt wird.
* Fehlerkorrektur – personalisierte Felder werden jetzt im Vorschaufenster eines Push-Benachrichtigungsversands angezeigt.
* Fehlerkorrektur – jetzt wird der Nachrichtentext einer Push-Benachrichtigung im Vorschaufenster mit Zeilenumbruch angezeigt.
* Fehlerkorrektur – jetzt tritt kein Fehler mehr auf, wenn ein wiederkehrender Versand mithilfe eines Workflows gesendet wird und die Hauptzielgruppe leer ist.
* Fehlerkorrektur – auf ein Zielgruppen-Mapping kann jetzt auch dann zugegriffen werden, wenn es mit einem nicht vorhandenen Schema verknüpft ist.
* Fehlerkorrektur – beim Import einer komprimierten Datei mithilfe einer Datei-laden-Aktivität tritt jetzt kein Fehler mehr auf. (CAMP-24309)
* Fehlerkorrektur – jetzt tritt bei der Durchführung eines wiederkehrenden Versands kein PostgreSQL-Fehler mehr auf. (CAMP-23613)
* Fehlerkorrektur – jetzt wird keine Fehlermeldung mehr angezeigt, wenn eine REST-API-Anfrage mit einem leeren JSON-Attribut gesendet wird. (CAMP-23506)
* Fehlerkorrektur – jetzt werden in Profilen die Buchstaben nach einem &quot;ß&quot; nicht mehr groß geschrieben. (CAMP-23136)
* Fehlerkorrektur – jetzt tritt kein Fehler mehr beim Versand von Nachrichten auf, bei denen eine Personalisierung oder eine Bedingung für dynamische Inhaltsbausteine verwendet wird, während Attribute von einem verknüpften Schema eines Profils verwendet werden. (CAMP-22751)
* Fehlerkorrektur – Dienste können jetzt gelöscht werden. (CAMP-22050)
* Fehlerkorrektur – in Testprofilen kann jetzt das Land oder das Bundesland geändert werden. (CAMP-20426)
* Fehlerkorrektur – Creative Designer kann jetzt geladen werden. (CAMP-24573)
* Fehlerkorrektur – jetzt werden im E-Mail-Betreff keine Zeichen mehr nach den Personalisierungsfeldern entfernt. (CAMP-24113)

## Version 18.4 - April 2018 {#release-18-4-april-2018}

**Patches**

_Plattform_

* Fehlerkorrektur – DSGVO-Zugriff- oder Löschanfragen können jetzt korrekt verarbeitet werden. Dieser Fehler trat in seltenen Fällen auf, wenn die extrahierten Daten eines der folgenden Zeichen enthielten: &amp; &lt; > &quot; &#39;.

_E-Mails, SMS und Briefpost_

* Fehlerkorrektur – KPIs werden jetzt nicht mehr mit falschen Werten überschrieben, wenn die Broadlog-Synchronisation über eine Stunde dauert.

_Workflows_

* Die Speicherverwaltung und Workflow-Performance wurden verbessert.

_Reporting_

* Mit dem KPI-Freigabe-Workflow werden jetzt die Zustellungswerte für die letzten zwei Monate anstatt der letzten sechs Monate abgerufen. Fehlerkorrektur – im externen KPI-Freigabe-Konto wird kein verkürztes Datum mehr angezeigt.
* Fehlerkorrektur – jetzt werden alle Nachrichten in den Metriken **Gesendet**, **Zugestellt** und **Bounce** berücksichtigt.
* Fehlerkorrektur – jetzt tritt kein Fehler mehr auf, wenn der gewählte Zeitraum im Bericht der **Versandzusammenfassung** zu lang war.

_Benutzerdefinierte Ressourcen_

* Fehlerkorrektur – jetzt tritt kein Fehler mehr bei der Vorbereitung der benutzerdefinierten Ressource auf.

## Version 18.3 - März 2018 {#release-18-3-march-2018}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> EU-Datenschutz-Grundverordnung (DSGVO)<br /> </td> 
   <td> Die DSGVO ist das neue Datenschutzgesetz der Europäischen Union (EU) zur Harmonisierung und Modernisierung von Datenschutzanforderungen, das am 25. Mai 2018 in Kraft trat. Die DSGVO gilt für Kundinnen und Kunden von Adobe Campaign, die Daten für Personen mit Wohnsitz in der EU erfassen.<br /> Aus diesem Grund möchten wir als Datenverarbeiter Ihnen als die Datenverantwortlichen zusätzlich zu den bereits in Adobe Campaign verfügbaren Datenschutzoptionen (Einverständnisverwaltung, Einstellungen für die Datenaufbewahrung und Benutzerrollen etc.) weitere Funktionen bereitstellen, mit deren Hilfe Sie DSGVO-konformes Verhalten sicherstellen können:<br /> 
    <ul> 
     <li> Recht auf Zugriff: Die betroffene Person hat das Recht, eine Kopie ihrer personenbezogenen Daten zu erhalten, die vom Datenverantwortlichen erfasst werden. Hierzu zählen unter Umständen auch die in Adobe Campaign gespeicherten Daten. </li> 
     <li> Recht auf Löschung: Die betroffene Person hat das Recht, seine personenbezogenen Daten, die vom Datenverantwortlichen erfasst werden, löschen zu lassen. Hierzu zählen unter Umständen auch die in Adobe Campaign gespeicherten Daten. </li> 
    </ul> Lesen Sie für weiterführende Informationen das <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy.html?lang=de">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Creative Designer für E-Mail (Beta-Version)<br /> </td> 
   <td> Der neue Creative Designer von Adobe Campaign ermöglicht ein vollständig integriertes Erstellungserlebnis in Campaign und sorgt für die rasche und einfache Gestaltung attraktiver, individuell personalisierter E-Mails, ohne dass auch nur eine einzige Zeile Code geschrieben werden muss. Mit der leistungsstarken Drag-and-Drop-Oberfläche unterstützt der Creative Designer bei der Skalierung der E-Mail-Erstellung. Benutzende können entweder mit einer leeren Seite beginnen oder vorhandene Inhaltsfragmente oder Vorlagen verwenden. <br /> Zu den wichtigsten Funktionen zählen:<br /> 
    <ul> 
     <li> Optische Gestaltung und Erstellung vollständig personalisierter, responsiver E-Mails mithilfe einer Drag-and-Drop-Benutzeroberfläche optimiert durch native Creative Cloud-Integrationen </li> 
     <li> Erstellung und Speicherung einer E-Mail Inhaltsvorlage und Verwendung gespeicherter Vorlagen zur Vereinfachung der E-Mail-Erstellung </li> 
     <li> Erstellen und Speichern von Inhaltsfragmenten (z. B. Kopf- und Fußzeile, Artikel) zur Optimierung der Inhaltserstellung und Sicherstellung der Markenkonsistenz </li> 
     <li> Nahtloser Wechsel zwischen der Erstellung in der Drag &amp; Drop-Benutzeroberfläche und der direkten Bearbeitung von HTML-Code einer E-Mail per Tastendruck </li> 
    </ul> Creative Designer für E-Mails ist nur auf Englisch verfügbar.<br /> Weitere Informationen finden Sie in der <a href="../../designing/using/designing-content-in-adobe-campaign.md">detaillierten Dokumentation</a> und in diesem <a href="https://www.youtube.com/watch?time_continue=1&amp;v=5S_6A4fsfms">Video</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Versand mehrsprachiger Push-Sendungen<br /> </td> 
   <td> Dieselbe mehrsprachige Benutzeroberfläche, die bereits für den E-Mail- und SMS-Kanal verfügbar ist, wurde zum Push-Kanal hinzugefügt, damit Sie Kundinnen und Kunden unabhängig von ihrer bevorzugten Sprache ansprechen können.<br /> Diese Funktion bietet eine skalierbare, automatische Lösung für Kundinnen und Kunden, die Push-Kampagnen verwalten, die sich über mehrere Regionen erstrecken, und Benutzende in ihrer bevorzugten Sprache ansprechen möchten. Sie können damit per Klick alle Sprachvarianten über eine Vorlage in einen Push-Versand hochladen. Adobe Campaign führt daraufhin eine automatische Segmentierung auf der Basis der Spracheinstellungen der Benutzenden durch und hilft dadurch, unnötige Arbeitsschritte durch die Vereinfachung von Workflows und Reporting zu vermeiden.<br /> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/creating-a-multilingual-push-notification.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Verwendung von benutzerdefinierten Ressourcen in Transaktionsnachrichten<br /> </td> 
   <td> Neben vorkonfigurierten Feldern können Sie beim Transaktions-Messaging nun auch benutzerdefinierte Ressourcen zur Inhaltsanreicherung Ihrer Nachrichten nutzen.<br /> Zum Beispiel:<br /> 
    <ul> 
     <li> Verwenden Sie benutzerdefinierte Felder als Abstimmungskriterien zwischen Transaktionsnachricht und Profil. </li> 
     <li> Verwenden Sie vollständige Profile, Dienste und verknüpfte Daten, um Transaktionsnachrichten stärker zu personalisieren. </li> 
    </ul> Lesen Sie für weiterführende Informationen das <a href="../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**Patches**

_Plattform_

* Fehlerkorrektur – jetzt können auch mehr als 5.000 Datensätze aus einer Liste exportiert werden.
* Fehlerkorrektur – Daten können jetzt in Dateien exportiert werden, deren Name eine Personalisierungsfeld-Variable enthält.

_E-Mails, SMS und Briefpost_

* Fehlerkorrektur – Multipart-SMS sind jetzt nicht mehr abgeschnitten, da die Größe der Teile nun in Byte anstelle von Zeichen berechnet wird.
* Eine Option wurde hinzugefügt, mit der die KPIs **[!UICONTROL Zugestellt]** oder **[!UICONTROL Bounces + Fehler]** in Echtzeit nach dem Versand aktualisiert werden können. Sie werden direkt anhand des im Provider übermittelten SR (Status Report) neu berechnet.
* Fehlerkorrektur – jetzt tritt im Kalender-Widget in der Versandplanung kein Fehler mehr auf.
* Fehlerkorrektur – jetzt tritt kein Fehler mehr in der Anzeige auf, wenn eine Zielgruppe zum zweiten Mal in einem bereits durchgeführten Versand geöffnet wird.
* Fehlerkorrektur – jetzt fordert keine Fehlermeldung mehr zur Eingabe eines Startdatums auf, wenn eine E-Mail-Vorlage mit verzögertem Versanddatum erstellt wird.
* Fehlerkorrektur – bei der Bearbeitung des Inhalts einer Nachricht treten jetzt keine Probleme mehr mit dem Bild-Rendering auf.
* Fehlerkorrektur – bei Testsendungen tritt bei der Duplizierung einer Kampagne kein Fehler mehr auf.
* Fehlerkorrektur – jetzt wird keine Fehlermeldung mehr angezeigt, wenn nach dem Hinzufügen eines Versands zum Workflow über die Navigationsleiste auf eine Kampagnenvorlage zugegriffen wird.
* Fehlerkorrektur – jetzt kann der Gewinner einer A/B-Test-E-Mail automatisch ausgewählt werden, sodass die E-Mail gesendet werden kann. Dieser Fehler konnte auftreten, wenn der Versand im Status **[!UICONTROL retryInProgress]** war.
* Fehlerkorrektur – jetzt tritt keine Fehlermeldung mehr auf, wenn die Parameter einer A/B-Test-E-Mail erneut geöffnet werden.

_Zielgruppen und Abfragen_

* Fehlerkorrektur – jetzt können Sie auf Daten zugreifen und Abfragen für Empfänger einrichten, die von Adobe Campaign Classic in Standard repliziert wurden.
* Fehlerkorrektur – jetzt tritt kein Fehler mehr auf, wenn nach Auswahl der Schaltfläche **Zählung** oder **Vorschau** im Abfrage-Editor ein Filtertyp-Feld verwendet wird.

_Workflows_

* Der Workflow **Rechnungsstellung (Billing)** wurde optimiert, um die Versandvorbereitungsphase zu verkürzen.
* Fehlerkorrektur – Populationsdaten werden jetzt auch dann in der ausgehenden Transition angezeigt, wenn eine wiederkehrende Versandaktivität verwendet wird.
* Fehlerkorrektur – in der ausgehenden Transition von **Daten-Update-Aktivitäten** werden Datensätze zu Zurückweisungen jetzt korrekt angezeigt.
* Fehlerkorrektur – jetzt tritt kein Fehler mehr beim technischen Workflow **deliverabilityUpdate** auf.

_Integrationen_

* Fehlerkorrektur – jetzt werden internationale Zeichen korrekt an Adobe Analytics gesendet.
* Assets werden jetzt schneller geladen, wenn versucht wird, ein Bild aus der Asset-Bibliothek von Experience Cloud in eine Nachricht einzufügen.
* Fehlerkorrektur – jetzt kann das Fenster für die Asset-Auswahl immer geschlossen werden.
* Sie können jetzt von der Detailansicht einer Datenquelle direkt auf ihren Workflow zugreifen und den Status des Workflows überprüfen.
* Sie können jetzt das Triggers-Schema direkt aktualisieren, wenn Sie ein Trigger-Ereignis definieren oder bearbeiten. Durch diese Änderung müssen Sie die Veröffentlichung des Triggers nicht mehr aufheben und keinen neuen erstellen.

_Transaktionsnachrichten_

* Fehlerkorrektur – jetzt tritt kein Fehler mehr mit der Transaktionsnachrichtenvorlage auf, wenn die Versandressource erweitert wird.
* Jetzt können Transaktionsnachrichten gelöscht werden.

## Version 18.2 - Februar 2018 {#release-18-2-february-2018}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Anmeldung – Eine Profilliste für mehrere Dienste an- oder abmelden<br /> </td> 
   <td> Die Workflow-Aktivität <strong>An-/Abmeldedienst</strong> ermöglicht es Ihnen jetzt, eine Profilliste für mehrere Dienste an- bzw. abzumelden. Importieren Sie in Ihren Workflow eine Datei mit Profilen sowie dem Aktionstyp und Dienst für jedes Profil. Die Aktivität <strong>Abonnementdienste</strong> kann diese Informationen nutzen und alle Ihre Profilabonnements und -abmeldungen dynamisch auf einmal bearbeiten.<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/subscription-services.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Aktivität „Anreicherung“ – Anreicherung von Daten auf der Basis eingehender Transitionen<br /> </td> 
   <td> Mit der neuen Workflow-Aktivität <span class="uicontrol">Anreicherung</span> können Sie die eingehenden Transitionen nutzen, um die ausgehenden Transitionen mit Zusatzdaten anzureichern. Wenn Sie Profile als Ziel auswählen, können Sie im Rahmen der Anreicherungsaktivität die Profilinformationen mit zusätzlichen Daten anreichern, die nicht in der Datenbank gespeichert sind (sondern z. B. aus einer importierten Datei kommen).<br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/enrichment.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**Patches**

_Plattform_

* Die Symbolleiste am oberen Bildschirmrand von Adobe Campaign enthält jetzt das neue Experience-Cloud-Menü.
* Fehlerkorrektur – der Link zur Option **[!UICONTROL Angebote]** wird jetzt in der Lösungs-Dropdown-Liste angezeigt.

_E-Mails, SMS und Briefpost_

* die Performance der Versandvorbereitungsphase wurde verbessert.
* Fehlerkorrektur – mehrere Probleme mit Trackinglogs wurden behoben, die in manchen Situationen fehlerhaft waren.
* Fehlerkorrektur – jetzt tritt kein Fehler mehr beim Kontaktdatum auf, wenn es zwischen der Vorbereitung und der Bestätigung eines Versands geändert wird. Wenn das Kontaktdatum jetzt nach der Vorbereitung geändert wird, muss der Versand erneut vorbereitet werden, bevor er bestätigt werden kann. Weitere Informationen finden Sie in der [ausführlichen Dokumentation](../../sending/using/preparing-the-send.md).

_Push-Benachrichtigungen_

* Fehlerkorrektur – Personalisierungsfelder funktionieren jetzt in iOS-Push-Benachrichtigungen fehlerlos.
* Fehlerkorrektur – die Klick- und Öffnungsraten werden im Push-Benachrichtigungs-Dashboard jetzt nicht mehr systematisch mit 0 % angegeben.

_Berichte_

* Fehlerkorrektur – die Liste verfügbarer Berichte wird jetzt allen Browsern korrekt angezeigt.
* Fehlerkorrektur – jetzt tritt im technischen Workflow **[!UICONTROL Berichtfreigabe]** unmittelbar vor dem Ablaufdatum kein Fehler mehr auf.

_Workflows_

* Fehlerkorrektur – auf Aktivitäten kann jetzt zugegriffen werden, nachdem sie durch Drag &amp; Drop verschoben wurden.
* Fehlerkorrektur – die Reihenfolge der ausgehenden Transitionen wird jetzt in der Aktivität **[!UICONTROL Segmentierung]** nicht mehr geändert.
* Fehlerkorrektur – beim Lesen von mithilfe eines Workflows gespeicherten Zielgruppen, die ein Auflistungsfeld enthalten, tritt kein Fehler mehr auf.
* Fehlerkorrektur – die Option **[!UICONTROL Vor dem Nachrichtenversand Bestätigung einholen]** bleibt jetzt nicht mehr aktiviert, nachdem sie bei der Definition der Planung eines in einem Workflow erstellten Versands deaktiviert wurde.
* Das automatische Löschen von Duplikaten (DISTINCT-Klausel) kann jetzt in **[!UICONTROL Abfrage]**-Aktivitäten mit einer neuen Option im Tab **[!UICONTROL Zusatzdaten]** deaktiviert werden. Die Deaktivierung dieser Option wird zur Performance-Verbesserung empfohlen, wenn zahlreiche (über 100) zusätzliche Elemente definiert werden.

_Integrationen_

* Der **[!UICONTROL Data sources]** Konfigurationsbildschirm wurde verbessert.

_Bekannte Probleme_

Wir raten von der Nutzung von Internet Explorer Version 11 ab, da Anzeigeprobleme auftreten können.

Probleme könnten auftreten, wenn Links zur kontextuellen Hilfe auf der Campaign-Benutzeroberfläche verwendet werden. Diese werden in Version 18.3 korrigiert.

## Version 18.1 - Januar 2018 {#release-18-1-january-2018}

**Neue Funktionen**

<table> 
 <thead> 
  <tr> 
   <th> Funktion<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Reporting für die Ermüdungsverwaltung<br /> </td> 
   <td> In diesem konfigurierbaren Bericht ist innerhalb eines bestimmten Zeitraums vor dem Versanddatum zu sehen, wie sich die Ermüdungsregeln auf E-Mail-, Push-, SMS- und Briefpost-Sendungen auswirken. Da sie nun alle in Konflikt zueinander stehenden Marketing-Kampagnen in einer einzigen Ansicht sehen können, sind Marketing-Fachleute in der Lage, Marketing-Kampagnen gemäß den Ermüdungsregeln effektiver zu planen und die Kommunikation entsprechend zu priorisieren.<br /> Lesen Sie für weiterführende Informationen das <a href="../../sending/using/fatigue-rules.md#viewing-the-fatigue-rule-summary-report">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Berichtfreigabe<br /> </td> 
   <td> Mit der Berichtfreigabe können Sie Adobe Campaign-Benutzenden automatisch regelmäßig Berichte als E-Mail-Anhang senden. Benutzende, die wiederkehrende Berichte erhalten, haben die Möglichkeit, sich über einen dedizierten Link in jeder E-Mail von diesen Nachrichten abzumelden.<br /> Lesen Sie für weiterführende Informationen das <a href="../../reporting/using/reporting-interface.md#share-tab">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Neue Push-Funktionen<br /> </td> 
   <td> Vorschau von Push-Benachrichtigungen: Zeigen Sie im Inhaltseditor für Push-Benachrichtigungen eine Vorschau von Push-Benachrichtigungen auf iOS- und Android-Geräten an, um genau zu sehen, was Ihre Empfängerinnen und Empfänger sehen, bevor Sie den Versand testen oder ausführen.<br /> Weitere Informationen finden Sie in der <a href="../../channels/using/preparing-and-sending-a-push-notification.md#preparing-the-notification">ausführlichen Dokumentation</a>.<br /> Verfügbare Inhalte: Wenn Apps über einen längeren Zeitraum nicht geöffnet werden, können ihre Daten veraltet sein. Dies führt dazu, dass die Daten zu dem Zeitpunkt aktualisiert oder ersetzt werden müssen, zu dem eine Benutzerin oder ein Benutzer die App schließlich öffnet. Dies kann zu Verzögerungen bei der Verwendung der App führen. Mit der zusätzlichen Unterstützung verfügbarer Inhalte können Adobe Campaign-Benutzende ihre App „aufwecken“, damit bei der Bereitstellung einer Push-Benachrichtigung im Hintergrund die Daten aktualisiert werden, was eine größere Konsistenz und Kontrolle über das In-App-Erlebnis von Benutzenden ermöglicht.<br /> Veränderlicher Inhalt: Durch die zusätzliche Unterstützung veränderlicher Inhalte können Adobe Campaign-Benutzende jetzt ihre App-Erweiterungen nutzen, um den Inhalt oder die Darstellung eintreffender Push-Benachrichtigungen, die von Adobe Campaign gesendet werden, weiter zu ändern. Beispielsweise können Benutzende veränderliche Inhalte für Folgendes nutzen <br /> 
    <ul> 
     <li> In einem verschlüsselten Format gesendete Daten entschlüsseln </li> 
     <li> Bilder oder andere Mediendateien herunterladen und als Anhänge zu einer Benachrichtigung hinzufügen </li> 
     <li> Den Text oder Titel einer Benachrichtigung ändern </li> 
     <li> Eine Thread-Id zur einer Benachrichtigung hinzufügen </li> 
    </ul> Weitere Informationen zu den Funktionen „Inhalt verfügbar“ und „Veränderlicher Inhalt“ finden Sie in der <a href="../../channels/using/customizing-a-push-notification.md#change-the-notification-behavior-for-ios">ausführlichen Dokumentation</a>.<br /> <strong>Warnung:</strong> Für diese Aktualisierungen der Push-Benachrichtigungen müssen Kundinnen und Kunden ihre Apps aktualisieren. Weiterführende Informationen finden Sie in <a href="https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/configuring-mobile/push-payload.html?lang=de">dieser Technote</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Zeitzonenoptimierte Sendungen<br /> </td> 
   <td> Sie können wiederkehrende E-Mails, SMS und Push-Benachrichtigungen so terminieren, dass sie zu einem bestimmten Datum und einer bestimmten Uhrzeit in der Zeitzone jedes Empfängers bzw. jeder Empfängerin gesendet werden, ohne dass Sie mehrere Sendungen einrichten müssen. <br /> Lesen Sie für weiterführende Informationen das <a href="../../automating/using/scheduler.md">entsprechende Handbuch</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> Aktivierung der API-Signal-Aktivität<br /> </td> 
   <td> Es ist jetzt möglich, eine Signalaktivität für Workflows direkt in der Adobe Campaign Standard-API auszulösen.<br /> Weitere Informationen finden Sie in der <a href="/help/api/using/triggering-a-signal-activity.md">ausführlichen Dokumentation</a>.<br /> </td> 
  </tr> 
 </tbody> 
</table>

**Patches**

_Plattform_

* Die Profilsuche wurde optimiert, um die Performance zu verbessern.
* Die interne Kennung von Standard-Sicherheitsgruppen ermöglicht jetzt Standardbenutzern nur mehr schreibgeschützten Zugriff.

_E-Mails, SMS und Briefpost_

* Fehlerkorrektur – jetzt tritt kein Anzeigeproblem mehr auf, wenn Emojis in den Inhalt von Sendungen eingefügt werden.
* Fehlerkorrektur – Benutzer können jetzt nicht mehr auf Versandlogs zugreifen, wenn der Versand noch in Bearbeitung ist.
* Sie haben jetzt die Möglichkeit, mit der Aktivität **[!UICONTROL Planung]** den Versandzeitpunkt entsprechend der Zeitzone der Empfänger festzulegen.
* SMS: Die Option **[!UICONTROL Eingehende MO in Datenbank speichern]** wurde zu externen Konten hinzugefügt. Wird diese Option aktiviert, so werden alle eingehenden SMS-Nachrichten in der **inSMS**-Tabelle gespeichert.
* SMS: Dienste sind jetzt mit einem Ereignis anstatt einer Transaktionsvorlage verknüpft.
* SMS: Das standardmäßige SMTP-Verbindungs-Timeout wurde auf 30 Sekunden reduziert.

_Push-Benachrichtigungen_

* Fehlerkorrektur – Sendungen von Push-Benachrichtigungen können jetzt angehalten werden.
* In den erweiterten Optionen von Push-Benachrichtigungen wurde eine Option hinzugefügt, mit der Apps durch Push-Benachrichtigungen aktiviert werden können.
* Für das Push-Benachrichtigungsvorschau-Video wurde eine Unterbrechungsschaltfläche hinzugefügt.
* Die Push-Benachrichtigungsvorschau ist jetzt für unterschiedliche Geräte wie iPhone, Android und Tablets verfügbar.

_Berichte_

* Fehlerkorrektur – jetzt werden keine Raten mehr von über 100 % dargestellt.
* Fehlerkorrektur – jetzt können Benutzer Berichte im CSV-Format herunterladen.
* Eine neue **[!UICONTROL Bericht]**-Karte wurde auf der Startseite hinzugefügt.

_Workflows_

* Fehlerkorrektur – bei der Verwendung von Zusatzdaten in einer Abfrage und beim Hinzufügen von Alias mit Leerzeichen werden nicht-alphanumerische Zeichen jetzt durch &quot;_&quot; ersetzt.
* Fehlerkorrektur – der technische Workflow zur Berechnung von KPIs wird nicht mehr standardmäßig angehalten.

_Profile und Zielgruppen_

* Fehlerkorrektur – jetzt tritt kein Fehler mehr auf, wenn in einer Zielgruppe-Abfrage mehrere Filter hinzugefügt werden.
* Fehlerkorrektur – jetzt tritt kein Anzeigeproblem mehr auf, wenn ein Profilbild geändert wird.
* Eine QuickInfo wurde hinzugefügt, in dem nach der Zählung der Population einer Abfrage die exakte Anzahl dargestellt wird.
* Fehlerkorrektur – jetzt tritt kein Fehler mehr auf, wenn Benutzer versuchen, eine Zielgruppe auszuwählen oder ein Zielgruppe-Auswahl-Fenster zu schließen.
* Die Liste verfügbarer Funktionen wurde im Ausdruckseditor aktualisiert. Die Funktionen **FormatCurrency** und **ConvertCurrency** wurden entfernt.


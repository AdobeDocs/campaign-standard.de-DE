---
title: Integration mit Microsoft Dynamics 365 verwenden
description: Erfahren Sie, wie Sie die Integration von Microsoft Dynamics 365 mit Campaign Standard verwenden.
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: ht
source-git-commit: 6078a16c679d368dd85cecbb8b715e2de3da805a
workflow-type: ht
source-wordcount: '1186'
ht-degree: 100%

---


# Integration mit Microsoft Dynamics 365 verwenden

Diese Integration kann verschiedene Aufgaben übernehmen:

* **Eingehend**:

   * Einbinden von **Kontakten** aus Dynamics 365 in Campaign

   * **Benutzerdefinierte Entitäten**: Einbinden von benutzerdefinierten Tabellen aus Dynamics 365 in Campaign. Weiterführende Informationen finden Sie [in diesem Abschnitt](../../integrating/using/map-campaign-custom-resources-and-dynamics-365-custom-entities.md).

* **Ausgehend**: Einbinden von E-Mail-Marketing-Ereignissen aus ACS in D365 (E-Mail-Versand, Öffnung, Klick, Bounce)

* **Opt-out**: Bidirektionale Synchronisation des Opt-out-Status (z. B. Blockierungsliste)

Weitere Informationen zu den Datenflüssen finden Sie [in diesem Abschnitt](#data-flows).

## Adobe Campaign Standard-Anwendererlebnis

Wenn ein Kontakt in Dynamics 365 erstellt oder geändert (bzw. gelöscht, falls aktiviert) wird, wird er an Campaign gesendet.  Solche Kontakte werden im Bildschirm &quot;Profile&quot; in Campaign angezeigt und können in Marketing-Kampagnen gezielt ausgewählt werden.  Siehe Bildschirm &quot;Profile&quot; unten.

![](assets/MSdynamicsACS-usage1.png)

Wenn ein Opt-out-Attribut in Campaign geändert wird, spiegelt sich das in Dynamics 365 wider, wenn Sie die Opt-out-Konfiguration &quot;Synchronisation von Campaign mit Dynamics 365&quot; oder &quot;bidirektional&quot; gewählt haben und dieses Attribut korrekt zugeordnet wurde.

## Microsoft Dynamics 365-Anwendererlebnis

Die folgenden E-Mail-Marketing-Ereignisse werden für ausgehende Daten von Campaign an Dynamics 365 gesendet und in der Dynamics 365-Timeline-Ansicht als benutzerdefinierte Aktivitäten angezeigt:

* Adobe Campaign – E-Mail-Versand

* Adobe Campaign – E-Mail-Öffnung

* Adobe Campaign – E-Mail-URL-Klick

* Adobe Campaign – E-Mail-Bounce

Um die Timeline eines Kontakts anzuzeigen, navigieren Sie zu Ihrer Kontaktliste, indem Sie im Dropdown-Menü von Dynamics 365 &quot;Vertriebshub&quot; auswählen.  Wählen Sie dann in der linken Menüleiste &quot;Kontakte&quot; und danach einen Kontakt aus.

>[!NOTE]
>
>Die Adobe Campaign for Dynamics 365-App in AppSource muss in Ihrer Dynamics 365-Instanz installiert werden, damit sich die Ereignisse anzeigen lassen.

Unten sehen Sie eine Abbildung des Kontaktbildschirms für &quot;Dynamics User&quot;.  In der Timeline-Ansicht werden Sie feststellen, dass an &quot;Dynamics User&quot; eine E-Mail im Zusammenhang mit dem Kampagnennamen &quot;2019LoyaltyCamp&quot; und dem Versandnamen &quot;DM190&quot; gesendet wurde.  &quot;Dynamics User&quot; hat die E-Mail geöffnet und auch auf eine URL in der E-Mail geklickt. Beide Aktionen führten zur Erstellung von Ereignissen, die auch unten angezeigt werden.  In der rechten Ecke finden Sie die Relationship Assistant (RA)-Karte, die derzeit eine Aufgabe zum Nachverfolgen der angeklickten URL enthält.

![](assets/do-not-localize/MSdynamicsACS-usage4.png)

Unten finden Sie eine Nahaufnahme der Timeline-Ansicht für &quot;Dynamics User&quot;.

![](assets/do-not-localize/MSdynamicsACS-usage5.png)

Nachfolgend sehen Sie eine Nahaufnahme der Relationship Assistant (RA)-Karte.  Die AppSource-App enthält einen Workflow, der nach einem Adobe E-Mail-URL-Klick-Ereignis Ausschau hält.  Wenn dieses Ereignis eintritt, wird eine Aufgabe erstellt und ein Fälligkeitsdatum festgelegt.  Dadurch kann die Aufgabe in der RA-Karte angezeigt werden, was zusätzliche Transparenz gewährt.  Für Adobe E-Mail-Bounce-Ereignisse gibt es einen ähnlichen Workflow. Dabei wird eine Aufgabe hinzugefügt, mit der eine ungültige E-Mail-Adresse abgeglichen wird.  Dieser Workflow kann in der Lösung deaktiviert werden.

![](assets/do-not-localize/MSdynamicsACS-usage6.png)

Wenn Sie den Betreff des Versandereignisses auswählen, wird ein Formular ähnlich dem unten stehenden geöffnet.  Die Formulare für Öffnungs- und Bounce-Ereignisse sind ähnlich.

![](assets/do-not-localize/mirror_page_url_send.png)

Das Formular für E-Mail-URL-Klick-Ereignisse fügt ein zusätzliches Attribut für die angeklickte URL hinzu:

![](assets/do-not-localize/mirror_page_url_click.png)

Im Folgenden finden Sie eine Liste der Attribute inklusive einer Beschreibung:

* Betreff: Betreff des Ereignisses; bestehend aus der Kennung der Kampagne und der Versandkennung des E-Mail-Versands

* Besitzer: Der in den Schritten nach der Bereitstellung erstellte Anwender

* Bezug: Name des Kontakts

* Kampagnenname: Die Kennung der Kampagne in Campaign Standard

* Versandname: Die Versandkennung in Campaign Standard

* Datum von Gesendet/Geöffnet/Angeklickt/Bounce: Datum/Uhrzeit der Erstellung des Ereignisses

* Tracking-URL: URL, auf die geklickt wurde

* URL der Mirrorseite: Die URL zur Mirrorseite der E-Mail, die gesendet/geöffnet/angeklickt oder als Bounce zurückgesendet wurde

>[!NOTE]
>
>Die Gültigkeitsdauer der E-Mail-Mirrorseite kann im Konfigurationsbildschirm der entsprechenden Campaign-E-Mail-Kanal-Aktivität geändert werden (siehe [Parameter für den Gültigkeitszeitraum](../../administration/using/configuring-email-channel.md#validity-period-parameters)).

>[!NOTE]
>
>Bei Opt-outs: Falls ein Opt-out-Attribut in Dynamics 365 geändert wird, spiegelt sich das in Campaign wider, wenn Sie die Opt-out-Konfiguration &quot;Synchronisation von Dynamics 365 mit Campaign&quot; oder &quot;bidirektional&quot; gewählt und dieses Attribut korrekt zugeordnet haben.

## Datenflüsse {#data-flows}

### Eingang von Kontakten und benutzerdefinierten Entitäten

Neue und aktualisierte (und gelöschte, falls aktiviert) Datensätze werden von der Kontakttabelle in Dynamics 365 an die Profiltabelle in Campaign gesendet.

Tabellen-Mapping kann so konfiguriert werden, dass die Tabellenattribute in Dynamics 365 den Tabellenattributen in Campaign zugeordnet werden. Das Tabellen-Mapping kann nach Bedarf geändert werden, um Attribute hinzuzufügen bzw. zu entfernen.

Die erste Ausführung des Datenflusses dient der Übertragung aller zugeordneten Datensätze, einschließlich der als &quot;inaktiv&quot; gekennzeichneten Datensätze. Anschließend verarbeitet die Integration nur inkrementelle Aktualisierungen. Eine Ausnahme bildet die Filterkonfiguration. Es können grundlegende, attributbasierte Filterregeln konfiguriert werden, um zu bestimmen, welche Datensätze mit Campaign synchronisiert werden sollen.

Grundlegende Ersetzungsregeln können so konfiguriert werden, dass ein Attributwert durch einen anderen Wert ersetzt wird (z. B. &quot;grün&quot; für &quot;#00FF00&quot;, &quot;F&quot; für 1 usw.).

Je nach Datensatzvolumen muss möglicherweise Ihr Campaign-SFTP-Speicher für die erste Datenübertragung verwendet werden.  Siehe Abschnitt &quot;Erste Datenübertragung&quot;.

Das Profiltabellenattribut &quot;externalId&quot; in Campaign muss mit dem Kontaktattribut &quot;contactId&quot; in Dynamics 365 gefüllt sein, damit der Eingang der Kontakte funktioniert. Benutzerdefinierte Entitäten in Campaign müssen ebenfalls mit einem eindeutigen ID-Attribut in Dynamics 365 gefüllt werden. Dieses Attribut kann jedoch in jedem benutzerdefinierten Entitätsattribut in Campaign gespeichert werden (d. h. es muss nicht &quot;externalId&quot; sein).

>[!NOTE]
>
>Beim Eingang benutzerdefinierter Entitäten muss für synchronisierte benutzerdefinierte Entitäten die Änderungsverfolgung innerhalb von Dynamics 365 aktiviert werden.

### Ereignisfluss beim E-Mail-Marketing

E-Mail-Marketing-Ereignisse werden von Campaign an Dynamics 365 gesendet, um in der Timeline-Ansicht angezeigt zu werden.

Unterstützte Marketing-Ereignistypen:
* Versand: E-Mail an den Empfänger gesendet
* Öffnung: E-Mail durch Empfänger geöffnet
* Klick: Vom Empfänger angeklickte URL innerhalb der E-Mail
* Bounce: E-Mail an Empfänger erfuhr einen Hardbounce

Die folgenden Ereignisattribute werden in D365 angezeigt:
* Name der Marketing-Kampagne
* Name des E-Mail-Versands
* Zeitstempel
* URL der E-Mail-Mirrorseite
* URL angeklickt (nur auf Klick-Ereignisse)

E-Mail-Marketing-Ereignisse können nach Typ (Versand, Öffnung, Klick, Bounce) aktiviert bzw. deaktiviert werden, sodass nur die von Ihnen ausgewählten Ereignistypen an Dynamics 365 übergeben werden.

### Opt-out-Fluss

Die Opt-out-Werte (z. B. Blockierungsliste) werden zwischen den Systemen synchronisiert. Während des Einstiegs (Onboarding) stehen folgende Optionen zur Auswahl:
* Dynamics 365 ist die &quot;Source of Truth&quot; für Opt-outs: Opt-out-Attribute werden in eine Richtung von Dynamics 365 zu Campaign Standard synchronisiert.
* Campaign Standard ist die &quot;Source of Truth&quot; für Opt-outs: Opt-out-Attribute werden in einer Richtung von Campaign Standard zu Dynamics 365 synchronisiert.
* Dynamics 365 UND Campaign Standard sind beide &quot;Source of Truth&quot;: Opt-out-Attribute werden in beide Richtungen zwischen Campaign Standard und Dynamics 365 synchronisiert.

Wenn Sie über einen separaten Prozess zum Verwalten der Opt-out-Synchronisation zwischen den Systemen verfügen, kann alternativ der Opt-out-Datenfluss der Integration deaktiviert werden.

Das Mapping des Opt-out-Flusses muss vom Kunden festgelegt werden, da die Geschäftsanforderungen zwischen den Unternehmen unterschiedlich sein können.  In Campaign können nur die OOTB-Opt-out-Attribute für das Opt-out-Mapping verwendet werden:
* denyList
* denyListEmail
* denyListFax
* denyListMobile
* denyListPhone
* denyListPostalMail
* denyListPushnotification
* ccpaOptOut

In Dynamics 365 haben die meisten Opt-out-Felder das Präfix &quot;donot&quot;. Sie können jedoch auch andere Attribute zu Opt-out-Zwecken nutzen, solange die Datentypen kompatibel sind.

### Erste Datenübertragung

Dynamics 365-Tabellen mit mehr als 500.000 Datensätzen müssen in Ihren Campaign-SFTP-Speicher exportiert werden, damit sie über den Campaign-Workflow importiert werden können.

Bei der ersten Datenübertragung handelt es sich um eine einmalige, dateibasierte Datenübertragung. Nach der Datenübertragung verwendet die Integration APIs für die inkrementellen Aktualisierungen.

---
title: Verwenden der Microsoft Dynamics 365-Integration
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
translation-type: tm+mt
source-git-commit: 6078a16c679d368dd85cecbb8b715e2de3da805a
workflow-type: tm+mt
source-wordcount: '1186'
ht-degree: 44%

---


# Verwenden der Microsoft Dynamics 365-Integration

Diese Integration kann verschiedene Aufgaben übernehmen:

* **Fortschritt**:

   * Integration von **Kontakten** aus Dynamics 365 in die Kampagne

   * **Benutzerdefinierte Entitäten**: Fügen Sie benutzerdefinierte Tabellen von Dynamics 365 in die Kampagne ein. Weiterführende Informationen finden Sie [in diesem Abschnitt](../../integrating/using/map-campaign-custom-resources-and-dynamics-365-custom-entities.md).

* **Fortschritte**: E-Mail-Marketing-Ereignis von ACS in D365 einbinden (E-Mail senden, öffnen, klicken, Absprung)

* **Ausschluss**: Bidirektionaler Abmeldestatus (z. B. Blockierungsliste)

Weitere Informationen zu den Datenflüssen finden Sie [in diesem Abschnitt](#data-flows).

## Adobe Campaign Standard-Anwendererlebnis

Wenn ein Kontakt in Dynamics 365 erstellt oder geändert (bzw. gelöscht, falls aktiviert) wird, wird er an die Kampagne gesendet.  Solche Kontakte werden im Bildschirm &quot;Profile&quot; in Campaign angezeigt und können in Marketing-Kampagnen gezielt ausgewählt werden.  Siehe Bildschirm &quot;Profile&quot; unten.

![](assets/MSdynamicsACS-usage1.png)

Wenn ein Ausschluss-Attribut in der Kampagne geändert wird, wird es in Dynamics 365 angezeigt, wenn Sie die Kampagne-zu-Dynamics 365- oder bidirektionale Opt-out-Konfiguration ausgewählt haben und das entsprechende Attribut korrekt zugeordnet wurde.

## Microsoft Dynamics 365-Anwendererlebnis

Die folgenden E-Mail-Marketing-Ereignis werden von Kampagne zu Dynamics 365 gesendet und in der Ansicht Dynamics 365 Timeline als benutzerdefinierte Aktivitäten angezeigt:

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

* Zu: Name der Kontaktperson

* Kampagnenname: Die Kennung der Kampagne in Campaign Standard

* Versandname: Die Versandkennung in Campaign Standard

* Datum von Gesendet/Geöffnet/Angeklickt/Bounce: Datum/Uhrzeit der Erstellung des Ereignisses

* Tracking-URL: URL, auf die geklickt wurde

* URL der Mirrorseite: Die URL zur Mirrorseite der E-Mail, die gesendet/geöffnet/angeklickt oder als Bounce zurückgesendet wurde

>[!NOTE]
>
>Die Gültigkeitsdauer der E-Mail-Mirrorseite kann im Konfigurationsbildschirm der entsprechenden Kampagne-E-Mail-Kanal-Aktivität geändert werden (siehe [Gültigkeitszeitparameter](../../administration/using/configuring-email-channel.md#validity-period-parameters)).

>[!NOTE]
>
>Bei Opt-outs: Falls ein Opt-out-Attribut in Dynamics 365 geändert wird, spiegelt sich das in Campaign wider, wenn Sie die Opt-out-Konfiguration &quot;Synchronisation von Dynamics 365 mit Campaign&quot; oder &quot;bidirektional&quot; gewählt und dieses Attribut korrekt zugeordnet haben.

## Datenfluss {#data-flows}

### Kontakt- und benutzerspezifische Entitätsaktualisierung

Neue und aktualisierte (und gelöschte, falls aktiviert) Datensätze werden von der Kontakttabelle Dynamics 365 an die Tabelle Kampagne Profil gesendet.

Tabellenzuordnungen können so konfiguriert werden, dass Dynamics 365-Tabellenattribute den Tabellenattributen der Kampagne zugeordnet werden. Die Tabellenzuordnungen können nach Bedarf geändert werden, um Attribute hinzuzufügen/zu entfernen.

Die anfängliche Ausführung des Datenflusses ist so ausgelegt, dass alle zugeordneten Datensätze, einschließlich der als &quot;inaktiv&quot; gekennzeichneten Datensätze, übertragen werden; Anschließend verarbeitet die Integration nur inkrementelle Aktualisierungen. Eine Ausnahme bildet die Konfiguration eines Filters. Es können einfache, attributbasierte Filterregeln konfiguriert werden, um zu bestimmen, welche Datensätze mit der Kampagne synchronisiert werden sollen.

Grundlegende Ersatzregeln können so konfiguriert werden, dass ein Attributwert durch einen anderen Wert ersetzt wird (z. B. &quot;grün&quot;für &quot;#00FF00&quot;, &quot;F&quot;für 1 usw.).

Je nach Datensatzvolumen muss Ihre Kampagne-SFTP-Datenspeicherung möglicherweise für die anfängliche Datenübertragung verwendet werden.  Siehe Abschnitt &quot;Ursprüngliche Datenübertragung&quot;.

Das Tabellenattribut externalId des Kampagne-Profils muss mit dem Kontaktattribut contactId des Dynamics 365 ausgefüllt werden, damit die Kontaktanmeldung funktioniert. Benutzerdefinierte Entitäten der Kampagne müssen auch mit einem Dynamics 365-Attribut für eindeutige ID ausgefüllt werden. Dieses Attribut kann jedoch in jeder beliebigen Kampagne des benutzerdefinierten Entitätsattributs gespeichert werden (d. h. muss nicht externalId sein).

>[!NOTE]
>
>Bei der benutzerdefinierten Entitätseingabe muss die Änderungsverfolgung in Dynamics 365 für synchronisierte benutzerdefinierte Entitäten aktiviert werden.

### E-Mail-Marketing-Ereignis-Fluss

E-Mail-Marketing-Ereignis werden von der Kampagne an Dynamics 365 gesendet, um in der Timeline-Ansicht angezeigt zu werden.

Unterstützte Marketing-Ereignistyp:
* Senden - E-Mail an Empfänger
* Öffnen - E-Mail durch Empfänger geöffnet
* Klicken - URL innerhalb der E-Mail, die vom Empfänger angeklickt wird
* Absprung - E-Mail an Empfänger hat einen harten Absprung erlebt

Die folgenden Ereignis-Attribute werden in D365 angezeigt:
* Name der Marketing-Kampagne
* Name des E-Mail-Versands
* Zeitstempel
* URL der E-Mail-Mirrorseite
* URL angeklickt (nur auf Ereignis klicken)

E-Mail-Marketing-Ereignis können nach Typ aktiviert/deaktiviert werden (Senden, Öffnen, Klicken, Absprung), sodass nur die ausgewählten Ereignistyp an Dynamics 365 übergeben werden.

### Abmeldefluss

Ausschlusswerte (z. B. Blockierungslisten) werden zwischen Systemen synchronisiert. Sie haben die folgenden Optionen, die Sie beim Einsteigen wählen können:
* Dynamics 365 ist die &quot;Source of Truth&quot; für Opt-outs: Opt-out-Attribute werden in eine Richtung von Dynamics 365 zu Campaign Standard synchronisiert.
* Campaign Standard ist die &quot;Source of Truth&quot; für Opt-outs: Opt-out-Attribute werden in einer Richtung von Campaign Standard zu Dynamics 365 synchronisiert.
* Dynamik 365 UND Campaign Standard sind beide Wahrheitsquellen: Ausschluss-Attribute werden bidirektional zwischen Campaign Standard und Dynamics 365 synchronisiert.

Alternativ kann der Ausschluss-Datenfluss der Integration deaktiviert werden, wenn Sie über einen separaten Prozess zur Verwaltung der Abmeldesynchronisierung zwischen den Systemen verfügen.

Die Abmeldezuordnung ist vom Kunden anzugeben, da die Geschäftsanforderungen je nach Firma unterschiedlich sein können.  Auf der Kampagne können nur die OOTB-Ausschluss-Attribute für die Abmeldezuordnung verwendet werden:
* Blockierungsliste
* denyListEmail
* denyListFax
* denyListMobile
* denyListPhone
* denyListPostalMail
* denyListPushnotification
* ccpaOptOut

In Dynamics 365 haben die meisten Ausschluss-Felder das Präfix &quot;donot&quot;. Sie können jedoch auch andere Attribute für Ausschluss-Zwecke verwenden, wenn die Datentypen kompatibel sind.

### Ursprüngliche Datenübertragung

Dynamics 365 Tabellen über 500.000 Datensätze müssen in Ihre Kampagne SFTP-Datenspeicherung exportiert werden, um über den Arbeitsablauf für Kampagnen importiert zu werden.

Bei der ersten Datenübertragung handelt es sich um eine einmalige, dateibasierte Datenübertragung. Nach der Datenübertragung verwendet die Integration APIs für die inkrementellen Aktualisierungen.

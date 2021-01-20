---
title: Integration mit Microsoft Dynamics 365 verwenden
description: Erfahren Sie, wie Sie die Integration von Microsoft Dynamics 365 mit Campaign Standard verwenden.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
translation-type: tm+mt
source-git-commit: fe5d40235abc33c0ea7e929cd2e69b7030cea0b1
workflow-type: tm+mt
source-wordcount: '1607'
ht-degree: 57%

---


# Verwenden der Microsoft Dynamics 365-Integration

Es gibt mehrere Datenflüsse, die die Adobe Campaign Standard Integration mit Microsoft Dynamics 365 durchführt. Diese Flüsse sind in [dieser Seite](../../integrating/using/d365-acs-self-service-app-workflows.md) detailliert.

Weitere Informationen zu den Datenflüssen finden Sie weiter unten in diesem Dokument im Abschnitt [Datenflüsse](#data-flows).

## Adobe Campaign Standard-Benutzererfahrung

Wenn ein Kontakt in Microsoft Dynamics 365 erstellt, geändert oder gelöscht wird (falls gelöscht), wird er an den Campaign Standard gesendet. Solche Kontakte werden im Bildschirm &quot;Profile&quot; in Campaign angezeigt und können in Marketing-Kampagnen gezielt ausgewählt werden. Siehe Bildschirm &quot;Profile&quot; unten.

![](assets/MSdynamicsACS-usage1.png)

Wenn ein Ausschluss-Attribut in der Kampagne geändert wird, wird es in Dynamics 365 angezeigt, wenn Sie die Option **Unidirektionale (Kampagne zu Microsoft Dynamics 365)** oder **Bidirektionale** Opt-out-Konfiguration ausgewählt haben und wenn Sie dieses Attribut korrekt zugeordnet haben.

## Microsoft Dynamics 365

Die folgenden E-Mail-Marketing-Ereignisse werden von Kampagne zu Dynamics 365 gesendet und in der Microsoft Dynamics 365-Zeitschiene-Ansicht als benutzerdefinierte Aktivitäten angezeigt:

* Adobe Campaign – E-Mail-Versand

* Adobe Campaign – E-Mail-Öffnung

* Adobe Campaign – E-Mail-URL-Klick

* Adobe Campaign – E-Mail-Bounce

Um die Timeline eines Kontakts anzuzeigen, navigieren Sie zu Ihrer Kontaktliste, indem Sie im Dropdown-Menü von Dynamics 365 &quot;Vertriebshub&quot; auswählen. Wählen Sie dann in der linken Menüleiste &quot;Kontakte&quot; und danach einen Kontakt aus.

>[!NOTE]
>
>Die App **Adobe Campaign für Microsoft Dynamics 365** in AppSource muss in Ihrer Microsoft Dynamics 365-Instanz installiert werden, um diese Ereignisse Ansicht. [Weitere Informationen](../../integrating/using/d365-acs-configure-d365.md#install-appsource-app).

Unten sehen Sie eine Momentaufnahme des Kontaktbildschirms für &quot;Dynamics User&quot;. In der Timeline-Ansicht werden Sie feststellen, dass Dynamics User eine E-Mail mit dem Namen der Kampagne &quot;2019LoyaltyCamp&quot;und dem Namen des Versands &quot;DM190&quot;gesendet wurde. &quot;Dynamics User&quot; hat die E-Mail geöffnet und auch auf eine URL in der E-Mail geklickt. Beide Aktionen führten zur Erstellung von Ereignissen, die auch unten angezeigt werden.  In der rechten Ecke finden Sie die Relationship Assistant (RA)-Karte, die derzeit eine Aufgabe zum Nachverfolgen der angeklickten URL enthält.

![](assets/do-not-localize/MSdynamicsACS-usage4.png)

Unten finden Sie eine Nahaufnahme der Timeline-Ansicht für &quot;Dynamics User&quot;.

![](assets/do-not-localize/MSdynamicsACS-usage5.png)

Nachfolgend sehen Sie eine Nahaufnahme der Relationship Assistant (RA)-Karte. Die AppSource-App enthält einen Workflow, der nach einem Adobe E-Mail-URL-Klick-Ereignis Ausschau hält. Wenn dieses Ereignis eintritt, wird eine Aufgabe erstellt und ein Fälligkeitsdatum festgelegt. Dadurch kann die Aufgabe in der RA-Karte angezeigt werden, was zusätzliche Transparenz gewährt. Für Adobe E-Mail-Bounce-Ereignisse gibt es einen ähnlichen Workflow. Dabei wird eine Aufgabe hinzugefügt, mit der eine ungültige E-Mail-Adresse abgeglichen wird. Dieser Workflow kann in der Lösung deaktiviert werden.

![](assets/do-not-localize/MSdynamicsACS-usage6.png)

Wenn Sie den Betreff des Versandereignisses auswählen, wird ein Formular ähnlich dem unten stehenden geöffnet. Die Formulare für Öffnungs- und Bounce-Ereignisse sind ähnlich.

![](assets/do-not-localize/mirror_page_url_send.png)

Das Formular für E-Mail-URL-Klick-Ereignisse fügt ein zusätzliches Attribut für die angeklickte URL hinzu:

![](assets/do-not-localize/mirror_page_url_click.png)

Im Folgenden finden Sie eine Liste der Attribute inklusive einer Beschreibung:

* **Betrifft**: Gegenstand des Ereignisses; bestehend aus Kampagnen-ID und Versand-ID des E-Mail-Versands

* **Inhaber**: Der in den Schritten nach der Bereitstellung erstellte Anwendungsbenutzer

* **Zu**: Name der Kontaktperson

* **Name** der Kampagne: Die Kampagnen-ID in Campaign Standard

* **Name** des Versands: Die Versand-ID in Campaign Standard

* **Datum gesendet/geöffnet/angeklickt/abgeschnitten**: Datum/Uhrzeit der Erstellung des Ereignisses

* **Tracking-URL**: URL, auf die geklickt wurde

* **Mirrorseiten-URL**: Die URL zur Mirrorseite der E-Mail, die gesendet/geöffnet/angeklickt/abgeschnitten wurde. Die Gültigkeitsdauer der E-Mail-Mirrorseite kann im Konfigurationsbildschirm der entsprechenden Kampagne-E-Mail-Kanal-Aktivität geändert werden. [Weitere Informationen](../../administration/using/configuring-email-channel.md#validity-period-parameters).

>[!NOTE]
>
>Wenn ein Opt-out-Attribut in Microsoft Dynamics 365 geändert wird, wird es in der Kampagne angezeigt, wenn Sie die Abmeldekonfiguration **Unidirektional (Kampagne zu Microsoft Dynamics 365)** oder **Bidirektional** ausgewählt haben und wenn Sie dieses Attribut korrekt zugeordnet haben.

## Datenflüsse {#data-flows}

### Kontakt- und benutzerdefinierte Entitätsdaten

Neue, aktualisierte und gelöschte Datensätze (Hinweis: gelöschte muss aktiviert sein) werden von der Microsoft Dynamics 365 Kontakttabelle an die Tabelle Kampagne Profil gesendet.

Tabellenzuordnungen können in der Benutzeroberfläche der Integrationsanwendung konfiguriert werden, um Microsoft Dynamics 365-Tabellenattribute Kampagne-Tabellenattributen zuzuordnen. Das Tabellen-Mapping kann nach Bedarf geändert werden, um Attribute hinzuzufügen bzw. zu entfernen.

Die anfängliche Ausführung des Datenflusses ist so ausgelegt, dass alle zugeordneten Datensätze, einschließlich der als &quot;inaktiv&quot; gekennzeichneten Datensätze, übertragen werden; Anschließend verarbeitet die Integration nur inkrementelle Aktualisierungen. Eine Ausnahme bilden Daten, die wiedergegeben werden oder für die ein Filter konfiguriert ist. Es können einfache, attributbasierte Filterregeln konfiguriert werden, um zu bestimmen, welche Datensätze mit der Kampagne synchronisiert werden sollen.

Grundlegende Ersatzregeln können in der Benutzeroberfläche der Integrationsanwendung konfiguriert werden, um einen Attributwert durch einen anderen Wert zu ersetzen (z. B. &quot;grün&quot;für &quot;#00FF00&quot;, &quot;F&quot;für 1 usw.).

Je nach Datensatzvolumen muss möglicherweise Ihr Campaign-SFTP-Speicher für die erste Datenübertragung verwendet werden. [Weitere Informationen](#initial-data-transfer).

Das Profiltabellenattribut &quot;externalId&quot; in Campaign muss mit dem Kontaktattribut &quot;contactId&quot; in Dynamics 365 gefüllt sein, damit der Eingang der Kontakte funktioniert. Benutzerdefinierte Entitäten in Campaign müssen ebenfalls mit einem eindeutigen ID-Attribut in Dynamics 365 gefüllt werden. Dieses Attribut kann jedoch in jedem benutzerdefinierten Entitätsattribut in Campaign gespeichert werden (d. h. es muss nicht &quot;externalId&quot; sein).

>[!NOTE]
>
>Beim Eingang benutzerdefinierter Entitäten muss für synchronisierte benutzerdefinierte Entitäten die Änderungsverfolgung innerhalb von Dynamics 365 aktiviert werden.

#### Benutzerdefinierte Entitäten

Die [Integration von Adobe Campaign Standard mit Microsoft Dynamics 365](../../integrating/using/d365-acs-get-started.md) unterstützt benutzerdefinierte Entitäten und ermöglicht die Synchronisation von benutzerdefinierten Entitäten in Dynamics 365 mit entsprechenden benutzerdefinierten Ressourcen in Campaign.

Die neuen Daten in den benutzerdefinierten Ressourcen können für verschiedene Zwecke verwendet werden, einschließlich Segmentierung und Personalisierung.

Die Integration unterstützt sowohl verknüpfte als auch nicht verknüpfte Tabellen. Die Verknüpfung wird auf bis zu drei Ebenen unterstützt (d. h. Level1->Level2->Level3).

>[!IMPORTANT]
>
>Wenn ein benutzerdefinierter Ressourcendatensatz in Campaign personenbezogene Daten enthält, gelten besondere Empfehlungen. Weiterführende Informationen finden Sie [in diesem Abschnitt](../../integrating/using/d365-acs-notices-and-recommendations.md#acs-msdyn-manage-data).


Bei der Konfiguration benutzerdefinierter Entitätsdatenflüsse ist Folgendes zu beachten:

* Die Erstellung und Änderung von benutzerdefinierten Campaign-Ressourcen sind heikle Aufgaben, die nur von erfahrenen Benutzern durchgeführt werden können.
* Bei benutzerdefinierten Entitätsdatenflüssen muss für synchronisierte benutzerdefinierte Entitäten die Änderungsverfolgung innerhalb von Dynamics 365 aktiviert werden.
* Wenn ein übergeordneter und ein verknüpfter untergeordneter Datensatz in Dynamics 365 aufgrund der parallelen Verarbeitung der Integration nahezu zur gleichen Zeit erstellt werden, besteht eine geringe Wahrscheinlichkeit, dass ein neuer untergeordneter Datensatz vor seinem übergeordneten Datensatz in Campaign geschrieben wird.

* Wenn das übergeordnete und das untergeordnete Element in Campaign mithilfe der Option **Einfache Relation mit Kardinalität 1** verknüpft sind, bleibt der untergeordnete Datensatz ausgeblendet und kann (über die Benutzeroberfläche oder API) nicht aufgerufen werden, bis der übergeordnete Datensatz in Campaign eintrifft.

* (Angenommen, **Einfache Relation mit Kardinalität 1** wird in Campaign verwendet.) Wenn der untergeordnete Datensatz in Dynamics 365 aktualisiert oder gelöscht wird und diese Änderung in Campaign geschrieben wird, bevor der übergeordnete Datensatz in Campaign angezeigt wird (nicht wahrscheinlich, aber möglich), wird diese Aktualisierung oder Löschung nicht in Campaign verarbeitet und ein Fehler ausgegeben. Im Falle einer Aktualisierung muss der betreffende Datensatz erneut in Dynamics 365 aktualisiert werden, um den aktualisierten Datensatz zu synchronisieren. Im Falle der Löschung muss der betreffende Datensatz in Campaign gesondert behandelt werden, da in Dynamics 365 kein Datensatz mehr zum Löschen oder Aktualisieren vorhanden ist.

* Wenn Sie in eine Situation geraten, in der Sie glauben, versteckte untergeordnete Datensätze zu haben und nicht darauf zugreifen zu können, können Sie den Kardinalität-Relationstyp vorübergehend in **Einfache Relation mit Kardinalität 0 oder 1** ändern, um auf diese Datensätze zuzugreifen.

Eine umfassendere Übersicht über benutzerdefinierte Campaign-Ressourcen finden Sie [in diesem Abschnitt](../../developing/using/key-steps-to-add-a-resource.md).

### Email Marketing Ereignis Flow{#email-marketing-event-flow}

E-Mail-Marketing-Ereignis werden von der Kampagne an Microsoft Dynamics 365 gesendet, um in der Timeline-Ansicht angezeigt zu werden.

Unterstützte Marketing-Ereignistypen:
* Versand: E-Mail an den Empfänger gesendet
* Öffnung: E-Mail durch Empfänger geöffnet
* Klick: Vom Empfänger angeklickte URL innerhalb der E-Mail
* Bounce: E-Mail an Empfänger erfuhr einen Hardbounce

Die folgenden Ereignis-Attribute werden in Dynamics 365 angezeigt:
* Name der Marketing-Kampagne
* Name des E-Mail-Versands
* Zeitstempel
* URL der E-Mail-Mirrorseite
* URL angeklickt (nur auf Klick-Ereignisse)

E-Mail-Marketing-Ereignisse können nach Typ (Versand, Öffnung, Klick, Bounce) aktiviert bzw. deaktiviert werden, sodass nur die von Ihnen ausgewählten Ereignistypen an Dynamics 365 übergeben werden.

### Ausschluss-Fluss {#opt-out-flow}

Die Opt-out-Werte (z. B. Blockierungsliste) werden zwischen den Systemen synchronisiert. Während des Einstiegs (Onboarding) stehen folgende Optionen zur Auswahl:

* **Unidirektional (Microsoft Dynamics 365 zur Kampagne)**: Dynamics 365 ist eine Quelle der Wahrheit für Opt-out-Möglichkeiten. Ausschlussattribute werden in einer Richtung von Dynamics 365 auf den Campaign Standard synchronisiert.&quot;
* **Unidirektional (Kampagne zu Microsoft Dynamics 365)**: Campaign Standard ist die Quelle der Wahrheit für Opt-out. Ausschlussattribute werden von Campaign Standard zu Dynamics 365 in eine Richtung synchronisiert.
* **Bidirektional**: Dynamics 365 UND Campaign Standard sind beide Wahrheitsquellen. Ausschlussattribute werden bidirektional zwischen Campaign Standard und Dynamics 365 synchronisiert

Wenn Sie über einen separaten Prozess zum Verwalten der Opt-out-Synchronisation zwischen den Systemen verfügen, kann alternativ der Opt-out-Datenfluss der Integration deaktiviert werden.

>[!NOTE]
>
>In der Benutzeroberfläche der Integrationsanwendung werden die Anwendungsfälle **Unidirektional (Microsoft Dynamics 365 zu Kampagne)** und **Bidirektional** für die Abmeldung konfiguriert. [Weitere Informationen](../../integrating/using/d365-acs-self-service-app-data-sync.md#opt-in-out-wf).
>
>Der Fall für das Abmeldeverfahren **Unidirektional (Kampagne zu Microsoft Dynamics 365)** ist eine Ausnahme. Es wird im Ingress-Workflow (Kontakt mit Profil) konfiguriert.


Das Mapping des Opt-out-Flusses muss vom Kunden festgelegt werden, da die Geschäftsanforderungen zwischen den Unternehmen unterschiedlich sein können. In Campaign können nur die OOTB-Opt-out-Attribute für das Opt-out-Mapping verwendet werden:

* denyList
* denyListEmail
* denyListFax
* denyListMobile
* denyListPhone
* denyListPostalMail
* denyListPushnotification
* ccpaOptOut

In Dynamics 365 haben die meisten Ausschluss-Felder das Präfix &quot;donot&quot;. Sie können jedoch auch andere Attribute für Ausschluss-Zwecke verwenden, wenn die Datentypen kompatibel sind.

### Erste Datenübertragung {#initial-data-transfer}

Die anfängliche Datenübertragung kann eine Weile dauern, je nachdem, wie viele Datensätze Sie von Microsoft Dynamics 365 abrufen. Nach der ersten Datenübertragung werden die inkrementellen Aktualisierungen von der Integration übernommen.

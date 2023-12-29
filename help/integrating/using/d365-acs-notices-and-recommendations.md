---
title: Management von Campaign- und Microsoft Dynamics 365-Daten
description: Erfahren Sie, wie Campaign Standard und Microsoft Dynamics 365 gemeinsame Daten verwalten.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
feature: Microsoft CRM Integration
role: Data Architect
level: Experienced
exl-id: aab6f005-f3da-4c0b-b856-da8504e611dc
source-git-commit: 17522f4df86c7fb46593472316d57b4ba4acee2b
workflow-type: tm+mt
source-wordcount: '2526'
ht-degree: 100%

---

# Best Practices und Einschränkungen {#acs-msdyn-best-practices}

## Verwalten von Daten {#acs-msdyn-manage-data}

Bei der Synchronisation von Kontakten und benutzerdefinierten Entitäten verwendet diese Integration **Microsoft Dynamics 365 als &quot;Source of Truth&quot;**. Änderungen an synchronisierten Attributen sollten in Dynamics 365 und nicht in Adobe Campaign Standard vorgenommen werden. Wenn Änderungen in Campaign vorgenommen werden, können diese bei der Synchronisation in Campaign überschrieben werden, da die Synchronisation in eine Richtung verläuft.

Die Integration kann optional so konfiguriert werden, dass beim Löschen eines Kontakts in Dynamics 365 Aufrufe zum Löschen von Profilen an Campaign ausgegeben werden, um die Datenintegrität zu bewahren. Der Löschvorgang eines Profils unterscheidet sich von einem datenschutzbezogenen Löschvorgang. Durch einen datenschutzbezogenen Löschvorgang in Campaign werden der Campaign-Profildatensatz und die zugehörigen Protokolleinträge entfernt, wohingegen bei einem regulären Profillöschvorgang nur der Campaign-Profildatensatz gelöscht wird, in den Campaign-Protokollen aber restliche Daten verbleiben. Wenn die Funktion zum Löschen von Profilen in der Integration aktiviert ist, müssen weitere Schritte ausgeführt werden, um Datenschutzanfragen für betroffene Personen ordnungsgemäß zu verarbeiten. Beachten Sie die Schritte im Abschnitt [Datenschutz](#manage-privacy-requests) weiter unten.

## Datenschutz{#acs-msdyn-manage-privacy}

Mit dieser Integration lassen sich Endbenutzerdaten zwischen Microsoft Dynamics 365 und Adobe Campaign Standard übertragen. Endbenutzerdaten enthalten personenbezogene Informationen.  Als Datenverantwortlicher ist Ihr Unternehmen zur Einhaltung der für die Erhebung und Nutzung personenbezogener Daten geltenden Datenschutzgesetze und -vorschriften verpflichtet.

Mit dieser Integration lassen sich Endbenutzerdaten (darunter auch personenbezogene Daten, sofern diese in Ihren Endbenutzerdaten enthalten sind) zwischen Microsoft Dynamics 365 und Adobe Campaign Standard übertragen. Als Datenverantwortlicher ist Ihr Unternehmen zur Einhaltung der für die Erhebung und Nutzung personenbezogener Daten geltenden Datenschutzgesetze und -vorschriften verpflichtet.

Bei der Integration werden keine datenschutzbezogenen Löschvorgänge für betroffene Personen ausgegeben (z. B. DSGVO) oder andere Datenschutzanfragen bearbeitet (mit Ausnahme von Opt-out). Wenn Sie Datenschutzanfragen bearbeiten, sollten Sie dies unabhängig voneinander in Microsoft Dynamics 365 und in Campaign (über den Adobe Experience Platform Privacy Service) tun.

Wenn Sie die Integration so konfiguriert haben, dass beim Löschen eines Kontakts in Dynamics 365 reguläre Aufrufe zum Löschen von Profilen an Campaign gesendet werden, sollten Sie die folgenden Schritte ausführen. Stellen Sie sicher, dass während dieses Vorgangs keine Aktualisierungen am betreffenden Datensatz vorgenommen werden.

1. Datenschutzbezogene Löschanfrage an [Adobe Experience Platform Privacy Service](https://developer.adobe.com/experience-platform-apis/references/privacy-service) senden

1. Anfrage bis zum erfolgreichen Abschluss überwachen

1. Überprüfen, ob sich der Datensatz nicht mehr in Ihrer Campaign-Instanz befindet

1. (Kurz danach) die datenschutzbezogene Löschung in Dynamics 365 veranlassen

1. Überprüfen, ob der Datensatz aus beiden Systemen entfernt wurde


>[!IMPORTANT]
>
>Wenn ein benutzerdefinierter Campaign-Ressourcendatensatz personenbezogene Daten enthält, die auch in Campaign verwendet werden, sollte dieser Datensatz mit einem entsprechenden Campaign-Profildatensatz verknüpft werden (entweder direkt oder über eine andere benutzerspezifische Ressource), sodass ein datenschutzbezogener Löschvorgang im Profildatensatz auch den verknüpften benutzerspezifischen Ressourcendatensatz mit personenbezogenen Daten löschen kann. Die Verknüpfungs- und Löschoptionen zwischen den Entitäten müssen so konfiguriert sein, dass eine solche kaskadierte Löschung der verknüpften Datensätze möglich wird. Personenbezogene Daten sollten nicht in benutzerdefinierte Ressourcen eingegeben werden, die nicht mit dem Profil verknüpft sind.

## Opt-out {#opt-out}

Aufgrund der unterschiedlichen Opt-out-Attribute zwischen Microsoft Dynamics 365 und Campaign sowie der unterschiedlichen Geschäftsanforderungen einzelner Kunden wurde das Opt-out-Mapping als vom Kunden auszuführende Option konzipiert. Es ist wichtig, dass die Opt-out-Option zwischen den Systemen ordnungsgemäß zugeordnet wird, damit die Voreinstellungen für die Opt-out-Option des Endbenutzers beibehalten werden und er keine Kommunikation über einen Kanal erhält, den er abgewählt hat.

Bitte beachten Sie, dass nur Folgendes in Opt-out-Mappings verwendet werden kann:

* Campaign-Attribute mit dem Präfix &quot;Nicht mehr per ... kontaktieren&quot; (z. B. &quot;Nicht mehr per E-Mail kontaktieren&quot;) oder

* das spezifische Attribut für den CCPA.

Weitere Informationen zu den Entitätsfeldern von Profilen finden Sie [hier](../../developing/using/datamodel-profile.md).

In Dynamics 365 haben die meisten Opt-out-Felder das Präfix &quot;donot&quot;. Sie können jedoch auch andere Attribute zu Opt-out-Zwecken nutzen, solange die Datentypen kompatibel sind.

Bei der Bereitstellung der Integration können Sie angeben, welche Opt-out-Konfiguration Sie für Ihr Unternehmen wünschen:

* **Unidirektional (Microsoft Dynamics 365 zu Campaign)**: Dynamics 365 ist die &quot;Source of Truth&quot; für Opt-outs. Opt-out-Attribute werden in einer Richtung von Dynamics 365 zu Campaign Standard synchronisiert.
* **Unidirektional (Campaign zu Microsoft Dynamics 365)**: Campaign Standard ist die &quot;Source of Truth&quot; für Opt-outs. Opt-out-Attribute werden in einer Richtung von Campaign Standard zu Dynamics 365 synchronisiert.
* **Bidirektional**: Dynamics 365 UND Campaign Standard sind beide &quot;Sources of Truth&quot;. Opt-out-Attribute werden bidirektional zwischen Campaign Standard und Dynamics 365 synchronisiert.

Wenn Sie über einen separaten Prozess zum Verwalten der Opt-out-Synchronisation zwischen den Systemen verfügen, kann alternativ der Opt-out-Datenfluss der Integration deaktiviert werden.

Die bidirektionale Opt-out-Konfiguration nutzt eine Logik, um zu bestimmen, welcher Wert in beide Systeme geschrieben werden soll. Die Logik vergleicht Zeitstempel zwischen den beiden Systemen (Änderung auf Datensatzebene in Dynamics 365, Änderung auf Attributebene in Campaign), um zu ermitteln, welches System sich durchsetzt. Wenn Campaign den aktuelleren Zeitstempel enthält, hat der Campaign-Wert Vorrang. Wenn Dynamics 365 den aktuelleren Zeitstempel enthält oder beide gleich sind, erhält opt-out=TRUE den Vorrang (vorausgesetzt, einer der Werte ist TRUE).

Informationen zum Auswählen von Opt-in-/Opt-out-Optionen finden Sie in [diesem Abschnitt](../../integrating/using/d365-acs-self-service-app-data-sync.md#opt-in-out-wf).

>[!NOTE]
>
>Bitte überprüfen Sie die standardmäßigen und spezifischen Typologieregeln in Adobe Campaign und aktualisieren Sie diese gegebenenfalls, bevor Sie hier Änderungen vornehmen, damit sie auf alle ausgehenden Nachrichten korrekt angewendet werden. Achten Sie beispielsweise darauf, dass alle Mappings zu Opt-out-Voreinstellungen die Absichten/Kommunikationsoptionen des Empfängers genau widerspiegeln und den Versand von Beziehungs- oder Transaktionsnachrichten (wie z. B. Auftragsbestätigungen des Kunden) nicht versehentlich beenden.

Wenn Sie die Opt-out-Konfiguration **Bidirektional** oder **Unidirektional (Campaign zu Microsoft Dynamics 365)** ausgewählt haben, werden die Campaign-Opt-out-Daten regelmäßig über den Workflow in Ihren Campaign-SFTP-Speicherbereich exportiert (siehe &quot;Campaign-SFTP-Nutzung&quot; unten). Falls Ihre Campaign-Opt-out-Workflows angehalten werden, müssen Sie sie so schnell wie möglich manuell neu starten, um die Möglichkeit verpasster Opt-out-Synchronisationen zu vermeiden.

>[!IMPORTANT]
>
>Wenn Sie die Opt-out-Konfiguration **Bidirektional** oder **Unidirektional (Campaign zu Microsoft Dynamics 365)** benötigen, stellen Sie eine diesbezügliche Anfrage an Ihren technischen Ansprechpartner bei Adobe, damit die Opt-out-Workflows in Ihrer Campaign-Instanz eingerichtet werden können.

## Campaign-SFTP-Nutzung

Ihre Campaign-SFTP-Datenspeicherung muss in den unten angegebenen Anwendungsbeispielen von der Integration genutzt werden.  Stellen Sie sicher, dass Ihr SFTP-Konto über ausreichende Speicherkapazität für diese Anwendungsfälle verfügt. Eine Überschreitung der lizenzierten SFTP-Speicherkapazität kann die funktionale Nutzung von Campaign, die Integration und/oder das SFTP-Konto erheblich beeinträchtigen.

| Anwendungsbeispiel | Beschreibung  |
|---|---|
| Bidirektional und unidirektional (Campaign zu Microsoft Dynamics 365) | Bidirektionale und unidirektionale (Campaign zu Microsoft Dynamics 365) Opt-out-Datenflüsse nutzen die Campaign-SFTP-Datenspeicherung. Ein Campaign-Workflow exportiert inkrementelle Änderungen in den SFTP-Ordner. Von dort werden die Datensätze beim Integrationsvorgang aufgenommen und verarbeitet. |
| Opt-out-Logs | Opt-out-Logs vom Connector sind bei der Fehlersuche in der Integration hilfreich. Opt-out-Logs können ein- und ausgeschaltet werden. |


>[!IMPORTANT]
>
>Sie selbst sind für die Informationen verantwortlich, die Sie aus den SFTP-Ordnern abrufen und herunterladen. Wenn die Informationen personenbezogene Daten enthalten, sind Sie für die Einhaltung der geltenden Datenschutzgesetze und -bestimmungen verantwortlich. [Weitere Informationen](#acs-msdyn-manage-privacy).

## Daten-Management

### Bestehende Campaign-Daten

Durch diese Integration werden Kontakte und benutzerdefinierte Entitäten von Microsoft Dynamics 365 nach Campaign synchronisiert. Campaign-Datensätze, die außerhalb der Integration erstellt werden (d. h. nicht vom Synchronisationsvorgang), werden durch die Integration nicht geändert, einschließlich der zum Zeitpunkt der Integrationskonfiguration vorhandenen Campaign-Datensätze.

Da bei dieser Integration das Feld **[!UICONTROL externalId]** in Campaign zum Synchronisieren von Campaign-Profildatensätzen mit Dynamics 365-Kontaktdatensätzen verwendet wird, muss dieses Campaign-Feld (**[!UICONTROL externalId]**) mit der Microsoft Dynamics 365- **[!UICONTROL contactId]** für diejenigen Datensätze ausgefüllt werden, die in Microsoft Dynamics 365 synchronisiert werden sollen.  Benutzerdefinierte Entitäten werden ebenfalls mit einer eindeutigen Microsoft Dynamics 365-ID synchronisiert. Die benutzerdefinierte Entität in Campaign muss dieses ID-Attribut als Tabellenspalte enthalten. Die Spalte &quot;externalId&quot; kann verwendet werden, um diesen Attributwert zu speichern, ist jedoch nicht für benutzerdefinierte Entitäten in Campaign erforderlich.

Denken Sie daran, dass Microsoft Dynamics 365 weiter die &quot;Source of Truth&quot; bleibt und die Campaign-Profildaten überschrieben werden können, wenn die Integration Aktualisierungen auf der Seite von Dynamics 365 erkennt.  Je nach Ihrer vorhandenen Bereitstellung können auch andere Schritte zum Aktivieren der Integration erforderlich sein. Daher wird empfohlen, eng mit Ihrem technischen Ansprechpartner bei Adobe zusammenzuarbeiten.

>[!NOTE]
>
>Aufgrund der Komplexität vorhandener Kundenbereitstellungen sollten Sie sich bei der Planung und Einrichtung der Integration von Ihrem technischen Ansprechpartner von Adobe unterstützen lassen.

### Häufigkeit der Datensynchronisation

Die Integration nutzt eine Architektur, mit der Aktualisierungen erkannt und der Verarbeitungswarteschlange hinzugefügt werden können, kurz nachdem sie in Microsoft Dynamics 365 aufgetreten sind (d. h. Streaming, nicht Stapelverarbeitung). Aus diesem Grund müssen keine Ausführungsfrequenzen für den Datenfluss oder Zeitpläne angegeben werden.

Eine Ausnahme bilden die Datenflüsse beim bidirektionalen Opt-out und beim unidirektionalen Opt-out &quot;Campaign zu Dynamics 365&quot;. Bei diesen Opt-out-Konfigurationen werden aktualisierte Campaign-Datensätze einmal täglich über den Campaign-Workflow in den SFTP-Speicherbereich exportiert. Anschließend liest das Integrations-Tool die Datei und verarbeitet den Datensatz.

### Datennutzungsvereinbarung

Wenn Sie sich in der Region EMEA oder APAC befinden, werden einige Ihrer Daten im Rahmen dieser Integration in den USA verarbeitet. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

## Schutzmechanismen und Begrenzungen

>[!IMPORTANT]
>
>Bestimmte Aktionen (z. B. anfängliche Aufnahme von Datensätzen, erneutes Abspielen von Datensatzdaten usw.) können dazu führen, dass eine große Anzahl von Datensätzen von Microsoft Dynamics 365 in Ihre Adobe Campaign-Instanz aufgenommen wird. Um das Risiko von Leistungsproblemen zu verringern, wird empfohlen, alle Campaign-Prozesse anzuhalten (z. B. keine Marketing-Aktivitäten, keine laufenden Workflows usw.), bis die große Menge an Datensätzen in Campaign aufgenommen wurde.

### Benutzerdefinierte Entitäten

Die [Integration von Adobe Campaign Standard mit Microsoft Dynamics 365](../../integrating/using/d365-acs-get-started.md) unterstützt benutzerdefinierte Entitäten und ermöglicht die Synchronisation von benutzerdefinierten Entitäten in Dynamics 365 mit entsprechenden benutzerdefinierten Ressourcen in Campaign.

Die Integration unterstützt sowohl verknüpfte als auch nicht verknüpfte Tabellen.

Bei der Konfiguration benutzerdefinierter Entitätsdatenflüsse ist Folgendes zu beachten:

* Die Erstellung und Änderung von benutzerdefinierten Campaign-Ressourcen sind heikle Aufgaben, die nur von erfahrenen Benutzern durchgeführt werden können.
* Bei benutzerdefinierten Entitätsdatenflüssen muss für synchronisierte benutzerdefinierte Entitäten die Änderungsverfolgung innerhalb von Dynamics 365 aktiviert werden.
* Wenn ein übergeordneter und ein verknüpfter untergeordneter Datensatz in Dynamics 365 aufgrund der parallelen Verarbeitung der Integration nahezu zur gleichen Zeit erstellt werden, besteht eine geringe Wahrscheinlichkeit, dass ein neuer untergeordneter Datensatz vor seinem übergeordneten Datensatz in Campaign geschrieben wird.

* Wenn das übergeordnete und das untergeordnete Element in Campaign mithilfe der Option **Einfache Relation mit Kardinalität 1** verknüpft sind, bleibt der untergeordnete Datensatz ausgeblendet und kann (über die Benutzeroberfläche oder API) nicht aufgerufen werden, bis der übergeordnete Datensatz in Campaign eintrifft.

* (Angenommen, **Einfache Relation mit Kardinalität 1** wird in Campaign verwendet.) Wenn der untergeordnete Datensatz in Dynamics 365 aktualisiert oder gelöscht wird und diese Änderung in Campaign geschrieben wird, bevor der übergeordnete Datensatz in Campaign angezeigt wird (nicht wahrscheinlich, aber möglich), wird diese Aktualisierung oder Löschung nicht in Campaign verarbeitet und ein Fehler ausgegeben. Im Falle einer Aktualisierung muss der betreffende Datensatz erneut in Dynamics 365 aktualisiert werden, um den aktualisierten Datensatz zu synchronisieren. Im Falle der Löschung muss der betreffende Datensatz in Campaign gesondert behandelt werden, da in Dynamics 365 kein Datensatz mehr zum Löschen oder Aktualisieren vorhanden ist.

* Wenn Sie in eine Situation geraten, in der Sie glauben, versteckte untergeordnete Datensätze zu haben und nicht darauf zugreifen zu können, können Sie den Kardinalität-Relationstyp vorübergehend in **Einfache Relation mit Kardinalität 0 oder 1** ändern, um auf diese Datensätze zuzugreifen.

Eine umfassendere Übersicht über benutzerdefinierte Campaign-Ressourcen finden Sie [in diesem Abschnitt](../../developing/using/key-steps-to-add-a-resource.md).

### Leitplanken bei der Integration

Die folgenden Leitplanken sollten bei der Verwendung dieser Integration berücksichtigt werden. Wenden Sie sich an Ihren technischen Adobe-Support-Mitarbeiter, wenn Sie glauben, dass Sie diese Leitplanken überschreiten.

* Sie müssen das richtige Campaign-Package lizenzieren, um das durch die Integration generierte Aufrufvolumen der Engine zu unterstützen. Eine Überschreitung des zulässigen Aufrufvolumens der Engine könnte zu einer Verschlechterung der Leistung von Campaign führen.

  Verwenden Sie Folgendes, um das durch die Integration generierte Engine-Aufrufvolumen abzuschätzen:

   * Einfügungen von Datensätzen (d. h. neuer Datensatz): 1 Engine-Aufruf
   * Löschungen von Datensätzen: 1 Engine-Aufruf
   * Aktualisierungen von Datensätzen: 2 Engine-Aufrufe (nur 1 Aufruf, wenn der Zieldatensatz mit dem Quelldatensatz identisch ist, d. h., wenn keine Änderung am Campaign-Datensatz erfolgt)

  Bei der Schätzung des Gesamtaufrufvolumens der Campaign-Engine ist es wichtig, andere Quellen für Engine-Aufrufe zu berücksichtigen, einschließlich Landingpages, Web-Anwendungen, JSSP, APIs, Registrierungen von Mobile Apps usw.

  Informationen zum Adobe Campaign Standard-Package finden Sie hier: [https://helpx.adobe.com/de/legal/product-descriptions/campaign-standard.html](https://helpx.adobe.com/de/legal/product-descriptions/campaign-standard.html)

* Die Integration unterstützt maximal 15 Millionen Einträge für die erste Synchronisation mit Ressourcen in Campaign. Die inkrementelle Synchronisation wird durch das Adobe Campaign Standard-Package eingeschränkt.

* Das standardmäßige Integrationsangebot unterstützt bis zu 20 benutzerdefinierte Entitäten mit einer Größe von jeweils maximal 50 Spalten.

* Sie müssen Ihre benutzerdefinierten Ressourcen erstellen und veröffentlichen, bevor Sie die Integration implementieren.

* Die maximale Tabellentiefe beim Verknüpfen von Tabellen beträgt zwei (d. h. Tabelle1->Tabelle2->Tabelle3).

* Die Integration unterstützt bis zu 5 verknüpfte Spalten pro benutzerdefinierter Ressource. Die Verknüpfung mehrerer Spalten zwischen benutzerdefinierten Ressourcen kann erhebliche Leistungseinbußen zur Folge haben. **Einfache Relation mit Kardinalität 0 oder 1** wird gegenüber **Einfacher Relation mit Kardinalität 1** bevorzugt.

* Die Integration unterstützt die Transformation zwischen einfachen Datentypen in Microsoft Dynamics 365 (boolesch, Ganzzahl, Dezimal, Doublette, Zeichenfolge, Datum + Uhrzeit, Datum) und Adobe Campaign Standard-Datentypen (Ganzzahl, boolesch, Gleitkommazahl, Doublette, Datum, Datum + Uhrzeit, Zeichenfolge). Komplexere Datentypen werden als Zeichenfolgen interpretiert und in der jeweils vorliegenden Form synchronisiert.

* Möglicherweise müssen zwischen Adobe und dem Kunden Wartungsfenster für das Onboarding festgelegt werden.

* Beachten Sie, dass signifikante Steigerungen oder Spitzen bei der Nutzung der Integration (z. B. ein starker Anstieg neuer oder aktualisierter Datensätze) zu einer Verlangsamung bei der Datensynchronisation führen können.

* Im Rahmen der Integration wird erwartet, dass Sie die Konfigurationsschritte vor der Integration in Microsoft Azure und Dynamics 365 ausführen. Sie Konfigurationsschritte finden Sie [auf dieser Seite](../../integrating/using/d365-acs-configure-d365.md).

* Es wird erwartet, dass Sie Ihre Dynamics 365- und Campaign-Datenmodelle in die Integration einbinden und pflegen.

### Grenzen der Integration

Die Integration wurde entwickelt, um den allgemeinen Anwendungsfall von Datenbewegungen zwischen Microsoft Dynamics 365 und Campaign zu unterstützen. Dabei war nicht beabsichtigt, jeden kundenspezifischen Anwendungsfall damit zu lösen:

* Durch die Integration werden keine datenschutzbezogenen Löschvorgänge (z. B. DSGVO) veranlasst. Die Verantwortung für die Erfüllung von Datenschutzanfragen der Endbenutzer liegt beim Kunden. Solche Anfragen sollten sowohl in Campaign (über den Adobe Experience Platform Privacy Service) als auch in Dynamics 365 unabhängig voneinander gestellt werden. Die Integration kann bei Bedarf reguläre Löschvorgänge auslösen, um die Datensynchronisation zu unterstützen.   Weitere Informationen finden Sie im Abschnitt [Datenschutz](#manage-privacy-requests).

* Mit Ausnahme der Opt-out-Informationen (sofern vom Kunden konfiguriert) werden keine Profil- oder benutzerdefinierten Entitätsdaten von Campaign zu Dynamics 365 synchronisiert.

* Die Abonnementverwaltung (d. h. Abonnieren/Abbestellen von Abonnements) in Campaign wird nicht nativ unterstützt.

* Das Erstellen und Auslösen von Campaign-E-Mail-Kampagnen in Dynamics 365 wird nicht unterstützt.

* Die Integration unterstützt **keine** erneute Modellierung von Daten zwischen den Dynamics 365- und Campaign Standard-Datenmodellen. Es wird erwartet, dass bei der Integration eine einzelne Dynamics 365-Tabelle mit einer einzelnen Campaign-Tabelle synchronisiert wird.

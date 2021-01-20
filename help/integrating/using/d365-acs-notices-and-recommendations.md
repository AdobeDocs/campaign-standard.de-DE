---
solution: Campaign Standard
product: campaign
title: Management von Campaign- und Microsoft Dynamics 365-Daten
description: Erfahren Sie, wie Campaign Standard und Microsoft Dynamics 365 gemeinsame Daten verwalten.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
translation-type: tm+mt
source-git-commit: cce30fd5cd3d5d63563d1dab3bb1e7554c26fb3e
workflow-type: tm+mt
source-wordcount: '2470'
ht-degree: 58%

---


# Best Practices und Einschränkungen {#acs-msdyn-best-practices}

## Daten verwalten {#acs-msdyn-manage-data}

Bei der Synchronisierung von Kontakten und benutzerdefinierten Entitäten behandelt diese Integration **Microsoft Dynamics 365 als Quelle der Wahrheit**.  Änderungen an synchronisierten Attributen sollten in Dynamics 365 und nicht in Adobe Campaign Standard vorgenommen werden.  Wenn Änderungen in der Kampagne vorgenommen werden, können sie während der Synchronisierung in einer Kampagne überschrieben werden, da die Synchronisierung in eine Richtung verläuft.

Die Integration kann optional so konfiguriert werden, dass Profil-Löschaufrufe an die Kampagne gesendet werden, wenn ein Kontakt in Dynamics 365 gelöscht wird, um die Datenintegrität zu wahren. Beim Löschen eines Profils handelt es sich jedoch nicht um einen datenschutzbezogenen Löschvorgang. Durch einen Datenschutz-Löschvorgang in der Kampagne werden der Datensatz zum Kampagne-Profil und die zugehörigen Protokolleinträge entfernt. Während ein normales Profil löschen, löscht nur die Kampagne Profil-Datensatz, hinterlässt Überbleibsel in Kampagnen-Logs. Wenn die Funktion zum Löschen von Profilen in der Integration aktiviert ist, müssen weitere Schritte ausgeführt werden, um Datenschutzanfragen für betroffene Personen ordnungsgemäß zu verarbeiten. Lesen Sie die Schritte im Abschnitt [Datenschutz unten](#manage-privacy-requests).

## Datenschutz{#acs-msdyn-manage-privacy}

Diese Integration wurde entwickelt, um Endbenutzerdaten zwischen Microsoft Dynamics 365 und Adobe Campaign Standard zu übertragen. Diese Daten enthalten persönliche Daten, wenn diese in Ihren Endbenutzerdaten enthalten sind.  Als für die Verarbeitung der Daten verantwortliche Person ist Ihre Firma für die Einhaltung der für die Erhebung und Nutzung personenbezogener Daten geltenden Datenschutzgesetze und -vorschriften verantwortlich.

Mit dieser Integration lassen sich Endbenutzerdaten (darunter auch personenbezogene Daten, sofern diese in Ihren Endbenutzerdaten enthalten sind) zwischen Microsoft Dynamics 365 und Adobe Campaign Standard übertragen. Als Datenverantwortlicher ist Ihr Unternehmen zur Einhaltung der für die Erhebung und Nutzung personenbezogener Daten geltenden Datenschutzgesetze und -vorschriften verpflichtet.

Bei der Integration werden keine datenschutzbezogenen Löschvorgänge für betroffene Personen ausgegeben (z. B. DSGVO) oder andere Datenschutzanfragen bearbeitet (mit Ausnahme von Opt-out). Bei der Verarbeitung von Datenschutzanfragen sollten Sie dies sowohl in Microsoft Dynamics 365 als auch in der Kampagne (über das Adobe Experience Platform Privacy Service) unabhängig tun.

Wenn Sie die Integration so konfiguriert haben, dass beim Löschen eines Kontakts in Dynamics 365 reguläre Aufrufe zum Löschen von Profilen an Campaign gesendet werden, sollten Sie die folgenden Schritte ausführen. Stellen Sie sicher, dass während dieses Vorgangs keine Aktualisierungen am betreffenden Datensatz vorgenommen werden.

1. Datenschutzbezogene Löschanfrage an [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experiencecloud/gdpr.html) senden

1. Anfrage bis zum erfolgreichen Abschluss überwachen

1. Überprüfen, ob sich der Datensatz nicht mehr in Ihrer Campaign-Instanz befindet

1. (Kurz danach) die datenschutzbezogene Löschung in Dynamics 365 veranlassen

1. Überprüfen, ob der Datensatz aus beiden Systemen entfernt wurde

Nachstehend finden Sie Links, die Sie bei der Implementierung von datenschutzbezogenen Anfragen in Bezug auf den Zugriff oder die Löschung in jedem System unterstützen:

* [Microsoft Dynamics 365](https://docs.microsoft.com/en-us/dynamics365/get-started/gdpr/)

* [Adobe Campaign Standard](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)

>[!IMPORTANT]
>
>Wenn ein benutzerdefinierter Campaign-Ressourcendatensatz personenbezogene Daten enthält, die auch in Campaign verwendet werden, sollte dieser Datensatz mit einem entsprechenden Campaign-Profildatensatz verknüpft werden (entweder direkt oder über eine andere benutzerspezifische Ressource), sodass ein datenschutzbezogener Löschvorgang im Profildatensatz auch den verknüpften benutzerspezifischen Ressourcendatensatz mit personenbezogenen Daten löschen kann. Die Verknüpfungs- und Löschoptionen zwischen den Entitäten müssen so konfiguriert sein, dass eine solche kaskadierte Löschung der verknüpften Datensätze möglich wird. Personenbezogene Daten sollten nicht in benutzerdefinierte Ressourcen eingegeben werden, die nicht mit dem Profil verknüpft sind.

## Opt-out {#opt-out}

Aufgrund der unterschiedlichen Ausschlussattribute von Microsoft Dynamics 365 und Kampagne sowie der unterschiedlichen Geschäftsanforderungen der einzelnen Kunden wurde die Abmeldezuordnung für den Kunden beibehalten.  Es ist wichtig, sicherzustellen, dass Opt-outs ordnungsgemäß zwischen den Systemen zugeordnet werden, damit die Voreinstellungen für die Abmeldung des Endbenutzers beibehalten werden und sie keine Kommunikation über einen Kanal erhalten, für den sie sich entschieden haben.

Bitte beachten Sie, dass bei Abmeldezuordnungen nur Folgendes verwendet werden kann:

* Kampagnen-Attribute mit dem Präfix &quot;Keine Kontaktaufnahme mehr&quot;(z. B. keine E-Mail-Kontaktaufnahme mehr) oder

* das spezifische Attribut für CCPA

Weitere Informationen zu den Profil-Entitätsfeldern finden Sie [hier](../../developing/using/datamodel-profile.md).

In Dynamics 365 haben die meisten Ausschluss-Felder das Präfix &quot;Donot&quot;. Sie können jedoch auch andere Attribute für Ausschluss-Zwecke verwenden, wenn die Datentypen kompatibel sind.

Bei der Bereitstellung der Integration können Sie angeben, welche Opt-out-Konfiguration Sie für Ihr Unternehmen wünschen:

* **Unidirektional (Microsoft Dynamics 365 zur Kampagne)**: Dynamics 365 ist eine Quelle der Wahrheit für Opt-out-Möglichkeiten. Ausschlussattribute werden in einer Richtung von Dynamics 365 auf den Campaign Standard synchronisiert
* **Unidirektional (Kampagne zu Microsoft Dynamics 365)**: Campaign Standard ist die Quelle der Wahrheit für Opt-out. Ausschlussattribute werden von Campaign Standard zu Dynamics 365 in eine Richtung synchronisiert.
* **Bidirektional**: Dynamics 365 UND Campaign Standard sind beide Wahrheitsquellen. Ausschlussattribute werden bidirektional zwischen Campaign Standard und Dynamics 365 synchronisiert

Wenn Sie über einen separaten Prozess zum Verwalten der Opt-Out-Synchronisation zwischen den Systemen verfügen, kann alternativ der Opt-Out-Datenfluss der Integration deaktiviert werden.

Die bidirektionale Opt-out-Konfiguration nutzt eine Logik, um zu bestimmen, welcher Wert in beide Systeme geschrieben werden soll. Die Logik vergleicht Zeitstempel zwischen den beiden Systemen (Änderung auf Datensatzebene in Dynamics 365, Änderung auf Attributebene in Campaign), um zu ermitteln, welches System sich durchsetzt. Wenn Campaign den aktuelleren Zeitstempel enthält, hat der Campaign-Wert Vorrang. Wenn Dynamics 365 den aktuelleren Zeitstempel enthält oder beide gleich sind, erhält opt-out=TRUE den Vorrang (vorausgesetzt, einer der Werte ist TRUE).

Erfahren Sie, wie Sie in [diesem Abschnitt](../../integrating/using/d365-acs-self-service-app-data-sync.md#opt-in-out-wf) Optionen für das Ein-/Ausschließen auswählen.

>[!NOTE]
>
>Bitte überprüfen Sie die standardmäßigen und spezifischen Typologieregeln in Adobe Campaign und aktualisieren Sie diese gegebenenfalls, bevor Sie hier Änderungen vornehmen, damit sie auf alle ausgehenden Nachrichten korrekt angewendet werden. Achten Sie beispielsweise darauf, dass alle Mappings zu Opt-out-Voreinstellungen die Absichten/Kommunikationsoptionen des Empfängers genau widerspiegeln und den Versand von Beziehungs- oder Transaktionsnachrichten (wie z. B. Auftragsbestätigungen des Kunden) nicht versehentlich beenden.

Wenn Sie die Option **Bidirektionale** oder **Unidirektionale (Kampagne zu Microsoft Dynamics 365)** Abmeldekonfiguration ausgewählt haben, werden die Abmeldedaten der Kampagne regelmäßig über den Workflow in den Bereich Ihrer Kampagne SFTP-Datenspeicherung exportiert (siehe &quot;Kampagne SFTP-Nutzung unten&quot;). Falls Ihre Campaign-Opt-Out-Workflows nicht mehr ausgeführt werden, müssen Sie sie so schnell wie möglich manuell neu starten, um die Möglichkeit verpasster Opt-Out-Synchronisationen zu vermeiden.

>[!IMPORTANT]
>
>Wenn Sie die Option **Bidirektionale** oder **Unidirektionale (Kampagne zu Microsoft Dynamics 365)** Abmeldekonfiguration benötigen, müssen Sie bei Ihrer Adobe den technischen Kontakt auffordern, die Workflows für die Abmeldung in Ihrer Instanz der Kampagne einzurichten

## Campaign-SFTP-Nutzung

Ihre Campaign-SFTP-Datenspeicherung muss in den unten angegebenen Anwendungsbeispielen von der Integration genutzt werden.  Sie müssen sicherstellen, dass Ihr SFTP-Konto über eine ausreichende Speicherkapazität für diese Anwendungsfälle verfügt. Eine Überschreitung der lizenzierten SFTP-Speicherkapazität kann die funktionale Nutzung von Campaign, die Integration und/oder das SFTP-Konto erheblich beeinträchtigen.

| Anwendungsbeispiel | Beschreibung  |
|---|---|
| Bidirektionale und unidirektionale (Kampagne zu Microsoft Dynamics 365) | Bidirektionale und unidirektionale (Kampagne zu Microsoft Dynamics 365) Abmeldedatenflüsse nutzen die Kampagne SFTP-Datenspeicherung. Ein Arbeitsablauf für die Kampagne exportiert inkrementelle Änderungen in den SFTP-Ordner. Von dort nimmt die Integration die Datensätze auf und verarbeitet sie. |
| Abmeldeprotokolle | Ausgabsprotokolle vom Connector sind bei der Fehlerbehebung der Integration hilfreich. Ausgabsprotokolle können ein-/ausgeschaltet werden. |


>[!IMPORTANT]
>
>Sie sind für die Informationen verantwortlich, die Sie aus den SFTP-Ordnern aufrufen und herunterladen können. Wenn die Informationen personenbezogene Daten enthalten, sind Sie für die Einhaltung der geltenden Datenschutzgesetze und -vorschriften verantwortlich. [Weitere Informationen](#acs-msdyn-manage-privacy).

## Data management

### Bestehende Campaign-Daten

Durch diese Integration werden Kontakte und benutzerdefinierte Entitäten von Microsoft Dynamics 365 zur Kampagne synchronisiert. Campaign-Datensätze, die außerhalb der Integration erstellt werden (d. h. nicht vom Synchronisationsvorgang), werden durch die Integration nicht geändert, einschließlich der zum Zeitpunkt der Integrationskonfiguration vorhandenen Campaign-Datensätze.

Da bei dieser Integration das Feld **[!UICONTROL externalId]** in der Kampagne zum Synchronisieren von Kampagne-Profil-Datensätzen mit Dynamics 365-Kontaktdatensätzen verwendet wird, muss dieses Feld für die Kampagne (**[!UICONTROL externalId]**) mit Microsoft Dynamics 365 **[!UICONTROL contactId]** ausgefüllt werden, um die aus Microsoft Dynamics 36 synchronisiert werden zu können 5.  Benutzerdefinierte Entitäten werden auch mit einer eindeutigen Microsoft Dynamics 365-ID synchronisiert. Die benutzerdefinierte Entität in Campaign muss dieses ID-Attribut als Tabellenspalte enthalten. Die Spalte &quot;externalId&quot; kann verwendet werden, um diesen Attributwert zu speichern, ist jedoch nicht für benutzerdefinierte Entitäten in Campaign erforderlich.

Denken Sie daran, dass Microsoft Dynamics 365 immer noch die Quelle der Wahrheit ist und dass die Kampagne Profil-Daten überschrieben werden können, wenn die Integration Updates auf der Dynamics 365-Seite erkennt.  Je nach Ihrer vorhandenen Implementierung können auch andere Schritte zum Aktivieren der Integration erforderlich sein. Daher wird empfohlen, eng mit Ihrem technischen Ansprechpartner bei Adobe zusammenzuarbeiten.

>[!NOTE]
>
>Aufgrund der Komplexität vorhandener Kundenimplementierungen sollten Sie sich bei der Planung und Einrichtung der Integration von Ihrem technischen Ansprechpartner von Adobe unterstützen lassen.

### Häufigkeit der Datensynchronisation

Die Integration nutzt eine Architektur, mit der Updates erkannt und der Verarbeitungswarteschlange hinzugefügt werden können, kurz nachdem sie in Microsoft Dynamics 365 aufgetreten sind (d. h. Streaming, nicht Stapelverarbeitung). Aus diesem Grund müssen keine Ausführungsfrequenzen für den Datenfluss oder Zeitpläne angegeben werden.

Eine Ausnahme bilden die bidirektionale und Kampagne zu Dynamics 365 Ausschluss-Datenströmen. Bei diesen Ausschluss-Konfigurationen werden aktualisierte Kampagnen einmal täglich über einen Kampagnen-Workflow in das SFTP exportiert. Danach liest das Integrationstool die Datei und verarbeitet den Datensatz.

### Datennutzungsvereinbarung

Wenn Sie sich in der Region EMEA oder APAC befinden, werden einige Ihrer Daten im Rahmen dieser Integration in den USA verarbeitet. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

## Garantien und Einschränkungen

>[!IMPORTANT]
>
>Bestimmte Aktionen (z. B. anfängliche Erfassung von Datensätzen, Wiedergeben von Datensatzdaten usw.) kann dazu führen, dass eine große Anzahl von Datensätzen von Microsoft Dynamics 365 in Ihre Adobe Campaign-Instanz aufgenommen wird. Um das Risiko von Leistungsproblemen zu verringern, wird empfohlen, alle Kampagnen zu beenden (z.B. keine Marketing-Aktivität, keine Workflows usw.) bis die große Menge der Datensätze in die Kampagne aufgenommen wurde.

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

### Limits bei der Integration

Die folgenden Limits sollten bei der Verwendung dieser Integration berücksichtigt werden. Wenden Sie sich an Ihren technischen Adobe-Support-Mitarbeiter, wenn Sie glauben, dass Sie diese Limits überschreiten.

* Sie müssen das richtige Kampagne-Paket lizenzieren, um die durch die Integration generierte Anzahl von Motoraufrufen zu unterstützen. Eine Überschreitung des zulässigen Aufrufvolumens der Engine könnte zu einer Verschlechterung der Leistung von Campaign führen.

   Verwenden Sie Folgendes, um das durch die Integration generierte Engine-Aufrufvolumen abzuschätzen:

   * Einfügungen von Datensätzen (d. h. neuer Datensatz): 1 Engine-Aufruf
   * Löschungen von Datensätzen: 1 Engine-Aufruf
   * Aktualisierungen aufzeichnen: 2 Engine-Aufrufe (nur 1 Aufruf, wenn der Zieldatensatz identisch mit dem Quelldatensatz ist, d. h. wenn keine Änderung am Kampagne-Datensatz erfolgt)

   Bei der Schätzung des gesamten Aufrufvolumens der Kampagne-Engine ist es wichtig, andere Quellen für Motorabrufe zu berücksichtigen, einschließlich Landingpages, WebApps, JSSP, APIs, Registrierungen mobiler Apps usw.

   Informationen zum Campaign-Package finden Sie hier: https://helpx.adobe.com/de/legal/product-descriptions/campaign-standard.html

* Die Integration unterstützt maximal 30 Millionen Kontakte.

* Das Standardintegrationsangebot umfasst die Unterstützung für bis zu fünf benutzerdefinierte Entitäten., jeweils mit einer Größe von maximal 50 Spalten.

* Sie müssen Ihre benutzerdefinierten Ressourcen erstellen und veröffentlichen, bevor Sie die Integration implementieren.

* Die maximale Tabellentiefe beim Verknüpfen von Tabellen beträgt zwei (d. h. Tabelle1->Tabelle2->Tabelle3).

* Microsoft Dynamic 365-Datentypen werden nur eingeschränkt unterstützt. Wenn Ihr Datenmodell einen anderen Datentyp als einfache Datentypen enthält (z. B. Zeichenfolgen, Ganzzahlen, Dezimalzahlen usw.), müssen Sie Ihr Datenmodell möglicherweise aktualisieren, bevor Sie die Integration verwenden.

* Wenn Sie sich dafür entschieden haben, vorhandene Daten in benutzerdefinierten Entitäten der Kampagne beizubehalten, müssen Sie die Daten für die Integration vorbereiten.

* Die Wartungsfenster für das Einbordgehen müssen ggf. zwischen der Adobe und dem Kunden eingerichtet werden.

* Beachten Sie, dass signifikante Steigerungen oder &quot;Spitzen&quot;bei der Nutzung der Integration (z. B. starke Zunahme neuer oder aktualisierter Datensätze) zu einer Verlangsamung der Datensynchronisierung führen können.

* Im Rahmen der Integration wird erwartet, dass Sie die Konfigurationsschritte vor der Integration in Microsoft Azure und Dynamics 365 ausführen. Sie Konfigurationsschritte finden Sie [auf dieser Seite](../../integrating/using/d365-acs-configure-d365.md).

* Es wird erwartet, dass Sie Ihre Dynamics 365- und Campaign-Datenmodelle in die Integration einbinden und pflegen.

### Grenzen der Integration

Die Integration wurde konzipiert, um den allgemeinen Verwendungsfall der allgemeinen Datenbewegung zwischen Microsoft Dynamics 365 und Kampagne zu lösen, ist jedoch nicht dazu gedacht, jeden Anwendungsfall, der für jeden Kunden spezifisch ist, zu behandeln:

* Durch die Integration werden keine datenschutzbezogenen Löschvorgänge (z. B. DSGVO) veranlasst. Die Verantwortung für die Erfüllung von Datenschutzanfragen der Endbenutzer liegt beim Kunden. Solche Anfragen sollten sowohl in Campaign (über den Adobe Experience Platform Privacy Service) als auch in Dynamics 365 unabhängig voneinander gestellt werden. Die Integration kann bei Bedarf reguläre Löschvorgänge auslösen, um die Datensynchronisation zu unterstützen.   Weitere Informationen finden Sie im Abschnitt Datenschutz](#manage-privacy-requests).[

* Mit Ausnahme der Opt-out-Informationen (sofern vom Kunden konfiguriert) werden keine Profil- oder benutzerdefinierten Entitätsdaten von Campaign zu Dynamics 365 synchronisiert.

* Die Abonnementverwaltung (d. h. Abonnieren/Abbestellen von Abonnements) in Campaign wird nicht nativ unterstützt.

* Das Erstellen und Auslösen von Campaign-E-Mail-Kampagnen in Dynamics 365 wird nicht unterstützt.

* Die Integration unterstützt nicht **die Umformung von Daten zwischen den Modellen Dynamics 365 und Campaign Standard.** Es wird erwartet, dass die Integration eine Dynamics 365-Tabelle mit einer Campaign-Tabelle synchronisiert.

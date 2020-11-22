---
solution: Campaign Standard
product: campaign
title: Management von Campaign- und Microsoft Dynamics 365-Daten
description: Erfahren Sie, wie Campaign Standard und Microsoft Dynamics 365 gemeinsame Daten verwalten.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '1451'
ht-degree: 100%

---


# Daten zwischen Campaign und Microsoft Dynamics 365 verwalten

## &quot;Source of Truth&quot; für unidirektionale Synchronisation

Für die Synchronisation von Kontakten und benutzerdefinierten Entitäten behandelt diese Integration Dynamics 365 als &quot;Source of Truth&quot;. Änderungen an synchronisierten Attributen sollten in Dynamics 365 und nicht in Campaign vorgenommen werden. Wenn Änderungen in Campaign vorgenommen werden, können diese bei der Synchronisation in Campaign überschrieben werden, da die Synchronisation in eine Richtung verläuft.

## Löschung von Kontakten

Falls gewünscht, kann die Integration so konfiguriert werden, dass beim Löschen eines Kontakts in Dynamics 365 Aufrufe zum Löschen von Profilen an Campaign ausgegeben werden, um die Datenintegrität zu gewährleisten.

Beim Löschen eines Profils handelt es sich jedoch nicht um einen datenschutzbezogenen Löschvorgang. Durch einen datenschutzbezogenen Löschvorgang in Campaign werden der Campaign-Profildatensatz und die zugehörigen Protokolleinträge entfernt, wohingegen ein regulärer Profillöschvorgang nur den ACS-Profildatensatz löscht und Reste in den Campaign-Protokollen zurücklässt.

Wenn die Funktion zum Löschen von Profilen in der Integration aktiviert ist, müssen weitere Schritte ausgeführt werden, um Datenschutzanfragen für betroffene Personen ordnungsgemäß zu verarbeiten. Beachten Die die Schritte im [folgenden Abschnitt](#manage-privacy-requests).

## Datenschutz

### Datenschutzanfragen verwalten {#manage-privacy-requests}

Mit dieser Integration lassen sich Endbenutzerdaten (darunter auch personenbezogene Daten, sofern diese in Ihren Endbenutzerdaten enthalten sind) zwischen Microsoft Dynamics 365 und Adobe Campaign Standard übertragen. Als Datenverantwortlicher ist Ihr Unternehmen zur Einhaltung der für die Erhebung und Nutzung personenbezogener Daten geltenden Datenschutzgesetze und -vorschriften verpflichtet.

Bei der Integration werden keine datenschutzbezogenen Löschvorgänge für betroffene Personen ausgegeben (z. B. DSGVO) oder andere Datenschutzanfragen bearbeitet (mit Ausnahme von Opt-out). Wenn Sie Datenschutzanfragen bearbeiten, sollten Sie dies sowohl in Dynamics 365 als auch in Campaign (über den Adobe Experience Platform Privacy Service) unabhängig voneinander tun.

Wenn Sie die Integration so konfiguriert haben, dass beim Löschen eines Kontakts in Dynamics 365 reguläre Aufrufe zum Löschen von Profilen an Campaign gesendet werden, sollten Sie die folgenden Schritte ausführen. Stellen Sie sicher, dass während dieses Vorgangs keine Aktualisierungen am betreffenden Datensatz vorgenommen werden.

1. Datenschutzbezogene Löschanfrage an [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experiencecloud/gdpr.html) senden

1. Anfrage bis zum erfolgreichen Abschluss überwachen

1. Überprüfen, ob sich der Datensatz nicht mehr in Ihrer Campaign-Instanz befindet

1. (Kurz danach) die datenschutzbezogene Löschung in Dynamics 365 veranlassen

1. Überprüfen, ob der Datensatz aus beiden Systemen entfernt wurde

Nachstehend finden Sie Links, die Sie bei der Implementierung von datenschutzbezogenen Anfragen in Bezug auf den Zugriff oder die Löschung in jedem System unterstützen:

* [Microsoft Dynamics 365](https://docs.microsoft.com/en-us/microsoft-365/compliance/gdpr-dsr-dynamics365?toc=/microsoft-365/enterprise/toc.json)

* [Adobe Campaign Standard](https://www.adobe.io/apis/experiencecloud/gdpr/docs.html)


### Datenschutz und verknüpfte Ressourcen {#privacy-linked-resources}

Wenn ein benutzerdefinierter Campaign-Ressourcendatensatz personenbezogene Daten enthält, die auch in Campaign verwendet werden, sollte dieser Datensatz mit einem entsprechenden Campaign-Profildatensatz verknüpft werden (entweder direkt oder über eine andere benutzerspezifische Ressource), sodass ein datenschutzbezogener Löschvorgang im Profildatensatz auch den verknüpften benutzerspezifischen Ressourcendatensatz mit personenbezogenen Daten löschen kann. Die Verknüpfungs- und Löschoptionen zwischen den Entitäten müssen so konfiguriert sein, dass eine solche kaskadierte Löschung der verknüpften Datensätze möglich wird. Personenbezogene Daten sollten nicht in benutzerdefinierte Ressourcen eingegeben werden, die nicht mit dem Profil verknüpft sind.

[In diesem Abschnitt](../../integrating/using/map-campaign-custom-resources-and-dynamics-365-custom-entities.md) erfahren Sie, wie Sie Campaign-Ressourcen und Dynamics 365-Entitäten zuordnen.

## Opt-out

Aufgrund der unterschiedlichen Opt-out-Attribute zwischen Dynamics 365 und Campaign sowie der unterschiedlichen Geschäftsanforderungen einzelner Kunden wurde das Opt-out-Mapping als vom Kunden auszuführende Option konzipiert. Es ist wichtig, dass die Opt-out-Option zwischen den Systemen ordnungsgemäß zugeordnet wird, damit die Voreinstellungen für die Opt-out-Option des Endbenutzers beibehalten werden und er keine Kommunikation über einen Kanal erhält, den er abgewählt hat.

Beachten Sie, dass beim Opt-out-Mapping nur Campaign-Attribute mit dem Präfix &quot;Nicht mehr per&quot; (z. B. &quot;Nicht mehr per E-Mail kontaktieren&quot;) oder dem spezifischen Attribut für den CCPA-Opt-out verwendet werden können – [mehr dazu](../../developing/using/datamodel-profile.md).
In Dynamics 365 haben die meisten Opt-out-Felder das Präfix &quot;donot&quot;. Sie können jedoch auch andere Attribute zu Opt-out-Zwecken nutzen, solange die Datentypen kompatibel sind.

Bei der Bereitstellung der Integration können Sie angeben, welche Opt-out-Konfiguration Sie für Ihr Unternehmen wünschen:

* Dynamics 365 ist die &quot;Source of Truth&quot; für Opt-outs: Opt-out-Attribute werden in eine Richtung von Dynamics 365 zu Campaign synchronisiert.
* Campaign ist die &quot;Source of Truth&quot; für Opt-outs: Opt-out-Attribute werden in einer Richtung von Campaign zu Dynamics 365 synchronisiert.
* Dynamics 365 UND Campaign sind beide &quot;Source of Truth&quot;: Opt-out-Attribute werden in beide Richtungen zwischen Campaign und Dynamics 365 synchronisiert.

Wenn Sie über einen separaten Prozess zum Verwalten der Opt-Out-Synchronisation zwischen den Systemen verfügen, kann alternativ der Opt-Out-Datenfluss der Integration deaktiviert werden.

Die bidirektionale Opt-out-Konfiguration nutzt eine Logik, um zu bestimmen, welcher Wert in beide Systeme geschrieben werden soll. Die Logik vergleicht Zeitstempel zwischen den beiden Systemen (Änderung auf Datensatzebene in Dynamics 365, Änderung auf Attributebene in Campaign), um zu ermitteln, welches System sich durchsetzt. Wenn Campaign den aktuelleren Zeitstempel enthält, hat der Campaign-Wert Vorrang. Wenn Dynamics 365 den aktuelleren Zeitstempel enthält oder beide gleich sind, erhält opt-out=TRUE den Vorrang (vorausgesetzt, einer der Werte ist TRUE).

>[!NOTE]
>
>Bitte überprüfen Sie die standardmäßigen und spezifischen Typologieregeln in Adobe Campaign und aktualisieren Sie diese gegebenenfalls, bevor Sie hier Änderungen vornehmen, damit sie auf alle ausgehenden Nachrichten korrekt angewendet werden. Achten Sie beispielsweise darauf, dass alle Mappings zu Opt-out-Voreinstellungen die Absichten/Kommunikationsoptionen des Empfängers genau widerspiegeln und den Versand von Beziehungs- oder Transaktionsnachrichten (wie z. B. Auftragsbestätigungen des Kunden) nicht versehentlich beenden.

Wenn Sie die Opt-out-Konfiguration &quot;Campaign zu Dynamics 365&quot; oder &quot;bidirektional&quot; ausgewählt haben, werden die Campaign-Opt-Out-Daten regelmäßig über den Workflow in Ihren Campaign-SFTP-Speicherbereich exportiert (siehe &quot;Campaign-SFTP-Nutzung&quot; unten). Falls Ihre Campaign-Opt-Out-Workflows nicht mehr ausgeführt werden, müssen Sie sie so schnell wie möglich manuell neu starten, um die Möglichkeit verpasster Opt-Out-Synchronisationen zu vermeiden.

## Campaign-SFTP-Nutzung

Ihre Campaign-SFTP-Datenspeicherung muss in den unten angegebenen Anwendungsbeispielen von der Integration genutzt werden.  Sie müssen sicherstellen, dass Ihr SFTP-Konto über eine ausreichende Speicherkapazität für diese Anwendungsfälle verfügt.  Eine Überschreitung der lizenzierten SFTP-Speicherkapazität kann die funktionale Nutzung von Campaign, die Integration und/oder das SFTP-Konto erheblich beeinträchtigen.

| Anwendungsbeispiel | Beschreibung  |
|---|---|
| Erster Datenladevorgang | Dynamics 365-Tabellen mit mehr als 500.000 Datensätzen müssen in den Campaign-SFTP-Speicher exportiert werden, damit sie über einen Workflow importiert werden können. Ab diesem Zeitpunkt verwendet die Integration APIs für inkrementelle Aktualisierungen. |
| Bidirektionaler Opt-out und unidirektionaler Opt-out &quot;Campaign zu Dynamics 365&quot; | Die Datenflüsse beim bidirektionalen Opt-out und beim unidirektionalen Opt-out &quot;Campaign zu Dynamics 365&quot; verwenden die Campaign-SFTP-Speicherung. Ein ACS-Workflow exportiert inkrementelle Änderungen in den SFTP-Ordner. Von dort nimmt die Integration die Datensätze auf und verarbeitet sie. |
| Notfallwiederherstellung | Im unwahrscheinlichen Fall einer Systemkatastrophe wird das Anwendungsbeispiel &quot;Erster Datenladevorgang&quot; befolgt, um die fehlenden inkrementellen Aktualisierungen an Campaign weiterzuleiten. |

## Bestehende Campaign-Daten

Durch diese Integration werden Kontakte und benutzerdefinierte Entitäten von Dynamics 365 nach Campaign synchronisiert. Campaign-Datensätze, die außerhalb der Integration erstellt werden (d. h. nicht vom Synchronisationsvorgang), werden durch die Integration nicht geändert, einschließlich der zum Zeitpunkt der Integrationskonfiguration vorhandenen Campaign-Datensätze.

Da bei dieser Integration das Feld **[!UICONTROL externalId]** in Campaign zum Synchronisieren von Campaign-Profildatensätzen mit Dynamics 365-Kontaktdatensätzen verwendet wird, muss dieses Campaign-Feld (**[!UICONTROL externalId]**) mit der Dynamics 365- **[!UICONTROL contactId]** für die Datensätze ausgefüllt werden, die aus Dynamics 365 synchronisiert werden sollen.  Benutzerdefinierte Entitäten werden auch mit einer eindeutigen Dynamics 365-ID synchronisiert. Die benutzerdefinierte Entität in Campaign muss dieses ID-Attribut als Tabellenspalte enthalten. Die Spalte &quot;externalId&quot; kann verwendet werden, um diesen Attributwert zu speichern, ist jedoch nicht für benutzerdefinierte Entitäten in Campaign erforderlich.

Denken Sie daran, dass Dynamics 365 weiter die &quot;Source of Truth&quot; bleibt und die Campaign-Profildaten überschrieben werden können, wenn die Integration Aktualisierungen auf der Seite von Dynamics 365 erkennt.  Je nach Ihrer vorhandenen Implementierung können auch andere Schritte zum Aktivieren der Integration erforderlich sein. Daher wird empfohlen, eng mit Ihrem technischen Ansprechpartner bei Adobe zusammenzuarbeiten.

>[!NOTE]
>
>Aufgrund der Komplexität vorhandener Kundenimplementierungen sollten Sie sich bei der Planung und Einrichtung der Integration von Ihrem technischen Ansprechpartner von Adobe unterstützen lassen.

## Häufigkeit der Datensynchronisation

Die Integration nutzt eine Architektur, mit der Aktualisierungen erkannt und der Verarbeitungswarteschlange hinzugefügt werden können, kurz nachdem sie in Dynamics 365 aufgetreten sind (d. h. Streaming, nicht Stapelverarbeitung). Aus diesem Grund müssen keine Ausführungsfrequenzen für den Datenfluss oder Zeitpläne angegeben werden.

Eine Ausnahme bilden die Datenflüsse beim bidirektionalen Opt-out und beim unidirektionalen Opt-out &quot;Campaign zu Dynamics 365&quot;. Bei diesen Opt-out-Konfigurationen werden aktualisierte ACS-Datensätze einmal täglich über den ACS-Workflow nach SFTP exportiert. Anschließend liest das Integrations-Tool die Datei und verarbeitet den Datensatz.

## Datennutzungsvereinbarung

Wenn Sie sich in der Region EMEA oder APAC befinden, werden einige Ihrer Daten im Rahmen dieser Integration in den USA verarbeitet. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

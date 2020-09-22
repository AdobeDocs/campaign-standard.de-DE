---
title: Kampagne und Microsoft Dynamics 365-Data Management
description: Erfahren Sie, wie Campaign Standard und Microsoft Dynamics 365 allgemeine Daten verwalten.
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
source-git-commit: 2ef169d9bf76856bb687af88358e0452953313a0
workflow-type: tm+mt
source-wordcount: '1451'
ht-degree: 37%

---


# Daten zwischen Kampagne und Microsoft Dynamics 365 verwalten

## Quelle der Wahrheit für einseitige Synchronisierung

Für die Synchronisierung von Kontakten und benutzerdefinierten Entitäten behandelt diese Integration Dynamics 365 als Quelle der Wahrheit.  Änderungen an synchronisierten Attributen sollten in Dynamics 365, nicht in der Kampagne vorgenommen werden.  Wenn Änderungen in Campaign vorgenommen werden, können diese bei der Synchronisation in Campaign überschrieben werden, da die Synchronisation in eine Richtung verläuft.

## Löschung von Kontakten

Bei Bedarf kann die Integration so konfiguriert werden, dass beim Löschen eines Profils in Dynamics 365 -Löschaufrufe an die Kampagne gesendet werden, um die Datenintegrität zu wahren.

Beim Löschen eines Profils handelt es sich jedoch nicht um eine Datenschutzlöschung. Durch einen Datenschutz-Löschvorgang in der Kampagne werden der Datensatz zum Kampagne-Profil und die zugehörigen Protokolleinträge entfernt. Während ein regulärer Profil-Löschvorgang nur den ACS-Profil-Datensatz löscht, hinterlässt der Rest in den Kampagnen-Protokollen.

Wenn die Funktion zum Löschen von Profilen in der Integration aktiviert ist, müssen weitere Schritte ausgeführt werden, um Datenschutzanforderungen für betroffene Personen ordnungsgemäß zu verarbeiten. Gehen Sie zu den Schritten im [folgenden](#manage-privacy-requests)Abschnitt.

## Datenschutz

### Datenschutzanforderungen verwalten {#manage-privacy-requests}

Mit dieser Integration lassen sich Endbenutzerdaten (darunter auch personenbezogene Daten, sofern diese in Ihren Endbenutzerdaten enthalten sind) zwischen Microsoft Dynamics 365 und Adobe Campaign Standard übertragen. Als Datenverantwortlicher ist Ihr Unternehmen zur Einhaltung der für die Erhebung und Nutzung personenbezogener Daten geltenden Datenschutzgesetze und -vorschriften verpflichtet.

Durch die Integration werden keine Datenschutzanforderungen (z.B. GDPR) gelöscht oder andere Datenschutzanforderungen (mit Ausnahme der Opt-out-Klausel) bearbeitet. Bei der Bearbeitung von Datenschutzanfragen sollten Sie dies sowohl in Dynamics 365 als auch in der Kampagne (über die Adobe Experience Platform Privacy Service) unabhängig tun.

Wenn Sie die Integration so konfiguriert haben, dass beim Löschen eines Kontakts in Dynamics 365 regelmäßige Profil-Löschaufrufe an die Kampagne gesendet werden, sollten Sie die folgenden Schritte ausführen. Stellen Sie sicher, dass während dieses Prozesses keine Aktualisierungen am betreffenden Datensatz vorgenommen werden.

1. Anforderung zum Löschen des Datenschutzes an [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experiencecloud/gdpr.html)

1. Anfrage bis zum erfolgreichen Abschluss überwachen

1. Überprüfen Sie, ob sich der Datensatz nicht mehr in Ihrer Kampagne befindet.

1. (Bald danach) Löschen des Datenschutzes in Dynamics 365

1. Überprüfen Sie, ob der Datensatz aus beiden Systemen entfernt wurde

Nachstehend finden Sie Links, die Sie bei der Implementierung von datenschutzbezogenen Anfragen in Bezug auf den Zugriff oder die Löschung in jedem System unterstützen:

* [Microsoft Dynamics 365](https://docs.microsoft.com/en-us/microsoft-365/compliance/gdpr-dsr-dynamics365?toc=/microsoft-365/enterprise/toc.json)

* [Adobe Campaign Standard](https://www.adobe.io/apis/experiencecloud/gdpr/docs.html)


### Datenschutz und verknüpfte Ressourcen {#privacy-linked-resources}

Wenn ein benutzerdefinierter Campaign-Ressourcendatensatz personenbezogene Daten enthält, die auch in Campaign verwendet werden, sollte dieser Datensatz mit einem entsprechenden Campaign-Profildatensatz verknüpft werden (entweder direkt oder über eine andere benutzerspezifische Ressource), sodass ein datenschutzbezogener Löschvorgang im Profildatensatz auch den verknüpften benutzerspezifischen Ressourcendatensatz mit personenbezogenen Daten löschen kann. Die Verknüpfungs- und Löschoptionen zwischen den Entitäten müssen so konfiguriert sein, dass eine solche kaskadierte Löschung der verknüpften Datensätze möglich wird. Personenbezogene Daten sollten nicht in benutzerdefinierte Ressourcen eingegeben werden, die nicht mit dem Profil verknüpft sind.

Hier erfahren Sie, wie Sie die Ressourcen der Kampagne und die Dynamics 365-Entitäten [in diesem Abschnitt](../../integrating/using/map-campaign-custom-resources-and-dynamics-365-custom-entities.md)zuordnen.

## Opt-out

Aufgrund der unterschiedlichen Opt-out-Attribute zwischen Dynamics 365 und Campaign sowie der unterschiedlichen Geschäftsanforderungen einzelner Kunden wurde das Opt-out-Mapping als vom Kunden auszuführende Option konzipiert. Es ist wichtig, sicherzustellen, dass Opt-outs ordnungsgemäß zwischen den Systemen zugeordnet werden, damit die Voreinstellungen für die Abmeldung des Endbenutzers beibehalten werden und sie keine Kommunikation über einen Kanal erhalten, für den sie sich entschieden haben.

Bitte beachten Sie, dass bei der Abmeldezuordnung nur Kampagnen mit dem Präfix &quot;Keine Kontaktaufnahme mehr&quot;(z.B. keine E-Mail mehr) oder mit dem spezifischen Attribut für CCPA-Abmeldung verwendet werden können. [mehr dazu](../../developing/using/datamodel-profile.md).
In Dynamics 365 haben die meisten Ausschluss-Felder das Präfix &quot;donot&quot;. Sie können jedoch auch andere Attribute für Ausschluss-Zwecke verwenden, wenn die Datentypen kompatibel sind.

Bei der Bereitstellung der Integration können Sie angeben, welche Opt-out-Konfiguration Sie für Ihr Unternehmen wünschen:

* Dynamics 365 ist die &quot;Source of Truth&quot; für Opt-outs: Opt-out-Attribute werden in eine Richtung von Dynamics 365 zu Campaign synchronisiert.
* Campaign ist die &quot;Source of Truth&quot; für Opt-outs: Opt-out-Attribute werden in einer Richtung von Campaign zu Dynamics 365 synchronisiert.
* Dynamics 365 UND Campaign sind beide &quot;Source of Truth&quot;: Opt-out-Attribute werden in beide Richtungen zwischen Campaign und Dynamics 365 synchronisiert.

Alternativ kann der Ausschluss-Datenfluss der Integration deaktiviert werden, wenn Sie über einen separaten Prozess zur Verwaltung der Abmeldesynchronisierung zwischen den Systemen verfügen.

Die bidirektionale Ausschluss-Konfiguration verwendet Logik, um zu bestimmen, welcher Wert auf beiden Systemen geschrieben werden soll. Die Logik vergleicht Zeitstempel zwischen den beiden Systemen (Änderung auf Datensatzebene in Dynamics 365, Änderung auf Attributebene in Campaign), um zu ermitteln, welches System sich durchsetzt. Wenn Campaign den aktuelleren Zeitstempel enthält, hat der Campaign-Wert Vorrang. Wenn Dynamics 365 den aktuelleren Zeitstempel enthält oder beide gleich sind, erhält opt-out=TRUE den Vorrang (vorausgesetzt, einer der Werte ist TRUE).

>[!NOTE]
>
>Bitte überprüfen Sie die standardmäßigen und spezifischen Typologieregeln in Adobe Campaign und aktualisieren Sie diese gegebenenfalls, bevor Sie hier Änderungen vornehmen, damit sie auf alle ausgehenden Nachrichten korrekt angewendet werden. Achten Sie beispielsweise darauf, dass alle Mappings zu Opt-out-Voreinstellungen die Absichten/Kommunikationsoptionen des Empfängers genau widerspiegeln und den Versand von Beziehungs- oder Transaktionsnachrichten (wie z. B. Auftragsbestätigungen des Kunden) nicht versehentlich beenden.

Wenn Sie die bidirektionale oder Kampagne auf Dynamics 365-Ausschluss-Konfiguration ausgewählt haben, werden die Ausschluss-Daten der Kampagne regelmäßig über den Workflow in Ihren SFTP-Datenspeicherung-Bereich der Kampagne exportiert (siehe &quot;Kampagne SFTP Nutzung unten&quot;). In dem Ereignis, dass Ihre Kampagne-Ausschluss-Workflows nicht mehr ausgeführt werden, müssen Sie so bald wie möglich manuell neu starten, um die Möglichkeit zu verringern, dass Sie die Ausschluss-Synchronisierung auslassen.

## Kampagne SFTP-Nutzung

Ihre Kampagne-SFTP-Datenspeicherung muss in den unten stehenden Anwendungsfällen von der Integration genutzt werden.  Sie müssen sicherstellen, dass Ihr SFTP-Konto über eine ausreichende Datenspeicherung für diese Anwendungsfälle verfügt.  Eine Überschreitung der lizenzierten SFTP-Datenspeicherung kann die funktionelle Nutzung der Kampagne, der Integration und/oder des SFTP-Kontos erheblich beeinträchtigen.

| Anwendungsbeispiel | Beschreibung  |
|---|---|
| Datenladevorgang beim Öffnen | Dynamics 365-Tabellen über 500.000 Datensätze müssen in die Kampagne SFTP-Datenspeicherung exportiert werden, um über einen Workflow importiert zu werden. Ab diesem Zeitpunkt verwendet die Integration APIs für inkrementelle Aktualisierungen. |
| Bidirektionales Opt-out und Kampagne auf Dynamics 365 (uni-direktionales Opt-out) | Bidirektionales Opt-out und Kampagne zu Dynamics 365 uni-direktionalen Ausschluss-Datenströmen nutzen die Kampagne SFTP-Datenspeicherung. Ein ACS-Workflow exportiert inkrementelle Änderungen in den SFTP-Ordner. Von dort nimmt die Integration die Datensätze und Prozesse auf. |
| Wiederherstellung nach Katastrophen | Im unwahrscheinlichen Ereignis einer Systemkatastrophe wird der &quot;Initial Data Load&quot;-Anwendungsfall befolgt, um die inkrementellen Aktualisierungen an die verpasste Kampagne zu leiten. |

## Bestehende Campaign-Daten

Durch diese Integration werden Kontakte und benutzerdefinierte Entitäten von Dynamics 365 zur Kampagne synchronisiert. Kampagnen, die außerhalb der Integration erstellt wurden (d. h. nicht vom Synchronisierungsauftrag erstellt wurden), werden von der Integration nicht verändert, einschließlich der zum Zeitpunkt der Integrationskonfiguration vorhandenen Kampagnen.

Because this integration uses the **[!UICONTROL externalId]** field in Campaign to sync Campaign profile records with Dynamics 365 contact records, this Campaign field (**[!UICONTROL externalId]** ) must be populated with the Dynamics 365 **[!UICONTROL contactId]** for the records you wish to be synced from Dynamics 365.  Benutzerdefinierte Entitäten werden auch mit einer eindeutigen Dynamics 365-ID synchronisiert. Die benutzerdefinierte Entität der Kampagne muss dieses ID-Attribut als Tabellenspalte enthalten. Die Spalte externalId kann verwendet werden, um diesen Attributwert zu speichern, ist jedoch nicht für die Kampagne benutzerdefinierter Entitäten erforderlich.

Denken Sie daran, dass Dynamics 365 immer noch die Quelle der Wahrheit ist und dass die Kampagne Profil-Daten überschrieben werden können, wenn die Integration Updates auf der Dynamics 365-Seite erkennt.  Je nach Ihrer vorhandenen Implementierung können auch andere Schritte zum Aktivieren der Integration erforderlich sein. Daher wird empfohlen, eng mit Ihrem technischen Ansprechpartner bei Adobe zusammenzuarbeiten.

>[!NOTE]
>
>Aufgrund der Komplexität vorhandener Kundenimplementierungen sollten Sie sich bei der Planung und Einrichtung der Integration von Ihrem technischen Ansprechpartner von Adobe unterstützen lassen.

## Häufigkeit der Datensynchronisierung

Die Integration nutzt eine Architektur, mit der Updates erkannt und der Verarbeitungswarteschlange hinzugefügt werden können, kurz nachdem sie in Dynamics 365 aufgetreten sind (d. h. Streaming, nicht Stapelverarbeitung). Aus diesem Grund müssen keine Datenflusslaufzeitfrequenzen oder Zeitpläne angegeben werden.

Eine Ausnahme bildet die bidirektionale Kampagne zu Dynamics 365-Ausschluss-Datenströmen. Bei diesen Ausschluss-Konfigurationen werden aktualisierte ACS-Datensätze einmal täglich über den ACS-Workflow in SFTP exportiert. Danach liest das Integrationstool die Datei und verarbeitet den Datensatz.

## Datenverwendungsvereinbarung

Wenn Sie sich in der Region EMEA oder APAC befinden, werden einige Ihrer Daten im Rahmen dieser Integration in den USA verarbeitet. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

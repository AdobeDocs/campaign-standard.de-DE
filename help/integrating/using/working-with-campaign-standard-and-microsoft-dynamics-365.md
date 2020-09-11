---
title: Erste Schritte mit der Integration von Microsoft Dynamics 365
description: Erfahren Sie, wie Sie mit der Integration von Microsoft Dynamics 365 beginnen können.
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 3590fd42e4692df6bba21ac721568ae60dfcdd65
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 43%

---


# Erste Schritte mit der Integration von Microsoft Dynamics 365

Aktivieren Sie Ihre CRM-Daten für kanalübergreifende Kommunikation: Erfahren Sie, wie Sie Kontakte von Microsoft Dynamics 365 an Adobe Campaign übertragen und Kampagnenleistungsdaten (Sendungen, Öffnungen, Klicks und Bounces) von Adobe Campaign in Microsoft Dynamics 365 freigeben können.

Unterstützte Versionen sind [in diesem Abschnitt](#support-software-versions)aufgeführt.

>[!CAUTION]
>
>Diese Funktion ist im Lieferumfang des Produkts nicht verfügbar. Die Implementierung erfordert die Einbindung von Adobe Consulting. Wenden Sie sich an Ihren Kundenbetreuer, um weitere Informationen zu erhalten.

## Grundsätze

Die Adobe Campaign- und Microsoft Dynamics 365-Integration ermöglicht die Synchronisierung aller verfügbaren Kontaktdaten im CRM-System und stellt alle relevanten Kontaktdaten für Kampagnen-Aktivitäten zur Verfügung.

Umgekehrt werden diese Daten bei Interaktion von Profilen in Adobe Campaign mit Nachrichten (z. B.: sendet, öffnet, klickt und absprünge) automatisch in Microsoft Dynamics 365 fließen, um Kontaktdatensätze auch mit der Marketing-Aktivität vollständig zu halten.

Die Integration unterstützt auch benutzerdefinierte Entitäten, sodass [benutzerdefinierte Entitäten](../../integrating/using/map-campaign-custom-resources-and-dynamics-365-custom-entities.md) in Dynamics 365 mit entsprechenden benutzerdefinierten Entitäten in der Kampagne synchronisiert werden können.

Diese Integration unterstützt vier wichtige Anwendungsfälle:

1. Synchronisieren von Kontakten von Dynamics 365 zur Kampagne, damit sie in Marketing-Kampagnen ausgerichtet werden können
1. Synchronisieren von benutzerdefinierten Entitäten von Dynamics 365 mit Campaign, damit sie zur Segmentierung und Personalisierung verwendet werden können
1. Senden von E-Mail-Marketing-Ereignissen (Sendungen, Öffnungen, Klicks, Bounces) von Campaign zu Dynamics 365 zum Bereitstellen an das Sales-Repository in der Dynamics 365-Benutzeroberfläche
1. Synchronisieren der Ausschlussstatus (z. B. keine E-Mail) zwischen Dynamics 365 und ACS, um die Datenschutzeinstellungen der Kunden beizubehalten.

## Wichtigste Vorteile

* Konsistentes Messaging zwischen Vertrieb und Marketing

Die Adobe Campaign- und Microsoft Dynamics 365-Integration ermöglicht beiden Systemen den Zugriff auf Kundeninformationen und E-Mail-Marketing-Verläufe, sodass die gesamte Nachrichtenübermittlung an den Kunden konsistent ist.

* Ganzheitliche Ansicht aller Interessenten- und Kundendaten

Durch die Integration von Adobe Campaign in Dynamics 365 ist es möglich, E-Mail-Marketingverlauf bei jedem Kontakt innerhalb des CRM-Systems freizugeben und abzurufen.

* Dynamics 365-Daten auf allen Kanälen aktivieren

Mit Kontaktdaten, die mit Adobe Campaign synchronisiert werden, können Sie unter Verwendung von Campaign über jeden Online- oder Offline-Kanal Nachrichten senden, inklusive Mobile Push, In-App, E-Mail oder Briefpost. Unabhängig vom bevorzugten Kanal jedes Kontakts haben Sie die Kampagne abgedeckt.

>[!CAUTION]
>
>Für die Synchronisierung von Kontakten und benutzerdefinierten Entitäten betrachtet diese Integration Dynamics 365 als Quelle der Wahrheit.  Änderungen an synchronisierten Attributen sollten in Dynamics 365 vorgenommen werden, nicht in der Kampagne.  Wenn Änderungen in Campaign vorgenommen werden, kann es sein, dass sie bei der Synchronisation wieder überschrieben werden.

## Support-Softwareversionen {#support-software-versions}

Für diese Integration sind die folgenden Softwareversionen erforderlich:

* Microsoft Dynamics 365 nur für Sales Online, neueste Version

* Adobe Campaign Standard, neueste Version

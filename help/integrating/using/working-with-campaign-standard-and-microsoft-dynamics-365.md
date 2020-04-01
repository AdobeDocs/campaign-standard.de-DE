---
title: Arbeiten mit Campaign Standard und Microsoft Dynamics 365
description: Erfahren Sie, wie Sie mit Campaign Standard und Microsoft Dynamics 365 arbeiten können
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 74cc176a1b93a7983629ccccb1fea00628241952

---


# Arbeiten mit Campaign Standard und Microsoft Dynamics 365

Aktivieren Sie Ihre CRM-Daten bei der Kommunikation über Kanal hinweg: Erfahren Sie, wie Sie Kontakte von Microsoft Dynamics 365 an Adobe Campaign weitergeben und Kampagnen-Leistungsdaten (Sende-, Öffnen-, Klicks- und Absprünge) wieder von Adobe Campaign an Microsoft Dynamics 365 freigeben können.

>[!NOTE]
>
>Die Integration von Microsoft Dynamics 365/Adobe Campaign Standard unterstützt nur die **Microsoft Dynamics 365 Sales-App** .

## Vorteile und Anwendungsfälle

### Grundsätze

Die Integration von Adobe Campaign und Microsoft Dynamics 365 ermöglicht die Synchronisierung aller verfügbaren Kontaktdaten im CRM-System, sodass alle relevanten Kontaktdaten für Aktivitäten der Kampagne zur Verfügung stehen.

Umgekehrt werden diese Daten (z. B.: sendet, öffnet, klickt und absprünge) automatisch in Microsoft Dynamics 365 fließen, um Kontaktdatensätze auch mit der Marketing-Aktivität zu vervollständigen.

Die neueste Version der Integration unterstützt auch benutzerdefinierte Entitäten, sodass benutzerdefinierte Entitäten in Dynamics 365 mit entsprechenden benutzerdefinierten Entitäten in der Kampagne synchronisiert werden können.

Diese Integration unterstützt drei Hauptverwendungsfälle:

1. Synchronisieren von Kontakten von Dynamics 365 zur Kampagne, damit sie in Marketing-Kampagnen ausgerichtet werden können
1. Senden von E-Mail-Marketing-Ereignissen (Senden, Öffnen, Klicks, Absprünge) von Kampagne zu Dynamics 365 zur Anzeige an das Sales-Repository in der Dynamics 365-Oberfläche
1. Synchronisieren von benutzerdefinierten Entitäten von Dynamics 365 zur Kampagne, damit sie für die Segmentierung und Personalisierung verwendet werden können

Video zur Integration von Dynamics 365-Campaign Standard [hier](https://helpx.adobe.com/campaign/kt/acs/using/acs-ms-dynamics-crm-connector-tutorial.html).

### Wichtigste Vorteile

* Konsistentes Messaging zwischen Vertrieb und Marketing

Die Integration von Adobe Campaign und Microsoft Dynamics 365 ermöglicht beiden Systemen den Zugriff auf Kundeninformationen und E-Mail-Marketingverlauf, sodass alle Nachrichten an den Kunden dieselbe konsistente Botschaft weitergeben können.

* Ganzheitliche Ansicht aller Potenzieller Kunden- und Kundendaten

Durch die Integration von Adobe Campaign in Dynamics 365 ist es möglich, E-Mail-Marketingverlauf über jeden Kontakt im CRM-System freizugeben und darauf zuzugreifen.

* Dynamics 365-Daten auf jedem Kanal aktivieren

Bei mit Adobe Campaign synchronisierten Kontaktdaten können Sie mit Kampagnen wie mobilen Push, In-App, E-Mail oder Direktversand auf jedem Online- oder Offline-Kanal Nachrichten senden. Unabhängig vom bevorzugten Kanal der einzelnen Kontakte haben Sie die Kampagne abgedeckt.

>[!CAUTION]
>
>Für die Kontaktsynchronisierung betrachtet diese Integration Dynamics 365 als die Quelle der Wahrheit.  Änderungen an synchronisierten Kontaktattributen sollten in Dynamics 365 vorgenommen werden, nicht in Kampagne.  Wenn Änderungen in der Kampagne vorgenommen werden, können sie während der Synchronisierung überschrieben werden.


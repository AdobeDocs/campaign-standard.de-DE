---
title: Erste Schritte mit Microsoft Dynamics 365
description: Erfahren Sie, wie Sie mit der Integration von Microsoft Dynamics 365 beginnen können
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
source-git-commit: 277663c4cf0e810f691eeebfade17bf8dd73698e

---


# Erste Schritte mit Microsoft Dynamics 365

Aktivieren Sie Ihre CRM-Daten bei der Kommunikation über Kanal hinweg: Erfahren Sie, wie Sie Kontakte von Microsoft Dynamics 365 an Adobe Campaign weitergeben und Kampagnen-Performance-Daten (Sende-, Öffnen-, Klicks- und Absprünge) von Adobe Campaign an Microsoft Dynamics 365 weitergeben können.

>[!NOTE]
>
>Die Microsoft Dynamics 365 / Adobe Campaign Standard Integration unterstützt nur die **Microsoft Dynamics 365 Sales App** .

## Vorteile und Anwendungsfälle

### Grundsätze

Die Adobe Campaign- und Microsoft Dynamics 365-Integration ermöglicht die Synchronisierung aller verfügbaren Kontaktdaten im CRM-System und stellt alle relevanten Kontaktdaten für Kampagnen-Aktivitäten zur Verfügung.

Umgekehrt werden diese Daten bei Interaktion von Profilen in Adobe Campaign mit Nachrichten (z. B.: sendet, öffnet, klickt und absprünge) automatisch in Microsoft Dynamics 365 fließen, um Kontaktdatensätze auch mit der Marketing-Aktivität zu vervollständigen.

Die neueste Version der Integration unterstützt auch benutzerdefinierte Entitäten, sodass benutzerdefinierte Entitäten in Dynamics 365 mit entsprechenden benutzerdefinierten Entitäten in der Kampagne synchronisiert werden können.

Diese Integration unterstützt drei Hauptverwendungsfälle:

1. Synchronisieren von Kontakten von Dynamics 365 zur Kampagne, damit sie in Marketing-Kampagnen ausgerichtet werden können
1. Senden von E-Mail-Marketing-Ereignissen (Senden, Öffnen, Klicks, Absprünge) von Kampagne zu Dynamics 365 zur Anzeige an das Sales-Repository in der Dynamics 365-Oberfläche
1. Synchronisieren von benutzerdefinierten Entitäten von Dynamics 365 zur Kampagne, damit sie für die Segmentierung und Personalisierung verwendet werden können

Video zur Integration von Dynamics 365-Campaign Standard [hier](https://helpx.adobe.com/campaign/kt/acs/using/acs-ms-dynamics-crm-connector-tutorial.html).

### Wichtigste Vorteile

* Konsistentes Messaging zwischen Vertrieb und Marketing

Die Adobe Campaign- und Microsoft Dynamics 365-Integration ermöglicht beiden Systemen den Zugriff auf Kundeninformationen und E-Mail-Marketingverlauf, sodass alle Nachrichten an den Kunden dieselbe konsistente Messaging-Funktion nutzen können.

* Ganzheitliche Ansicht aller Potenzieller Kunden- und Kundendaten

Durch die Integration von Adobe Campaign in Dynamics 365 ist es möglich, E-Mail-Marketingverlauf über jeden Kontakt im CRM-System freizugeben und darauf zuzugreifen.

* Dynamics 365-Daten auf jedem Kanal aktivieren

Mit Kontaktdaten, die mit Adobe Campaign synchronisiert werden, können Sie auf jedem Online- oder Offline-Kanal mit Kampagnen wie mobilen Push-, In-App-, E-Mail- oder Direktversand senden. Unabhängig vom bevorzugten Kanal der einzelnen Kontakte haben Sie die Kampagne abgedeckt.

>[!CAUTION]
>
>Für die Kontaktsynchronisierung betrachtet diese Integration Dynamics 365 als die Quelle der Wahrheit.  Änderungen an synchronisierten Kontaktattributen sollten in Dynamics 365 vorgenommen werden, nicht in Kampagne.  Wenn Änderungen in der Kampagne vorgenommen werden, können sie während der Synchronisierung überschrieben werden.

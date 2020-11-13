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
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '431'
ht-degree: 100%

---


# Erste Schritte mit der Integration von Microsoft Dynamics 365

Aktivieren Sie Ihre CRM-Daten für kanalübergreifende Kommunikation: Erfahren Sie, wie Sie Kontakte von Microsoft Dynamics 365 an Adobe Campaign übertragen und Kampagnenleistungsdaten (Sendungen, Öffnungen, Klicks und Bounces) von Adobe Campaign in Microsoft Dynamics 365 freigeben können.

Die unterstützten Versionen sind [in diesem Abschnitt](#support-software-versions) aufgeführt.

>[!CAUTION]
>
>Diese Funktion ist im Lieferumfang des Produkts nicht verfügbar. Die Implementierung erfordert die Einbindung von Adobe Consulting. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um weitere Informationen zu erhalten.

## Grundsätze

Die Integration zwischen Adobe Campaign Standard und Microsoft Dynamics 365 ermöglicht eine Synchronisation aller verfügbaren Kontaktdaten im CRM-System, sodass alle relevanten Kontaktdaten für Kampagnenaktivitäten verfügbar sind.

Umgekehrt werden in Adobe Campaign bei der Interaktion von Profilen mit Nachrichten diese Daten (z. B. Sendungen, Öffnungen, Klicks und Bounces) automatisch an Microsoft Dynamics 365 übermittelt, sodass Kontaktdatensätzen Marketing-Aktivitäten hinzugefügt werden.

Die Integration unterstützt auch benutzerdefinierte Entitäten, sodass [benutzerdefinierte Entitäten](../../integrating/using/map-campaign-custom-resources-and-dynamics-365-custom-entities.md) in Dynamics 365 mit entsprechenden benutzerdefinierten Entitäten in der Kampagne synchronisiert werden können.

Diese Integration unterstützt vier Hauptanwendungsfälle:

1. Synchronisieren von Kontakten von Dynamics 365 mit Campaign, damit sie in Marketing-Kampagnen für Zielgruppen ausgewählt werden können
1. Synchronisieren von benutzerdefinierten Entitäten von Dynamics 365 mit Campaign, damit sie zur Segmentierung und Personalisierung verwendet werden können
1. Senden von E-Mail-Marketing-Ereignissen (Sendungen, Öffnungen, Klicks, Bounces) von Campaign zu Dynamics 365 zum Bereitstellen an das Sales-Repository in der Dynamics 365-Benutzeroberfläche
1. Synchronisieren der Opt-out-Status (z. B. keine E-Mail) zwischen Dynamics 365 und ACS, um die Datenschutzeinstellungen der Kunden einzuhalten.

## Wichtigste Vorteile

* Konsistentes Messaging zwischen Vertrieb und Marketing

Die Adobe Campaign- und Microsoft Dynamics 365-Integration ermöglicht beiden Systemen den Zugriff auf Kundeninformationen und E-Mail-Marketing-Verläufe, sodass die gesamte Nachrichtenübermittlung an den Kunden konsistent ist.

* Ganzheitliche Ansicht aller Interessenten- und Kundendaten

Durch die Integration von Adobe Campaign mit Dynamics 365 ist es möglich, den E-Mail-Marketing-Verlauf für einzelne Kontakte im CRM-System freizugeben und darauf zuzugreifen.

* Dynamics 365-Daten auf allen Kanälen aktivieren

Mit Kontaktdaten, die mit Adobe Campaign synchronisiert werden, können Sie unter Verwendung von Campaign über jeden Online- oder Offline-Kanal Nachrichten senden, inklusive Mobile Push, In-App, E-Mail oder Briefpost. Unabhängig vom bevorzugten Kanal der einzelnen Kontakte unterstützt Campaign alle Kanäle.

>[!CAUTION]
>
>Für die Synchronisation von Kontakten und benutzerdefinierten Entitäten betrachtet diese Integration Dynamics 365 als &quot;Source of Truth&quot;.  Änderungen an synchronisierten Attributen sollten in Dynamics 365 und nicht in Campaign vorgenommen werden.  Wenn Änderungen in Campaign vorgenommen werden, kann es sein, dass sie bei der Synchronisation wieder überschrieben werden.

## Unterstützte Software-Versionen {#support-software-versions}

Für diese Integration sind die folgenden Software-Versionen erforderlich:

* Nur Microsoft Dynamics 365 for Sales Online, neueste Version

* Adobe Campaign Standard, neueste Version

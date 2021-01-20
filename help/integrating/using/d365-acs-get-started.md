---
title: Erste Schritte mit der Integration von Microsoft Dynamics 365
description: Erfahren Sie, wie Sie mit der Integration von Microsoft Dynamics 365 beginnen können.
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
translation-type: tm+mt
source-git-commit: fe5d40235abc33c0ea7e929cd2e69b7030cea0b1
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 42%

---


# Erste Schritte mit der Integration von Microsoft Dynamics 365

Aktivieren Sie Ihre CRM-Daten für kanalübergreifende Kommunikation: Erfahren Sie, wie Sie Kontakte von Microsoft Dynamics 365 an Adobe Campaign übertragen und Kampagnenleistungsdaten (Sendungen, Öffnungen, Klicks und Bounces) von Adobe Campaign in Microsoft Dynamics 365 freigeben können.

Für diese Integration sind die folgenden Software-Versionen erforderlich:

* Nur Microsoft Dynamics 365 for Sales Online, neueste Version

* Adobe Campaign Standard, neueste Version

>[!CAUTION]
>
>Diese Funktion ist im Lieferumfang des Produkts nicht verfügbar. Die Implementierung erfordert die Einbindung von Adobe Consulting. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um weitere Informationen zu erhalten.


## Grundsätze

Die Adobe Campaign Standard Integration mit Microsoft Dynamics 365 ermöglicht die Synchronisierung aller verfügbaren Kontaktdaten im CRM-System, sodass alle relevanten Kontaktdaten für Kampagnen-Aktivitäten zur Verfügung stehen.

Umgekehrt werden diese Daten, wenn Profil innerhalb von Adobe Campaign Standard mit Nachrichten interagieren (z. B.: sendet, öffnet, klickt und absprünge) automatisch in Microsoft Dynamics 365 fließen, um Kontaktdatensätze auch mit der Marketing-Aktivität vollständig zu halten.

Die Integration unterstützt auch die Synchronisierung von [benutzerdefinierten Entitäten](../../integrating/using/d365-acs-self-service-app-settings.md) in Dynamics 365 mit entsprechenden **benutzerdefinierten Ressourcen** in der Kampagne.

Diese Integration unterstützt vier Hauptanwendungsfälle:

1. Synchronisieren von Kontakten von Dynamics 365 mit Campaign, damit sie in Marketing-Kampagnen für Zielgruppen ausgewählt werden können
1. Synchronisieren von benutzerdefinierten Entitäten von Dynamics 365 mit Campaign, damit sie zur Segmentierung und Personalisierung verwendet werden können
1. Senden von E-Mail-Marketing-Ereignissen (Sendungen, Öffnungen, Klicks, Bounces) von Campaign zu Dynamics 365 zum Bereitstellen an das Sales-Repository in der Dynamics 365-Benutzeroberfläche
1. Synchronisieren der Ausschlussstatus (z. B. keine E-Mail) zwischen Dynamics 365 und der Kampagne, um die Datenschutzeinstellungen der Kunden beizubehalten.

Die wichtigsten Vorteile sind:

* Konsistentes Messaging zwischen Vertrieb und Marketing: Die Integration von Adobe Campaign Standard mit Dynamics 365 ermöglicht beiden Systemen den Zugriff auf Kundeninformationen und E-Mail-Marketingverlauf, sodass alle Nachrichten an den Kunden dieselbe konsistente Botschaft weitergeben können.

* Ganzheitliche Ansicht aller Potenzieller Kunden- und Kundendaten: Durch die Integration von Adobe Campaign Standard mit Dynamics 365 ist es möglich, E-Mail-Marketingverlauf bei jedem Kontakt innerhalb des CRM-Systems freizugeben und darauf zuzugreifen.

* Dynamics 365-Daten auf einem beliebigen Kanal aktivieren: Bei mit Adobe Campaign synchronisierten Kontaktdaten kann die Kommunikation auf jedem Online- oder Offline-Kanal mit Kampagne wie mobilen Push-, In-App-, E-Mail- oder Direktversand gesendet werden. Kampagne &quot;hat Sie abgedeckt&quot;, unabhängig vom bevorzugten Kanal jedes Kontakts.

>[!CAUTION]
>
>Diese Integration betrachtet Dynamics 365 als die Quelle der Wahrheit für die Kontakt- und benutzerdefinierte Entitätssynchronisierung.  Änderungen an synchronisierten Attributen sollten in Dynamics 365, nicht in Adobe Campaign Standard vorgenommen werden.  Wenn Änderungen in Campaign vorgenommen werden, kann es sein, dass sie bei der Synchronisation wieder überschrieben werden.


## Wichtige Schritte zur Implementierung der Microsoft Dynamics 365-Integration{#request-and-implement-this-integration}

Um diese Integration bereitzustellen, müssen Sie die folgenden Schritte ausführen.

Bitte folgen Sie dem unten stehenden Flussdiagramm und den entsprechenden Details, um die Integration anzufordern und zu konfigurieren.

![](assets/provisioning-wf.png)

Details des Flussdiagramms (sind mit den oben genannten Schritten verknüpft):

* **Schritt 1**: Es wird davon ausgegangen, dass Sie bereits über eine Lizenz für Microsoft Dynamics 365 for Sales und für Adobe Campaign Standard verfügen oder diese gerade erwerben.
* **Schritt 2**  - Das Standardangebot für die Integration ist für alle Kunden kostenlos. jedoch können je nach Bedarf zusätzliche Kosten anfallen. Weitere Informationen zu [Best Practices und Einschränkungen](../../integrating/using/d365-acs-notices-and-recommendations.md). Ein neuer Auftrag (SO) muss unterzeichnet werden, um die Integration nutzen zu können, wenn er nicht in der ursprünglichen SO enthalten war.
* **Schritt 3**: Vollständige Vorintegrationsschritte für Dynamics 365 und Campaign. Siehe [Diese Integration konfigurieren](#configure-this-integration).
* **Schritt 4**  - Das Adobe-Onboarding-Team bietet Ihnen Zugriff auf die Benutzeroberfläche der Integrationsanwendung (UI).
* **Schritt 5**  - Sie können Ihre Datenzuordnungen, Ersetzungen, Filter usw. konfigurieren. und testen Sie Ihre Integration über die Benutzeroberfläche der Integrationsanwendung.

   >[!IMPORTANT]
   >
   > Wenn Sie die bidirektionale oder Kampagne auf Dynamics 365-Ausschluss-Konfiguration benötigen, müssen Sie die Anfrage an Ihren technischen Ansprechpartner bei Ihrer Adobe richten, damit die Ausschluss-Workflows auf Ihrer Kampagne eingerichtet werden kann. [Weitere Informationen](../../integrating/using/d365-acs-notices-and-recommendations.md#opt-out).

### Diese Integration konfigurieren {#configure-this-integration}

Für diese Integration müssen drei Systeme bereitgestellt und konfiguriert werden:

* **Adobe Campaign Standard**: Sie müssen den API-Zugriff einrichten und eine neue Integration für das Integrationstool konfigurieren. Lesen Sie dazu [diesen Artikel](../../integrating/using/d365-acs-configure-adobe-io.md).
* **Microsoft Dynamics 365**: Sie müssen eine neue App-Registrierung erstellen und einem Anwendungsbenutzer die Verwendung der Integration ermöglichen.  Informationen zum Konfigurieren von Microsoft Dynamics 365 für diese Integration finden Sie in [diesem Artikel](../../integrating/using/d365-acs-configure-d365.md).
* **Adobe Campaign Standard-Integration mit Microsoft Dynamics 365 Self-Service-App**: Sie müssen die Schritte in  [diesem Artikel](../../integrating/using/d365-acs-self-service-app-control-access.md) ausführen.

>[!IMPORTANT]
>
>Für jedes System müssen diese Schritte von einem **administrator** ausgeführt werden.
>
>Die Schritte in dieser Dokumentation führen Sie durch das Erstellen von Integrationen/Registrierungen, bei denen Berechtigungen und/oder Administratorzugriff zugewiesen werden.  Sie müssen vor der Ausführung sicherstellen, dass diese Schritte den Richtlinien Ihres Unternehmens entsprechen, und die Schritte dann sorgfältig durchführen.


### Support anfordern

Support-Tickets können beim Kundendienst der Adobe protokolliert werden.

Bei Problemen mit dem Integrationsdatenfluss sollten Sie neben den folgenden Informationen auch die Report Suite als Teil der Problembeschreibung angeben:

* **Prozessverantwortlicher**: Technische Architekten
* **ES-Prozess-ID**: Wurde während des Onboarding-Prozesses bereitgestellt
* **Prozesstitel**: Microsoft Dynamics 365/Adobe Campaign Standard-Integration
* **Problembeschreibung**: Beschreibung des Problems

Support für die Integration ist derzeit rund um die Uhr verfügbar (Montag bis Freitag, ausgenommen Feiertage und Betriebsferien von Adobe).

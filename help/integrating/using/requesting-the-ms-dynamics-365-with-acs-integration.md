---
title: Microsoft Dynamics 365-Integration anfordern und konfigurieren
description: Erfahren Sie, wie Sie die Konfiguration von Microsoft Dynamics 365 mit Campaign Standard anfordern und konfigurieren können.
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
source-git-commit: e90f878814e65a9a61ee4013d94fd0bf3b1f7875
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 35%

---


# Microsoft Dynamics 365-Integration anfordern und konfigurieren

Um diese Integration bereitzustellen, müssen Sie die folgenden Schritte ausführen.

Bitte folgen Sie dem unten stehenden Flussdiagramm und den entsprechenden Details, um die Integration anzufordern und zu konfigurieren.

![](assets/provisioning-wf.png)

Details des Flussdiagramms (sind mit den oben genannten Schritten verknüpft):

* **Schritt 1** - Es wird davon ausgegangen, dass Sie bereits eine Lizenz für Microsoft Dynamics 365 für Vertrieb und für Adobe Campaign Standard besitzen oder sich im Prozess der Beschaffung befinden.

* **Schritt 2** - Das standardmäßige Integrationsangebot steht allen Kunden kostenlos zur Verfügung. jedoch können je nach Bedarf zusätzliche Kosten anfallen (siehe [Integrationsgarantien und -grenzen](../../integrating/using/ms-dynamics-365-integration-guardrails.md)). Um die Integration nutzen zu können, muss ein neuer Auftrag unterzeichnet werden.

* **Schritt 3** - Vollständige Vorintegrationsschritte für Dynamics 365 und Kampagne. Siehe [Diese Integration](#configure-this-integration)konfigurieren.

* **Schritte 4-7** - Die Adobe über das Bordteam wird mit Ihnen während des Einstiegsprozesses zusammenarbeiten.

## Diese Integration konfigurieren {#configure-this-integration}

Für diese Integration müssen drei Systeme bereitgestellt und konfiguriert werden: Adobe Campaign Standard, Microsoft Dynamics 365 für Vertrieb und das Integrationstool. Links zu Konfigurationsartikeln finden Sie unten.

>[!CAUTION]
>
>Für jedes System müssen diese Schritte von einem Administrator ausgeführt werden.
>
>Die Schritte in den unten stehenden Artikeln führen Sie durch das Erstellen von Integrationen/Registrierungen, die das Zuweisen von Administratorberechtigungen und/oder Administratorzugriff beinhalten.  Sie müssen vor der Ausführung sicherstellen, dass diese Schritte den Richtlinien Ihres Unternehmens entsprechen, und die Schritte dann sorgfältig durchführen.

In ADOBE CAMPAIGN müssen Sie den API-Zugriff einrichten und eine neue Integration für das Integrationstool konfigurieren. Lesen Sie dazu [diesen Artikel](../../integrating/using/configure-adobe-io-for-ms-dynamic.md).

In MICROSOFT DYNAMICS 365 müssen Sie eine neue App-Registrierung erstellen und einen Anwender für die Verwendung der Integration aktivieren.  Informationen zum Konfigurieren von Microsoft Dynamics 365 für diese Integration finden Sie in [diesem Artikel](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

Sie müssen mit dem Adobe on boarding-Team zusammenarbeiten, um die Konfiguration für die Datenflüsse für die Ein- und Ausstieg und Abmeldung einzurichten.


## Support anfordern

Support-Tickets können wie gewohnt bei der Adobe Custom Care protokolliert werden. Die Kundenunterstützung bringt bei Bedarf Support-Mitarbeiter ein.

Bei Problemen mit Integrationsdatenflüssen sollten Sie die Report Suite als Teil der Problembeschreibung sowie die folgenden Informationen berücksichtigen:

* Prozesseigentümer: Ingenieurarchitekten

* ES-Prozess-ID: [Während des Einbogens bereitgestellt]

* Prozesstitel: Dynamics 365/Adobe Campaign Standard-Integration

* Beschreibung des Problems: [Beschreibung des Problems]

Der Integrationssupport ist derzeit rund um die Uhr verfügbar (Montag bis Freitag, ausgenommen Feiertage und Pausen der Adobe).
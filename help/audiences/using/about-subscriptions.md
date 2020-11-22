---
solution: Campaign Standard
product: campaign
title: Über Abonnements
description: Erfahren Sie mehr über Dienste und Abonnements in Campaign Standard.
audience: audiences
content-type: reference
topic-tags: managing-subscriptions
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 100%

---


# Über Abonnements{#about-subscriptions}

In Adobe Campaign können Sie Newsletter und kanalübergreifende Sendungen mithilfe einer Reihe von **Diensten** erstellen und verwalten. Dabei können Nachrichten nur an Profile gesendet werden, die sich ausdrücklich für den Dienst angemeldet haben. Diese Profile werden mithilfe eines speziellen Filters bei der Erstellung einer Nachricht identifiziert.

Sie können Anmeldemechanismen einrichten, um Ihren Kunden die Möglichkeit zu geben, sich vor allem über **E-Mails** und **Landingpages** für diese Dienste anzumelden.

Jeder Dienst ist mit folgenden Mechanismen ausgestattet:

* Mechanismen zur **Anmeldung** (Opt-in) und **[!UICONTROL Abmeldung]** (Opt-out).
* Vorhandensein von **Mechanismen zur Bestätigung** von An- und/oder Abmeldung.
* Verfolgung des **Verlaufs** von An- und Abmeldungen.

Abonnements können auch mithilfe der Adobe Campaign Standard API verwaltet werden. Weiterführende Informationen finden Sie in der [entsprechenden Dokumentation](../../api/using/creating-a-service.md).

## Wichtige Schritte zum Einrichten und Verwalten von Abonnements

Gehen Sie wie folgt vor, um einen Abonnement-Mechanismus zu erstellen:

1. **Erstellen eines Dienstes** – führen Sie die [in diesem Abschnitt](../../audiences/using/creating-a-service.md) beschriebenen Schritte aus, um einen Abonnementdienst zu erstellen.
1. **Link freigeben** – erfahren Sie [auf dieser Seite](../../audiences/using/promoting-a-service.md), wie Sie Ihren Dienst fördern und freigeben können.
1. **Abonnements überwachen** – [in diesem Abschnitt](../../audiences/using/monitoring-subscriptions.md) finden Sie mehrere Möglichkeiten, Abonnements zu Ihrem Dienst zu überwachen.
1. **Abonnements bestätigen** – folgen Sie [diesem Tutorial](../../audiences/using/confirming-subscription-to-a-service.md), um eine Nachricht über eine Anmeldebestätigung zu senden.

## Zusätzliche Ressourcen

* [Anwendungsfall: Inkrementelle Abfrage bezüglich Dienst-Abonnenten](../../automating/using/incremental-query-on-subscribers.md)
* [Anwendungsfall: Mehrere Abonnementstatus über eine Datei aktualisieren](../../automating/using/updating-subscriptions-from-file.md)
* [Profile bei einem spezifischen Dienst nach dem Import einer Datei anmelden](../../automating/using/subscribing-profiles-from-file.md)
* [Opt-in- und Opt-out-Verfahren in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

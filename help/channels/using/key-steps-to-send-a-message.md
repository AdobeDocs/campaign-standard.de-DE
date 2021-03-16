---
solution: Campaign Standard
product: campaign
title: Wichtigste Schritte im Nachrichtenversand
description: Diese Schritte zeigen Ihnen, wie Sie Nachrichten mit Adobe Campaign erstellen und senden können.
audience: channels
content-type: reference
topic-tags: about-communication-channels
feature: 'Übersicht  '
role: Geschäftspraktiker
level: Anfänger
translation-type: tm+mt
source-git-commit: a7a1aa2841410674597264927325c073fef4ce26
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 19%

---


# Wichtigste Schritte im Nachrichtenversand{#key-steps-to-send-a-message}

In diesem Abschnitt erfahren Sie, wie Sie personalisierte Nachrichten mit Adobe Campaign Standard erstellen und an eine zielgerichtete Audience senden.

Spezifische Informationen zum Erstellen und Konfigurieren der einzelnen Kommunikations-Kanal finden Sie in den folgenden Abschnitten:

* [E-Mails erstellen](../../channels/using/creating-an-email.md) 
* [SMS erstellen](../../channels/using/creating-an-sms-message.md)
* [Briefpost-Versand erstellen](../../channels/using/creating-the-direct-mail.md)
* [Erstellen einer Push-Benachrichtigung](../../channels/using/preparing-and-sending-a-push-notification.md).
* [In-App-Nachricht vorbereiten und senden](../../channels/using/preparing-and-sending-an-in-app-message.md)

Um etwas über die Best Practices beim Versand zu erfahren, besuchen Sie den Abschnitt [Best Practices beim Versand](../../sending/using/delivery-best-practices.md).

## Nachricht erstellen

Nutzen Sie Campaign Standard [Marketing-Aktivitäten](../../start/using/marketing-activities.md), um eine E-Mail, eine SMS, eine Direktnachricht, eine Push-Benachrichtigung oder eine In-App-Nachricht zu erstellen.

![](assets/marketing-activities.png)

Nachrichten können entweder aus der Liste der Marketingaktivitäten oder aus einem Workflow mit [dedizierten Aktivitäten](../../automating/using/about-channel-activities.md) erstellt werden.

![](assets/steps-channel.png)

## Audience definieren

Definieren Sie die Empfänger Ihrer Nachricht. Verwenden Sie dazu den Editor [Abfrage](../../automating/using/editing-queries.md) im linken Bereich, um die in Ihrer Datenbank enthaltenen Daten zu filtern und Regeln zur Zielgruppe Ihrer Audience zu erstellen.

Es stehen verschiedene Audiencen zur Verfügung:

* **[!UICONTROL Targetis]** ist die wichtigste Zielgruppe Ihrer E-Mail,
* **[!UICONTROL Testprofile]** sind die Profil, mit denen Sie Ihre E-Mail testen und validieren können (siehe  [Verwalten von Test-Profilen](../../audiences/using/managing-test-profiles.md)).

![](assets/steps-audience.png)

## Entwerfen und Anpassen von Inhalten

Entwerfen und personalisieren Sie im Block **[!UICONTROL Content]** den Inhalt Ihrer Nachricht mithilfe von Feldern aus Ihrer Datenbank. Weitere Informationen zum Entwerfen von Inhalten für einen bestimmten Kanal finden Sie in den Abschnitten oben auf dieser Seite.

![](assets/steps-content.png)

## Vorbereiten und Testen

[Die Nachricht ](../../sending/using/preparing-the-send.md) vorbereiten. Während dieses Vorgangs werden die Zielpopulation berechnet und die personalisierte Nachricht vorbereitet.

![](assets/steps-prepare.png)

**Überprüfen und testen Sie Ihre** Nachricht, bevor Sie sie mit den Campaign Standard-Funktionen senden: Vorschau, E-Mail-Rendering, Proof usw. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/previewing-messages.md).

Verwenden Sie den Block **[!UICONTROL Planen]**, um zu definieren, wann Ihre Nachrichten gesendet werden (siehe [Planen von Nachrichten](../../sending/using/about-scheduling-messages.md)).

![](assets/steps-schedule.png)

## Senden und verfolgen

Sobald die Nachricht fertig ist, können Sie den Versand bestätigen. Der Block **[!UICONTROL Bereitstellung]** zeigt den Sendefortschritt und das Ergebnis an.

![](assets/steps-send.png)

Es stehen mehrere Protokolle zur Verfügung, mit denen Sie den Versand Ihrer Nachrichten überwachen können (siehe [Überwachung eines Versands](../../sending/using/monitoring-a-delivery.md)). Sie können auch das Verhalten Ihrer Versand-Empfänger verfolgen, dank der [Verfolgungsfunktionen des Campaign Standards](../../sending/using/tracking-messages.md).

![](../../sending/using/assets/tracking_logs.png)

Messen Sie die Effektivität Ihrer Nachrichten und die Entwicklung Ihrer Sends und Kampagnen anhand verschiedener Indikatoren und Diagramme (siehe [Zugriff auf Berichte](../../reporting/using/about-dynamic-reports.md)).

![](assets/steps-reports.png)

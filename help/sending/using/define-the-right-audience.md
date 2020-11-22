---
solution: Campaign Standard
product: campaign
title: Festlegen der richtigen Audience
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
translation-type: tm+mt
source-git-commit: a7300666587362048431d0bafacc317170b317aa
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 100%

---


# Festlegen der richtigen Audience {#define-the-right-audience}

Die Bestimmung der Zielgruppen ist besonders wichtig. Gehen Sie bei der Erstellung Ihrer Kontaktlisten sorgfältig vor, testen Sie Ihre E-Mails in den gängigsten E-Mail-Clients, Smartphones und Tablets und stellen Sie sicher, dass Ihre Verteilerlisten aktuell sind (und keine unbekannten oder veralteten Adressen enthalten). Sie können auch Testsendungen vornehmen, um einen vollständigen Validierungszyklus durchzuführen.

Weiterführende Informationen zu Zielgruppen finden Sie in [diesem Abschnitt](../../audiences/using/selecting-an-audience-in-a-message.md).

## Ansprechen der richtigen Audience {#target-the-right-audience}

Wenn Ihr Inhalt fertiggestellt ist, müssen Sie sorgfältig auswählen, wer Ihre Nachricht erhalten soll.

Um einen erfolgreichen Versand durchzuführen, müssen Sie möglichst relevanten personalisierten Inhalt an die richtigen Empfänger senden. Mit Adobe Campaign können Sie eine präzise Zielgruppe bestimmen, indem Sie die Empfänger nach Alter, Ort, Einkäufen, Klicks auf frühere Sendungen usw. auswählen. Sie können mit Adobe Campaign auch Testprofile und Kontrollgruppen definieren und Testsendungen durchführen, um sicherzustellen, dass Sie die richtige Zielgruppe erreichen.

## Zielgruppen-Mappings {#target-mappings}

Standardmäßig werden bei Versandvorlagen **Profile** angesprochen. Adobe Campaign ermöglicht aber auch andere Zielgruppen-Mappings für Ihre Sendungen, die Sie entsprechend Ihren Anforderungen anpassen können.

Diese Zuordnungen (Mapping) werden [in diesem Abschnitt](../../automating/using/query.md#targeting-dimensions-and-resources) dargestellt.

Sie können auch ein benutzerdefiniertes Zielgruppen-Mapping erstellen und verwenden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../administration/using/target-mappings-in-campaign.md).

## Externe Daten {#external-data}

Sie können Nachrichten an Empfänger senden, die in einer externen Datei anstatt in der Datenbank gespeichert sind. Zu diesem Zweck entwerfen Sie einen Workflow, der Daten aus einer Datei in Ihre Datenbank lädt und eine zugeordnete Audience erstellt. Weitere Informationen finden Sie [in diesem Anwendungsbeispiel](../../automating/using/use-case-calling-workflow.md). Siehe auch [Aufrufen eines Workflows mit Parametern](../../automating/using/calling-a-workflow-with-external-parameters.md).

## Versand an Ihre Abonnenten {#send-to-subscribers}

Um den Abonnenten eines Newsletters Nachrichten zu senden, können Sie die Abonnenten des jeweiligen Informationsdienstes direkt anschreiben. Weiterführende Informationen finden Sie [in diesem Abschnitt](../../audiences/using/about-subscriptions.md).

**Tipp** – Sie können eine Listenzielgruppe erstellen, die mit Hilfe eines Workflows die Abonnenten Ihres Newsletters anspricht. Sie können diese Audience dann in einem Versand auswählen. Weiterführende Informationen dazu finden Sie im Abschnitt [Erstellung von Listenzielgruppen](../../audiences/using/creating-audiences.md#creating-list-audiences).

## Testsendungen, Testprofile und Kontrollgruppen {#proofs-test-control-groups}

Nutzen Sie Testsendungen, bevor Sie Ihre Nachricht an die Hauptzielgruppe senden.
Achten Sie darauf, geeignete Testversand-Empfänger auszuwählen, da diese die Form und den Inhalt Ihrer Nachricht validieren. Die Schritte zur Durchführung von Testsendungen werden [in diesem Abschnitt](../../sending/using/sending-proofs.md) beschrieben.

Weiterführende Informationen zu Testprofilen finden Sie in [diesem Abschnitt](../../audiences/using/managing-test-profiles.md).

Sie können jetzt [Kontrollgruppen](../../sending/using/control-group.md) verwenden, um die Wirkung Ihrer Kampagnen zu messen, indem Sie einen Teil ihrer Audience ausschließen. Sie können dann das Verhalten der Zielpopulation, die die Nachricht erhalten hat, mit dem Verhalten der Kontakte vergleichen, die nicht in der Zielpopulation enthalten waren. Anhand der Versandlogs können Sie auch eine Kontrollgruppe in zukünftigen Kampagnen auswählen.

## Deduplizieren von Adressen {#deduplicate-addresses}

Vermeiden Sie doppelte E-Mail-Adressen, da sich dies auf Ihre Zielgruppe auswirken kann:

* Wenn eine Zielgruppe geteilt wird, kann es vorkommen, dass dieselbe Nachricht öfter als ein Mal gesendet wird.

* Wenn sich ein Empfänger nach dem Erhalt einer Nachricht abmeldet, könnten an sein dupliziertes Profil weiterhin Nachrichten gesendet werden.

Die Deduplizierung von Adressen schützt Ihre Reputation und gewährleistet eine gute Quarantäneverwaltung.

Weitere Informationen finden Sie [in diesem Anwendungsbeispiel](../../automating/using/deduplicating-data-imported-file.md).

---
title: Festlegen der richtigen Zielgruppe
seo-title: Festlegen der richtigen Zielgruppe
page-status-flag: never-activated
uuid: a540efc7-105d-4c7f-a2ee-ade4d22b3445
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
discoiquuid: 0cbc4e92-482f-4dac-a1fb-b738e7127938
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: d5d9d50474142306457a8c76a24388c3c574791d
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 69%

---


# Festlegen der richtigen Zielgruppe {#define-the-right-audience}

Die Bestimmung der Zielgruppen ist besonders wichtig. Gehen Sie bei der Erstellung Ihrer Kontaktlisten sorgfältig vor, testen Sie Ihre E-Mails in den gängigsten E-Mail-Clients, Smartphones und Tablets und stellen Sie sicher, dass Ihre Verteilerlisten aktuell sind (und keine unbekannten oder veralteten Adressen enthalten). Sie können auch Testsendungen vornehmen, um einen vollständigen Validierungszyklus durchzuführen.

Weiterführende Informationen zu Zielgruppen finden Sie in [diesem Abschnitt](../../audiences/using/selecting-an-audience-in-a-message.md).

## Ansprechen der richtigen Zielgruppe {#target-the-right-audience}

Wenn Ihr Inhalt fertiggestellt ist, müssen Sie sorgfältig auswählen, wer Ihre Nachricht erhalten soll.

Um einen erfolgreichen Versand durchzuführen, müssen Sie möglichst relevanten personalisierten Inhalt an die richtigen Empfänger senden. Mit Adobe Campaign können Sie eine präzise Zielgruppe bestimmen, indem Sie die Empfänger nach Alter, Ort, Einkäufen, Klicks auf frühere Sendungen usw. auswählen. Sie können mit Adobe Campaign auch Testprofile und Kontrollgruppen definieren und Testsendungen durchführen, um sicherzustellen, dass Sie die richtige Zielgruppe erreichen.

## Zielgruppen-Mappings {#target-mappings}

Standardmäßig werden bei Versandvorlagen **Profil** Zielgruppe. Adobe Campaign ermöglicht aber auch andere Zielgruppen-Mappings für Ihre Sendungen, die Sie entsprechend Ihren Anforderungen anpassen können.

Diese Zuordnungen (Mapping) werden [in diesem Abschnitt](../../automating/using/query.md#targeting-dimensions-and-resources) dargestellt.

Sie können auch ein benutzerdefiniertes Zielgruppen-Mapping erstellen und verwenden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../administration/using/target-mappings-in-campaign.md).

## Externe Daten {#external-data}

Sie können Nachrichten an Empfänger senden, die in einer externen Datei anstatt in der Datenbank gespeichert sind. Dazu wird ein Workflow zum Laden von Daten aus einer Datei in Ihre Datenbank und zum Erstellen einer zugehörigen Audience eingesetzt.  Weitere Informationen finden Sie [in diesem Anwendungsbeispiel](../../automating/using/use-case-calling-workflow.md). Siehe auch [Aufrufen eines Workflows mit Parametern](../../automating/using/calling-a-workflow-with-external-parameters.md).

## Versand an Ihre Abonnenten {#send-to-subscribers}

Um den Abonnenten eines Newsletters Nachrichten zu senden, können Sie die Abonnenten des jeweiligen Informationsdienstes direkt anschreiben. Weiterführende Informationen finden Sie [in diesem Abschnitt](../../audiences/using/about-subscriptions.md).

**Tipp** : Sie können eine Audience zur Liste erstellen, mit der die Abonnenten mithilfe eines Workflows zum Newsletter Zielgruppe werden. Sie können diese Audience dann in einem Versand auswählen. For more on this, see [Creating list audiences](../../audiences/using/creating-audiences.md#creating-list-audiences).

## Testversand, Test-Profil und Kontrollgruppen {#proofs-test-control-groups}

Nutzen Sie Testsendungen, bevor Sie Ihre Nachricht an die Hauptzielgruppe senden.
Achten Sie darauf, geeignete Testversand-Empfänger auszuwählen, da diese die Form und den Inhalt Ihrer Nachricht validieren. Die Schritte zum Senden von Testversänden werden [in diesem Abschnitt](../../sending/using/sending-proofs.md)beschrieben.

Learn more about test profiles [in this section](../../audiences/using/managing-test-profiles.md).

Sie können [Kontrollgruppen](../../sending/using/control-group.md) verwenden, um die Auswirkungen Ihrer Kampagnen zu messen, indem Sie einen Teil ihrer Audience ausschließen. Sie können dann das Verhalten der Zielgruppe, die die Nachricht erhalten hat, mit dem Verhalten der nicht zielgerichteten Kontakte vergleichen. Auf der Grundlage der gesendeten Protokolle können Sie auch eine Kontrollgruppe in zukünftigen Kampagnen Zielgruppe werden.

## Deduplizieren von Adressen {#deduplicate-addresses}

Vermeiden Sie doppelte E-Mail-Adressen, da sich dies auf Ihre Zielgruppe auswirken kann:

* Wenn eine Zielgruppe geteilt wird, kann es vorkommen, dass dieselbe Nachricht öfter als ein Mal gesendet wird.

* Wenn sich ein Empfänger nach dem Erhalt einer Nachricht abmeldet, könnten an sein dupliziertes Profil weiterhin Nachrichten gesendet werden.

Die Deduplizierung von Adressen schützt Ihre Reputation und gewährleistet eine gute Quarantäneverwaltung.

Weitere Informationen finden Sie [in diesem Anwendungsbeispiel](../../automating/using/deduplicating-data-imported-file.md).

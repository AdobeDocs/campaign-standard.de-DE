---
title: Briefpost-Audience definieren
description: Hier erfahren Sie, wie Sie die Zielgruppe für Ihren Briefpostversand definieren.
page-status-flag: never-activated
uuid: f843e368-5c07-4b53-8943-46f7bf45b62b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: direct-mail
discoiquuid: f993d1b6-4b9a-4f95-81fc-60c126211bd2
context-tags: delivery,directMailContent,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Briefpost-Audience definieren{#defining-the-direct-mail-audience}

Sie können die Audience entweder im Erstellungsassistenten oder durch Klicken in den Bereich **Audience** im Versand-Dashboard festlegen.

![](assets/direct_mail_15.png)

## Hauptzielgruppe definieren    {#defining-the-main-target}

Bei Briefpost werden die Zielgruppenprofile in die Extraktionsdatei eingefügt, die Sie an Ihren Briefpost-Dienstleister senden.

Für jedes Zielgruppenprofil wird eine neue Zeile der Extraktionsdatei hinzugefügt. Die Menge der für jeden Empfänger hinzugefügten Profilinformationen wird im Bildschirm [Extraktion definieren](#defining-the-extraction) definiert.

>[!CAUTION]
>
>Achten Sie darauf, dass Ihre Profile eine Anschrift enthalten, da diese Information für den Briefpost-Dienstleister wesentlich ist. Beachten Sie außerdem, dass in der Profilinformation die Option **[!UICONTROL Anschrift angegeben]** aktiviert ist. Siehe [Empfehlungen](../../channels/using/about-direct-mail.md#recommendations).

## Hinzufügen von Test- und Trap-Profilen   {#adding-test-and-trap-profiles}

Fügen Sie Testprofile hinzu, sodass Sie Ihre Datei mit einer kleinen Anzahl von Profilen testen können. Dadurch können Sie rasch eine Beispieldatei erstellen, um ihren Aufbau zu testen und zu validieren, bevor Sie die eigentliche Datei vorbereiten. Siehe [Verwalten von Testprofilen und Senden von Testsendungen](../../sending/using/managing-test-profiles-and-sending-proofs.md).

Die Verwendung von Traps (Fallen) ist für den Briefpost-Versand besonders wichtig. Sie können damit überprüfen, ob Ihr Direkt-Mail-Anbieter die Kommunikation tatsächlich versendet, und Sie stellen sicher, dass er Ihre Kundenliste an keinen anderen Provider weiterleitet. Siehe [Verwenden von Traps](../../sending/using/managing-test-profiles-and-sending-proofs.md#using-traps).

Für den Briefpost-Versand werden Traps während der Extraktion hinzugefügt und im Ausgabedokument unter die restlichen Informationen gemischt. Standardmäßig werden Trap-Ausgaben in die Sortierreihenfolge der Ausgabedatei eingefügt. Sie können jedoch auch angeben, dass sie am Anfang oder Ende der Datei aufgeführt werden. Wählen Sie beim Definieren der Zielgruppe die gewünschte Option auf der Registerkarte **[!UICONTROL Trap-Einfügemodus]**.

![](assets/direct_mail_trap_insertion_mode.png)

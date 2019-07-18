---
title: Briefpost-Audience definieren
seo-title: Briefpost-Audience definieren
description: Briefpost-Audience definieren
seo-description: Hier erfahren Sie, wie Sie die Zielgruppe für Ihren Briefpostversand definieren.
page-status-flag: nie aktiviert
uuid: f 843 e 368-5 c 07-4 b 53-8943-46 f 7 bf 45 b 62 b
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Kanäle
content-type: Referenz
topic-tags: Direktnachricht
discoiquuid: f 993 d 1 b 6-4 b 9 a -4 f 95-81 fc -60 c 126211 bd 2
context-tags: Bereitstellung, directmailcontent, back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b0cf437ec97153b53bd4502171b24286abb25731

---


# Briefpost-Audience definieren{#defining-the-direct-mail-audience}

Sie können die Audience entweder im Erstellungsassistenten oder durch Klicken in den Bereich **Audience** im Versand-Dashboard festlegen.

![](assets/direct_mail_15.png)

## Hauptzielgruppe definieren {#defining-the-main-target}

Bei Briefpost werden die Zielgruppenprofile in die Extraktionsdatei eingefügt, die Sie an Ihren Briefpost-Dienstleister senden.

Für jedes Zielgruppenprofil wird eine neue Zeile der Extraktionsdatei hinzugefügt. Die Menge der für jeden Empfänger hinzugefügten Profilinformationen wird im Bildschirm [Extraktion definieren](../../channels/using/defining-the-direct-mail-content.md#defining-the-extraction) definiert.

>[!CAUTION]
>
>Achten Sie darauf, dass Ihre Profile eine Anschrift enthalten, da diese Information für den Briefpost-Dienstleister wesentlich ist. Beachten Sie außerdem, dass in der Profilinformation die Option **[!UICONTROL Anschrift angegeben]aktiviert ist.** Siehe [Empfehlungen](../../channels/using/about-direct-mail.md#recommendations).

## Test- und Fallen-Profile hinzufügen {#adding-test-and-trap-profiles}

Fügen Sie Testprofile hinzu, sodass Sie Ihre Datei mit einer kleinen Anzahl von Profilen testen können. Dadurch können Sie rasch eine Beispieldatei erstellen, um ihren Aufbau zu testen und zu validieren, bevor Sie die eigentliche Datei vorbereiten. Lesen Sie diesbezüglich den Abschnitt [Testprofile verwalten und Testsendungen durchführen](../../sending/using/managing-test-profiles-and-sending-proofs.md).

Die Verwendung von Fallen ist für den Briefpost-Versand besonders wichtig. Beispielsweise können Sie damit sicherstellen, dass Ihr Briefpost-Dienstleister selbst die Nachricht aussendet und Ihre Kundenliste nicht an andere Dienstleister weitergibt.

Für den Briefpost-Versand werden Fallen während der Extraktion hinzugefügt und im Ausgabedokument unter die restlichen Informationen gemischt. Standardmäßig werden sie in der Sortierreihenfolge der Ausgabedatei eingefügt, Sie können sie aber auch am Ende oder Anfang der Datei einfügen (Tab **[!UICONTROL Fallen-Einfüge-Modus]).**

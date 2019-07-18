---
title: Nachrichten-Dashboards
seo-title: Nachrichten-Dashboards
description: Nachrichten-Dashboards
seo-description: Hier erfahren Sie, woraus das Nachrichten-Dashboard besteht, einschließlich der Symbolleiste und der unterschiedlichen Kacheln.
page-status-flag: nie aktiviert
uuid: 9 bb 44 ee 8-2 cf 6-43 ce -94 a 4-367 f 4 e 669713
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Kanäle
content-type: Referenz
topic-tags: about-communication-channels
discoiquuid: 90 a 78742-697 f -46 da -8 c 54-108048 e 57 b 67
context-tags: delivery, main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6df0e764750a31f29d6fe3ec4d92e19b3f07f728

---


# Nachrichten-Dashboards{#message-dashboard}

Das Dashboard einer Nachricht enthält einen Arbeitsbereich mit verschiedenen Kacheln und eine Symbolleiste mit Schaltflächen, die der Konfiguration und dem Versand der Nachricht dienen. Die einzelnen Elemente werden im Folgenden näher erläutert.

![](assets/delivery_dashboard_2.png)

## Graue Leiste {#gray-bar}

Die graue Leiste enthält verschiedene auf Ihre Nachricht bezogene Symbole.

* **[!UICONTROL Zusammenfassung ein-/ausblenden]**: blendet zusammenfassende Informationen zur Nachricht ein oder aus.
* **[!UICONTROL Eigenschaften bearbeiten]**: bietet Zugriff auf den Eigenschaftenbildschirm der Nachricht, der u. a. die Bearbeitung der erweiterten Parameter ermöglicht.
* **[!UICONTROL Berichte]**: bietet Zugriff auf Berichte zur Nachricht.

**Verwandte Themen:**

* [Kanäle konfigurieren](../../administration/using/about-channel-configuration.md)
* [Zugriff auf Berichte](../../reporting/using/about-dynamic-reports.md)

## Symbolleiste {#action-bar}

Die Symbolleiste enthält verschiedene Schaltflächen, die die Bearbeitung der Nachricht ermöglichen.

![](assets/delivery_dashboard_4.png)

Je nach angegebenen Parametern und Bearbeitungsfortschritt stehen gewisse Schaltflächen u. U. nicht zur Verfügung.

* **[!UICONTROL Testsendungen anzeigen]**: blendet die Liste der gesendeten Tests ein oder aus. Diese Schaltfläche ist nur aktiv, wenn Testsendungen existieren.

   Weiterführende Informationen zu Testsendungen finden Sie im Abschnitt [Testprofile verwalten und Testsendungen durchführen](../../sending/using/managing-test-profiles-and-sending-proofs.md).

* **[!UICONTROL Einen Test senden]**: ermöglicht die Auswahl des zu verwendenden Genehmigungsmodus: **[!UICONTROL E-Email-Wiedergabe]**, **[!UICONTROL Proof]** oder beides. Weiterführende Informationen zu Testprofilen finden Sie im Abschnitt [Testversand durchführen](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs).

   Die Schaltfläche ist nur dann aktiv, wenn mindestens ein Testprofil definiert wurde.

   >[!NOTE]
   >
   >Bei einem SMS-Versand ist nur der **[!UICONTROL Testversand verfügbar]**.

* **[!UICONTROL Versand vorbereiten]**: startet die Versandvorbereitung. Die Kachel **[!UICONTROL Freigabe]erscheint und zeigt das Ergebnis der Vorbereitung an.** Diese Schaltfläche erscheint nur, wenn die Zielgruppe angegeben wurde. Mithilfe der Schaltfläche "Vorbereitung stoppen" kann die Vorbereitung jederzeit unterbrochen werden.

   Weiterführende Informationen zur Nachrichtenvorbereitung finden Sie im Abschnitt [Versandvorbereitung](../../sending/using/preparing-the-send.md).

* **[!UICONTROL Versand bestätigen]**: löst den endgültigen Versand der Nachricht aus. In der Kachel **[!UICONTROL Freigabe]erscheint nun das Versandergebnis.** Diese Schaltfläche erscheint erst nach Abschluss der Versandvorbereitung. Der Versand kann mithilfe der Schaltflächen **Versand anhalten** oder **[!UICONTROL Aussetzen]jederzeit unterbrochen werden.**

   Lesen Sie diesbezüglich auch den Abschnitt [Nachrichten senden](../../sending/using/confirming-the-send.md).

## Bausteine {#blocks}

Der Arbeitsbereich besteht aus verschiedenen Kacheln. Klicken Sie in eine Kachel, um auf die entsprechenden Versandparameter zugreifen zu können:

![](assets/delivery_dashboard_3.png)

* **[!UICONTROL Freigabe]**: gibt Auskunft über den Fortschritt der Vorbereitung oder des Versands der Nachricht. Mithilfe der Schaltfläche unten rechts in der Kachel lässt sich das Analyse- und Versandprotokoll anzeigen. Diese Kachel erscheint erst nach abgeschlossener Versandvorbereitung. Weiterführende Informationen dazu finden Sie im Abschnitt [Versand bestätigen](../../sending/using/confirming-the-send.md).
* **[!UICONTROL Audience]**: dient der Bestimmung der Hauptzielgruppe der Nachricht sowie der Testprofile. Siehe [Erstellung von Audiences](../../audiences/using/creating-audiences.md).
* **[!UICONTROL Versandplanung]**: dient der Bestimmung des Versanddatums der Nachricht. Siehe [Über die Versandplanung](../../sending/using/about-scheduling-messages.md).
* **[!UICONTROL Inhalt]**: dient der Erstellung des Nachrichteninhalts und seiner Vorschau. Siehe [Inhalte erstellen](../../designing/using/designing-content-in-adobe-campaign.md).


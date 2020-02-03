---
title: Nachrichten-Dashboards
description: Hier erfahren Sie, woraus das Nachrichten-Dashboard besteht, einschließlich der Symbolleiste und der unterschiedlichen Kacheln.
page-status-flag: never-activated
uuid: 9bb44ee8-2cf6-43ce-94a4-367f4e469713
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: about-communication-channels
discoiquuid: 90a78742-697f-46da-8c54-108048e57b67
context-tags: delivery,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 0fe16001c57d3ccc2e7d42b94bc14e73d8b47ddb

---


# Nachrichten-Dashboards{#message-dashboard}

Das Dashboard einer Nachricht enthält einen Arbeitsbereich mit verschiedenen Kacheln und eine Symbolleiste mit Schaltflächen, die der Konfiguration und dem Versand der Nachricht dienen. Die einzelnen Elemente werden im Folgenden näher erläutert.

![](assets/delivery_dashboard_2.png)

## Graue Leiste {#gray-bar}

Die graue Leiste enthält verschiedene auf Ihre Nachricht bezogene Symbole.

* **[!UICONTROL Zusammenfassung ein-/ausblenden]**: blendet zusammenfassende Informationen zur Nachricht ein oder aus.
* **[!UICONTROL Eigenschaften bearbeiten]**: bietet Zugriff auf den Eigenschaftenbildschirm der Nachricht, der u. a. die Bearbeitung der[erweiterten Parameter](../../administration/using/configuring-email-channel.md#list-of-email-properties)ermöglicht.
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

* **[!UICONTROL Testen]**: ermöglicht u. a. die Auswahl des Validierungsmodus (**[!UICONTROL  Testversand]** und/oder **[!UICONTROL E-Mail-Rendering]**bei E-Mails). Weiterführende Informationen zu Testprofilen finden Sie im Abschnitt[Testversand durchführen](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs).

   Die Schaltfläche ist nur dann aktiv, wenn mindestens ein Testprofil definiert wurde.

   >[!NOTE]
   >
   >Bei einem SMS-Versand ist nur der **[!UICONTROL Testversand verfügbar]**.

* **[!UICONTROL Versand vorbereiten]**: startet die Versandvorbereitung. Die Kachel**[!UICONTROL  Freigabe]** erscheint und zeigt das Ergebnis der Vorbereitung an. Diese Schaltfläche erscheint nur, wenn die Zielgruppe angegeben wurde. Mithilfe der Schaltfläche &quot;Vorbereitung stoppen&quot; kann die Vorbereitung jederzeit unterbrochen werden.

   Weiterführende Informationen zur Nachrichtenvorbereitung finden Sie im Abschnitt [Versandvorbereitung](../../sending/using/preparing-the-send.md).

* **[!UICONTROL Versand bestätigen]**: löst den endgültigen Versand der Nachricht aus. In der Kachel**[!UICONTROL  Freigabe]** erscheint nun das Versandergebnis. Diese Schaltfläche erscheint erst nach Abschluss der Versandvorbereitung. Der Versand kann mithilfe der Schaltflächen **Versand anhalten** oder **[!UICONTROL Aussetzen]**jederzeit unterbrochen werden.

   Lesen Sie diesbezüglich auch den Abschnitt [Nachrichten senden](../../sending/using/confirming-the-send.md).

## Bausteine {#blocks}

Der Arbeitsbereich besteht aus verschiedenen Kacheln. Klicken Sie in eine Kachel, um auf die entsprechenden Versandparameter zugreifen zu können:

![](assets/delivery_dashboard_3.png)

* **[!UICONTROL Freigabe]**: gibt Auskunft über den Fortschritt der Vorbereitung oder des Versands der Nachricht. Mithilfe der Schaltfläche unten rechts in der Kachel lässt sich das Analyse- und Versandprotokoll anzeigen. Diese Kachel erscheint erst nach abgeschlossener Versandvorbereitung. Weiterführende Informationen dazu finden Sie im Abschnitt[Versand bestätigen](../../sending/using/confirming-the-send.md).
* **[!UICONTROL Audience]**: dient der Bestimmung der Hauptzielgruppe der Nachricht sowie der Testprofile. Siehe[Erstellung von Audiences](../../audiences/using/creating-audiences.md).
* **[!UICONTROL Versandplanung]**: dient der Bestimmung des Versanddatums der Nachricht. Siehe[Über die Versandplanung](../../sending/using/about-scheduling-messages.md).
* **[!UICONTROL Inhalt]**: dient der Definition und Vorschau des Nachrichteninhalts. Siehe[Wichtigste Schritte im Nachrichtenversand](../../channels/using/key-steps-to-send-a-message.md).

## Warnhinweise {#warnings}

In einigen Fällen kann eine Warnung in einem gelben Banner über dem Nachrichten-Dashboard angezeigt werden.

![](assets/delivery_dashboard_warnings.png)

Im Folgenden finden Sie eine Liste der Meldungen, die angezeigt werden können:

* *&quot;Die Option für den SMTP-Testmodus ist für diese E-Mail aktiviert: keine Nachrichten gesendet werden.&quot;*

   Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../administration/using/configuring-email-channel.md#smtp-test-mode).

* *&quot;Routing des externen Kontos wurde deaktiviert.&quot;*

   Weitere Informationen finden Sie unter [Externe Konten](../../administration/using/external-accounts.md).

* *&quot;Nachrichten können nicht gesendet werden, da die aktuelle IP-Affinität von keinem Versandprozess verarbeitet wird.&quot;*

   Wenn diese Meldung angezeigt wird, liegt ein Problem auf der Ebene der IP-Affinitätsdefinition oder auf der Ebene des sendenden Prozesses vor. Wenden Sie sich an Ihren Adobe-Administrator.

* *&quot;Bei dieser Transaktionsnachricht handelt es sich um eine vordefinierte Vorlage für Transaktionsnachrichten. Wenn Sie sie bearbeiten möchten, müssen Sie sie duplizieren und eine Kopie bearbeiten.&quot;*

   Einige dieser vordefinierten Vorlagen für Transaktionsmeldungen sind integrierte Vorlagen für Einstiegsseiten. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../channels/using/landing-page-templates.md).

* *&quot;Bei dieser Nachricht handelt es sich um eine Nachrichtenvorlage für technische Transaktionen. Sie können Sie bearbeiten oder veröffentlichen.&quot;*

   Diese Warnung wird in leeren, nicht bearbeitbaren Transaktionsmeldungsvorlagen angezeigt. For more on transactional messages, see [this section](../../channels/using/about-transactional-messaging.md).

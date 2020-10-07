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
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 92%

---


# Nachrichten-Dashboards{#message-dashboard}

Das Dashboard einer Nachricht enthält einen Arbeitsbereich mit verschiedenen Kacheln und eine Symbolleiste mit Schaltflächen, die der Konfiguration und dem Versand der Nachricht dienen. Die einzelnen Elemente werden im Folgenden näher erläutert.

![](assets/delivery_dashboard_2.png)

## Graue Leiste     {#gray-bar}

Die graue Leiste enthält verschiedene auf Ihre Nachricht bezogene Symbole.

* **[!UICONTROL Zusammenfassung]**: blendet zusammenfassende Informationen zur Nachricht ein oder aus.
* **[!UICONTROL Eigenschaften bearbeiten]**: bietet Zugriff auf die [erweiterten Parameter](../../administration/using/configuring-email-channel.md#list-of-email-properties) der Nachricht.
* **[!UICONTROL Berichte]**: bietet Zugriff auf Berichte zur Nachricht.

**Verwandte Themen:**

* [Kanäle konfigurieren](../../administration/using/about-channel-configuration.md)
* [Zugriff auf Berichte](../../reporting/using/about-dynamic-reports.md)

## Symbolleiste     {#action-bar}

Die Symbolleiste enthält verschiedene Schaltflächen, die die Bearbeitung der Nachricht ermöglichen.

![](assets/delivery_dashboard_4.png)

Je nach angegebenen Parametern und Bearbeitungsfortschritt stehen gewisse Schaltflächen u. U. nicht zur Verfügung.

* **[!UICONTROL Testsendungen anzeigen]**: blendet die Liste der gesendeten Tests ein oder aus. Diese Schaltfläche ist nur aktiv, wenn Testsendungen existieren.

   Weiterführende Informationen zu Testsendungen finden Sie im Abschnitt [Testversand durchführen](../../sending/using/sending-proofs.md).

* **[!UICONTROL Test]** senden: können Sie den zu verwendenden Genehmigungsmodus auswählen: **[!UICONTROL E-Mail-Rendering]** (nur E-Mail), **[!UICONTROL Testversand]** oder beides. Weiterführende Informationen zu Testprofilen finden Sie im Abschnitt [Testversand durchführen](../../sending/using/sending-proofs.md). Diese Schaltfläche ist erst aktiviert, nachdem Sie Test-Profil erstellt haben.

* **[!UICONTROL Versand vorbereiten]**: startet die Versandvorbereitung. Die Kachel **[!UICONTROL Freigabe]** erscheint und zeigt das Ergebnis der Vorbereitung an. Diese Schaltfläche erscheint nur, wenn die Zielgruppe angegeben wurde. Mithilfe der Schaltfläche &quot;Vorbereitung stoppen&quot; kann die Vorbereitung jederzeit unterbrochen werden. For more on message preparation, refer to [Preparing the send](../../sending/using/preparing-the-send.md).

* **[!UICONTROL Versand bestätigen]**: löst den endgültigen Versand der Nachricht aus. In der Kachel **[!UICONTROL Freigabe]** erscheint nun das Versandergebnis. Diese Schaltfläche erscheint erst nach Abschluss der Versandvorbereitung. Der Versand kann mithilfe der Schaltflächen **Versand anhalten** oder **[!UICONTROL Unterbrechen]** jederzeit unterbrochen werden. For more on confirming sending, refer to [Sending messages](../../sending/using/confirming-the-send.md).

## Bausteine     {#blocks}

Der Arbeitsbereich besteht aus verschiedenen Kacheln. Klicken Sie in eine Kachel, um auf die entsprechenden Versandparameter zugreifen zu können:

![](assets/delivery_dashboard_3.png)

* **[!UICONTROL Freigabe]**: gibt Auskunft über den Fortschritt der Vorbereitung oder des Versands der Nachricht. Mithilfe der Schaltfläche unten rechts in der Kachel lässt sich das Analyse- und Versandprotokoll anzeigen. Diese Kachel erscheint erst nach abgeschlossener Versandvorbereitung. Weiterführende Informationen dazu finden Sie im Abschnitt [Versand bestätigen](../../sending/using/confirming-the-send.md).
* **[!UICONTROL Audience]**: dient der Bestimmung der Hauptzielgruppe der Nachricht sowie der Testprofile. Siehe [Audiences erstellen](../../audiences/using/creating-audiences.md).
* **[!UICONTROL Planung]**: dient der Bestimmung des Versanddatums der Nachricht. Siehe [Versandplanung](../../sending/using/about-scheduling-messages.md).
* **[!UICONTROL Inhalt]**: dient der Definition und Vorschau des Nachrichteninhalts. Siehe [Wichtigste Schritte im Nachrichtenversand](../../channels/using/key-steps-to-send-a-message.md).

## Warnhinweise {#warnings}

In einigen Fällen kann ein Warnhinweis in einem gelben Banner über dem Nachrichten-Dashboard angezeigt werden.

![](assets/delivery_dashboard_warnings.png)

Im Folgenden finden Sie eine Liste der Warnhinweise, die angezeigt werden können:

* *„Die SMTP-Testmodus-Option ist für diese E-Mail aktiviert: Es werden keine Nachrichten gesendet.“*

   Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../administration/using/configuring-email-channel.md#smtp-test-mode).

* *„Routing des externen Kontos wurde deaktiviert.“*

   Weiterführende Informationen hierzu finden Sie im Abschnitt [Externe Konten](../../administration/using/external-accounts.md).

* *„Nachrichten können nicht gesendet werden, da die aktuelle IP-Affinität von keinem Versandprozess verarbeitet wird.“*

   Wenn dieser Warnhinweis angezeigt wird, liegt ein Problem auf der Ebene der IP-Affinitätsdefinition oder auf der Ebene des Versandprozesses vor. Wenden Sie sich an Ihren Adobe-Administrator.

* *„Dies ist eine vordefinierte Transaktionsnachrichtenvorlage. Wenn Sie Änderungen vornehmen möchten, müssen Sie die Vorlage duplizieren und die Kopie bearbeiten.“*

   Einige dieser vordefinierten Transaktionsnachrichten-Vorlagen sind native Landingpage-Vorlagen. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../channels/using/landing-page-templates.md).

* *„Bei dieser Nachricht handelt es sich um eine Nachrichtenvorlage für technische Transaktionen. Sie können sie bearbeiten oder veröffentlichen.“*

   Dieser Warnhinweis wird in leeren, nicht bearbeitbaren Transaktionsnachrichten-Vorlagen angezeigt. Weiterführende Informationen zu Transaktionsnachrichten finden Sie in [diesem Abschnitt](../../channels/using/getting-started-with-transactional-msg.md).

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
source-git-commit: 07d68b5bf8d800ebd95919f491e98f1b7a015705

---


# Nachrichten-Dashboards{#message-dashboard}

Das Dashboard einer Nachricht enthält einen Arbeitsbereich mit verschiedenen Kacheln und eine Symbolleiste mit Schaltflächen, die der Konfiguration und dem Versand der Nachricht dienen. Die einzelnen Elemente werden im Folgenden näher erläutert.

![](assets/delivery_dashboard_2.png)

## Graue Leiste {#gray-bar}

Die graue Leiste enthält verschiedene auf Ihre Nachricht bezogene Symbole.

* **[!UICONTROL Summary]**: Blendet die Hauptinformationen zur Nachricht ein bzw. aus.
* **[!UICONTROL Edit properties]**: können Sie die [erweiterten Parameter](../../administration/using/configuring-email-channel.md#list-of-email-properties)der Nachricht bearbeiten.
* **[!UICONTROL Reports]**: gibt Ihnen Zugriff auf die Berichte zu der Nachricht.

**Verwandte Themen:**

* [Kanäle konfigurieren](../../administration/using/about-channel-configuration.md)
* [Zugriff auf Berichte](../../reporting/using/about-dynamic-reports.md)

## Symbolleiste {#action-bar}

Die Symbolleiste enthält verschiedene Schaltflächen, die die Bearbeitung der Nachricht ermöglichen.

![](assets/delivery_dashboard_4.png)

Je nach angegebenen Parametern und Bearbeitungsfortschritt stehen gewisse Schaltflächen u. U. nicht zur Verfügung.

* **[!UICONTROL Show proofs]**: Blendet die Liste der gesendeten Nachweise ein bzw. aus, sofern vorhanden. Diese Schaltfläche ist nur aktiv, wenn Testsendungen existieren.

   For more on proofs, see [Sending proofs](../../sending/using/sending-proofs.md).

* **[!UICONTROL Send a test]**: können Sie den zu verwendenden Genehmigungsmodus auswählen: **[!UICONTROL Email rendering]**, **[!UICONTROL Proof]** oder beide für eine E-Mail. Weiterführende Informationen zu Testprofilen finden Sie im Abschnitt [Testversand durchführen](../../sending/using/sending-proofs.md).

   Die Schaltfläche ist nur dann aktiv, wenn mindestens ein Testprofil definiert wurde.

   >[!NOTE]
   >
   >For an SMS message, there is no other choice: it is automatically a **[!UICONTROL Proof]**.

* **[!UICONTROL Prepare send]**: beginnt, den Versand vorzubereiten. The **[!UICONTROL Deployment]** block appears and displays the result of the preparation. Diese Schaltfläche erscheint nur, wenn die Zielgruppe angegeben wurde. Mithilfe der Schaltfläche &quot;Vorbereitung stoppen&quot; kann die Vorbereitung jederzeit unterbrochen werden.

   Weiterführende Informationen zur Nachrichtenvorbereitung finden Sie im Abschnitt [Versandvorbereitung](../../sending/using/preparing-the-send.md).

* **[!UICONTROL Confirm send]**: bestätigt das Senden der Nachricht. The sending statistics appear in the **[!UICONTROL Deployment]** block. Diese Schaltfläche erscheint erst nach Abschluss der Versandvorbereitung. You can stop or pause the send at any time using the **Stop send** and **[!UICONTROL Pause]** buttons.

   Lesen Sie diesbezüglich auch den Abschnitt [Nachrichten senden](../../sending/using/confirming-the-send.md).

## Bausteine {#blocks}

Der Arbeitsbereich besteht aus verschiedenen Kacheln. Klicken Sie in eine Kachel, um auf die entsprechenden Versandparameter zugreifen zu können:

![](assets/delivery_dashboard_3.png)

* **[!UICONTROL Deployment]**: ermöglicht es Ihnen, den Fortschritt der Nachrichtenvorbereitung oder des Nachrichtenversands zu verfolgen. Mithilfe der Schaltfläche unten rechts in der Kachel lässt sich das Analyse- und Versandprotokoll anzeigen. Diese Kachel erscheint erst nach abgeschlossener Versandvorbereitung. Weiterführende Informationen dazu finden Sie im Abschnitt [Versand bestätigen](../../sending/using/confirming-the-send.md).
* **[!UICONTROL Audience]**: ermöglicht Ihnen, das Hauptziel der Nachricht sowie die Testprofile festzulegen. Weiterführende Informationen dazu finden Sie im Abschnitt [Erstellung von Audiences](../../audiences/using/creating-audiences.md).
* **[!UICONTROL Schedule]**: können Sie das Datum angeben, an dem Ihre Nachricht gesendet werden soll. Siehe [Zeitplan](../../sending/using/about-scheduling-messages.md).
* **[!UICONTROL Content]**: können Sie den Inhalt der Nachricht definieren und eine Vorschau davon anzeigen. Siehe [Wichtigste Schritte im Nachrichtenversand](../../channels/using/key-steps-to-send-a-message.md).

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

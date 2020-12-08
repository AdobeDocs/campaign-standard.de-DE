---
title: Transaktionsnachrichten konfigurieren
description: Hier erfahren Sie, wie Transaktionsnachrichten konfiguriert werden.
page-status-flag: never-activated
uuid: 4caeadbe-f4a7-43ce-986d-e99fa9ca0d0d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 3f968556-e774-43dc-a0b8-7188d7665fbc
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: caa41d6c727385bd6e77f64750872f191a5ad040
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 12%

---


# Anwendungsfall für Transaktionsnachrichten {#transactional-messaging-use-case}

In diesem Beispiel möchten Sie die Transaktionsnachrichtenfunktion des Adobe Campaigns verwenden, um nach jedem Einkauf auf auf Ihrer Website eine Bestätigungs-E-Mail zu senden und Ihre Kunden anhand ihrer CRM-ID zu identifizieren.

Folgende Voraussetzungen sind erforderlich:

* Stellen Sie sicher, dass die Ressource **[!UICONTROL Profil]** um ein neues Feld entsprechend der CRM-ID erweitert wurde.

* Erstellen und veröffentlichen Sie eine benutzerspezifische Ressource, die Käufen entspricht, und verknüpfen Sie sie mit der Ressource **[!UICONTROL Profil]**. Auf diese Weise werden Sie in der Lage sein, Informationen aus dieser Ressource zur Anreicherung des Nachrichteninhalts abzurufen.

Weitere Informationen zum Erweitern, Erstellen und Veröffentlichen von Ressourcen finden Sie in [diesem Abschnitt](../../developing/using/key-steps-to-add-a-resource.md).

Die wichtigsten Schritte zur Implementierung dieses Anwendungsfalls werden nachfolgend beschrieben.

>[!NOTE]
>
>Eine grafische Darstellung des allgemeinen Transaktionsprozesses finden Sie in [diesem Schema](../../channels/using/getting-started-with-transactional-msg.md#key-steps).

## Schritt 1: Ereigniskonfiguration erstellen und publizieren {#create-event-configuration}

1. Erstellen Sie ein neues Ereignis mit dem Kanal **[!UICONTROL Email]**. Siehe [Erstellen eines Ereignisses](../../channels/using/configuring-transactional-event.md#creating-an-event).

1. Wählen Sie die Zielgruppendimension **[!UICONTROL Profil]** aus, um eine [Profil-basierte Transaktionsnachricht](../../channels/using/configuring-transactional-event.md#profile-based-transactional-messages) zu erstellen.

1. Definieren Sie die Attribute, die zur Personalisierung der Transaktionsnachricht verfügbar sein sollen. Fügen Sie in diesem Beispiel die Felder &quot;CRM-ID&quot;und &quot;Produkt-ID&quot;hinzu. Siehe [Definieren der Ereignis-Attribute](../../channels/using/configuring-transactional-event.md#defining-the-event-attributes).

   ![](assets/message-center_usecase1.png)

1. Um den Inhalt der Nachricht mit Informationen über die Käufe des Kunden zu bereichern, erstellen Sie eine Anreicherung, die auf die **[!UICONTROL Kauf]**-Ressource abzielt. Siehe [Anreichern des Ereignisses](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content).

   ![](assets/message-center_usecase2.png)

1. Erstellen Sie eine Verbindungsbedingung zwischen dem Feld &quot;Produkt-ID&quot;, das dem Ereignis zuvor hinzugefügt wurde, und dem entsprechenden Feld aus der Ressource **[!UICONTROL Kauf]**.

   ![](assets/message-center_usecase3.png)

1. Da dies für Profil-basierte Ereignis obligatorisch ist, müssen Sie auch eine Anreicherung erstellen, die auf die **[!UICONTROL Profil]**-Ressource abzielt.

1. Erstellen Sie eine Verbindungsbedingung zwischen dem Feld &quot;CRM-ID&quot;, das der Nachricht zuvor hinzugefügt wurde, und dem entsprechenden Feld der von Ihnen erweiterten Ressource **[!UICONTROL Profil]**. <!--What's the purpose to have created a CRM ID for this event and to have the CRM ID as a join condition? could it be any other field provided you created it in the event?-->

   ![](assets/message-center_usecase4.png)

1. Wählen Sie im Abschnitt **[!UICONTROL Targeting-Anreicherung]** die Anreicherung für die **[!UICONTROL Profil]**-Ressource aus, die während der Ausführung des Versands als Zielgruppe der Nachricht verwendet wird.

   ![](assets/message-center_usecase5.png)

1. Vorschau und Veröffentlichung des Ereignisses. Siehe [Anzeigen einer Vorschau und Veröffentlichung des Ereignisses](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event).

## Schritt 2: Transaktionsnachricht bearbeiten und publizieren {#create-transactional-message}

1. Wechseln Sie zu der Transaktionsnachricht, die beim Veröffentlichen des Ereignisses automatisch erstellt wurde. Siehe [Zugriff auf Transaktionsnachrichten](../../channels/using/editing-transactional-message.md#accessing-transactional-messages).

1. Bearbeiten und personalisieren Sie die Nachricht. Siehe [Bearbeiten einer Profil-Transaktionsnachricht](../../channels/using/editing-transactional-message.md#editing-profile-transactional-message).

1. Durch Abgleich mit dem Feld &quot;CRM-ID&quot;, das Sie der Ressource **[!UICONTROL Profil]** hinzugefügt haben, haben Sie direkten Zugriff auf alle Profil-Informationen zu [personalize](../../designing/using/personalization.md#inserting-a-personalization-field) Ihrer Nachricht.

   ![](assets/message-center_usecase6.png)

1. Durch Abgleich mit dem Feld &quot;Produkt-ID&quot;können Sie den Inhalt der Nachricht mit Informationen zu den Käufen des Kunden bereichern, indem Sie ein Feld aus der Ressource **[!UICONTROL Kauf]** hinzufügen.

   ![](assets/message-center_usecase7.png)

   Wählen Sie dazu **[!UICONTROL Personalisierungsfeld]** in der Kontextsymbolleiste einfügen. Öffnen Sie unter **[!UICONTROL Kontext]** > **[!UICONTROL Transaktionskontext]** > **[!UICONTROL Ereignis-Kontext]** den Knoten, der der **[!UICONTROL Benutzerspezifische Ressource entspricht, und wählen Sie ein beliebiges Feld aus.]**

1. Sie können Ihre Nachricht mit einem bestimmten Test-Profil testen. Siehe [Testen einer Transaktionsnachricht](../../channels/using/testing-transactional-message.md#testing-a-transactional-message).

1. Sobald der Inhalt fertig ist, speichern Sie die Änderungen und veröffentlichen Sie die Nachricht. Siehe [Transaktionsnachricht publizieren](../../channels/using/publishing-transactional-message.md#publishing-a-transactional-message).

## Schritt 3: Ereignis-Aktivierung integrieren {#integrate-event-trigger}

Integrieren Sie das Ereignis in Ihre Website. Siehe [Integrieren Sie das Ereignis, das](../../channels/using/getting-started-with-transactional-msg.md#integrate-event-trigger) auslöst.

## Schritt 4: Nachrichtenversand {#message-delivery}

Sobald alle diese Schritte ausgeführt wurden, erhalten Kunden, sobald sie Produkte von Ihrer Website erwerben, eine persönliche Bestätigungs-E-Mail mit Informationen zum Kauf.
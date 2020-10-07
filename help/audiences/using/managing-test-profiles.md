---
title: 'Verwaltung von Testprofilen '
description: Erfahren Sie, wie Sie Test-Profil verwalten.
page-status-flag: never-activated
uuid: eb4d893b-3724-4b15-9312-1ec74784368d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
discoiquuid: 37320ec5-196c-4260-8156-98932da3e4a5
context-tags: seedMember,overview
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 79%

---


# Verwaltung von Testprofilen  {#managing-test-profiles}

## Über Testprofile {#about-test-profiles}

Testprofile ermöglichen es, zusätzliche Empfänger anzusprechen, die nicht den definierten Zielgruppenkriterien entsprechen. Sie werden Audiences hinzugefügt, um beispielsweise Missbrauch bei der Nutzung Ihrer Empfängerliste aufzudecken oder den korrekten Erhalt der Sendungen zu kontrollieren.

Testprofile werden im erweiterten Menü **[!UICONTROL Profile &amp; Audiences > Testprofile]** verwaltet.

Testprofile sind Profile mit fiktiven oder vom Absender kontrollierten Kontaktinformationen, die verschiedenen Zwecken dienen können:

* For sending **Proofs**: The Proof is a specific message used to check the message before sending the finalized delivery to recipients. Testversand-Empfänger sind verantwortlich für die Validierung des Inhalts und der Form von Sendungen. Siehe [Testversand durchführen](../../sending/using/sending-proofs.md).
* For **Email rendering**: The Email rendering test profile is used to check the way in which a message is displayed according to the message inbox that receives it. Beispielsweise Webmail, SMS, Mobilgeräte etc. Siehe [E-Mail-Rendering](../../sending/using/email-rendering.md).

   Die Funktion **E-Mail-Rendering** ist schreibgeschützt. Testprofile mit diesem Verwendungszweck sind ausschließlich nativ in Adobe Campaign enthalten.

* As a **Trap**: The message is sent to the test profile just as it is sent to the main target. Siehe [Verwenden von Traps](../../sending/using/using-traps.md).
* To **Preview** messages: A test profile can be selected when previewing a message to test the personalization elements. Siehe [Vorschau der Nachricht erzeugen](/help/sending/using/previewing-messages.md).

![](assets/test_profile.png)

## Testprofile erstellen {#creating-test-profiles}

1. Greifen Sie mithilfe des Adobe-Campaign-Logos auf das erweiterte Menü **Profile &amp; Audiences > Testprofile** zu, um die Liste mit Testprofilen aufzurufen.

   ![](assets/test_profile_creation_1.png)

1. Verwenden Sie in der Übersicht der **[!UICONTROL Testprofile]** die Schaltfläche **Erstellen**.

   ![](assets/test_profile_creation_2.png)

1. Machen Sie die erforderlichen Angaben zum Profil.

   ![](assets/test_profile_creation_3.png)

1. Kreuzen Sie die Verwendung des Testprofils an.

   ![](assets/test_profile_creation_4.png)

1. Geben Sie die verschiedenen Kontaktkanäle (**[!UICONTROL E-Mail, Telefon, Mobiltelefon, Mobile App]**) sowie bei Bedarf die Adresse des Testprofils an.

   >[!NOTE]
   >
   >Sie können ein bevorzugtes E-Mail-Format definieren: **[!UICONTROL Text]** oder **[!UICONTROL HTML]**.

1. Geben Sie einen Ereignistyp sowie die Ereignisdaten an, wenn Sie dieses Testprofil dazu verwenden möchten, die Personalisierung einer Transaktionsnachricht zu testen.
1. Speichern Sie das Testprofil mithilfe der Schaltfläche **[!UICONTROL Erstellen]**.

Das Testprofil wurde der Liste der Profile hinzugefügt.

**Verwandtes Thema:**

Video [Creating a test profile](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/profiles-and-audiences/test-profiles.html)

## Testprofile bearbeiten {#editing-test-profiles}

Gehen Sie wie folgt vor, um ein bereits existierendes Testprofil zu bearbeiten bzw. seine Daten einzusehen oder es zu ändern:

1. Wählen Sie das zu ändernde Testprofil aus, indem Sie auf sein Bild klicken.
1. Nehmen Sie bei Bedarf die gewünschten Änderungen vor.

   ![](assets/test_profile_edit.png)

1. Verwenden Sie die Schaltfläche **[!UICONTROL Speichern]**, falls Sie Änderungen vorgenommen haben. Andernfalls können Sie oben im Bildschirm den Namen des Testprofils anklicken und dann in der sich öffnenden Dropdown-Liste **[!UICONTROL Testprofile]** auswählen, um zur Übersicht der Testprofile zurückzukehren.

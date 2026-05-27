---
title: Verwaltung von Testprofilen
description: Erfahren Sie, wie Sie Testprofile verwalten.
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
context-tags: seedMember,overview
feature: Profiles
role: User
level: Intermediate
exl-id: 56ece9da-18ec-4d27-a637-c22709a5e6aa
TQID: https://experienceleague.adobe.com/csDw0anKGvAW22BcB5p0Rb1bHYA2NvdWpLVIWtZrC98
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 471
ht-degree: 97%

---

# Verwaltung von Testprofilen {#managing-test-profiles}

## Über Testprofile {#about-test-profiles}

Testprofile ermöglichen es, zusätzliche Empfänger anzusprechen, die nicht den definierten Targeting-Kriterien entsprechen. Sie werden Zielgruppen hinzugefügt, um beispielsweise Missbrauch bei der Nutzung Ihrer Empfängerliste aufzudecken oder den korrekten Erhalt der Sendungen zu kontrollieren.

![](assets/do-not-localize/how-to-video.png) [Mehr zu dieser Funktion erfahren Sie im Video.](#video).

Testprofile werden im erweiterten Menü **[!UICONTROL Profile und Zielgruppen > Testprofile]** verwaltet.

Testprofile sind Profile mit fiktiven oder vom Absender kontrollierten Kontaktinformationen, die verschiedenen Zwecken dienen können:

* **Testsendungen**: Dabei handelt es sich um einen speziellen Versand, der es ermöglicht, eine Nachricht vor dem Versenden an die Empfänger zu validieren. Testversand-Empfänger sind verantwortlich für die Validierung des Inhalts und der Form von Sendungen. Siehe [Testversand durchführen](../../sending/using/sending-proofs.md).
* **E-Mail-Rendering**: Diese Art von Testprofilen wird verwendet, um den Empfang und die Darstellung Ihrer Nachricht in den verschiedenen E-Mail-Clients zu testen. Zum Beispiel Webmail, Nachrichten-Service, Mobilgerät usw. Siehe [Email Rendering](../../sending/using/email-rendering.md).

  Die Funktion **E-Mail-Rendering** ist schreibgeschützt. Testprofile mit diesem Verwendungszweck sind ausschließlich nativ in Adobe Campaign enthalten.

* Als **Falle**: Die Nachricht wird auf dieselbe Weise an das Testprofil gesendet wie an die Hauptzielgruppe. Siehe [Verwenden von Fallen](../../sending/using/using-traps.md).
* **Vorschau** einer Nachricht: Durch Auswahl eines Testprofils lässt sich die korrekte Umsetzung von Personalisierungselementen innerhalb einer Nachricht prüfen. Siehe [Vorschau der Nachricht erzeugen](/help/sending/using/previewing-messages.md).

![](assets/test_profile.png)

## Testprofile erstellen {#creating-test-profiles}

1. Greifen Sie mithilfe des Adobe Campaign-Logos auf das erweiterte Menü **Profile und Zielgruppen > Testprofile** zu, um die Liste mit Testprofilen aufzurufen.

   ![](assets/test_profile_creation_1.png)

1. Verwenden Sie im **[!UICONTROL Testprofile]**-Dashbord die Schaltfläche **Erstellen**.

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

## Testprofile bearbeiten {#editing-test-profiles}

Gehen Sie wie folgt vor, um ein bereits existierendes Testprofil zu bearbeiten bzw. seine Daten einzusehen oder es zu ändern:

1. Wählen Sie das zu ändernde Testprofil aus, indem Sie auf sein Bild klicken.
1. Nehmen Sie bei Bedarf die gewünschten Änderungen vor.

   ![](assets/test_profile_edit.png)

1. Verwenden Sie die Schaltfläche **[!UICONTROL Speichern]**, falls Sie Änderungen vorgenommen haben. Andernfalls können Sie oben im Bildschirm den Namen des Testprofils anklicken und dann in der sich öffnenden Dropdown-Liste **[!UICONTROL Testprofile]** auswählen, um zum Testprofile-Dashbord zurückzukehren.

## Anleitungsvideo {#video}

In diesem Video wird gezeigt, wie man ein Testprofil erstellt.

>[!VIDEO](https://video.tv.adobe.com/v/30205?captions=ger&quality=12)

Weitere Anleitungsvideos zu Campaign Standard finden Sie [hier](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/overview.html?lang=de).

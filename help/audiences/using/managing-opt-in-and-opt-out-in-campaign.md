---
title: Opt-in- und Opt-out-Verfahren in Campaign verwalten
description: Hier erfahren Sie, wie das Opt-in- und Opt-out-Verfahren in Adobe Campaign funktioniert.
page-status-flag: never-activated
uuid: aa1801ec-562b-420e-8d79-c07d066b7b1a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: understanding-opt-in-and-opt-out-processes
discoiquuid: 6b5680f2-bba9-453e-a0d5-8ca69dd02001
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 012546e109b085b7ed968bcefa8f76482656ae0d
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 80%

---


# Opt-in- und Opt-out-Verfahren in Campaign verwalten{#managing-opt-in-and-opt-out-in-campaign}

## Opt-in- und Opt-out-Verfahren in einem Profil verwalten {#managing-opt-in-and-opt-out-from-a-profile}

Ein Benutzer kann von einem Empfänger direkt im Profil-Tab **[!UICONTROL Allgemein]** an- oder abgemeldet werden.

In the **[!UICONTROL No longer contact (on block list)]** section, the selected checkboxes correspond to the channels from which the user chose to opt out. Wählen Sie die Kanäle entsprechend den Anforderungen des Empfängers aus.

![](assets/optin_landingpage_3.png)

## Opt-in- und Opt-out-Landingpages einrichten  {#setting-up-opt-in-and-opt-out-landing-pages}

Um Empfängern die Möglichkeit zu geben, sich an- oder abzumelden, müssen Sie eine **[!UICONTROL Profilakquise]**-Landingpage erstellen und veröffentlichen. Empfänger können dann entsprechend ihren Anforderungen die gewünschten Kanäle auswählen. Gehen Sie dazu wie folgt vor:

You can also set up a **[!UICONTROL Block List]** landing page that will enable users to opt out from all deliveries. Weiterführende Informationen dazu finden Sie im Abschnitt [Landingpage zur Abmeldung von allen Sendungen einrichten](#setting-up-a-landing-page-to-opt-out-from-all-deliveries).

>[!NOTE]
>
>Landingpages können auch verwendet werden, um die Anmeldung zu Diensten zu ermöglichen. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../channels/using/configuring-landing-page.md#linking-a-landing-page-to-a-service).

1. Erstellen Sie eine **[!UICONTROL Profilakquise]**-Landingpage (siehe [diesen Abschnitt](../../channels/using/getting-started-with-landing-pages.md)).
1. Fügen Sie zum Inhalt der Landingpage für jeden gewünschten Kanal ein Kontrollkästchen hinzu und verknüpfen Sie es dann mit dem entsprechenden Feld in der Campaign-Datenbank.

   ![](assets/optin_landingpage_1.png)

1. Speichern Sie die Landingpage und veröffentlichen Sie sie.
1. Die Kontrollkästchen in der Landingpage sind bereits entsprechend dem Profil-Tab **[!UICONTROL Allgemein]** markiert. Der Empfänger kann die Kanäle entsprechend seinen Anforderungen beliebig auswählen oder löschen und das Formular senden.

   ![](assets/optin_landingpage_2.png)

1. Nachdem das Formular gesendet wurde, wird der Profil-Tab **[!UICONTROL Allgemein]** gemäß der Auswahl des Empfängers aktualisiert.

   ![](assets/optin_landingpage_3.png)

### Landingpage zum Opt-out von allen Sendungen einrichten {#setting-up-a-landing-page-to-opt-out-from-all-deliveries}

To give users the ability to opt out from all deliveries, you have to create and publish a **[!UICONTROL Block list]** landing page. Weiterführende Informationen zur Landingpage-Erstellung finden Sie auf [dieser Seite](../../channels/using/getting-started-with-landing-pages.md).

Sobald ein Empfänger den Link in der Landingpage auswählt, wird automatisch die Option **[!UICONTROL Nicht mehr kontaktieren (alle Kanäle)]** im Profil des Empfängers aktiviert.

![](assets/blocklisting_allchannels.png)


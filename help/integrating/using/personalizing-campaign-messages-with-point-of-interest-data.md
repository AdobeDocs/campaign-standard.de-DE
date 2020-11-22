---
solution: Campaign Standard
product: campaign
title: Campaign-Nachrichten mit POI-Daten personalisieren
description: Hier erfahren Sie, wie Sie durch die Integration von POI-Daten eine personalisierte Nachricht entsprechend dem Standort Ihrer Abonnenten erstellen.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics-for-mobile
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 100%

---


# Campaign-Nachrichten mit POI-Daten personalisieren{#personalizing-campaign-messages-with-point-of-interest-data}

Mit den von Abonnenten Ihrer Mobile App erfassten POI-Daten können Sie diesen Abonnenten über Adobe Campaign personalisierte Marketing-Nachrichten wie E-Mails senden.

Sie können auf POI-Daten nur mit Standardsendungen reagieren. [Transaktionsnachrichten](../../channels/using/getting-started-with-transactional-msg.md) können keine Standortdaten verwenden.

Die Reaktionszeit beträgt mindestens 10 Minuten.

Im Folgenden wird beschrieben, wie Sie Abonnenten, die innerhalb der letzten zwei Wochen Ihr Geschäft in Boston besucht haben, eine E-Mail senden können:

1. Erstellen Sie eine E-Mail-Marketing-Aktivität.
1. Ziehen Sie beim Bestimmen der Versand-Audience das Element **[!UICONTROL App-Abonnements]** in den Arbeitsbereich.

   ![](assets/poi_subscriptions_app.png)

   Die Verwaltung von Audiences wird im Abschnitt [Audiences bestimmen](../../audiences/using/creating-audiences.md) beschrieben.

1. Ziehen Sie im Fenster **[!UICONTROL Regel hinzufügen - Profil/App-Abonnements]** das Element **[!UICONTROL POI-Standortmitgliedschaft]** in den Arbeitsbereich.

   ![](assets/poi_add_rule_profile_subscription.png)

1. Geben Sie im Fenster **[!UICONTROL Regel hinzufügen - POI-Standortmitgliedschaft]** den Titel des POI ein, den Sie verwenden möchten.

   ![](assets/poi_location_subscription.png)

1. Wählen Sie im Feld **[!UICONTROL Filtertyp]** die Option **[!UICONTROL Relativ]** aus.
1. Markieren Sie die Option **[!UICONTROL In den letzten Tagen]** und geben Sie im entsprechenden Feld **[!UICONTROL 15]** ein.
1. Geben Sie an, wie oft der Benutzer den POI besucht haben muss.
1. Klicken Sie auf **[!UICONTROL Validieren]**, um Ihre Audience zu speichern.

   ![](assets/poi_subscriptions_app_audience_defined.png)

1. Fügen Sie zu Ihrer E-Mail Inhalt hinzu.

   ![](assets/poi_email_content.png)

1. Bestätigen Sie die Erstellung der Aktivität, um das Dashboard der E-Mail zu öffnen.
1. Senden Sie Ihre Nachricht.

Die E-Mail mit dem Angebot eines 10 %-Rabatts wird an Abonnenten gesendet, die:

* Ihr Geschäft in Boston mindestens einmal in den letzten zwei Wochen besucht haben,
* Hatten ihre Mobile App mindestens einmal während ihres Besuchs im Vordergrund geöffnet

**Verwandte Themen:**

* [E-Mails erstellen](../../channels/using/creating-an-email.md)
* [Inhalte erstellen](../../designing/using/personalization.md#example-email-personalization)
* [Nachrichten senden](../../sending/using/confirming-the-send.md)


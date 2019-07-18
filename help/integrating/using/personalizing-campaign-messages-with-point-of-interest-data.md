---
title: Campaign-Nachrichten mit POI-Daten personalisieren
seo-title: Campaign-Nachrichten mit POI-Daten personalisieren
description: Campaign-Nachrichten mit POI-Daten personalisieren
seo-description: Hier erfahren Sie, wie Sie durch die Integration von POI-Daten eine personalisierte Nachricht entsprechend dem Standort Ihrer Abonnenten erstellen.
page-status-flag: nie aktiviert
uuid: d 74 c 3 e 55-f 130-441 b-bc 2 a -6 ddcd 5 d 9784
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird integriert
content-type: Referenz
topic-tags: working-with-campaign-and-analytics-for-mobile
discoiquuid: a 1736 ba 3-5121-4 d 01-bf 04-ebb 7 e 701 e 2 e 0
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Campaign-Nachrichten mit POI-Daten personalisieren{#personalizing-campaign-messages-with-point-of-interest-data}

Mit den von Abonnenten Ihrer Mobile App erfassten POI-Daten können Sie diesen Abonnenten über Adobe Campaign personalisierte Marketing-Nachrichten wie E-Mails senden.

Sie können auf POI-Daten nur mit Standardsendungen reagieren. [Transaktionsnachrichten](../../channels/using/about-transactional-messaging.md) können keine Standortdaten verwenden.

Die Reaktionszeit beträgt mindestens 10 Minuten.

Im Folgenden wird beschrieben, wie Sie Abonnenten, die innerhalb der letzten zwei Wochen Ihr Geschäft in Boston besucht haben, eine E-Mail senden können:

1. Erstellen Sie eine E-Mail-Marketing-Aktivität.
1. Ziehen Sie beim Bestimmen der Versand-Audience das Element **[!UICONTROL App-Abonnements]in den Arbeitsbereich.**

   ![](assets/poi_subscriptions_app.png)

   Die Verwaltung von Audiences ist im Abschnitt [Audiences bestimmen](../../audiences/using/creating-audiences.md) beschrieben.

1. Ziehen Sie im Fenster **[!UICONTROL Regel hinzufügen - Profil/App-Abonnements]** das Element **POI-Standortmitgliedschaft]in den Arbeitsbereich.[!UICONTROL **

   ![](assets/poi_add_rule_profile_subscription.png)

1. Geben Sie im Fenster **[!UICONTROL Regel hinzufügen - POI-Standortmitgliedschaft]den Titel des POI ein, den Sie verwenden möchten.**

   ![](assets/poi_location_subscription.png)

1. In the **[!UICONTROL Filter type]** field, select **[!UICONTROL Relative]**.
1. Markieren Sie die Option **[!UICONTROL In den letzten Tagen]** und geben Sie im entsprechenden Feld **15]ein.[!UICONTROL **
1. Geben Sie an, wie oft der Benutzer den POI besucht haben muss.
1. Klicken Sie auf **[!UICONTROL Validieren], um Ihre Audience zu speichern.**

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
* [Inhalte erstellen](../../designing/using/example--email-personalization.md)
* [Nachrichten senden](../../sending/using/confirming-the-send.md)


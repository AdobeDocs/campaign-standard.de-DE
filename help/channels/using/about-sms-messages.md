---
title: Über SMS-Nachrichten
seo-title: Über SMS-Nachrichten
description: Über SMS-Nachrichten
seo-description: Hier erhalten Sie die wichtigsten Informationen zum SMS-Kanal in Adobe Campaign.
page-status-flag: nie aktiviert
uuid: 14 dc 7434-8171-4 ad 1-9540-52 ca 637659 a 9
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Kanäle
content-type: Referenz
topic-tags: sms-messages
discoiquuid: 6134 fe 72-77 de -4 fd 0-b 794-4 d 966 effaccf
delivercontext-tags: Deliverycreation, Wizard; Bereitstellung, smscontent, zurück
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b0cf437ec97153b53bd4502171b24286abb25731

---


# Über SMS-Nachrichten{#about-sms-messages}

Adobe Campaign ermöglicht den Versand von Nachrichten per SMS (Short Message Service).

>[!NOTE]
>
>SMS-Kanal ist ein Add-on. Prüfen Sie diesbezüglich Ihren Lizenzvertrag.

Die Inhalt-Kachel von SMS bietet ebenfalls die Möglichkeit der Erstellung, Anpassung und Personalisierung von Nachrichteninhalten, jedoch ausschließlich im Textformat. Es ist außerdem möglich, vor dem Versand eine Vorschau der SMS zu erzeugen.

SMS, die das GSM-Alphabet verwenden, sind auf 160 Zeichen begrenzt, in Unicode verfasste SMS auf 70 Zeichen. Beachten Sie, dass gewisse Sonderzeichen einen Einfluss auf die Nachrichtenlänge haben können. Lesen Sie diesbezüglich auch den Abschnitt [SMS-Kodierung](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration).

SMS-Nachrichten können im Menü **[!UICONTROL Marketingaktivitäten]**, im Rahmen einer Kampagne oder in einem Workflow erstellt werden. Siehe [SMS erstellen](../../channels/using/creating-an-sms-message.md).

Folgende Voraussetzungen müssen gegeben sein, um SMS an Mobiltelefone senden zu können:

* ein externes Konto vom Typ **[!UICONTROL Routing]**, das für den Kanal **[!UICONTROL Mobiltelefon (SMS)]mit dem Versandmodus** Gebündelter Versand] konfiguriert wurde. **[!UICONTROL ** Lesen Sie diesbezüglich auch den Abschnitt [Routing](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing).
* eine Versandvorlage, die auf das externe Konto Bezug nimmt.

**Verwandte Themen:**

* [Marketingaktivitäten-Vorlagen](../../start/using/about-templates.md)
* [SMS-Konfiguration](../../administration/using/configuring-sms-channel.md#defining-an-sms-routing)

## SMS-Versandvorlage {#sms-delivery-template}

Adobe Campaign enthält eine vorkonfigurierte Vorlage für Sendungen auf Mobiltelefone. Diese Vorlage muss korrekt mit dem für den Kanal **[!UICONTROL Mobiltelefon (SMS)]verwendeten externen Konto verknüpft werden.** So greifen Sie zur Bearbeitung darauf zu:

1. Select **[!UICONTROL Resources]** &gt; **[!UICONTROL Templates]** &gt; **[!UICONTROL Delivery templates]** from the advanced menu.
1. Bewegen Sie die Maus über die Vorlage **[!UICONTROL Per SMS senden]** und wählen Sie die Option **Element duplizieren** aus.
1. Wählen Sie die neue Vorlage aus.
1. Benutzen Sie die Schaltfläche **[!UICONTROL Eigenschaften bearbeiten].**
1. Prüfen Sie im Bereich **[!UICONTROL Erweiterte Parameter]der Vorlageneigenschaften, ob die Vorlage korrekt mit dem für den SMS-Versand zu verwendenden externen Konto verknüpft ist.**

   ![](assets/sms_template.png)

**Verwandte Themen:**

* [Marketingaktivitäten-Vorlagen](../../start/using/about-templates.md)


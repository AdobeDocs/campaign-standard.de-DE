---
solution: Campaign Standard
product: campaign
title: Dynamische Texte definieren
description: Mit diesen Schritten können Sie unterschiedliche Texte dem Benutzer in Abhängigkeit von in Adobe Campaign definierten Bedingungen dynamisch anzeigen.
audience: designing
content-type: reference
topic-tags: defining-conditional-content
translation-type: ht
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: ht
source-wordcount: '218'
ht-degree: 100%

---


# Dynamische Texte definieren{#defining-dynamic-text}

Die Definition des dynamischen Texts erfolgt analog zur Definition des dynamischen Inhalts. Lesen Sie diesbezüglich auch den Abschnitt [Dynamische Inhalte definieren](../../designing/using/personalization.md#defining-dynamic-content-in-an-email).

>[!NOTE]
>
>Für SMS und Push-Benachrichtigungen können Sie nur dynamischen Text definieren. Für Landingpages können Sie sowohl dynamische Inhalte als auch dynamischen Text definieren. Wenn Sie dynamischen Text mit [Email Designer](../../designing/using/designing-content-in-adobe-campaign.md) definieren möchten, lesen Sie den Abschnitt [Dynamische Inhalte in einer E-Mail definieren](../../designing/using/personalization.md#defining-dynamic-content-in-an-email).

Beachten Sie, dass Ersatzzeichenpaare, Zeichen, die nicht im Basic Multilingual Plane des Unicode-Zeichensatzes enthalten sind, nicht in 2 Byte (16 Bit) gespeichert werden können und in 2 UTF-16-Zeichen kodiert werden müssen. Zu diesen Zeichen gehören einige CJK-Ideogramme, die meisten Emojis und einige Sprachen.
<br>Diese Zeichen können zu Inkompatibilitätsproblemen im dynamischen Text führen. Vor dem Senden Ihrer Nachrichten müssen Sie umfangreiche Tests durchführen.


Im folgenden Beispiel wird beschrieben, wie dynamischer Text in einer SMS definiert wird.

1. Markieren Sie innerhalb des Textkörpers Ihrer Nachricht oder Ihrer Landingpage einen Abschnitt.
1. Verwenden Sie die Schaltfläche **[!UICONTROL Dynamischen Text aktivieren]**.

   ![](assets/dynamic_text_sms_1.png)

   Daraufhin erscheint in der Palette die Option **[!UICONTROL Dynamischer Text]**. Die Konfiguration des dynamischen Texts entspricht der des dynamischen Inhalts.

1. Wählen Sie eine Variante aus.

   ![](assets/dynamic_text_sms_2.png)

1. Definieren Sie eine Bedingung für diese Variante.

   ![](assets/dynamic_text_sms_4.png)

Wenn für zumindest eine Variante eine Bedingung definiert wurde, wird um den dynamischen Text ein violetter Rahmen angezeigt.

![](assets/dynamic_text_sms_3.png)

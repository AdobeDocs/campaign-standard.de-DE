---
title: SMS personalisieren
seo-title: SMS personalisieren
description: SMS personalisieren
seo-description: Hier erhalten Sie Informationen zu Transliterationsoptionen bei der Personalisierung von SMS-Nachrichten.
page-status-flag: nie aktiviert
uuid: 123 fe 70 c-c 279-40 a 3-88 b 6-6 bfb 2453 ec 83
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Kanäle
content-type: Referenz
topic-tags: sms-messages
discoiquuid: 7 c 64785 c-e 3 c 2-4 caa-a 547-002990 aae 3 f 9
delivercontext-tags: Deliverycreation, Wizard; delivery, smscontent, back; Bereitstellung, smscontent, zurück
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b0cf437ec97153b53bd4502171b24286abb25731

---


# SMS personalisieren{#personalizing-sms-messages}

Die Personalisierung von SMS erfolgt analog zu der von [E-Mail-Inhalten](../../designing/using/inserting-a-personalization-field.md). Beachten Sie jedoch die Transliterations-Optionen, die u. U. einen Einfluss auf den verwendeten Zeichensatz und somit auf die Anzahl an gesendeten SMS haben können. Lesen Sie diesbezüglich auch den Abschnitt [Transliteration und Länge von SMS](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration).

Das folgende Beispiel zeigt einen SMS-Inhalt mit Personalisierungsfeldern, welche je nachdem, ob die Transliteration aktiviert wird oder nicht, die Verwendung eines unterschiedlichen Zeichensatzes auslösen, was wiederum die Anzahl an zu sendenden SMS beeinflusst.

**Guten Tag &lt;Vorname&gt; &lt;Nachname&gt;, die neue Kollektion ist eingetroffen. Sehen und staunen Sie jetzt in Ihrem Shop!**

* Für einen Empfänger mit Namen "Paul Schmidt" wählt Adobe Campaign das GSM-Alphabet, welches bis zu 160 Zeichen pro SMS zulässt. Die Nachricht wird also in nur einer SMS gesendet.
* Bei einem Empfänger mit Namen "Raphaël Laforêt" sind die Zeichen "ë" und "ê" nicht im GSM-Alphabet enthalten. Abhängig von der Transliterations-Konfiguration bestehen zwei Möglichkeiten:

   * Wenn die Transliteration zugelassen wurde, werden "ë" und "ê" durch "e" ersetzt. Dies ermöglicht die Verwendung des GSM-Alphabets und lässt bis zu 160 Zeichen pro SMS zu. Die Nachricht wird also in nur einer SMS gesendet, allerdings in leicht abgewandelter Form.
   * Wenn die Transliteration nicht zugelassen wurde, sendet Adobe Campaign die Nachricht in Unicode und alle Zeichen werden unverändert übermittelt. Da SMS bei Verwendung des Unicode-Zeichensatzes auf 70 Zeichen begrenzt sind, wird Adobe Campaign die Nachricht automatisch in zwei Teilen senden.

>[!NOTE]
>
>Der Algorithmus, der automatisch den besten Zeichensatz auswählt, wird auf jede Nachricht einzeln angewendet. Dies bedeutet, dass nur die personalisierten Nachrichten, die nicht dem GSM-Alphabet entsprechen, in Unicode gesendet werden.


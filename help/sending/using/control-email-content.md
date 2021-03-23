---
solution: Campaign Standard
product: campaign
title: Kontrollieren von E-Mail-Inhalten in Adobe Campaign Standard
description: Erfahren Sie, wie Sie beim Bearbeiten von E-Mail-Inhalten die Zustellbarkeit in Adobe Campaign Standard verbessern können.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: Zustellbarkeit
role: Business Practitioner
level: Fortgeschritten
translation-type: tm+mt
source-git-commit: fb9a6218bb754f803affde1fdf6c6fc01570126f
workflow-type: tm+mt
source-wordcount: '801'
ht-degree: 34%

---


# Kontrollieren von E-Mail-Inhalten{#control-email-content}

<!--TO KEEP because specific to Campaign-->

Um sicherzustellen, dass Ihre E-Mails Ihre Empfänger erreichen und Ihre E-Mail-Zustellungsrate verbessern, müssen sie eine Reihe von Regeln beachten. Andernfalls kann der Inhalt bestimmter Nachrichten als Spam erkannt werden. Adobe Campaign stellt Ihnen mehrere Tools zur Verfügung, mit denen Sie Ihre Inhalte mit diesen Regeln in Einklang bringen können.

Befolgen Sie beim Entwerfen Ihres Nachrichteninhalts die folgenden Grundsätze:

* [Name und Anschrift](#sender-name) des Absenders: die Adresse muss den Absender explizit identifizieren. Die Domäne muss sich im Besitz des Absenders befinden und beim Absender registriert sein. Das Domänenregister darf nicht privatisiert werden.

   <!--**Subject**: Avoid excessive capitalization and punctuation, and words that are frequently used by spammers ("Win", "Free", etc.).-->
* [Personalisierung und Optimierung](#perso-send-time-optimization) der Sendezeit: Die Personalisierung von Inhalten und das Definieren einer Sendezeit pro Empfänger erhöhen die Wahrscheinlichkeit, dass Ihre Nachricht geöffnet wird.
* Bilder und Text: ein angemessenes Verhältnis von Text und Bild (z. B. 60 % Text und 40 % Bilder).
* [Abmeldung ](#opt-out) und Landingpage: der Link zur Abmeldung ist unverzichtbar. Es muss sichtbar und gültig sein, und das Formular muss funktionsfähig sein.
* Vorschau: Verwenden Sie die von Adobe Campaign angebotenen Tools, um den Inhalt Ihrer E-Mail zu überprüfen und zu optimieren ([Anti-Spam-Analyse](#anti-spam-analysis), [E-Mail-Rendering](#message-responsiveness)).

Weitere Tipps zur Optimierung der Bereitstellbarkeit von Inhalten finden Sie im Leitfaden [Best Practice Guide](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/content-best-practices-for-optimal-delivery.html) zur Adobe-Bereitstellung.

>[!NOTE]
>
>Weitere Informationen zum Bearbeiten von E-Mail-Inhalten finden Sie in der [Übersicht über den E-Mail-Designer](../../designing/using/designing-content-in-adobe-campaign.md) und den [Best Practices für den Nachrichtenentwurf](../../designing/using/designing-content-in-adobe-campaign.md#content-design-best-practices).

## Name und Anschrift des Absenders {#sender-name}

Bestimmte ISPs prüfen die Gültigkeit der Absenderadresse (**[!UICONTROL Von]**), bevor sie Nachrichten annehmen. Eine schlecht geformte Adresse kann dazu führen, dass sie vom empfangenden Server abgelehnt wird.

![](assets/delivery_content_edition16.png)

Sie müssen sicherstellen, dass eine richtige Adresse auf Instanzebene oder in den am häufigsten verwendeten Szenarien angegeben wird. Wenden Sie sich dazu an Ihren Administrator.

Weitere Informationen hierzu finden Sie unter [Definieren des E-Mail-Absenders einer E-Mail](../../designing/using/subject-line.md#email-sender).

## Personalisierung und Optimierung der Sendezeit {#perso-send-time-optimization}

Um die Benutzererfahrung zu verbessern und Ihre E-Mail-Adresse zu öffnen, können Sie mit Adobe Campaign Ihre Nachrichten personalisieren. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../designing/using/personalization.md).

Um die Öffnungsrate Ihrer Nachrichten zu erhöhen, können Sie auch manuell eine Sendezeit pro Empfänger definieren. Jedes Profil erhält dann die Nachricht zum spezifizierten Zeitpunkt. Weitere Informationen dazu finden Sie unter [Versandzeitpunkt optimieren](../../sending/using/optimizing-the-sending-time.md).

## Abmelde-Link und -Formular {#opt-out}

Bei der Analyse einer Nachricht wird standardmäßig von einer Typologieregel überprüft, ob ein Abmelde-Link vorhanden ist. Ist dies nicht der Fall, wird ein Warnhinweis erstellt. Weitere Informationen zum Verwalten von Links finden Sie in [diesem Abschnitt](../../designing/using/links.md).

Sie müssen vor jedem Senden überprüfen, ob der Ausschluss-Link korrekt funktioniert. Wenn Sie beispielsweise den Testversand [senden, stellen Sie sicher, dass der Link gültig ist, dass das Formular online ist und dass bei der Überprüfung dieses Links die Felder **[!UICONTROL Keine Kontaktanschrift]** überprüft werden. ](../../sending/using/sending-proofs.md) Sie sollten diese Überprüfung systematisch durchführen, da menschliches Versagen immer möglich ist, wenn Sie den Link eingeben oder das Formular ändern. Weitere Informationen zur Verwaltung der Teilnahme- und Abmeldeoption finden Sie in [diesem Abschnitt](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md).

![](assets/optin_landingpage_3.png)

Wenn ein Abmeldeproblem erkannt wird, nachdem der Versand bereits begonnen hat, können Sie diejenigen, die auf den Abmelde-Link klicken, manuell abmelden (z. B. über die gebündelte Aktualisierung), selbst wenn sie ihre Auswahl nicht bestätigen konnten.

In der Regel sollten Sie Empfängern, die sich ausschließen möchten, nicht den Weg verwehren, indem Sie sie z. B. dazu verpflichten, Felder wie z. B. ihre E-Mail-Adresse oder ihren Namen auszufüllen. Die Landingpage der Abmeldung sollte nur eine Überprüfungsschaltfläche enthalten.

Die Anforderung zusätzlicher Bestätigung ist nicht zuverlässig: Ein Benutzer kann zwei E-Mail-Adressen in dasselbe Feld umgeleitet haben (z. B. firstname.lastname@club.com und firstname.lastname@internet-club.com). Wenn das Profil nur die erste Adresse speichern kann und sich über eine an die andere Adresse gesendete Nachricht abmelden möchte, verweigert das Formular dies, da die verschlüsselte Kennung und die eingegebene E-Mail-Adresse nicht übereinstimmen.

## Anti-Spam-Analyse {#anti-spam-analysis}

Der Nachrichteneditor von Adobe Campaign ist mit einer **Anti-Spam-Analyse** ausgestattet, mit der sich für E-Mails das Risiko bestimmen lässt, von Anti-Spam-Tools des Empfängers als Spam eingestuft zu werden. Lesen Sie diesbezüglich auch den Abschnitt [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md).

Wählen Sie im Inhaltseditor für die Nachricht die Option **[!UICONTROL Vorschau]** aus. Wenn die Anti-Spam-Prüfung ein hohes Risiko für die Nachricht feststellt, werden Sie durch eine Mitteilung gewarnt. Mit **[!UICONTROL Anti-Spam-Analyse]** können Sie die Details öffnen.

![](assets/sending_anti-spam_analysis.png)

## E-Mail-Rendering {#message-responsiveness}

Bevor Sie Ihre Nachricht senden, können Sie die Reaktionsgeschwindigkeit Ihrer Nachricht testen, indem Sie überprüfen, wie Ihre Nachricht auf verschiedenen Geräten aussehen wird. So wird sichergestellt, dass sie in unterschiedlichen Webclients, Webmails und Geräten optimal dargestellt wird.

![](assets/inbox_rendering_report_3.png)

Zu diesem Zweck unterstützt Adobe Campaign das Rendering und stellt dessen Ergebnisse in einem entsprechenden Bericht zur Verfügung. Dadurch können Sie sich ansehen, wie Nachrichten je nach verwendetem Empfangsmedium beim Empfänger dargestellt werden.

Weiterführende Informationen dazu finden Sie im Abschnitt [E-Mail-Rendering](../../sending/using/email-rendering.md).
---
title: Steuern von E-Mail-Inhalten in Adobe Campaign Standard
description: Erfahren Sie, wie Sie die Auslieferbarkeit in Adobe Campaign Standard verbessern können, wenn Sie Ihren E-Mail-Inhalt bearbeiten.
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1b70e18be29fd48d102313f6d741e9ffe053cc34

---


# Steuern von E-Mail-Inhalten{#control-email-content}

Um die Zustellrate Ihrer E-Mails zu optimieren, muss die Nachricht einer Reihe von Regeln entsprechen.

* **Name und Anschrift** des Absenders: Die Adresse muss den Absender explizit identifizieren.Die Domäne muss sich im Besitz des Absenders befinden und beim Absender registriert sein.Das Domänenregister darf nicht privatisiert werden.
* **Betrifft**: Vermeiden Sie übermäßige Groß- und Kleinschreibung sowie Wörter, die häufig von Spammer ("Win", "Free" usw.) verwendet werden.
* **E-Mail** personalisieren: Die Personalisierung der E-Mail erhöht die Wahrscheinlichkeit, dass Ihre Nachricht geöffnet wird.
* **Bilder und Text**: Achten Sie auf ein angemessenes Verhältnis von Text und Bild (z. B. 60 % Text und 40 % Bilder).
* **Link zum Rückgängigmachen des Abonnements und Einstiegsseite**: Der Link zum Abbestellen des Abonnements ist unbedingt erforderlich.Es muss sichtbar und gültig sein, und das Formular muss funktionsfähig sein.
* **Verwenden Sie Werkzeuge** von Adobe Campaign zur Optimierung des Inhalts Ihrer E-Mail (Versandanalyse, Anti-Spam-Analyse).

Weitere Informationen zum Bearbeiten von E-Mail-Inhalten finden Sie in der Übersicht über den [E-Mail-Designer](../../designing/using/designing-content-in-adobe-campaign.md) und in den Best Practices[zum ](../../designing/using/designing-content-in-adobe-campaign.md#content-design-best-practices)Nachrichtenentwurf.

## Name und Anschrift des Absenders {#sender-name}

Bestimmte ISPs prüfen die Gültigkeit der Absenderadresse (Von), bevor sie Nachrichten annehmen.Eine schlecht geformte Adresse kann dazu führen, dass sie vom empfangenden Server abgelehnt wird.Sie müssen sicherstellen, dass eine richtige Adresse auf Instanzebene oder in den am häufigsten verwendeten Szenarien angegeben wird.Wenden Sie sich an Ihren Administrator.

![](assets/delivery_content_edition16.png)

Weitere Informationen hierzu finden Sie unter [Personalisieren des Absendernamens](../../designing/using/personalization.md#personalizing-the-sender).

## Betreff {#subject-line}

Beim Bearbeiten von E-Mails können Sie verschiedene Betreffzeilen ausprobieren und dabei eine jeweilige Einschätzung der Öffnungsrate erhalten, bevor Sie die E-Mail senden. For more on this, see [Testing the subject line of an email](../../sending/using/testing-subject-line-email.md).

![](assets/predictive_subject_line_example.png)

Weitere Informationen zum Definieren der Betreffzeile einer E-Mail finden Sie in [diesem Abschnitt](../../designing/using/subject-line.md).

## Versandzeitpunkt optimieren {#send-time-optimization}

Um die Erfolgsrate Ihrer Nachrichten zu erhöhen, können Sie für jeden Empfänger manuell einen Versandzeitpunkt festlegen. Jedes Profil erhält dann die Nachricht zum spezifizierten Zeitpunkt.

Weitere Informationen hierzu finden Sie unter [Optimieren der Sendezeit](../../sending/using/optimizing-the-sending-time.md).

## Abmelde-Link und -Formular {#opt-out}

Bei der Analyse einer Nachricht wird standardmäßig von einer Typologieregel überprüft, ob ein Abmelde-Link vorhanden ist. Ist dies nicht der Fall, wird ein Warnhinweis erstellt.

Prüfen Sie vor jedem Versand, ob der Abmelde-Link ordnungsgemäß funktioniert. Achten Sie beispielsweise beim Testversand darauf, dass der Link gültig ist, das Formular online ist und dass durch seine Validierung der Wert des Feldes Nicht mehr kontaktieren aktiviert wird. Führen Sie diese Prüfung regelmäßig durch, da bei der manuellen Eingabe des Links oder der Änderung des Formulars Fehler auftreten können.

Wenn ein Abmeldeproblem erkannt wird, nachdem der Versand bereits begonnen hat, können Sie diejenigen, die auf den Abmelde-Link klicken, manuell abmelden (z. B. über die gebündelte Aktualisierung), selbst wenn sie ihre Auswahl nicht bestätigen konnten.

Generell empfehlen wir, Empfänger nicht daran zu hindern, sich abzumelden, indem Sie von ihnen verlangen, Felder wie beispielsweise ihre E-Mail-Adresse oder ihren Namen auszufüllen. Die Abmelde-Landingpage sollte nur eine einzige Validierungsschaltfläche aufweisen. Eine zusätzliche Bestätigung zu verlangen ist keine verlässliche Methode: Ein Benutzer könnte zwei E-Mail-Adressen besitzen, die zum selben Postfach gesendet werden (z. B. vorname.nachname@club.com und vorname.nachname@internet-club.com). Wenn sich der Empfänger nur an die erste Adresse erinnert und sich über eine an die andere Adresse gesendete Nachricht abmelden möchte, würde das Formular dies ablehnen, da die verschlüsselte Kennung und die eingegebene E-Mail-Adresse nicht übereinstimmen.

## Anti-Spam-Analyse {#anti-spam-analysis}

Adobe Campaign's message editor integrates an **Anti-spam analysis** which allows you to score emails to determine whether a message runs the risk of being considered as spam by the anti-spam tools used upon receipt. For more on this, see [Previewing messages](../../sending/using/previewing-messages.md).

Wählen Sie im Inhaltseditor für die Nachricht die Option **[!UICONTROL Vorschau]** aus. Wenn die Anti-Spam-Prüfung ein hohes Risiko für die Nachricht feststellt, werden Sie durch eine Mitteilung gewarnt. Mit **Anti-Spam-Analyse]können Sie die Details öffnen.[!UICONTROL **

![](assets/sending_anti-spam_analysis.png)

## Darstellung der Nachricht überprüfen {#message-responsiveness}

Bevor Sie Ihre Nachricht senden, können Sie überprüfen, wie Ihre Nachricht auf verschiedenen Geräten aussehen wird. Dadurch soll sichergestellt werden, dass es auf einer optimalen Weise auf einer Vielzahl von Web-Clients, Web-Mails und Geräten angezeigt wird.

Zu diesem Zweck unterstützt Adobe Campaign das Rendering und stellt dessen Ergebnisse in einem entsprechenden Bericht zur Verfügung. Dadurch können Sie sich ansehen, wie Nachrichten je nach verwendetem Empfangsmedium beim Empfänger dargestellt werden.

Weiterführende Informationen dazu finden Sie im Abschnitt [E-Mail-Rendering](../../sending/using/email-rendering.md).

![](assets/inbox_rendering_report_3.png)

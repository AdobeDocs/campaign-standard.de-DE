---
title: Kontrollieren von E-Mail-Inhalten in Adobe Campaign Standard
description: Erfahren Sie, wie Sie beim Bearbeiten von E-Mail-Inhalten die Zustellbarkeit in Adobe Campaign Standard verbessern können.
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
translation-type: ht
source-git-commit: 1b70e18be29fd48d102313f6d741e9ffe053cc34

---


# Kontrollieren von E-Mail-Inhalten{#control-email-content}

Wenn Sie die Zustellrate Ihrer E-Mails optimieren möchten, müssen die Nachrichten einer Reihe von Regeln entsprechen.

* **Name und Adresse des Absenders:** Die Adresse muss die Identität eines Absenders enthalten. Die Domain muss im Besitz des Absenders und auf ihn registriert sein. Die Domain-Registrierung darf nicht anonymisiert sein.
* **Betreff:** Vermeiden Sie übermäßige Großschreibung und Satzzeichen sowie häufig von Spammern verwendete Begriffe (&quot;gewinnen&quot;, &quot;gratis&quot; etc.).
* **Personalisieren Sie Ihre E-Mails:** Eine Personalisierung von E-Mails erhöht die Wahrscheinlichkeit, dass sie geöffnet werden.
* **Bilder und Text:** Achten Sie auf ein gefälliges Verhältnis zwischen Text und Bildern (z. B. 60 % Text und 40 % Bilder).
* **Abmelde-Link und -Landingpage:** Ein Abmelde-Link muss unbedingt vorhanden sein. Er muss gut sichtbar und gültig sein; außerdem muss das Formular funktionieren.
* **Verwenden Sie Werkzeuge** von Adobe Campaign zur Optimierung des Inhalts Ihrer E-Mail (Versandanalyse, Anti-Spam-Analyse).

Weitere Informationen zum Bearbeiten von E-Mail-Inhalten finden Sie in der Übersicht zu [Email Designer](../../designing/using/designing-content-in-adobe-campaign.md) und in den [Best Practices zur Nachrichtengestaltung](../../designing/using/designing-content-in-adobe-campaign.md#content-design-best-practices).

## Name und Anschrift des Absenders {#sender-name}

Manche ISPs prüfen die Gültigkeit der Absenderadresse (Von), bevor sie Nachrichten akzeptieren. Eine schlecht formulierte Adresse könnte vom Empfangs-Server abgelehnt werden. Achten Sie darauf, dass auf Instanzenebene oder in den am häufigsten verwendeten Szenarien eine korrekte Adresse vorhanden ist. Kontaktieren Sie diesbezüglich Ihren Administrator.

![](assets/delivery_content_edition16.png)

Siehe auch den Abschnitt zur [Personalisierung des Absendernamens](../../designing/using/personalization.md#personalizing-the-sender).

## Betreff {#subject-line}

Beim Bearbeiten von E-Mails können Sie verschiedene Betreffzeilen ausprobieren und dabei eine jeweilige Einschätzung der Öffnungsrate erhalten, bevor Sie die E-Mail senden. Weitere Informationen dazu finden Sie unter [Betreffzeile einer E-Mail testen](../../sending/using/testing-subject-line-email.md).

![](assets/predictive_subject_line_example.png)

Weitere Informationen zum Definieren der Betreffzeile einer E-Mail finden Sie in [diesem Abschnitt](../../designing/using/subject-line.md).

## Versandzeitpunkt optimieren {#send-time-optimization}

Um die Erfolgsrate Ihrer Nachrichten zu erhöhen, können Sie für jeden Empfänger manuell einen Versandzeitpunkt festlegen. Jedes Profil erhält die Nachricht dann zum spezifizierten Zeitpunkt.

Weitere Informationen dazu finden Sie unter [Versandzeitpunkt optimieren](../../sending/using/optimizing-the-sending-time.md).

## Abmelde-Link und -Formular {#opt-out}

Bei der Analyse einer Nachricht wird standardmäßig von einer Typologieregel überprüft, ob ein Abmelde-Link vorhanden ist. Ist dies nicht der Fall, wird ein Warnhinweis erstellt.

Prüfen Sie vor jedem Versand, ob der Abmelde-Link ordnungsgemäß funktioniert. Achten Sie beispielsweise beim Testversand darauf, dass der Link gültig ist, das Formular online ist und durch seine Validierung der Wert des Feldes &quot;Nicht mehr kontaktieren&quot; aktiviert wird. Führen Sie diese Prüfung regelmäßig durch, da bei manueller Eingabe des Links oder Änderung des Formulars Fehler auftreten können.

Wenn ein Abmeldeproblem erkannt wird, nachdem der Versand bereits begonnen hat, können Sie diejenigen, die auf den Abmelde-Link klicken, manuell abmelden (z. B. über die gebündelte Aktualisierung), selbst wenn sie ihre Auswahl nicht bestätigen konnten.

Generell empfehlen wir, Empfänger nicht daran zu hindern, sich abzumelden, indem Sie von ihnen verlangen, Felder wie beispielsweise ihre E-Mail-Adresse oder ihren Namen auszufüllen. Die Abmelde-Landingpage sollte nur eine einzige Validierungsschaltfläche aufweisen. Eine zusätzliche Bestätigung zu verlangen, ist keine verlässliche Methode: Ein Benutzer könnte zwei E-Mail-Adressen besitzen, die zum selben Postfach gesendet werden (z. B. vorname.nachname@club.com und vorname.nachname@internet-club.com). Wenn sich der Empfänger nur an die erste Adresse erinnert und sich über eine an die andere Adresse gesendete Nachricht abmelden möchte, würde das Formular dies ablehnen, da die verschlüsselte Kennung und die eingegebene E-Mail-Adresse nicht übereinstimmen.

## Anti-Spam-Analyse {#anti-spam-analysis}

Der Nachrichteneditor von Adobe Campaign ist mit einer **Anti-Spam-Analyse** ausgestattet, mit der sich für E-Mails das Risiko bestimmen lässt, von Anti-Spam-Tools des Empfängers als Spam eingestuft zu werden. Lesen Sie diesbezüglich auch den Abschnitt [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md).

Wählen Sie im Inhaltseditor für die Nachricht die Option **[!UICONTROL Vorschau]**aus. Wenn die Anti-Spam-Prüfung ein hohes Risiko für die Nachricht feststellt, werden Sie durch eine Mitteilung gewarnt. Mit**[!UICONTROL  Anti-Spam-Analyse]** können Sie die Details öffnen.

![](assets/sending_anti-spam_analysis.png)

## Darstellung der Nachricht überprüfen {#message-responsiveness}

Bevor Sie Ihre Nachricht senden, können Sie überprüfen, wie diese auf verschiedenen Geräten aussehen wird. So wird sichergestellt, dass sie in unterschiedlichen Webclients, Webmails und Geräten optimal dargestellt wird.

Zu diesem Zweck unterstützt Adobe Campaign das Rendering und stellt dessen Ergebnisse in einem entsprechenden Bericht zur Verfügung. Dadurch können Sie sich ansehen, wie Nachrichten je nach verwendetem Empfangsmedium beim Empfänger dargestellt werden.

Weiterführende Informationen dazu finden Sie im Abschnitt [E-Mail-Rendering](../../sending/using/email-rendering.md).

![](assets/inbox_rendering_report_3.png)

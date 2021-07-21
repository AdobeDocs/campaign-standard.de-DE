---
solution: Campaign Standard
product: campaign
title: Vor dem Senden prüfen
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
description: '"Erfahren Sie, wie Sie im Anschluss an die Fertigstellung Ihrer Nachricht alle Prüfungen durchführen, bevor Sie sie versenden."'
feature: Zustellbarkeit
role: User
level: Intermediate
exl-id: dfc5fc00-87aa-4d22-ad7c-cc0ba1ee21be
source-git-commit: aeeb6b4984b3bdd974960e8c6403876fdfedd886
workflow-type: ht
source-wordcount: '412'
ht-degree: 100%

---

# Durchführen aller Prüfungen vor dem Senden {#perform-all-checks}

Wenn Ihre Nachricht fertig ist, prüfen Sie, ob ihr Inhalt auf allen Geräten richtig dargestellt wird, und stellen Sie sicher, dass sie keine Fehler wie falsche Personalisierung oder defekte Links enthält.

Prüfen Sie vor dem Nachrichtenversand außerdem, ob die Parameter und die Konfiguration dem Versand entsprechen.

## Warum die Validierung wichtig ist {#validation-is-key}

Bevor Sie einen Versand durchführen, müssen Sie sicherstellen, dass Ihre Empfänger tatsächlich die Nachricht erhalten, die Sie ihnen senden möchten. Zu diesem Zweck müssen Sie den Nachrichteninhalt und die Versandparameter validieren.

Durch diese Maßnahme können Sie mögliche Fehler erkennen und beheben, bevor Sie den Versand an Ihre Hauptzielgruppe durchführen.

In [diesem Abschnitt](../../sending/using/get-started-sending-messages.md#prepare-test-send) werden die Schritte zur Validierung eines Versands vorgestellt.

## E-Mail-Rendering {#email-rendering}

Bevor Sie die Schaltfläche **[!UICONTROL Senden]** betätigen, sollten Sie sicherstellen, dass Ihre Nachricht in unterschiedlichen Web-Clients, Web-Mails und Geräten optimal dargestellt wird.

Zu diesem Zweck unterstützt Adobe Campaign das Rendering und stellt dessen Ergebnisse in einem entsprechenden Bericht zur Verfügung. Dadurch können Sie sich ansehen, wie Nachrichten je nach verwendetem Empfangsmedium beim Empfänger dargestellt werden.

**Tipps**:

* Sie können sich ansehen, wie Nachrichten je nach verwendetem Empfangsmedium (Smartphones und Tablets, Web-Clients etc.) beim Empfänger dargestellt werden.

* Fähigkeiten zum E-Mail-Rendering sind entscheidend, um festzustellen, ob Ihre E-Mail-Kampagnen erfolgreich durch die Filter der großen ISPs (Internet Service Provider) und Webmail-Dienste befördert werden. Diese Tools senden vorab eine Kopie einer E-Mail an ein Netzwerk von Test-Posteingängen, damit Sie sehen, wie eine Nachricht in diesen Diensten dargestellt wird. Manche dieser Tools bieten auch Berichte und Code-Korrektur-Möglichkeiten, mit denen Sie Fehler rasch erkennen und beheben und so die Zustellbarkeit verbessern können.

Weitere Informationen finden Sie in [diesem Abschnitt](../../sending/using/email-rendering.md).

## Nachrichten in Testsendungen {#proof-messages}

Mit Testsendungen können Sie den Abmelde-Link, die Mirrorseite und andere Links testen, die Nachricht validieren, die Anzeige von Bildern überprüfen, mögliche Fehler erkennen etc. Außerdem können Sie Ihr Design und die Darstellung auf verschiedenen Geräten testen.

Weiterführende Informationen finden Sie [in diesem Abschnitt](../../sending/using/sending-proofs.md).

## Einrichten von A/B-Test-Sendungen {#a-b-testing-deliveries}

Wenn mehrere Versionen von Inhalten für den E-Mail-Versand vorhanden sind, können Sie mithilfe von A/B-Tests feststellen, welche Version die größte Auswirkung auf die Zielkontakte hat.

**Tipps**:

* Senden Sie die unterschiedlichen Versionen an einige Ihrer Empfänger.

* Wählen Sie die Version mit der höchsten Erfolgsquote aus und senden Sie sie an die restliche Zielgruppe.

Weiterführende Informationen finden Sie [in diesem Abschnitt](../../channels/using/designing-an-a-b-test-email.md).

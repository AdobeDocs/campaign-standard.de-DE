---
title: Prüfen vor dem Senden
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: true
description: Sobald Ihre Nachricht fertig ist, führen Sie alle Prüfungen vor dem Senden durch
feature: Deliverability
role: User
level: Intermediate
exl-id: dfc5fc00-87aa-4d22-ad7c-cc0ba1ee21be
TQID: https://experienceleague.adobe.com/3qM5opRzD4u8HV5PALkfERzsLnWx1AsLuaDs8frG-Ic
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2: id: a075b2c1-7748-4328-b7f6-343aa314616a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 413
ht-degree: 100%

---

# Durchführen aller Prüfungen vor dem Senden {#perform-all-checks}

Wenn Ihre Nachricht fertig ist, prüfen Sie, ob ihr Inhalt auf allen Geräten richtig dargestellt wird, und stellen Sie sicher, dass sie keine Fehler wie falsche Personalisierung oder defekte Links enthält.

Prüfen Sie vor dem Nachrichtenversand außerdem, ob die Parameter und die Konfiguration dem Versand entsprechen.

## Warum die Validierung wichtig ist {#validation-is-key}

Bevor Sie einen Versand durchführen, müssen Sie sicherstellen, dass Ihre Empfänger bzw. Empfängerinnen tatsächlich die Nachricht erhalten, die Sie ihnen senden möchten. Dazu müssen Sie den Nachrichteninhalt und die Versandparameter validieren.

Durch diese Maßnahme können Sie mögliche Fehler erkennen und beheben, bevor Sie den Versand an Ihre Hauptzielgruppe durchführen.

In [diesem Abschnitt](../../sending/using/get-started-sending-messages.md#prepare-test-send) werden die Schritte zur Validierung eines Versands vorgestellt.

## E-Mail-Rendering {#email-rendering}

Bevor Sie die Schaltfläche **[!UICONTROL Senden]** betätigen, sollten Sie sicherstellen, dass Ihre Nachricht in unterschiedlichen Web-Clients, Web-Mails und Geräten optimal dargestellt wird.

Zu diesem Zweck unterstützt Adobe Campaign das Rendering und stellt dessen Ergebnisse in einem entsprechenden Bericht zur Verfügung. Dadurch können Sie sich ansehen, wie Nachrichten je nach verwendetem Empfangsmedium beim Empfänger dargestellt werden.

**Tipps**:

* Sie können sich ansehen, wie Nachrichten je nach verwendetem Empfangsmedium (Mobilgeräte, Web-Clients etc.) beim Empfänger dargestellt werden.

* E-Mail-Rendering-Funktionen sind von entscheidender Bedeutung, um festzustellen, ob Ihre E-Mail-Kampagnen die Filter der wichtigsten ISPs (Internet Service Provider) und Webmail-Dienste erfolgreich passieren. Solche Tools senden eine Pre-Flight-Kopie einer E-Mail an ein Netzwerk von Test-Posteingängen, sodass Sie sehen können, wie die Nachricht über diese Dienste hinweg angezeigt oder gerendert wird. Sie können auch Berichte und Optionen zur Code-Korrektur enthalten, mit denen Sie schnell Korrekturen zur Verbesserung der Zustellbarkeit ermitteln und vornehmen können.

Weitere Informationen finden Sie in [diesem Abschnitt](../../sending/using/email-rendering.md).

## Nachrichten in Testsendungen {#proof-messages}

Mit Testsendungen können Sie den Ausschluss-Link, die Mirrorseite und andere Links testen, die Nachricht validieren, die Anzeige von Bildern überprüfen und mögliche Fehler erkennen. Außerdem können Sie das Design und die Darstellung auf verschiedenen Geräten testen.

Weiterführende Informationen finden Sie [in diesem Abschnitt](../../sending/using/sending-proofs.md).

## Einrichten von A/B-Test-Sendungen {#a-b-testing-deliveries}

Wenn mehrere Versionen von Inhalten für den E-Mail-Versand vorhanden sind, können Sie mithilfe von A/B-Tests feststellen, welche Version die größte Auswirkung auf die Zielpopulation hat.

**Tipps**:

* Senden Sie die unterschiedlichen Versionen an einige Ihrer Empfänger.

* Wählen Sie die Version mit der höchsten Erfolgsquote aus und senden Sie sie an die restliche Zielgruppe.

Weiterführende Informationen finden Sie [in diesem Abschnitt](../../channels/using/designing-an-a-b-test-email.md).

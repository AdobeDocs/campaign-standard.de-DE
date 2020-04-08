---
title: Über den Versand mit Campaign
description: Hier erfahren Sie über die erforderlichen Schritte zum Testen und Senden einer Nachricht.
page-status-flag: never-activated
uuid: 58666444-6e7c-4049-b2d2-8b26eabf5a82
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: about-sending-messages-with-campaign
discoiquuid: ae2eba1c-24ad-4839-afa9-5a2975570d9b
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c49fcd793cbb13d26ccf3a47af145de7acd697e7

---


# Über den Versand mit Campaign{#about-sending-messages-with-campaign}

Nachdem Sie die Zielgruppe definiert und den Inhalt einer Nachricht erstellt haben, müssen Sie Inhalte, Personalisierung, Wiedergabe und Konfiguration testen und genehmigen und sicherstellen, dass alles korrekt ist, bevor Sie die Nachricht an die Hauptversion senden.

Zu diesem Zweck werden folgende Best Practices angewendet:

* Bereiten Sie den Versand vor: In diesem Schritt werden die zu sendenden Nachrichten analysiert und vorbereitet. Bei der Nachrichtenvorbereitung wird die Zielgruppe, die Personalisierung und die Gültigkeit der Nachricht analysiert. Fehler, die bei diesem Schritt erkannt werden, müssen vor dem weiteren Vorgehen korrigiert werden. Sie können die Nachrichtenvorbereitung beliebig oft starten. For more on message preparation, refer to [this section](../../sending/using/preparing-the-send.md).

   >[!NOTE]
   >
   >Sie können globale, kanalübergreifende Ermüdungsregeln festlegen, mit denen Profile, die bereits zu oft angesprochen wurden, automatisch von Kampagnen ausgeschlossen werden. Näheres dazu finden Sie unter [Ermüdungsregeln](../../sending/using/fatigue-rules.md).

* Meldungen zur Vorschau mithilfe eines Test-Profils. For more on previewing messages, refer to [this section](../../sending/using/previewing-messages.md).
* Senden Sie Testversand zum Testen von Nachrichten. For more on proofs, refer to [this  section](../../sending/using/sending-proofs.md).
* Prüfen Sie die Meldungswiedergabe: Stellen Sie sicher, dass Ihre Nachricht auf verschiedenen Web-Clients, Web-E-Mails und Geräten optimal angezeigt wird. Learn more about Email rendering in [this section](../../sending/using/email-rendering.md).

Anschließend können Sie:

* Planen Sie den Versand: Sie können festlegen, wann Nachrichten gesendet werden. Sie können beispielsweise das Senden an die Zeitzone des Empfängers anpassen, die Sendezeit optimieren oder das Versanddatum berechnen. Learn more in [this section](../../sending/using/about-scheduling-messages.md).
* Senden Sie die Nachricht: Wenn die Nachricht sendebereit ist, können Sie den Versand starten. Öffnen Sie Protokolle und Berichte, um die Zustellung Ihrer Nachricht zu verfolgen und die Wirkung Ihrer Kampagne zu messen. Adobe Campaign verfügt auch über ein E-Mail-Warnsystem, über das Sie von erfolgreichen und fehlgeschlagenen Sendungen informiert werden. Weitere Informationen finden Sie auf [dieser Seite](../../sending/using/confirming-the-send.md).

## Verwandte Themen

| Nützliche Seiten | Zusätzliche Ressourcen |
|---|---|
| [Zustellbarkeit optimieren](../../sending/using/about-deliverability.md) | [Ermüdungsverwaltung](../../sending/using/fatigue-rules.md) |
| [Steuern des Durchsatzes von Versänden](../../reporting/using/delivery-throughput.md) | [Entwerfen von E-Mails zum A/B-Test](../../channels/using/designing-an-a-b-test-email.md) |
| [Empfang einer Benachrichtigung bei einem Fehler](../../sending/using/receiving-alerts-when-failures-happen.md) | [Sendungen beobachten](../../sending/using/monitoring-a-delivery.md) |
| [Kontrollgruppe erstellen](../../automating/using/workflow-control-group.md) | [Weiterleitungsmeldungen senden](../../channels/using/follow-up-messages.md) |
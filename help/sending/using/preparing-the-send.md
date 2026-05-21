---
title: Versandvorbereitung
description: Hier erfahren Sie, wie Sie einen Versand vorbereiten.
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
feature: Send Time Optimization
role: User
level: Intermediate
exl-id: 0140c41a-7255-4b77-a1b7-c6f7b1135e51
TQID: https://experienceleague.adobe.com/ARRxgarwKQmsl21vcz-rJ6MzcLP6RDmMnsBJDVsH25c
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2:
  - id: a075b2c1-7748-4328-b7f6-343aa314616a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 465
ht-degree: 100%

---

# Versandvorbereitung{#preparing-the-send}

In diesem Schritt werden die Zielpopulation berechnet und der Nachrichteninhalt für jedes Profil in der Zielgruppe erzeugt. Sobald die Vorbereitung abgeschlossen ist, können die Nachrichten entweder sofort oder am [geplanten Datum und zur geplanten Uhrzeit](../../sending/using/about-scheduling-messages.md) gesendet werden.

1. Klicken Sie in der Aktionsleiste auf die Schaltfläche **Vorbereiten**, um die Vorbereitung zu starten.

   ![](assets/preparing_delivery_2.png)

1. In der Kachel **[!UICONTROL Bereitstellung]** werden zunächst der Vorbereitungsfortschritt und dann das Ergebnis der Vorbereitung angezeigt: die Anzahl der in der Zielgruppe enthaltenen Kontakte und zu sendenden Nachrichten usw.

   Abhängig von der Größe der Ziel-Population kann dieser Vorgang einige Zeit in Anspruch nehmen.

   ![](assets/preparing_delivery.png)

1. Die Schaltfläche **Anhalten** in der Aktionsleiste ermöglicht es, die Vorbereitung jederzeit zu unterbrechen.

   Dies ist mit keinerlei Risiko verbunden, da in dieser Phase keine Nachrichten gesendet werden. Je nach Größe der Zielgruppe kann die Dauer der Versandvorbereitung variieren.

   ![](assets/preparing_delivery_6.png)

1. Ihre Nachricht wird automatisch während der Versandvorbereitung gespeichert. Wenn Sie nach dem Vorbereitungsschritt den Zeitplan Ihrer Nachricht ändern müssen, wählen Sie die Schaltfläche **[!UICONTROL Vorbereiten]** erneut aus, damit diese Änderungen wirksam werden. Weiterführende Informationen zur Planung einer Nachricht finden Sie auf [dieser Seite](../../sending/using/about-scheduling-messages.md).

   ![](assets/preparing_delivery_5.png)

1. Verwenden Sie zur Anzeige der Vorbereitungslogs die Schaltfläche unten rechts in der Kachel.

   ![](assets/preparing_delivery_4.png)

1. Das Fenster **[!UICONTROL Bereitstellung]** wird geöffnet. Korrigieren Sie etwaige Fehler und starten Sie die Vorbereitung neu.

   Der letzte Logeintrag zeigt eventuelle Fehler und deren Anzahl an. Ein spezifisches Symbol verdeutlicht den Fehlertyp: Ein gelbes Symbol kennzeichnet beispielsweise einen nicht blockierenden Verarbeitungsfehler, während ein rotes Symbol einen Fehler bezeichnet, der den Versand der Nachrichten verhindert.

   ![](assets/preparing_delivery_3.png)

1. Prüfen Sie das Vorbereitungsergebnis, bevor Sie den Versand der Nachrichten bestätigen. Wenn die Anzahl zu sendender Nachrichten nicht Ihrer Konfiguration entspricht, passen Sie die Zielpopulationsbestimmung an (siehe [Zielgruppe in einer Nachricht auswählen](../../audiences/using/selecting-an-audience-in-a-message.md)) und starten Sie die Vorbereitung neu.

Nach Abschluss der Vorbereitung ist die Nachricht versandbereit. Weiterführende Informationen dazu finden Sie im Abschnitt [Versand bestätigen](../../sending/using/confirming-the-send.md).

**Typologieregeln**

Adobe Campaign ist mit integrierten Typologieregeln ausgestattet, die während der Nachrichtenvorbereitung angewendet werden. Mithilfe dieser Regeln wird geprüft, ob eine Nachricht gültig ist und Ihre Qualitätskriterien erfüllt. Näheres dazu finden Sie unter [Typologien](../../sending/using/about-typology-rules.md). Sie können Ihre eigenen Typologieregeln definieren, wie beispielsweise globale, kanalübergreifende Ermüdungsregeln, mit denen Profile, die bereits zu oft angesprochen wurden, automatisch von Kampagnen ausgeschlossen werden. Näheres dazu finden Sie unter [Ermüdungsregeln](../../sending/using/fatigue-rules.md).

**Kontrolle von SMS-Nachrichten**

Die Verwendung von Personalisierungsfeldern oder bedingten Texten im SMS-Inhalt kann dazu führen, dass u. U. nicht von GSM unterstützte Zeichen eingefügt werden. Im Zuge der Vorbereitung wird die Nachrichtenlänge geprüft und bei Überschreiten der Höchstgrenze ein Warnhinweis ausgelöst.

Weiterführende Information dazu finden Sie in den Abschnitten [Kodierung, Länge und Tansliteration von SMS](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration) und [SMS personalisieren](../../channels/using/personalizing-sms-messages.md).

---
solution: Campaign Standard
product: campaign
title: Die wichtigsten Schritte zum Einrichten einer Transaktionsnachricht
description: Erfahren Sie, was Transaktionsnachrichten sind, und lernen Sie die wichtigsten Schritte zum Einrichten einer Transaktionsnachricht in Adobe Campaign Standard kennen.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
translation-type: tm+mt
source-git-commit: 00032b1a8bfef301d1a87750695ba1670b2eed6c
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 63%

---


# Erste Schritte mit Transaktionsnachrichten {#getting-started-with-transactional-messaging}

## Übersicht {#overview}

### Was ist eine Transaktionsnachricht?

Es handelt sich dabei um eine individuelle und einzigartige Kommunikation, die von einem Anbieter wie einer Website in Echtzeit gesendet wird. Sie wird erwartet, weil sie wichtige Informationen enthält, die der Empfänger überprüfen oder bestätigen möchte.

* **Wann wird diese Nachricht gesendet?** Da diese Nachricht wichtige Informationen enthält, erwartet der Benutzer, dass sie in Echtzeit gesendet wird. Folglich muss die Verzögerung zwischen der Auslösung des Ereignisses und dem Eintreffen der Nachricht sehr kurz sein.

* **Warum ist das wichtig?** Im Allgemeinen hat eine Transaktionsnachricht hohe Öffnungsraten. Es sollte daher sorgfältig konzipiert werden, da es starke Auswirkungen auf das Verhalten der Kunden haben kann, da es die Kundenbeziehung definiert.

* **Beispiel?** Es kann sich um eine Begrüßungsnachricht nach der Erstellung eines Kontos, eine Bestätigung, dass eine Bestellung versandt wurde, eine Rechnung, eine Nachricht zur Bestätigung einer Passwortänderung oder eine Benachrichtigung nach dem Besuch einer Website durch einen Kunden handeln...

### Transaktionsnachricht senden

In Adobe Campaign empfängt die entsprechende Funktion Ereignisse von einem Informationssystem, auf die sie mit personalisierten Transaktionsnachrichten reagiert.

Transaktionsnachrichten können je nach Ihren Optionen per E-Mail, SMS oder Push-Benachrichtigung versendet werden. Prüfen Sie diesbezüglich Ihren Lizenzvertrag.

>[!NOTE]
>
>In Adobe Campaign hat die Verarbeitung von Transaktionsnachrichten Priorität vor allen anderen Sendungen.

Transaktionsnachrichten sind auch in der Adobe Campaign Standard API verfügbar. Weitere Informationen hierzu finden Sie in der [Dokumentation](../../api/using/managing-transactional-messages.md).

>[!NOTE]
>
>Alle Transaktionsnachrichten werden nun mit dem erweiterten MTA von Adobe Campaign gesendet, um die Zustellbarkeit, den Durchsatz und die Bounce-Handhabung zu verbessern. Alle Auswirkungen sind dieselben wie bei standardmäßigen Marketing-Nachrichten. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../administration/using/configuring-email-channel.md).

### Transaktionsnachrichtentypen {#transactional-message-types}

In Adobe Campaign sind zwei Arten von Transaktionsnachrichten verfügbar:

**Ereignis-Transaktionsnachrichten** zielen auf ein Ereignis ab:
* Sie enthalten keine Informationen zum Profil.
* Sie sind nicht mit Ermüdungsregeln kompatibel (auch nicht im Falle einer Anreicherung mit Profilen).
* Die Zielgruppe des Versands wird durch die Daten definiert, die im Ereignis selbst enthalten sind.

**Profil-Transaktionsnachrichten** zielen auf Profil aus der Kampagne Marketing-Datenbank ab. Mit dieser Art von Nachrichten können Sie:
* Wenden Sie [Marketing-Typologieregeln](../../sending/using/managing-typology-rules.md) oder [Ermüdungsregeln](../../sending/using/fatigue-rules.md) an.
* einen Abmelde-Link in die Nachricht einfügen
* die Transaktionsnachrichten zur allgemeinen Versandberichterstattung hinzufügen
* die Transaktionsnachrichten für die Customer Journey nutzen

Der Nachrichtentyp wird bei der Konfiguration des Ereignisses definiert, das eine Transaktionsnachricht auslösen soll. Siehe [diesen Abschnitt](../../channels/using/configuring-transactional-event.md#transactional-event-specific-configurations).

>[!IMPORTANT]
>
>Sie können nur dann auf alle Transaktionsnachrichten zugreifen, wenn Sie der Sicherheitsgruppe **[!UICONTROL Administratoren (alle Einheiten)]** angehören.

## Funktionsweise von Transaktionsnachrichten {#transactional-messaging-operating-principle}

Der gesamte Prozess der Transaktionsnachrichten kann wie folgt beschrieben werden:

![](assets/message-center-process.png)

Nehmen wir beispielsweise an, Sie sind eine Firma mit einer Website, auf der Ihre Kunden Produkte kaufen können.

Mit Adobe Campaign können Sie eine Benachrichtigungs-E-Mail an Kunden senden, die dem Warenkorb Produkte hinzugefügt haben: Wenn einer von ihnen Ihre Website verlässt, ohne mit seinen Einkäufen fertig zu werden (externes Ereignis, das ein Kampagne-Ereignis auslöst), wird ihm automatisch eine Warenkorbabbruchs-E-Mail zugesendet (Transaktionsnachricht-Versand).

<!--The steps for putting this into place are detailed below.-->

### Die wichtigsten Schritte {#key-steps}

Die wichtigsten Schritte beim Erstellen und Verwalten personalisierter Transaktionsnachrichten in Adobe Campaign sind in der folgenden Tabelle zusammengefasst.

![](assets/message-center-overview.png)

Jeder dieser Schritte wird nachfolgend beschrieben.

### Schritt 1: Ereigniskonfiguration erstellen und publizieren {#create-event-configuration}

<img src="assets/do-not-localize/icon_config.svg" width="60px">

| Benutzer | Aktion | Ergebnis |
|--- |--- |--- |
| Dieser Schritt muss von einem Benutzer mit [Administratorrechten](../../administration/using/users-management.md#functional-administrators) ausgeführt werden. | Konfigurieren Sie ein Ereignis mit dem Namen „Warenkorbabbruch“ und publizieren Sie diese Ereigniskonfiguration. | Die von Ihrem Website-Entwickler verwendete API wird bereitgestellt und eine Transaktionsnachricht automatisch erstellt. |

Das Erstellen und Veröffentlichen eines Ereignisses wird in den Abschnitten [Konfigurieren eines transaktionalen Ereignisses](../../channels/using/configuring-transactional-event.md) und [Veröffentlichen eines transaktionalen Ereignisses](../../channels/using/publishing-transactional-event.md) beschrieben.

### Schritt 2: Transaktionsnachricht bearbeiten und publizieren {#create-transactional-message}

<img src="assets/do-not-localize/icon_notification.svg" width="40px">

| Benutzer | Aktion | Ergebnis |
|--- |--- |--- |
| Dieser Schritt kann von jedem Marketing-Anwender mit [grundlegenden Zugriffsrechten](../../administration/using/users-management.md#basic-users) ausgeführt werden. | Bearbeiten und personalisieren Sie die Transaktionsnachricht, testen Sie sie und publizieren Sie sie dann. | Die Transaktionsnachricht kann dann gesendet werden. |

Weitere Informationen zum Bearbeiten und Veröffentlichen einer Transaktionsnachricht finden Sie unter [Bearbeiten von Transaktionsnachrichten](../../channels/using/editing-transactional-message.md) und [Transaktionsnachricht-Lebenszyklus](../../channels/using/publishing-transactional-message.md).

### Schritt 3: Ereignis-Aktivierung integrieren {#integrate-event-trigger}

<img src="assets/do-not-localize/icon_api.svg" width="55px">

<!--**Event triggering integration**-->

| Benutzer | Aktion | Ergebnis |
|--- |--- |--- |
| Dieser Schritt wird vom Entwickler Ihrer Website ausgeführt. | Verwenden Sie die REST-Transaktionsnachrichten-API, um das Ereignis in Ihre Website zu integrieren. | Das Ereignis wird ausgelöst, wenn ein Kunde seinen Warenkorb abbricht. |

Nachdem Sie ein Ereignis erstellt haben, müssen Sie die Auslösung dieses Ereignisses in Ihre Website integrieren.<!--In this example, you want a "Cart abandonment" event to be triggered whenever one of your clients leaves your website before purchasing the products in their cart.-->**Zu diesem Zweck muss der Web-Entwickler Ihrer Seite die Adobe Campaign Standard REST-API verwenden**.

Weitere Informationen zur Verwendung der Kampagne REST API zum Verwalten von Transaktionsnachrichten finden Sie in der [REST API-Dokumentation](../../api/using/managing-transactional-messages.md).

### Schritt 4: Nachrichtenversand {#message-delivery}

<img src="assets/do-not-localize/icon_channels.svg" width="60px">

Sobald alle diese Schritte ausgeführt wurden, kann die Nachricht gesendet werden.

Sobald ein Benutzer die Website verlässt, ohne die Produkte in seinem Warenkorb zu bestellen, wird das entsprechende Campaign-Ereignis ausgelöst. Der Benutzer erhält automatisch eine Benachrichtigungs-E-Mail.

## Verwandte Themen

* [Die wichtigsten Schritte im Nachrichtenversand](../../channels/using/key-steps-to-send-a-message.md)
* [Erste Schritte mit Kommunikationskanälen](../../channels/using/get-started-communication-channels.md)
* [Push-Benachrichtigungen für Transaktionen](../../channels/using/transactional-push-notifications.md)
* [Folgenachrichten](../../channels/using/follow-up-messages.md)

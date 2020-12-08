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
source-git-commit: c276c468627208b584a0342414cdbe382e349f50
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 39%

---


# Erste Schritte mit Transaktionsnachrichten {#getting-started-with-transactional-messaging}

## Übersicht {#overview}

<img src="assets/do-not-localize/icon_transactional.svg" width="60px">

Eine Transaktionsnachricht ist eine individuelle und einzigartige Kommunikation, die von einem Anbieter wie einer Website in Echtzeit gesendet wird. Sie wird erwartet, weil sie wichtige Informationen enthält, die der Empfänger überprüfen oder bestätigen möchte.

* **Wann wird diese Nachricht gesendet?** Da diese Nachricht wichtige Informationen enthält, erwartet der Benutzer, dass sie in Echtzeit gesendet wird. Folglich muss die Verzögerung zwischen der Auslösung des Ereignisses und dem Eintreffen der Nachricht sehr kurz sein.

* **Warum ist das wichtig?** Im Allgemeinen hat eine Transaktionsnachricht hohe Öffnungsraten. Es sollte daher sorgfältig konzipiert werden, da es starke Auswirkungen auf das Verhalten der Kunden haben kann, da es die Kundenbeziehung definiert.

* **Beispiel?** Es kann sich um eine Begrüßungsnachricht nach der Erstellung eines Kontos, eine Bestätigung, dass eine Bestellung versandt wurde, eine Rechnung, eine Meldung zur Bestätigung einer Passwortänderung oder eine Benachrichtigung nach dem Besuch einer Website durch einen Kunden usw. handeln.

In Adobe Campaign empfängt die entsprechende Funktion Ereignisse von einem Informationssystem, auf die sie mit personalisierten Transaktionsnachrichten reagiert.

Transaktionsnachrichten können je nach Ihren Optionen per E-Mail, SMS oder [Push-Benachrichtigung](../../channels/using/transactional-push-notifications.md) gesendet werden. Prüfen Sie diesbezüglich Ihren Lizenzvertrag.

>[!NOTE]
>
>In Adobe Campaign hat die Verarbeitung von Transaktionsnachrichten Priorität vor allen anderen Sendungen.

<!--Guidelines to implement transactional messaging capabilities in your website are detailed in [this section](../../api/using/managing-transactional-messages.md).-->

<!--All transactional messages are now sent with the Adobe Campaign Enhanced MTA for improved deliverability, throughput, and bounce handling. All impacts are the same as for standard marketing messages. For more on this, see [this section](../../administration/using/configuring-email-channel.md).-->

Bevor Sie mit Transaktionsnachrichten beginnen, sollten Sie die entsprechenden [Best Practices und Einschränkungen](../../channels/using/transactional-messaging-limitations.md) lesen.

## Funktionsweise von Transaktionsnachrichten {#transactional-messaging-operating-principle}

Der gesamte Prozess der Transaktionsnachrichten kann wie folgt beschrieben werden:

![](assets/message-center-process.png)

Angenommen, Sie sind eine Firma mit einer Website, auf der Ihre Kunden Produkte kaufen können.

Mit Adobe Campaign können Sie eine Benachrichtigungs-E-Mail an Kunden senden, die Produkte zum Einkaufswagen hinzugefügt haben. Wenn einer von ihnen Ihre Website verlässt, ohne mit seinen Einkäufen fertig zu werden (externes Ereignis, das ein Ereignis der Kampagne auslöst), wird ihm automatisch eine E-Mail zum Warenkorbabbruch gesendet (Transaktionsnachricht Versand).

Die wichtigsten Schritte für die Einrichtung sind nachfolgend in [diesem Abschnitt](#key-steps) beschrieben.

## Transaktionsnachrichtentypen {#transactional-message-types}

In Adobe Campaign sind zwei Arten von Transaktionsnachrichten verfügbar.

**Ereignis-Transaktionsmessungs-** Zieldaten, die im Ereignis selbst enthalten sind. Diese Meldungen:
* Binden Sie keine Profil-Informationen ein und können Sie daher keine Abmeldung-Links einschließen.
* sind nicht mit Ermüdungsregeln vereinbar (auch nicht bei einer Anreicherung mit Profilen).
* Lassen Sie die Zielgruppe des Versands durch die im Ereignis enthaltenen Daten definiert.

Möglicherweise möchten Sie eine Ereignis-Transaktionsnachricht an einen Kunden senden, der zum Beispiel ein vergessenes Kennwort abrufen oder eine Bestellung bestätigen muss. Sie möchten nicht, dass Ihr Empfänger sich von dieser Art von Mitteilungen abmeldet, und diese Benachrichtigung sollte nicht im Rahmen einer Ermüdungsregel zum Zähler der Marketingmeldungen hinzugefügt werden.

**Profil-Transaktionsnachrichten-** Profil aus der Kampagne Marketing-Datenbank. Mit dieser Art von Nachrichten können Sie:
* Nutzen Sie die in der Adobe Campaign-Datenbank enthaltenen Daten.
* Personalisieren Sie Ihre Nachricht mit Profil-Informationen, indem Sie der Ereignis-Konfiguration eine [Anreicherung](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content) hinzufügen.
* Wenden Sie [Marketing-Typologieregeln](../../sending/using/managing-typology-rules.md) oder [Ermüdungsregeln](../../sending/using/fatigue-rules.md) an.
* einen Abmelde-Link in die Nachricht einfügen
* die Transaktionsnachrichten zur allgemeinen Versandberichterstattung hinzufügen
* die Transaktionsnachrichten für die Customer Journey nutzen

Beispielsweise können Sie diese Art von Nachrichten verwenden, wenn Sie Ihre Kunden kontaktieren, nachdem sie ihren Warenkorb auf Ihrer Website verlassen haben, um sie zu ermutigen, mit ihrem Kauf fortzufahren. Auf diese Weise können Sie Ihre Nachricht einfacher personalisieren, indem Sie direkt auf alle Informationen aus Ihrer Profil-Datenbank zugreifen, Marketingregeln anwenden und diese Nachricht auf die globale Kundenreise und den Berichte für eine bessere Ansicht Ihres Kundenverhaltens einbeziehen.

Der Nachrichtentyp wird bei der Konfiguration des Ereignisses definiert, das eine Transaktionsnachricht auslösen soll. Siehe Konfigurationsabschnitte [Ereignis-basierte Transaktionsnachrichten](../../channels/using/configuring-transactional-event.md#event-based-transactional-messages) und [Profil-basierte Transaktionsnachrichten](../../channels/using/configuring-transactional-event.md#profile-based-transactional-messages).

## Die wichtigsten Schritte {#key-steps}

Die wichtigsten Schritte beim Erstellen und Verwalten personalisierter Transaktionsnachrichten in Adobe Campaign sind im folgenden Schema zusammengefasst.

![](assets/message-center-overview.png)

Jeder dieser Schritte wird nachfolgend beschrieben.

>[!IMPORTANT]
>
>Nur Benutzer mit der Rolle [Administration](../../administration/using/users-management.md#functional-administrators) können transaktionale Ereignis konfigurieren und auf Transaktionsnachrichten zugreifen.

### Schritt 1: Ereigniskonfiguration erstellen und publizieren {#create-event-configuration}

<img src="assets/do-not-localize/icon_config.svg" width="60px">

| Benutzer | Aktion | Ergebnis |
|--- |--- |--- |
| Dieser Schritt muss von einem Administrator durchgeführt werden, der [Administratorrechte](../../administration/using/users-management.md#functional-administrators) besitzt. | Konfigurieren Sie ein Ereignis mit dem Namen „Warenkorbabbruch“ und publizieren Sie diese Ereigniskonfiguration. | Die von Ihrem Website-Entwickler verwendete API wird bereitgestellt und eine Transaktionsnachricht automatisch erstellt. |

Das Erstellen und Veröffentlichen eines Ereignisses wird in den Abschnitten [Konfigurieren eines transaktionalen Ereignisses](../../channels/using/configuring-transactional-event.md) und [Veröffentlichen eines transaktionalen Ereignisses](../../channels/using/publishing-transactional-event.md) beschrieben.

### Schritt 2: Transaktionsnachricht bearbeiten und publizieren {#create-transactional-message}

<img src="assets/do-not-localize/icon_notification.svg" width="40px">

| Benutzer | Aktion | Ergebnis |
|--- |--- |--- |
| Dieser Schritt kann von einem Marketingbenutzer durchgeführt werden, der [Administratorrechte](../../administration/using/users-management.md#functional-administrators) besitzt. | Bearbeiten und personalisieren Sie die Transaktionsnachricht, testen Sie sie und publizieren Sie sie dann. | Die Transaktionsnachricht kann dann gesendet werden. |

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

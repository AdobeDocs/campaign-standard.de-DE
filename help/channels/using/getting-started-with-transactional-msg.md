---
title: Die wichtigsten Schritte zum Einrichten einer Transaktionsnachricht
description: Erfahren Sie, was Transaktionsnachrichten sind, und lernen Sie die wichtigsten Schritte zum Einrichten einer Transaktionsnachricht in Adobe Campaign Standard kennen.
page-status-flag: never-activated
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 1b1fb4a0dc0f7881e24e10f8ac171feab2ac8cba
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 83%

---


# Erste Schritte mit Transaktionsnachrichten {#getting-started-with-transactional-messaging}

## Übersicht

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_transactional.svg" width="60px"><br><p>Einführung des Konzepts der <b>Transaktionsnachrichten</b></p></td>
<td ><br><p>Mit Transaktionsnachrichten können Sie Ihren Kunden <b>individuelle und einzigartige Nachrichten</b> in Echtzeit senden.</p></td>
<td>Das können Willkommensnachrichten, Auftragsversandbestätigungen, Kennwortänderungen usw. sein.</td>
<td>In Adobe Campaign empfängt die entsprechende Funktion Ereignisse von einem Informationssystem, auf die sie mit personalisierten Transaktionsnachrichten reagiert.</td>
</tr>
</table>

Transaktionsnachrichten können je nach Ihren Optionen per E-Mail, SMS oder Push-Benachrichtigung versendet werden. Prüfen Sie diesbezüglich Ihren Lizenzvertrag.

In Adobe Campaign hat die Verarbeitung von Transaktionsnachrichten Priorität vor allen anderen Sendungen.

Transaktionsnachrichten sind auch in der Adobe Campaign Standard API verfügbar. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../api/using/managing-transactional-messages.md).

>[!NOTE]
>
>Alle Transaktionsnachrichten werden nun mit dem erweiterten MTA von Adobe Campaign gesendet, um die Zustellbarkeit, den Durchsatz und die Bounce-Handhabung zu verbessern. Alle Auswirkungen sind dieselben wie bei standardmäßigen Marketing-Nachrichten. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../administration/using/configuring-email-channel.md).

## Definition von Transaktionsnachrichten {#transactional-messaging-definition}

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_concepts.svg" width="60px"><br><p><b>Was ist eine Transaktionsnachricht?</b></p></td>
<td><p>Es handelt sich um eine individuelle und einmalige Nachricht, die von einem Anbieter wie einer Website gesendet wird.</p></td>
<td><p>Sie wird erwartet, weil sie wichtige Informationen enthält, die der Empfänger überprüfen oder bestätigen möchte.</p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_channels.svg" width="60px"><br><p><b>Wann wird diese Nachricht gesendet?</b></p></td>
<td><p> Da diese Nachricht wichtige Informationen enthält, erwartet der Benutzer, dass sie in Echtzeit gesendet wird.</p></td>
<td><p>Folglich muss die Verzögerung zwischen der Auslösung des Ereignisses und dem Eintreffen der Nachricht sehr kurz sein.</p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_important.svg" width="60px"><br><p><b>Warum ist das wichtig?</b></p></td>
<td><p>Im Allgemeinen hat eine Transaktionsnachricht hohe Öffnungsraten. Sie sollte daher sorgfältig gestaltet werden.</p></td>
<td><p>Sie kann einen starken Einfluss auf das Verhalten der Kunden haben, da sie die Kundenbeziehung definiert.</p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_example.svg" width="60px"><br><p><b>Einige Beispiele:</b></p></td>
<td><p>Eine Transaktionsnachricht kann eine Begrüßungsnachricht nach der Kontoerstellung, eine Bestätigung nach einer Bestellung, eine Rechnung usw. sein.</p></td>
<td><p>Es kann sich auch um eine Nachricht handeln, die eine Kennwortänderung bestätigt, oder um eine Benachrichtigung, nachdem ein Kunde Ihre Website besucht hat.</p></td>
</tr>
</table>

## Transaktionsnachrichtentypen

In Adobe Campaign sind zwei Arten von Transaktionsnachrichten verfügbar:

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_event.svg" width="60px"><br><p><a href="../../channels/using/event-transactional-messages.md">Ereignis-Transaktionsnachrichten</a><br><b>, die sich auf ein Ereignis beziehen</b></p></td>
<td><p><ul><li>Ereignis-Transaktionsnachrichten enthalten keine Profil-Informationen.</li><li>Sie sind nicht mit <a href="../../sending/using/fatigue-rules.md">Ermüdungsregeln</a> kompatibel (auch nicht im Falle einer Anreicherung mit Profilen).</li><li>Die Zielgruppe des Versands wird durch die Daten definiert, die im Ereignis selbst enthalten sind.</li></ul></p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_profile.svg" width="60px"><br><p><a href="../../channels/using/profile-transactional-messages.md">Profil-Transaktionsnachrichten</a><br><b>, die sich auf Profile in der Marketing-Datenbank von Adobe Campaign beziehen</b></p></td>
<td><p>Profil-Transaktionsnachrichten ermöglichen Ihnen Folgendes:<ul><li>Wenden Sie Marketing- <a href="../../sending/using/managing-typology-rules.md">Typologieregeln</a> oder <a href="../../sending/using/fatigue-rules.md">Ermüdungsregeln</a>an.</li><li>einen Abmelde-Link in die Nachricht einfügen</li><li>die Transaktionsnachrichten zur allgemeinen Versandberichterstattung hinzufügen</li><li>Die Transaktionsnachrichten für die Customer Journey nutzen</li></ul></p></td>
</tr>
</table>

Der Nachrichtentyp wird bei der Konfiguration des Ereignisses definiert, das eine Transaktionsnachricht auslösen soll. Siehe [Transaktionsnachrichten konfigurieren](../../administration/using/configuring-transactional-messaging.md).

>[!IMPORTANT]
>
>Sie können nur dann auf alle Transaktionsnachrichten zugreifen, wenn Sie der Sicherheitsgruppe **[!UICONTROL Administratoren (alle Einheiten)]** angehören.

## Funktionsweise von Transaktionsnachrichten {#transactional-messaging-operating-principle}

Nehmen wir zur Erläuterung der Funktionsweise den Fall einer Firmen-Website, auf der Kunden Artikel kaufen können.

Verlässt ein Website-Besucher die Seite, ohne den Kauf abzuschließen, wird ihm automatisch eine Benachrichtigungs-E-Mail zugeschickt, um ihn an seinen stehen gelassenen Warenkorb zu erinnern.

Die Schritte zur Umsetzung dieser Richtlinie sind wie folgt:

### Schritt 1: Ereigniskonfiguration erstellen und publizieren {#create-event-configuration}

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_config.svg" width="60px"><br><p><b>Transactional Ereignis Configuration</b></p></td>
<td><br><p>Konfigurieren Sie ein Ereignis mit dem Namen „Warenkorbabbruch“ und publizieren Sie diese Ereigniskonfiguration.</p></td>
<td>Die von Ihrem Website-Entwickler verwendete API wird bereitgestellt und eine Transaktionsnachricht automatisch erstellt.</td>
<td>Beachten Sie, dass dieser Schritt von einem Benutzer mit <a href="../../administration/using/users-management.md#functional-administrators">Administratorrechten</a>ausgeführt werden muss.</td>
</tr>
</table>

Die Erstellung und Veröffentlichung eines Ereignisses finden Sie im Abschnitt [Ereignis konfigurieren, um eine Ereignis-Transaktionsnachricht zu senden](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message).

### Schritt 2: Transaktionsnachricht bearbeiten und publizieren {#create-transactional-message}

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_notification.svg" width="40px"><br><p><b>Transaktionsnachricht</b></p></td>
<td><br><p>Bearbeiten und personalisieren Sie die Transaktionsnachricht, testen Sie sie und publizieren Sie sie dann.</p></td>
<td>Die Transaktionsnachricht kann dann versandt werden.</td>
<td>Dieser Schritt kann von jedem Marketingbenutzer mit <a href="../../administration/using/users-management.md#basic-users">grundlegenden Zugriffsrechten</a>ausgeführt werden.
</tr>
</table>

Weitere Informationen zum Bearbeiten und Publizieren einer Transaktionsnachricht finden Sie unter [Ereignis-Transaktionsnachrichten](../../channels/using/event-transactional-messages.md).

### Schritt 3: Ereignis-Aktivierung integrieren {#integrate-event-trigger}

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_api.svg" width="55px"><br><p><b>Ereignis, das die Integration auslöst</b></p></td>
<td><br><p>Verwenden Sie die REST-Transaktionsnachrichten-API, um das Ereignis in Ihre Website zu integrieren.</p></td>
<td>Das Ereignis wird ausgelöst, wenn ein Kunde seinen Warenkorb abbricht.</td>
<td>Dieser Schritt wird vom Entwickler Ihrer Website ausgeführt.
</tr>
</table>

Weitere Informationen zur Integration des Ereignisses in Ihre Website finden Sie unter [Website-Integration](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website).

### Schritt 4: Nachrichtenversand {#message-delivery}

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_channels.svg" width="60px"><br><p><b>Externes Ereignis von Ihrer Website</b></p></td>
<td><br><p>Sobald alle diese Schritte durchgeführt wurden, kann die Nachricht gesendet werden.</p></td>
<td>Sobald ein Benutzer die Site verlässt, ohne die Produkte in seinem Einkaufswagen zu bestellen, wird das entsprechende Ereignis der Kampagne ausgelöst.</td>
<td>Der Benutzer erhält dann automatisch eine Benachrichtigungs-E-Mail.</td>
</tr>
</table>

## Die wichtigsten Schritte {#key-steps}

Die wichtigsten Schritte beim Erstellen und Verwalten personalisierter Transaktionsnachrichten in Adobe Campaign sind in der folgenden Tabelle zusammengefasst.

![](assets/message-center-overview.png)

**Verwandte Themen:**

* [Die wichtigsten Schritte im Nachrichtenversand](../../channels/using/key-steps-to-send-a-message.md)
* [Erste Schritte mit Kommunikationskanälen](../../channels/using/get-started-communication-channels.md)

<!--## Transactional messaging publication process {#transactional-messaging-pub-process}

The chart below illustrates the whole transactional messaging publication process.

![](assets/message-center_pub-process.png)

For more on the event configuration steps, see [Transactional messaging configuration](../../administration/using/configuring-transactional-messaging.md).

Read more:

* [Event transactional messages](../../channels/using/event-transactional-messages.md)
* [Profile transactional messages](../../channels/using/profile-transactional-messages.md)
* [Transactional push notifications](../../channels/using/transactional-push-notifications.md)
* [Follow-up messages](../../channels/using/follow-up-messages.md)-->
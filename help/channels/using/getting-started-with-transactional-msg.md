---
title: Wichtigste Schritte zum Einrichten einer Transaktionsnachricht
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
source-git-commit: 9927fa9402c23766049afac0f3a10d83ed08236d
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 33%

---


# Erste Schritte mit transaktionalem Messaging {#getting-started-with-transactional-messaging}

## Übersicht

<table>
<tr>
<td class="noborder"><img src="assets/do-not-localize/icon_transactional.svg" width="90px"></td>
<td class="noborder"><p>Mit Transaktionsnachrichten können Sie Ihren Kunden individuelle und eindeutige Nachrichten <b>in Echtzeit</b> senden.<br>Es kann sich um Willkommensmeldungen, Versandbestätigungen, Passwortänderung usw. handeln.</p></td>
</tr>
</table>

Mit Adobe Campaign können Sie diese Funktion in ein Informationssystem integrieren, das Ereignis sendet, die in benutzerdefinierte Transaktionsnachrichten umgewandelt werden sollen.

>[!NOTE]
>
>Transaktionsnachrichten können je nach Ihren Optionen per E-Mail, SMS oder Push-Benachrichtigung versendet werden. Prüfen Sie diesbezüglich Ihren Lizenzvertrag.
>
>Adobe Campaign priorisiert die Verarbeitung von Transaktionsnachrichten gegenüber jedem anderen Versand.

Transaktionsnachrichten sind auch in der Adobe Campaign Standard API verfügbar. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../api/using/managing-transactional-messages.md).

>[!NOTE]
>
>Alle Transaktionsnachrichten werden nun mit dem erweiterten MTA von Adobe Campaign gesendet, um die Zustellbarkeit, den Durchsatz und die Bounce-Handhabung zu verbessern. Alle Auswirkungen sind dieselben wie bei standardmäßigen Marketing-Nachrichten. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../administration/using/configuring-email-channel.md).

## Definition von Transaktionsnachrichten {#transactional-messaging-definition}

<table>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_concepts.svg" width="60px"><br><p><b>Was ist eine Transaktionsnachricht?</b></p></td>
<td><p>Es handelt sich um eine individuelle und einzigartige Kommunikation, die von einem Anbieter wie einer Website gesendet wird. Es ist besonders zu erwarten, da es wichtige Informationen enthält, die der Empfänger überprüfen oder bestätigen möchte.</p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_channels.svg" width="60px"><br><p><b>Wann ist es fällig?</b></p></td>
<td><p> Da diese Meldung wichtige Informationen enthält, erwartet der Benutzer, dass sie in Echtzeit gesendet wird. Folglich muss die Verzögerung zwischen dem ausgelösten Ereignis und der eingetretenen Meldung sehr kurz sein.</p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_important.svg" width="60px"><br><p><b>Warum ist es wichtig?</b></p></td>
<td><p>Im Allgemeinen hat eine Transaktionsnachricht hohe offene Raten. Sie sollte daher sorgfältig konzipiert werden, da sie sich stark auf das Verhalten der Kunden auswirken kann. Es definiert die Kundenbeziehung.</p></td>
</tr>
<tr>
<td align="center"><img src="assets/do-not-localize/icon_example.svg" width="60px"><br><b>Beispiel?</b></td>
<td><p>Es kann sich um eine Begrüßungsnachricht nach der Erstellung eines Kontos, eine Bestätigung, dass eine Bestellung versandt wurde, eine Rechnung, eine Nachricht zur Bestätigung einer Passwortänderung oder eine Benachrichtigung nach dem Besuch einer Website durch einen Kunden handeln...</p></td>
</tr>
</table>

## Transaktionsnachrichten

In Adobe Campaign sind zwei Arten von Transaktionsnachrichten verfügbar:

* [Ereignis-Transaktionsnachrichten](../../channels/using/event-transactional-messages.md)**, die sich auf ein Ereignis beziehen**.<!--The data contained in the event itself is used to define the delivery target.-->

   <table>
    <tr>
    <td><img src="assets/do-not-localize/icon_event.svg" width="60px"></td>
    <td><p><ul><li>Sie enthalten keine Informationen zum Profil.</li><li>Sie sind nicht mit <a href="../../sending/using/fatigue-rules.md">Ermüdungsvorschriften</a> vereinbar (auch nicht im Falle einer Anreicherung mit Profilen).</li><li>Die Zielgruppe des Versands wird durch die Daten definiert, die im Ereignis selbst enthalten sind.</li></ul></p></td>
    </tr>
    </table>

* [Profil-Transaktionsnachrichten](../../channels/using/profile-transactional-messages.md)**, die sich auf Profile in der Marketingdatenbank von Adobe Campaign beziehen**.<!--You can use information from the Adobe Campaign database to send a transactional message based on customer marketing profiles.-->

   <table>
    <tr>
    <td><img src="assets/do-not-localize/icon_profile.svg" width="60px"></td>
    <td><p>Profil-Transaktionsnachrichten ermöglichen Ihnen Folgendes:<ul><li>Marketing-Typologieregeln wie <b>Adresse auf Blockierungsliste</b> oder <a href="../../sending/using/fatigue-rules.md">Ermüdungsregeln</a> anwenden</li><li>einen Abmelde-Link in die Nachricht einfügen</li><li>die Transaktionsnachrichten zur allgemeinen Versandberichterstattung hinzufügen</li><li>Die Transaktionsnachrichten für die Customer Journey nutzen</li></ul></p></td>
    </tr>
    </table>

Der Nachrichtentyp wird bei der Konfiguration des Ereignisses definiert, das eine Transaktionsnachricht auslösen soll. Siehe [Transaktionsnachrichten konfigurieren](../../administration/using/configuring-transactional-messaging.md).

>[!IMPORTANT]
>
>To access all transactional messages, you must be part of the **[!UICONTROL Administrators (all units)]** security group.

<!--Event transactional messages do not contain profile information, therefore they are not compatible with fatigue rules (even in the case of an enrichment with profiles). However, profile transactional messages are compatible. For more on fatigue rules, see [this section](../../sending/using/fatigue-rules.md#choosing-the-channel).-->

## Funktionsweise von Transaktionsnachrichten {#transactional-messaging-operating-principle}

Nehmen wir das Beispiel einer Firma, die eine Website hat und auf dieser Website ihre Kunden Produkte kaufen können.

Verlässt ein Webseitenbesucher die Seite, ohne den Kauf abzuschließen, wird ihm automatisch eine Benachrichtigungs-E-Mail zugeschickt, um ihn an seinen stehen gelassenen Warenkorb zu erinnern.

Die folgenden Schritte sind für die Einrichtung des Systems erforderlich.

### Schritt 1: Erstellen und Veröffentlichen der Ereignis-Konfiguration {#create-event-configuration}

<table>
<tr>
<td class="noborder"><img src="assets/do-not-localize/icon_config.svg" width="60px"></td>
<td class="noborder"><p>Konfigurieren Sie ein Ereignis mit dem Namen "Warenkorbabbruch"und veröffentlichen Sie diese Ereignis-Konfiguration.</p></td>
</tr>
</table>

Die API, die von Ihrem Website-Entwickler verwendet wird, wird bereitgestellt und eine Transaktionsnachricht wird automatisch erstellt.

Die Erstellung und Veröffentlichung eines Ereignisses finden Sie im Abschnitt [Ereignis konfigurieren, um eine Ereignis-Transaktionsnachricht zu senden](../../administration/using/configuring-transactional-messaging.md#use-case--configuring-an-event-to-send-a-transactional-message).

### Schritt 2: Bearbeiten und Veröffentlichen der Transaktionsnachricht {#create-transactional-message}

<table>
<tr>
<td class="noborder"><img src="assets/do-not-localize/icon_transactional.svg" width="60px"></td>
<td class="noborder"><p>Bearbeiten und personalisieren Sie die Transaktionsnachricht, testen Sie sie und veröffentlichen Sie sie dann.</p></td>
</tr>
</table>

For more on editing and publishing a transactional message, see [Event transactional messages](../../channels/using/event-transactional-messages.md).

### Schritt 3: Integration des auslösenden Ereignisses {#integrate-event-trigger}

<table>
<tr>
<td class="noborder"><img src="assets/do-not-localize/icon_api.svg" width="60px"></td>
<td class="noborder"><p>Verwenden Sie die REST-Transaktionsnachrichten-API, um das Ereignis in Ihre Website zu integrieren.</p></td>
</tr>
</table>

Das Ereignis wird ausgelöst, wenn ein Kunde seinen Warenkorb verlässt.

Weitere Informationen zur Integration des Ereignisses in Ihre Website finden Sie unter [Site-Integration](../../administration/using/configuring-transactional-messaging.md#integrating-the-triggering-of-the-event-in-a-website).

### Schritt 4: Message Versand {#message-delivery}

<!--Once all of these steps have been carried out, the message can be delivered:-->

<table>
<tr>
<td class="noborder"><img src="assets/do-not-localize/icon_notification.svg" width="60px"></td>
<td class="noborder"><p><br>Sobald ein Benutzer die Site verlässt, ohne die Produkte in seinem Einkaufswagen zu bestellen, erhält er automatisch eine Benachrichtigungs-E-Mail.</p></td>
</tr>
</table>

## Die wichtigsten Schritte {#key-steps}

Die wichtigsten Schritte beim Erstellen und Verwalten personalisierter Transaktionsnachrichten in Adobe Campaign sind in der folgenden Tabelle zusammengefasst.

![](assets/message-center-overview.png)

<!--## Transactional messaging publication process {#transactional-messaging-pub-process}

The chart below illustrates the whole transactional messaging publication process.

![](assets/message-center_pub-process.png)

For more on the event configuration steps, see [Transactional messaging configuration](../../administration/using/configuring-transactional-messaging.md).

Read more:

* [About transactional messaging](../../channels/using/about-transactional-messaging.md)
* [Event transactional messages](../../channels/using/event-transactional-messages.md)
* [Profile transactional messages](../../channels/using/profile-transactional-messages.md)
* [Transactional push notifications](../../channels/using/transactional-push-notifications.md)
* [Follow-up messages](../../channels/using/follow-up-messages.md)-->

**Verwandte Themen:**

* [Die wichtigsten Schritte im Nachrichtenversand](../../channels/using/key-steps-to-send-a-message.md)
* [Erste Schritte mit Kommunikationskanälen](../../channels/using/get-started-communication-channels.md)
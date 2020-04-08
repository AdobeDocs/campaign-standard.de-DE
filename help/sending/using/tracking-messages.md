---
title: Nachrichten tracken
description: Hier erfahren Sie, wie Sie das Verhalten von Versandempfängern tracken können.
page-status-flag: never-activated
uuid: c3721647-0663-4614-a9c9-3b3a40af328a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sending-and-tracking-messages
discoiquuid: 6fa50f0d-3dcf-4a9e-bccc-1ecda2bfb449
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 50aeb40d891f6a089a556ef25eba87e568a88e94

---


# Nachrichten tracken{#tracking-messages}

## Über das Tracking {#about-tracking}

Dank der Tracking-Funktionen ermöglicht Adobe Campaign die Verfolgung des Verhaltens von Versandempfängern. Dabei kommen mit Adobe Campaign Sitzungs-Cookies und permanente Cookies zum Einsatz.

Eine Möglichkeit besteht darin, Besucher von Webtracking betroffenen Seiten zur Zustimmung aufzufordern, indem im oberen Bereich auf der ersten besuchten Seite ein Banner eingeblendet und zum Ankreuzen eines Feldes aufgefordert wird. Vermeiden Sie jedoch Pop-ups, da diese häufig von den Browsern blockiert werden.

Tracking information are available for each contact of your database into **[!UICONTROL integrated customer profiles]**. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../audiences/using/integrated-customer-profile.md).

Adobe Campaign verwendet zwei Arten von Cookies:

* Sitzungs-Cookie (nlid). Er enthält die Kennung der an den Kontakt gesendeten E-Mail (broadlogId) und die Kennung der Nachrichtenvorlage (deliveryId). Er wird gesetzt, sobald der Kontakt eine in einer mit Adobe Campaign gesendeten E-Mail enthaltene URL anklickt, und ermöglicht, das Webverhalten des Kontakts zu verfolgen. Dieser Sitzungs-Cookie wird automatisch mit Schließen des Browsers gelöscht. Der Kontakt hat die Möglichkeit, das Setzen des Cookies zu verbieten, indem er seine Browser-Einstellungen dementsprechend ändert.
* Von verschiedenen Lösungen in Adobe Experience Cloud gemeinsam genutzter Cookie. Er ermöglicht die Identifizierung eines Internetbenutzers, der mit Lösungen der Experience Cloud bei Webseitenbesuchen interagiert. Weiterführende Informationen zu diesem Cookie finden Sie hier: [https://marketing.adobe.com/resources/help/de_DE/whitepapers/cookies/cookies_mc.html](https://marketing.adobe.com/resources/help/de_DE/whitepapers/cookies/cookies_mc.html).

Die Verfolgung mit dem Adobe Campaign Standard ermöglicht Ihnen den Zugriff auf die folgenden Funktionen:

<table>
<tr>
    <td valign="top">
        <a href="../../administration/using/configuring-email-channel.md#tracking-parameters"><img width="60px" alt="Bedingungen" src="assets/icon_email_parameters.png"/></a>
    </td>
    <td valign="top">
        <a href="https://helpx.adobe.com/de/campaign/kb/push-tracking.html"><img width="60px" alt="Bedingungen" src="assets/icon_push_parameters.png"/></a>
    </td>
    <td valign="top">
        <a href="../../designing/using/links.md#about-tracked-urls"><img width="60px" alt="Bedingungen" src="assets/icon_url.png"/></a>
    </td>
        <td valign="top">
          <a href="../../sending/using/tracking-messages.md#tracking-logs"><img width="60px" alt="Bedingungen" src="assets/icon_log.png"/></a>
    </td>
    </td>
    <td valign="top">
          <a href="../../reporting/using/tracking-indicators.md"><img width="60px" alt="Bedingungen" src="assets/icon_report.png"/></a>
</tr>
<tr>
<td>E-Mail-Tracking</td>
<td>Push-Verfolgung</td>
<td>Tracked URLs</td>
<td>Trackinglogs </td>
<td>Verfolgungsbericht</td>
</tr>
</table>

## Trackinglogs  {#tracking-logs}

The **[!UICONTROL Tracking logs]** tab lists the tracking history for this delivery. Angezeigt werden die zu allen gesendeten Nachrichten für die jeweils getrackten URLs gesammelten Informationen. Die Trackinginformationen in diesem Tab werden alle 10 Minuten aktualisiert.

>[!NOTE]
>
>Sollte das Tracking für einen Versand nicht aktiviert worden sein, wird dieser Tab nicht angezeigt. Trackinglogs sind nur für die Kanäle **E-Mail** und **Push-Benachrichtigung** verfügbar.

![](assets/tracking_logs.png)

Im obigen Beispiel hat sich der Empfänger folgendermaßen verhalten:

* Er hat die Nachricht geöffnet.
* Er hat auf den benutzerspezifischen Link &quot;MEHR DAZU&quot; geklickt.
* Er hat auf den Abmelde- und Mirrorseiten-Link geklickt.

In the **[!UICONTROL Type]** column, the possible values are:

* **[!UICONTROL Email click]**: die Empfänger, die auf einen benutzerspezifischen Link geklickt haben.
* **[!UICONTROL Mirror page]**: der Empfänger auf einen Link zur Mirrorseite geklickt hat.
* **[!UICONTROL Open]**: der Empfänger die E-Mail geöffnet hat.
* **[!UICONTROL Opt-out]**: Der Empfänger hat auf einen Abmelde-Link geklickt.

>[!NOTE]
>
>Für den Kanal **Push-Benachrichtigung** werden nur Klicks auf Mobile-App-Benachrichtigungen getrackt. In diesem Fall wird der Wert **[!UICONTROL Click on mobile notification]** verwendet.

Weiterführende Informationen zum Einfügen von Tracking-Links finden Sie auf [dieser Seite](../../designing/using/links.md#inserting-a-link).

## Getrackte URLs {#tracked-urls}

The **[!UICONTROL Tracked URLs]** tab regroups the URLs contained in the sent message, including their URL type and their source URL.

![](assets/sending_delivery6.png)

Weiterführende Informationen zu Tracking-Links finden Sie in [diesem Abschnitt](../../designing/using/links.md#about-tracked-urls).

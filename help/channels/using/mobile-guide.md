---
title: Handbuch zu Campaign Standard Mobile
description: Erfahren Sie mehr über die allgemeinen Richtlinien für mobile Sendungen in Adobe Campaign Standard, z. B. wie Sie Ihre Mobile Apps konfigurieren oder Push-Benachrichtigungen und In-App-Nachrichten erstellen.
audience: channels
content-type: reference
topic-tags: mobile-guide
feature: Overview
role: User
level: Beginner
exl-id: d4e1b935-b21f-4a24-99ba-f455db0f7cfc
source-git-commit: 7767b39a48502f97e2b3af9d21a3f49b9283ab2e
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 100%

---

# Erste Schritte mit mobilen Kanälen {#mobile-guide}

<table style="table-layout:fixed">
<tr>
<td><img src="assets/do-not-localize/config_push.png" width="60px"><p>Erfahren Sie, wie Sie Ihre Mobile App für Push-Benachrichtigungen konfigurieren </br><a href="#configuration-push">Hier klicken</a></p></td>
<td><img src="assets/do-not-localize/config_inapp.png" width="60px"><p>Erfahren Sie, wie Sie Ihre Mobile App für In-App-Nachrichten konfigurieren </br><a href="#configuring-mobile-app">Hier klicken</a></p></td>
</tr>
<tr>
<td><img src="assets/do-not-localize/push2.png" width="60px"><p>Erfahren Sie mehr über das Erstellen von Push-Benachrichtigungen </br><a href="#create-push">Hier klicken</a></p></td>
<td><img src="assets/do-not-localize/inapp.png" width="60px"><p>Erfahren Sie, wie Sie In-App-Nachrichten erstellen</br><a href="#create-inapp">Hier klicken</a></p></td></tr>
</table>

## Über den Versand an Mobilgeräte {#about-mobile}

Mit Adobe Campaign können Sie personalisierte Nachrichten auf verschiedenen Kanälen erstellen und versenden, den Kampagnenerfolg messen und die Ergebnisse in Berichten detailliert darstellen.

Mit Adobe Campaign Standard können Sie Sendungen an Mobilgeräte über drei verschiedene Kanäle durchführen:

* SMS, siehe Abschnitt &quot;Über SMS-Nachrichten&quot;.
* Push-Benachrichtigungen, siehe Abschnitt &quot;Über Push-Benachrichtigungen&quot;.
* In-App-Nachrichten, siehe Abschnitt &quot;Über In-App-Nachrichten&quot;.

## Mobile App für Push-Benachrichtigungen konfigurieren {#configuration-push}

<table style="table-layout:fixed">
<tr>
  <td>
    <div>
    <p><strong>Konfiguration einer Mobile App mithilfe von Adobe Experience Platform SDKs</strong></p>
    </div>
    <p>Zum Versand von In-App-Nachrichten und Push-Benachrichtigungen müssen Ihre Mobile Apps in Adobe Campaign unter Verwendung von Adobe Experience Platform SDKs eingerichtet werden.</br><a href="../../administration/using/configuring-a-mobile-application.md"><strong>Klicken Sie hier</strong></a>, um weitere Informationen zu erhalten.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>Die Struktur der Payload von Push-Benachrichtigungen in Campaign Standard</strong></p>
    </div>
    <p>Erfahren Sie mehr über die Struktur der Payload, die in Mobile Apps empfangen wird, wenn Adobe Campaign Standard erfolgreich eine Push-Benachrichtigung an diese App sendet.</br><a href="../../administration/using/push-payload.md"><strong>Klicken Sie hier</strong></a>, um weitere Informationen zu erhalten.</p>
    <br>
  </td>
</tr>
<tr>
  <td>
    <div>
    <p><strong>Lokales Benachrichtigungs-Tracking implementieren</strong></p>
    </div>
    <p>Hier erfahren Sie, wie Sie sicherstellen können, dass das lokale Benachrichtigungs-Tracking korrekt implementiert wurde. </br><a href="../../administration/using/local-tracking.md"><strong>Klicken Sie hier</strong></a>, um weitere Informationen zu erhalten.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>Implementieren von Push-Tracking</strong></p>
    </div>
    <p>Erfahren Sie, wie Sie sicherstellen können, dass das Tracking von Push-Benachrichtigungen unter iOS und Android richtig implementiert wurde.</br><a href="../../administration/using/push-tracking.md"><strong>Klicken Sie hier</strong></a>, um weitere Informationen zu erhalten.</p>
    <br>
  </td>
</tr>
</table>

## Mobile App für In-App-Nachrichten konfigurieren {#configuring-mobile-app}

<table style="table-layout:fixed">
<tr>
  <td>
    <div>
    <p><strong>Konfiguration einer Mobile App mithilfe von Adobe Experience Platform SDKs</strong></p>
    </div>
    <p>Zum Versand von In-App-Nachrichten und Push-Benachrichtigungen müssen Ihre Mobile Apps in Adobe Campaign unter Verwendung von Adobe Experience Platform SDKs eingerichtet werden.</br><a href="../../administration/using/configuring-a-mobile-application.md"><strong>Klicken Sie hier</strong></a>, um weitere Informationen zu erhalten.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>Unterstützte Anwendungsfälle für Mobilgeräte unter Verwendung von Adobe Experience Platform SDKs</strong></p>
    </div>
    <p>Anwendungsfälle für Mobilgeräte, die in Adobe Campaign Standard durch die Verwendung von Adobe Experience Platform SDKs unterstützt werden.</br><a href="../../administration/using/supported-mobile-use-cases.md"><strong>Klicken Sie hier</strong></a>, um weitere Informationen zu erhalten.</p>
    <br>
  </td>
</tr>
<tr>
  <td>
    <div>
    <p><strong>Konfigurieren von Tag-Regeln zur Unterstützung von Adobe Campaign Standard-Anwendungsfällen</strong></p>
    </div>
    <p><a href="../../administration/using/configuring-rules-launch.md"><strong>Klicken Sie hier</strong></a>, um mit der Erstellung von Datenelementen und Regeln in der Datenerfassungs-UI zu beginnen und personenbezogene Daten sowie andere Daten von Mobile Apps an Adobe Campaign Standard zu senden.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>Lokales Benachrichtigungs-Tracking implementieren</strong></p>
    </div>
    <p>Hier erfahren Sie, wie Sie sicherstellen können, dass das lokale Benachrichtigungs-Tracking korrekt implementiert wurde. </br><a href="../../administration/using/local-tracking.md"><strong>Klicken Sie hier</strong></a>, um weitere Informationen zu erhalten.</p>
    <br>
  </td>
</tr>
</table>

## Push-Benachrichtigung erstellen {#create-push}

<table style="table-layout:fixed">
<tr>
  <td>
    <div>
    <p><strong>Push-Benachrichtigung vorbereiten und senden</strong></p>
    </div>
    <p><a href="../../channels/using/preparing-and-sending-a-push-notification.md"><strong>Hier erfahren Sie</strong></a>, wie Sie Ihre Push-Benachrichtigung vorbereiten und dann an Ihre Zielgruppe senden.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>Push-Benachrichtigung anpassen</strong></p>
    </div>
    <p>In Adobe Campaign stehen Ihnen zur Anpassung von Sendungen bei der Erstellung von Push-Benachrichtigungen eine Reihe von Optionen zur Verfügung.</br><a href="../../channels/using/customizing-a-push-notification.md"><strong>Klicken Sie hier</strong></a>, um weitere Informationen zu erhalten.</p>
    <br>
  </td>
</tr>
<tr>
  <td>
    <div>
    <p><strong>Mehrsprachige Push-Benachrichtigungen erstellen</strong></p>
    </div>
    <p>Personalisieren Sie den Inhalt Ihrer Push-Benachrichtigung, indem Sie Nachrichten senden, die in der bevorzugten Sprache des Empfängers verfasst sind und auf der jeweiligen Region basieren.</br><a href="../../channels/using/creating-a-multilingual-push-notification.md"><strong>Klicken Sie hier</strong></a>, um weitere Informationen zu erhalten.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>Bild aus einer Push-Benachrichtigung von Adobe Campaign Standard anzeigen</strong></p>
    </div>
    <p><a href="../../administration/using/image-push-notification.md"><strong>Hier erfahren Sie, wie Sie ein Bild aus einer Adobe Campaign-Push-Benachrichtigung auf einem iOS-Gerät anzeigen.</strong></a></p>
    <br>
  </td>
</tr>
</table>

## In-App-Nachricht erstellen {#create-inapp}

<table style="table-layout:fixed">
<tr>
  <td>
    <div>
    <p><strong>In-App-Nachricht vorbereiten und senden</strong></p>
    </div>
    <p><a href="../../channels/using/preparing-and-sending-an-in-app-message.md"><strong>Hier erfahren Sie</strong></a>, wie Sie Ihre In-App-Nachrichten vorbereiten und an Ihre Zielgruppe senden können.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>In-App-Nachrichten anpassen</strong></p>
    </div>
    <p>In Adobe Campaign stehen Ihnen zur Anpassung von Sendungen bei der Erstellung von In-App-Nachrichten eine Reihe erweiterter Optionen zur Verfügung.</br><a href="../../channels/using/customizing-an-in-app-message.md"><strong>Klicken Sie hier</strong></a>, um weitere Informationen zu erhalten.</p>
    <br>
  </td>
</tr>
<tr>
  <td>
    <div>
    <p><strong>Nachricht vom Typ "Lokale Benachrichtigung" anpassen</strong></p>
    </div>
    <p>Lokale Benachrichtigungen können nur von einer App zu einer bestimmten Zeit und abhängig von einem Ereignis ausgelöst werden. </br><a href="../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type"><strong>Klicken Sie hier</strong></a>, um weitere Informationen zu erhalten.</p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>In-App-Bericht</strong></p>
    </div>
    <p>Der In-App-Bericht liefert Details zu In-App-Sendungen.</br><a href="../../reporting/using/in-app-report.md"><strong>Klicken Sie hier</strong></a>, um weitere Informationen zu erhalten.</p>
    <br>
  </td>
</tr>
</table>

## SMS-Nachrichten erstellen {#create-sms}

<table style="table-layout:fixed">
<tr>
  <td>
    <div>
    <p><strong>SMS erstellen</strong></p>
    </div>
    <p>Die Erstellung eines SMS-Versands ist der Erstellung einer üblichen E-Mail sehr ähnlich. </br>Die hier <a href="../../channels/using/creating-an-sms-message.md"><strong>beschriebenen Schritte</strong></a> beschreiben die Konfiguration, die speziell für diesen Kanal nötig ist.</br></p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>SMS-Nachrichten anpassen
</strong></p>
    </div>
    <p>In Adobe Campaign stehen Ihnen zur Anpassung von Sendungen bei der Erstellung von SMS-Nachrichten eine Reihe erweiterter Optionen zur Verfügung.</br><a href="../../channels/using/sms-and-push-content-editor-interface.md"><strong>Klicken Sie hier, um weitere Informationen zu erhalten.</br><a href="../../channels/using/sms-and-push-content-editor-interface.md"><strong></p>
    <br>
  </td>
</tr>
<tr>
  <td>
    <div>
    <p><strong>Eingehende SMS verwalten</strong></p>
    </div>
    <p>Wenn ein Profil auf eine per Campaign gesendete SMS-Nachricht antwortet, können Sie die automatisch an das Profil zu sendenden Nachrichten sowie die auszuführende Aktion konfigurieren. Anpassen eines Nachrichtentyps für lokale Benachrichtigungen</br><a href="../../channels/using/managing-incoming-sms.md"><strong>Klicken Sie hier, um weitere Informationen zu erhalten.</br><a href="../../channels/using/managing-incoming-sms.md"><strong></p>
    <br>
  </td>
  <td>
    <div>
    <p><strong>SMS-Bericht</strong></p>
    </div>
    <p>Der SMS-Bericht bietet Informationen zu SMS-Sendungen, wie die Anzahl der zugestellten Nachrichten und die Bounces.</br><a href="../../reporting/using/sms-report.md"><strong>Klicken Sie hier</strong></a>, um weitere Informationen zu erhalten.</p>
    <br>
  </td>
</tr>
</table>

## Fehlerbehebung bei Sendungen an Mobilgeräte {#mobile-troubleshooting}

Die folgenden Seiten helfen Ihnen, die häufigsten Probleme zu lösen, die beim Versand an Mobilgeräte in Adobe Campaign Classic auftreten.

<table style="table-layout:fixed">
<tr>
  <td>
    <div>
    <p><strong>Häufig gestellte Fragen zu Push-Benachrichtigungen</strong></p>
    </div>
    <p><a href="../../channels/using/about-push-notifications.md#push-faq"><strong>Klicken Sie hier, um weitere Informationen zu erhalten.</p>
  </td>
  <td>
    <div>
    <p><strong>Häufig gestellte Fragen zur Synchronisation von Adobe Launch</strong></p>
    </div>
    <p><a href="../../channels/using/in-app-faq.md"><strong>Klicken Sie hier, um weitere Informationen zu erhalten.</p>
  </td>
  <td>
    <div>
    <p><strong>Häufig gestellte Fragen zu In-App-Nachrichten</strong></p>
    </div>
    <p><a href="../../administration/using/syncwithlaunch-faq.md"><strong>Klicken Sie hier, um weitere Informationen zu erhalten.</p>
  </td>
</tr>
</table>

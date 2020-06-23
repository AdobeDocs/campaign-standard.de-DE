---
title: Erste Schritte mit Tests und Senden
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
source-git-commit: 2df909256b910e5e26e0fdac7e150edd0603c8ab
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 26%

---


# Erste Schritte mit Tests und Senden {#about-sending-messages-with-campaign}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_prepare.svg" width="60px"><p><a href="#prepare-test-send">Vorbereitung und Test</a></p></td>
<td><img src="assets/do-not-localize/icon_send.svg" width="60px"><p><a href="#send-track-messages">Senden, überwachen und verfolgen</a></p></td>
<td><img src="assets/do-not-localize/icon_deliverability.svg" width="60px"><p><a href="#improve-deliverability">Richtlinien zur Lieferbarkeit</a></p></td></tr>
</table>

Nachdem Sie die Zielgruppe definiert und den Inhalt einer Nachricht erstellt haben, müssen Sie den Inhalt, die Personalisierung, das Rendering und die Konfiguration Ihrer Versand vorbereiten und testen. Auf diese Weise können Sie sicherstellen, dass alles korrekt ist, bevor Sie die Nachricht an die Haupt-Zielgruppe senden. Dazu stehen mehrere Funktionen zur Verfügung, wie z. B. Vorschau, Testversand, E-Mail-Betreffzeilentests oder E-Mail-Rendering.

Nachdem die Marketing-Kampagnen ausgeführt und die verschiedenen Nachrichten gesendet wurden, überwachen Sie sie mithilfe von Protokollen, um den Erfolg Ihrer Kampagne zu überprüfen und Rückverfolgungsinformationen über die Empfänger abzurufen.

Nutzen Sie schließlich die im Campaign Standard verfügbaren Richtlinien und Tools zur Bereitstellung, um die Anzahl der ausgelieferten Nachrichten zu erhöhen und erfolgreiche Marketing-Kampagnen sicherzustellen.

## Vorbereitung und Test {#prepare-test-send}

<img src="assets/do-not-localize/icon_prepare.svg" width="60px">

Campaign Standard **message preparation** analyzes the target, the personalization and the validity of the message. Fehler, die bei diesem Schritt erkannt werden, müssen vor dem weiteren Vorgehen korrigiert werden.

**Vorschau und Testen** Ihrer Nachrichten mit verschiedenen Funktionen: Senden Sie Testversand, um Profil oder zielgerichtete Profil zu testen, die Betreffzeile Ihrer E-Mails zu testen und die Wiedergabe Ihrer Nachrichten zu überprüfen, um sicherzustellen, dass sie auf verschiedenen Web-Clients, Web-Mails und Geräten optimal angezeigt werden.

Nutzen Sie Planungsfunktionen für Kampagnen, um zu definieren, wann Ihre Nachrichten gesendet werden. Sie können beispielsweise den Versand an die Zeitzone des Empfängers anpassen, die Sendezeit optimieren oder das Versanddatum berechnen.

Verwenden Sie **Typologien** , um während der Vorbereitung zu überprüfen, ob Ihre Nachricht gültig ist und Ihre Qualitätskriterien durch Ermüdungs-, Kontroll- und Targeting-Regeln erfüllt. So können Sie beispielsweise überprüfen, ob Ihre E-Mails immer eine Betreffzeile enthalten, oder Abonnenten von den Empfängern der Nachricht ausschließen.

mehr dazu:

* [Versandvorbereitung](../../sending/using/preparing-the-send.md)
* [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md)
* [Testversand durchführen](../../sending/using/sending-proofs.md)
* [E-Mail-Rendering](../../sending/using/email-rendering.md)
* [Versandplanung](../../sending/using/about-scheduling-messages.md)
* [Über Typologien und Typologieregeln](../../sending/using/about-typology-rules.md)

## Senden, überwachen und verfolgen {#send-track-messages}

<img src="assets/do-not-localize/icon_send.svg"  width="60px">

Sobald Ihre Nachricht fertig ist, können Sie die Senden- und Zugriffsprotokolle und Berichte bestätigen, um den Versand **zu** überwachen und den Erfolg Ihrer Kampagne zu messen. Adobe Campaign bietet außerdem ein E-Mail-Warnsystem, um Erfolge oder Fehler von Versänden sowie Quarantänen-Management-Funktionen zu verfolgen.

**Verfolgen Sie das Verhalten** der Empfänger der Nachricht mithilfe von Sitzungs- und dauerhaften Cookies, um Verfolgungsinformationen abzurufen (angeklickte URLs, Mirrorseiten, geöffnete Nachrichten...).

Finally, you can configure Adobe Campaign to **keep a copy of emails** sent from your platform through Email BCC. Wenn Ihr Unternehmen aus Compliance-Gründen alle ausgehenden E-Mail-Nachrichten archivieren muss, können Sie diese Funktion aktivieren.

mehr dazu:

* [Versand bestätigen](../../sending/using/confirming-the-send.md)
* [Nachrichten tracken](../../sending/using/tracking-messages.md)
* [Mit E-Mail-BCC archivieren](../../sending/using/archiving.md)
* [Sendungen beobachten](../../sending/using/monitoring-a-delivery.md)
* [Ursachen von fehlgeschlagenen Sendungen](../../sending/using/understanding-delivery-failures.md)
* [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md)

## Richtlinien zur Lieferbarkeit {#improve-deliverability}

<img src="assets/do-not-localize/icon_deliverability.svg"  width="60px">

Die Zustellbarkeit misst, wie viele Ihrer Nachrichten erfolgreich an die Empfängerpostfächer zugestellt und nicht als unzustellbar zurückgesendet bzw. als Spam gekennzeichnet werden.

Campaign Standard bietet mehrere **Bereitstellungs-Tools** , mit denen Sie die Anzahl der erfolgreich ausgelieferten Nachrichten verbessern können: Versand-Berichte, Optimierung der Sendezeit, Vorschau von Nachrichten, E-Mail-Rendering, Verwaltung von Quarantänen usw.

mehr dazu:

* [Über die Zustellbarkeit](../../sending/using/about-deliverability.md)
* [Überwachen der Zustellbarkeit](../../sending/using/monitor-deliverability.md)
* [Verbessern Ihres Rufs](../../sending/using/improving-reputation.md)
* [Technische Empfehlungen](../../sending/using/technical-recommendations.md)
* [Versanddurchsatz kontrollieren](../../reporting/using/delivery-throughput.md)

## Zusätzliche Ressourcen

* [E-Mails für A/B-Test entwerfen](../../channels/using/designing-an-a-b-test-email.md)
* [Senden eines Tests, Vorbereiten und Senden einer E-Mail (Video)](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/sending-test-preparing-sending-email.html)
* [Überprüfen eines E-Mail-Versands und von Berichten (Video)](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/reviewing-personalized-email-delivery-and-reports.html)
* [Erste Schritte mit E-Mails](https://helpx.adobe.com/de/campaign/kb/acs-get-started-with-emails.html)
* [Best Practices beim Versand](https://helpx.adobe.com/de/campaign/kb/delivery-best-practices.html)
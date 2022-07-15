---
title: Erste Schritte mit Testen und Senden
description: Bereiten Sie Ihre Nachrichten vor und testen, planen, versenden und überwachen Sie sie.
audience: sending
content-type: reference
topic-tags: about-sending-messages-with-campaign
role: User
level: Intermediate
exl-id: bcb28ef5-5cad-43c1-b11b-080abc791a72
source-git-commit: 013293fce8a923e771e10585c41e4ad482003080
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 100%

---

# Erste Schritte mit Testen und Senden {#about-sending-messages-with-campaign}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_prepare.svg" width="60px"><p><a href="#prepare-test-send">Vorbereiten und Testen</a></p></td>
<td><img src="assets/do-not-localize/icon_send.svg" width="60px"><p><a href="#send-track-messages">Senden, Überwachen und Tracking</a></p></td>
<td><img src="assets/do-not-localize/icon_deliverability.svg" width="60px"><p><a href="#improve-deliverability">Zustellbarkeitsrichtlinien</a></p></td></tr>
</table>

Nachdem Sie die Zielgruppe definiert und den Inhalt einer Nachricht erstellt haben, müssen Sie den Inhalt, die Personalisierung, das Rendering und die Konfiguration Ihrer Sendungen vorbereiten und testen. Auf diese Weise können Sie sicherstellen, dass alles korrekt ist, bevor Sie die Nachricht an die Hauptzielgruppe senden. Dazu stehen mehrere Funktionen zur Verfügung, wie z. B. Vorschau, Testversand, Testen der E-Mail-Betreffzeilen oder E-Mail-Rendering.

Sobald die Marketing-Kampagnen ausgeführt und die verschiedenen Nachrichten gesendet wurden, können Sie diese mithilfe von Protokollen überwachen, um den Erfolg Ihrer Kampagne zu überprüfen und Tracking-Informationen zu den Empfängern abzurufen.

Nutzen Sie schließlich die in Campaign Standard verfügbaren Zustellbarkeitsrichtlinien und Tools, um die Anzahl der zugestellten Nachrichten zu erhöhen und den Erfolg Ihrer Marketing-Kampagnen sicherzustellen.

![](assets/do-not-localize/how-to-video.png) [Erfahren Sie im Video, wie man eine Test-E-Mail sendet und einen E-Mail-Versand vorbereitet und ausführt.](#video)

## Vorbereiten und Testen {#prepare-test-send}

<img src="assets/do-not-localize/icon_prepare.svg" width="60px">

Bei der **Nachrichtenvorbereitung** in Campaign Standard wird die Zielgruppe, die Personalisierung und die Gültigkeit der Nachricht analysiert. Fehler, die bei diesem Schritt erkannt werden, müssen vor dem weiteren Vorgehen korrigiert werden.

**Zeigen Sie Ihre Nachrichten in einer Vorschau an und testen** Sie sie mit verschiedenen Funktionen: Senden Sie Testsendungen an Testprofile oder Zielgruppenprofile, testen Sie den Betreff Ihrer E-Mails und überprüfen Sie das Rendering Ihrer Nachrichten, um sicherzustellen, dass sie über eine Vielzahl von Web-Clients, Web-Mails und Geräten optimal angezeigt werden.

Nutzen Sie Planungsfunktionen in Campaign, um festzulegen, wann Ihre Nachrichten gesendet werden. Sie können beispielsweise den Versand an die Zeitzone des Empfängers anpassen, die Sendezeit optimieren oder das Versanddatum berechnen.

Verwenden Sie **Typologien**, um während der Vorbereitung zu überprüfen, ob Ihre Nachricht gültig ist und sie Ihre Qualitätskriterien durch Ermüdungs-, Kontroll- und Zielgruppenbestimmungsregeln erfüllt. So können Sie beispielsweise überprüfen, ob Ihre E-Mails immer einen Betreff enthalten, oder abgemeldete Profile von den Empfängern der Nachricht ausschließen.

Mehr dazu:

* [Versandvorbereitung](../../sending/using/preparing-the-send.md)
* [Vorschau der Nachricht erzeugen](../../sending/using/previewing-messages.md)
* [Testversand durchführen](../../sending/using/sending-proofs.md)
* [E-Mail-Rendering](../../sending/using/email-rendering.md)
* [Versandplanung](../../sending/using/about-scheduling-messages.md)
* [Über Typologien und Typologieregeln](../../sending/using/about-typology-rules.md)

## Senden, Überwachen und Tracking {#send-track-messages}

<img src="assets/do-not-localize/icon_send.svg"  width="60px">

Sobald Ihre Nachricht fertig ist, können Sie den Versand bestätigen und auf Protokolle und Berichte zugreifen, um den **Versand** zu überwachen und den Erfolg Ihrer Kampagne zu messen. Adobe Campaign bietet außerdem ein E-Mail-Benachrichtigungssystem zur Tracking von Erfolgen oder Fehlschlägen beim Versand sowie Funktionen zur Quarantäneverwaltung.

**Tracken Sie das Verhalten** der Nachrichtenempfänger, indem Sie Sitzungs- und permanente Cookies verwenden, um Tracking-Informationen abzurufen (angeklickte URLs, Mirrorseiten, geöffnete Nachrichten usw.).

Außerdem können Sie Adobe Campaign so konfigurieren, dass von E­Mails, die von der Plattform per E-Mail-BCC gesendet werden, **eine Kopie beibehalten** wird. Insbesondere wenn Ihr Unternehmen aus Compliance-Gründen alle ausgehenden E-Mail-Nachrichten archivieren muss, können Sie diese Funktion aktivieren.

Mehr dazu:

* [Versand bestätigen](../../sending/using/confirming-the-send.md)
* [Nachrichten tracken](../../sending/using/tracking-messages.md)
* [Archivieren mit E-Mail-BCC](../../sending/using/archiving.md)
* [Sendungen überwachen](../../sending/using/monitoring-a-delivery.md)
* [Ursachen von fehlgeschlagenen Sendungen](../../sending/using/understanding-delivery-failures.md)
* [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md)

## Zustellbarkeitsrichtlinien {#improve-deliverability}

<img src="assets/do-not-localize/icon_deliverability.svg"  width="60px">

Die Zustellbarkeit misst, wie viele Ihrer Nachrichten erfolgreich an die Empfängerpostfächer zugestellt und nicht als unzustellbar zurückgesendet bzw. als Spam gekennzeichnet werden.

Campaign Standard bietet verschiedene **Zustellbarkeits-Tools**, mit denen Sie die Anzahl der erfolgreich zugestellten Nachrichten verbessern können: Berichte zum Versanddurchsatz, Optimierung des Sendezeitpunkts, Vorschau von Nachrichten, E-Mail-Rendering, Quarantäneverwaltung usw.

Mehr dazu:

* [Über die Zustellbarkeit](../../sending/using/about-deliverability.md)
* [Überwachen der Zustellbarkeit](../../sending/using/monitor-deliverability.md)
* [Adobe-Handbuch mit den Best Practices zur Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=de)
* [Steuern des Versanddurchsatzes](../../reporting/using/delivery-throughput.md)

## Zusätzliche Ressourcen

* [E-Mails für A/B-Test entwerfen](../../channels/using/designing-an-a-b-test-email.md)
* [Erste Schritte mit Nachrichten](../../channels/using/key-steps-to-send-a-message.md)
* [Best Practices beim Versand](../../sending/using/delivery-best-practices.md)
* [Hinzufügen einer Kontrollgruppe](../../sending/using/control-group.md)

## Anleitungsvideo {#video}

In diesem Video wird gezeigt, wie man eine Test-E-Mail sendet, einen E-Mail-Versand vorbereitet und dann in Campaign Standard ausführt.

>[!VIDEO](https://video.tv.adobe.com/v/24013/)

Weitere Anleitungsvideos zu Campaign Standard finden Sie [hier](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/overview.html?lang=de).

---
title: Monitoring der Zustellbarkeit in Adobe Campaign Standard
description: Verwenden Sie die von Adobe Campaign Standard bereitgestellten Werkzeuge zur Überwachung der Zustellbarkeit Ihrer Plattform.
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
internal: n
snippet: y
translation-type: ht
source-git-commit: c89973e2c733d9c0b1c4434e77ef51103ccde0fa
workflow-type: ht
source-wordcount: '443'
ht-degree: 100%

---


# Monitoring der Zustellbarkeit{#monitor-deliverability}

Im Folgenden finden Sie Details zum **[!UICONTROL Versanddurchsatz]**-Bericht sowie zu den unterschiedlichen von Adobe Campaign bereitgestellten Monitoring-Werkzeugen. Hier sind zusätzliche Tipps für das Monitoring der Zustellbarkeit:
* Prüfen Sie regelmäßig den Versanddurchsatz für die gesamte Plattform, um festzustellen, ob er der ursprünglichen Einstellung entspricht.
* Achten Sie darauf, dass weitere Versuche in den Versandvorlagen korrekt eingerichtet sind (30 Minuten für das Versuchsintervall und mehr als 20 weitere Versuche).
* Prüfen Sie regelmäßig, ob das Bounce-Postfach zugänglich ist, und sorgen Sie dafür, dass die Gültigkeit des Kontos nicht abläuft.
* Prüfen Sie, ob die einzelnen Versanddurchsätze der Gültigkeit des Versandinhalts entsprechen (&quot;Flash Sales&quot; zum Beispiel sollten innerhalb von Minuten, nicht von Tagen zugestellt werden).
* Wenn der Versand in Schüben erfolgt, stellen Sie sicher, dass genügend Zeit vorhanden ist, damit ein Schub fertiggestellt werden kann, bevor der nächste beginnt.
* Prüfen Sie, ob die Anzahl der Fehler und der neuen Quarantänen der anderer Sendungen entspricht.
* Prüfen Sie in den Versandlogs sorgfältig die Art der hervorgehobenen Fehler (Blockierungsliste, DNS-Probleme, Anti-Spam-Regeln usw.).

## Versanddurchsatz {#delivery-throughput}

Dieser Bericht enthält Informationen zum Versanddurchsatz der gesamten Plattform in einem bestimmten Zeitraum und misst die Geschwindigkeit der Nachrichtenzustellung.

Weitere Informationen finden Sie unter [Versanddurchsatz](../../reporting/using/delivery-throughput.md).

![](assets/delivery_reports_1.png)

Sie können die angezeigten Werte konfigurieren, indem Sie den Parameter ändern.

Es stehen weitere Berichte zur Verfügung, z. B. **[!UICONTROL Versandzusammenfassung]** oder **[!UICONTROL Fehler und Bounces]**. Weiterführende Informationen dazu finden Sie unter [Dynamische Berichte](../../reporting/using/about-dynamic-reports.md).

## Sendungen beobachten {#monitoring-deliveries}

Über das Nachrichten-Dashboard können Sie auf diese Versandlogs zugreifen: **[!UICONTROL Versandlogs]**, **[!UICONTROL Ausschlusslogs]**, **[!UICONTROL Ausschlussgründe]**, **[!UICONTROL Trackinglogs]** und **[!UICONTROL Getrackte URLs]**. In ihnen erfahren Sie Versanddetails, welche Zielgruppe ausgeschlossen war und den Ausschlussgrund sowie Tracking-Informationen wie Öffnungen und Klicks.

Weiterführende Informationen dazu finden Sie unter [Sendungen beobachten](../../sending/using/monitoring-a-delivery.md).

![](assets/sending_delivery1.png)

## Warnungen erhalten {#receiving-alerts}

Bei der Funktion **[!UICONTROL Versandwarnungen]** handelt es sich um ein Warnungsmanagementsystem, über das eine Benutzergruppe automatisch Benachrichtigungen zu ihren Sendungen erhält.

Weiterführende Informationen dazu finden Sie unter [Warnungen bei Zustellproblemen erhalten](../../sending/using/receiving-alerts-when-failures-happen.md).

## Signal Spam {#signal-spam}

Signal Spam ist ein französischer Dienst, der anonymisiertes Feedback-Schleifen-Reporting für französische ISPs anbietet (Orange, SFR).

Mit diesem Dienst können Sie die Reputation französischer ISPs verfolgen und die Kundenaktivität tracken.

Signal Spam bietet auch eine eigene Benutzeroberfläche für die direkte Beschwerdemöglichkeit zum Beenden von Benutzerlogs. Durch diese Beschwerden werden dann E-Mails aus der Datenbank entfernt und in Quarantäne gestellt.

## 250ok {#solution-250ok}

250ok ist eine Überwachungslösung, die IP- und Domain-Blockierungslisten sowie Reputationsindikatoren bereitstellt.

Die Informationen werden in Echtzeit bereitgestellt und ermöglichen damit eine proaktive Unterstützung. 250ok ergänzt interne Zustellbarkeits-Tools von Adobe.

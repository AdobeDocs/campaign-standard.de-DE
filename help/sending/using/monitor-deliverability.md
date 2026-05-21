---
title: Monitoring der Zustellbarkeit in Adobe Campaign Standard
description: Verwenden Sie die von Adobe Campaign Standard bereitgestellten Werkzeuge zur Überwachung der Zustellbarkeit Ihrer Plattform.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: Deliverability
role: User
level: Intermediate
exl-id: 683341fb-fef5-4aa1-8606-9526d9ae6290
TQID: https://experienceleague.adobe.com/e185wubn3YVJGYrzxDtT6CquM1hojLGStmxbsvtV0oE
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 330
ht-degree: 100%

---

# Überwachen der Zustellbarkeit{#monitor-deliverability}

Im Folgenden finden Sie Details zum Bericht **[!UICONTROL Versanddurchsatz]** sowie zu den unterschiedlichen von Adobe Campaign bereitgestellten Monitoring-Tools. Im Folgenden finden Sie einige zusätzliche Richtlinien zum Zustellbarkeits-Monitoring:

* Prüfen Sie regelmäßig den Versanddurchsatz für die gesamte Plattform, um festzustellen, ob er der ursprünglichen Einstellung entspricht.
* Achten Sie darauf, dass weitere Versuche in den Versandvorlagen korrekt eingerichtet sind (30 Minuten für das Versuchsintervall und mehr als 20 weitere Versuche).
* Prüfen Sie regelmäßig, ob das Bounce-Postfach zugänglich ist, und sorgen Sie dafür, dass die Gültigkeit des Kontos nicht abläuft.
* Prüfen Sie, ob die einzelnen Versanddurchsätze der Gültigkeit des Versandinhalts entsprechen (&quot;Flash Sales&quot; zum Beispiel sollten innerhalb von Minuten, nicht von Tagen zugestellt werden).
* Prüfen Sie, ob die Anzahl der Fehler und der neuen Quarantänen der anderer Sendungen entspricht.
* Prüfen Sie in den Versandlogs sorgfältig die Art der hervorgehobenen Fehler (Blockierungsliste, DNS-Probleme, Anti-Spam-Regeln usw.).

## Versanddurchsatz {#delivery-throughput}

Dieser Bericht enthält Informationen zum Versanddurchsatz der gesamten Plattform in einem bestimmten Zeitraum und misst die Geschwindigkeit der Nachrichtenzustellung.

Weitere Informationen finden Sie unter [Versanddurchsatz](../../reporting/using/delivery-throughput.md).

![](assets/delivery_reports_1.png)

Sie können die angezeigten Werte konfigurieren, indem Sie den Parameter ändern.

Es stehen weitere Berichte zur Verfügung, z. B. **[!UICONTROL Versandzusammenfassung]** oder **[!UICONTROL Unzustellbare Nachrichten und Bounces]**. Weiterführende Informationen dazu finden Sie unter [Dynamische Berichte](../../reporting/using/about-dynamic-reports.md).

## Sendungen überwachen {#monitoring-deliveries}

Das Nachrichten-Dashboard bietet Ihnen Zugriff auf die Versandlogs: **[!UICONTROL Versandprotokolle]**, **[!UICONTROL Ausschlussprotokolle]**, **[!UICONTROL Ausschlussgründe]**, **[!UICONTROL Trackinglogs]** und **[!UICONTROL Tracking-URLs]**. In ihnen werden Details zum Versand dargestellt und Sie erfahren, welche Zielgruppe warum ausgeschlossen wurde sowie Tracking-Informationen wie z. B. Öffnungen und Klicks.

Weiterführende Informationen dazu finden Sie unter [Überwachen von Sendungen](../../sending/using/monitoring-a-delivery.md).

![](assets/sending_delivery1.png)

## Warnungen erhalten {#receiving-alerts}

Bei der Funktion **[!UICONTROL Versandwarnungen]** handelt es sich um ein Warnungsmanagementsystem, über das eine Benutzergruppe automatisch Benachrichtigungen zu ihren Sendungen erhält.

Weiterführende Informationen dazu finden Sie unter [Warnungen bei Zustellproblemen erhalten](../../sending/using/receiving-alerts-when-failures-happen.md).

<!--
## External tools (#external-tools)

### Signal Spam {#signal-spam}

Signal Spam is a French service which offers anonymized feedback loop reporting for French ISPs (Orange, SFR).

This service allows you to follow the reputation of the French ISPs and track customers' activity evolution.

Signal Spam also provides direct complaints that end users log through a dedicated interface. Those complaints are then quarantined from the email address database.

### 250ok {#solution-250ok}

250ok is a monitoring solution which provides IP and domain denylists, as well as reputation indicators.

The information provided is real-time, which allows for a pro-active assistance. 250ok a complementary solution to the Adobe deliverability internal tools.
-->

---
title: Überwachung der Lieferbarkeit in Adobe Campaign Standard
description: Verwenden Sie die von Adobe Campaign Standard angebotenen Tools, um die Zustellbarkeit Ihrer Plattform zu überwachen.
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
translation-type: tm+mt
source-git-commit: 1d5bb21ab16df87e268b9eabe92965be1b052556

---


# Überwachung der Zustellbarkeit{#monitor-deliverability}

Nachstehend finden Sie Angaben zum **[!UICONTROL Bereitstellungsdurchsatz]** sowie zu den verschiedenen Überwachungswerkzeugen von Adobe Campaign. Im Folgenden finden Sie einige zusätzliche Leitlinien zur Überwachung der Lieferbarkeit:
* Überprüfen Sie regelmäßig den Lieferdurchsatz für die gesamte Plattform, um zu überprüfen, ob er mit dem ursprünglichen Setup übereinstimmt.
* Vergewissern Sie sich, dass die Wiederholungen in den Bereitstellungsvorlagen korrekt eingerichtet sind (30 Minuten für die Wiederholungszeit und mehr als 20 Wiederholungen).
* Überprüfen Sie regelmäßig, ob der Absprungkasten verfügbar ist und ob das Konto nicht abläuft.
* Überprüfen Sie, ob der Lieferdurchsatz mit der Gültigkeit des Lieferinhalts (z. B. 'Flash-Verkäufe' sollten in Minuten und nicht in Tagen ausgeliefert werden.
* Wenn Sie Wellen verwenden, stellen Sie sicher, dass jede Welle genügend Zeit hat, um zu beenden, bevor die nächste ausgelöst wird.
* Vergewissern Sie sich, dass die Anzahl der Fehler und neuen Quarantäne mit anderen Lieferungen übereinstimmt.
* Die Lieferprotokolle sind sorgfältig zu lesen, um die Art der hervorgehobenen Fehler (graue oder schwarze Liste, DNS-Probleme, Anti-Spam-Regeln usw.) zu überprüfen.

## Versanddurchsatz {#delivery-throughput}

Dieser Bericht enthält Informationen zum Bereitstellungsdurchsatz der gesamten Plattform für einen bestimmten Zeitraum, um die Geschwindigkeit zu messen, mit der die Nachrichten gesendet werden.

Weitere Informationen finden Sie unter [Bereitstellungsdurchsatz](../../reporting/using/delivery-throughput.md).

![](assets/delivery_reports_1.png)

Sie können die angezeigten Werte konfigurieren, indem Sie den Zeitplan ändern.

Es stehen weitere Berichte zur Verfügung, z. B. **[!UICONTROL Lieferzusammenfassung]** oder **[!UICONTROL Nicht-Lieferzeiten]**. Weitere Informationen finden Sie unter [Dynamische Berichte](../../reporting/using/about-dynamic-reports.md).

## Überwachung der Lieferungen {#monitoring-deliveries}

Das Meldungsdashboard gibt Ihnen Zugriff auf die Lieferprotokolle: **[!UICONTROL Senden von Protokollen]**, **[!UICONTROL Ausschlussprotokolle]**, **[!UICONTROL Ausschlussursachen]**, **[!UICONTROL Verfolgungsprotokolle]** und **[!UICONTROL verfolgte URLs]**. In ihnen werden Details zum Versand dargestellt und Sie erfahren, welche Zielgruppe warum ausgeschlossen wurde sowie Tracking-Informationen wie z. B. Öffnungen und Klicks.

For more on this, see [Monitoring a delivery](../../sending/using/monitoring-a-delivery.md).

![](assets/sending_delivery1.png)

## Erhalt von Warnungen {#receiving-alerts}

Bei der Funktion **[!UICONTROL Versandwarnungen]handelt es sich um ein Warnungsmanagementsystem, über das eine Benutzergruppe automatisch Benachrichtigungen zu ihren Sendungen erhält.**

Weitere Informationen finden Sie unter [Erhalten von Warnungen bei Fehlern](../../sending/using/receiving-alerts-when-failures-happen.md).

## Signal-Spam {#signal-spam}

Signal Spam ist ein französischer Dienst, der anonymisierte Feedback-Schleifenberichte für französische ISPs (Orange, SFR) anbietet.

Dieser Service ermöglicht es Ihnen, den Ruf der französischen ISPs zu verfolgen und die Entwicklung der Kundenaktivität zu verfolgen.

Signal Spam bietet auch direkte Beschwerden, dass Endbenutzer sich über eine dedizierte Schnittstelle anmelden. Diese Beschwerden werden dann aus der E-Mail-Adressdatenbank isoliert.

## 250ok {#solution-250ok}

250ok ist eine Überwachungslösung, die IP, Domain Blacklisting und Reputationsindikatoren liefert.

Die bereitgestellten Informationen sind in Echtzeit verfügbar, was eine proaktive Unterstützung ermöglicht. 250Bietet eine ergänzende Lösung zu den internen Werkzeugen von Adobe.

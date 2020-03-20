---
title: Bounces
description: Über die Bounces im vordefinierten Bericht erhalten Sie Informationen zum Status Ihrer versendeten Kampagnen und über etwaige Versandfehler.
page-status-flag: never-activated
uuid: 90087311-4236-4df9-ae7d-4a15c00c70ab
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: list-of-reports
discoiquuid: 5ae561b4-03cf-4541-87ff-47f1027d53b8
context-tags: bounceReport,main;campaignCirculationReport,main;programCirculationReport,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: bee7ea0f1728da2a96c1f225b91b13a7903be660

---


# Bounces{#bounce-summary}

Dieser Bericht zeigt die Gesamtheit aller Statistiken zu bei Sendungen aufgetretenen Hard- und Softbounces und der automatischen Bounce-Verarbeitung.

![](assets/campaign_reports_bounces.png)

Für jede Tabelle werden Zusammenfassungen und Grafiken erstellt. Die Darstellung dieser Details können Sie in deren Einstellungen ändern.

Die Liste **Flop-5-Verteilung** enthält die fünf Sendungen mit der höchsten Anzahl von Adressen, die neu in Quarantäne sind.

Die Tabelle **Bounce-Gründe** enthält für jeden Versand alle verfügbaren Daten zur jeweiligen Fehlerursache der Bounces:

* **[!UICONTROL User unknown]**: Der Fehlertyp, der beim Senden eines Versands an eine ungültige E-Mail-Adresse generiert wird.
* **[!UICONTROL Invalid domain]**: Der Fehlertyp, der erzeugt wird, wenn ein Versand an eine E-Mail-Adresse gesendet wird, deren Domäne falsch ist oder nicht mehr existiert.
* **[!UICONTROL Unreachable]**: Der Fehlertyp, der in der Meldungszeichenfolge (z. B. Domäne vorübergehend unerreichbar) aufgetreten ist.
* **[!UICONTROL Account disabled]**: Der Fehlertyp, der generiert wird, wenn ein Versand an eine E-Mail-Adresse gesendet wird, die nicht mehr vorhanden ist.
* **[!UICONTROL Mailbox full]**: Der Typ des Fehlers, der erzeugt wird, wenn der Posteingang des Empfängers voll ist. Vor der Generierung dieses Fehlers werden fünf Zustellversuche unternommen.
* **[!UICONTROL Not connected]**: Der Typ des Fehlers, der erzeugt wird, wenn das Handy des Empfängers ausgeschaltet ist oder zum Zeitpunkt des Sendens der Nachricht keine Verbindung zu einem Netzwerk besteht.

   >[!NOTE]
   >
   >Dieser Fehler bezieht sich nur auf Sendungen über den Mobile-Kanal.

* **[!UICONTROL Refused]**: Die Fehlerart, die erzeugt wird, wenn eine Adresse vom Internet Dienstleister (ISP) abgelehnt wird. wenn beispielsweise eine Sicherheitsregel von einer Anti-Spam-Software angewendet wurde.

In der Tabelle **Domänenverteilung** werden alle Probleme während des Versands entsprechend der Domain des Empfängers angezeigt.

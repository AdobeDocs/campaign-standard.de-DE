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
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '285'
ht-degree: 100%

---


# Bounces{#bounce-summary}

Dieser Bericht zeigt die Gesamtheit aller Statistiken zu bei Sendungen aufgetretenen Hard- und Softbounces und der automatischen Bounce-Verarbeitung.

![](assets/campaign_reports_bounces.png)

Für jede Tabelle werden Zusammenfassungen und Grafiken erstellt. Die Darstellung dieser Details können Sie in deren Einstellungen ändern.

Die Liste **Flop-5-Verteilung** enthält die fünf Sendungen mit der höchsten Anzahl von Adressen, die neu in Quarantäne sind.

Die Tabelle **Bounce-Gründe** enthält für jeden Versand alle verfügbaren Daten zur jeweiligen Fehlerursache der Bounces:

* **[!UICONTROL Unbekannter Nutzer]**: Fehler, der bei einem Versand erzeugt wird, wenn die E-Mail-Adresse ungültig ist.
* **[!UICONTROL Ungültige Domain]**: Fehler, der bei einem Versand erzeugt wird, wenn die E-Mail-Domain ungültig ist oder nicht mehr existiert.
* **[!UICONTROL Unerreichbar]**: Fehler, der in der Zeichenfolge des Nachrichtenversands erscheint (z. B. Domain vorübergehend unerreichbar).
* **[!UICONTROL Konto deaktiviert]**: Fehler, der bei einem Versand erzeugt wird, wenn eine Adresse nicht mehr existiert.
* **[!UICONTROL Postfach voll]**: Fehler, der erzeugt wird, wenn die Inbox des Empfängers voll ist. Vor der Generierung dieses Fehlers werden fünf Zustellversuche unternommen.
* **[!UICONTROL Nicht angemeldet]**: Fehler, der erzeugt wird, wenn das Mobiltelefon des Empfängers zum Zeitpunkt des Nachrichtenversands ausgeschaltet oder nicht mit dem Netz verbunden ist.

   >[!NOTE]
   >
   >Dieser Fehler bezieht sich nur auf Sendungen über den Mobile-Kanal.

* **[!UICONTROL Abgelehnt]**: Fehler, der erzeugt wird, wenn eine Adresse von einem ISP (Internet Service Provider) abgelehnt wird, wenn beispielsweise eine Sicherheitsregel von einer Anti-Spam-Software angewendet wurde.

In der Tabelle **Domänenverteilung** werden alle Probleme während des Versands entsprechend der Domain des Empfängers angezeigt.

---
title: Bounces
seo-title: Bounces
description: Bounces
seo-description: Über die Bounces im vordefinierten Bericht erhalten Sie Informationen zum Status Ihrer versendeten Kampagnen und über etwaige Versandfehler.
page-status-flag: nie aktiviert
uuid: 90087311-4236-4 df 9-ae 7 d -4 a 15 c 00 c 70 ab
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Berichterstellung
content-type: Referenz
topic-tags: list-of-reports
discoiquuid: 5 ae 561 b 4-03 cf -4541-87 ff -47 f 1027 d 53 b 8
context-tags: Bouncereport, main; Campaigncirculationreport, main; Programcirculationreport, main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 77b0933bcd004cedc6a58f80717a4284b284e0cd

---


# Bounces{#bounce-summary}

Dieser Bericht zeigt die Gesamtheit aller Statistiken zu bei Sendungen aufgetretenen Hard- und Softbounces und der automatischen Bounce-Verarbeitung.

![](assets/campaign_reports_bounces.png)

Für jede Tabelle werden Zusammenfassungen und Grafiken erstellt. Die Darstellung dieser Details können Sie in deren Einstellungen ändern.

Die Liste **Flop-5-Verteilung** enthält die fünf Sendungen mit der höchsten Anzahl von Adressen, die neu in Quarantäne sind.

Die Tabelle **Bounce-Gründe** enthält für jeden Versand alle verfügbaren Daten zur jeweiligen Fehlerursache der Bounces:

* **[!UICONTROL Unbekannter Nutzer]**: Fehler, der bei einem Versand erzeugt wird, wenn die E-Mail-Adresse ungültig ist.
* **[!UICONTROL Ungültige Domain]**: Fehler, der bei einem Versand erzeugt wird, wenn die E-Mail-Domain ungültig ist oder nicht mehr existiert.
* **[!UICONTROL Unerreichbar]**: Fehler, der im Nachrichtenversand-String auftritt. Beispielsweise SMTP-Relais-Vorfall, vorübergehend unerreichbare Domain etc.
* **[!UICONTROL Konto deaktiviert]**: Fehler, der bei einem Versand erzeugt wird, wenn eine Adresse nicht mehr existiert.
* **[!UICONTROL Postfach voll]**: Fehler, der erzeugt wird, wenn die Inbox des Empfängers voll ist. Vor der Generierung dieses Fehlers werden fünf Zustellversuche unternommen.
* **[!UICONTROL Nicht angemeldet]**: Fehler, der erzeugt wird, wenn das Mobiltelefon des Empfängers zum Zeitpunkt des Nachrichtenversands ausgeschaltet oder nicht mit dem Netz verbunden ist.

   >[!NOTE]
   >
   >Dieser Fehler bezieht sich nur auf Sendungen über den Mobile-Kanal.

* **[!UICONTROL Abgelehnt]**: Fehler, der erzeugt wird, wenn eine Adresse von einem ISP (Internet Service Provider) abgelehnt wird, wenn beispielsweise eine Sicherheitsregel von einer Anti-Spam-Software angewendet wurde.

In der Tabelle **Domänenverteilung** werden alle Probleme während des Versands entsprechend der Domain des Empfängers angezeigt.

---
title: Über dynamische Berichte
seo-title: Über dynamische Berichte
description: Über dynamische Berichte
seo-description: Mit dynamischen Berichten können Sie Variablen und Dimensionen in Ihre Freiformumgebung ziehen und die Wirkung Ihrer Kampagnen analysieren.
page-status-flag: never-activated
uuid: a84a18bd-4e33-466e-a6ce-d7008fe12746
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: about-reporting
discoiquuid: bbb41c38-12c1-4625-85d5-69627e2f4b39
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4d3f2efb118e07247caa15ef7edaa67657d164ea

---


# Über dynamische Berichte{#about-dynamic-reports}

>[!NOTE]
>
>Nur Benutzer, die Administratorrechte besitzen oder deren Organisationseinheiten mit **Alle** festgelegt sind, können einen neuen Bericht erstellen oder speichern. Weiterführende Informationen hierzu finden Sie in diesem [Abschnitt](../../administration/using/users-management.md).

![](assets/dynamic_report_intro.png)

Die dynamische Berichterstellung ermöglicht vollständig anpassbare und in Echtzeit aktualisierte Berichte. Durch sie kann auf Profildaten zugegriffen werden, was die demografische Analyse nach Profildimensionen wie Geschlecht, Stadt und Alter sowie nach Daten von E-Mail-Kampagnen wie Öffnungen und Klicks ermöglicht. Mit der Drag &amp; Drop-Funktion können Sie Daten analysieren sowie feststellen, wie Ihre E-Mail-Kampagnen bei Ihren wichtigsten Kundensegmenten angekommen sind, und ihre Wirkung auf die Empfänger messen.

Dank dem Drag &amp; Drop-Menü und den anpassbaren Grafiken können Sie mit dieser Funktion Dimensionen, Messwerte und Zeitspannen beliebig kombinieren und so dynamische Berichte mit unbegrenzten Verteilungs- und Vergleichsmöglichkeiten erstellen.


**Verwandte Themen:**

* [Verfügbare Berichte](../../reporting/using/defining-the-report-period.md)
* [Organisationseinheiten](../../administration/using/organizational-units.md)
* Video [Dynamic reports](https://helpx.adobe.com/campaign/kt/acs/using/acs-creating-a-dynamic-report-feature-video-use.html)

## Zugriff auf dynamische Berichte {#accessing-dynamic-reports}

Der Zugriff auf Berichte erfolgt:

* Über die Startseite durch die Auswahl des Tabs **[!UICONTROL Berichte]** in der Symbolleiste am oberen Bildschirmrand oder die Karte **[!UICONTROL Berichte]**, um Berichte zu allen Sendungen anzuzeigen.

   ![](assets/campaign_reports_access.png)

* In allen Programmen, Kampagnen und Nachrichten über die Schaltfläche **Berichte** durch Anklicken von **Dynamische Berichte**, um nur die Berichte für diesen Versand anzuzeigen.

   ![](assets/campaign_reports_description.png)

Gewisse Berichte stehen mitunter nicht unmittelbar nach einem Versand zur Verfügung, was von der Dauer der Datenerhebung und Informationsverarbeitung abhängt.

Es gibt zwei Kategorien von dynamischen Berichten:

* **Vorlagen** können geändert werden, indem sie ausgehend von der Vorlage mit der Option **Speichern als** (**Projekt &gt; Speichern als...**) kopiert werden.
* **Benutzerdefinierte Berichte** (blau) können direkt durch die Auswahl der Schaltfläche **Neues Projekt erstellen** auf der **Berichte**-Startseite erstellt werden.

>[!NOTE]
>
>Die Daten werden entsprechend Ihrer Organisationseinheit gefiltert.

![](assets/dynamic_report_overview.png)

## Nutzungsvereinbarung zur dynamischen Berichterstattung {#dynamic-reporting-usage-agreement}

>[!NOTE]
>
>Diese Änderungen gelten nur ab Version 19.4 von Campaign Standard.

Der Zweck der Vereinbarung über die Verwendung dynamischer Berichte besteht darin, als Popup-Zustimmung für die Datenverarbeitung zu fungieren. Standardmäßig kann diese Vereinbarung nur durch Benutzer mit Administratorrechten sichtbar gemacht und akzeptiert oder abgelehnt werden.

Drei Optionen sind verfügbar:

* **[!UICONTROL Später fragen]**: Mit dieser Auswahl wird die Nutzervereinbarung erst wieder in 24 Stunden angezeigt.
* **[!UICONTROL Akzeptieren]**: Indem Sie diese Vereinbarung akzeptieren, autorisieren Sie Adobe Campaign, die persönlichen ID-Informationen Ihrer Kunden zu erfassen und sie an das Berichterstellungs- oder Rechenzentrum zu übertragen.
* **[!UICONTROL Ablehnen]**: Wenn Sie die Nutzervereinbarung ablehnen, erscheinen die Profildimensionen nicht in Ihren Berichten und die personenbezogenen Daten Ihrer Kunden werden weder erfasst noch transferiert. Beachten Sie, dass in diesem Fall die externe ID noch erfasst und zur Identifizierung der Endbenutzer verwendet wird.

Die nachstehende Tabelle zeigt, was nach der Annahme mit dieser Vereinbarung je nach Region geschieht.

|  | Dynamische Berichterstellung | Microsoft Dynamics 365 Connector |
|---|---|---|
| Amerika und APAC (Asien/Pazifik) | **Funktion verfügbar**. <br>Alle sofort einsetzbaren (d.h. Stadt, Land/Region, Bundesland, Geschlecht und Segmente auf der Grundlage des Alters) und benutzerspezifische Profildaten, die in das US-Berichtszentrum gesendet werden. For more information on profile dimensions, refer to this [page](../../reporting/using/list-of-components-.md) | **Funktion verfügbar**. <br>Alle vordefinierten und benutzerdefinierten Profilfelder und Ereignisfelder von Adobe Campaign Standard werden im US-Rechenzentrum verarbeitet. |
| EMEA (Europe Middle East &amp; Africa) | **Funktion verfügbar**. <br>Alle vordefinierten (d.h. Stadt, Land/Region, Bundesland, Geschlecht und Segmente auf der Grundlage des Alters) und benutzerspezifische Profilinformationen, die in das EMEA-Berichtszentrum gesendet werden. For more information on profile dimensions, refer to this [page](../../reporting/using/list-of-components-.md) | **Funktion verfügbar.** Im Rechenzentrum von EMEA werden <br>alle vordefinierten und benutzerdefinierten Profilfelder und Ereignisfelder von Adobe Campaign Standard verarbeitet. **[!UICONTROL Steuerungsdaten]** , die Adobe-I/O-Registrierungsdaten und IDs von Kundenereignissen enthalten, die im US-Rechenzentrum gesendet und gespeichert werden. |

Die nachstehende Tabelle zeigt an, was nach dem Ablehnen dieser Vereinbarung je nach Region geschieht. Beachten Sie, dass Berichte zu Auslieferungen und Microsoft Dynamics 365-Integration auch dann verfügbar sein werden, wenn Sie diese Vereinbarung ablehnen.

| Region | Dynamische Berichterstellung | Microsoft Dynamics 365 Connector |
|---|---|---|
| Amerika und APAC (Asien/Pazifik) | **Funktion verfügbar**. <br> Keine standardmäßigen und benutzerspezifischen Profilinformationen werden mit Ausnahme von ExternalID in das US-Berichterstellungszentrum gesendet. | **Funktion verfügbar**. <br>Es werden keine vordefinierten oder benutzerdefinierten Profilfelder an das US-Rechenzentrum gesendet, mit Ausnahme der externen ID und Empfänger-ID. <br>Alle Ereignisfelder in Adobe Campaign Standard, die im US-Rechenzentrum verarbeitet werden, mit Ausnahme von Segmentcode und Spiegelseite-ID. |
| EMEA (Europe Middle East &amp; Africa) | **Funktion verfügbar**. <br>Keine standardmäßigen und benutzerspezifischen Profilinformationen wurden mit Ausnahme von ExternalID in das EMEA-Berichterstellungszentrum gesendet. | **Funktion verfügbar.** Es werden <br>keine vordefinierten oder benutzerdefinierten Profilfelder an das EMEA-Rechenzentrum gesendet, mit Ausnahme der externen ID und Empfänger-ID. <br>Alle Adobe Campaign Standard-Ereignisfelder, die im EMEA-Rechenzentrum verarbeitet werden, mit Ausnahme von Segmentcode und Spiegelseite-ID. |

Diese Entscheidung ist nicht endgültig. Sie können sie jederzeit ändern durch die Auswahl von **[!UICONTROL Transfer von personenbezogenen Daten in die USA ermöglichen, um Reporting zu Profildaten zu verwenden]** in **[!UICONTROL Administration]** &gt; **[!UICONTROL Anwendungseinstellungen]** &gt; **[!UICONTROL Optionen]**.

Der Wert kann jederzeit geändert werden. The value 1 corresponds to **[!UICONTROL Ask me later]**, 2 **[!UICONTROL Decline]** and 3 **[!UICONTROL Accept]**.

![](assets/pii_window_2.png)

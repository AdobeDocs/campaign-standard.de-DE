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
translation-type: ht
source-git-commit: 4d95fe00c1958399ff4d22d5f0e7762f895b4032

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
* Video [Dynamic reports](https://helpx.adobe.com/de/campaign/kt/acs/using/acs-creating-a-dynamic-report-feature-video-use.html)

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

Mithilfe dynamischer Berichte können Sie auf Profildaten basierende Berichte nach Profildimensionen filtern.

Sie müssen erst die Nutzungsvereinbarung zur dynamischen Berichterstattung akzeptieren, bevor Sie die Profildimensionen in Ihren Berichten anzeigen und verwenden können. Standardmäßig kann diese Vereinbarung nur durch Benutzer mit Administratorrechten sichtbar gemacht und akzeptiert oder abgelehnt werden.

Diese Vereinbarung ermöglicht den Transfer und die Speicherung folgender Profildaten in den USA: Stadt, Land/Region, Bundesland, Geschlecht und Alterssegmente.

Wenn Sie diese Vereinbarung akzeptieren, werden alle europäischen und nicht-europäischen Daten in die USA übertragen.

![](assets/pii_window.png)

Drei Optionen sind verfügbar:

* **[!UICONTROL Später fragen]**: Mit dieser Auswahl wird die Nutzervereinbarung erst wieder in 24 Stunden angezeigt.
* **[!UICONTROL Annehmen]**: Wenn Sie die Nutzervereinbarung akzeptieren, gestatten Sie Adobe Campaign, die personenbezogenen Daten Ihres Kunden zu erfassen und in die USA zu transferieren.
* **[!UICONTROL Ablehnen]**: Wenn Sie die Nutzervereinbarung ablehnen, erscheinen die Profildimensionen nicht in Ihren Berichten und die personenbezogenen Daten Ihrer Kunden werden weder erfasst noch transferiert.

Diese Entscheidung ist nicht endgültig. Sie können sie jederzeit ändern durch die Auswahl von **[!UICONTROL Transfer von personenbezogenen Daten in die USA ermöglichen, um Reporting zu Profildaten zu verwenden]** in **[!UICONTROL Administration]** &gt; **[!UICONTROL Anwendungseinstellungen]** &gt; **[!UICONTROL Optionen]**.

Der Wert kann jederzeit geändert werden. Der Wert -1 bedeutet **[!UICONTROL Später fragen]**, 1 bedeutet **[!UICONTROL Akzeptieren]** und 0 bedeutet **[!UICONTROL Ablehnen]**.

![](assets/pii_window_2.png)


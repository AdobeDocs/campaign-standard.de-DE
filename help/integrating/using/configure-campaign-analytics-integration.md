---
title: Integration von Campaign mit Analytics konfigurieren
description: Hier erfahren Sie, wie Sie die Integration von Adobe Analytics konfigurieren müssen, um die Wirkung Ihrer E-Mail-Sendungen zu messen.
page-status-flag: never-activated
uuid: bdaa00b0-7445-469c-8268-9d06c53ce2b0
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
discoiquuid: 92b9004c-cba0-41fd-a035-32bee1d6a42c
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '257'
ht-degree: 100%

---


# Integration von Campaign mit Analytics konfigurieren{#configure-campaign-analytics-integration}

Durch diese Integration können Sie Ihre KPI-Daten direkt von Adobe Campaign an Adobe Analytics Standard oder Premium übertragen.

Für die Integration von Adobe Campaign mit Adobe Analytics müssen Sie zunächst das externe mit Adobe Analytics verknüpfte Konto konfigurieren.

Externe Konten und technische Workflows können nur vom funktionalen Administrator der Plattform verwaltet werden.

1. Greifen Sie mithilfe des Adobe-Campaign-Logos oben links im Bildschirm und der Schaltflächen **[!UICONTROL Administration > Anwendungskonfiguration > externe Konten auf das entsprechende Menü zu]**.
1. Wählen Sie das externe Konto **[!UICONTROL KPIs mit Adobe Analytics teilen]** aus.

   ![](assets/analytics_2.png)

1. Geben Sie Ihren **[!UICONTROL Webdienst-Benutzernamen]** und die **[!UICONTROL Geheimfrage für Webdienst]** im Feld **[!UICONTROL Verbindung]** ein.

   Diese Parameter können in Analytics durch die Auswahl von **[!UICONTROL Admin > Unternehmenseinstellungen > Webdienste abgerufen werden]**.

   ![](assets/analytics_1.png)

1. Verwenden Sie die Schaltfläche **[!UICONTROL Report Suites aktualisieren]**.
1. Wählen Sie in der Dropdown-Liste **[!UICONTROL Standard-Report-Suite von Analytics]** die Adobe-Analytics-Report-Suite aus, die Sie mit Adobe-Campaign-Daten anreichern möchten.

   Ihr externes Konto steht nun bereit und ist mit Adobe Analytics verknüpft. Sie können es jederzeit deaktivieren, indem Sie die Option **[!UICONTROL Aktiviert]** aktivieren.

   ![](assets/analytics.png)

Der technische Workflow **[!UICONTROL KPIs mit Adobe Analytics teilen]** wird jetzt automatisch gestartet und kann im erweiterten Menü über die Schaltflächen **[!UICONTROL Administration > Anwendungskonfiguration > Workflow]** aufgerufen werden. Dieser technische Workflow wird automatisch alle 15 Minuten ausgeführt und überträgt bis zu sechs Monate alte Daten an Adobe Analytics.

![](assets/analytics_3.png)

Ihre Daten sind nun in Adobe Analytics verfügbar.

**Verwandte Themen:**

* [Externe Konten](../../administration/using/external-accounts.md)
* [Technische Workflows](../../administration/using/technical-workflows.md)
* Video [Share KPIs for integrated Campaign reporting](https://helpx.adobe.com/de/marketing-cloud/how-to/email-marketing.html)


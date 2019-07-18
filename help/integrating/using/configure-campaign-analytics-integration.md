---
title: Integration von Campaign mit Analytics konfigurieren
seo-title: Integration von Campaign mit Analytics konfigurieren
description: Integration von Campaign mit Analytics konfigurieren
seo-description: Hier erfahren Sie, wie Sie die Integration von Adobe Analytics konfigurieren müssen, um die Wirkung Ihrer E-Mail-Sendungen zu messen.
page-status-flag: nie aktiviert
uuid: bdaa 00 b 0-7445-469 c -8268-9 d 06 c 53 ce 2 b 0
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird integriert
content-type: Referenz
topic-tags: working-with-campaign-and-analytics
discoiquuid: 92 b 9004 c-cba 0-41 fd-a 035-32 bee 1 d 6 a 42 c
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Integration von Campaign mit Analytics konfigurieren{#configure-campaign-analytics-integration}

Durch diese Integration können Sie Ihre KPI-Daten direkt von Adobe Campaign an Adobe Analytics Standard oder Premium übertragen.

Für die Integration von Adobe Campaign mit Adobe Analytics müssen Sie zunächst das externe mit Adobe Analytics verknüpfte Konto konfigurieren.

Externe Konten und technische Workflows können nur vom funktionalen Administrator der Plattform verwaltet werden.

1. Greifen Sie mithilfe des Adobe-Campaign-Logos oben links im Bildschirm und der Schaltflächen **[!UICONTROL Administration &gt; Anwendungskonfiguration &gt; externe Konten auf das entsprechende Menü zu]**.
1. Wählen Sie das externe Konto **[!UICONTROL KPIs mit Adobe Analytics teilen]aus.**

   ![](assets/analytics_2.png)

1. Geben Sie Ihren **[!UICONTROL Webdienst-Benutzernamen]** und die **[!UICONTROL Geheimfrage für Webdienst]im Feld** Verbindung] ein.**[!UICONTROL **

   Diese Parameter können in Analytics durch die Auswahl von **[!UICONTROL Admin &gt; Unternehmenseinstellungen &gt; Webdienste abgerufen werden]**.

   ![](assets/analytics_1.png)

1. Verwenden Sie die Schaltfläche **[!UICONTROL Report Suites aktualisieren].**
1. Wählen Sie in der Dropdown-Liste **[!UICONTROL Standard-Report-Suite von Analytics]die Adobe-Analytics-Report-Suite aus, die Sie mit Adobe-Campaign-Daten anreichern möchten.**

   Ihr externes Konto steht nun bereit und ist mit Adobe Analytics verknüpft. Sie können es jederzeit deaktivieren, indem Sie die Option **[!UICONTROL Aktiviert]aktivieren.**

   ![](assets/analytics.png)

The **[!UICONTROL Share KPIs with Adobe Analytics]** technical workflow will now automatically launch and can be viewed from the advanced menu by selecting **[!UICONTROL Administration &gt; Application settings &gt; Workflow]**. Dieser technische Workflow wird automatisch alle 15 Minuten ausgeführt und überträgt bis zu sechs Monate alte Daten an Adobe Analytics.

![](assets/analytics_3.png)

Ihre Daten sind nun in Adobe Analytics verfügbar.

**Verwandte Themen:**

* [Externe Konten](../../administration/using/external-accounts.md)
* [Technische Workflows](../../administration/using/technical-workflows.md)
* Video [Share KPIs for integrated Campaign reporting](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html)


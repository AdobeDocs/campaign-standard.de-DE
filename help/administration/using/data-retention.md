---
title: Datenspeicherung
description: Erfahren Sie mehr über die standardmäßigen Beibehaltungswerte für Standardtabellen
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 01cfa2a0-4ff5-4520-a515-11676de82528
source-git-commit: bd4b6d0d7d8fae6b14a41dc9001027d8154c9222
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 69%

---

# Datenspeicherung{#data-retention}

>[!NOTE]
>
>Datenberichte sind nur für die letzten drei Jahre verfügbar. Weitere Informationen zu Datenspeicherungszeiträumen erhalten Sie vom Adobe-Beratungspersonal oder von Ihren technischen Admins.

Die Standard-Protokolltabellen in Campaign haben voreingestellte Aufbewahrungsfristen, die die Dauer der Datenspeicherung begrenzen, um eine Überlastung Ihres Systems zu vermeiden.

Die Konfiguration der Datenaufbewahrung wird von den technischen Administrierenden von Adobe während der Implementierung festgelegt, und die Werte können bei jeder Implementierung je nach Kundenanforderungen variieren.

Wenden Sie sich an das Beratungspersonal von Adobe oder die technischen Administrierenden, um mehr über die Aufbewahrungsfristen zu erfahren, die für Ihre Umgebung gelten, oder um individuelle Aufbewahrungsfristen festzulegen.

Beachten Sie, dass es mit der standardmäßigen Workflow-Funktionalität möglich ist, Aufbewahrungsfristen für jede benutzerdefinierte Tabelle einzurichten.

Nachfolgend finden Sie die standardmäßigen Aufbewahrungsfristen für Standardtabellen. Wann immer möglich und abhängig von Ihrer Datennutzung empfiehlt Adobe Ihnen, die empfohlenen Aufbewahrungsfristen einzuhalten, um die Performance Ihrer Campaign-Instanz zu verbessern.

* **Konsolidiertes Tracking**: 6 Monate (empfohlen: 1 Monat)
* **Versandlogs**: 6 Monate (empfohlen: 1 Monat)
* **Trackinglogs**: 6 Monate (empfohlen: 1 Monat)
* **Ereignisse**: 1 Monat
* **Statistiken zur Ereignisverarbeitung**: 6 Monate (empfohlen: 1 Monat)
* **Archivierte Ereignisse**: 6 Monate (empfohlen: 1 Monat)
* **Vorläufige Entitäten**: 7 Tage
* **Ignorierte Pipeline-Ereignisse**: 1 Monat
* **Versandwarnungen**: 1 Monat
* **Export-Audit**: 6 Monate (empfohlen: 1 Monat)
* **Sendungen**: 2 Jahre

## Aufbewahrungszeitraum für Sendungen {#deliveries}

<!-- By default, the retention period for deliveries is unlimited.-->

Ab dem 1. Juni 2025 bleiben nur noch Sendungen aus den letzten zwei Jahren im System verfügbar. Weitere Informationen finden Sie unten:

* Sendungen, die älter als zwei Jahre sind, werden dauerhaft entfernt und sind nicht mehr zugänglich.
* Diese Bereinigung umfasst nur gesendete und fehlgeschlagene Sendungen. Wiederkehrende Sendungen, Versandentwürfe und Vorlagen sind davon nicht betroffen.
* Sobald ein Versand entfernt wurde, werden auch alle verknüpften Tracking- oder Versandinformationen dauerhaft gelöscht.
* Marketing- oder Transaktionsversandvorlagen werden nicht gelöscht.
* Bei wiederkehrenden Sendungen werden untergeordnete Sendungen, deren Aggregat-Zeitraum auf Monat oder Jahr festgelegt ist, nicht gelöscht.

Wenn Sie Prozesse wie den Workflow **[!UICONTROL Kopfzeilen aus Versandvorlagen kopieren]** beschleunigen möchten, kann die Aufbewahrungsfrist für Sendungen reduziert werden. Wenden Sie sich dazu bitte an Ihren Adobe-Support-Mitarbeiter.

<!--

However, if there is a high volume of deliveries on your instance, you can update the **NmsCleanup_DeliveryPurgeDelay** option available from the **[!UICONTROL Administration]** > **[!UICONTROL Application settings]** menu.

Each time the **[!UICONTROL Database cleanup]** workflow is run, the deliveries meeting the conditions set for this option will be deleted.

-->

<!--

When updating the **NmsCleanup_DeliveryPurgeDelay** option, it is recommended to proceed gradually with multiple iterations. For example, you can start by setting the value to 300 days, then 180 days, then 120 days, and so on - making sure iterations are at least 2 days apart. Otherwise, the **[!UICONTROL Database cleanup]** workflow may take much longer because of a large number of deliveries to delete.

This action can help speeding up processes such as the **[!UICONTROL Copy headers from delivery templates]** workflow. Learn more on technical workflows in [this section](technical-workflows.md).

The default value for the **NmsCleanup_DeliveryPurgeDelay** option is `-1`. In this case, no delivery is deleted.

For example, if you set it to `180`, any non-template deliveries that have not been updated in the last 180 days will be deleted when the **[!UICONTROL Database cleanup]** workflow is run.

-->



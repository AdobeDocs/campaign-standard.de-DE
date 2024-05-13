---
title: Datenbeibehaltung
description: Erfahren Sie mehr über die standardmäßigen Beibehaltungswerte für Standardtabellen
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 01cfa2a0-4ff5-4520-a515-11676de82528
source-git-commit: 2e81a05b1b647991250d13d7d37f5da275a8db44
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 47%

---

# Datenspeicherung{#data-retention}

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

## Aufbewahrungsfrist für Sendungen {#deliveries}

Standardmäßig ist die Aufbewahrungsfrist für Sendungen unbegrenzt.

Wenn Ihre Instanz jedoch eine hohe Versandmenge enthält, können Sie die **NmsCleanup_DeliveryPurgeDelay** -Option verfügbar über **[!UICONTROL Administration]** > **[!UICONTROL Anwendungseinstellungen]** Menü.

Jedes Mal, wenn **[!UICONTROL Datenbankbereinigung]** -Workflow ausgeführt wird, werden die Sendungen gelöscht, die die für diese Option festgelegten Bedingungen erfüllen.

Diese Aktion kann dazu beitragen, Prozesse wie die **[!UICONTROL Kopfzeilen aus Versandvorlagen kopieren]** Arbeitsablauf.

>[!NOTE]
>
>Weitere Informationen zu technischen Workflows finden Sie unter [diesem Abschnitt](technical-workflows.md).


Der Standardwert für die **NmsCleanup_DeliveryPurgeDelay** Option ist `-1`. In diesem Fall wird kein Versand gelöscht.

Wenn Sie beispielsweise `180`, werden alle Sendungen, die keine Vorlagen sind und in den letzten 180 Tagen nicht aktualisiert wurden, gelöscht, wenn die Variable **[!UICONTROL Datenbankbereinigung]** Workflow ausgeführt wird.

>[!NOTE]
>
>* Marketing- oder Transaktionsversandvorlagen werden nicht gelöscht.
>
>* Bei wiederkehrenden Sendungen werden untergeordnete Sendungen, deren Aggregat-Zeitraum auf Monat oder Jahr festgelegt ist, nicht gelöscht.

Beim Aktualisieren der **NmsCleanup_DeliveryPurgeDelay** -Option, wird empfohlen, schrittweise mehrere Iterationen durchzuführen. Sie können beispielsweise den Wert auf 300 Tage, dann auf 180 Tage, dann auf 120 Tage usw. setzen, um sicherzustellen, dass die Iterationen mindestens 2 Tage voneinander entfernt sind. Andernfalls wird die **[!UICONTROL Datenbankbereinigung]** Der Workflow kann aufgrund einer großen Anzahl von zu löschenden Sendungen viel länger dauern.


---
title: Datenspeicherung
description: Erfahren Sie mehr über die standardmäßigen Beibehaltungswerte für Standardtabellen
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 01cfa2a0-4ff5-4520-a515-11676de82528
source-git-commit: 99c092bc40c9176a25a6ec2a164ee1d3f85d5cbe
workflow-type: ht
source-wordcount: '434'
ht-degree: 100%

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

## Aufbewahrungszeitraum für Sendungen {#deliveries}

Standardmäßig ist der Aufbewahrungszeitraum für Sendungen unbegrenzt.

Wenn Sie jedoch ein hohes Volumen an Sendungen auf Ihrer Instanz haben, können Sie die Option **NmsCleanup_DeliveryPurgeDelay** aktualisieren, die im Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungseinstellungen]** verfügbar ist.

Jedes Mal, wenn der Workflow **[!UICONTROL Datenbankbereinigung]** ausgeführt wird, werden die Sendungen gelöscht, die die für diese Option festgelegten Bedingungen erfüllen.

Diese Aktion kann dazu beitragen, Prozesse wie den Workflow **[!UICONTROL Kopfzeilen aus Versandvorlagen kopieren]** zu beschleunigen.

>[!NOTE]
>
>Weitere Informationen zu technischen Workflows finden Sie in [diesem Abschnitt](technical-workflows.md).


Der Standardwert für die Option **NmsCleanup_DeliveryPurgeDelay** ist `-1`. In diesem Fall wird kein Versand gelöscht.

Wenn Sie ihn beispielsweise auf `180` festlegen, werden alle Sendungen ohne Vorlagen gelöscht, die in den letzten 180 Tagen nicht aktualisiert wurden, wenn der Workflow **[!UICONTROL Datenbankbereinigung]** ausgeführt wird.

>[!NOTE]
>
>* Marketing- oder Transaktionsversandvorlagen werden nicht gelöscht.
>
>* Bei wiederkehrenden Sendungen werden untergeordnete Sendungen, deren Aggregat-Zeitraum auf Monat oder Jahr festgelegt ist, nicht gelöscht.

Bei der Aktualisierung der Option **NmsCleanup_DeliveryPurgeDelay** wird empfohlen, schrittweise mit mehreren Ausführungen vorzugehen. Sie können beispielsweise den Wert auf 300 Tage, dann auf 180 Tage, dann auf 120 Tage usw. setzen. Dabei sollten Sie sicherstellen, dass die Ausführungen mindestens 2 Tage voneinander entfernt sind. Andernfalls kann der Workflow **[!UICONTROL Datenbankbereinigung]** aufgrund einer großen Anzahl von zu löschenden Sendungen viel länger dauern.


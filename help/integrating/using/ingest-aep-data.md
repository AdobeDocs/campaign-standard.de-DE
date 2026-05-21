---
title: Adobe Experience Platform-Zielgruppen in Campaign aufnehmen
description: Erfahren Sie, wie Sie Adobe Experience Platform-Zielgruppen in Campaign Standard aufnehmen.
audience: integrating
content-type: reference
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 5c266c44-535b-4954-862d-74c83a6f6406
TQID: https://experienceleague.adobe.com/LdVWEXa90p4yOKgPGG5LUOGRk3xWE8kJ8SkKM7ODBXk
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2:
  - id: a658c786-869b-4194-a780-2594d663adda
subfeature_v2:
  - id: b70f632b-2cfd-43d0-9266-284281100d70
  - id: fcb46c0f-76e1-48bc-9dd0-fcf9d97526cf
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 100%

---

# Adobe Experience Platform-Zielgruppen in Campaign aufnehmen {#destinations}

Um Adobe Experience Platform-Zielgruppen in Campaign aufzunehmen und sie in Ihren Workflows zu verwenden, müssen Sie zunächst Adobe Campaign als ein Adobe Experience Platform-**Ziel** verbinden und mit dem zu exportierenden Segment konfigurieren.

Nachdem das Ziel konfiguriert ist, werden die Daten an Ihren Speicherort exportiert. Zur Aufnahme der Daten muss in Campaign Standard noch ein spezieller Workflow erstellt werden.

## Adobe Campaign als Ziel verbinden

Konfigurieren Sie in Adobe Experience Platform eine Verbindung mit Adobe Campaign, indem Sie einen Speicherort für die exportierten Segmente auswählen. In diesem Schritt können Sie auch die zu exportierenden Segmente auswählen und zusätzliche XDM-Felder angeben, die einbezogen werden sollen.

Weitere Informationen finden Sie in der [Dokumentation zu Zielen](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/email-marketing/adobe-campaign.html?lang=de).

Nachdem das Ziel konfiguriert wurde, erstellt Adobe Experience Platform eine tabulatorgetrennte .txt- oder .csv-Datei an dem von Ihnen angegebenen Speicherort. Dieser Vorgang wird einmal alle 24 Stunden geplant und ausgeführt.

Sie können jetzt einen Campaign Standard-Workflow konfigurieren, um das Segment in Campaign aufzunehmen.

## Import-Workflow in Campaign Standard erstellen

Nachdem Campaign Standard als Ziel konfiguriert wurde, müssen Sie einen Workflow erstellen, um die von Adobe Experience Platform exportierte Datei zu importieren.

Fügen Sie dazu die Aktivität **[!UICONTROL Dateiübertragung]** hinzu und konfigurieren Sie sie. Weiterführende Informationen zur Konfiguration dieser Aktivität finden Sie in [diesem Abschnitt](../../automating/using/transfer-file.md).

![](assets/rtcdp-transfer-file.png)

Sie können dann Ihren Workflow gemäß Ihren Anforderungen erstellen (Datenbank mit den Segmentdaten aktualisieren, kanalübergreifende Sendungen an das Segment ausführen usw.).

Beispielsweise wird im folgenden Workflow die Datei täglich von Ihrem Speicherort heruntergeladen und anschließend die Campaign-Datenbank mit den Segmentdaten aktualisiert.

![](assets/rtcdp-workflow.png)

Beispiele für Daten-Management-Workflows sind im Abschnitt [Workflow-Anwendungsfälle](../../automating/using/about-workflow-use-cases.md#management) verfügbar.

Verwandte Themen:

* [Datenverwaltungsaktivitäten](../../automating/using/about-data-management-activities.md)
* [Über den Datenimport und -export](../../automating/using/about-data-import-and-export.md)

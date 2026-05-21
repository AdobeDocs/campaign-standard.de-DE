---
title: Daten von Campaign nach Adobe Experience Platform exportieren
description: Erfahren Sie, wie Sie Daten von Campaign Standard nach Adobe Experience Platform exportieren.
audience: integrating
content-type: reference
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: eccd2922-0e75-4525-9b60-b48f628deeae
TQID: https://experienceleague.adobe.com/wevJB72xRacTndQ1-VOyKHOtRak0UKJT2V-pzUd6d-Q
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
source-wordcount: 542
ht-degree: 94%

---

# Daten von Campaign nach Adobe Experience Platform exportieren {#sources}

Um Campaign Standard-Daten in die Adobe Echtzeit-Kundendatenplattform (RTCDP) zu exportieren, müssen Sie zunächst einen Workflow in Campaign Standard erstellen, um die Daten, die Sie austauschen möchten, in Ihren Speicherort auf Amazon Storage Service (S3) oder Azure Blob zu exportieren.

Nachdem der Workflow konfiguriert und Daten an Ihren Speicherort gesendet wurden, müssen Sie Ihren S3- oder Azure-Blob-Speicherort in Adobe Experience Platform als **Quelle** verbinden.

>[!NOTE]
>
>Wir empfehlen, nur in Campaign generierte Daten zu exportieren (z. B. Sendungen, Öffnungen, Klicks usw.) nach Adobe Experience Platform. Daten, die in einer Drittanbieter-Quelle (wie Ihrem CRM-System) aufgenommen werden, sollten direkt in Adobe Experience Platform importiert werden.

## Export-Workflow in Campaign Standard erstellen

Um Daten von Campaign Standard in Ihren S3- oder Azure-Blob-Speicher zu exportieren, müssen Sie einen Workflow erstellen, mit dem die zu exportierenden Daten bestimmt und an Ihren Speicherort gesendet werden.

Hierzu müssen Sie Folgendes hinzufügen und konfigurieren:

* Die Aktivität **[!UICONTROL Dateiextraktion]**, um die Zieldaten in eine CSV-Datei zu extrahieren. Weiterführende Informationen zur Konfiguration dieser Aktivität finden Sie in [diesem Abschnitt](../../automating/using/extract-file.md).

  ![](assets/rtcdp-extract-file.png)

* Die Aktivität **[!UICONTROL Dateiübertragung]**, um die CSV-Datei an Ihren Speicherort zu übertragen. Weiterführende Informationen zur Konfiguration dieser Aktivität finden Sie in [diesem Abschnitt](../../automating/using/transfer-file.md).

  ![](assets/rtcdp-transfer-file.png)

Im folgenden Workflow werden beispielsweise regelmäßig Protokolle in eine CSV-Datei extrahiert und anschließend an einen Speicherort übertragen.

![](assets/aep-export.png)

Beispiele für Daten-Management-Workflows sind im Abschnitt [Workflow-Anwendungsfälle](../../automating/using/about-workflow-use-cases.md#management) verfügbar.

Verwandte Themen:

* [Datenverwaltungsaktivitäten](../../automating/using/about-data-management-activities.md)
* [Über den Datenimport und -export](../../automating/using/about-data-import-and-export.md)


## Speicherort als Quelle verbinden

Die wichtigsten Schritte zum Verbinden Ihres Speicherorts auf Amazon Storage Service (S3) oder Azure Blob als **Quelle** in Adobe Experience Platform sind unten aufgeführt. Ausführliche Informationen zu jedem dieser Schritte finden Sie in der [Dokumentation zu Quell-Connectoren](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=de).

1. Erstellen Sie in Adobe Experience Platform im Menü **[!UICONTROL Quellen]** eine Verbindung zu Ihrem Speicherort:

   * [Erstellen einer Amazon S3-Quellverbindung](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/s3.html?lang=de)
   * [Azure Blob-Connector](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/cloud-storage/blob.html?lang=de)

   >[!NOTE]
   >
   >Beim Speicherort kann es sich um Amazon S3, SFTP mit Kennwort, SFTP mit SSH-Schlüssel oder Azure Blob handeln. Die bevorzugte Methode zum Senden von Daten an Adobe Campaign ist Amazon S3 oder Azure Blob:

   ![](assets/rtcdp-connector.png)

1. Konfigurieren Sie einen Datenfluss für eine Cloud-Speicherplatz-Batch-Verbindung. Ein Datenfluss ist eine geplante Aufgabe, mit der Daten vom Speicherort abgerufen und in einen Adobe Experience Platform-Datensatz aufgenommen werden. Mit diesen Schritten können Sie die Datenaufnahme an Ihrem Speicherort konfigurieren, einschließlich der Datenauswahl und der Zuordnung der CSV-Felder zu einem XDM-Schema.

   Ausführliche Informationen finden Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/cloud-storage.html?lang=de).

   ![](assets/rtcdp-map-xdm.png)

1. Nachdem die Quelle konfiguriert wurde, importiert Adobe Experience Platform die Datei von dem von Ihnen angegebenen Speicherort.

   Dieser Vorgang kann je nach Bedarf geplant werden. Es wird empfohlen, den Export abhängig von der Auslastung der Instanz bis zu 6-mal täglich durchzuführen.

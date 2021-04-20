---
solution: Campaign Standard
product: campaign
title: Adobe Experience Platform-Audiencen in die Kampagne integrieren
description: Erfahren Sie, wie Sie Adobe Experience Platform-Audiencen in Campaign Standard aufnehmen.
audience: integrating
content-type: reference
feature: Sources and Destinations
role: Data Architect
level: Intermediate
translation-type: tm+mt
source-git-commit: 894d691f1df3a613bacc74e149e5fdf7f4531d92
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 3%

---


# Adobe Experience Platform-Audiencen in Kampagne {#destinations} einbinden

Um Adobe Experience Platform-Audiencen in die Kampagne zu integrieren und sie in Ihrer Workflows zu verwenden, müssen Sie zunächst das Adobe Campaign als Adobe Experience Platform **Ziel** verbinden und es mit dem zu exportierenden Segment konfigurieren.

Nachdem das Ziel konfiguriert wurde, werden die Daten an den Speicherort Ihrer Datenspeicherung exportiert und Sie müssen in Campaign Standard einen eigenen Arbeitsablauf erstellen, um die Daten zu erfassen.

## Adobe Campaign als Ziel verbinden

Konfigurieren Sie auf der Adobe Experience-Plattform eine Verbindung mit Adobe Campaign, indem Sie einen Speicherort für die Datenspeicherung für die exportierten Segmente auswählen. Mit diesen Schritten können Sie auch die zu exportierenden Segmente auswählen und zusätzliche XDM-Felder angeben, die einbezogen werden sollen.

Weitere Informationen finden Sie in der [Dokumentation zu Zielen](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/email-marketing/adobe-campaign.html).

Nachdem das Ziel konfiguriert wurde, erstellt Adobe Experience Platform eine tabulatorgetrennte .txt- oder .csv-Datei am Speicherort der Datenspeicherung, den Sie bereitgestellt haben. Dieser Vorgang wird einmal pro 24 Stunden geplant und ausgeführt.

Sie können jetzt einen Campaign Standard-Workflow konfigurieren, um das Segment in Kampagne zu erfassen.

## Erstellen eines Importarbeitsablaufs in Campaign Standard

Nachdem Campaign Standard als Ziel konfiguriert wurde, müssen Sie einen dedizierten Arbeitsablauf erstellen, um die Datei zu importieren, die von Adobe Experience Platform exportiert wurde.

Dazu müssen Sie eine **[!UICONTROL Übertragungsdatei]**-Aktivität hinzufügen und konfigurieren. Weitere Informationen zum Konfigurieren dieser Aktivität finden Sie in [diesem Abschnitt](../../automating/using/transfer-file.md).

![](assets/rtcdp-transfer-file.png)

Anschließend können Sie Ihren Workflow entsprechend Ihren Anforderungen erstellen (aktualisieren Sie die Datenbank mit den Segmentdaten, senden Sie einen Kanal-übergreifenden Versand an das Segment usw.)

Beispielsweise lädt der unten stehende Arbeitsablauf die Datenspeicherung täglich von Ihrem Speicherort herunter und aktualisiert dann die Kampagne-Datenbank mit den Segmentdaten.

![](assets/rtcdp-workflow.png)

Beispiele für Workflows sind im Abschnitt [Workflows Anwendungsfälle](../../automating/using/about-workflow-use-cases.md#management) verfügbar.

Verwandte Themen:

* [Datenverwaltungsaktivitäten](../../automating/using/about-data-management-activities.md)
* [Über den Datenimport und -export](../../automating/using/about-data-import-and-export.md)

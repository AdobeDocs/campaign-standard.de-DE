---
title: Verwalten von Adobe Experience Platform-Zielgruppen
description: Erfahren Sie, wie Sie Adobe Experience Platform in Campaign Standard verwalten.
page-status-flag: never-activated
uuid: b3996642-96ec-489e-b146-c8c2cb52aa32
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
discoiquuid: 750ecd8d-67a5-4180-bfec-2a8e3098c812
context-tags: audience,wizard;audience,overview;delivery,audience,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: ff3b41589f47e7697a69bb68824aefd4d9036793

---


# Verwalten von Adobe Experience Platform-Zielgruppen {#about-audiences}

>[!IMPORTANT]
>
>Der Zielgruppen-Zieldienst befindet sich derzeit in der Betaphase, die häufig ohne Vorankündigung aktualisiert werden kann. Kunden müssen auf Azurblau gehostet werden (derzeit nur in der Beta-Version für Nordamerika), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an den Adobe-Kundendienst, wenn Sie Zugriff haben möchten.

## Zugriff auf Zielgruppen der Adobe Experience Platform

Um auf den Segmentaufbau für die Adobe Experience Platform zuzugreifen, navigieren Sie zur Karte **[!UICONTROL Zielgruppen]**auf der Homepage von Campaign Standard (oder zum Link**[!UICONTROL  Zielgruppen]** in der Kopfzeile) und wählen Sie dann die Option **[!UICONTROL Adobe Experience Platform]**.

![](assets/aep_audiences_access.png)

Sie werden zunächst zur Segmentlistenseite von Adobe Experience Platform weitergeleitet, auf der bereits vorhandene Adobe Experience Platform-Segmente zur weiteren Bearbeitung aufgerufen werden können.

Es stehen eine Suchleiste und ein Filter zur Verfügung, mit denen Sie das gewünschte Segment für die Adobe Experience Platform finden können.

![](assets/aep_audiences_list.png)

## Erstellen von Adobe Experience Platform-Zielgruppen

Gehen Sie wie folgt vor, um eine Adobe Experience Platform-Zielgruppe direkt in Campaign Standard zu erstellen:

1. Klicken Sie auf der Segmentlistenseite von Adobe Experience Platform auf die Schaltfläche **[!UICONTROL Neue Zielgruppe]**in der rechten Ecke.

   ![](assets/aep_audiences_creation_create.png)

1. Der einheitliche Segmentaufbau sollte jetzt in Ihrer Arbeitsfläche angezeigt werden. Damit können Sie ein Segment mithilfe von Daten aus Adobe Experience Platform erstellen, die letztendlich zur Erstellung Ihrer Zielgruppe verwendet werden.

1. Benennen Sie das Segment im rechten Bereich und geben Sie eine Beschreibung ein (optional).

   ![](assets/aep_audiences_creation_edit_name.png)

1. Um ein Segment erfolgreich zu erstellen, müssen Sie eine **Zusammenführungsrichtlinie** auswählen, die Ihrem Marketingzweck für dieses Segment entspricht.

   Im Einstellungsbereich ist eine Plattform-Standardrichtlinie für die Zusammenführung ausgewählt. Weitere Informationen zu Zusammenführungsrichtlinien finden Sie im entsprechenden Abschnitt im [Segment Builder-Benutzerhandbuch](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/segmentation/segment-builder-guide.md).

   ![](assets/aep_audiences_mergepolicy.png)

1. Definieren Sie die Regeln, die die Profile identifizieren, die in Ihrer Zielgruppe abgerufen werden sollen.

   Ziehen Sie dazu die gewünschten Attribute und/oder Ereignisse aus dem linken Bereich in den Arbeitsbereich, definieren Sie die entsprechenden Regeln und klicken Sie dann auf die Schaltfläche Segment ****erstellen, um das Segment zu speichern (siehe[Verwenden des einheitlichen Segmentaufbaus](../../audiences/using/aep-using-segment-builder.md)).

   ![](assets/aep_audiences_creation_query.png)

Die Zielgruppe kann jetzt aktiviert werden. Sie können sie als Ziel für Ihre Kampagnen verwenden (siehe [Targeting von Adobe Experience Platform-Zielgruppen](../../automating/using/aep-targeting-audiences.md)).

## Audiences ändern

Um eine Zielgruppe zu bearbeiten, öffnen Sie sie und ändern Sie die Regeln nach Bedarf in der Benutzeroberfläche des einheitlichen Segmentaufbaus (siehe [Verwenden des einheitlichen Segmentaufbaus](../../audiences/using/aep-using-segment-builder.md)).

Klicken Sie nach Abschluss der Änderungen auf die Schaltfläche Segment **[!UICONTROL speichern]**, um Ihre Zielgruppe zu aktualisieren.

![](assets/aep_audiences_editing.png)

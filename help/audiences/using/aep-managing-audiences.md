---
title: Adobe Experience Platform-Audiences verwalten
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
source-git-commit: e1fa546313e8d543685ef30a072ae2d97c5bf236

---


# Adobe Experience Platform-Audiences verwalten {#about-audiences}

>[!IMPORTANT]
>
>Der Audience Destination Service befindet sich derzeit in der Betaphase, die häufig ohne Vorankündigung aktualisiert werden kann. Kunden müssen auf Azure gehostet werden (derzeit nur für Nordamerika in der Betaphase), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an die Adobe-Kundenunterstützung, wenn Sie Zugriff haben möchten.

## Zugriff auf Adobe Experience Platform-Audiencen

Um auf den Segmentaufbau für die Adobe Experience Platform zuzugreifen, navigieren Sie zur **[!UICONTROL Audiences]** Karte auf der Startseite des Campaign Standards (oder zum **[!UICONTROL Audiences]** Link in der Kopfzeile) und wählen Sie dann die **[!UICONTROL Adobe Experience Platform]** Umgebung aus.

![](assets/aep_audiences_access.png)

Sie werden zunächst zur Segmentseite der Adobe Experience Platform weitergeleitet, auf der bereits vorhandene Adobe Experience Platform-Listen zur weiteren Bearbeitung aufgerufen werden können.

Es stehen eine Suchleiste und ein Filter zur Verfügung, die Ihnen bei der Suche nach dem gewünschten Segment für die Adobe Experience Platform helfen.

![](assets/aep_audiences_list.png)

## Erstellen von Adobe Experience Platform-Audiencen

Gehen Sie wie folgt vor, um eine Adobe Experience Platform-Audience direkt in Campaign Standard zu erstellen:

1. Klicken Sie auf der Seite &quot;Liste der Segmente für Adobe Experience Platform&quot;auf die **[!UICONTROL New audience]** Schaltfläche in der rechten Ecke.

   ![](assets/aep_audiences_creation_create.png)

1. Der einheitliche Segmentaufbau sollte jetzt in Ihrer Arbeitsfläche angezeigt werden. Damit können Sie ein Segment mithilfe von Daten aus Adobe Experience Platform erstellen, die letztendlich zur Erstellung Ihrer Audience verwendet werden.

1. Benennen Sie das Segment im rechten Bereich und geben Sie eine Beschreibung ein (optional).

   ![](assets/aep_audiences_creation_edit_name.png)

1. Um ein Segment erfolgreich zu erstellen, müssen Sie eine **Zusammenführungsrichtlinie** auswählen, die Ihrem Marketingzweck für dieses Segment entspricht.

   Im Einstellungsbereich ist eine Plattform-Standardrichtlinie für die Zusammenführung ausgewählt. Weitere Informationen zu Zusammenführungsrichtlinien finden Sie im entsprechenden Abschnitt im [Segment Builder-Benutzerhandbuch](https://docs.adobe.com/content/help/en/experience-platform/segmentation/ui/overview.html).

   ![](assets/aep_audiences_mergepolicy.png)

1. Definieren Sie die Regeln, die die Profil identifizieren, die in Ihrer Audience abgerufen werden sollen.

   Ziehen Sie dazu die gewünschten Attribute und/oder Ereignis aus dem linken Bereich in den Arbeitsbereich, definieren Sie die entsprechenden Regeln und klicken Sie dann auf die **[!UICONTROL Create segment]** Schaltfläche zum Speichern des Segments (siehe [Verwenden des Segmentaufbaus](../../audiences/using/aep-using-segment-builder.md)).

   ![](assets/aep_audiences_creation_query.png)

Die Audience kann jetzt aktiviert werden. Sie können sie als Zielgruppe für Ihre Kampagnen verwenden (siehe [Targeting von Adobe Experience Platform-Audiencen](../../automating/using/aep-targeting-audiences.md)).

## Audiences ändern

Um eine Audience zu bearbeiten, öffnen Sie sie und ändern Sie die Regeln nach Bedarf in der Benutzeroberfläche des einheitlichen Segmentaufbaus (siehe [Verwenden des einheitlichen Segmentaufbaus](../../audiences/using/aep-using-segment-builder.md)).

Klicken Sie nach Abschluss der Änderungen auf die **[!UICONTROL Save segment]** Schaltfläche, um Ihre Audience zu aktualisieren.

![](assets/aep_audiences_editing.png)

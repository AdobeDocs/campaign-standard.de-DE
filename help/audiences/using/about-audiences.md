---
title: Über Audiences
description: Hier erfahren Sie, wie Sie Audiences mithilfe einer Abfrage, einer Liste oder einer Datei erstellen oder aus Adobe Experience Cloud importieren.
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
source-git-commit: 68e825bc3b6b7f94f61875e7da2bc8f63f06d9cb

---


# Über Audiences{#about-audiences}

Eine Audience ist eine Liste mit Profilen basierend auf Regeln und Attributen.

Audiences können in Adobe Campaign manuell mittels Abfragen oder automatisch mittels dedizierter Workflows erstellt werden. Außerdem besteht die Möglichkeit zur Verwendung von freigegebenen Zielgruppen aus Adobe Experience Cloud. Alle sind in einer Liste zusammengefasst, auf die entweder über die **[!UICONTROL Audiences]**-Karte der Adobe-Campaign-Startseite oder über den **[!UICONTROL Audiences]** Audiences-Link zugegriffen werden kann.

![](assets/audience_1.png)

Adobe Campaign bietet die Möglichkeit, mit verschiedenen Audience-Typen zu arbeiten. Der Typ einer Audience entspricht der Art ihrer Erstellung:

* **[!UICONTROL Query]**: gibt an, dass die Audience aus einer [Abfrage](../../automating/using/editing-queries.md#about-query-editor) über Daten aus der Adobe Campaign-Datenbank aus der Liste der Audiencen erstellt wurde. Über Abfragen definierte Audiences werden bei jeder Verwendung erneut berechnet.
* **[!UICONTROL List]**: gibt an, dass die Audience eine feste Liste von Profilen ist. Diese Listen werden in [Workflows](../../automating/using/get-started-workflows.md) erstellt, wenn bei Speicherung der Audience die Dimension der Daten bekannt ist. For example, after targeting activities (especially **[!UICONTROL Query]** ) or after the reconciliation of data imported from a file.
* **[!UICONTROL File]**: gibt an, dass die Audience direkt aus einem Arbeitsablauf für den [Dateiimport](../../automating/using/load-file.md) erstellt wurde und dass die Datendimension beim Speichern der Audience unbekannt war.
* **[!UICONTROL Experience Cloud]** – bedeutet, dass die Audience auf einer aus Adobe Experience Cloud importierten freigegebenen Zielgruppe beruht. Diese Option ist nur dann verfügbar, wenn die Funktion der Zielgruppenfreigabe konfiguriert wurde. Weitere Informationen finden Sie in [Importieren einer Zielgruppe aus Adobe Experience Cloud](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md#importing-an-audience).

![](assets/audience_type_selection.png)

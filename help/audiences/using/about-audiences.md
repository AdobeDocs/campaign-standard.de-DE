---
title: Über Audiences
seo-title: Über Audiences
description: Über Audiences
seo-description: Hier erfahren Sie, wie Sie Audiences mithilfe einer Abfrage, einer Liste oder einer Datei erstellen oder aus Adobe Experience Cloud importieren.
page-status-flag: nie aktiviert
uuid: b 3996642-96 ec -489 e-b 146-c 8 c 2 cb 52 aa 32
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Zielgruppen
content-type: Referenz
topic-tags: managing-audiences
discoiquuid: 750 ecd 8 d -67 a 5-4180-bfec -2 a 8 e 3098 c 812
context-tags: Zielgruppe, Assistent; audience, overview; Bereitstellung, Zielgruppe, zurück
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6a877d878f01fa1e541dc20b8b0941602113d15b

---


# Über Audiences{#about-audiences}

Eine Audience ist eine Liste mit Profilen basierend auf Regeln und Attributen.

Audiences können in Adobe Campaign manuell mittels Abfragen oder automatisch mittels dedizierter Workflows erstellt werden. Außerdem besteht die Möglichkeit zur Verwendung von freigegebenen Zielgruppen aus Adobe Experience Cloud. Alle Audiences sind in einer Liste zusammengefasst, auf die entweder über die **[!UICONTROL Audiences]**-Karte der Adobe-Campaign-Startseite oder über den **Audiences]-Link zugegriffen werden kann.[!UICONTROL **

![](assets/audience_1.png)

Adobe Campaign bietet die Möglichkeit, mit verschiedenen Audience-Typen zu arbeiten. Der Typ einer Audience entspricht der Art ihrer Erstellung:

* **[!UICONTROL Abfrage]**: bedeutet, dass die Audience mithilfe einer [Abfrage](../../automating/using/editing-queries.md#about-query-editor) über die in der Adobe-Campaign-Datenbank enthaltenen Daten, ausgehend von der Liste der Audiences, erstellt wurde. Über Abfragen definierte Audiences werden bei jeder Verwendung erneut berechnet.
* **[!UICONTROL Liste]** - bedeutet, dass es sich bei der Audience um eine feststehende Liste von Profilen handelt. Diese Listen werden in [Workflows](../../automating/using/discovering-workflows.md) erstellt, wenn bei Speicherung der Audience die Dimension der Daten bekannt ist. For example, after targeting activities (especially **[!UICONTROL Query]** ) or after the reconciliation of data imported from a file.
* **[!UICONTROL Datei]** – bedeutet, dass die Audience direkt durch [Importieren einer Datei](../../automating/using/load-file.md) in einen Workflow erstellt wurde und dass die Dimension der Daten bei Speicherung der Audience unbekannt war.
* **[!UICONTROL Experience Cloud]** – bedeutet, dass die Audience auf einer aus Adobe Experience Cloud importierten freigegebenen Zielgruppe beruht. Diese Option ist nur dann verfügbar, wenn die Funktion der Zielgruppenfreigabe konfiguriert wurde. Weitere Informationen finden Sie in [Importieren einer Zielgruppe aus Adobe Experience Cloud](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md#importing-an-audience).

![](assets/audience_type_selection.png)


---
title: Über Zielgruppen
description: Hier erfahren Sie, wie Sie Zielgruppen mithilfe einer Abfrage, einer Liste oder einer Datei erstellen oder aus Adobe Experience Cloud importieren.
audience: audiences
content-type: reference
topic-tags: managing-audiences
context-tags: audience,wizard;audience,overview;delivery,audience,back
feature: Audiences
role: User
level: Beginner
exl-id: f99987d8-b1bf-4ec7-885c-fb511f4168ac
TQID: https://experienceleague.adobe.com/NPcDi1kh8Ye1Y14CAwVxBLW-0qwHnpFRUQ2WYj7BJbI
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 257
ht-degree: 100%

---

# Über Zielgruppen{#about-audiences}

Eine Zielgruppe ist eine Liste mit Profilen basierend auf Regeln und Attributen.

Zielgruppen können in Adobe Campaign manuell mittels Abfragen oder automatisch mittels dedizierter Workflows erstellt werden. Außerdem besteht die Möglichkeit zur Verwendung von freigegebenen Zielgruppen aus Adobe Experience Cloud. Alle Zielgruppen sind in einer Liste zusammengefasst, auf die entweder über die **[!UICONTROL Zielgruppen]**-Karte der Adobe Campaign-Startseite oder über den **[!UICONTROL Zielgruppen]**-Link zugegriffen werden kann.

![](assets/audience_1.png)

Adobe Campaign bietet die Möglichkeit, mit verschiedenen Zielgruppe-Typen zu arbeiten. Der Typ einer Zielgruppe entspricht der Art ihrer Erstellung:

* **[!UICONTROL Abfrage]**: bedeutet, dass die Zielgruppe mithilfe einer [Abfrage](../../automating/using/editing-queries.md#about-query-editor) von in der Adobe Campaign-Datenbank enthaltenen Daten über die Liste der Zielgruppen erstellt wurde. Über Abfragen definierte Zielgruppen werden bei jeder Verwendung erneut berechnet.
* **[!UICONTROL Liste]** – bedeutet, dass es sich bei der Zielgruppe um eine feststehende Liste von Profilen handelt. Diese Listen werden in [Workflows](../../automating/using/get-started-workflows.md) erstellt, wenn bei Speicherung der Zielgruppe die Dimension der Daten bekannt ist. Dies kann beispielsweise nach Zielgruppenbestimmungsaktivitäten (insbesondere **[!UICONTROL Abfragen]**) oder nach der Abstimmung von aus einer Datei importierten Daten geschehen.
* **[!UICONTROL Datei]** – bedeutet, dass die Zielgruppe direkt durch [Importieren einer Datei](../../automating/using/load-file.md) in einen Workflow erstellt wurde und dass die Dimension der Daten bei Speicherung der Zielgruppe unbekannt war.
* **[!UICONTROL Experience Cloud]** – bedeutet, dass die Audience auf einer aus Adobe Experience Cloud importierten freigegebenen Zielgruppe beruht. Diese Option ist nur dann verfügbar, wenn die Funktion der Zielgruppenfreigabe konfiguriert wurde. Weitere Informationen finden Sie in [Importieren einer Zielgruppe aus Adobe Experience Cloud](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md#importing-an-audience).

![](assets/audience_type_selection.png)

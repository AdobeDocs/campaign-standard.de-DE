---
title: Aktive Profile
description: Sie können auf einen eigenen Bericht mit Kundenmetriken zugreifen und aktive Profile in Ihrer Campaign-Datenbank darstellen.
page-status-flag: never-activated
uuid: ee8ac493-c297-49ca-aed4-3976d8a685a4
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-profiles
discoiquuid: e029213f-0b65-41b1-8adf-34fa813b0c70
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4575c1152f1a33ff18b2200151346cc6e56b45fa
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 72%

---


# Aktive Profile{#active-profiles}

Adobe Campaign erstellt einen Bericht, in dem die Anzahl der aktiven Profile dargestellt wird. Dieser Bericht hat nur informativen Charakter und keine direkte Auswirkung auf die Rechnungsstellung. Nur Administratoren haben Zugriff auf diesen Bericht. Er kann unter **[!UICONTROL Administration > Kundenmetriken abgerufen werden]**.

![](assets/audience_active_profiles1.png)

Mit dem technischen Workflow **[!UICONTROL Rechnungsstellung]** wird jeden Monat ein Bericht erzeugt, in dem die Anzahl der aktiven Profile aufgeführt wird, die in den letzten zwölf Monaten angesprochen wurden.

Die Profile, die während der Versandvorbereitung ausgeschlossen wurden (Typologieregeln, Quarantänen), werden nicht berücksichtigt. Ein Profil, das mehrere Sendungen erhalten hat, wird nur einmal gezählt. Am Ende des Berichts finden Sie die Liste der aktiven Profile für jede Zielgruppendimension.

![](assets/audience_active_profiles2.png)

Wenn Sie auf AWS gehostet werden und Campaign Standard aus Build 10368 verwenden, können Sie auch die Anzahl der aktiven Profil, die auf Ihren Instanzen verwendet werden, direkt über die Systemsteuerung überwachen. For more on this, refer to the [Control Panel documentation](https://docs.adobe.com/content/help/en/control-panel/using/performance-monitoring/active-profiles-monitoring.html).

---
title: Inkrementelle Abfrage über Abonnenten eines Dienstes
description: Im folgenden Beispiel wird erläutert, wie eine Inkrementelle Abfrage-Aktivität zum Filtern von Abonnenten zu einem Dienst konfiguriert wird.
page-status-flag: never-activated
uuid: 73b42422-e815-43ef-84c0-97c4433ccc98
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 80961e73-42ec-463a-8496-cff69fab0475
context-tags: incremental,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7ffa48365875883a98904d6b344ac005afe26e18
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 81%

---


# Incremental query on subscribers to a service {#example--incremental-query-on-subscribers-to-a-service}

Im folgenden Beispiel wird die Konfiguration der Aktivität **[!UICONTROL Inkrementelle Abfrage]** illustriert, die der Filterung der Profile der Adobe-Campaign-Datenbank dient, die Abonnenten des Diensts **Running-Newsletter** sind, um diesen eine Willkommens-E-Mail mit einem Sonderangebotscode zu senden.

Der Workflow besteht aus folgenden Aktivitäten:

![](assets/incremental_query_example1.png)

* Eine [Planung](../../automating/using/scheduler.md), damit der Workflow jeden Montag um 6 Uhr ausgeführt wird.

   ![](assets/incremental_query_example2.png)

* Eine [Inkrementelle Abfrage](../../automating/using/incremental-query.md), die bei der ersten Ausführung zunächst den Abruf aller aktuellen Abonnenten, dann bei den folgenden Ausführungen nur den Abruf der im Laufe der Woche dazugekommenen, neuen Abonnenten ermöglicht.

   ![](assets/incremental_query_example3.png)

* Ein [E-Mail-Versand. ](../../automating/using/email-delivery.md) Der Workflow wird einmal pro Woche ausgeführt, Sie haben jedoch die Möglichkeit, gesendete E-Mails sowie Ergebnisse pro Monat zu aggregieren, um so beispielsweise Berichte für einen ganzen Monat anstatt nur auf wöchentlicher Basis zu erzeugen.

   Wählen Sie hierzu an dieser Stelle die Erstellung einer **[!UICONTROL E-Mail zum wiederkehrenden Versand]** aus, die E-Mails und Ergebnisse **[!UICONTROL Pro Monat]** zusammenfasst.

   Definieren Sie den Inhalt Ihrer E-Mail und fügen Sie den Willkommenscode für ein Sonderangebot ein. Weitere Informationen hierzu finden Sie unter [Definieren von E-Mail-Inhalten](../../designing/using/personalization.md) .

Starten Sie nun die Ausführung des Workflows. Jede Woche erhalten neue Abonnenten die Willkommens-E-Mail mit dem Sonderangebotscode.

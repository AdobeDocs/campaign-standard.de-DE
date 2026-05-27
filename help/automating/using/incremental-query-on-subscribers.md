---
title: Inkrementelle Abfrage bezüglich Dienst-Abonnenten
description: Im folgenden Beispiel wird gezeigt, wie eine inkrementelle Abfrageaktivität konfiguriert wird, um Abonnenten eines Dienstes zu filtern.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: incremental,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: c80ed1f6-ad8a-4448-a6df-b9881327228a
TQID: https://experienceleague.adobe.com/MHB1ETCecN9gQq51bSii-keTyFaYof0JtAyckFSCKQE
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 218
ht-degree: 100%

---

# Inkrementelle Abfrage bezüglich Service-Abonnenten {#example--incremental-query-on-subscribers-to-a-service}

Im folgenden Beispiel wird die Konfiguration der Aktivität **[!UICONTROL Inkrementelle Abfrage]** illustriert, die der Filterung der Profile der Adobe Campaign-Datenbank dient, die Abonnenten des Diensts **Running-Newsletter** sind, um diesen eine Begrüßungs-E-Mail mit einem Sonderangebots-Code zu senden.

Der Workflow besteht aus folgenden Aktivitäten:

![](assets/incremental_query_example1.png)

* Eine [Planung](../../automating/using/scheduler.md), damit der Workflow jeden Montag um 6 Uhr ausgeführt wird.

  ![](assets/incremental_query_example2.png)

* Eine [Inkrementelle Abfrage](../../automating/using/incremental-query.md), die bei der ersten Ausführung zunächst den Abruf aller aktuellen Abonnenten, dann bei den folgenden Ausführungen nur den Abruf der im Laufe der Woche dazugekommenen, neuen Abonnenten ermöglicht.

  ![](assets/incremental_query_example3.png)

* Ein [E-Mail-Versand. ](../../automating/using/email-delivery.md) Der Workflow wird einmal pro Woche ausgeführt, Sie haben jedoch die Möglichkeit, gesendete E-Mails sowie Ergebnisse pro Monat zu aggregieren, um so beispielsweise Berichte für einen ganzen Monat anstatt nur auf wöchentlicher Basis zu erzeugen.

  Wählen Sie hierzu an dieser Stelle die Erstellung einer **[!UICONTROL E-Mail zum wiederkehrenden Versand]** aus, die E-Mails und Ergebnisse **[!UICONTROL pro Monat]** zusammenfasst.

  Definieren Sie den Inhalt Ihrer E-Mail und fügen Sie den Willkommenscode für ein Sonderangebot ein. Weitere Informationen hierzu finden Sie in den Abschnitten zum [Definieren von E-Mail-Inhalten](../../designing/using/personalization.md).

Starten Sie nun die Ausführung des Workflows. Jede Woche erhalten neue Abonnenten die Begrüßungs-E-Mail mit dem Sonderangebotscode.

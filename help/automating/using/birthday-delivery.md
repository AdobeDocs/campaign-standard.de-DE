---
title: Versand zum Geburtstag
description: Das folgende Beispiel zeigt einen Geburtstags-Workflow. Jeden Tag wird eine E-Mail an alle Profile gesendet, die Geburtstag haben.
audience: automating
content-type: reference
topic-tags: channel-activities
context-tags: delivery,workflow,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 535ddbce-d8ba-4578-9e37-10604291c95d
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 100%

---

# Versand zum Geburtstag {#birthday-delivery}

![](assets/wkf_delivery_example_1.png)

Das folgende Beispiel zeigt einen Geburtstags-Workflow. Jeden Tag wird eine E-Mail an alle Profile gesendet, die Geburtstag haben.

Gehen Sie wie folgt vor, um den Workflow zu erstellen:

* Eine [Planung](../../automating/using/scheduler.md) startet den Workflow täglich um 8 Uhr.

  ![](assets/wkf_delivery_example_2.png)

* Die Aktivität [Abfrage](../../automating/using/query.md) ermöglicht es, bei jeder Ausführung des Workflows die Profile zu berechnen, die eine E-Mail-Adresse angegeben haben und deren Geburtstag auf den aktuellen Tag fällt. Der Geburtstagsfilter ist standardmäßig im Abfragetool enthalten.

  ![](assets/wkf_delivery_example_3.png)

* Der [E-Mail-Versand](../../automating/using/email-delivery.md) ist wiederkehrend. die Sendungen werden pro Monat aggregiert. Auf diese Weise sind alle innerhalb eines Monats gesendeten E-Mails in einer einzigen Ansicht enthalten. Innerhalb eines Jahres werden folglich 365 Sendungen ausgeführt, die jedoch innerhalb der Adobe Campaign-Benutzeroberfläche in nur 12 Ansichten (auch **wiederkehrende Ausführungen** genannt) zusammengefasst werden. Der Verlauf und die Berichte zeigen monatliche Zusammenfassungen und nicht jeden einzelnen Versand.

  ![](assets/wkf_delivery_example_4.png)

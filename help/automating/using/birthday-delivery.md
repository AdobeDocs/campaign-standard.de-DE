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
TQID: https://experienceleague.adobe.com/LXiYfz5VXaY7j0pOHWUCGJzp5F4bCsSCmFzEqsQG18E
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 174
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

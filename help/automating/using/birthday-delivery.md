---
solution: Campaign Standard
product: campaign
title: Versand zum Geburtstag
description: Das folgende Beispiel zeigt einen Geburtstags-Workflow. Jeden Tag wird eine E-Mail an alle Profile gesendet, die Geburtstag haben.
audience: automating
content-type: reference
topic-tags: channel-activities
context-tags: delivery,workflow,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 535ddbce-d8ba-4578-9e37-10604291c95d
translation-type: ht
source-git-commit: e7fdaa4b1d77afdae8004a88bbe41bbbe75a3f3c
workflow-type: ht
source-wordcount: '173'
ht-degree: 100%

---

# Versand zum Geburtstag {#birthday-delivery}

![](assets/wkf_delivery_example_1.png)

Das folgende Beispiel zeigt einen Geburtstags-Workflow. Jeden Tag wird eine E-Mail an alle Profile gesendet, die Geburtstag haben.

Gehen Sie wie folgt vor, um den Workflow zu erstellen:

* Eine [Planung](../../automating/using/scheduler.md) startet den Workflow täglich um 8 Uhr.

   ![](assets/wkf_delivery_example_2.png)

* Die auf die Planung folgende [Abfrage](../../automating/using/query.md) ruft alle Profile aus der Datenbank ab, die am aktuellen Datum Geburtstag haben und deren E-Mail-Adresse bekannt ist. Der Geburtstagsfilter ist standardmäßig im Abfragetool enthalten.

   ![](assets/wkf_delivery_example_3.png)

* Der [E-Mail-Versand](../../automating/using/email-delivery.md) ist wiederkehrend. die Sendungen werden pro Monat aggregiert. Auf diese Weise sind alle innerhalb eines Monats gesendeten E-Mails in einer einzigen Ansicht enthalten. Innerhalb eines Jahres werden folglich 365 Sendungen ausgeführt, die jedoch innerhalb der Adobe-Campaign-Benutzeroberfläche in nur 12 Ansichten (auch **wiederkehrende Ausführungen** genannt) zusammengefasst werden. Der Verlauf und die Berichte zeigen monatliche Zusammenfassungen und nicht jeden einzelnen Versand.

   ![](assets/wkf_delivery_example_4.png)

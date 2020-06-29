---
title: Geburtstag, Versand
description: Das folgende Beispiel zeigt einen Geburtstags-Workflow. Jeden Tag wird eine E-Mail an alle Profile gesendet, die Geburtstag haben.
page-status-flag: never-activated
uuid: 7de53431-84ae-4d21-8361-2775ad314ed2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: channel-activities
discoiquuid: 5f288cf6-f8ff-4ac9-9c1a-8010260554bb
context-tags: delivery,workflow,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7ffa48365875883a98904d6b344ac005afe26e18
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 90%

---


# Geburtstag, Versand {#birthday-delivery}

![](assets/wkf_delivery_example_1.png)

Das folgende Beispiel zeigt einen Geburtstags-Workflow. Jeden Tag wird eine E-Mail an alle Profile gesendet, die Geburtstag haben.

Gehen Sie zum Erstellen des Workflows wie folgt vor:

* Eine [Planung](../../automating/using/scheduler.md) startet den Workflow täglich um 8 Uhr.

   ![](assets/wkf_delivery_example_2.png)

* Die auf die Planung folgende [Abfrage](../../automating/using/query.md) ruft alle Profile aus der Datenbank ab, die am aktuellen Datum Geburtstag haben und deren E-Mail-Adresse bekannt ist. Der Geburtstagsfilter ist standardmäßig im Abfragetool enthalten.

   ![](assets/wkf_delivery_example_3.png)

* The [Email delivery](../../automating/using/email-delivery.md) is recurring. die Sendungen werden pro Monat aggregiert. Auf diese Weise sind alle innerhalb eines Monats gesendeten E-Mails in einer einzigen Ansicht enthalten. Innerhalb eines Jahres werden folglich 365 Sendungen ausgeführt, die jedoch innerhalb der Adobe-Campaign-Benutzeroberfläche in nur 12 Ansichten (auch **wiederkehrende Ausführungen** genannt) zusammengefasst werden. Der Verlauf und die Berichte zeigen monatliche Zusammenfassungen und nicht jeden einzelnen Versand.

   ![](assets/wkf_delivery_example_4.png)

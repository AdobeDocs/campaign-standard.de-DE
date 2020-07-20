---
title: Vereinigung von zwei eingegrenzten Audiences
description: In diesem Anwendungsfall wird die Vereinigung von zwei "Audience lesen"-Aktivitäten vorgestellt.
page-status-flag: never-activated
uuid: 58c54e71-f4a7-4ae9-80a3-33c379ab1db9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: 674684e5-8830-4d2f-ba97-59ed4ba7422f
context-tags: readAudience,main
internal: n
snippet: y
translation-type: ht
source-git-commit: 7ffa48365875883a98904d6b344ac005afe26e18
workflow-type: ht
source-wordcount: '157'
ht-degree: 100%

---


# Vereinigung von zwei eingegrenzten Audiences {#example--union-on-two-refined-audiences}

In diesem Beispiel werden im Workflow zwei **[!UICONTROL Audience lesen]**-Aktivitäten vereint. Ziel dieses Workflows ist es, eine E-Mail an Gold- oder Silber-Mitglieder zu senden, die zwischen 18 und 30 Jahre alt sind. Spezifische Audiences wurden im System bereits erstellt, um Gold- und Silber-Mitglieder zu erfassen.

Der Workflow setzt sich folgendermaßen zusammen:

![](assets/readaudience_activity_example1.png)

* Eine erste [Audience lesen](../../automating/using/read-audience.md)-Aktivität ruft die Audience der Gold-Mitglieder ab und schränkt sie ein, indem nur Profile zwischen 18 und 30 Jahren ausgewählt werden.
* Eine zweite **[!UICONTROL Audience lesen]**-Aktivität ruft die Audience der Silber-Mitglieder ab und schränkt sie ein, indem nur Profile zwischen 18 und 30 Jahren ausgewählt werden.
* Die Aktivität [Vereinigung](../../automating/using/union.md) fasst die Populationen der beiden **[!UICONTROL Audience lesen]**-Aktivitäten zu einer endgültigen Population zusammen.
* Die Aktivität [E-Mail-Versand](../../automating/using/email-delivery.md) sendet E-Mails an die Population der Aktivität **[!UICONTROL Vereinigung]**.

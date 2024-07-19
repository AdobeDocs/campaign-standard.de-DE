---
title: Vereinigung von zwei eingegrenzten Audiences
description: In diesem Anwendungsfall wird die Vereinigung von zwei "Audience lesen"-Aktivitäten vorgestellt.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: readAudience,main
feature: Workflows
role: Data Architect
level: Intermediate
exl-id: 6261f800-11bd-4b02-a587-49ddb0da240f
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '163'
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

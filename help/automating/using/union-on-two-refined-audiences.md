---
title: Vereinigung von zwei eingegrenzten Zielgruppen
description: In diesem Anwendungsfall wird die Vereinigung von zwei "Zielgruppe lesen"-Aktivitäten vorgestellt.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: readAudience,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 6261f800-11bd-4b02-a587-49ddb0da240f
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: ht
source-wordcount: '163'
ht-degree: 100%

---

# Vereinigung von zwei eingegrenzten Zielgruppen {#example--union-on-two-refined-audiences}

In diesem Beispiel werden im Workflow zwei **[!UICONTROL Zielgruppe lesen]**-Aktivitäten vereint. Ziel dieses Workflows ist es, eine E-Mail an Gold- oder Silber-Mitglieder zu senden, die zwischen 18 und 30 Jahre alt sind. Spezifische Zielgruppen wurden im System bereits erstellt, um Gold- und Silber-Mitglieder zu erfassen.

Der Workflow setzt sich folgendermaßen zusammen:

![](assets/readaudience_activity_example1.png)

* Eine erste [Zielgruppe lesen](../../automating/using/read-audience.md)-Aktivität ruft die Zielgruppe der Gold-Mitglieder ab und schränkt sie ein, indem nur Profile zwischen 18 und 30 Jahren ausgewählt werden.
* Eine zweite **[!UICONTROL Zielgruppe lesen]**-Aktivität ruft die Zielgruppe der Silber-Mitglieder ab und schränkt sie ein, indem nur Profile zwischen 18 und 30 Jahren ausgewählt werden.
* Die Aktivität [Vereinigung](../../automating/using/union.md) fasst die Populationen der beiden **[!UICONTROL Zielgruppe lesen]**-Aktivitäten zu einer endgültigen Population zusammen.
* Die Aktivität [E-Mail-Versand](../../automating/using/email-delivery.md) sendet E-Mails an die Population der Aktivität **[!UICONTROL Vereinigung]**.

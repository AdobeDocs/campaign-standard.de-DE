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
TQID: https://experienceleague.adobe.com/NZA7DqSxrgPvNPfo4dgWvyJaOp-2Ma07MZJuHff3sAA
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 163
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

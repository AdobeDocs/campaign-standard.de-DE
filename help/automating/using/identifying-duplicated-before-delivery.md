---
title: Duplikate vor einem Versand identifizieren
description: Das folgende Beispiel zeigt eine Deduplizierung, mithilfe derer die Duplikate einer Zielgruppe vor dem Versand einer E-Mail ausgeschlossen werden können. Dadurch lässt sich vermeiden, eine Information mehrmals an ein und dasselbe Profil zu schicken.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: dedup,main
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: a09b101b-f76f-4377-9854-1fcffaad4f9a
TQID: https://experienceleague.adobe.com/4t0TujgM3kHTT36-Gy2lmiVQIRMy3OeChAw-Xx5MnWY
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
source-wordcount: 290
ht-degree: 100%

---

# Duplikate vor einem Versand identifizieren {#identifying-duplicates-before-a-delivery}

Das folgende Beispiel zeigt eine Deduplizierung, mithilfe derer die Duplikate einer Zielgruppe vor dem Versand einer E-Mail ausgeschlossen werden können. Dadurch lässt sich vermeiden, eine Information mehrmals an ein und dasselbe Profil zu schicken.

Der Workflow setzt sich folgendermaßen zusammen:

![](assets/deduplication_example_workflow.png)

* [Abfrage](../../automating/using/query.md) zur Bestimmung der Zielgruppe der E-Mail. Im vorliegenden Beispiel zielt der Workflow auf all jene Profile im Alter zwischen 18 und 25 Jahren ab, die seit mehr als einem Jahr in der Kundendatenbank sind.

  ![](assets/deduplication_example_query.png)

* [Deduplizierung](../../automating/using/deduplication.md) zur Identifizierung der aus der vorangehenden Abfrage hervorgehenden Duplikate. Im vorliegenden Beispiel wird für jedes Duplikat ein einziger Datensatz beibehalten. Die Duplikate werden mittels der E-Mail-Adresse identifiziert. Auf diese Weise kann ein E-Mail-Versand nur ein einziges Mal an jede in der Zielgruppenbestimmung enthaltene E-Mail-Adresse gesendet werden.

  Bei der ausgewählten Deduplizierungsmethode handelt es sich um **[!UICONTROL Wert nicht leer]**. Dadurch kann sichergestellt werden, dass es sich bei den im Fall von Duplikaten beibehaltenen Datensätzen vornehmlich um diejenigen handelt, bei denen das Feld **Vorname** ausgefüllt ist. Dies ist insbesondere dann empfehlenswert, wenn der Vorname in den Personalisierungsfeldern des E-Mail-Inhalts verwendet wird.

  Des Weiteren wird eine komplementäre Transition erzeugt, um die Duplikate beizubehalten und sie auflisten zu können.

  ![](assets/deduplication_example_dedup.png)

* [E-Mail-Versand](../../automating/using/email-delivery.md), der im Anschluss an die ausgehende Haupttransition der Deduplizierung platziert wird.
* Die Aktivität [Zielgruppen-Speicherung](../../automating/using/save-audience.md), die im Anschluss an die zusätzliche Transition der Deduplizierung platziert wird, um die Duplikate in einer **Duplikate**-Zielgruppe zu speichern. Diese Zielgruppe kann in der Folge wiederverwendet werden, um ihre Mitglieder direkt von jeglichem E-Mail-Versand auszuschließen.

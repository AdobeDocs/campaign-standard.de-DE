---
solution: Campaign Standard
product: campaign
title: Dubletten vor einem Versand identifizieren
description: Das folgende Beispiel zeigt eine Deduplizierung, mithilfe derer die Dubletten einer Zielgruppe vor dem Versand einer E-Mail ausgeschlossen werden können. Dadurch lässt sich vermeiden, eine Information mehrmals an ein und dasselbe Profil zu schicken.
audience: automating
content-type: reference
topic-tags: targeting-activities
context-tags: dedup,main
translation-type: ht
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: ht
source-wordcount: '287'
ht-degree: 100%

---


# Dubletten vor einem Versand identifizieren {#identifying-duplicates-before-a-delivery}

Das folgende Beispiel zeigt eine Deduplizierung, mithilfe derer die Dubletten einer Zielgruppe vor dem Versand einer E-Mail ausgeschlossen werden können. Dadurch lässt sich vermeiden, eine Information mehrmals an ein und dasselbe Profil zu schicken.

Der Workflow setzt sich folgendermaßen zusammen:

![](assets/deduplication_example_workflow.png)

* [Abfrage](../../automating/using/query.md) zur Bestimmung der Zielgruppe der E-Mail. Im vorliegenden Beispiel zielt der Workflow auf all jene Profile im Alter zwischen 18 und 25 Jahren ab, die seit mehr als einem Jahr in der Kundendatenbank sind.

   ![](assets/deduplication_example_query.png)

* [Deduplizierung](../../automating/using/deduplication.md) zur Identifizierung der aus der vorangehenden Abfrage hervorgehenden Dubletten. Im vorliegenden Beispiel wird für jede Dublette ein einziger Datensatz beibehalten. Die Dubletten werden mittels der E-Mail-Adresse identifiziert. Auf diese Weise kann ein E-Mail-Versand nur ein einziges Mal an jede in der Zielgruppenbestimmung enthaltene E-Mail-Adresse gesendet werden.

   Bei der ausgewählten Deduplizierungsmethode handelt es sich um **[!UICONTROL Wert nicht leer]**. Dadurch kann sichergestellt werden, dass es sich bei den im Fall von Dubletten beibehaltenen Datensätzen vornehmlich um diejenigen handelt, bei denen das Feld **Vorname** ausgefüllt ist. Dies ist insbesondere dann empfehlenswert, wenn der Vorname in den Personalisierungsfeldern des E-Mail-Inhalts verwendet wird.

   Des Weiteren wird eine komplementäre Transition erzeugt, um die Dubletten beizubehalten und sie auflisten zu können.

   ![](assets/deduplication_example_dedup.png)

* [E-Mail-Versand](../../automating/using/email-delivery.md), der im Anschluss an die ausgehende Haupttransition der Deduplizierung platziert wird.
* Die Aktivität [Audience-Speicherung](../../automating/using/save-audience.md), die im Anschluss an die zusätzliche Transition der Deduplizierung platziert wird, um die Dubletten in einer **Dubletten**-Audience zu speichern. Diese Audience kann in der Folge wiederverwendet werden, um ihre Mitglieder direkt von jeglichem E-Mail-Versand auszuschließen.

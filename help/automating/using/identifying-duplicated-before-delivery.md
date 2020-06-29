---
title: Identifizieren von Duplikaten vor einem Versand
description: Das folgende Beispiel zeigt eine Deduplizierung, mithilfe derer die Dubletten einer Zielgruppe vor dem Versand einer E-Mail ausgeschlossen werden können. Dadurch lässt sich vermeiden, eine Information mehrmals an ein und dasselbe Profil zu schicken.
page-status-flag: never-activated
uuid: 11a22a9c-3bfe-4953-8a52-2f4e93c128fb
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: targeting-activities
discoiquuid: e7a5e1e7-4680-46c7-98b8-0a47bb7be2b8
context-tags: dedup,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7ffa48365875883a98904d6b344ac005afe26e18
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 96%

---


# Identifying duplicates before a delivery {#identifying-duplicates-before-a-delivery}

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
* [Audience-Speicherung](../../automating/using/save-audience.md), die im Anschluss an die komplementäre Transition der Deduplizierung platziert wird, um die Dubletten in einer **Dubletten**-Audience zu speichern. Diese Audience kann in der Folge wiederverwendet werden, um ihre Mitglieder direkt von jeglichem E-Mail-Versand auszuschließen.

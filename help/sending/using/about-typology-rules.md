---
title: Typologien und Typologieregeln
description: Entdecken Sie, wie Typologien und Typologieregeln in Adobe Campaign funktionieren.
page-status-flag: never-activated
uuid: a98ebc36-172d-4f46-b6ee-b2636a1007c9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
discoiquuid: 2590d94c-51ef-4c0f-b1ec-c2837e94da40
context-tags: typology,overview;typologyRule,main;typologyRule,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a9c0e3cc4609e747bbfebeb90049862f29c9d8d9

---


# Typologien und Typologieregeln{#about-typology-rules}

Mit Campaign Standard können Sie eine Nachricht mit einer **Typologie** verknüpfen, um zu überprüfen, ob die Nachricht gültig ist und Ihre Qualitätskriterien erfüllt.

Typologien sind Gruppen von **Typologieregeln**, die während der Analyse der Nachricht ausgeführt werden. Sie ermöglichen es Ihnen, sicherzustellen, dass Ihre E-Mails immer bestimmte Elemente enthalten (z. B. einen Link zur Abmeldung oder eine Betreffzeile) oder Filterregeln, um Gruppen von Ihrer beabsichtigten Zielgruppe auszuschließen (z. B. Abonnenten, Konkurrent oder Nichtloyalkunden).

![](assets/typology_messagelink.png)

In Campaign Standard stehen gebrauchsfertige Typologien und Typologieregeln zur Verfügung. Je nach Bedarf können Sie auch neue Regeln erstellen und diese zu vorhandenen oder neuen Typologien hinzufügen, um eine Verknüpfung zu Ihren Nachrichten herzustellen.

Die Schritte zum Erstellen und Anwenden einer Typologie auf Nachrichten sind:

1. Erstellen Sie Typologieregeln (siehe [diesen Abschnitt](../../sending/using/managing-typology-rules.md#creating-a-typology-rule)).
1. Create a typology and reference the rules you created into it (see [this section](../../sending/using/managing-typologies.md#creating-a-typology)).
1. Konfigurieren Sie Ihren Versand für die Verwendung der von Ihnen erstellten Typologie (siehe [diesen Abschnitt](../../sending/using/managing-typologies.md#applying-typologies-to-messages)).
1. Während der Nachrichtenvorbereitung werden Profil ausgeschlossen, wenn das Kriterium erfüllt ist. Sie können Protokolle überprüfen, um Ausschlüsse zu überwachen.

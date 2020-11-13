---
title: Über Typologien und Typologieregeln
description: Erfahren Sie, wie Typologien und Typologieregeln in Adobe Campaign funktionieren.
page-status-flag: never-activated
uuid: a98ebc36-172d-4f46-b6ee-b2636a1007c9
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
discoiquuid: 2590d94c-51ef-4c0f-b1ec-c2837e94da40
context-tags: typology,overview;typologyRule,main;typologyRule,overview
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '190'
ht-degree: 100%

---


# Über Typologien und Typologieregeln{#about-typology-rules}

Mit Campaign Standard können Sie eine Nachricht mit einer **Typologie** verknüpfen, um zu überprüfen, ob die Nachricht gültig ist und Ihre Qualitätskriterien erfüllt.

Typologien sind Gruppen von **Typologieregeln**, die während der Nachrichtenanalyse ausgeführt werden. Damit können Sie sicherstellen, dass Ihre E-Mails immer bestimmte Elemente (z. B. einen Link zur Abmeldung oder eine Betreffzeile) oder Filterregeln enthalten, um Gruppen aus Ihrer beabsichtigten Zielgruppe auszuschließen (z. B. ehemalige Abonnenten, Konkurrenten oder Kunden, die nicht Mitglied im Treueprogramm sind).

![](assets/typology_messagelink.png)

In Campaign Standard stehen gebrauchsfertige Typologien und Typologieregeln zur Verfügung. Je nach Bedarf können Sie auch neue Regeln erstellen und zu vorhandenen oder neuen Typologien hinzufügen, um eine Verknüpfung zu Ihren Nachrichten herzustellen.

Die Schritte zum Erstellen und Anwenden einer Typologie für Nachrichten sind:

1. Richten Sie Typologieregeln ein (siehe [diesen Abschnitt](../../sending/using/managing-typology-rules.md#creating-a-typology-rule)).
1. Erstellen Sie eine Typologie und referenzieren Sie diese mit den Regeln, die Sie erstellt haben (siehe [diesen Abschnitt](../../sending/using/managing-typologies.md#creating-a-typology)).
1. Konfigurieren Sie Ihren Versand für die Verwendung der von Ihnen erstellten Typologie (siehe [diesen Abschnitt](../../sending/using/managing-typologies.md#applying-typologies-to-messages)).
1. Während der Nachrichtenvorbereitung werden Profile ausgeschlossen, wenn das Kriterium erfüllt wird. In den Logs können Sie die Ausführung von Ausschlüssen überprüfen.

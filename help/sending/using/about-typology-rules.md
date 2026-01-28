---
title: Über Typologien und Typologieregeln
description: Erfahren Sie, wie Typologien und Typologieregeln in Adobe Campaign funktionieren.
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
context-tags: typology,overview;typologyRule,main;typologyRule,overview
feature: Typology Rules
role: User
level: Intermediate
exl-id: dff72856-d28c-45c4-a073-12cc25f51f23
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
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

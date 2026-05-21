---
title: Verwenden von Typologieregeln
description: Erfahren Sie, wie Sie Typologieregeln verwenden können.
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
context-tags: typology,overview;typologyRule,main;typologyRule,overview
feature: Typology Rules
role: User
level: Intermediate
exl-id: 5ef66b1b-1c81-42fb-a18c-fcf7f21e1ff7
TQID: https://experienceleague.adobe.com/EAQzeoYku9S-ZThn-x3IBpLetTHqO2zNeY1ZsWQKVPE
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 582
ht-degree: 93%

---

# Verwenden von Typologieregeln {#managing-typology-rules}

## Über Typologieregeln {#about-typology-rules}

Typologieregeln sind Geschäftsregeln, mit denen Sie eine Nachricht prüfen und filtern können, bevor Sie sie senden. Verfügbare Arten von Typologieregeln sind:

* **Filterregeln**: Damit können Sie einen Teil der Nachrichten-Zielgruppe anhand von in einer Abfrage definierten Kriterien ausschließen. Mögliche Kriterien sind zum Beispiel Profile in Quarantäne oder Profile, die bereits eine bestimmte Anzahl an E-Mails erhalten haben. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/filtering-rules.md).

* **Ermüdungsregeln**: Damit können Sie eine Höchstzahl an Nachrichten festlegen, die an jedes Profil gesendet wird. Auf diese Weise stellen Sie sicher, dass die einzelnen Profile nicht zu häufig angesprochen werden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/fatigue-rules.md).

* **Kontrolle** Regeln: Mit dieser Art von Regeln kann der Benutzer die Gültigkeit und Qualität der Nachrichten überprüfen, bevor sie gesendet werden, z. B. die Zeichenanzeige, die Größe der SMS-Nachricht, das Adressformat usw. Weiterführende Informationen hierzu finden Sie [diesem Abschnitt](../../sending/using/control-rules.md).

Typologieregeln sind verfügbar über das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL Typologien]** > **[!UICONTROL Typologieregeln]**.

Standardmäßig sind mehrere vordefinierte **Filter**- und **Kontroll**-Typologieregeln verfügbar. Sie werden in den Abschnitten [Filterregeln](../../sending/using/filtering-rules.md) und [Kontrollregeln](../../sending/using/control-rules.md) genauer beschrieben.

Je nach Bedarf können Sie bestehende Typologieregeln ändern oder neue erstellen, mit Ausnahme von **[!UICONTROL Kontrollregeln]**, die schreibgeschützt sind und sich nicht ändern lassen.

## Erstellung einer Typologieregel {#creating-a-typology-rule}

Die wichtigsten Schritte zum Erstellen einer Typologieregel sind:

1. Rufen Sie das Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanal]** > **[!UICONTROL Typologien]** > **[!UICONTROL Typologieregeln]** auf und wählen Sie dann **[!UICONTROL Erstellen]**.

   ![](assets/typology_create-rule.png)

1. Geben Sie den **[!UICONTROL Titel]** der Typologie ein und geben Sie dann den **[!UICONTROL Kanal]** an, auf den die Regel angewendet werden soll.

   ![](assets/typology-rule-label.png)

1. Geben Sie den **[!UICONTROL Typ]** der Typologieregel an und konfigurieren Sie sie dann entsprechend Ihren Anforderungen. Beachten Sie, dass die Konfiguration der Typologieregeln je nach Typ unterschiedlich ist. Weiterführende Informationen finden Sie in den Abschnitten **[Filterregeln](../../sending/using/filtering-rules.md)** und **[Ermüdungsregeln](../../sending/using/fatigue-rules.md)**.

1. Wählen Sie die Typologien aus, in die die neue Regel eingefügt werden soll. Wählen Sie dazu den Tab **[!UICONTROL Typologien]** und dann die Schaltfläche **[!UICONTROL Element erstellen]** aus.

   ![](assets/typology-typologies-tab.png)

1. Wählen Sie die gewünschte Typologie aus und dann **[!UICONTROL Bestätigen]**.

   ![](assets/typology-link.png)

1. Bestätigen Sie nach Auswahl aller Typologien die Erstellung der Typologieregel mit **[!UICONTROL Erstellen]**.

## Ausführungsreihenfolge von Typologieregeln {#typology-rules-execution-order}

Die Typologieregeln werden in der Reihenfolge ausgeführt, die während der Zielgruppenbestimmung, Analyse und Nachrichtenpersonalisierung festgelegt wird.

Im Standard-Ausführungsmodus werden die Regeln in der folgenden Reihenfolge ausgeführt:

1. Kontrollregeln, wenn sie zu Beginn der Zielgruppenbestimmung angewendet werden
1. Filterregeln:

   * Native Anwendungsregeln für die Adressqualifizierung: definierte Adresse / nicht verifizierte Adresse / Adresse auf der Blockierungsliste / Adresse in Quarantäne / Qualität der Adresse.
   * Vom Benutzer definierte Filterregeln

1. Kontrollregeln, wenn sie am Ende der Zielgruppenbestimmung angewendet werden
1. Kontrollregeln, wenn sie zu Beginn der Personalisierung angewendet werden
1. Kontrollregeln, wenn sie am Ende der Personalisierung angewendet werden

Sie können die Ausführungsreihenfolge für Regeln desselben Typs jedoch in jeder Typologie anpassen. Wenn während einer Nachrichtenverarbeitungsphase mehrere Regeln ausgeführt werden, können Sie sogar wählen, in welcher Reihenfolge sie angewendet werden sollen.

Eine Filterregel, die in der Ausführungsreihenfolge an Position 20 steht, wird zum Beispiel vor einer Filterregel ausgeführt, die in der Ausführungsreihenfolge an Position 30 steht.

In den **[!UICONTROL Eigenschaften]** einer Typologieregel können Sie deren Ausführungsreihenfolge festlegen. Wenn mehrere Regeln angewendet werden müssen, wird durch die Ausführungsreihenfolge jeder Regel bestimmt, welche zuerst ausgeführt wird. Lesen Sie diesbezüglich auch den Abschnitt [Ausführungsreihenfolge von Typologieregeln](#typology-rules-execution-order).

![](assets/typology_rule-active.png)

Eine Typologieregel kann über **[!UICONTROL Eigenschaften]** deaktiviert werden, wenn die Regel zum Zeitpunkt der Analyse der von der Regel betroffenen Nachrichten nicht angewendet werden soll.

![](assets/typology_rule-order.png)

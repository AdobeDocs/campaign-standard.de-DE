---
title: Verwalten von Typologieregeln
description: Erfahren Sie, wie Sie Typologieregeln verwenden.
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
source-git-commit: ba1fcca02ce9582d85e57bde815ccf3f551ac7a3

---


# Verwalten von Typologieregeln {#managing-typology-rules}

## Über Typologieregeln {#about-typology-rules}

Typologieregeln sind Geschäftsregeln, mit denen Sie eine Nachricht prüfen und filtern können, bevor Sie sie senden. Verfügbare Typologieregeln sind:

* **Filtern** von Regeln: Mit diesem Regeltyp können Sie einen Teil der Zielgruppe der Nachricht nach Kriterien ausschließen, die in einer Abfrage definiert sind, wie z. B. isolierte Profil oder Profil, die bereits eine bestimmte Anzahl von E-Mails gesendet wurden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/filtering-rules.md).

* **Ermüdungsregeln** : Mit diesem Regeltyp können Sie eine maximale Anzahl von Meldungen pro Profil definieren, um zu vermeiden, dass sie übermäßig angefordert werden. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/fatigue-rules.md).

* **Steuerungsregeln** : Diese Art von Regeln ermöglicht es dem Benutzer, die Gültigkeit und Qualität der Nachrichten zu überprüfen, bevor sie gesendet werden, wie z.B. Zeichenanzeige, SMS-Größe, Adressformat usw. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/control-rules.md).

Typologieregeln stehen unter **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Typologies]** > **[!UICONTROL Typology rules]** Menü zur Verfügung.

Standardmäßig sind mehrere vordefinierte **Filter** - und **Steuerungs** -Typologieregeln verfügbar. Sie werden in den Abschnitten [Filterregeln](../../sending/using/fatigue-rules.md) und [Kontrollregeln](../../sending/using/control-rules.md) ausführlich beschrieben.

Je nach Bedarf können Sie bestehende Typologieregeln ändern oder neue erstellen, mit Ausnahme von **[!UICONTROL Control]** Regeln, die schreibgeschützt sind und nicht geändert werden können.

## Erstellung einer Typologieregel {#creating-a-typology-rule}

Die wichtigsten Schritte zum Erstellen einer Typologieregel sind:

1. Rufen Sie das **[!UICONTROL Administration]** / **[!UICONTROL Channels]** / **[!UICONTROL Typologies]** / **[!UICONTROL Typology rules]** Menü auf und klicken Sie dann auf **[!UICONTROL Create]**.

   ![](assets/typology_create-rule.png)

1. Geben Sie die Typologie ein **[!UICONTROL Label]** und legen Sie dann fest, **[!UICONTROL Channel]** für welche Regel gelten soll.

   ![](assets/typology-rule-label.png)

1. Geben Sie die Typologieregel an **[!UICONTROL Type]** und konfigurieren Sie sie dann entsprechend Ihren Anforderungen. Beachten Sie, dass die Konfiguration der Typologieregeln je nach Typ unterschiedlich ist. Weitere Informationen finden Sie in den Abschnitten **[Filterregeln](../../sending/using/filtering-rules.md)**und**[ Ermüdungsregeln](../../sending/using/fatigue-rules.md)** .

1. Wählen Sie die Typologien aus, in die die neue Regel eingefügt werden soll. Wählen Sie dazu die **[!UICONTROL Typologies]** Registerkarte und klicken Sie dann auf **[!UICONTROL Create element]** Schaltfläche.

   ![](assets/typology-typologies-tab.png)

1. Wählen Sie die gewünschte Typologie aus und klicken Sie auf **[!UICONTROL Confirm]**.

   ![](assets/typology-link.png)

1. Nachdem Sie alle Typologien ausgewählt haben, klicken Sie auf **[!UICONTROL Create]** , um die Erstellung der Typologieregel zu bestätigen.

## Ausführungsreihenfolge von Typologieregeln {#typology-rules-execution-order}

Typologieregeln werden in einer Reihenfolge ausgeführt, die während der Targeting-, Analyse- und Meldungspersonalisierungsphase angegeben wird.

Im Standard-Ausführungsmodus werden die Regeln in der folgenden Reihenfolge ausgeführt:

1. Kontrollregeln, wenn sie zu Beginn der Zielgruppenbestimmung angewendet werden
1. Filterregeln:

   * Nativ in der Anwendung enthaltene Regeln für die Adressenqualifizierung: definierte Adressen/nicht überprüfte Adressen/Adressen auf der Blacklist/Adressen in Quarantäne/Adressenqualität
   * Vom Benutzer definierte Filterregeln

1. Kontrollregeln, wenn sie am Ende der Zielgruppenbestimmung angewendet werden
1. Kontrollregeln, wenn sie zu Beginn der Personalisierung angewendet werden
1. Kontrollregeln, wenn sie am Ende der Personalisierung angewendet werden

Sie können die Ausführungsreihenfolge für Regeln desselben Typs jedoch in jeder Typologie anpassen. Wenn während einer Nachrichtenverarbeitungsphase mehrere Regeln ausgeführt werden, können Sie sogar wählen, in welcher Reihenfolge sie angewendet werden sollen.

Eine Filterregel, die in der Ausführungsreihenfolge an Position 20 steht, wird zum Beispiel vor einer Filterregel ausgeführt, die in der Ausführungsreihenfolge an Position 30 steht.

In the **[!UICONTROL Properties]** of a typology rule, you can set its execution order. Wenn mehrere Regeln angewendet werden müssen, wird durch die Ausführungsreihenfolge jeder Regel bestimmt, welche zuerst ausgeführt wird. Lesen Sie diesbezüglich auch den Abschnitt [Ausführungsreihenfolge von Typologieregeln](#typology-rules-execution-order).

![](assets/typology_rule-active.png)

A typology rule can be deactivated through its **[!UICONTROL Properties]** if you do not want the rule to be applied at the moment that the messages concerned by the rule are analyzed.

![](assets/typology_rule-order.png)
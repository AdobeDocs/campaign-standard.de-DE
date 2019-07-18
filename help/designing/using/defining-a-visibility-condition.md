---
title: Sichtbarkeitsbedingung definieren
seo-title: Sichtbarkeitsbedingung definieren
description: Sichtbarkeitsbedingung definieren
seo-description: Hier erfahren Sie, wie Sie ein Webseitenelement nur dann sichtbar machen, wenn eine gewisse Bedingung erfüllt wird.
page-status-flag: nie aktiviert
uuid: 224005 ba-ef 09-4790-b 2 f 0-30 ed 74 cfa 32 d
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: entwerfen
content-type: Referenz
topic-tags: define-conditional-content
discoiquuid: c 12125 a 7-a 1 cf -4 bc 1-a 138-57 ff 74974024
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Sichtbarkeitsbedingung definieren{#defining-a-visibility-condition}

Es besteht die Möglichkeit, für alle Elemente Sichtbarkeitsbedingungen zu definieren. Das entsprechende Element wird nur dann angezeigt, wenn die Bedingung erfüllt ist.

Markieren Sie den gewünschten Block und geben Sie in den Einstellungen im Feld **[!UICONTROL Sichtbarkeitsbedingung]die zu erfüllende Bedingung an.**

![](assets/delivery_content_5.png)

Diese Option steht nur für folgende Elemente zur Verfügung: ADDRESS, BLOCKQUOTE, CENTER, DIR, DIV, DL, FIELDSET, FORM, H1, H2, H3, H4, H5, H6, NOSCRIPT, OL, P, PRE, UL, TR, TD.

Weiterführende Informationen zum Ausdruckseditor finden Sie im Abschnitt [Ausdrucksbearbeitung](../../automating/using/editing-queries.md#about-query-editor).

These conditions adopt the XTK expression syntax (e.g. **context.profile.email !=''** or **context.profile.status='0'**). Standardmäßig werden alle Felder angezeigt.

>[!NOTE]
>
>Es ist nicht möglich, Bedingungen für Blöcke zu definieren, die Unterelemente mit dynamischen Inhalten enthalten oder die selbst bereits einem dynamischen Inhalt angehören. Unsichtbare dynamische Blöcke, wie beispielsweise Dropdown-Menüs, können nicht bearbeitet werden.


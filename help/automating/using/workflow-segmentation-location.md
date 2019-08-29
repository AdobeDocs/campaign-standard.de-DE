---
title: '" Workflow use-case: Segmentierung am Standort "'
seo-title: '" Workflow use-case: Segmentierung am Standort "'
description: '" Workflow use-case: Segmentierung am Standort "'
seo-description: '" Workflow use-case: Segmentierung am Standort "'
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: 'Arbeitsfluss, Verwendung, Abfrage, Segmentierung, Lieferung '
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f57775ec88925d43046fe4162f2753c189d50c62

---


# Einsatz von Workflow: Segmentierung am Standort {#segmentation-on-location}

Sie können eine E-Mail an Kunden mit Angeboten in ihren lokalen Geschäften schicken.

1. In **[!UICONTROL Marketing Activities]**, click **[!UICONTROL Create]** and select **[!UICONTROL Workflow]**.
1. Wählen **[!UICONTROL Sie New Workflow]** als Workflow und klicken **[!UICONTROL Sie als Nächstes]**.
1. Geben Sie die Eigenschaften des Arbeitslaufs und Klicken **[!UICONTROL .]**

## Auswahl der Empfänger durch E-Mail{#selecting-recipients-contactable-via-email}

1. Bei **[!UICONTROL Tätigkeiten]** &gt; **[!UICONTROL Zielstreben]**, Abschleppung und Absturz einer **[!UICONTROL Query-Aktivität]**![](assets/query.png).
1. Verdoppeln Sie die Aktivität auf.
1. Bei **[!UICONTROL Abzügen]**, Abbremsungen **[!UICONTROL und Abschlagsprofilen ist]** die E **[!UICONTROL -Email]** mit dem Betreiber **[!UICONTROL nicht leer]**.
1. Bei **[!UICONTROL Abschlagsabzügen und]****[!UICONTROL Abschlagsprofilen Profile und]** Auswahl der Felder **[!UICONTROL nicht mehr per E-Email]** mit dem Wert **[!UICONTROL Nr]**.
1. Klicken **[!UICONTROL Sie bitte]** zweimal.

## Creating a Segmentation activity{#creating-a-segmentation-activity}

1. Ziehen Sie eine **[!UICONTROL Segmentation]** und verdoppeln Sie sie.
1. Klicken auf Segmente, dann offener Übergang zur Zielgruppe in der ersten Stadt. Hier ist Boston.
1. Standort und **[!UICONTROL Fallort und]** Auswahl **[!UICONTROL der Stadt]** mit dem Betreiber **[!UICONTROL und]** dem Wert **[!UICONTROL Boston]**.
Anmerkung: Um alle Menschen zu erreichen, die in Boston eingetroffen sind, ist es nicht möglich, die fallempfindliche Option zu ignorieren.
1. Wählen Sie **[!UICONTROL Bestätigen]**.
1. In Liste **[!UICONTROL der outbound segmente]****[!UICONTROL einfügen Sie ein Element]** und ![](assets/edit_darkgrey-24px.png) klicken Sie darauf, ein Segment in der zweiten Stadt zu schaffen. Hier Chicago.
1. Standort und **[!UICONTROL Fallort Ort]** und Auswahl **[!UICONTROL der Stadt]** mit dem Betreiber **[!UICONTROL in]** **[!UICONTROL Chicago]** .

>[!NOTE]
>
>Um alle Menschen, die in Chicago eingereist sind, zu erreichen, ist es nicht möglich, die Sache unkritisch zu machen.

1. Wählen Sie **[!UICONTROL Bestätigen]**.

## Creating an email delivery{#creating-an-email-delivery}

1. Bei **[!UICONTROL Tätigkeiten]** &gt; **[!UICONTROL Kanäle]**, Abschleppung und Absturz einer **[!UICONTROL E-Mail nach]** jedem Segment.
1. Klicken Sie die Tätigkeit und wählen ![](assets/edit_darkgrey-24px.png) Sie sich zum Edit aus.
1. Wählen **[!UICONTROL Sie einfache E-Email]** und Klicken **[!UICONTROL Sie.]**
1. Wählen Sie eine E-Email-Vorlage und klicken Sie **[!UICONTROL als Nächstes]**.
1. Geben Sie die E-Email-Eigenschaften und klicken **[!UICONTROL Sie.]**
1. Um das Layout Ihrer E-Email zu schaffen, klicken Sie **[!UICONTROL auf Email Designer]**.
1. Elemente einfügen oder ein bestehendes Muster auswählen.
1. Personalisieren Sie Ihre E-Email mit spezifischen Angeboten.

Weitere Informationen sind [der Konzeption einer E-Mail](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch)zu entnehmen.

1. Klick **[!UICONTROL , um]** deine Layout zu überprüfen.
1. Wählen Sie **[!UICONTROL Speichern aus]**.

**Verwandte Themen:**

* [Sporttätigkeit](../../automating/using/query.md)
* [Segmentierung](../../automating/using/segmentation.md)
* [E-Mail-Versand](../../automating/using/email-delivery.md)

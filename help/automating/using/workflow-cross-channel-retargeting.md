---
title: '" Workflow use-case: Neuausrichtung von Nichtöffnern "'
seo-title: '" Workflow use-case: Neuausrichtung von Nichtöffnern "'
description: '" Workflow use-case: Neuausrichtung von Nichtöffnern "'
seo-description: '" Workflow use-case: Neuausrichtung von Nichtöffnern "'
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: 'Arbeitsfluss, Einsatz-Case, Abfrage, Abwarten, Lieferung '
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f57775ec88925d43046fe4162f2753c189d50c62

---


# Einsatz von Workflow: Neuausrichtung der Arbeitsabläufe, die eine neue Lieferung an Nichtöffnungs-{#retargeting-delivery-to-non-openers}

Sie können eine E-Mail an Kunden schicken und dann an diejenigen, die die Post nicht geöffnet haben.

1. In **[!UICONTROL Marketing Activities]**, click **[!UICONTROL Create]** and select **[!UICONTROL Workflow]**.
1. Wählen **[!UICONTROL Sie New Workflow]** als Workflow und klicken **[!UICONTROL Sie als Nächstes]**.
1. Geben Sie die Eigenschaften des Arbeitslaufs und Klicken **[!UICONTROL .]**

## Creating a query activity{#creating-a-query-activity}

1. Bei **[!UICONTROL Tätigkeiten]** &gt; **[!UICONTROL Zielstreben]**, Abschleppung und Absturz einer **[!UICONTROL Query-Aktivität]**![](assets/query.png).
1. Verdoppeln Sie die Aktivität auf.
1. Bei **[!UICONTROL Abzügen]**, Abbremsungen **[!UICONTROL und Abschlagsprofilen ist]** die **[!UICONTROL E-Email]** **[!UICONTROL nicht leer]**.
1. Bei **[!UICONTROL Abschlagsabzügen und]****[!UICONTROL Abschlagsprofilen Profile und]** Auswählen **[!UICONTROL nicht mehr per E-Email]** mit dem Wert **[!UICONTROL Nr]**.
1. Wählen Sie **[!UICONTROL Bestätigen]**.

## Creating an email delivery{#creating-an-email-delivery}

1. Stell eine**[!UICONTROL E-Mail-Lieferung]nach jedem Segment vor.
1. Klicken Sie die Tätigkeit und wählen ![](assets/edit_darkgrey-24px.png) Sie sich zum Edit aus.
1. Wählen **[!UICONTROL Sie einfache E-Email]** und Klicken **[!UICONTROL Sie.]**
1. Wählen **[!UICONTROL Sie einen freien Übergang ohne die Bevölkerung]** und klicken **[!UICONTROL Sie als Nächstes]**.
1. Wählen Sie eine E-Email-Vorlage und klicken Sie **[!UICONTROL als Nächstes]**.
1. Geben Sie die E-Email-Eigenschaften und klicken **[!UICONTROL Sie.]**
1. Gib das E-Email **-Mail-Angebot**.
1. Um das Layout Ihrer E-Email zu schaffen, klicken Sie auf **[!UICONTROL den Email Designer]**.
1. Elemente einfügen oder ein bestehendes Muster auswählen.
1. Personalisierung Ihrer E-Email mit spezifischen Angeboten für jeden Ort. Für weitere Informationen ist eine E-Email zu [erstellen](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch).
1. Klick **[!UICONTROL , um]** deine Layout zu überprüfen.
1. Wählen Sie **[!UICONTROL Speichern aus]**.

## Gezielte Einstellung von Nichtöffnern in einer Abfragetätigkeit{#targeting-non-openers-in-a-query-activity}

1. Bei **[!UICONTROL Tätigkeiten]** &gt; **[!UICONTROL Hinrichtung]**, Hinrichtung und Absturz einer **[!UICONTROL Warteaktivität]**![](assets/wait.png).
1. In **[!UICONTROL Laufzeit]**, klicken ![](assets/duration-icon.png) Sie einen Tag.
1. Bei **[!UICONTROL Tätigkeiten]** &gt; **[!UICONTROL Zielstreben]**, Abschleppung und Absturz einer **[!UICONTROL Query-Aktivität]**![](assets/query.png).
1. Verdoppeln Sie die Aktivität auf.
1. Bei **[!UICONTROL Abzugshindernissen]****[!UICONTROL und Abschlagsbohrungen]** und bei dem Bediener **[!UICONTROL gibt]** es eine Ablenkung.
1. Bei **[!UICONTROL Abgrenzungen]**&gt; **[!UICONTROL Die Lieferung]**, die Abschleppung **[!UICONTROL und die Abnahme]** bei dem Betreiber **[!UICONTROL sind gleich]** und wählen die Lieferung als Wert aus.
1. Bei **[!UICONTROL Absendern]**&gt; **[!UICONTROL Lieferung]**, Bremsung und **[!UICONTROL Fallart]** und Prüfung **[!UICONTROL offen]** als Wert.
1. Wählen Sie den Betreiber so aus, als ob es sich um Regeln **** handelt.
1. Wählen Sie **[!UICONTROL Bestätigen]**.

## Schaffung einer SMS-Lieferung{#creating-a-sms-delivery}

1. Ziehen Sie eine SMS-Lieferung nach jedem Segment ab.
1. Klicken Sie die Tätigkeit und wählen ![](assets/edit_darkgrey-24px.png) Sie sich zum Edit aus.
1. Wählen **[!UICONTROL Sie einfache SMS]** und Klicken **[!UICONTROL .]**
1. Wählen Sie ein SMS-Muster und klicken Sie **[!UICONTROL als Nächstes]**.
1. Geben Sie die SMS-Eigenschaften und klicken **[!UICONTROL Sie als Nächstes]**.
1. Um Ihre SMS zu schaffen, klicken Sie auf **[!UICONTROL Email Designer]**.
1. Elemente einfügen oder ein bestehendes Muster auswählen.
1. Personalisieren Sie Ihre SMS mit spezifischen Angeboten für jeden Ort.
Weitere Informationen sind [der Planung eines SMS](../../channels/using/creating-an-sms-message.md)zu entnehmen.
1. Klick **[!UICONTROL , um]** deine Layout zu überprüfen.
1. Wählen Sie **[!UICONTROL Speichern aus]**.

**Verwandte Themen:**

* [Abfrage](../../automating/using/query.md)
* [SMS-Versand](../../automating/using/sms-delivery.md)
* [E-Mail-Versand](../../automating/using/email-delivery.md)
* [E-Mail-Kanal](../../channels/using/creating-an-email.md)

---
title: '" Workflow use-case: Schaffung von Lieferungen mit einer Ergänzung "'
seo-title: '" Workflow use-case: Schaffung von Lieferungen mit einer Ergänzung "'
description: '" Workflow use-case: Schaffung von Lieferungen mit einer Ergänzung "'
seo-description: '" Workflow use-case: Schaffung von Lieferungen mit einer Ergänzung "'
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow, use-case, segmentierung
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e77c8a65834009f2f7157d9535ae8e12e59244ff

---


# Einsatz von Workflow: Schaffung von Lieferungen mit Ergänzung {#deliveries-with-complement}

Sie können eine E-Mail an Kunden senden: einer für die kunden, die vor weniger als einem jahr gegründet wurden, eines für die kunden vor über einem jahr.

1. In **[!UICONTROL Marketing Activities]**, click **[!UICONTROL Create]** and select **[!UICONTROL Workflow]**.
1. Wählen **[!UICONTROL Sie New Workflow]** als Workflow und klicken **[!UICONTROL Sie als Nächstes]**.
1. Geben Sie Eigenschaften des Arbeitslaufs und Klicken **[!UICONTROL .]**

## Schaffen eine Sporttätigkeit {#create-a-query-activity}

1. Bei **[!UICONTROL Tätigkeiten]** &gt; **[!UICONTROL Zielstreben]**, Abschleppung und Absturz einer **[!UICONTROL Query-Aktivität]**![](assets/query.png).
1. Verdoppeln Sie die Aktivität auf.
1. Bei **[!UICONTROL Abzügen]**, Abbremsungen **[!UICONTROL und Abschlagsprofilen ist]** die **[!UICONTROL E-Email]** **[!UICONTROL nicht leer]**.
1. Bei **[!UICONTROL Abschlagsabzügen und]****[!UICONTROL Abschlagsprofilen Profile und]** Auswählen **[!UICONTROL nicht mehr per E-Email]** mit dem Wert **[!UICONTROL Nr]**.
1. Wählen Sie **[!UICONTROL Bestätigen]**.

## Schaffen eine Segmentierung {#create-a-segmentation-activity}

1. Bei **[!UICONTROL Tätigkeiten]** &gt; **[!UICONTROL Zielstreben]**, Abschleppung und Absturz einer **[!UICONTROL Segmentierung]** .
1. Hover über das Segment klicken dann ![](assets/edit_darkgrey-24px.png) auf Zielkunden, die dieses Jahr in der Datenbank hinzugefügt werden.
1. Abbremsung und **[!UICONTROL Fallprofile und]** Auswählen **[!UICONTROL mit]** dem Filtertyp **[!UICONTROL Relative]**.
1. Die **[!UICONTROL Genauigkeit]** des **[!UICONTROL Jahres ändern]** und **[!UICONTROL dieses Jahr auswählen]**.
1. Klicken **[!UICONTROL Sie bitte]** zweimal.
1. Bei **[!UICONTROL fortgeschrittenen Optionen]** ist es möglich **[!UICONTROL , die Generierung zu ergänzen,]** um ein Segment zu schaffen, das die verbleibenden Empfänger betrifft.
1. Wählen Sie **[!UICONTROL Bestätigen]**.
1. Wählen Sie **[!UICONTROL Speichern aus]**.

>[!NOTE]
>
>Um die Struktur der Regel zu beachten, klicken **[!UICONTROL Sie auf Advanced Mode]**.

## Creating an Email delivery {#create-an-email-delivery}

1. Bei **[!UICONTROL Tätigkeiten]** &gt; **[!UICONTROL Kanäle]**, Schleppen und Abstürzen einer E-Email nach jedem Segment.
1. Klicken Sie die Tätigkeit und wählen ![](assets/edit_darkgrey-24px.png) Sie sich zum Edit aus.
1. Wählen **[!UICONTROL Sie Single Mail und]** klicken **[!UICONTROL Sie danach]**.
1. Wählen Sie eine E-Email-Vorlage und klicken Sie **[!UICONTROL als Nächstes]**.
1. Geben Sie die E-Email-Eigenschaften und klicken **[!UICONTROL Sie.]**
1. Um das Layout Ihrer E-Email zu schaffen, klicken Sie **[!UICONTROL auf Email Designer]**.
1. Elemente einfügen oder ein bestehendes Muster auswählen.
1. Personalisieren Sie Ihre E-Email mit spezifischen Angeboten.
1. Klick **[!UICONTROL , um]** deine Layout zu überprüfen.
1. Wählen Sie **[!UICONTROL Speichern aus]**.

Weitere Informationen sind [der Konzeption einer E-Mail](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch)zu entnehmen.

**Verwandte Themen:**

* [Abfrage](../../automating/using/query.md)
* [Segmentierung](../../automating/using/segmentation.md)
* [E-Mail-Versand](../../automating/using/email-delivery.md)

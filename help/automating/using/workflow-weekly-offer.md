---
title: '" Workflow use-case: Schaffung einer wöchentlichen Lieferung "'
seo-title: '" Workflow use-case: Schaffung einer wöchentlichen Lieferung "'
description: '" Workflow use-case: Schaffung einer wöchentlichen Lieferung "'
seo-description: '" Workflow use-case: Schaffung einer wöchentlichen Lieferung "'
page-status-flag: never-activated
uuid: 396a3de1-6ffa-4385-ac9f-15fdeae5a366
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: 'execution-activities '
discoiquuid: 377821e6-69f8-41cc-a1ad-8a2f5ed4d409
context-tags: workflow, use-case, search, delivery, schedule
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e77c8a65834009f2f7157d9535ae8e12e59244ff

---


# Fallfall für den Weltraum: Jeden Dienstag eine E-Email-Lieferung schaffen{#creating-email-every-tuesday}

Sie können jeden Dienstag eine E-Email an alle Kunden für Sonderangebote schicken.

1. In **[!UICONTROL Marketing Activities]**, click **[!UICONTROL Create]** and select **[!UICONTROL Workflow]**.
1. Wählen **[!UICONTROL Sie New Workflow]** als Workflow und klicken **[!UICONTROL Sie als Nächstes]**.
1. Geben Sie Eigenschaften des Arbeitslaufs und Klicken **[!UICONTROL .]**

## Creating a Scheduler activity{#creating-a-scheduler-activity}

1. Bei **[!UICONTROL Tätigkeiten]** &gt; **[!UICONTROL Hinrichtung]**, Hinrichtung und Abbruch einer **[!UICONTROL Flugplantätigkeit]**![](assets/scheduler_icon.png).
1. Verdoppeln Sie die Aktivität auf.
1. Konfiguriert die Ausführung Ihrer Lieferung.
1. In **[!UICONTROL Ausführungsfrequenz]** ist **[!UICONTROL wöchentlich auszuwählen]**.
1. Wählen Sie eine **[!UICONTROL Zeit]** und **[!UICONTROL eine Wiederholungsfrequenz]** für Ihre Lieferungen.
1. In Tagen **[!UICONTROL der Woche wird]****[!UICONTROL Dienstag ausgewählt]**.
1. Geben Sie einen **[!UICONTROL Start]** und einen **[!UICONTROL Abfahrungsparameter]** für Ihren Arbeitsablauf.
1. Validieren Sie die Aktivität und speichern Sie den Workflow.

![](assets/scheduler_properties.png)

>[!NOTE]
>
>Um Ihren Arbeitsablauf in einer bestimmten **[!UICONTROL Zeitzone]** zu beginnen, wird in der **[!UICONTROL Ausführungsoption]** die Zeitzone für Ihren Zeitplan im Zeitzone eingerichtet.

## Creating a Query activity{#creating-a-query-activity}

1. Bei **[!UICONTROL Tätigkeiten]** &gt; **[!UICONTROL Zielausrichtung]**, Auswahl von Empfängern, Abschleppung und Abrutschen und **[!UICONTROL Doppelarbeit]** .
1. Bei **[!UICONTROL Abgrenzungen]** &gt; **[!UICONTROL Profil]**, Abschleppung und Abnahme **[!UICONTROL von E-Mail]**.
1. Auswahl **[!UICONTROL ist nicht leer]** als Betreiber.
1. Bei **[!UICONTROL Abgrenzungen]** &gt; **[!UICONTROL Allgemeine]** Profile hinzufügen und nicht **[!UICONTROL mehr per E-Email]** mit dem Wert **[!UICONTROL Nr]**.
1. Wählen Sie **[!UICONTROL Bestätigen]**.

## Creating an Email delivery{#creating-an-email-delivery}

1. Bei **[!UICONTROL Tätigkeiten]** &gt; **[!UICONTROL Kanäle]**, Schleppen und Abstürzen einer **[!UICONTROL E-Mail-Lieferung]**.
1. Klicken Sie die Tätigkeit und wählen ![](assets/edit_darkgrey-24px.png) Sie sich zum Edit aus.
1. Wählen **[!UICONTROL Sie wiederkehrende E-Email]** und klicken **[!UICONTROL Sie.]**
1. Wählen Sie eine E-Email-Vorlage und klicken Sie **[!UICONTROL als Nächstes]**.
1. Geben Sie die E-Email-Eigenschaften und klicken **[!UICONTROL Sie.]**
1. Um das Layout Ihrer E-Email zu schaffen, klicken Sie auf **[!UICONTROL Use Email Designer]**.
1. Elemente einfügen oder ein bestehendes Muster auswählen.
1. Personalisierung deine E-Email unter Nutzung von Feldern und Verbindungen.
1. Wählen Sie **[!UICONTROL Speichern aus]**.

Weitere Informationen sind [der Konzeption einer E-Mail](../../designing/using/about-email-content-design.md#designing-an-email-content-from-scratch)zu entnehmen.

**Verwandte Themen:**

* [Sporttätigkeit](../..//automating/using/query.md)
* [Flugplantätigkeit](../..//automating/using/scheduler.md)
* [E-Mail-Versand](../..//automating/using/email-delivery.md)
* [E-Mail-Kanal](../..//channels/using/creating-an-email.md)

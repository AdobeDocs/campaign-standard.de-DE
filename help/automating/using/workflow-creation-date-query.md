---
title: Sendungen zum Erstellungsdatum des Profils erstellen
description: Dieser Anwendungsfall zeigt, wie Sie Sendungen zum Erstellungsdatum des Profils erstellen können.
audience: automating
content-type: reference
topic-tags: execution-activities
context-tags: workflow,use-case,query
feature: Workflows
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: f611e023-f74c-476e-83b9-aff451f68c81
TQID: https://experienceleague.adobe.com/qkMV-OW4cYN-u6R3PYn9kdMt7DgIgxA8WTsDhvLIzJw
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 2fe8bfb2bc8d0266bea52504feffb7b11f481b91
workflow-type: ht
source-wordcount: 405
ht-degree: 100%

---

# Sendungen zum Erstellungsdatum von Profilen erstellen {#creation-date-query}

Sie können am Jahrestag der Profilerstellung eines Kunden diesem ein Angebot per E-Mail senden.

1. Wählen Sie dazu in **[!UICONTROL Marketing-Aktivitäten]** die Option **[!UICONTROL Erstellen]** und dann **[!UICONTROL Workflow]** aus.
1. Wählen Sie als Workflow-Typ **[!UICONTROL Neuer Workflow]** und danach **[!UICONTROL Weiter]** aus.
1. Geben Sie die Eigenschaften des Workflows ein und wählen Sie **[!UICONTROL Erstellen]** aus.

## Planungsaktivität erstellen {#creating-a-scheduler-activity}

1. Ziehen Sie in **[!UICONTROL Aktivitäten]** > **[!UICONTROL Ausführung]** eine [](../../automating/using/scheduler.md)Planungsaktivität in den Arbeitsbereich.
1. Doppelklicken Sie auf die Aktivität.
1. Konfigurieren Sie Ihren Versand.
1. Wählen Sie in **[!UICONTROL Ausführungsfrequenz]** die Option **[!UICONTROL Täglich]** aus.
1. Wählen Sie eine **[!UICONTROL Zeit]** und das **[!UICONTROL Ausführungsintervall]** für Ihren Workflow aus.
1. Wählen Sie ein **[!UICONTROL Anfangsdatum]** und die **[!UICONTROL Gültigkeit]** für Ihren Workflow aus.
1. Bestätigen Sie die Aktivität und speichern Sie den Workflow.

>[!NOTE]
>
>Um Ihren Workflow mit einer bestimmten Zeitzone zu verbinden, richten Sie im Tab **[!UICONTROL Ausführungsoptionen]** im Feld **[!UICONTROL Zeitzone]** die Zeitzone für Ihren Zeitplan ein. Standardmäßig ist die ausgewählte Zeitzone die in den Eigenschaften des Workflows definierte Zeitzone (siehe [Workflow erstellen](../../automating/using/building-a-workflow.md)).

![](assets/time_zone.png)

## Abfrageaktivität erstellen {#creating-a-query-activity}

1. Um Empfänger auszuwählen, ziehen Sie eine [](../../automating/using/query.md)Abfrageaktivität in den Arbeitsbereich und doppelklicken Sie darauf.
1. Fügen Sie **[!UICONTROL Profile]** hinzu und wählen Sie **[!UICONTROL Nicht mehr per E-Mail kontaktieren]** mit dem Wert **[!UICONTROL Nein]** aus.

### Profile abrufen, die am Versandtag erstellt wurden {#retrieving-profiles-created-on-the-same-day}

1. Ziehen Sie unter **[!UICONTROL Profil]** das Feld **[!UICONTROL Erstellt]** in den Arbeitsbereich und klicken Sie auf **[!UICONTROL Erweiterter Modus]**.
   ![](assets/advanced_mode.png)
1. Doppelklicken Sie in der **[!UICONTROL Funktionsliste]** im Knoten **[!UICONTROL Datum]** auf **[!UICONTROL Tag]**.
1. Fügen Sie dann das Feld **[!UICONTROL Erstellt]** als Argument ein.
1. Wählen Sie als Operator **[!UICONTROL Gleich (=)]** aus.
1. Wählen Sie für den Wert in der **[!UICONTROL Funktionsliste]** im Knoten **[!UICONTROL Datum]** die Option **[!UICONTROL Tag]** aus.
1. Fügen Sie die Funktion **[!UICONTROL GetDate()]** als Argument ein.

Somit haben Sie die Profile abgerufen, deren Erstellungsdatum mit dem aktuellen Datum identisch ist.

Das Ergebnis sollte folgendermaßen aussehen:

`Day(@created) = Day(GetDate())`

![](assets/day_creation_query.png)

Klicken Sie auf **[!UICONTROL Bestätigen]**.

### Profile abrufen, die im Versandmonat erstellt wurden{#retrieving-profiles-created-on-the-same-month}

1. Wählen Sie im **[!UICONTROL Abfrageeditor]** die erste Abfrage aus und duplizieren Sie sie.
1. Öffnen Sie das Duplikat.
1. Ersetzen Sie in der Abfrage **[!UICONTROL Tag]** durch **[!UICONTROL Monat]**.
1. Klicken Sie auf **[!UICONTROL Bestätigen]**.

![](assets/month_rule.png)

Das Ergebnis sollte folgendermaßen aussehen:

`Month(@created) = Month(GetDate())`

Die endgültige Abfrage sieht folgendermaßen aus:

`Day(@created) = Day(GetDate()) AND Month(@created) = Month(GetDate())`

![](assets/expression_editor_1.png)

## E-Mail-Versand erstellen{#creating-an-email-delivery}

1. Ziehen Sie die Aktivität [E-Mail-Versand](../../automating/using/email-delivery.md) in den Arbeitsbereich.
1. Wählen Sie die Aktivität aus und danach ![](assets/edit_darkgrey-24px.png), um die Bearbeitung zu ermöglichen.
1. Wählen Sie **[!UICONTROL Wiederkehrende E-Mail]** und danach **[!UICONTROL Weiter]** aus.
1. Wählen Sie eine E-Mail-Vorlage und danach **[!UICONTROL Weiter]** aus.
1. Geben Sie die E-Mail-Eigenschaften ein und wählen Sie **[!UICONTROL Weiter]** aus.
1. Um das Layout Ihrer E-Mail zu erstellen, wählen Sie **[!UICONTROL Email Designer]** aus.
1. Fügen Sie Elemente ein oder wählen Sie eine bestehende Vorlage aus.
1. Personalisieren Sie Ihre E-Mail mit Feldern und Links. Weitere Informationen finden Sie unter [Gestalten einer E-Mail](../../designing/using/designing-from-scratch.md#designing-an-email-content-from-scratch).
1. Wählen Sie **[!UICONTROL Vorschau]** aus, um Ihr Layout zu überprüfen.
1. Klicken Sie auf **[!UICONTROL Speichern]**.

**Verwandte Themen:**

* [E-Mail-Kanal](../../channels/using/creating-an-email.md)

---
title: Verwenden von Segment Builder
description: Erfahren Sie, wie Sie mit Unified Segment Builder Audiences erstellen können.
page-status-flag: never-activated
uuid: b3996642-96ec-489e-b146-c8c2cb52aa32
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-audiences
discoiquuid: 750ecd8d-67a5-4180-bfec-2a8e3098c812
context-tags: audience,wizard;audience,overview;delivery,audience,back
internal: n
snippet: y
translation-type: ht
source-git-commit: 573131986d52bb4415cca59600048fd7dc5ba0db

---


# Verwenden von Unified Segment Builder {#using-the-unified-segment-builder}

>[!IMPORTANT]
>
>Der Audience Destinations-Dienst befindet sich derzeit in der Betaphase, die häufig ohne Vorankündigung aktualisiert werden kann. Kunden müssen auf Azure gehostet werden (derzeit nur für Nordamerika in der Betaphase), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an die Adobe-Kundenunterstützung, wenn Sie Zugriff haben möchten.

Mit Unified Segment Builder können Sie Audiences erstellen, indem Sie Regeln definieren, die auf Daten aus dem [Unified Profile Service](https://docs.adobe.com/content/help/de-DE/experience-platform/profile/home.html) stammen.

In diesem Abschnitt werden allgemeine Konzepte zum Erstellen eines Segments vorgestellt. Detaillierte Informationen zu Unified Segment Builder selbst finden Sie im [Segment Builder-Benutzerhandbuch](https://docs.adobe.com/content/help/de-DE/experience-platform/segmentation/ui/overview.html).

Die Benutzeroberfläche von Unified Segment Builder sieht wie folgt aus:

* Im linken Bereich finden Sie alle verfügbaren Attribute, Ereignisse und Audiences zum Erstellen des Segments. Ziehen Sie dazu die gewünschten Felder per Drag-and-Drop in den Segment Builder-Arbeitsbereich.
* Der mittlere Bereich bietet einen Arbeitsbereich zum Erstellen des Segments, indem Regeln aus den verfügbaren Feldern definiert und kombiniert werden.
* Die Kopfzeile und der rechte Bereich zeigen die Segmenteigenschaften (d. h. Name, Beschreibung und geschätzte qualifizierte Profile für das Segment) an.

![](assets/aep_audiences_interface.png)

## Erstellen eines Segments

Gehen Sie wie folgt vor, um ein Segment zu erstellen:

Unified Segment Builder sollte jetzt in Ihrem Arbeitsbereich angezeigt werden. Damit können Sie ein Segment mithilfe von Daten aus Adobe Experience Platform erstellen, das letztendlich zur Erstellung Ihrer Audience dienen wird.

1. Benennen Sie das Segment und geben Sie dann eine Beschreibung ein (optional).

   ![](assets/aep_audiences_creation_edit_name.png)

1. Vergewissern Sie sich, dass im Einstellungsfeld die gewünschte Zusammenführungsrichtlinie ausgewählt ist.

   Weiterführende Informationen zu Zusammenführungsrichtlinien finden Sie im entsprechenden Abschnitt des [Segment Builder-Benutzerhandbuchs](https://docs.adobe.com/content/help/de-DE/experience-platform/segmentation/ui/overview.html).

   ![](assets/aep_audiences_mergepolicy.png)

1. Suchen Sie nach den gewünschten Feldern im linken Bereich und ziehen Sie sie in den mittleren Arbeitsbereich.

   ![](assets/aep_audiences_dragfield.png)

1. Konfigurieren Sie die Regeln entsprechend den gezogenen Feldern.

   ![](assets/aep_audiences_configure_rules.png)

1. Wählen Sie die Schaltfläche **[!UICONTROL Segment erstellen]** aus.

## Die richtigen Felder für ein Segment finden

Im linken Bereich werden alle Attribute, Ereignisse und Audiences aufgelistet, die zum Erstellen von Regeln zur Verfügung stehen.

Die aufgeführten Felder sind Attribute, die durch Ihr Unternehmen erfasst und über das [Experience-Datenmodell-System (XDM)](https://docs.adobe.com/content/help/de-DE/experience-platform/xdm/home.html) zur Verfügung gestellt werden.

Die Felder sind in Tabs unterteilt:

* **[!UICONTROL Attribute]**: Vorhandene Profilattribute, die aus Ihrer Adobe Campaign-Datenbank und/oder Adobe Experience Platform stammen können. Sie beziehen sich auf statische Daten, die mit einem Profil verknüpft sind (z. B. E-Mail-Adresse, Wohnsitzland, Status im Treueprogramm usw.).

   ![](assets/aep_audiences_attributestab.png)

* **[!UICONTROL Ereignisse]**: Aktivitäten, die Verbraucher identifizieren, die mit den Touchpoints Ihres Unternehmens auf bestimmte Weise interagiert haben, z. B. &quot;alle Personen, die in zwei Wochen zweimal bestellt haben&quot;. Diese können aus Adobe Analytics gestreamt oder mithilfe von ETL-Tools anderer Anbieter direkt in die Adobe Experience Platform integriert werden.

   ![](assets/aep_audiences_eventstab.png)

>[!NOTE]
>
>Bei der **Segmentierung mit mehreren Entitäten** können Sie Profildaten um zusätzliche Daten erweitern, die auf Produkten, Geschäften oder anderen nicht-profilbasierten Klassen beruhen. Sobald eine Verbindung besteht, stehen Daten aus zusätzlichen Klassen zur Verfügung, so als wären sie im Profilschema nativ vorhanden.
>
>Weiterführende Informationen finden Sie im [entsprechenden Handbuch](https://docs.adobe.com/content/help/de-DE/experience-platform/segmentation/multi-entity-segmentation.html).

Standardmäßig zeigt Unified Segment Builder Felder an, in denen bereits Daten vorhanden sind. Um das vollständige Schema einschließlich der Felder anzuzeigen, für die keine Daten vorhanden sind, aktivieren Sie in den Einstellungen die Option **[!UICONTROL Gesamtes XDM-Schema anzeigen]**.

![](assets/aep_audiences_populatedfields.png)

Das Symbol am Ende der einzelnen Felder enthält weitere Informationen zum Attribut und dessen Verwendung.

![](assets/aep_audiences_isymbol.png)

## Definieren von Regeln für ein Segment

>[!NOTE]
>
>Im folgenden Abschnitt finden Sie allgemeine Informationen zur Definition von Regeln. Weiterführende Informationen finden Sie im [Segment Builder-Benutzerhandbuch](https://docs.adobe.com/content/help/de-DE/experience-platform/segmentation/ui/overview.html).

Gehen Sie wie folgt vor, um eine Regel zu erstellen:

1. Suchen Sie im linken Bereich nach dem Feld, das die Attribute oder Ereignisse enthält, auf denen die Regel basieren soll.

1. Ziehen Sie das Feld in den mittleren Arbeitsbereich und konfigurieren Sie es dann entsprechend der gewünschten Segmentdefinition. Dazu stehen mehrere Funktionen für Zeichenfolgen und Datum/Uhrzeit zur Verfügung.

   Im folgenden Beispiel werden alle Profile mit einem Geschlecht &quot;Männlich&quot; von der Regel in die Zielgruppe aufgenommen.

   ![](assets/aep_audiences_malegender.png)

   Die geschätzte Population, die dem Segment entspricht, wird im Abschnitt **[!UICONTROL Segmenteigenschaften]** automatisch neu berechnet.

1. Über die Schaltfläche **[!UICONTROL Profile anzeigen]** erhalten Sie eine Vorschau der ersten 20 Einträge, die der Regel entsprechen. So können Sie das Segment schnell überprüfen.

   ![](assets/aep_audiences_samplepreview.png)

   Sie können beliebig viele weitere Regeln hinzufügen, um die richtigen Profile in die Zielgruppe aufzunehmen.

   Wenn Sie einem Container eine Regel hinzufügen, wird sie mit dem logischen UND-Operator an alle vorhandenen Regeln angehängt. Wählen Sie bei Bedarf den logischen Operator aus, um ihn zu ändern.

   ![](assets/aep_audiences_andoperator.png)

Sobald beide Regeln miteinander verknüpft sind, bilden sie einen Container.

## Vergleichen von Feldern

Mit Unified Segment Builder können Sie zwei Felder miteinander vergleichen, um eine Regel zu definieren. Weibliche Personen beispielsweise, deren Wohnadresse eine andere Postleitzahl hat als die Arbeitsadresse.

Gehen Sie dazu wie folgt vor:

1. Ziehen Sie das erste Feld, das Sie vergleichen möchten (z. B. die Postleitzahl der Wohnadresse) in den zentralen Arbeitsbereich.

   ![](assets/aep_audiences_comparing_1.png)

1. Wählen Sie das zweite Feld (z. B. die Postleitzahl der Arbeitsadresse) aus, das mit dem ersten Feld verglichen werden soll.

   Ziehen Sie es in den zentralen Arbeitsbereich in den gleichen Container wie das erste Feld in das Feld **[!UICONTROL Hier ablegen, um Operanden zu vergleichen]**.

   ![](assets/aep_audiences_comparing_2.png)

1. Konfigurieren Sie den Operator zwischen den beiden Feldern nach Bedarf. In diesem Beispiel möchten wir, dass unser Segment Profile in die Zielgruppe aufnimmt, deren Wohnadresse sich von der Arbeitsadresse unterscheidet.

   ![](assets/aep_audiences_comparing_3.png)

Die Regel ist jetzt konfiguriert und kann als Audience aktiviert werden.

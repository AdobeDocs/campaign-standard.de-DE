---
title: Verwenden des einheitlichen Segmentaufbaus
description: Erfahren Sie, wie Sie mit dem einheitlichen Segmentaufbau Zielgruppen erstellen.
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
translation-type: tm+mt
source-git-commit: e9d4239182a7ebdec61e85fece6ec49dca8f665a

---


# Verwenden des einheitlichen Segmentaufbaus {#using-the-unified-segment-builder}

>[!IMPORTANT]
>
>Der Zielgruppen-Zieldienst befindet sich derzeit in der Betaphase, die häufig ohne Vorankündigung aktualisiert werden kann. Kunden müssen auf Azurblau gehostet werden (derzeit nur in der Beta-Version für Nordamerika), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an den Adobe-Kundendienst, wenn Sie Zugriff haben möchten.

Mit dem einheitlichen Segmentaufbau können Sie Zielgruppen erstellen, indem Sie Regeln definieren, die auf Daten aus dem [Unified Profile Service](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation.html)basieren.

In diesem Abschnitt werden globale Konzepte beim Erstellen eines Segments vorgestellt. Detaillierte Informationen zum Einheitlichen Segmentaufbau selbst finden Sie im [Segment Builder-Benutzerhandbuch](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/segmentation/segment-builder-guide.md).

Die Benutzeroberfläche des einheitlichen Segmentaufbaus besteht wie folgt:

* Im linken Bereich finden Sie alle verfügbaren Attribute, Ereignisse und Zielgruppen zum Erstellen des Segments durch Ziehen und Ablegen der gewünschten Felder in den Segment Builder-Arbeitsbereich.
* Der mittlere Bereich bietet einen Arbeitsbereich zum Erstellen des Segments, indem Regeln aus den verfügbaren Feldern definiert und kombiniert werden.
* Im Kopf- und rechten Bereich werden die Eigenschaften des Segments (d. h. Name, Beschreibung und geschätzte qualifizierte Profile für das Segment) angezeigt.

![](assets/aep_audiences_interface.png)

## Erstellen eines Segments

Gehen Sie wie folgt vor, um ein Segment zu erstellen:

Der einheitliche Segmentaufbau sollte jetzt in Ihrer Arbeitsfläche angezeigt werden. Damit können Sie ein Segment mithilfe von Daten aus Adobe Experience Platform erstellen, die letztendlich zur Erstellung Ihrer Zielgruppe verwendet werden.

1. Benennen Sie das Segment und geben Sie dann eine Beschreibung ein (optional).

   ![](assets/aep_audiences_creation_edit_name.png)

1. Vergewissern Sie sich, dass die gewünschte Richtlinie für die Zusammenführung im Einstellungsbereich ausgewählt ist.

   Weitere Informationen zu Zusammenführungsrichtlinien finden Sie im entsprechenden Abschnitt des Benutzerhandbuchs zum [Segmentaufbau](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/segmentation/segment-builder-guide.md)

   ![](assets/aep_audiences_mergepolicy.png)

1. Suchen Sie die gewünschten Felder im linken Bereich und ziehen Sie sie in den mittleren Arbeitsbereich.

   ![](assets/aep_audiences_dragfield.png)

1. Konfigurieren Sie die Regeln für die gezogenen Felder.

   ![](assets/aep_audiences_configure_rules.png)

1. Click the **[!UICONTROL Create segment]**button.

## Die richtigen Felder für ein Segment suchen

Im linken Bereich werden alle Attribute, Ereignisse und Zielgruppen aufgelistet, die zum Erstellen von Regeln zur Verfügung stehen.

Die aufgelisteten Felder sind Attribute, die von Ihrem Unternehmen erfasst werden und die über das XDM-System ( [Experience Data Model) verfügbar gemacht werden können](https://www.adobe.io/apis/experienceplatform/home/xdm.html).

Die Felder sind in Registerkarten unterteilt:

* **[!UICONTROL Attribute]**: Vorhandene Profilattribute, die aus Ihrer Adobe Campaign-Datenbank und/oder Adobe Experience Platform stammen können Sie beziehen sich auf statische Informationen, die mit einem Profil verbunden sind (z.B. E-Mail-Adresse, Wohnsitzland, Status des Treueprogramms usw.).

   ![](assets/aep_audiences_attributestab.png)

* **[!UICONTROL Ereignisse]**: Aktivitäten, die Verbraucher identifizieren, die mit den Touchpoints Ihrer Kunden in Kontakt gekommen sind, z. B. &quot;Jeder, der zweimal in zwei Wochen bestellt hat&quot;. Dies kann aus Adobe Analytics gestreamt oder mithilfe von ETL-Tools von Drittanbietern direkt in die Adobe Experience Platform integriert werden.

   ![](assets/aep_audiences_eventstab.png)

>[!NOTE]
>
>**Mit der Segmentierung** mehrerer Entitäten können Sie Profildaten um zusätzliche Daten erweitern, die auf Produkten, Stores oder anderen nicht Profilklassen basieren. Nach der Verbindung stehen Daten aus zusätzlichen Klassen zur Verfügung, als wären sie nativ im Profilschema.
>
>Weiterführende Informationen finden Sie im [entsprechenden Handbuch](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/tutorials/segmentation/multi_entity_segmentation.md).

Standardmäßig zeigt der Unified Segment Builder Felder an, für die Daten vorhanden sind. Um das vollständige Schema anzuzeigen, einschließlich der Felder, für die keine Daten vorhanden sind, aktivieren Sie die Option Vollständiges XDM-Schema ****anzeigen in den Einstellungen.

![](assets/aep_audiences_populatedfields.png)

Das Symbol am Ende jedes Felds enthält weitere Informationen zum Attribut und dessen Verwendung.

![](assets/aep_audiences_isymbol.png)

## Definieren von Regeln für ein Segment

>[!NOTE]
>
>Im folgenden Abschnitt finden Sie globale Informationen zur Regeldefinition. Weitere Informationen finden Sie im [Segment Builder-Benutzerhandbuch](https://www.adobe.io/apis/experienceplatform/home/profile-identity-segmentation/profile-identity-segmentation-services.html#!api-specification/markdown/narrative/technical_overview/segmentation/segment-builder-guide.md).

Gehen Sie zum Erstellen einer Regel wie folgt vor:

1. Suchen Sie im linken Bereich nach dem Feld, das die Attribute oder Ereignisse widerspiegelt, auf denen die Regel basiert.

1. Ziehen Sie das Feld in den mittleren Arbeitsbereich und konfigurieren Sie es dann entsprechend der gewünschten Segmentdefinition. Dazu stehen mehrere Funktionen für Zeichenfolge und Datum/Uhrzeit zur Verfügung.

   Im Beispiel unten zielt die Regel auf alle Profile mit Geschlecht ab, die &quot;Männlich&quot;entsprechen.

   ![](assets/aep_audiences_malegender.png)

   Die geschätzte Population, die dem Segment entspricht, wird im Abschnitt **[!UICONTROL Segmenteigenschaften]**automatisch neu berechnet.

1. Über die Schaltfläche &quot;Profile **[!UICONTROL anzeigen]**&quot;erhalten Sie eine Vorschau der ersten 20 Datensätze, die der Regel entsprechen, sodass Sie das Segment schnell überprüfen können.

   ![](assets/aep_audiences_samplepreview.png)

   Sie können beliebig viele zusätzliche Regeln hinzufügen, um die richtigen Profile als Ziel festzulegen.

   Beim Hinzufügen einer Regel zu einem Behälter wird diese an alle vorhandenen Regeln mit dem UND-Operator angehängt. Klicken Sie auf den Operator, um auf die Option zuzugreifen, um sie in ODER zu ändern.

   ![](assets/aep_audiences_andoperator.png)

Sobald beide Regeln miteinander verknüpft sind, bilden sie einen Behälter.

## Felder vergleichen

Mit dem einheitlichen Segmentaufbau können Sie zwei Felder vergleichen, um eine Regel zu definieren. Weibchen, deren Hausadresse sich beispielsweise in einer anderen Postleitzahl als ihre Arbeitsadresse befindet.

Gehen Sie dazu wie folgt vor:

1. Ziehen Sie das erste Feld, das Sie vergleichen möchten (z. B. die Postleitzahl der Hausadresse) in den Arbeitsbereich der Mitte.

   ![](assets/aep_audiences_comparing_1.png)

1. Wählen Sie das zweite Feld (z. B. die Arbeitsadresse Postleitzahl) aus, das mit dem ersten Feld verglichen wird.

   Ziehen Sie es in den mittleren Arbeitsbereich, im gleichen Container wie das erste Feld, in das Feld **[!UICONTROL Legen Sie hier ab, um Operanden]**zu vergleichen.

   ![](assets/aep_audiences_comparing_2.png)

1. Konfigurieren Sie den Operator zwischen den beiden Feldern nach Bedarf. In diesem Beispiel verlangt unser Segment, dass die Postleitzahl der Hausadresse nicht mit der der Arbeitsadresse übereinstimmt.

   ![](assets/aep_audiences_comparing_3.png)

Die Regel ist jetzt konfiguriert und kann als Zielgruppe aktiviert werden.

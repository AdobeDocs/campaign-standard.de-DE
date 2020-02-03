---
title: Zuordnungsdefinition
description: Erfahren Sie, wie Sie ein Feld "Campaign Standard"einem Feld für ein Erlebnisdatenmodell (XDM) zuordnen.
page-status-flag: never-activated
uuid: 867b1c4b-4c79-4c52-9d0a-ef71993e50a2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: configuring-channels
discoiquuid: 406c955a-b2d2-4099-9918-95f5fa966067
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 67223cf8eed46e2431c03674bd837262e37c7473

---


# Zuordnungsdefinition {#mapping-definition}

>[!IMPORTANT]
>
>Der Campaign Standard-Datendienst befindet sich derzeit in der Betaphase, die möglicherweise ohne Vorankündigung häufig aktualisiert wird. Kunden müssen auf Azurblau gehostet werden (derzeit nur in der Beta-Version für Nordamerika), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an den Adobe-Kundendienst, wenn Sie Zugriff haben möchten.

In diesem Abschnitt erfahren Sie, wie Sie ein Feld &quot;Campaign Standard&quot;einem Feld mit einem Erlebnisdatenmodell (XDM) zuordnen.

Zur Durchführung dieser Aufgabe sind folgende Voraussetzungen erforderlich:

* eine XDM-Schemadefinition über die Schnittstelle oder über die REST-API, die XDM zugeordnet ist
* Dataset-Erstellung basierend auf der XDM-Schemadefinition

1. Gehen Sie zu **[!UICONTROL Administration]**>**[!UICONTROL  Entwicklung]** > **[!UICONTROL Plattform]**und wählen Sie den Eintrag**[!UICONTROL  Datenzuordnungen]** .

1. Klicken Sie auf **[!UICONTROL Erstellen]**, um eine neue XDM-Zuordnung zu starten.

   ![](assets/aep_createmapping.png)

1. Füllen Sie die erforderlichen Felder aus und wählen Sie:

   * eine **Targeting-Dimension**: dies ist das Campaign Standard-Schema, das zugeordnet werden soll
   * ein **Datensatz**: dies ist das Datenpaket, das einem XDM-Schema in Adobe Experience Platform zugeordnet ist.

>[!NOTE]
>
>Damit ein Stapel in Echtzeit-Kundenprofil oder Identitätsdienst integriert werden kann, muss der Datensatz für Echtzeit-Kundenprofil[](https://www.adobe.io/apis/experienceplatform/home/tutorials/alltutorials.html#!api-specification/markdown/narrative/tutorials/data_ingestion_tutorial/data_ingestion_tutorial.md)aktiviert werden.
>
>Wenn der ausgewählte Datensatz bereits in einer vorhandenen Datenzuordnung verwendet wird, wird eine Warnmeldung angezeigt, die Sie darüber informiert, dass Ihre Daten in Adobe Experience Platform überschrieben werden können. Dies kann vorkommen, wenn in Datamappings mit demselben Datensatz einige häufig verwendete Empfänger vorhanden sind.

Im folgenden Bildschirm wird der Abschnitt **[!UICONTROL Feldzuordnungen]**angezeigt, in dem Sie eine neue Zuordnung für jedes Feld im Campaign Standard-Schema erstellen können.

![](assets/aep_fieldmappings.png)

Mit der Schaltfläche **[!UICONTROL Neue Feldzuordnung]**erstellen können Sie das Feld &quot;Campaign Standard&quot;und den entsprechenden Feldpfadausdruck im XDM-Schema auswählen.

Wenn Sie kein Kampagnen-Standard-Feld finden können, können Sie das Suchfeld verwenden, um nach dem Feld zu suchen. Derzeit funktioniert die Suche nur für Felder, die in der Hierarchie geöffnet sind.

![](assets/aep_mapfield.png)

Die in Campaign Standard definierten erweiterten Ressourcen werden allen nativen Feldern zugeordnet. Sie werden in der Erweiterung _customer/default in XDM definiert.

![](assets/aep_fieldscusmapping.png)

Sie können die XDM-Erweiterung über die API anpassen und Ihre eigene Erweiterung definieren, um eine bessere Steuerung der Zuordnung zu ermöglichen.

Weitere Informationen zur XDM-API finden Sie im Tutorial[ zur ](https://www.adobe.io/apis/experienceplatform/home/xdm/xdmservices.html#!api-specification/markdown/narrative/tutorials/schema_registry_api_tutorial/schema_registry_api_tutorial.md)Schemakanzlei.

Um ein Aufzählungsfeld zuzuordnen, müssen Sie den Ausdruckseditor verwenden, um jeden Aufzählungswert zu definieren, der dem XDM-Wert entspricht. So muss zum Beispiel das postAdressfield wie folgt definiert werden:

![](assets/aep_enummapping.png)

Wenn der XDM-Wert als Aufzählung im XDM-Schema definiert ist, können Sie die native EXDM-Funktion verwenden, die die **lif** -Syntax automatisch ersetzt.

![](assets/aep_enummappingexdm.png)

Um eine XDM-Zuordnung zu bearbeiten, öffnen Sie sie, ändern Sie die gewünschten Informationen und speichern Sie sie.

![](assets/aep_editmapping.png)

>[!IMPORTANT]
>
>Wenn Sie zunächst einen Wert im Abschnitt **[!UICONTROL Feldzuordnungen]**bearbeiten und dann außerhalb des Felds klicken, wird die Änderung erst dann auf der Benutzeroberfläche angezeigt, wenn Sie auf die Schaltfläche**[!UICONTROL  Speichern]** klicken. Dieses Verhalten tritt nur einmal auf, wenn die Bearbeitung bei **[!UICONTROL Feldzuordnungen]**die erste Bearbeitung auf der Seite ist.

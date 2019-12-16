---
title: ' Exportieren/Importieren benutzerdefinierter Ressourcen'
description: In diesem Lernprogramm wird erläutert, wie Sie ein Paket mit benutzerdefinierten Ressourcen exportieren und importieren.
page-status-flag: never-activated
uuid: 631f0fbd-9e8d-4f77-a338-fcb7f4fc1774
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: a06509f9-4731-4187-b43d-3bfa361284d3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b10a4b3a81d676e279a9514530158286d58db813

---


# Exporting / importing custom resources {#exporting-importing-custom-resources}

Das Ziel dieser kurzen Einführung besteht darin, den Export und Import eines Packages mit benutzerdefinierten Ressourcen aus einem Entwicklungsumfeld in ein Produktionsumfeld zu zeigen.

Dieses Beispiel ist an funktionale Adobe Campaign-Administratoren gerichtet.

Folgende Voraussetzungen müssen gegeben sein:

* **Eine oder mehrere benutzerdefinierte Ressourcen** , die verfügbar und veröffentlicht sind.

   Darüber hinaus müssen Sie einen eindeutigen Schlüssel für diese Ressourcen definiert haben, da die automatischen Primärschlüssel nicht in die Pakete exportiert werden. Die Ressource kann daher über einen Primärschlüssel und einen zusätzlichen eindeutigen Schlüssel verfügen, um die Einzigartigkeit der Datensätze zu gewährleisten.
* **Der Benutzer muss über die für Package-Erstellung und -Export erforderlichen Berechtigungen** verfügen.

Zusätzliche Ressourcen:

* [Package-Verwaltung](../../automating/using/managing-packages.md)
* [Package-Freigabe: Grundprinzip](../../developing/using/data-model-concepts.md)
* [Ressource hinzufügen oder erweitern](../../developing/using/key-steps-to-add-a-resource.md)

## Struktur exportieren {#exporting-the-structure}

In diesem Schritt nehmen wir einen ersten Package-Export vor, der die Beschreibung der physischen Datenstruktur der benutzerdefinierten Ressource enthält.

Unser Beispiel umfasst zwei benutzerdefinierte Ressourcen: **Artikel** und **Bestellungen**.

1. Gehen Sie zum Menü **[!UICONTROL Administration]** / **[!UICONTROL Bereitstellung]** / **[!UICONTROL Paket-Exporte]** .

   Wir werden ein neues Paket erstellen, um die **[!UICONTROL benutzerdefinierte Ressource (cusResource)]** zu exportieren, die mit den beiden benutzerspezifischen Ressourcen "Produkte"und "Bestellungen"gefiltert wurde.

1. Gehen Sie in **[!UICONTROL Package-Exporte]** und verwenden Sie zur Erstellung eines neuen Packages die Schaltfläche **Erstellen[!UICONTROL .]**
1. Füllen Sie die Beschriftung aus und klicken Sie dann auf Element **[!UICONTROL erstellen]**.

   ![](assets/cusresources_export1.png)

1. Search for and select the **[!UICONTROL Custom resource (cusResource)]**.

   ![](assets/cusresources_export2.png)

1. Configure the details of the **[!UICONTROL Custom resource]** by selecting the two resources, **Products** and **Orders**, in the filtering conditions.

   Vergessen Sie dabei nicht, den logischen Operator zu ändern. Dieser muss **ODER** sein, damit die Struktur beider Ressourcen, "Artikel" und "Bestellungen", in das Package integriert wird.

   ![](assets/cusresources_export3.png)

1. Validieren und speichern Sie das definierte Package.

Sie können nun mithilfe der gleichnamigen Schaltfläche den **[!UICONTROL Export starten]**.

![](assets/cusresources_export4.png)

Auf das erstellte Package kann im Download-Ordner zugegriffen werden. Der Name der zip-Datei wird nach dem Zufallsprinzip vergeben. Sie können die Datei bei Bedarf umbenennen.

## Daten exportieren {#exporting-the-data}

Mithilfe dieses zweiten Exports lassen sich die Daten der benutzerdefinierten Ressourcen **Artikel** und **Bestellungen** exportieren.

Bei der Erstellung des zweiten, die Daten enthaltenden Packages können Sie sich auf den gleichen Exporttyp wie für den Strukturexport stützen.

1. Gehen Sie in **[!UICONTROL Package-Exporte]** und verwenden Sie zur Erstellung eines neuen Packages die Schaltfläche **Erstellen[!UICONTROL .]**
1. Vergeben Sie den Titel **[!UICONTROL Daten meiner Ressourcen exportieren]** und verwenden Sie im Anschluss im Tab **[!UICONTROL Definition des Exports]die Schaltfläche** Element erstellen **.**
1. Wählen Sie **Artikel** aus der Liste der Ressourcen aus.

   ![](assets/cusresources_exportdata1.png)

1. Konfigurieren Sie eine erweiterte **Filterbedingung** mit **@Label IS NOT NULL**.

   ![](assets/cusresources_exportdata2.png)

1. Überprüfen Sie die Anzahl.

   ![](assets/cusresources_exportdata3.png)

1. Wiederholen Sie den gleichen Vorgang für die benutzerdefinierte Ressource **Bestellungen**.

   ![](assets/cusresources_exportdata4.png)

1. Validieren und speichern Sie das definierte Package.

Sie können nun mithilfe der gleichnamigen Schaltfläche den **[!UICONTROL Export starten]**.

![](assets/cusresources_exportdata5.png)

Auf das erstellte Package kann im Download-Ordner zugegriffen werden. Der Name der zip-Datei wird nach dem Zufallsprinzip vergeben. Sie können die Datei bei Bedarf umbenennen.

## Struktur importieren {#importing-the-structure}

### Package importieren {#importing-the-structure-package}

1. Loggen Sie sich in die **Zielinstanz** ein, in die Sie die gerade erstellten Packages importieren möchten.
1. Go to the **[!UICONTROL Administration]** / **[!UICONTROL Deployment]** / **[!UICONTROL Package imports]** menu to create a new package to import the file from the first export.
1. Ziehen Sie die **Strukturdatei** in den dafür vorgesehenen Bereich. Es werden die Formate ZIP oder XML unterstützt.

   ![](assets/cusresources_import2.png)

1. Ändern Sie den Titel z. B. in **Struktur importieren** um und **[!UICONTROL Speichern Sie]**.
1. Verwenden Sie die Schaltfläche **[!UICONTROL Import starten]**.

   ![](assets/cusresources_import3.png)

### Publizieren {#publish-structure}

1. Go to the **[!UICONTROL Administration]** / **[!UICONTROL Development]** / **[!UICONTROL Publication]** menu.
1. Verwenden Sie die Schaltflächen **[!UICONTROL Publikation vorbereiten]** und anschließend **Publizieren], um die Instanz mit der Struktur der neuen benutzerdefinierten Ressourcen zu aktualisieren.[!UICONTROL **
1. Die dem installierten Package entsprechenden Menüeinträge fügen sich in das Menü **[!UICONTROL Benutzerdefinierte Daten]ein.**

   ![](assets/cusresources_import1.png)

## Daten importieren {#importing-the-data}

In diesem Schritt werden wir die mit dem im vorangehenden Schritt in der Instanz installierten Package verknüpften **Daten importieren**.

Der Schritt ist hier ebenfalls in zwei Etappen unterteilt: den Package-Import und eine Publikation.

### Package importieren {#importing-the-data-package}

1. Go to the **[!UICONTROL Administration]** / **[!UICONTROL Deployment]** / **[!UICONTROL Package imports]** menu to create a new package to import the file containing the data.
1. Ziehen Sie die Datendatei in den dafür vorgesehenen Bereich. Es werden die Formate ZIP oder XML unterstützt.
1. Modify the label, for example "Import data", then click **[!UICONTROL Save]**.
1. Verwenden Sie die Schaltfläche **[!UICONTROL Import starten]**.

   ![](assets/cusresources_importdata.png)

### Publizieren {#publish-data}

1. Go to the **[!UICONTROL Administration]** / **[!UICONTROL Development]** / **[!UICONTROL Publication]** menu.
1. Verwenden Sie die Schaltflächen **[!UICONTROL Publikation vorbereiten]** und anschließend **Publizieren], um die Instanz mit den Daten der benutzerdefinierten Ressourcen zu aktualisieren.[!UICONTROL **

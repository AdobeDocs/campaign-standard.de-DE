---
title: Mapping-Definition
description: Erfahren Sie, wie Sie ein Campaign Standard-Feld auf ein XDM-Feld (Experience-Datenmodell) abbilden.
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
translation-type: ht
source-git-commit: c2ed4b3c85ceef3b604a8f68d924c7e5d9fad900
workflow-type: ht
source-wordcount: '516'
ht-degree: 100%

---


# Mapping-Definition {#mapping-definition}

>[!IMPORTANT]
>
>Adobe Experience Platform Data Connector befindet sich derzeit in der Betaphase, die häufig ohne Vorankündigung aktualisiert werden kann. Kunden müssen auf Azure gehostet werden (derzeit nur für Nordamerika in der Betaphase), um auf diese Funktionen zugreifen zu können. Wenden Sie sich an die Adobe-Kundenunterstützung, wenn Sie Zugriff haben möchten.

In diesem Abschnitt erfahren Sie, wie Sie ein Campaign Standard-Feld auf ein XDM-Feld (Experience-Datenmodell) abbilden.

Zur Durchführung dieser Aufgabe sind folgende Voraussetzungen erforderlich:

* XDM-Schemadefinition über die Oberfläche oder die REST-API, die XDM zugeordnet ist
* Datensatzerstellung anhand der XDM-Schemadefinition

1. Gehen Sie zu **[!UICONTROL Administration]** > **[!UICONTROL Entwicklung]** > **[!UICONTROL Plattform]** und wählen Sie den Eintrag **[!UICONTROL Daten-Mappings]** aus.

1. Klicken Sie auf **[!UICONTROL Erstellen]**, um ein neues XDM-Mapping zu starten.

   ![](assets/aep_createmapping.png)

1. Füllen Sie die erforderlichen Felder aus und wählen Sie:

   * eine **Zielgruppendimension**: dies ist das Campaign Standard-Schema, das abgebildet werden soll
   * einen **Datensatz**: dies ist das Datenpaket, das einem XDM-Schema in Adobe Experience Platform zugeordnet ist.

>[!NOTE]
>
>Damit ein Batch in das Echtzeit-Kundenprofil oder den Identitätsdienst aufgenommen werden kann, muss der Datensatz für [Echtzeit-Kundenprofil aktiviert](https://docs.adobe.com/content/help/de-DE/experience-platform/rtcdp/intro/get-started.html) werden.
>
>Wenn der ausgewählte Datensatz bereits in einem vorhandenen Daten-Mapping verwendet wird, wird ein Warnhinweis angezeigt, der Sie darüber informiert, dass Ihre Daten in Adobe Experience Platform möglicherweise überschrieben werden. Dies kann passieren, wenn es einige gemeinsame Empfänger in Daten-Mappings gibt, die den gleichen Datensatz verwenden.

Im folgenden Bildschirm wird der Abschnitt **[!UICONTROL Feld-Mappings]** angezeigt, in dem Sie für jedes Feld im Campaign Standard-Schema ein neues Mapping erstellen können.

![](assets/aep_fieldmappings.png)

Mit der Schaltfläche **[!UICONTROL Neues Feld-Mapping erstellen]** können Sie das Campaign Standard-Feld und den entsprechenden Feldpfadausdruck im XDM-Schema auswählen.

Wenn Sie ein Campaign Standard-Feld nicht finden können, können Sie das Suchfeld verwenden, um nach dem Feld zu suchen. Derzeit funktioniert die Suche nur für Felder, die in der Hierarchie geöffnet sind.

![](assets/aep_mapfield.png)

Die in Campaign Standard definierten erweiterten Ressourcen werden wie alle nativen Felder abgebildet. Sie werden in der _customer/default-Erweiterung in XDM definiert.

![](assets/aep_fieldscusmapping.png)

Sie können die XDM-Erweiterung über die API anpassen und Ihre eigene Erweiterung definieren, um die Kontrolle über das Mapping zu verbessern.

Weitere Informationen zur XDM-API finden Sie im [Tutorial zur Schema Registry-API](https://docs.adobe.com/content/help/de-DE/experience-platform/xdm/api/getting-started.html).

Um ein Auflistungsfeld abzubilden, müssen Sie den Ausdruckseditor verwenden, um jeden Auflistungswert zu definieren, der dem XDM-Wert entspricht. So muss zum Beispiel postAdressfield wie folgt definiert werden:

![](assets/aep_enummapping.png)

Wenn der XDM-Wert als Auflistung im XDM-Schema definiert ist, können Sie die native EXDM-Funktion verwenden, die die **lif**-Syntax automatisch ersetzt.

![](assets/aep_enummappingexdm.png)

Um ein XDM-Mapping zu bearbeiten, öffnen Sie es, ändern Sie die gewünschten Informationen und speichern Sie es.

![](assets/aep_editmapping.png)

>[!IMPORTANT]
>
>Wenn Sie zunächst einen Wert im Abschnitt **[!UICONTROL Feld-Mappings]** bearbeiten und dann außerhalb des Felds klicken, wird die Änderung erst dann auf der Benutzeroberfläche angezeigt, wenn Sie auf die Schaltfläche **[!UICONTROL Speichern]** klicken. Dieses Verhalten tritt nur einmal auf, wenn die Bearbeitung bei **[!UICONTROL Feld-Mappings]** die erste Bearbeitung auf der Seite ist.

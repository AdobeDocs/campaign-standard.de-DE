---
title: Filterdefinition konfigurieren
description: Hier erfahren Sie mehr über die Filterfunktion zur Verwaltung großer Datenmengen.
page-status-flag: never-activated
uuid: c9db95fe-e9aa-40f8-9c0a-e74bb21ac14b
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: 993ab2bd-e05f-468e-9ef8-a603761247f8
context-tags: cusResource,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Filterdefinition konfigurieren{#configuring-filter-definition}

Sie können im Tab **[!UICONTROL Filterdefinition]** erweiterte Filter erstellen, auf die Benutzer anschließend direkten Zugriff haben, wenn sie komplexe Abfragen wie beispielsweise die Definition einer Audience erstellen.

Dieser Schritt ist nicht zwingend erforderlich, da dennoch Daten in Ihre Ressource geladen werden können und Sie darauf über Workflows, Audiences und REST-API zugreifen können.

![](assets/custom_resource_filter-definition.png)

Diese Filter finden im Abfrageeditor in Form von vorkonfigurierten Regeln Verwendung. Durch sie können die Schritte zum Erhalt der gewünschten Konfiguration reduziert werden, was insbesondere für den Fall wiederholter Segmentierungen von Interesse ist.

Sie können zum Beispiel einen Filter definieren, mit dem Sie alle Transaktionen auswählen können, die innerhalb der letzten drei Monate einen bestimmten Wert überstiegen haben.

Erweitern Sie dazu die Ressource **[!UICONTROL Profile]**, definieren Sie einen Filter und verknüpfen Sie ihn über eine Regel mit einer zuvor erstellten Transaktionstabelle. Definieren Sie in der Regel, dass der Transaktionspreis größer oder gleich einem bestimmten Parameter sein muss und das Transaktionsdatum in einem Zeitraum innerhalb der letzten drei Monate liegen muss.

1. Beachten Sie dabei, dass Sie eine Transaktionstabelle erstellen und publizieren müssen. Siehe auch [Ressource erstellen oder erweitern](../../developing/using/creating-or-extending-the-resource.md).

   >[!NOTE]
   >
   >In diesem Beispiel wird eine benutzerdefinierte Transaktionstabelle verwendet. Sie können diese auf Ihre eigenen Geschäftsanforderungen anpassen.

1. Bevor Sie in der Ressource **[!UICONTROL Profile]** einen mit der Transaktionstabelle verknüpften Filter definieren, müssen Sie die Relation mit dieser Tabelle definieren und Ihre Änderungen publizieren. Siehe auch [Relationen mit anderen Ressourcen definieren](../../developing/using/configuring-the-resource-s-data-structure.md#defining-links-with-other-resources) und [Datenbankstruktur aktualisieren](../../developing/using/updating-the-database-structure.md).
1. Wählen Sie im Tab **[!UICONTROL Definition]** des Definitionsbildschirms des neuen Filters die Transaktionstabelle aus.

   ![](assets/custom_resource_filter-definition_example-empty.png)

1. Ziehen Sie im Fenster **[!UICONTROL Regel hinzufügen - Profile/Transaktionen]** die Transaktionstabelle in den Arbeitsbereich. Wählen Sie im nächsten Fenster das Feld, das Sie verwenden möchten.

   ![](assets/custom_resource_filter-definition_example-field.png)

1. Aktivieren Sie im Fenster **[!UICONTROL Regel hinzufügen - Transaktionen]** unter **[!UICONTROL Optionale Parametereinstellungen]** die Option **[!UICONTROL In den Parametermodus wechseln]**.

   Wählen Sie in den **[!UICONTROL Filterbedingungen]** den Operator **[!UICONTROL Größer oder gleich]**. Geben Sie im **[!UICONTROL Parameter]**-Feld einen Namen ein und klicken Sie auf das Pluszeichen, um den neuen Parameter zu erstellen.

   ![](assets/custom_resource_filter-definition_example-parameter.png)

1. Bestätigen Sie Ihre Änderungen. Hierbei handelt es sich um das konfigurierbare Eingabefeld, in das der Benutzer später zur Ausführung seiner Abfrage einfach einen Wert eintragen muss.

   ![](assets/custom_resource_filter-definition_ex_edit-rule.png)

1. Kombinieren Sie diese Regel mit einer anderen Regel, die besagt, dass das Datum in einem die letzten drei Monate umfassenden Zeitraum liegen muss.

   ![](assets/custom_resource_filter-definition_example.png)

1. Wählen Sie die Kategorie aus, in der Ihr Filter erscheinen soll.

   ![](assets/custom_resource_filter-definition_category.png)

1. Passen Sie im **[!UICONTROL Parameter]**-Tab des Bildschirms zur Filterdefinition Beschreibung und Titel des Filters an, um den Benutzern den Betreff Ihres Filters zu verdeutlichen. Ebendiese Informationen werden im Abfrageeditor angezeigt.

   ![](assets/custom_resource_filter-definition_parameters.png)

   Sollten Sie mehrere konfigurierbare Felder definieren, können Sie die Reihenfolge ändern, in der diese in der Benutzeroberfläche angezeigt werden.

1. Speichern Sie Ihre Änderungen und publizieren Sie die Ressourcen. Weiterführende Informationen finden Sie im Abschnitt [Datenbankstruktur aktualisieren](../../developing/using/updating-the-database-structure.md).

Sobald die Erweiterung der **[!UICONTROL Profile]**-Ressource publiziert wurde, ist der Filter für Benutzer in den Schnellzugriffen der [Abfrageeditor](../../automating/using/editing-queries.md)-Benutzeroberfläche sichtbar.

Bei der Erstellung einer E-Mail können Benutzer auf diese Weise einfach ihre Audience so definieren, dass die Nachricht an alle Kunden gesendet wird, die in den letzten drei Monaten einen gewissen Betrag ausgegeben haben.

![](assets/custom_resource_filter-definition_email-audience.png)

Dafür haben Benutzer lediglich den gewünschten Betrag in der angezeigten Dialogbox einzugeben, anstatt die Konfiguration selbst vornehmen zu müssen.

![](assets/custom_resource_filter-definition_email-audience_filter.png)


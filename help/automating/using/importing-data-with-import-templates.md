---
title: Datenimport mit Importvorlagen
description: Hier erfahren Sie, wie Sie für Ihre Campaign-Datenbank Daten sammeln können.
page-status-flag: never-activated
uuid: bfc03235-2032-448a-a9ed-21ff2a83fa09
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
discoiquuid: fb511bb8-6be7-43f6-86ab-94d5cfa3efc9
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 68e825bc3b6b7f94f61875e7da2bc8f63f06d9cb

---


# Datenimport mit Importvorlagen{#importing-data-with-import-templates}

Durch den Datenimport können Sie Daten erfassen und Ihre Adobe-Campaign-Datenbank erweitern.

Adobe Campaign bietet eine vereinfachte Importfunktion, welche unter bestimmten Bedingungen eine Alternative zur Verwendung komplexerer [Workflow](../../automating/using/get-started-workflows.md)-Aktivitäten darstellt.

Das Prinzip dahinter sieht wie folgt aus: Ein **Administrator** definiert und verwaltet Importvorlagen (siehe [Importvorlagen konfigurieren](../../automating/using/defining-import-templates.md)). These import templates are then made available to users with simplified views under the **[!UICONTROL Profiles & audiences]** > **[!UICONTROL Imports]** menu.

Die Benutzer müssen lediglich den gewünschten Importtyp auswählen und die Datei mit den zu importierenden Daten hochladen. Für den Benutzer transparent wird nun der zuvor durch den Administrator konfigurierte Workflow ausgeführt. Nach Abschluss des Imports kann der Benutzer auf das Ergebnis des Imports zugreifen.

>[!NOTE]
>
>Import data function can be managed by users with **[!UICONTROL GENERIC IMPORT (import)]** and **[!UICONTROL WORKFLOW (workflow)]** roles. Weiterführende Informationen zu Benutzerrollen finden Sie in [diesem Abschnitt](../../administration/using/list-of-roles.md).

Die Importliste kann nach der zugrunde liegenden Vorlage, dem Ausführungsdatum und -status gefiltert werden.

1. From the imports overview, click the **[!UICONTROL Create]** button. um den Importassistenten zu öffnen.
1. Wählen Sie den gewünschten Importtyp aus. Die Importtypen entsprechen den verfügbaren Importvorlagen.
1. Laden Sie bei Bedarf die in der Vorlage enthaltene Beispieldatei herunter, um sicherzustellen, dass die in der zu importierenden Datei enthaltenen Daten den erwarteten Datentypen entsprechen.
1. Laden Sie die Datei mit den zu importierenden Daten im Assistenten hoch.
1. Starten Sie den Import. Der Assistent wird geschlossen und Sie werden zur Liste der anhand der verwendeten Vorlage realisierten Importe weitergeleitet.
1. Aktualisieren Sie die Seite und wählen Sie den zuvor ausgeführten Import aus, um die Ausführungsdetails anzuzeigen.

   ![](assets/simplified_import1.png)

Die Ausführungsdetails sind jetzt verfügbar. Sie haben somit die Möglichkeit, die importierte Datei sowie eine die Zurückweisungen, d. h. nicht importierte Daten, enthaltende Datei herunterzuladen.

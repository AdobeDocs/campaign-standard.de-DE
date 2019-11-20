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
translation-type: ht
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Datenimport mit Importvorlagen{#importing-data-with-import-templates}

Durch den Datenimport können Sie Daten erfassen und Ihre Adobe-Campaign-Datenbank erweitern.

Adobe Campaign bietet eine vereinfachte Importfunktion, welche unter bestimmten Bedingungen eine Alternative zur Verwendung komplexerer [Workflow](../../automating/using/discovering-workflows.md)-Aktivitäten darstellt.

Das Prinzip dahinter sieht wie folgt aus: Ein **Administrator** definiert und verwaltet Importvorlagen (siehe [Importvorlagen konfigurieren](../../automating/using/defining-import-templates.md)). Diese Importvorlagen werden dann Benutzern im Menü **[!UICONTROL Profile &amp; Audiences]** &gt; **[!UICONTROL Importe]** mit vereinfachten Ansichten zur Verfügung gestellt.

Die Benutzer müssen lediglich den gewünschten Importtyp auswählen und die Datei mit den zu importierenden Daten hochladen. Für den Benutzer transparent wird nun der zuvor durch den Administrator konfigurierte Workflow ausgeführt. Nach Abschluss des Imports kann der Benutzer auf das Ergebnis des Imports zugreifen.

>[!NOTE]
>
>Die Datenimportfunktion kann von Benutzern mit den Benutzerrollen **[!UICONTROL ALLGEMEINER IMPORT (import)]** und **[!UICONTROL WORKFLOW (workflow)]** verwaltet werden. Weiterführende Informationen zu Benutzerrollen finden Sie in [diesem Abschnitt](../../administration/using/list-of-roles.md).

Die Importliste kann nach der zugrunde liegenden Vorlage, dem Ausführungsdatum und -status gefiltert werden.

1. Verwenden Sie in der Importübersicht die **[!UICONTROL Erstellen]**-Schaltfläche, um den Importassistenten zu öffnen.
1. Wählen Sie den gewünschten Importtyp aus. Die Importtypen entsprechen den verfügbaren Importvorlagen.
1. Laden Sie bei Bedarf die in der Vorlage enthaltene Beispieldatei herunter, um sicherzustellen, dass die in der zu importierenden Datei enthaltenen Daten den erwarteten Datentypen entsprechen.
1. Laden Sie die Datei mit den zu importierenden Daten im Assistenten hoch.
1. Starten Sie den Import. Der Assistent wird geschlossen und Sie werden zur Liste der anhand der verwendeten Vorlage realisierten Importe weitergeleitet.
1. Aktualisieren Sie die Seite und wählen Sie den zuvor ausgeführten Import aus, um die Ausführungsdetails anzuzeigen.

   ![](assets/simplified_import1.png)

Die Ausführungsdetails sind jetzt verfügbar. Sie haben somit die Möglichkeit, die importierte Datei sowie eine die Zurückweisungen, d. h. nicht importierte Daten, enthaltende Datei herunterzuladen.

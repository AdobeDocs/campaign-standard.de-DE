---
title: Datenimport mit Importvorlagen
seo-title: Datenimport mit Importvorlagen
description: Datenimport mit Importvorlagen
seo-description: Hier erfahren Sie, wie Sie für Ihre Campaign-Datenbank Daten sammeln können.
page-status-flag: nie aktiviert
uuid: bfc 03235-2032-448 a-a 9 ed -21 ff 2 a 83 fa 09
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird automatisiert
content-type: Referenz
topic-tags: import-and-exporting-data
discoiquuid: fb 511 bb 8-6 be 7-43 f 6-86 ab -94 d 5 cfa 3 efc 9
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Datenimport mit Importvorlagen{#importing-data-with-import-templates}

Durch den Datenimport können Sie Daten erfassen und Ihre Adobe-Campaign-Datenbank erweitern.

Adobe Campaign bietet eine vereinfachte Importfunktion, welche unter bestimmten Bedingungen eine Alternative zur Verwendung komplexerer [Workflow](../../automating/using/discovering-workflows.md)-Aktivitäten darstellt.

Das Prinzip dahinter sieht wie folgt aus: Ein **Administrator** definiert und verwaltet Importvorlagen (siehe [Importvorlagen konfigurieren](../../automating/using/defining-import-templates.md)). These import templates are then made available to users with simplified views under the **[!UICONTROL Profiles &amp; audiences]** &gt; **[!UICONTROL Imports]** menu.

Die Benutzer müssen lediglich den gewünschten Importtyp auswählen und die Datei mit den zu importierenden Daten hochladen. Für den Benutzer transparent wird nun der zuvor durch den Administrator konfigurierte Workflow ausgeführt. Nach Abschluss des Imports kann der Benutzer auf das Ergebnis des Imports zugreifen.

>[!NOTE]
>
>Die Datenimportfunktion kann von Benutzern mit den Benutzerrollen **[!UICONTROL ALLGEMEINER IMPORT (import)]** und **[!UICONTROL WORKFLOW (workflow)]** verwaltet werden. Weiterführende Informationen zu Benutzerrollen finden Sie in [diesem Abschnitt](../../administration/using/list-of-roles.md).

Die Importliste kann nach der zugrunde liegenden Vorlage, dem Ausführungsdatum und -status gefiltert werden.

1. Verwenden Sie in der Importübersicht die **[!UICONTROL Erstellen]-Schaltfläche,** um den Importassistenten zu öffnen.
1. Wählen Sie den gewünschten Importtyp aus. Die Importtypen entsprechen den verfügbaren Importvorlagen.
1. Laden Sie bei Bedarf die in der Vorlage enthaltene Beispieldatei herunter, um sicherzustellen, dass die in der zu importierenden Datei enthaltenen Daten den erwarteten Datentypen entsprechen.
1. Laden Sie die Datei mit den zu importierenden Daten im Assistenten hoch.
1. Starten Sie den Import. Der Assistent wird geschlossen und Sie werden zur Liste der anhand der verwendeten Vorlage realisierten Importe weitergeleitet.
1. Aktualisieren Sie die Seite und wählen Sie den zuvor ausgeführten Import aus, um die Ausführungsdetails anzuzeigen.

   ![](assets/simplified_import1.png)

Die Ausführungsdetails sind jetzt verfügbar. Sie haben somit die Möglichkeit, die importierte Datei sowie eine die Zurückweisungen, d. h. nicht importierte Daten, enthaltende Datei herunterzuladen.

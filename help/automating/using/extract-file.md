---
title: Dateiextraktion
seo-title: Dateiextraktion
description: Dateiextraktion
seo-description: Die Dateiextraktionsaktivität erlaubt den Export von in Adobe Campaign enthaltenen Daten in Form von externen Dateien.
page-status-flag: nie aktiviert
uuid: 631 f 0 fbd -9 e 8 d -4 f 77-a 338-fcb 7 f 4 fc 1774
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird automatisiert
content-type: Referenz
topic-tags: data-management-activities
discoiquuid: a 06509 f 9-4731-4187-b 43 d -3 bfa 361284 d 3
context-tags: Fileexport, main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e384a0cef325bc01eb5ea050b0f3d926aea9a88f

---


# Dateiextraktion{#extract-file}

## Beschreibung {#description}

![](assets/export.png)

Die Aktivität **[!UICONTROL Dateiextraktion]erlaubt den Export von in Adobe Campaign enthaltenen Daten in Form von externen Dateien.**

## Anwendungskontext {#context-of-use}

Die Art der Datenextraktion wird im Zuge der Aktivitätskonfiguration definiert.

>[!CAUTION]
>
>Die Aktivität **[!UICONTROL Dateiextraktion]** kann nur im Anschluss an eine **Abfrage]-Aktivität verwendet werden.[!UICONTROL **

## Konfiguration {#configuration}

1. Ziehen Sie eine **[!UICONTROL Dateiextraktion]in den Workflow-Arbeitsbereich.**

   ![](assets/wkf_data_export1.png)

1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der ![-Schaltfläche aus den angezeigten Quick Actions.](assets/edit_darkgrey-24px.png)
1. Geben Sie den Titel der **Ausgabedatei** an. Der Dateiname wird automatisch mit dem Datum und der Uhrzeit der Erstellung ergänzt, um seine Eindeutigkeit zu gewährleisten, z. B.: Empfänger_20150815_081532.txt für eine Datei, die am 15. August 2015 um 8.15 Uhr und 32 Sekunden erstellt wurde.

   >[!NOTE]
   >
   >Sie können den Dateinamen mit der in diesem Feld befindlichen Funktion **[!UICONTROL formatDate]spezifizieren.**

1. Sie können die Ausgabedatei bei Bedarf komprimieren, indem Sie im Feld **[!UICONTROL Anschlussvorgangsetappe hinzufügen]** die Option **Komprimierung]auswählen.[!UICONTROL ** Die Ausgabedatei wird in eine GZIP-Datei (.gz) komprimiert.
1. Fügen Sie mithilfe der Schaltflächen ![](assets/add_darkgrey-24px.png) oder **Element hinzufügen]eine Ausgabespalte hinzu.[!UICONTROL **

   ![](assets/wkf_data_export2.png)

   Es öffnet sich ein neues Fenster.

   ![](assets/wkf_data_export3.png)

1. Erstellen Sie einen Ausdruck. Hierzu können Sie einen bereits existierenden Ausdruck auswählen oder mit dem **Ausdruckseditor** einen neuen erstellen.
1. Validieren Sie den Ausdruck.

   Der Ausdruck wird den Ausgabespalten hinzugefügt.

1. Erstellen Sie so viele Spalten wie nötig. Klicken Sie zur Bearbeitung der Spalten auf deren Ausdruck oder Titel.

   Wenn Sie Profile exportieren, um sie in einem externen Tool zu verwenden, empfehlen wir auch den Export einer eindeutigen Kennung. Nicht alle Profile verfügen standardmäßig über eine eindeutige Kennung. Dies hängt von der Weise ab, wie sie zur Datenbank hinzugefügt werden. Weiterführende Informationen finden Sie im Abschnitt [Eindeutige Kennung für Profile erstellen](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources).

1. Klicken Sie auf den **[!UICONTROL Dateistruktur]-Tab, um das Ausgabe-, Datums- und Zahlenformat der zu exportierenden Datei zu konfigurieren.**

   Wenn Sie Auflistungswerte exportieren, aktivieren Sie die Option **[!UICONTROL Titel anstelle der internen Werte der Auflistungen exportieren.]** Mit dieser Option können Sie kürzere Titel abrufen, die einfacher verständlich sind als IDs.

1. Wählen Sie im Tab **[!UICONTROL Eigenschaften]** die Option **Keine Datei erstellen, wenn die eingehende Transition leer ist]aus, um zu verhindern, dass leere Dateien erstellt und auf SFTP-Server hochgeladen werden, wenn die eingehende Transition leer ist.[!UICONTROL **
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

## Beispiel {#example}

Im folgenden Beispiel wird die Konfiguration einer auf eine **[!UICONTROL Abfrage]** folgenden **Dateiextraktion]erläutert.[!UICONTROL **

Ziel dieses Workflows ist es, eine Profilliste in eine externe Datei zu exportieren, um die Daten außerhalb von Adobe Campaign verwenden zu können.

1. Platzieren Sie eine **[!UICONTROL Dateiextraktion]** im Anschluss an eine **Abfrage]im Workflow-Arbeitsbereich.[!UICONTROL **

   Im vorliegenden Beispiel werden alle Profile im Alter von 18 bis 30 Jahren aus der Datenbank abgefragt.

1. Öffnen Sie die Dateiextraktion, um sie zu konfigurieren.
1. Benennen Sie die Ausgabedatei.
1. Fügen Sie die gewünschten Ausgabespalten hinzu.

   Im vorliegenden Beispiel sind dies E-Mail-Adresse, Alter, Geburtsdatum, Vor- und Nachname der abgefragten Profile.

   ![](assets/wkf_data_export6.png)

1. Gehen Sie in den **[!UICONTROL Dateistruktur]-Tab und definieren Sie folgende Elemente:**

   * CSV als Ausgabeformat,

      ![](assets/wkf_data_export7.png)

   * Datumsformat,

      ![](assets/wkf_data_export9.png)

1. Validieren Sie die Aktivität.
1. Platzieren Sie nun im Anschluss an die **[!UICONTROL Dateiextraktion]** eine **Dateiübertragung], um die Extraktionsdatei mittels eines externen Kontos abrufen zu können.[!UICONTROL **
1. Öffnen Sie die Aktivität und wählen Sie die Aktion **[!UICONTROL Datei-Upload]aus.**

   ![](assets/wkf_data_export11.png)

1. Wählen Sie ein externes Konto aus und geben Sie den Pfad des Ordners auf dem Server an.

   ![](assets/wkf_data_export12.png)

1. Validieren Sie die Aktivität und speichern Sie den Workflow.
1. Starten Sie den Workflow.

   Nach erfolgreicher Ausführung des Workflows ist die Extraktionsdatei im externen Konto verfügbar.


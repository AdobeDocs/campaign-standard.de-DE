---
title: Dateiübertragung
description: Die Dateiübertragungsaktivität ermöglicht den Empfang und Versand von Dateien. Ferner können Sie damit die Präsenz von Dateien testen und die in Adobe Campaign vorhandenen Dateien auflisten.
page-status-flag: never-activated
uuid: a2f18118-b681-4310-aee0-9e82179d2032
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: data-management-activities
discoiquuid: 752f2aed-f897-485e-b329-f3cc1756ee8e
context-tags: fileTransfer,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7f203ff0e635faf802a5577f761dc308dae4ab66

---


# Dateiübertragung{#transfer-file}

## Beschreibung {#description}

![](assets/file_transfer.png)

The **[!UICONTROL Transfer file]** activity allows you to receive or send files, test whether there are files present, or list files in Adobe Campaign.

## Anwendungskontext {#context-of-use}

Die Art der Datenextraktion wird im Zuge der Aktivitätskonfiguration definiert. Bei der zu ladenden Datei kann es sich z. B. um eine Kontaktliste handeln.

You can use this activity to recover data that will then be structured with the **[!UICONTROL Load file]** activity.

## Konfiguration {#configuration}

1. Legen Sie eine **[!UICONTROL Transfer file]** Aktivität in Ihren Workflow ein.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der im Schnellzugriff angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. Use the drop-down list in the **[!UICONTROL Action]** field to select one of the following activity actions:

   ![](assets/wkf_file_transfer_01.png)

   * **Datei-Download** - dient dem Herunterladen von Dateien.
   * **Datei-Upload** - dient dem Hochladen von Dateien. Uploading a file from Adobe Campaign file generates a log entry in the **[!UICONTROL Export audits]** menu. Weiterführende Informationen zu Export-Audits finden Sie im Abschnitt [Log-Exporte überprüfen](../../administration/using/auditing-export-logs.md).
   * **Existenztest einer Datei** - dient der Prüfung des Vorhandenseins einer Datei.
   * **Dateiliste**: ermöglicht die Liste der auf dem Server vorhandenen Dateien, die auf der **[!UICONTROL Protocol]** Registerkarte definiert sind. Diese Aktion wird hauptsächlich zum Debugging verwendet, um zu überprüfen, ob die Aktivität Ihren Anforderungen entsprechend konfiguriert ist, bevor die Dateien vom Remote-Server heruntergeladen werden.

1. Wählen Sie das gewünschte Protokoll aus:
   * [HTTP](#HTTP-configuration-wf)
   * [SFTP](#SFTP-configuration-wf)
   * [Amazon S3](#S3-configuration-wf)
   * [Microsoft Azure Blob Storage](#azure-blob-configuration-wf)
   * [Auf dem Adobe Campaign-Server vorhandene Datei(en)](#files-server-configuration-wf)

1. The **[!UICONTROL Additional options]** section, available depending on the protocol selected, allows you to add parameters to your protocol. Sie haben folgende Möglichkeiten:

   * **[!UICONTROL Delete the source files after transfer]**
   * **[!UICONTROL Disable passive mode]**
   * **[!UICONTROL List all files]**: Diese Option ist verfügbar, wenn Sie die **[!UICONTROL File listing]** Aktion.in der **[!UICONTROL General]** Registerkarte auswählen. Mithilfe dieser Option können alle auf dem Server verfügbaren Dateien in der Ereignisvariable **vars.filenames** verzeichnet werden. Darin sind die Dateinamen durch die Zeichen **&#39;n&#39;** getrennt.

1. The **[!UICONTROL If no files are found]** section of the **[!UICONTROL Advanced options]** tab allows you to configure specific actions if any errors or inexistent files are detected when the activity is started.

   Sie können darüber hinaus Neuversuche definieren. Die einzelnen Versuche erscheinen im Ausführungsprotokoll des Workflows.

   ![](assets/wkf_file_transfer_09.png)

1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.

### Konfiguration mit HTTP {#HTTP-configuration-wf}

Mit dem HTTP-Protokoll können Sie Beginn beim Herunterladen einer Datei aus einem Externe Konto oder einer URL ausführen.

Mit diesem Programm können Sie eine **[!UICONTROL Use connection parameters defined in an external account]** Option wählen. Wählen Sie in diesem Fall das gewünschte Konto aus und geben Sie den Pfad der herunterzuladenden Datei an.
![](assets/wkf_file_transfer_03.png)

Sie können auch die **[!UICONTROL Quick configuration]** Option auswählen. Sie müssen nur die URL in das Feld URL eingeben.
![](assets/wkf_file_transfer_04.png)

### Konfiguration mit SFTP {#SFTP-configuration-wf}

Mit dem SFTP-Protokoll können Sie Beginn beim Herunterladen einer Datei von einer URL oder einem Externe Konto ausführen.

Mit diesem Programm können Sie die **[!UICONTROL Use connection parameters defined in an external account]** Option auswählen, dann das gewünschte Konto auswählen und den Pfad der Datei zum Herunterladen angeben.
![](assets/wkf_file_transfer_07.png)

>[!CAUTION]
>
>Die Verwendung von Platzhaltern ist möglich.

Sie können auch die **[!UICONTROL Quick configuration]** Option auswählen. Sie müssen nur die URL in das Feld URL eingeben.

### Konfiguration mit Amazon S3 {#S3-configuration-wf}

Mit dem Amazon S3-Protokoll können Sie Beginn beim Herunterladen einer Datei von einer URL oder einem Externe Konto über den Amazon Simple Datenspeicherung Service (S3) ausführen.

1. Wählen Sie ein Amazon S3-Externe Konto aus. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../administration/using/external-accounts.md#amazon-s3-external-account).

2. Wählen Sie aus, ob Sie möchten **[!UICONTROL Define a file path]** oder **[!UICONTROL Use a dynamic file path]**.

3. Geben Sie den Pfad der herunterzuladenden Datei an.

   ![](assets/wkf_file_transfer_08.png)

4. Wenn Sie Ihre Quelldateien nach Abschluss der Übertragung löschen möchten, überprüfen Sie **[!UICONTROL Delete the source files after transfer]**.

### Konfiguration mit der Datenspeicherung von Microsoft Azurblauch {#azure-blob-configuration-wf}

Das Microsoft Azurblase-Protokoll erlaubt Ihnen, auf Blob zugreifen, der auf einem Microsoft Azurblase Datenspeicherung-Konto.

1. Wählen Sie ein **[!UICONTROL Microsoft Azure Blob]** Externe Konto aus. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../administration/using/external-accounts.md#microsoft-azure-external-account).

1. Wählen Sie aus, ob Sie möchten **[!UICONTROL Define a file path]** oder **[!UICONTROL Use a dynamic file path]**.

   ![](assets/wkf_file_transfer_10.png)

1. Geben Sie den Pfad der Datei herunterzuladen, kann es mehrere Blobs. In diesem Fall aktiviert die **[!UICONTROL File transfer]** Aktivität die ausgehende Transition einmal pro gefundenem Block. Sie werden dann in alphabetischer Reihenfolge verarbeitet.

   >[!CAUTION]
   >
   >Platzhalter werden nicht unterstützt, um mehrere Dateinamen zuzuordnen. Stattdessen müssen Sie ein Präfix eingeben. Alle Blob-Namen, die mit diesem Präfix übereinstimmen, sind zulässig.

   Nachfolgend finden Sie eine Liste der Beispiele für Dateipfade:

   * **&quot;Kampagne/&quot;**: findet alle Blobs im Ordner &quot;Kampagne&quot;im Stammordner des Containers.
   * **&quot;Kampagne/Neu-&quot;**: findet alle Blobs mit einem Dateinamen, der mit &quot;new-&quot;beginnt und sich im Ordner &quot;Kampagne&quot;befindet.
   * **&quot;&quot;**: Wenn Sie einen leeren Pfad hinzufügen, können Sie alle im Container verfügbaren Blobs abgleichen.

### Konfiguration mit auf dem Adobe Campaign-Server vorhandenen Dateien {#files-server-configuration-wf}

Das **[!UICONTROL File(s) present on the Adobe Campaign server]** Protokoll entspricht dem Repository, das die wiederherzustellenden Dateien enthält.
Zur Filterung der Dateien ist die Verwendung von Platzhaltern oder Jokern (zum Beispiel * oder ?) möglich.

Wählen Sie, ob Sie **[!UICONTROL Define a file path]** oder **[!UICONTROL Use a dynamic file path]** Die **[!UICONTROL Use a dynamic file path]** Option, können Sie einen Standard-Ausdruck und Ereignis-Variablen verwenden, um den Namen der zu übertragenden Datei zu personalisieren. Weiterführende Informationen dazu finden Sie im Abschnitt [Anpassen von Aktivitäten mit Ereignisvariablen](../../automating/using/calling-a-workflow-with-external-parameters.md#customizing-activities-with-events-variables).

Bitte beachten Sie, dass der Pfad relativ zum Ordner &quot;Datenspeicherung Space&quot;des Adobe Campaign-Servers sein muss. Die Dateien befinden sich im Verzeichnis **sftp&lt;yourinstancename>/**. Darüber hinaus können dem Speicherort übergeordnete Verzeichnisse nicht durchsucht werden. Beispiel:

    >**user&amp;lt;yourinstancename>/my_recipients.csv** ist korrekt.
    >
    >**../hello/my_recipients.csv** ist nicht korrekt.
    >
    >**//myserver/hello/myrecipients.csv** ist nicht korrekt.

## Verlaufsparameter  {#historization-settings}

Every time a **[!UICONTROL Transfer file]** activity is executed, it stores the uploaded or downloaded files in a dedicated folder. One folder is created for each **[!UICONTROL Transfer file]** activity of a workflow. Deshalb ist es wichtig, die Größe dieses Ordners zu begrenzen, um physischen Platz auf dem Server zu sparen.

Dazu können Sie **[!UICONTROL Historization settings]** im **[!UICONTROL Advanced options]** Bereich der **[!UICONTROL Transfer File]** Aktivität definieren.

**[!UICONTROL Historization settings]** können Sie eine maximale Dateianzahl oder Gesamtgröße für den Ordner der Aktivität festlegen. Standardmäßig sind 100 Dateien und 50 MB zugelassen.

Jedes Mal, wenn die Aktivität ausgeführt wird, wird der Ordner folgendermaßen überprüft:

* Nur Dateien, die mehr als 24 Stunden vor der Durchführung der Aktivität erstellt wurden, werden berücksichtigt.
* If the number of files taken into account is greater than the value of the **[!UICONTROL Maximum number of files]** parameter, the oldest files are deleted until the **[!UICONTROL Maximum number of files]** allowed is reached.
* If the total size of files taken into account is greater than the value of the **[!UICONTROL Maximum size (in MB)]** parameter, the oldest files are deleted until the **[!UICONTROL Maximum size (in MB)]** allowed is reached.

>[!NOTE]
>
>Wenn die Aktivität nicht ausgeführt wird, wird der Ordner weder überprüft noch geleert. Seien Sie deshalb achtsam beim Transfer großer Dateien.

## Beispiel  {#example}

Das folgende Beispiel zeigt die Konfiguration einer **Dateiübertragung**-Aktivität, die von einer **Datei laden**-Aktivität und schließlich von einer **Daten-Update**-Aktivität gefolgt wird. Ziel ist die Anreicherung der Adobe-Campaign-Datenbank mit neuen Profilen und gegebenenfalls die Aktualisierung existierender Profile mit den durch den Workflow abgerufenen Daten.

1. Ziehen Sie eine **Dateiübertragung** in den Workflow-Arbeitsbereich.
1. Markieren Sie die Aktivität und öffnen Sie sie mithilfe der im Schnellzugriff angezeigten Schaltfläche ![](assets/edit_darkgrey-24px.png).
1. In the **[!UICONTROL Protocol]** tab, select **SFTP**.
1. Aktivieren Sie die Option **In einem externen Konto definierte Verbindungsparameter verwenden**.
1. Geben Sie den Namen des externen Kontos an.
1. Geben Sie den **Pfad der Dateien auf dem Remote-Server** an.

   ![](assets/wkf_file_transfer_07.png)

1. Validieren Sie die Aktivität und speichern Sie den Workflow.


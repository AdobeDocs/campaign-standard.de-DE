---
title: Verwalten verschlüsselter Daten
description: Erfahren Sie, wie Sie verschlüsselte Daten verwalten.
page-status-flag: never-activated
uuid: d909d26a-cf50-46af-ae09-f0fd7258ca27
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: workflow-general-operation
discoiquuid: 75b83165-dcbd-4bb7-b703-ed769f489b16
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 44d6126023e9411477ccd7ffc07ecde806e7976d
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 80%

---


# Verwalten verschlüsselter Daten {#managing-encrypted-data}

In manchen Fällen müssen die Daten, die Sie auf Campaign-Server importieren möchten, verschlüsselt werden, z. B. wenn sie PII-Daten enthalten.

Um verschlüsselte Dateien importieren oder exportieren zu können, müssen Sie sich zunächst an den Adobe-Kundendienst wenden, damit für Ihre Instanz die erforderlichen Verschlüsselungs-/Entschlüsselungsbefehle bereitgestellt werden.

Senden Sie dazu eine Anfrage mit folgenden Angaben:

* Dem **Titel**, der in der Campaign-Benutzeroberfläche angezeigt wird, zum Verwenden des Befehls. Beispiel: &quot;Datei verschlüsseln&quot;.
* Dem **Befehl** zum Installieren in Ihrer Instanz.
Um eine Datei beispielsweise mit PGP zu entschlüsseln, lautet der Befehl:

   ```
   <path-to_pgp_if-not_global_or_server/>pgp.exe --decrypt --input nl6/var/vp/import/filename.pgp --passphrase "your password" --recipient recipient @email.com --verbose --output nl6/var/vp/import/filename
   ```

Once the request is processed, the encryption / decryption commands will be available in the **[!UICONTROL Pre-processing stage]** field from the **[!UICONTROL Load file]** and **[!UICONTROL Extract file]** activities. Diese können Sie zum Entschlüsseln oder Verschlüsseln der Dateien verwenden, die Sie importieren oder exportieren möchten.

![](assets/preprocessing-encryption.png)

**Verwandte Themen:**

* [Datei laden](../../automating/using/load-file.md)
* [Dateiextraktion](../../automating/using/extract-file.md)

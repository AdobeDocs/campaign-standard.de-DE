---
title: Externe Konten
description: Konfigurieren Sie externe Konten, um Verbindungen mit externen Systemen wie SFTP-Servern herzustellen.
page-status-flag: never-activated
uuid: 5d2e2e3d-5d1f-4466-97e5-842c50390146
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: application-settings
discoiquuid: d5c6a3d4-f767-46c1-a8c0-3b9dc52dcea8
internal: n
snippet: y
context-tags: extAccount,main;extAccount,overview
translation-type: tm+mt
source-git-commit: a73cbdd1af2ce134e10222ab07709639ba419ebe

---


# Externe Konten{#external-accounts}

Externe Konten sind Konfigurationen, die den Zugriff auf Server außerhalb von Adobe Campaign erlauben.

Mit diesen externen Konten ist es möglich, in Campaign-Workflows auf Daten zuzugreifen und diese zu verwalten.

Die folgenden externen Konten können eingerichtet werden:

* SFTP. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](#sftp-external-account).
* Amazon Storage Service (S3). Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](#amazon-s3-external-account).
* Adobe Experience Manager: Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](#adobe-experience-manager-external-account).
* Adobe Analytics. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../integrating/using/configure-campaign-analytics-integration.md).
* Google reCAPTCHA. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](#google-recaptcha-external-account).
* Microsoft Azure Blob Storage. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](#microsoft-azure-external-account).

>[!NOTE]
>
>Adobe verwendet auch andere Typen von externen Konten während des Produktbereitstellungsprozesses. Ab Campaign Standard 17.9 können externe FTP-Konten zwar definiert, aber nicht mehr in neuen Workflow-Aktivitäten verwendet werden. Wenn Sie bereits eine Verbindung eingerichtet hatten, ist sie nach wie vor aktiviert.

Externe Konti können von Administratoren im **[!UICONTROL Administration > Application settings > External accounts]** Menü konfiguriert werden.

## Externes Konto erstellen {#creating-an-external-account}

Adobe Campaign enthält eine Reihe vordefinierter externer Konten. Sie können aber auch Ihre eigenen externen Konten erstellen, um eine Verbindung mit externen Systemen wie FTP-Servern zum Zweck des Dateitransfers herzustellen.

Externe Konten werden von technischen Prozessen, wie technischen Workflows oder Kampagnen-Workflows, verwendet. Bei der Einrichtung eines Dateitransfers in einem Workflow oder bei einem Datenaustausch mit einer anderen Anwendung (Adobe Target, Experience Manager etc.) müssen Sie ein externes Konto auswählen.

1. Click the **[!UICONTROL Create]** button.
1. Geben Sie einen Titel ein. Der Titel und die Kennung werden verwendet, wenn Sie in Workflows externe Konten auswählen möchten.
1. Wählen Sie den Kontotyp aus, den Sie erstellen möchten.
1. Konfigurieren Sie den Zugriff auf das Konto, indem Sie die Zugangsdaten, die Server-Adresse, die Port-Nummer und/oder gegebenenfalls die Schlüssel spezifizieren.

   Die nötigen Informationen werden normalerweise vom Anbieter des Servers bereitgestellt, mit dem Sie eine Verbindung herstellen möchten.

1. Speichern Sie das Konto.

Das externe Konto wurde erstellt und ist nun in der Liste der Konten sichtbar. Es steht jetzt für Ihre Daten-/Dateitransfers oder Routing-Konfigurationen in Workflow-Aktivitäten und Versandeigenschaften bereit.

## Externes SFTP-Konto    {#sftp-external-account}

Unterschiedliche Typen externer Konten erfordern die Angabe unterschiedlicher Informationen.

Geben Sie für ein externes SFTP-Konto die folgenden Details an:

* Serveradresse, z. B. **ftp.domain.com**
* Port-Nummer, z. B. **22**
* SFTP-Server-Zugangsdaten: Kontoname und Passwort, die zur Verbindung mit dem Server verwendet werden

### Empfehlungen für von Adobe gehostete SFTP-Server    {#adobe-hosted-sftp-server-recommendations}

Wenn Dateien und Daten für ETL-Zwecke verwaltet werden, werden diese Dateien auf einem von Adobe bereitgestellten gehosteten SFTP-Server gespeichert. Dieser SFTP-Server ist ein vorübergehender Speicherplatz, auf dem Sie die Aufbewahrung und Löschung von Dateien selbst kontrollieren können.

Wenn der Speicherplatz nicht korrekt verwendet oder gewartet wird, kann der verfügbare physische Platz schnell aufgebraucht sein und ernsthafte Probleme bereiten. Als Folge kann Datenverlust oder die Beschädigung Ihrer Plattform auftreten.

Um solche Probleme zu vermeiden, empfiehlt Adobe, die unten stehenden Best Practice zu befolgen:

* Bewahren Sie nur die Mindestmenge an Daten auf.
* Verwenden Sie eine schlüsselbasierte Authentifizierung, um das Ablaufen von Kennwörtern zu vermeiden. Unterstützt werden nur die Formate **OpenSSH** und **SSH2**. Stellen Sie dem Adobe-Supportteam den öffentlichen Schlüssel bereit, damit er zum Campaign-Server hochgeladen werden kann.
* Bewahren Sie Daten nur so lange wie unbedingt nötig auf. 15 Tage sind das Limit.
* Verwenden Sie Workflows, um Daten ordnungsgemäß zu löschen (verwalten Sie die Beibehaltung von Daten innerhalb der Workflows, die die Daten nutzen).
* Verwenden Sie Batch-Prozesse bei SFTP-Uploads und in Workflows.
* Beseitigen Sie Fehler/Ausnahmen.
* Melden Sie sich gelegentlich beim SFTP-Server direkt an, um dessen Inhalt zu prüfen.
* Beachten Sie bitte, dass die Verwaltung des SFTP-Speichers hauptsächlich Ihre Verantwortung ist.

Beachten Sie außerdem, dass die öffentlichen IPs, mit denen Sie die SFTP-Verbindung aufbauen, in der Campaign-Instanz auf der Whitelist stehen müssen. Wenn Sie IP-Adressen auf eine Whitelist setzen lassen möchten, senden Sie ein [Support-Ticket](https://support.neolane.net) und stellen Sie den öffentlichen Schlüssel zur Authentifizierung bereit.

SFTP-Server können über das Control Panel verwaltet werden. Weitere Informationen finden Sie in der [Control Panel-Dokumentation](https://docs.adobe.com/content/help/de-DE/control-panel/using/sftp-management/about-sftp-management.html).

>[!NOTE]
>
>Das Control Panel ist nur für Admin-Benutzer von Kunden verfügbar, die auf AWS gehostet werden.
Überprüfen Sie [hier](https://docs.adobe.com/content/help/de-DE/control-panel/using/faq.html#ims-org-id), ob Ihre Instanz auf AWS gehostet wird.

## Externes Amazon-S3-Konto {#amazon-s3-external-account}

Das Amazon-S3-Server-Feld sollte folgendermaßen ausgefüllt werden:

```
<S3 bucket name>.s3.amazonaws.com/<s3 object path>
```

Um Ihre Datei im S3-verschlüsselten Modus zu speichern, markieren Sie das **[!UICONTROL Keep files in S3 encrypted]** Kästchen.

![](assets/external_accounts_2.png)

Die nötigen Informationen werden normalerweise vom Anbieter des Servers bereitgestellt, mit dem Sie eine Verbindung herstellen möchten.

Geben Sie die Ihrem Endpunkt **[!UICONTROL AWS Region]** zugeordnete Zeichenfolge an. Die unterstützten Regionen und Signaturversionen finden Sie in der offiziellen [Amazon-Dokumentation zu S3](https://docs.aws.amazon.com/general/latest/gr/rande.html#s3_region).

>[!NOTE]
>
>Your **[!UICONTROL Receiver server]** should be entered without your AWS Region, it will later be automatically added to your URL.

### Empfehlungen für das Amazon-S3-Konto {#amazon-s3-account-recommendations}

Wir empfehlen zum Einrichten des Amazon-S3-Kontos folgende Vorgehensweise:

* Erstellen Sie eine restriktive Bucket-Richtlinie, um den Zugriff auf S3-Buckets zu beschränken. Die Bucket-Richtlinie kann während der Erstellung eines Buckets konfiguriert werden. Weiterführende Informationen finden Sie in der [Amazon-Dokumentation zu S3](https://docs.aws.amazon.com/AmazonS3/latest/dev//example-bucket-policies.html).
* While creating an external account, enable the encryption to store sensitive data in the S3 bucket by checking the **[!UICONTROL Keep files in S3 encrypted]** box.
* Vergeben Sie Bucket-Berechtigungen, um festzulegen, wer auf das Objekt in einem Bucket zugreifen kann. Weiterführende Informationen zu Bucket-Berechtigungen finden Sie in der [Amazon-Dokumentation zu S3](https://docs.aws.amazon.com/AmazonS3/latest/dev//access-control-overview.html).

## Externes Adobe-Experience-Manager-Konto {#adobe-experience-manager-external-account}

Externe Konten vom Typ Adobe Experience Manager werden bei der Integration von Campaign mit Experience Manager verwendet.

Der Vorgang und die Anforderungen für diese Integration sind in [diesem Dokument](../../integrating/using/get-started-campaign-integrations.md) beschrieben.

Zum Einrichten dieses neuen externen Kontos benötigen Sie die folgenden Informationen:

* Server: Geben Sie die URL des Adobe-Experience-Manager-Servers an. z. B. **http://aem.domain.com:4502**.
* Zugangsdaten zum AEM-Konto: Verwenden Sie das Konto, über das auf die Adobe-Experience-Manager-Instanz zugegriffen wird. Es sollte ein Konto sein, das Teil der campaign-remote-Gruppe in Adobe Experience Manager ist.

## Externes Google-reCAPTCHA-Konto    {#google-recaptcha-external-account}

>[!NOTE]
>
>Für die Konfiguration von Google reCAPTCHA ist ein Google-Konto erforderlich.

Mithilfe von Google reCAPTCHA können Sie Ihre Landingpage vor Spam und Missbrauch durch Bots schützen. Dies erfordert nur wenig Einsatz aufseiten Ihrer Kunden, da nur eine Interaktion mit Ihrer Website erforderlich ist. Auf dieser [Seite](https://www.google.com/recaptcha/admin/create) können Sie Ihre Website registrieren. Wählen Sie den Typ &quot;V3 reCAPTCHA&quot;.

Damit Sie Google reCAPTCHA V3 zu Ihrer Landingpage hinzufügen können, müssen Sie sie zunächst in Ihrem externen Konto konfigurieren. Weiterführende Information zum Hinzufügen zu Ihrer Landingpage finden Sie in diesem [Abschnitt](../../channels/using/configuring-landing-page.md#setting-google-recaptcha).

Geben Sie für ein externes Google-reCAPTCHA-V3-Konto die folgenden Details an:

* A **[!UICONTROL Label]** and **[!UICONTROL ID]** of your external account
* **[!UICONTROL Type]**: Google reCAPTCHA
* Ihre **[!UICONTROL Site key]** und **[!UICONTROL Site secret]**
* A **[!UICONTROL Threshold]** between 0 and 1

   The 0.0 **[!UICONTROL Threshold]** value means that it is likely a bot and 1.0 likely a good interaction. Verwenden Sie den Standard-Schwellenwert von 0,5.

![](assets/external_accounts_3.png)

## Externes Microsoft Azure Blob Storage-Konto {#microsoft-azure-external-account}

>[!NOTE]
>
>Information needed to configure your external account in Adobe Campaign Standard can be found in the Azure Portal by selecting **[!UICONTROL Settings]** > **[!UICONTROL Access keys]**.

The Azure Blob storage connector can be used to import or export data to Adobe Campaign using a **[!UICONTROLTransfer file]** workflow activity. Weiterführende Informationen hierzu finden Sie in diesem [Abschnitt](../../automating/using/transfer-file.md#azure-blob-configuration-wf).

Geben Sie für ein externes Microsoft Azure Blob Storage-Konto die folgenden Informationen ein:

* A **[!UICONTROL Label]** and **[!UICONTROL ID]** of your external account
* **[!UICONTROL Type]**: Microsoft Azure Blob Storage
* Ihr **[!UICONTROL Account name]** und **[!UICONTROL Account key]**. Auf dieser [Seite](https://docs.microsoft.com/de-DE/azure/storage/common/storage-account-keys-manage) erfahren Sie, wo Sie Ihren Kontonamen und Kontoschlüssel finden können.
* Ihr **[!UICONTROL Endpoint suffix]**. It can be found within your **[!UICONTROL Connection string]** of the **[!UICONTROL Access keys]** menu in the Azure Portal. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](https://docs.microsoft.com/de-DE/azure/storage/common/storage-account-keys-manage).
* Ihr **[!UICONTROL Container]** Name. Wenn Sie mehr als einen Container verwenden möchten, müssen Sie so viele externe Konten wie Container einrichten.
* The **[!UICONTROL Concurrency]** option lets you fine tune the speed of your file transfers.

![](assets/external_accounts_4.png)

Once configured, click **[!UICONTROL Test connection]** to link Adobe Campaign to Microsoft Azure Blob storage.

### Microsoft Azure Blob Storage – Empfehlungen {#azure-blob-recommendations}

**Verschlüsselung**

Adobe Campaign nutzt eine gesicherte Verbindung (HTTPS), um auf Ihr Microsoft Azure Blob Storage-Konto zuzugreifen.

**Kontoschlüssel**

When configuring your external account, you must use one of the **[!UICONTROL Account key]** available in the Azure Portal. Weitere Informationen zum Auffinden Ihrer Kontoschlüssel erhalten Sie auf dieser [Seite](https://docs.microsoft.com/de-DE/azure/storage/common/storage-account-keys-manage#view-access-keys-and-connection-string).

**Optimieren der Geschwindigkeit bei der Dateiübertragung**

The **[!UICONTROL Concurrency]** option lets you fine tune the speed of your file transfers.
Die Option stellt die Anzahl der Threads dar, die bei der Durchführung der Dateiübertragung verwendet werden. Jeder dieser Threads lädt einen Teil von ca. 1 MB aus dem Blob-Speicher herunter. Diese werden dann in die Warteschlange gestellt, um auf die Festplatte geschrieben zu werden. Beachten Sie, dass bei Erhöhung der Thread-Zahl auch die Auslastung der Ressourcen steigt, die von der Anwendung zur Dateiübertragung genutzt werden.

Nach Abschluss der Dateiübertragung finden Sie Leistungsmetriken in den Workflow-Logs.

**Weitere Zustellversuche**

Standardmäßig werden bei der Dateiübertragung für Azure Blob bis zu vier weitere Zustellversuche durchgeführt.  Wenn der Azure Storage-Dienst einen Fehler-Code wie 503 (Server ist ausgelastet) oder 500 (Zeitüberschreitung bei Vorgang) zurückgibt, kann dies darauf hindeuten, dass Sie die Skalierbarkeit Ihres Speicherkontos bald erreichen oder überschreiten werden. Das kann passieren, wenn ein neues Konto verwendet wird bzw. Tests durchgeführt werden.

If the error persists, you can increase the number of retries by creating an option under the advanced menu **[!UICONTROL Administration]** > **[!UICONTROL Application Settings]** > **[!UICONTROL Options]**.

Im Falle einer Implementierung muss die Option wie folgt eingerichtet werden:

```
ID:        AzureBlob_Max_Retries
Date type: Integer
Default:   <the number of retries needed>
```

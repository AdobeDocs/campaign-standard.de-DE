---
title: Adobe IO für Microsoft Dynamics 365-Integration konfigurieren
description: Erfahren Sie, wie Sie die Adobe IO for Microsoft Dynamics 365-Integration konfigurieren.
page-status-flag: never-activated
uuid: effa1028-66b2-4bef-b5e4-7319dbb23d5d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-analytics
discoiquuid: eb3639f5-7246-46c4-8ddb-da9413b40c32
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4dd1ada05b6681a4e2f7676b177747bdfb0e9bff

---


# Adobe IO für Microsoft Dynamics 365-Integration konfigurieren

Aktivieren Sie Ihre CRM-Daten bei der Kommunikation über Kanal hinweg: lernen Sie die Schritte, die während der Bereitstellung erforderlich sind, um eine neue Integration für Microsoft Dynamics 365 zu erstellen.

## Übersicht

Die Integration von Adobe Campaign Standard - Microsoft Dynamics 365 wird auf [dieser Seite](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)beschrieben.

Bevor Sie die Schritte nach der Bereitstellung in diesem Artikel durchführen, wird davon ausgegangen, dass Sie bereits bereitgestellt wurden und Administratorrechte auf die Instanz im Campaign Standard Ihres Unternehmens haben.  Ist dies nicht der Fall, müssen Sie sich mit dem Adobe-Kundendienst in Verbindung setzen, um die Bereitstellung der Kampagne abzuschließen.

>[!CAUTION]
>
>Die unten beschriebenen Schritte müssen von einem Administrator ausgeführt werden.

## Konfiguration 

Sie müssen den API-Zugriff einrichten und eine neue Integration für Unifi konfigurieren.

Die Konfiguration erfolgt in Adobe IO: Sie müssen eine neue Integration für Unifi erstellen, wie in diesem Video dargestellt:

>[!VIDEO](https://video.tv.adobe.com/v/27308)

### Neue Integration erstellen

Gehen Sie wie folgt vor, um dies zu erreichen:

1. Navigieren Sie zur [Adobe IO-Konsole](https://console.adobe.io/home#) und wählen Sie im Dropdown-Menü oben links Ihre Adobe IMS-Organisations-ID aus (siehe unten).

Klicken Sie dann auf **[!UICONTROL New Integration]** oben rechts.

>[!NOTE]
>
>Ist dies die erste Integration in Ihrem Unternehmen, befindet sich die Schaltfläche für **[!UICONTROL New Integration]** möglicherweise in der Mitte der Seite.

1. Wählen Sie **[!UICONTROL Access an API]** und klicken Sie auf **[!UICONTROL Continue]**.

1. Wählen Sie _Adobe Campaign_ aus dem **[!UICONTROL Experience Cloud]** Abschnitt und klicken Sie auf **[!UICONTROL Continue]**.

1. Generieren Sie ein Zertifikat und einen Schlüssel.

**Für MacOS- und Linux-Plattformen**

Öffnen Sie die Terminalanwendung und führen Sie folgenden Befehl aus:

```
openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout private.key -out certificate_pub.crt
```

**Windows-Plattformen**

* Laden Sie einen openssl-Client herunter, um öffentliche Zertifikate zu generieren (z. B. [OpenSSL-Windows-Client](https://bintray.com/vszakats/generic/download_file?file_path=openssl-1.1.1-win64-mingw.zip))

* Ordner aus der ZIP-Datei extrahieren

* Öffnen Sie die Eingabeaufforderung und führen Sie unterhalb der Befehle aus.

Ersetzen Sie `<containing folder path>` unten durch den Pfad des extrahierten Ordners (z. B. C:\Users\labuser\Downloads\openssl-1.1.1-win64-mingw\openssl-1.1.1-win64-mingw):

```
set OPENSSL_CONF=<containing folder path>/openssl.cnf
 
cd <containing folder path>/
 
openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout private.key -out certificate_pub.crt
```

**Für alle Plattformen**

Befolgen Sie die Anweisungen, um die Zertifikatanforderung abzuschließen:

```
Generating a 2048 bit RSA private key
 
.................+++
 
.......................................+++
 
writing new private key to 'private.key'
 
-----
 
You are about to be asked to enter information that will be incorporated
 
into your certificate request.
 
What you are about to enter is what is called a Distinguished Name or a DN.
 
There are quite a few fields but you can leave some blank
 
For some fields there will be a default value,
 
If you enter '.', the field will be left blank.
 
-----
```

Nach Eingabe der Informationen werden zwei Dateien generiert: **[!UICONTROL certificate_pub.crt]** und **[!UICONTROL private.key]**.

* **[!UICONTROL certificate_pub.crt]** läuft in 365 Tagen ab. Sie können den Ablaufzeitraum ändern, indem Sie den Wert von Tagen im oben stehenden Befehl openssl ändern. Das regelmäßige Drehen von Anmeldedaten ist jedoch eine gute Sicherheitsmaßnahme.

* **[!UICONTROL certificate_pub.crt]** wird im nächsten Bildschirm verwendet, um die Integration in Adobe I/O Console abzuschließen.

>[!NOTE]
>
> **[!UICONTROL private.key]** wird zu einem späteren Zeitpunkt während der Schritte zur Bereitstellung von Unifi verwendet.

1. Gehen Sie zurück zur Adobe I/O Console und geben Sie einen Namen und eine Beschreibung für die Integration ein.

1. Upload **[!UICONTROL certificate_pub.crt]**

1. Wählen Sie das Produkt-Profil aus, das im Titel enthalten ist:

   * Die Organisations-ID Ihrer Instanz in der Kampagne
   * **[!UICONTROL Administrators]**

Beispiel:  Campaign Standard - Ihre Kampagne-Organisations-ID - Administratoren

Klicken Sie auf **[!UICONTROL Create Integration]**.

![](assets/MSdynACSIntegration-4B.png)

### Integrationsdetails einrichten

1. Auswählen **[!UICONTROL Continue to Integration Details]**

Überprüfen Sie die Integrationsdetails.  Sie müssen auf diese zurückverweisen, wenn Sie Unifi-Schritte zur Bereitstellung nach der Bereitstellung durchführen.

![](assets/MSdynACSIntegration-5.png)

1. Klicken Sie auf die **[!UICONTROL Services]** Registerkarte und fügen Sie **[!UICONTROL I/O Events]** und **[!UICONTROL I/O Management API]** Dienste hinzu.  Um den Dienst hinzuzufügen, klicken Sie auf das Optionsfeld und dann **[!UICONTROL Add service]**.  Dies wird für jeden Dienst separat durchgeführt.

Wenn Sie fertig sind, sollten Ihre Dienste oben erscheinen, wie das folgende Bild. Sie müssen den Abschnitt-A-on nicht abschließen und eine JWT und ein Zugriffstoken erstellen.

![](assets/MSdynACSIntegration-6.png)

Die Beitragsbereitstellung in der Kampagne ist jetzt abgeschlossen.  Fahren Sie fort, um die [Schritte zur Bereitstellung für Microsoft Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)abzuschließen.

**Verwandte Themen**

* [Adobe IO - Integration von Dienstkonten](https://www.adobe.io/authentication/auth-methods.html#!AdobeDocs/adobeio-auth/master/AuthenticationOverview/ServiceAccountIntegration.md)
* [Campaign Standard - API-Zugriffseinstellung](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#setting-up-api-access)
* [Campaign Standard - Integration von Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)

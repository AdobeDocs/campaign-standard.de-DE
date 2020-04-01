---
title: Microsoft Dynamics 365 für die Integration von Kampagnen konfigurieren
description: Erfahren Sie, wie Sie Microsoft Dynamics 365 für die Integration von Kampagnen konfigurieren.
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
source-git-commit: a1bc9d23163d12517c4501a572fc92aac6aacbc6

---


# Microsoft Dynamics 365 für die Integration von Kampagnen konfigurieren

Erfahren Sie, wie Sie die Microsoft Dynamics 365-Integration konfigurieren und Ihre CRM-Daten bei der Kommunikation mit Adobe Campaign Standard über Kanal hinweg aktivieren.

## Übersicht

Die Integration von Adobe Campaign Standard - Microsoft Dynamics 365 wird auf [dieser Seite](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)beschrieben.

Drei Systeme, die für diese Integration bereitgestellt werden müssen:

1. Adobe Campaign Standard - [Weitere Informationen](../../integrating/using/configure-adobe-io-for-ms-dynamic.md)
1. Microsoft Dynamics 365 for Sales - siehe Beschreibung
1. Unifi - [Weitere Informationen](../../integrating/using/configure-unifi-for-microsoft-dynamics-365-integration.md)

Nach der Bereitstellung müssen diese Systeme von einem Administrator konfiguriert werden.

In diesem Artikel werden die Schritte auf der Seite Microsoft Dynamics 365 beschrieben, die während der Postbereitstellung erforderlich sind, damit ein Kunde die Integration von Adobe Campaign Standard - Microsoft Dynamics 365 verwenden kann.

## Voraussetzungen

Bevor Sie die Schritte nach der Bereitstellung in diesem Dokument durchführen, wird davon ausgegangen, dass Sie bereits eine Bereitstellung vorgenommen haben und Administratorzugriff auf die Microsoft Dynamics 365-Instanz in Ihrem Unternehmen haben.  Ist dies nicht der Fall, müssen Sie sich mit dem Microsoft-Kundensupport in Verbindung setzen, um die Dynamics 365-Bereitstellung abzuschließen.

## Einrichten der Anwendung und der Berechtigungen

Ein OAuth-Zugriffstoken ermöglicht es Unifi, sich mit Ihrer Microsoft Dynamics 365-Instanz über Web-APIs zu authentifizieren, um Campaign Standard-Experience-Ereignisse an die Zeitschiene der Microsoft Dynamics 365-Schnittstelle zu veröffentlichen.

Die wichtigsten Schritte werden im folgenden Video beschrieben:

** VIDEO**

Gehen Sie wie unten beschrieben vor, um das OAuth-Zugriffstoken zu generieren.

### Neue Anwendung registrieren

1. Melden Sie sich unter Ihrer Administratoranmeldung bei portal.azure.com an.

1. Klicken Sie **[!UICONTROL Azure Active Directory]** im Menü links auf . klicken Sie dann auf **[!UICONTROL App registrations]** das Untermenü, das angezeigt wird.

1. Klicken Sie **[!UICONTROL New registration]** oben auf dem Bildschirm.

![](assets/MSdynACSIntegration-7.png)

Füllen Sie den Registrierungsbildschirm der App aus:

* Name: adobe Kampagne
* Unterstützter Kontotyp: **[!UICONTROL Accounts in this organizational directory only]** (Standardwert)

For more information about creating a new application, refer to [this section](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-register-app).

>[!NOTE]
>
>Azurblauer Anzeige weist Ihrer App eine eindeutige Anwendungs-(Client-)ID zu. Sie benötigen diese ID später bei der Konfiguration von Dynamics 365 sowie bei der Durchführung von Unifi Post Provisioning-Schritten.

### Clientgeheimnis generieren

1. Klicken Sie im Anzeigebereich &quot;App-Übersicht&quot;im Untermenü links auf **[!UICONTROL Certificates and Secrets > New client secret]**

   ![](assets/MSdynACSIntegration-8.png)

1. Geben Sie eine Beschreibung ein, legen Sie die Dauer fest und klicken Sie auf **[!UICONTROL OK]**.

Ihr Client-Geheimnis wird jetzt erstellt.  Bewahren Sie den Wert für den Abschluss der Unifi-Schritte nach der Bereitstellung auf.

>[!CAUTION]
>
>Halten Sie diesen Wert so, wie Sie ihn benötigen, um den Unifi-Schritt nach der Bereitstellung abzuschließen. Es kann nicht danach abgerufen werden.

Weitere Informationen zum Generieren eines Clientgeheimnisses finden Sie in diesem Abschnitt.

### Setup-Berechtigungen

1. Klicken Sie in diesem Bildschirm oder im App-Übersichtsbildschirm auf **[!UICONTROL API permissions]** das Untermenü links.  Nach dem Klicken **[!UICONTROL Add a permission]** müssen Sie **[!UICONTROL Dynamics CRM]** im Menü auswählen.

   ![](assets/MSdynACSIntegration-9.png)

1. Markieren Sie dann das Kästchen und klicken Sie auf **[!UICONTROL user_impersonation]** die **[!UICONTROL Add permissions]** Schaltfläche.

   ![](assets/MSdynACSIntegration-10.png)

Weitere Informationen zum Einrichten von Berechtigungen finden Sie in [diesem Abschnitt](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis#add-permissions-to-access-web-apis).

### App-Benutzer erstellen

Dieser neue Benutzer ist ein generischer Benutzer. Es wird vom Antrag verwendet: Änderungen an Microsoft Dynamics 365 mithilfe der API werden von diesem Benutzer vorgenommen. Gehen Sie wie folgt vor, um sie zu erstellen:

1. Navigieren Sie zu Ihrer Dynamics 365-Instanz und melden Sie sich als Administrator an.

1. Klicken Sie auf das Zahnradsymbol in der oberen rechten Ecke und dann auf **[!UICONTROL Advanced Setting]**s. Klicken Sie im oberen Banner auf das Dropdown-Feld neben **[!UICONTROL Settings]** und klicken Sie auf **[!UICONTROL Security > Users]**.

1. Klicken Sie auf das Dropdown-Menü gehen Sie zu **[!UICONTROL Application Users]**. Klicks **[!UICONTROL New]**.

1. Stellen Sie sicher, dass die Dropdownliste neben dem Benutzersymbol angezeigt wird **[!UICONTROL USER:APPLICATION USER]**.

Füllen Sie den Bildschirm für den neuen Benutzer aus.  Parametervorschläge:

* **[!UICONTROL User Name]** (E-Mail): adobeapi@`<hostname>`, wobei `<hostname>` der Hostname der Dynamics 365-Instanz ist
* **[!UICONTROL Application ID]**: ID der Anwendung, die Sie in der Azurblauen Anzeige registriert haben (erforderlich)
* Sie können leer lassen **[!UICONTROL Application ID URI]** und **[!UICONTROL Azure AD Object ID]**
* **[!UICONTROL Full Name]**: Adobe API
* **[!UICONTROL Email]**: gleich **[!UICONTROL User Name]** (oder falls gewünscht auch die E-Mail des Administrators)

Weitere Informationen zur App-Benutzererstellung finden Sie in [diesem Abschnitt](https://docs.microsoft.com/en-gb/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

1. Klicken Sie auf das Benutzersymbol und laden Sie ein Adobe Campaign-Symbol hoch. Dies ist das Symbol, das in der Timeline-Ansicht angezeigt wird, wenn in Dynamics 365 neue Adobe-Ereignis angezeigt werden.

***getfile***

1. Öffnen Sie die Liste der Benutzerrollen, indem Sie auf **[!UICONTROL MANAGE ROLES]** das obere Band klicken.

1. Blättern Sie nach unten und wählen Sie **[!UICONTROL System administrator]** Zugriff für diesen Benutzer.

1. Klicks **[!UICONTROL OK]**.

### Pächter-ID abrufen

Befolgen Sie die Anweisungen im folgenden Link, um Ihre Mandanten-ID zu finden.  Sie benötigen diese ID während der Bereitstellung in Unifi: [https://docs.microsoft.com/en-us/onedrive/find-your-office-365-tenant-id](https://docs.microsoft.com/en-us/onedrive/find-your-office-365-tenant-id).

## Installieren von Campaign Standard für Microsoft Dynamics 365

Gehen Sie wie folgt vor, um die Dynamics 365-App in die Umgebung Ihres Campaign Standards zu integrieren:

1. Navigieren Sie zum folgenden Link: [https://appsource.microsoft.com/en-us/marketplace/apps](https://appsource.microsoft.com/en-us/marketplace/apps) und suchen Sie in der Suchleiste nach _Adobe Campaign for Dynamics 365_ .
Alternativ können Sie zu diesem [Link](https://appsource.microsoft.com/en-us/product/dynamics-365/adobecampaign.re4snj-a4n7-5t6y-a14br-d5d1b?flightCodes=adobesignhide&tab=Overview)navigieren.
1. Befolgen Sie die Anweisungen zum Installieren der App für Ihre Dynamics 365-Instanz.
1. Nach der Installation navigieren Sie zu Ihrer Dynamics 365-Instanz und melden Sie sich als Administrator an.
1. Klicken Sie auf das Zahnradsymbol in der oberen rechten Ecke und dann auf **[!UICONTROL Advanced Settings]**. Klicken Sie im oberen Banner auf die Dropdown-Liste neben **[!UICONTROL Settings]** und klicken Sie **[!UICONTROL Processes]** unter **[!UICONTROL Process Center]**.
1. Suchen Sie nach **[!UICONTROL Adobe Campaign Email Bounce]** Aufgabe und klicken Sie darauf.
1. Ändern Sie auf der **[!UICONTROL Administration]** Registerkarte den Inhaber in den zuvor erstellten Adobe API-Anwendungsbenutzer, indem Sie auf **[!UICONTROL Actions]** das obere Band klicken, und wählen Sie dann die **[!UICONTROL Assign to another User]** Option aus und wählen Sie aus der Dropdown-Liste **[!UICONTROL Adobe API application user]** , die Sie zuweisen möchten.
1. Reaktivieren Sie den Prozess.
1. Tu das Gleiche für die **[!UICONTROL Adobe Campaign Email Click]** Aufgabe.

>[!NOTE]
>
>Wenn Sie diese Prozesse jederzeit deaktivieren möchten, können Sie dies in diesem **[!UICONTROL Processes]** Bildschirm tun.

Nach Abschluss dieser Konfiguration können Sie die Unifi-Konfiguration einrichten. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md).

**Verwandte Themen**

* [Campaign Standard - Microsoft Dynamics 365-Integration](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)
* [Adobe IO für Microsoft Dynamics 365-Integration konfigurieren](../../integrating/using/configure-adobe-io-for-ms-dynamic.md)
* [Unifi für Kampagne konfigurieren - Microsoft Dynamics 365-Integration](../../integrating/using/configure-unifi-for-microsoft-dynamics-365-integration.md)

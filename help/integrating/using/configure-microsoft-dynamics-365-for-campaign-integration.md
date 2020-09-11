---
title: Microsoft Dynamics 365 für die Integration mit Campaign konfigurieren
description: Erfahren Sie, wie Sie Microsoft Dynamics 365 für die Integration mit Campaign konfigurieren.
page-status-flag: never-activated
uuid: effa1028-66b2-4bef-b5e4-7319dbb23d5d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
discoiquuid: eb3639f5-7246-46c4-8ddb-da9413b40c32
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a7e02fa4fdef05d67118baf0f49fda7886c6768f
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 74%

---


# Microsoft Dynamics 365 für die Integration mit Campaign konfigurieren

Erfahren Sie, wie Sie die Integration mit Microsoft Dynamics 365 konfigurieren und Ihre CRM-Daten für die kanalübergreifende Kommunikation mit Adobe Campaign Standard aktivieren können.

## Übersicht

Die Integration zwischen Adobe Campaign Standard und Microsoft Dynamics 365 wird auf [dieser Seite](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md) beschrieben.

Drei Systeme, die für diese Integration bereitgestellt werden müssen:

1. Adobe Campaign Standard – [mehr dazu](../../integrating/using/configure-adobe-io-for-ms-dynamic.md)
1. Microsoft Dynamics 365 for Sales – siehe Beschreibung unten
1. Integrationstool - Eigentum des Adobe Consulting Teams

Nach der Bereitstellung müssen diese Systeme von einem Administrator konfiguriert werden.

In diesem Artikel werden die Schritte auf der Seite Microsoft Dynamics 365 beschrieben, die während der Einrichtung vor der Integration erforderlich sind, damit ein Kunde die Integration Adobe Campaign Standard - Microsoft Dynamics 365 nutzen kann.

>[!NOTE]
>
>Solange die Benutzeroberfläche für das Selbstbedienungstool noch in diesem Jahr verfügbar ist, wird das Bordteam Sie bei der Konfiguration der Integration unterstützen.

## Voraussetzungen

Bevor Sie die Vorintegration in diesem Dokument durchführen, wird davon ausgegangen, dass Sie bereits eine Version bereitgestellt haben und Administratorrechte auf die Microsoft Dynamics 365-Instanz in Ihrem Unternehmen haben.  Ist dies nicht der Fall, müssen Sie sich mit der Kundenunterstützung von Microsoft in Verbindung setzen, um die Dynamics 365-Bereitstellung abzuschließen.

Wenn Sie die Integration sowohl für die Staging- als auch für die Produktions-Umgebung konfigurieren, müssen Sie die folgenden Schritte für Ihre Staging- und Produktions-Dynamics 365-Instanzen durchführen. Einige unten stehende Anweisungen variieren leicht, je nachdem, ob Sie eine stage- oder production Dynamics 365-Instanz konfigurieren (z. B. für Produktionsinstanzen &quot;prod&quot;wählen `<stage or prod>`)

## Einrichten der Anwendung und der Berechtigungen

Ein OAuth-Zugriffstoken ermöglicht es dem Integrationstool, sich über Web-APIs mit Ihrer Microsoft Dynamics 365-Instanz zu authentifizieren, um Campaign Standard-Experience-Ereignis an die Zeitschiene der Microsoft Dynamics 365-Schnittstelle zu veröffentlichen.

Die wichtigsten Schritte werden im folgenden Video beschrieben:

>[!VIDEO](https://video.tv.adobe.com/v/27637)

Gehen Sie wie unten beschrieben vor, um das OAuth-Zugriffstoken zu generieren.

### Neue Anwendung registrieren

1. Melden Sie sich mit Ihren Administratoranmeldedaten bei portal.azure.com an.

1. Wählen Sie im Menü links **[!UICONTROL Azure Active Directory]** und dann im angezeigten Untermenü **[!UICONTROL App-Registrierungen]** aus.

1. Wählen Sie oben im Bildschirm **[!UICONTROL Neue Registrierung]** aus.

   ![](assets/do-not-localize/MSdynACSIntegration-7.png)

1. Füllen Sie den Registrierungsbildschirm für die App aus:

   * Name: adobe campaign `<stage or prod>`
   * Unterstützter Kontotyp: **[!UICONTROL Nur Konten in diesem Organisationsverzeichnis]** (Standardwert)

Weiterführende Informationen zur Erstellung einer neuen Anwendung finden Sie in [diesem Abschnitt](https://docs.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app).

>[!NOTE]
>
>Azurblauer Anzeige weist Ihrer App eine eindeutige Applikations-ID zu. Sie benötigen diese ID später bei der Konfiguration von Dynamics 365 sowie bei der Einrichtung des Integrationstools vor der Integration.

### Client-Geheimnis generieren

1. Wählen Sie im Bildschirm mit der App-Übersicht im Untermenü auf der linken Seite **[!UICONTROL Zertifikate und Geheimnisse > Neues Client-Geheimnis]** aus.

   ![](assets/do-not-localize/MSdynACSIntegration-8.png)

1. Geben Sie eine Beschreibung ein, legen Sie eine Laufzeit fest und wählen Sie **[!UICONTROL OK]** aus.

Ihr Client-Geheimnis wird jetzt erstellt. Bewahren Sie den Wert vorübergehend für den Abschluss der Einrichtung des Integrationstools vor der Integration auf.

>[!CAUTION]
>
>Halten Sie diesen Wert so, wie Sie ihn benötigen, um die Einrichtung des Integrationstools vor der Integration abzuschließen. Er kann danach nicht mehr abgerufen werden.


### Berechtigungen einrichten

1. Wählen Sie in diesem Bildschirm oder im Bildschirm mit der App-Übersicht im Untermenü links **[!UICONTROL API-Berechtigungen]** aus.  Nachdem Sie **[!UICONTROL Berechtigung hinzufügen]** ausgewählt haben, wählen Sie **[!UICONTROL Dynamics CRM]** im Menü aus.

   ![](assets/do-not-localize/MSdynACSIntegration-9.png)

1. Markieren Sie anschließend die Checkbox für **[!UICONTROL user_impersonation]** und wählen Sie die Schaltfläche **[!UICONTROL Berechtigungen hinzufügen]** aus.

   ![](assets/do-not-localize/MSdynACSIntegration-10.png)

Weiterführende Informationen zum Einrichten von Berechtigungen finden Sie in [diesem Abschnitt](https://docs.microsoft.com/de-de/azure/active-directory/develop/quickstart-configure-app-access-web-apis#add-permissions-to-access-web-apis).

### App-Anwender erstellen

Dieser neue Anwender ist ein generischer Anwender. Er wird von der Anwendung genutzt: Alle Änderungen an Microsoft Dynamics 365 mithilfe der API werden von diesem Anwender vorgenommen. Gehen Sie dazu wie folgt vor:

1. Navigieren Sie zu Ihrer Dynamics 365-Instanz und melden Sie sich als Administrator an.

1. Wählen Sie das Zahnradsymbol oben rechts und dann **[!UICONTROL Erweiterte Einstellungen]** aus. Wählen Sie im oberen Banner neben **[!UICONTROL Einstellungen]** die Optionen **[!UICONTROL Sicherheit > Anwender]** aus.

1. Wählen Sie das Dropdown-Menü aus, um **[!UICONTROL Anwender]** aufzurufen. Wählen Sie **[!UICONTROL Neu]** aus.

1. Stellen Sie sicher, dass im Dropdown-Menü neben dem Anwendersymbol steht: **[!UICONTROL USER:APPLICATION USER]**.

   Füllen Sie den Bildschirm für den neuen Anwender aus.  Empfohlene Parameter:

   * **[!UICONTROL Benutzername]** (E-Mail): adobe_api_`<stage-or-prod>`@`<your-d365-hostname>`&quot;(z. B. adobe_api_stage@some-company.crm.dynamics.com)
   * **[!UICONTROL Anwendungs-ID]**: Kennung der Anwendung, die Sie in Azure AD registriert haben (das ist obligatorisch).
   * Sie können **[!UICONTROL URl der Anwendungs-ID]** und **[!UICONTROL Azure AD-Objektkennung]** leer lassen.
   * **[!UICONTROL Vollständiger Name]**: Adobe-API. `<stage or prod>`
   * **[!UICONTROL E-Mail]**: identisch mit **[!UICONTROL Benutzername]** (oder der E-Mail-Adresse des Administrators, falls gewünscht).

   Weiterführende Informationen zur Erstellung von Anwendern finden Sie in [diesem Abschnitt](https://docs.microsoft.com/de-de/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

1. Wählen Sie das Anwendersymbol aus und laden Sie ein Adobe Campaign-Symbol hoch. Dies ist das Symbol, das in der Timeline-Ansicht angezeigt wird, wenn in Dynamics 365 neue Adobe-Ereignisse erscheinen.

<!-- ***getfile*** adobe campaign logo-->

1. Öffnen Sie die Liste der Anwenderrollen, indem Sie im oberen Band **[!UICONTROL ROLLEN VERWALTEN]** auswählen.

1. Blättern Sie nach unten und wählen Sie **[!UICONTROL Systemadministrator]**-Zugriff für diesen Anwender.

1. Wählen Sie **[!UICONTROL OK]** aus.

### Mandantenkennung abrufen

Befolgen Sie die Anweisungen [auf dieser Seite](https://docs.microsoft.com/de-de/onedrive/find-your-office-365-tenant-id) , um Ihre Mandanten-ID zu finden.  Sie benötigen diese ID während der Einrichtung vor der Integration im Integrationstool.

## Campaign Standard für Microsoft Dynamics 365 installieren

Gehen Sie wie folgt vor, um die Dynamics 365-App in die Campaign Standard-Umgebung zu integrieren:

1. Navigieren Sie zum folgenden Link: [https://appsource.microsoft.com/de-de/marketplace/apps](https://appsource.microsoft.com/de-de/marketplace/apps) und suchen Sie in der Suchleiste nach _Adobe Campaign for Dynamics 365_.
Alternativ können Sie zu diesem [Link](https://appsource.microsoft.com/en-us/product/dynamics-365/adobecampaign.re4snj-a4n7-5t6y-a14br-d5d1b?flightCodes=adobesignhide&amp;tab=Overview) navigieren.
1. Befolgen Sie die Anweisungen zum Installieren der App für Ihre Dynamics 365-Instanz.
1. Nach der Installation navigieren Sie zu Ihrer Dynamics 365-Instanz und melden Sie sich als Administrator an.
1. Wählen Sie das Zahnradsymbol oben rechts und dann **[!UICONTROL Erweiterte Einstellungen]** aus. Wählen Sie im oberen Banner das Dropdown-Menü neben **[!UICONTROL Einstellungen]** und dann **[!UICONTROL Prozesse]** unter **[!UICONTROL Process Center]** aus.
1. Suchen Sie nach der Aufgabe **[!UICONTROL Adobe Campaign – E-Mail-Bounce]** und wählen Sie sie aus.
1. Ändern Sie auf dem Tab **[!UICONTROL Administration]** den Besitzer in den zuvor erstellten Adobe API-Anwender, indem Sie im oberen Band **[!UICONTROL Aktionen]** auswählen und dann die Option **[!UICONTROL Einem anderen Anwender zuweisen]** wählen. Wählen Sie dann aus der Dropdown-Liste die Option **[!UICONTROL Adobe API-Anwender]** für die Zuweisung aus.
1. Reaktivieren Sie den Prozess.
1. Tun Sie dasselbe für die Aufgabe **[!UICONTROL Adobe Campaign – E-Mail-Klick]**.

>[!NOTE]
>
>Sie können diese Prozesse zu einem beliebigen späteren Zeitpunkt im Bildschirm **[!UICONTROL Prozesse]** deaktivieren.

**Verwandte Themen**

* [Integration zwischen Campaign Standard und Microsoft Dynamics 365](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)
* [Adobe IO für die Integration mit Microsoft Dynamics 365 konfigurieren](../../integrating/using/configure-adobe-io-for-ms-dynamic.md)

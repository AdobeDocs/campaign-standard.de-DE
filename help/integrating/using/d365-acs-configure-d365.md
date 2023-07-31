---
title: Microsoft Dynamics 365 für die Integration mit Campaign konfigurieren
description: Erfahren Sie, wie Sie Microsoft Dynamics 365 für die Integration mit Campaign konfigurieren.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
feature: Microsoft CRM Integration
role: Data Architect
level: Experienced
exl-id: 57e85f8e-65b4-44ea-98e6-0c555acf6dee
source-git-commit: 6947d163119dd6fc5966fdc723530b02bdd4a469
workflow-type: ht
source-wordcount: '988'
ht-degree: 100%

---

# Microsoft Dynamics 365 für die Integration mit Adobe Campaign Standard konfigurieren

Erfahren Sie, wie Sie die Integration mit Microsoft Dynamics 365 konfigurieren und Ihre CRM-Daten für die kanalübergreifende Kommunikation mit Adobe Campaign Standard aktivieren können.

## Übersicht

Die allgemeine Beschreibung der Integration von Adobe Campaign Standard mit Microsoft Dynamics 365 finden Sie auf [dieser Seite](../../integrating/using/d365-acs-get-started.md).

Für die Integration müssen mehrere Anwendungen konfiguriert werden. Dieser Artikel konzentriert sich jedoch auf die in Dynamics 365 erforderlichen Schritte.

## Voraussetzungen

Bevor Sie die in diesem Dokument beschriebenen Einrichtungsschritte vor der Integration durchführen, wird davon ausgegangen, dass Sie bereits eine Bereitstellung vorgenommen haben und Administratorzugriff auf die Microsoft Dynamics 365-Instanz Ihres Unternehmens haben.  Ist dies nicht der Fall, müssen Sie sich mit der Kundenunterstützung von Microsoft in Verbindung setzen, um die Dynamics 365-Bereitstellung abzuschließen.

Wenn Sie die Integration sowohl für die Staging- als auch für die Produktionsumgebung konfigurieren, müssen Sie die folgenden Schritte für Ihre Staging- und Produktions-Dynamics 365-Instanzen durchführen. Die folgenden Anweisungen variieren geringfügig, je nachdem, ob Sie eine Staging- oder Produktions-Dynamics 365-Instanz konfigurieren (z. B. wählen Sie für die Produktionsinstanz &quot;prod&quot; für `<stage or prod>` aus).

## Einrichten der Anwendung und der Berechtigungen

Ein OAuth-Zugriffstoken ermöglicht es dem Integrations-Tool, sich über Web-APIs bei Ihrer Microsoft Dynamics 365-Instanz zu authentifizieren, um Campaign Standard-Erlebnisereignisse in der Timeline-Ansicht der Microsoft Dynamics 365-Oberfläche zu veröffentlichen.

Die wichtigsten Schritte werden im folgenden Video beschrieben:

>[!VIDEO](https://video.tv.adobe.com/v/27637)

Gehen Sie wie unten beschrieben vor, um das OAuth-Zugriffstoken zu generieren.

### Neue Anwendung registrieren   {#register-a-new-app}

1. Melden Sie sich unter Ihrem Administrator-Login bei [portal.azure.com](https://portal.azure.com){target="_blank"} an.

1. Wählen Sie im Menü links **[!UICONTROL Azure Active Directory]** und dann im angezeigten Untermenü **[!UICONTROL App-Registrierungen]** aus.

1. Wählen Sie oben im Bildschirm **[!UICONTROL Neue Registrierung]** aus.

1. Füllen Sie den Registrierungsbildschirm für die App aus:

   * Name: adobe campaign       `<stage or prod>`
   * Unterstützter Kontotyp: **[!UICONTROL Nur Konten in diesem Organisationsverzeichnis]** (Standardwert)

Weiterführende Informationen zur Erstellung einer neuen Anwendung finden Sie in [diesem Abschnitt](https://docs.microsoft.com/de-de/azure/active-directory/develop/quickstart-register-app){target="_blank"}.

>[!NOTE]
>
>Microsoft Azure Directory weist Ihrer App eine eindeutige Anwendungs-(Client-)Kennung zu. Sie benötigen diese Kennung später bei der Konfiguration von Dynamics 365 sowie bei der Einrichtung des Integrations-Tools.

### Client-Geheimnis generieren {#generate-a-client-secret}

1. Wählen Sie im Bildschirm mit der App-Übersicht im Untermenü auf der linken Seite **[!UICONTROL Zertifikate und Geheimnisse > Neues Client-Geheimnis]** aus.

1. Geben Sie eine Beschreibung ein, legen Sie eine Laufzeit fest und wählen Sie **[!UICONTROL OK]** aus.

Ihr Client-Geheimnis wird jetzt erstellt. Bewahren Sie den Wert vorübergehend für den Abschluss der Einrichtung des Integrationstools vor der Integration auf.

>[!CAUTION]
>
>Bewahren Sie diesen Wert auf, da Sie ihn benötigen, um die Einrichtung des Integrationstools vor der Integration abzuschließen. Er kann danach nicht mehr abgerufen werden.


### Berechtigungen einrichten

1. Wählen Sie in diesem Bildschirm oder im Bildschirm mit der App-Übersicht im Untermenü links **[!UICONTROL API-Berechtigungen]** aus.  Nachdem Sie **[!UICONTROL Berechtigung hinzufügen]** ausgewählt haben, wählen Sie **[!UICONTROL Dynamics CRM]** im Menü aus.

1. Markieren Sie anschließend die Checkbox für **[!UICONTROL user_impersonation]** und wählen Sie die Schaltfläche **[!UICONTROL Berechtigungen hinzufügen]** aus.

Weiterführende Informationen zum Einrichten von Berechtigungen finden Sie in [diesem Abschnitt](https://docs.microsoft.com/de-de/azure/active-directory/develop/quickstart-configure-app-access-web-apis#add-permissions-to-access-web-apis){target="_blank"}.

### App-Anwender erstellen

Dieser neue Anwender ist ein generischer Anwender. Er wird von der Anwendung genutzt: Alle Änderungen an Microsoft Dynamics 365 mithilfe der API werden von diesem Anwender vorgenommen. Gehen Sie dazu wie folgt vor:

1. Navigieren Sie zu Ihrer Dynamics 365-Instanz und melden Sie sich als Administrator an.

1. Wählen Sie das Zahnradsymbol oben rechts und dann **[!UICONTROL Erweiterte Einstellungen]** aus. Wählen Sie im oberen Banner neben **[!UICONTROL Einstellungen]** die Optionen **[!UICONTROL Sicherheit > Anwender]** aus.

1. Wählen Sie das Dropdown-Menü aus, um **[!UICONTROL Anwender]** aufzurufen. Wählen Sie **[!UICONTROL Neu]** aus.

1. Stellen Sie sicher, dass im Dropdown-Menü neben dem Anwendersymbol steht: **[!UICONTROL USER:APPLICATION USER]**.

   Füllen Sie den Bildschirm für den neuen Anwender aus.  Empfohlene Parameter:

   * **[!UICONTROL Benutzername]** (E-Mail): adobe_api_`<stage-or-prod>`@`<your-d365-hostname>`&quot; (z. B. adobe_api_stage@some-company.crm.dynamics.com)
   * **[!UICONTROL Anwendungs-ID]**: Kennung der Anwendung, die Sie in Azure AD registriert haben (das ist obligatorisch).
   * Sie können **[!UICONTROL URl der Anwendungs-ID]** und **[!UICONTROL Azure AD-Objektkennung]** leer lassen.
   * **[!UICONTROL Vollständiger Name]**: Adobe-API.       `<stage or prod>`
   * **[!UICONTROL E-Mail]**: identisch mit **[!UICONTROL Benutzername]** (oder der E-Mail-Adresse der Administratorin oder des Administrators, falls gewünscht).

   Weiterführende Informationen zur Erstellung von Anwendern finden Sie in [diesem Abschnitt](https://docs.microsoft.com/de-de/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user){target="_blank"}.

1. Wählen Sie das Anwendersymbol aus und laden Sie ein Adobe Campaign-Symbol hoch. Dies ist das Symbol, das in der Timeline-Ansicht angezeigt wird, wenn in Dynamics 365 neue Adobe-Ereignisse erscheinen.

1. Öffnen Sie die Liste der Anwenderrollen, indem Sie im oberen Band **[!UICONTROL ROLLEN VERWALTEN]** auswählen.

1. Blättern Sie nach unten und wählen Sie **[!UICONTROL Systemadministrator]**-Zugriff für diesen Anwender.

1. Wählen Sie **[!UICONTROL OK]** aus.

### Mandantenkennung abrufen   {#get-the-tenant-id}

Befolgen Sie die Anweisungen [auf dieser Seite](https://docs.microsoft.com/de-de/onedrive/find-your-office-365-tenant-id), um Ihre Mandanten-ID zu finden.  Sie benötigen diese ID während der Einrichtung vor der Integration im Integrations-Tool.

## Campaign Standard für Microsoft Dynamics 365 installieren {#install-appsource-app}

Gehen Sie wie folgt vor, um die Dynamics 365-App in die Campaign Standard-Umgebung zu integrieren:

1. Navigieren Sie zu [Microsoft Business Apps](https://appsource.microsoft.com/de-de/marketplace/apps) und suchen Sie in der Suchleiste nach _Adobe Campaign Standard_ .
Alternativ können Sie zu diesem [Link](https://appsource.microsoft.com/de/product/dynamics-365/adobe.adobe_campaign_d365?tab=Overview) gehen.{target="_blank"}
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

* [Konfigurieren von Adobe Developer für die Microsoft Dynamics 365-Integration](../../integrating/using/d365-acs-configure-adobe-io.md) ist der nächste Schritt beim Einrichten der Integration.
* [Erste Schritte mit der Selfservice-Integrationsanwendung](../../integrating/using/d365-acs-self-service-app-quick-start-guide.md) enthält eine vollständige Anleitung zur Durchführung der Integration.

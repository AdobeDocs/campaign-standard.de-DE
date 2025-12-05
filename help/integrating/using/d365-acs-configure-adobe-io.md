---
title: Konfigurieren von Adobe Developer für die Integration mit Microsoft Dynamics 365
description: Erfahren Sie, wie Sie Adobe Developer für die Integration mit Microsoft Dynamics 365 konfigurieren
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-ms-dynamics
feature: Microsoft CRM Integration
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: ab21b694-d05c-4ba4-b828-936803651b82
source-git-commit: b3f3309a252971dc527d44913b7918abeea704d9
workflow-type: ht
source-wordcount: '602'
ht-degree: 100%

---

# Adobe Campaign Standard- und Adobe Developer-Konfiguration für die Integration mit Microsoft Dynamics 365

In diesem Artikel wird erläutert, wie Adobe Campaign Standard und Adobe I/O konfiguriert werden müssen, damit die Integrationsanwendung auf die Daten zugreifen kann.

## Adobe Campaign Standard konfigurieren {#campaign-standard}

### Profilerweiterungen

Bitte aktivieren Sie in Adobe Campaign Standard Profilerweiterungen.   Dies ist erforderlich, damit benutzerdefinierte Felder in der Profilressource von Microsoft Dynamics 365 synchronisiert werden können.   Die Aktivierungsschritte sind:

1. Gehen Sie zu &quot;Einstellungen&quot; > &quot;Administration&quot; > &quot;Entwicklung&quot; > &quot;Veröffentlichung&quot;.
1. Klicken Sie auf &quot;Publikation vorbereiten&quot;, um eine Veröffentlichung vorzubereiten.
1. Nachdem die Vorbereitung abgeschlossen ist, aktivieren Sie &quot;Die Profiles &amp; Services Ext API erstellen&quot; und klicken Sie auf &quot;Veröffentlichen&quot;.

## Adobe I/O konfigurieren {#adobe-io}

Mit Adobe I/O können Sie den API-Zugriff auf Adobe Campaign Standard sowie auf andere Adobe-Produkte aktivieren.   In diesem Artikel wird detailliert beschrieben, wie Sie Adobe I/O konfigurieren, um der Integration von Adobe Campaign Standard mit Microsoft Dynamics 365 Zugriff zum Synchronisieren der Daten zu gewähren.

### Übersicht

Bevor Sie die Einrichtungsschritte vor der Integration in diesem Artikel durchführen, wird davon ausgegangen, dass Sie bereits Administratorrechte für die Campaign Standard-Instanz Ihres Unternehmens erhalten haben.  Ist dies nicht der Fall, setzen Sie sich mit der Adobe-Kundenunterstützung in Verbindung, um die Bereitstellung von Campaign abzuschließen.

>[!CAUTION]
>
>Die unten beschriebenen Schritte müssen von einem Administrator ausgeführt werden.

### Konfiguration 

Sie müssen ein neues Adobe Developer-Projekt erstellen und es für die Integration konfigurieren.

#### Neues Projekt erstellen

Gehen Sie dazu wie folgt vor:

1. Gehen Sie zur [Adobe Developer Console](https://console.adobe.io/home#) und wählen Sie Ihre Adobe Organisations-ID aus dem Dropdown-Menü oben rechts aus.

1. Klicken Sie anschließend unter **[!UICONTROL Schnellstart]** auf **[!UICONTROL Neues Projekt erstellen]**.

   ![](assets/adobeIO1.png)

1. Klicken Sie unter **[!UICONTROL Erste Schritte mit Ihrem neuen Projekt]** auf **[!UICONTROL API hinzufügen]**.

   ![](assets/adobeIO2.png)

1. Wählen Sie Adobe Campaign aus und klicken Sie auf **[!UICONTROL Weiter]**.

   ![](assets/adobeIO3.png)

1. Auf dem nächsten Bildschirm haben Sie die Möglichkeit, den Authentifizierungstyp auszuwählen. Sie können entweder „OAuth-Server-zu-Server“ oder „Service-Konto (JWT)“ auswählen. Beachten Sie, dass die Anmeldedaten für Service-Konten (JWT) für neue Projekte nicht mehr empfohlen werden, sondern stattdessen die neueren OAuth-Server-zu-Server-Anmeldedaten verwendet werden sollten. Die Anweisungen in diesem Handbuch gelten nur für die Authentifizierung mit OAuth-Server-zu-Server.

   ![](assets/adobeIO4.png)

1. Auf dem nächsten Bildschirm wählen Sie Produktprofile aus, die diesem Projekt zugeordnet werden sollen. Wählen Sie das Produktprofil aus, das im Titel enthalten ist: Die Mandantenkennung Ihrer Campaign-Instanz – [!UICONTROL Administratoren]

   Beispiel: Campaign Standard – Ihre Campaign-Mandantenkennung – Administratoren

1. Klicken Sie auf **[!UICONTROL Konfigurierte API speichern]**.

   ![](assets/adobeIO5.png)

1. Auf dem nächsten Bildschirm sehen Sie die Details Ihres neuen Adobe Developer-Projekts. Klicken Sie oben links im Bildschirm auf **[!UICONTROL Zum Projekt hinzufügen]** und wählen Sie in der Dropdown-Liste die Option **API** aus.

   ![](assets/adobeIO6.png)

1. Wählen Sie im nächsten Bildschirm die I/O Events-API aus und klicken Sie dann auf **[!UICONTROL Weiter]**.

1. Klicken Sie im nächsten Bildschirm auf **[!UICONTROL Save the configured API]**.  Sie kehren zum Bildschirm mit den Projektdetails zurück.

1. Klicken Sie nun oben links im Bildschirm auf **[!UICONTROL Zum Projekt hinzufügen]** und wählen Sie wie zuvor in der Dropdown-Liste die Option **API** aus.

1. Wählen Sie im nächsten Bildschirm die I/O Management-API aus und klicken Sie auf **[!UICONTROL Weiter]**.

1. Klicken Sie im nächsten Bildschirm auf **[!UICONTROL Save the configured API]**.

Die Einrichtung vor der Integration in Campaign ist jetzt abgeschlossen.

**Verwandte Themen**

* [Konfigurieren von Adobe Developer für die Microsoft Dynamics 365-Integration](../../integrating/using/d365-acs-configure-adobe-io.md) ist der nächste Schritt beim Einrichten der Integration
* Die [Übersicht über die Selfservice-Integrationsanwendung](../../integrating/using/d365-acs-self-service-app-quick-start-guide.md) enthält eine vollständige Anleitung zur Durchführung der Integration.
* [Adobe Developer – Integration von Service-Konten](https://developer.adobe.com/developer-console/docs/guides/#!AdobeDocs/adobeio-auth/master/AuthenticationOverview/ServiceAccountIntegration.md)
* [Campaign Standard – Einrichtung von API-Zugriff](../../api/using/setting-up-api-access.md)
* [Campaign Standard – Integration mit Dynamics 365](../../integrating/using/d365-acs-configure-d365.md)
* [Migrieren von Anmeldedaten von JWT zu OAuth-Server-zu-Server](../../integrating/using/d365-acs-self-service-app-migrate-credentials.md) enthält die Schritte zum Migrieren von Anmeldedaten von JWT zu OAuth-Server-zu-Server.

---
title: Unifi für Microsoft Dynamics 365-Integration konfigurieren
description: Erfahren Sie, wie Sie die Unifi for Microsoft Dynamics 365-Integration konfigurieren
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
source-git-commit: 37e86c6143c52841e69d610fa9db35dff70a3587

---



# Unifi für Microsoft Dynamics 365-Integration konfigurieren

Konfigurieren Sie Unifi, um die Microsoft Dynamics 365 - Adobe Campaign-Integration einzurichten und zu aktivieren.

## Voraussetzungen

Bevor Sie die Schritte nach der Bereitstellung in diesem Artikel durchführen, wird davon ausgegangen, dass Sie die [Schritte nach der Bereitstellung für Kampagne](../../integrating/using/configure-adobe-io-for-ms-dynamic.md) und [für Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)bereits erfolgreich abgeschlossen haben.  Ist dies nicht der Fall, müssen Sie diese Schritte ausführen, um den Campaign Standard und Dynamics 365 nach der Bereitstellung abzuschließen.

Es wird auch davon ausgegangen, dass Sie Unifi kontaktiert haben, ein Unifi-Konto für Sie erstellt haben und sich erfolgreich anmelden konnten.  Ist dies nicht der Fall, führen Sie die in [diesem Artikel](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)beschriebenen Schritte aus.

>[!CAUTION]
>
>Es wird dringend empfohlen, bei der Konfiguration von Unifi mit Unifi und/oder Adobe-Beratung zu arbeiten (wenden Sie sich an Ihren Adobe CSM).

## Kampagne-Integration konfigurieren

Klicken Sie bei der ersten Verbindung auf **[!UICONTROL Adobe Campaign Standard]** , um Ihre Anmeldedaten für die Kampagne einzugeben.

Die meisten dieser Anmeldeinformationen stammen aus der Integration, die Sie während der [Campaign Standard-Konfigurationsschritte](../../integrating/using/configure-adobe-io-for-ms-dynamic.md)in der Adobe I/O-Konsole erstellt haben.

>[!NOTE]
>
>Um die Sicherheit und den Datenschutz zu gewährleisten, werden vertrauliche Felder mit den Anmeldeinformationen beim erneuten Besuch dieser Konfigurationsbildschirme leer angezeigt.

1. Geben Sie für die Adobe-Authentifizierungs-URL `https://ims-na1.adobelogin.com/ims/exchange/jwt`

1. Geben Sie Ihre **[!UICONTROL Adobe IO Organization ID]** und Ihre ein **[!UICONTROL Adobe IO Integration ID]**.

Um Ihre Adobe IO-Organisations- und Integrations-IDs abzurufen, navigieren Sie zum Bildschirm &quot;Integration der Adobe-E/A-Konsole über&quot;und beachten Sie die Web-URL.

Es sollte ungefähr so aussehen: `https://console.adobe.io/integrations/<Org ID>/<Int ID>/overview`, wobei Org-ID und Int-ID Zahlen sind.

1. Geben Sie Ihre **[!UICONTROL Tenant ID]**

Gehen Sie wie folgt vor, um Ihre Mandant-ID abzurufen:

1. Navigieren Sie zur [Adobe Admin Console](https://adminconsole.adobe.com/) und wählen Sie Ihr IMS-Org aus dem oberen rechten Dropdownmenü.
1. Wählen Sie Ihr Adobe Campaign Standard-Produkt und dann Ihre Campaign Standard-Instanz aus (wenn Sie mehr als eine haben).  Dadurch wird eine Liste von Produkt-Profilen entstehen.

   Die Produktbeschreibungen werden in der Regel in einem der folgenden Profil angezeigt, wobei die `<tenantID>` Mandant-ID der Instanz angegeben wird.

`Campaign Standard – https://<tenantID> - <ROLE>`

`Campaign Standard – <tenantID> - <ROLE>`

>[!NOTE]
>
>Sollten Sie Probleme bei der Identifizierung Ihrer Mandanten-ID haben, wenden Sie sich bitte an Sie > Technischer Kontakt von Adobe oder den Adobe-Kundendienst.
>
>Partner-Sandbox-Instanzenmieter-IDs folgen in der Regel dem Muster `https://<tenantId>`, wo `tenantId` es `tbd.campaign-sandbox.adobe.com`ist.

1. Geben Sie Ihre **[!UICONTROL Campaign Instance ID]** ein.

Gehen Sie wie folgt vor, um Ihre Instanz-ID abzurufen:

    1. Geben Sie &quot;https://&lt;acs-instance-url>/r/test&quot;in einen Webbrowser ein und ersetzen Sie &quot;&lt;acs-instance-url>&quot;durch die URL Ihrer Campaign Standard-Instanz.
    1. Die Antwort enthält &quot;instance=&quot;gefolgt von der Instanz-ID.

1. Wählen Sie den Bereich Ihrer Kampagne aus.

1. Sie können **[!UICONTROL Base Directory]** leer lassen.

1. Select the **[!UICONTROL Allow as Output Destination]** option.

Nachdem die Parameter festgelegt wurden, klicken Sie auf **[!UICONTROL CONNECT]** und überprüfen Sie, ob die Verbindung erfolgreich ist.

Ist dies nicht der Fall, klicken Sie auf **[!UICONTROL CLOSE]** und prüfen Sie die Parameter.

>[!NOTE]
>
>Wenn Sie diesen Schritt nicht ausführen können, wenden Sie sich an den [Unifi-Kundendienst](mailto:support@unifisoftware.atlassian.net).

## Dynamics 365-Integration konfigurieren

Klicken Sie auf Microsoft Dynamics CRM, um Dynamics 365-Anmeldeinformationen zu konfigurieren. Die meisten dieser Anmeldeinformationen stammen aus der Integration, die Sie in Microsoft Dynamics 365 während der Konfigurationsschritte von Microsoft Dynamics 365 erstellt haben.

>[!NOTE]
>
>Um die Sicherheit und den Datenschutz zu gewährleisten, werden vertrauliche Felder mit den Anmeldeinformationen beim erneuten Besuch dieser Konfigurationsbildschirme leer angezeigt.

1. Geben Sie **[!UICONTROL URL]** beispielsweise die URL Ihrer Dynamics 365-Instanz ein und achten Sie darauf, &quot;.api&quot;vor &quot;.crm&quot;einzufügen (z. B. `https://mydynamicsinstance.api.crm.dynamics.com`)

1. Sie **[!UICONTROL clientid]** verwenden beispielsweise die Anwendungs-ID, die beim Erstellen der App-Registrierung als [Konfiguration von Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)generiert wurde.

1. Sie verwenden **[!UICONTROL clientsecret]** beispielsweise das Clientgeheimnis, das generiert wurde, wenn Sie der App-Registrierung als [Konfiguration von Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)ein Clientgeheimnis hinzugefügt haben.

1. Fügen Sie **[!UICONTROL callbackurl]** zum Beispiel `http://localhost:33333`hinzu.

1. Lassen Sie **[!UICONTROL refresh token]** beispielsweise leer.

1. Verwenden Sie für die **[!UICONTROLMandanten-ID]** die Mieter-ID, die Sie von portal.azure.com erhalten haben, als [Konfiguration von Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

1. Markieren Sie abschließend das Kästchen **[!UICONTROL Allow as Output Destination]**.

Nachdem die Parameter eingegeben wurden, klicken Sie auf **[!UICONTROL CONNECT]** und überprüfen Sie, ob die Verbindung erfolgreich ist.

Ist dies nicht der Fall, klicken Sie auf **[!UICONTROL CLOSE]** und prüfen Sie die Parameter.

>[!NOTE]
>
>Wenn Sie diesen Schritt nicht ausführen können, wenden Sie sich an den [Unifi-Kundendienst](mailto:support@unifisoftware.atlassian.net).

## Abschluss des Unique Setup

Nachdem Sie Ihre Anmeldedaten eingerichtet haben, müssen Sie Unifi benachrichtigen, da einige zusätzliche Schritte ausgeführt werden müssen, bevor Sie die Integrationseinrichtung abschließen können.  Wenden Sie sich an die Unifi-Kontaktinformationen, die Ihnen zur Verfügung gestellt werden, um anzugeben, dass Sie Ihre Anmeldedaten eingerichtet haben.

Sie müssen eine Ausschluss-Option auswählen und Unifi nach Abschluss benachrichtigen (unter Angabe der gewählten Ausschluss-Option).  Eine Erläuterung der Ausschluss-Optionen finden Sie im [Unifi-Benutzerhandbuch](https://drive.google.com/drive/folders/16seHF45e6bFxHX15zWLqFLEXymCuA_wn).

Sobald Unifi ihre Arbeit abgeschlossen hat, werden sie Sie benachrichtigen und weitere Informationen bereitstellen, die Sie bei der Konfiguration Ihrer Unifi-Instanz unterstützen, einmal die Datenaufzeichnung ausführen und dann, sobald der Abschluss erfolgreich abgeschlossen ist, können Sie Zeitpläne aktivieren.

Für verschiedene Anwendungsfälle wird die folgende Häufigkeit empfohlen:

* Inkonversion: Alle 15 Minuten
* Stand: Alle 15 Minuten
* Löscht: Jeden Tag
* Opt-Outs: Jeden Tag

>[!NOTE]
>
>SEND-Marketing-Ereignis werden standardmäßig aus dem regulären Auftrag herausgefiltert.  Wenn Sie SEND Marketing-Ereignis in Dynamics 365 sehen möchten, müssen Sie den Filter (Schritt 5) des Regressauftrags in Unifi ändern.

Es gibt zwei separate Rollen in Unifi, einem Benutzer mit Eigentümer und einem Benutzer mit schreibgeschütztem Analyst. Ein Benutzer, der Eigentümer ist, kann Aufträge und Zeitpläne ändern, der schreibgeschützte Analyst nicht.  Für eine bestimmte Kundeninstanz kann es nur einen Eigentümer-Benutzer geben.  Wenn der Kunde die als Eigentümer zugewiesene Person ändern muss, kann er mit der angeforderten Änderung eine E-Mail an [adobe-support@unifisoftware.com](mailto:adobe-support@unifisoftware.com) senden.

Die folgenden Videos zeigen die Unifi-Konfiguration, Auftragsdetails, Einrichtung und Überwachung.

## Unifi-Aufträge

### Übersicht über die Unifi-Aufträge

>[!VIDEO](https://video.tv.adobe.com/v/27392)

In diesem Video werden die verschiedenen Unifi-Aufträge erläutert, die für die Integration von Adobe Campaign Standard mit Microsoft Dynamics 365 erforderlich sind (02:10 Min.)

### Unifi-Auftragsdetails: Ingress &amp; Kongress

>[!VIDEO](https://video.tv.adobe.com/v/27396)

In diesem Video werden die Aufnahmen und Aufnahmen in Unifi (04:27 Min.) erläutert.

### Operationalisierung und Überwachung

>[!VIDEO](https://video.tv.adobe.com/v/27391)

In diesem Video werden die Workflows und Zeitpläne (03:03 Min.)

Mehr dazu
* [Arbeiten mit Adobe Campaign Standard - Microsoft Dynamics 365](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)
* [Microsoft Dynamics 365 für die Integration von Kampagnen konfigurieren](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)
* [Adobe IO für Microsoft Dynamics 365 konfigurieren - Integration von Campaign Standards](../../integrating/using/configure-adobe-io-for-ms-dynamic.md)
* [Seite mit den Microsoft Dynamics 365-Integrationsfunktionen](https://helpx.adobe.com/campaign/kt/acs/using/acs-ms-dynamics-crm-connector-tutorial.html)
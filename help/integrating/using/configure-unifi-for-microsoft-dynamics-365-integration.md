---
title: Unifi für die Integration mit Microsoft Dynamics 365 konfigurieren
description: Erfahren Sie, wie Sie Unifi für die Integration mit Microsoft Dynamics 365 konfigurieren.
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
translation-type: ht
source-git-commit: 37e86c6143c52841e69d610fa9db35dff70a3587

---



# Unifi für die Integration mit Microsoft Dynamics 365 konfigurieren

Konfigurieren Sie Unifi, um die Integration mit Microsoft Dynamics 365 und Adobe Campaign einzurichten und zu aktivieren.

## Voraussetzungen

Bevor Sie nach der Bereitstellung die Schritte in diesem Artikel durchführen, wird davon ausgegangen, dass Sie die [Schritte nach der Bereitstellung für Campaign](../../integrating/using/configure-adobe-io-for-ms-dynamic.md) und [für Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)bereits erfolgreich abgeschlossen haben.  Ist dies nicht der Fall, müssen Sie die folgenden Schritte ausführen, um die Aufgaben nach der Bereitstellung für Campaign Standard und Dynamics 365 abzuschließen.

Voraussetzung hierfür ist, dass Sie Unifi kontaktiert haben, ein Unifi-Konto für Sie erstellt wurde und Sie sich erfolgreich anmelden konnten.  Ist dies nicht der Fall, führen Sie die in [diesem Artikel](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)beschriebenen Schritte aus.

>[!CAUTION]
>
>Es wird dringend empfohlen, bei der Konfiguration von Unifi mit Beratern von Unifi und/oder Adobe zusammenzuarbeiten (wenden Sie sich an Ihren Adobe-CSM).

## Campaign-Integration konfigurieren

Wählen Sie bei Ihrer ersten Verbindung **[!UICONTROL Adobe Campaign Standard]** aus, um Ihre Anmeldedaten für Campaign einzugeben.

Die meisten dieser Anmeldedaten stammen aus der Integration, die Sie bei den [Campaign Standard-Konfigurationsschritten](../../integrating/using/configure-adobe-io-for-ms-dynamic.md) in der Adobe I/O-Konsole erstellt haben.

>[!NOTE]
>
>Um die Sicherheit und den Datenschutz zu gewährleisten, werden vertrauliche Felder mit den Anmeldedaten beim erneuten Besuch dieser Konfigurationsbildschirme leer angezeigt.

1. Geben Sie als Adobe-Authentifizierungs-URL `https://ims-na1.adobelogin.com/ims/exchange/jwt` ein.

1. Geben Sie Ihre **[!UICONTROL Adobe IO-Organisationskennung]** und Ihre **[!UICONTROL Adobe IO-Integrationskennung]** ein.

Um Ihre Adobe IO-Organisations- und Integrationskennungen abzurufen, navigieren Sie zum Bildschirm der Adobe I/O-Konsole mit Integrationsinformationen und beachten Sie die Web-URL.

Sie sollte ungefähr so aussehen: `https://console.adobe.io/integrations/<Org ID>/<Int ID>/overview`, wobei &quot;Org ID&quot; und &quot;Int ID&quot; Zahlen sind.

1. Geben Sie Ihre **[!UICONTROL Mandantenkennung]** ein.

Gehen Sie wie folgt vor, um Ihre Mandantenkennung abzurufen:

1. Navigieren Sie zur [Adobe Admin Console](https://adminconsole.adobe.com/) und wählen Sie Ihre IMS-Org aus dem oberen rechten Dropdown-Menü.
1. Wählen Sie Ihr Adobe Campaign Standard-Produkt und dann Ihre Campaign Standard-Instanz aus (wenn Sie mehr als eine haben).  Dadurch wird eine Liste von Produktprofilen angezeigt.

   Die Produktprofilbeschreibungen werden in der Regel in einem der folgenden Formate angezeigt, wobei `<tenantID>` die Mandantenkennung Ihrer Instanz ist.

`Campaign Standard – https://<tenantID> - <ROLE>`

`Campaign Standard – <tenantID> - <ROLE>`

>[!NOTE]
>
>Sollten Sie Probleme bei der Ermittlung Ihrer Mandantenkennung haben, wenden Sie sich an Ihren technischen Ansprechpartner von Adobe oder die Kundenunterstützung von Adobe.
>
>Mandantenkennungen von Partner-Sandbox-Instanzen folgen in der Regel dem Muster `https://<tenantId>`, wobei `tenantId` `tbd.campaign-sandbox.adobe.com` ist.

1. Geben Sie die **[!UICONTROL Kennung Ihrer Campaign-Instanz]** ein.

Gehen Sie wie folgt vor, um die Kennung Ihrer Instanz abzurufen:

    1. Geben Sie &quot;https://&lt;acs-instance-url>/r/test&quot; in einen Webbrowser ein und ersetzen Sie &quot;&lt;acs-instance-url>&quot; durch die URL Ihrer Campaign Standard-Instanz.
    1. Die Antwort enthält &quot;instance=&quot;, gefolgt von der Kennung der Instanz.

1. Wählen Sie Ihre Campaign-Instanz aus.

1. Sie können das **[!UICONTROL Basisverzeichnis]** leer lassen.

1. Wählen Sie die Option **[!UICONTROL Als Ausgabeziel zulassen]** aus.

Nach dem Festlegen der Parameter wählen Sie **[!UICONTROL VERBINDEN]** aus. Prüfen Sie danach, ob die Verbindung erfolgreich hergestellt wurde.

Wenn nicht, wählen Sie **[!UICONTROL SCHLIESSEN]** aus und überprüfen Sie die Parameter.

>[!NOTE]
>
>Wenn Sie diesen Schritt nicht erfolgreich ausführen können, wenden Sie sich an den [Unifi-Kundendienst](mailto:support@unifisoftware.atlassian.net).

## Dynamics 365-Integration konfigurieren

Wählen Sie &quot;Microsoft Dynamics CRM&quot; aus, um Dynamics 365-Anmeldedaten zu konfigurieren. Die meisten dieser Anmeldedaten stammen aus der Integration, die Sie bei den Microsoft Dynamics 365-Konfigurationsschritten in Microsoft Dynamics 365 erstellt haben.

>[!NOTE]
>
>Um die Sicherheit und den Datenschutz zu gewährleisten, werden vertrauliche Felder mit den Anmeldedaten beim erneuten Besuch dieser Konfigurationsbildschirme leer angezeigt.

1. Geben Sie als **[!UICONTROL URL]** die URL Ihrer Dynamics 365-Instanz ein und fügen Sie &quot;.api&quot; vor &quot;.crm&quot; ein (z. B. `https://mydynamicsinstance.api.crm.dynamics.com`).

1. Als **[!UICONTROL clientid]** verwenden Sie die Anwendungs-ID, die beim Erstellen der App-Registrierung als [Konfiguration von Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)generiert wurde.

1. Verwenden Sie für **[!UICONTROL clientsecret]** das Client-Geheimnis, das generiert wurde, als Sie der App-Registrierung ein Client-Geheimnis als [Konfiguration von Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)hinzugefügt haben.

1. Als **[!UICONTROL callbackurl]** fügen Sie `http://localhost:33333` hinzu.

1. Lassen Sie das Feld für **[!UICONTROL Aktualisierungs-Token]** leer.

1. Verwenden Sie für **[!UICONTROLMandantenkennung]** die Mandantenkennung, die Sie von portal.azure.com als [Konfiguration von Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md) erhalten haben.

1. Markieren Sie abschließend die Checkbox **[!UICONTROL Als Ausgabeziel zulassen]**.

Nach der Eingabe der Parameter wählen Sie **[!UICONTROL VERBINDEN]** aus. Prüfen Sie danach, ob die Verbindung erfolgreich hergestellt wurde.

Wenn nicht, wählen Sie **[!UICONTROL SCHLIESSEN]** aus und überprüfen Sie die Parameter.

>[!NOTE]
>
>Wenn Sie diesen Schritt nicht erfolgreich ausführen können, wenden Sie sich an den [Unifi-Kundendienst](mailto:support@unifisoftware.atlassian.net).

## Abschluss der Unifi-Einrichtung

Nach dem Festlegen Ihrer Anmeldedaten müssen Sie Unifi benachrichtigen, da einige zusätzliche Schritte erledigt werden müssen, bevor Sie die Einrichtung der Integration abschließen können.  Teilen Sie Unifi über die Kontaktdaten, die Sie erhalten haben, mit, dass Sie Ihre Anmeldedaten eingerichtet haben.

Wählen Sie eine Opt-out-Option aus und benachrichtigen Sie anschließend Unifi (unter Angabe der gewählten Opt-out-Option).  Eine Erläuterung der Opt-out-Optionen finden Sie im [Unifi-Benutzerhandbuch](https://drive.google.com/drive/folders/16seHF45e6bFxHX15zWLqFLEXymCuA_wn).

Sobald Unifi seine Arbeit getan hat, werden Sie benachrichtigt und erhalten weitere Informationen, die Sie dabei unterstützen, Ihre Unifi-Instanz zu konfigurieren sowie einmal den Dateneingang auszuführen. Nach erfolgreichem Abschluss können Sie dann Zeitpläne aktivieren.

Für verschiedene Anwendungsfälle wird die folgende Häufigkeit empfohlen:

* Eingang: Alle 15 Minuten
* Ausgang: Alle 15 Minuten
* Löschen: Jeden Tag
* Opt-outs: Jeden Tag

>[!NOTE]
>
>SEND-Marketing-Ereignisse werden standardmäßig aus dem Ausgangsvorgang herausgefiltert.  Wenn Sie SEND-Marketing-Ereignisse in Dynamics 365 sehen möchten, müssen Sie den Filter des Ausgangsvorgangs in Unifi ändern (Schritt 5).

Es gibt zwei separate Rollen in Unifi: einen Besitzer-Anwender und einen schreibgeschützten Anwender für Analysen. Ein Anwender, der Besitzer ist, kann Vorgänge und Zeitpläne ändern, der schreibgeschützte Analytiker nicht.  Für jede Kundeninstanz kann es nur einen Anwender geben, der Besitzer ist.  Wenn der Kunde die als Besitzer zugewiesene Person ändern muss, kann er eine E-Mail mit der angeforderten Änderung an [adobe-support@unifisoftware.com](mailto:adobe-support@unifisoftware.com) senden.

Die folgenden Videos veranschaulichen die Unifi-Konfiguration, Details zu Vorgängen, Einrichtung und Überwachung.

## Unifi-Vorgänge

### Übersicht über die Unifi-Vorgänge

>[!VIDEO](https://video.tv.adobe.com/v/27392?captions=ger)

In diesem Video werden die verschiedenen Unifi-Vorgänge erläutert, die für die Integration von Adobe Campaign Standard mit Microsoft Dynamics 365 erforderlich sind (02:10 Min.).

### Unifi-Vorgangsdetails: Eingang und Ausgang

>[!VIDEO](https://video.tv.adobe.com/v/27396?captions=ger)

In diesem Video werden die Eingangs- und Ausgangsvorgänge in Unifi erläutert (04:27 Min.).

### Operationalisierung und Überwachung

>[!VIDEO](https://video.tv.adobe.com/v/27391?captions=ger)

In diesem Video werden die Workflows und Zeitpläne beschrieben (03:03 Min.).

Mehr dazu
* [Verwenden von Adobe Campaign Standard und Microsoft Dynamics 365](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)
* [Microsoft Dynamics 365 für die Integration mit Campaign konfigurieren](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)
* [Adobe I/O für die Integration mit Microsoft Dynamics 365 und Campaign Standard konfigurieren](../../integrating/using/configure-adobe-io-for-ms-dynamic.md)
* [Funktionsseite zur Integration mit Microsoft Dynamics 365](https://helpx.adobe.com/campaign/kt/acs/using/acs-ms-dynamics-crm-connector-tutorial.html)
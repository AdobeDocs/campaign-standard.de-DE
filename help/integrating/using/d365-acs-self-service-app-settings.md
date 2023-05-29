---
title: Campaign-Dynamics-Integrationsanwendung konfigurieren
description: Erfahren Sie, wie Sie die Campaign-Dynamics-Integrationsanwendung konfigurieren.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
feature: Microsoft CRM Integration
role: Data Architect
level: Intermediate
exl-id: 184bc656-2107-4380-9b35-148cb4380547
source-git-commit: 6530ca1726a2aff18c5be9566d8008c317918e64
workflow-type: ht
source-wordcount: '791'
ht-degree: 100%

---

# Systeme mit der Integrationsanwendung verbinden

## Zugangsdaten zur Integrationsanwendung hinzufügen

Im Bildschirm **[!UICONTROL Einstellungen]** können Sie die Zugangsdaten für Microsoft Dynamics 365 und die Adobe-API spezifizieren. Sie können auch die Einstellungen für die Adobe Campaign-SFTP-Instanz konfigurieren.

### Microsoft Dynamics 365-Zugangsdaten

Die Microsoft Dynamics 365-Zugangsdaten geben der Integrationsanwendung die Berechtigung, Ihre Daten aus Microsoft Dynamics 365 abzurufen.  Sie müssen zunächst die Schritte auf dem Bildschirm [Microsoft Dynamics 365 für die Integration mit Campaign konfigurieren](../../integrating/using/d365-acs-configure-d365.md) ausführen, um die Werte zu generieren, die danach in diesen Bildschirm eingefügt werden. Die unten beschriebenen Eingaben beziehen sich auf diesen Bildschirm.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-settings-d365.png)

* **[!UICONTROL Client-ID]**: In [diesem Abschnitt](../../integrating/using/d365-acs-configure-d365.md#register-a-new-app) erfahren Sie, wie Sie Ihre Client-ID referenzieren.

* **[!UICONTROL Client-Geheimnis]**: In [diesem Abschnitt](../../integrating/using/d365-acs-configure-d365.md#generate-a-client-secret) erfahren Sie, wie Sie Ihr Client-Geheimnis generieren.

* **[!UICONTROL Mandant]**: In [diesem Abschnitt ](../../integrating/using/d365-acs-configure-d365.md#get-the-tenant-id) erfahren Sie, wie Sie Ihre Mandantenkennung finden.

* **[!UICONTROL URL]**: Die URL hat das Format `https://&lt;servername&gt;.api.crm.dynamics.com/`

### Adobe-API-Zugangsdaten

Die Adobe Campaign-Zugangsdaten werden mit [Adobe I/O](https://www.adobe.io/) generiert. Sie müssen zuerst den Bildschirm [Adobe I/O konfigurieren](../../integrating/using/d365-acs-configure-adobe-io.md) aufrufen und den Anweisungen folgen, bevor Sie die erforderlichen Felder in diesem Abschnitt ausfüllen können.

In der folgenden Abbildung wird die Zuordnung zwischen Adobe I/O und den Eingaben im Einstellungsbildschirm im Detail erläutert.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-settings-adobeio.png)

* *Privater Schlüssel*: Der Prozess zum Definieren dieses Schlüssels beginnt mit einem Klick auf die Schaltfläche &quot;Generate public/private keypair&quot;. Dadurch wird eine ZIP-Datei erstellt, die Sie herunterladen müssen. Entpacken Sie danach die Datei. Sie erhalten zwei Dateien mit den Namen &quot;certificate_pub.crt&quot; und &quot;private.key&quot;. Bewahren Sie die Datei &quot;private.key&quot; an einem sicheren Ort auf und geben Sie sie nicht weiter. Öffnen Sie die Datei &quot;private.key&quot; in einem Texteditor. Kopieren Sie den gesamten Wert im Texteditor (Strg-A, dann Strg-C auf einem PC oder Cmd-A, dann Cmd-C auf einem Mac). Dies sollte die Zeilen mit &quot;BEGIN PRIVATE KEY&quot; und &quot;END PRIVATE KEY&quot; komplett einschließen. Fügen Sie den gesamten mehrzeiligen Text in das Eingabefeld &quot;Privater Schlüssel&quot; im Einstellungsbildschirm ein.

* *URL*: Dieser Wert entspricht dem Muster https\://mc.adobe.io/&lt;Name-der-Campaign-Instanz>. Die Kopfzeile der Integrationsanwendung enthält sowohl &quot;Org&quot; als auch &quot;Instanz&quot;. Der Teil &quot;Name-der-Campaign-Instanz&quot; der URL entspricht einfach dem in diesem Instanzwert gefundenen Namen.

## Adobe Campaign-SFTP-Einstellungen {#ac-smtp-settings}

Diese Einstellungen sind optional. Sie müssen sie definieren, wenn Sie Ihre Adobe Campaign-SFTP-Instanz zum Ausgeben von Protokollen des Connectors verwenden möchten. Dies ist hilfreich, wenn beim Ausführen der Integration Probleme auftreten und Sie in einer Fehlersuche herausfinden müssen, warum die Ausgabe nicht Ihren Erwartungen entspricht.

Ein weiterer Grund für die Einrichtung des SFTP-Servers wäre, wenn Sie den Opt-in-/Opt-out-Workflow ausführen möchten und Daten **[!UICONTROL unidirektional (Campaign zu Microsoft Dynamics 365)]** oder **[!UICONTROL bidirektional]** von Adobe Campaign zu Microsoft Dynamics 365 fließen.

>[!IMPORTANT]
>
>Sie sind für die Informationen verantwortlich, die Sie aus den SFTP-Ordnern abrufen und herunterladen. Wenn die Informationen personenbezogene Daten enthalten, sind Sie für die Einhaltung der geltenden Datenschutzgesetze und -bestimmungen verantwortlich. [Weitere Informationen](../../integrating/using/d365-acs-notices-and-recommendations.md#acs-msdyn-manage-privacy).

Informationen zur Definition der Campaign-SFTP-Einstellungen für die Integration mit Microsoft Dynamics 365 finden Sie im folgenden Abschnitt:

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-settings-sftp.png)

Sie müssen Folgendes angeben:

* **SFTP-Host**: Dieses Feld enthält &lt;Name-der-Campaign-Instanz>.campaign.adobe.com. Die Kopfzeile der Integrationsanwendung enthält sowohl **Org** als auch **Instanz**. Der Teil &quot;Name-der-Campaign-Instanz&quot; der URL entspricht einfach dem in diesem Instanzwert gefundenen Namen.

* **SFTP-Anwender**: Wenn Sie den SFTP-Anwender kennen, fügen Sie ihn hier hinzu. Anderenfalls finden Sie in [diesem Abschnitt](#ac-control-panel-settings) weitere Informationen. Im Zuge des Prozesses wird Ihnen der Benutzername angezeigt.

* **SFTP-Schlüssel**: Wenn Sie den SFTP-Schlüssel kennen, fügen Sie ihn hier hinzu. Anderenfalls finden Sie in [diesem Abschnitt](#ac-control-panel-settings) weitere Informationen.

* Die **IP-Bereiche** müssen in Ihrer Adobe Campaign-SFTP-Konfiguration enthalten sein. Diese müssen auf die Zulassungsliste gesetzt werden, damit die Integration den SFTP-Endpunkt nutzen kann.

* Mit der Option **Möchten Sie Protokolle in Ihr Adobe Campaign-SFTP exportieren?** können Sie festlegen, ob die Integration Protokollinformationen an den SFTP-Endpunkt ausgibt. Dies kann bei der Fehlersuche helfen, wenn Adobe Campaign oder Microsoft Dynamics 365 nicht die erwarteten Informationen anzeigt.

## SFTP-Einrichtung in Adobe Campaign {#ac-control-panel-settings}

Machen Sie sich in diesen Abschnitten mit der SFTP-Verwaltung über das [Campaign Control Panel](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=de) vertraut:

* [Über die SFTP-Verwaltung](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/about-sftp-management.html?lang=de#sftp-management)

* [SFTP-Speicherverwaltung](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/key-management.html?lang=de#installing-ssh-key)

* [IP-Bereiche hinzufügen](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/ip-range-allow-listing.html?lang=de#sftp-management)

* [Schlüssel verwalten](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/key-management.html?lang=de#sftp-management)

* [Bei Ihrem SFTP-Server anmelden](https://experienceleague.adobe.com/docs/control-panel/using/sftp-management/logging-into-sftp-server.html?lang=de#sftp-management)

Sobald die Konfiguration abgeschlossen ist, melden Sie sich mit dem privaten Schlüssel beim SFTP-Server an und erstellen Sie das Verzeichnis &quot;d365_loads/exports&quot;.

[Auf dieser Seite](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/monitoring-server-capacity.html?lang=de#sftp-management) finden Sie Informationen zum Adobe Campaign Standard-SFTP-Server.

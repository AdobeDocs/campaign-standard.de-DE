---
title: Mobile App konfigurieren
description: Hier erfahren Sie, wie Adobe Campaign konfiguriert werden muss, damit Push-Benachrichtigungen oder In-App-Nachrichten unter Verwendung des Experience Platform SDK gesendet werden können
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: 5f9a8e84-a362-42b6-8bd2-e5d56214c1db
source-git-commit: 7767b39a48502f97e2b3af9d21a3f49b9283ab2e
workflow-type: tm+mt
source-wordcount: '1360'
ht-degree: 62%

---

# Mobile App konfigurieren{#configuring-a-mobile-application}

## Konfiguration einer Mobile App mithilfe von Adobe Experience Platform SDKs {#using-adobe-experience-platform-sdk}

>[!IMPORTANT]
>
> Adobe Experience Platform Launch wurde als eine Suite von Datenerfassungstechnologien in Adobe Experience Platform umbenannt. Infolgedessen wurden in der gesamten Produktdokumentation mehrere terminologische Änderungen eingeführt. Weitere Informationen finden Sie unter [nachstehendes Dokument](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html) für eine konsolidierte Übersicht über die terminologischen Änderungen.

Beachten Sie, dass die Implementierung von Push-Benachrichtigungen und In-App-Benachrichtigungen von erfahrenen Benutzern durchgeführt werden muss. Um Unterstützung zu erhalten, kontaktieren Sie Ihren Adobe-Kundenbetreuer oder Professional Services-Partner.

Um Push-Benachrichtigungen und In-App-Nachrichten mit der Experience Platform SDK-Anwendung zu senden, muss eine Mobile App in der Datenerfassungs-Benutzeroberfläche eingerichtet und in Adobe Campaign konfiguriert werden.

Nach der Einrichtung einer Mobile App können Sie die von ihr erfassten personenbezogenen bzw. PII-Daten abrufen, um Profile aus Ihrer Datenbank zu erstellen oder zu aktualisieren. Weitere Informationen finden Sie unter [Erstellen und Aktualisieren von Profilinformationen auf Basis der von einer Mobile App erfassten Daten](../../channels/using/updating-profile-with-mobile-app-data.md).

Weiterführende Informationen zu den verschiedenen Anwendungsfällen für Mobilgeräte, die in Adobe Campaign Standard in Kombination mit dem Adobe Experience Platform SDK unterstützt werden, finden Sie auf dieser [Seite](../../administration/using/supported-mobile-use-cases.md).

Führen Sie die folgenden Schritte aus, um die Konfiguration abzuschließen:

1. Stellen Sie in Adobe Campaign sicher, dass Sie auf Folgendes zugreifen können:
   * **[!UICONTROL Push-Benachrichtigung]**
   * **[!UICONTROL In-App-Nachricht]**
   * **[!UICONTROL Adobe Places]**

   Ist dies nicht der Fall, kontaktieren Sie das für Ihr Konto zuständige Team.

1. Vergewissern Sie sich, dass Ihr Benutzer über die erforderlichen Berechtigungen in Adobe Campaign Standard und Tags in Adobe Experience Platform verfügt.
   * Stellen Sie in Adobe Campaign Standard sicher, dass der IMS-Benutzer zu den Standardbenutzer- und Administratorproduktprofilen gehört. Dieser Schritt ermöglicht es dem Benutzer, sich bei Adobe Campaign Standard anzumelden, zur Experience Platform SDK-Seite für mobile Apps zu navigieren und die Eigenschaften der mobilen App anzuzeigen, die Sie in der Datenerfassungs-Benutzeroberfläche erstellt haben.

   * Stellen Sie in der Datenerfassungs-Benutzeroberfläche sicher, dass Ihr IMS-Benutzer Teil eines Experience Platform Launch-Produktprofils ist.
Dieser Schritt ermöglicht es dem Benutzer, sich bei der Datenerfassungs-Benutzeroberfläche anzumelden, um die Eigenschaften zu erstellen und anzuzeigen. Weitere Informationen zu Produktprofilen in der Datenerfassungs-Benutzeroberfläche finden Sie unter [Produktprofil erstellen](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/manage-permissions.html?lang=en#gain-admin-rights-for-a-tags-product-profile). Im Produktprofil sollten keine Berechtigungen für das Unternehmen oder die Eigenschaften festgelegt sein, aber der Benutzer sollte sich trotzdem anmelden können.

   Um zusätzliche Aufgaben wie die Installation einer Erweiterung, die Veröffentlichung einer Anwendung, die Konfiguration von Umgebungen usw. durchzuführen, müssen Sie im Produktprofil Berechtigungen festlegen.

1. Erstellen Sie in der Datenerfassungs-Benutzeroberfläche eine **[!UICONTROL Mobileigenschaft]**. Weiterführende Informationen finden Sie unter [Eigenschaft für Mobilgeräte einrichten](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property).

1. Klicken Sie in der Datenerfassungs-Benutzeroberfläche auf die **[!UICONTROL Erweiterungen]** Registerkarte, navigieren Sie zu **[!UICONTROL Katalog]** und suchen Sie nach der **[!UICONTROL Adobe Campaign Standard]** -Erweiterung. Weitere Informationen finden Sie unter [Adobe Campaign Standard](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard).

1. Um Anwendungsfälle für Standorte in Campaign Standard zu unterstützen, installieren Sie die Erweiterungen **[!UICONTROL Places]** und **[!UICONTROL Places Monitor]**.
   * Installieren Sie die **[!UICONTROL Orte]** -Erweiterung in der Datenerfassungs-Benutzeroberfläche. Mehr dazu erfahren Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/places/using/places-ext-aep-sdks/places-extension/places-extension.html?lang=de).
   * Installieren Sie die **[!UICONTROL Places Monitor]** -Erweiterung in der Datenerfassungs-Benutzeroberfläche. Mehr dazu erfahren Sie auf [dieser Seite](https://experienceleague.adobe.com/docs/places/using/places-ext-aep-sdks/places-monitor-extension/using-places-monitor-extension.html?lang=de)

1. Konfigurieren Sie in Adobe Campaign Standard die Eigenschaft für Mobilgeräte, die Sie in der Benutzeroberfläche für die Datenerfassung erstellt haben. Weitere Informationen finden Sie unter [Adobe Experience Platform Launch-App in Adobe Campaign einrichten ](../../administration/using/configuring-a-mobile-application.md#set-up-campaign).

1. Fügen Sie die kanalspezifische Konfiguration für Ihre Mobile-App-Einrichtung hinzu.
Weiterführende Informationen finden Sie unter [Kanalspezifische Anwendungskonfiguration in Adobe Campaign](../../administration/using/configuring-a-mobile-application.md#channel-specific-config).

1. Bei Bedarf können Sie Ihre Tag-Eigenschaft löschen.
Weitere Informationen finden Sie unter [Anwendung löschen](../../administration/using/configuring-a-mobile-application.md#delete-app).

## Technischer Workflow &quot;Mobile App AEPSDK von Launch synchronisieren&quot;  {#aepsdk-workflow}

Nachdem Sie Ihre Eigenschaft für Mobilgeräte in der Datenerfassungs-Benutzeroberfläche erstellt und konfiguriert haben, muss die **[!UICONTROL Mobile App AEPSDK von Launch synchronisieren]** Der technische Workflow synchronisiert nun die in Adobe Campaign Standard importierten Tag-Eigenschaften für Mobilgeräte.

Standardmäßig startet der technische Workflow alle 15 Minuten. Bei Bedarf können Sie den Vorgang manuell neu starten:

1. Wählen Sie in Adobe Campaign Standard im erweiterten Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Workflows]** aus.
1. Öffnen Sie den Workflow **[!UICONTROL Mobile App AEPSDK von Launch synchronisieren (syncWithLaunch)]**.

   ![](assets/launch_10.png)

1. Klicken Sie auf die Aktivität **[!UICONTROL Planung]**.

1. Wählen Sie **[!UICONTROL Vorgezogene Ausführung]** aus.

   ![](assets/launch_11.png)

Ihr Workflow wird jetzt neu gestartet und die in Adobe Campaign Standard importierten Tag-Eigenschaften für Mobilgeräte werden synchronisiert.

## Einrichten der Anwendung in Adobe Campaign {#set-up-campaign}

Um eine mobile Tag-Eigenschaft in Campaign zu verwenden, müssen Sie diese Eigenschaft auch in Adobe Campaign konfigurieren. Stellen Sie in Adobe Campaign sicher, dass der IMS-Benutzer zu den Standardbenutzer- und Administratorproduktprofilen gehört.

Sie müssen warten, bis der technische Workflow ausgeführt und die Eigenschaft &quot;Tag mobile&quot;mit Adobe Campaign synchronisiert wird. Sie können sie dann in Adobe Campaign konfigurieren.

Weitere Informationen zum technischen Workflow &quot;Mobile App AEPSDK von Launch synchronisieren&quot; finden Sie in diesem [Abschnitt](../../administration/using/configuring-a-mobile-application.md#aepsdk-workflow).

>[!NOTE]
>
>Standardmäßig können Administratoren, deren Organisationseinheit auf &quot;ALL&quot; eingestellt ist, die Mobile App bearbeiten.

1. Wählen Sie im erweiterten Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL Mobile App (AEP SDK)]** aus.

   ![](assets/launch.png)

1. Wählen Sie die Mobile App aus, die Sie in der Datenerfassungs-Benutzeroberfläche erstellt haben.
Ihr **[!UICONTROL Property Status]** sollte **[!UICONTROL Bereit zum Konfigurieren]** lauten.

   >[!NOTE]
   >
   >Um die Liste der in der Datenerfassungs-Benutzeroberfläche erstellten Mobile Apps abzurufen, verwendet Campaign Standard standardmäßig den in der Option NmsServer_URL definierten Wert, um nach übereinstimmenden Eigenschaften zu suchen.
   >
   >In einigen Fällen kann sich der Campaign-Endpunkt für eine Mobile App von dem in NmsServer_URL definierten unterscheiden. Definieren Sie in diesem Fall den Endpunkt im `Launch_URL_Campaign` -Option. Campaign verwendet den Wert dieser Option, um in der Datenerfassungs-Benutzeroberfläche nach übereinstimmenden Eigenschaften zu suchen.

   ![](assets/launch_4.png)

1. Sie können die Organisationseinheit Ihrer Mobile App im Abschnitt **[!UICONTROL Zugriffsberechtigung]** ändern, um den Zugriff auf diese Mobile App auf bestimmte Organisationseinheiten zu beschränken. Weiterführende Informationen dazu finden Sie auf dieser Seite.

   Hier kann der Administrator untergeordnete Organisationseinheiten zuweisen, indem er sie aus der Dropdown-Liste auswählt.

   ![](assets/launch_12.png)

1. Um eine Verbindung zwischen Campaign und Tags in Adobe Experience Platform herzustellen, klicken Sie auf **[!UICONTROL Speichern]**.

1. Vergewissern Sie sich, dass der Status der Mobile App von **[!UICONTROL Bereit zum Konfigurieren]** in **[!UICONTROL Konfiguriert]** geändert wurde.

   Wenn die Campaign-Erweiterung &quot;&quot; anzeigt, dass der pkey erfolgreich eingerichtet wurde, können Sie auch überprüfen, ob die Eigenschaft in Campaign erfolgreich eingerichtet wurde.

   ![](assets/launch_5.png)

1. Damit diese Konfiguration wirksam wird, müssen die Änderungen in der Benutzeroberfläche für die Datenerfassung veröffentlicht werden.

   Weitere Informationen finden Sie unter [Konfiguration veröffentlichen](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-configuration).

## Kanalspezifische Mobile-App-Konfiguration in Adobe Campaign {#channel-specific-config}

Ihre mobile App kann jetzt in Campaign für Push-Benachrichtigungen oder In-App-Sendungen verwendet werden. Sie können sie jetzt bei Bedarf weiter konfigurieren, um Ereignisse zu erstellen, die Ihre In-App-Nachrichten auslösen und/oder Push-Zertifikate hochladen.

1. Wählen Sie im erweiterten Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL Mobile App (AEP SDK)]** aus.

1. Wählen Sie die von Ihnen erstellte und konfigurierte Mobile App in der Datenerfassungs-Benutzeroberfläche aus.

1. Fügen Sie auf der Registerkarte **[!UICONTROL Eigenschaften der Mobile App]** Ereignisse hinzu, die in Ihrer mobilen App für Ihre In-App-Nachrichten verfügbar sind.

1. Klicken Sie zum Konfigurieren Ihrer Ereignisse auf **[!UICONTROL Element erstellen]**.

   ![](assets/launch_6.png)

1. Geben Sie einen Namen und eine Beschreibung ein.

   ![](assets/launch_7.png)

1. Wählen Sie **[!UICONTROL Hinzufügen]** aus.

   Das entsprechende Ereignis ist jetzt bei der Erstellung einer In-App-Nachricht auf der Registerkarte „Triggers“ verfügbar. Weitere Informationen finden Sie unter [In-App-Nachricht vorbereiten und senden](../../channels/using/preparing-and-sending-an-in-app-message.md).

1. Geben Sie im Mobile-App-Dashboard im Bereich **[!UICONTROL Gerätespezifische Parameter]** die Anwendungsdetails für jedes Gerät an, einschließlich des Zertifikats für iOS und des Server-Schlüssels für Android.

   Nach dem Hochladen Ihres Zertifikats werden Sie in einer Nachricht benachrichtigt, dass der Upload erfolgreich war. Außerdem wird das Ablaufdatum Ihres Zertifikats angezeigt.

   >[!NOTE]
   >
   >Nachdem Sie das Zertifikat in Adobe Campaign Standard erfolgreich hinzugefügt haben, können Sie Ihre Einstellungen jetzt nicht mehr ändern, da der MCPNS-App nur eine APNS-Plattform (Produktion oder Sandbox) hinzugefügt werden kann.

   ![](assets/launch_8.png)

1. Klicken Sie auf den Tab **[!UICONTROL Abonnenten der Mobile App]**, um eine Liste mit Abonnenten und anderen Informationen zu diesen Abonnenten anzuzeigen, z. B. ob sie sich von Ihren Benachrichtigungen abgemeldet haben.

## Anwendung löschen {#delete-app}

>[!CAUTION]
>
>Das Löschen Ihrer Anwendung kann nicht rückgängig gemacht werden.

Um Ihre Anwendung zu löschen, führen Sie die Schritte unter [Löschen mobiler Eigenschaften](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard#deleting-mobile-properties-in-experience-platform-launch).

Überprüfen Sie nach dem Löschen Ihrer App in Adobe Campaign, ob der Status der Eigenschaften Ihrer App korrekt auf &quot;In Launch gelöscht&quot; aktualisiert wurde.

Wenn Sie diese App vollständig aus Adobe Campaign entfernen möchten, wählen Sie zunächst Ihre App in Adobe Campaign aus und danach &quot;Aus Campaign löschen&quot;.

![](assets/launch_9.png)

---
solution: Campaign Standard
product: campaign
title: Migration von SDK v4-Mobilanwendungen auf Adobe Experience Platform SDK
description: Mit diesem Dokument können Sie Ihre Mobilanwendung von SDK v4 auf Adobe Experience Platform SDK migrieren
audience: channels
content-type: reference
topic-tags: push-notifications
context-tags: mobileApp,overview
translation-type: tm+mt
source-git-commit: 6c171d45d655e4055d4a3c7927f1dd8e0913eeaa
workflow-type: tm+mt
source-wordcount: '1358'
ht-degree: 0%

---


# So migrieren Sie Ihre Mobilanwendung von SDK v4 zu Adobe Experience Platform SDK {#sdkv4-migration}

>[!IMPORTANT]
>
> Der Migrationsprozess ist unumkehrbar.
>
> Bitte lesen Sie das Dokument sorgfältig durch, bevor Sie die Migration Ihrer SDK V4-Mobilanwendung auf Adobe Experience Platform SDK starten.

## Informationen zur SDK V4-Migration

Adobe Campaign Standard verarbeitet Mobilanwendungen mit SDK V4 als separate Anwendungen und mit Adobe Experience Platform SDK.
Nach dem Upgrade der Adobe SDK-Version von v4 auf Adobe Experience Platform müssen Mobilanwendungen weiterhin vorhandene Daten und Kampagnen zum Abonnenten der Anwendung verwenden: Daher ist eine Migration erforderlich.

>[!NOTE]
>
> Auf dieser Seite wird die Migration einer SDK v4-Mobilanwendung zu einer neu erstellten Adobe Experience Platform SDK-Anwendung Dokumente. Ihre SDK v4-Mobilanwendungen werden nicht mit einer Adobe Experience Platform SDK-Mobilanwendung mit dem Status **[!UICONTROL Konfiguriert]** **[!UICONTROL Eigenschaft]** zusammengeführt.

| Was sich nach der Migration nicht ändert |
|:-:|
| Die Verwendung der migrierten SDK V4-Anwendung wirkt sich nicht auf bestehende Versand und Kampagnen aus. |
| Der Name der mobilen Anwendung bleibt gleich. |
| Die Plattformberechtigungen für iOS und Android werden beibehalten. |
| Alle Abonnenten der Anwendung und ihre Daten werden gespeichert. |
| Die vorhandene SDK v4-Mobilanwendung sendet weiterhin Daten (PII-Daten, Abonnenten- und Token-Informationen) an Adobe Campaign Standard. |
| Die **[!UICONTROL Organisatorische Einheit]** der mobilen Anwendung bleibt gleich. |

| Änderungen nach der Migration |
|:-:|
| Die Mobilanwendung ist unter **[!UICONTROL Administration]** > **[!UICONTROL Kanal]** > **[!UICONTROL Mobile App (Adobe Experience Platform SDK)]** verfügbar. Vor der Migration war sie unter **[!UICONTROL Administration]** > **[!UICONTROL Kanal]** > **[!UICONTROL Mobile App (SDK V4)]** verfügbar. |
| Der **[!UICONTROL PII-Endpunkt]** der Anwendung wird geändert. Der ältere **[!UICONTROL PII-Endpunkt sammeln]** funktioniert weiterhin, gesendete Daten gehen nicht verloren. |
| Die Anwendung wird mit einer Adobe Experience Platform Launch **[!UICONTROL Mobile-Eigenschaft]** verknüpft. Es wird als neu erstellte Mobilanwendung verarbeitet. |
| Die ursprüngliche Adobe Experience Platform SDK-Anwendung, die bei der Migration verwendet wird, ist nicht als separate Anwendung vorhanden. Es ist nur die migrierte SDK v4-Anwendung verfügbar. |

## Migrieren der Mobilanwendung von SDK v4 zu Adobe Experience Platform SDK {#how-to-migrate}

Vor der Migration sollten Sie die folgenden Empfehlungen berücksichtigen:

* Der Migrationsprozess ist unumkehrbar.
* Sie sollten die Migration mehrerer Anwendungen nicht gleichzeitig ausführen. Sie sollten auch sicherstellen, dass die Migration einer Anwendung nicht durch mehrere Fenster gleichzeitig ausgelöst wird.
* Stellen Sie vor der Migration sicher, dass Sie die **[!UICONTROL Organisationseinheit]** der mobilen Anwendung, die Sie migrieren möchten, und der Adobe Experience Platform-Anwendung, die Sie für die Migration verwenden, zugewiesen haben.
* Nach der Migration wird die Anwendung zu einer Adobe Experience Platform SDK-Anwendung. Die Änderungen werden mit dem entsprechenden Launch **[!UICONTROL Mobile Property]** verknüpft.

1. Erstellen Sie eine neue **[!UICONTROL Mobile-Eigenschaft]** im Adobe Experience Platform Launch. Weitere Informationen hierzu finden Sie in der [Adobe Experience Platform Launch-Dokumentation](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-mobile-property).

1. Wählen Sie in Adobe Campaign Standard im erweiterten Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungseinstellungen]** > **[!UICONTROL Workflows]** und öffnen Sie den Workflow **[!UICONTROL syncWithLaunch]**. Überprüfen Sie, ob der Workflow ohne Fehler beendet wurde.

1. Überprüfen Sie nach Abschluss des Workflows im Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanal]** > **[!UICONTROL Mobil-App (Adobe Experience Platform SDK)]**, ob die Mobilanwendung in Adobe Campaign Standard verfügbar ist und sich im Status **[!UICONTROL Bereit zum Konfigurieren]** befindet.

   ![](assets/aep_v4_2.png)

1. Wählen Sie unter **[!UICONTROL Administration]** > **[!UICONTROL Kanal]** > **[!UICONTROL Mobile App (SDK V4)]** die SDK V4-Anwendung aus, die Sie migrieren möchten.

1. Wählen Sie die Registerkarte **[!UICONTROL Migration mobiler Anwendungen zu AEP SDK]**.

   ![](assets/aep_v4_3.png)

1. Wählen Sie in der Dropdownliste **[!UICONTROL AEP SDK-Mobilanwendung auswählen, um die aktuelle Anwendung mit]** zusammenzuführen, die zuvor erstellte Adobe Experience Platform SDK-Mobilanwendung aus.

1. Klicken Sie auf **[!UICONTROL Migrieren]**.

   ![](assets/aep_v4_4.png)

1. Klicken Sie im Fenster **[!UICONTROL Migrationsanwendung]** auf **[!UICONTROL OK]**.

   ![](assets/aep_v4_5.png)

1. Das Fenster zum erfolgreichen Abschluss wird angezeigt. Klicken Sie auf **[!UICONTROL Gehe zu Adobe Experience Platform SDK Kanal Liste]**.

1. Vergewissern Sie sich auf der Seite &quot;Liste des Adobe Experience Platform SDK-Kanals&quot;, dass die vorherige V4-Mobilanwendung auf **[!UICONTROL Bereit zum Konfigurieren]** eingestellt ist.

1. Wählen Sie Ihre Mobilanwendung und klicken Sie auf **[!UICONTROL Speichern]**, um die Migration abzuschließen.

Nach dieser Migration werden in der migrierten Anwendung Abonnenten, die mit der V4-Version der mobilen Anwendung erfasst wurden, und neue Abonnenten, die mit der AEP-Version der mobilen Anwendung erfasst wurden, verfügbar sein.

Um die beiden verschiedenen Abonnentypen zu unterscheiden, können Sie ein neues benutzerdefiniertes Feld vom Typ **[!UICONTROL text]** hinzufügen, wenn Sie die benutzerdefinierte Ressource **[!UICONTROL Abonnement auf eine Anwendung (appSubscriptionRcp)]** als `sdkversion` oder `appVersion` erweitern. Weitere Informationen zum Erweitern einer benutzerdefinierten Ressource finden Sie auf dieser [Seite](../../developing/using/creating-or-extending-the-resource.md).
Anschließend müssen Sie die zugehörige Launch **[!UICONTROL Mobile-Eigenschaft]** konfigurieren, um diesen benutzerdefinierten Feldwert im PII-Aufruf erfassen zu senden und die Konfiguration der mobilen Anwendung entsprechend zu ändern.

## Häufig gestellte Fragen {#faq}

### Q: In der SDK v4-Mobilanwendung ist die Registerkarte Migration der Mobilanwendung zum Adobe Experience Platform SDK nicht sichtbar. {#tab-not-visible}

A: Überprüfen Sie im erweiterten Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungseinstellungen]** > **[!UICONTROL Optionen]** den Wert der Option **[!UICONTROL Migration der mobilen App von SDK v4 auf Adobe Experience Platform SDK aktivieren]**. Es sollte auf 1 gesetzt und standardmäßig aktiviert werden. Möglicherweise hat der Administrator sie manuell deaktiviert.

![](assets/aep_v4_1.png)

### Q: Auf der Registerkarte Migration von Mobilanwendungen auf Adobe Experience Platform SDK wird die Meldung Keine Daten angezeigt. {#no-data}

A: In der Liste werden nur die förderfähigen Anwendungen Ihrer **[!UICONTROL Organisationseinheit]** angezeigt. Vergewissern Sie sich bitte, dass Sie über den richtigen Adobe Experience Platform-Antrag für die Migration verfügen. Der **[!UICONTROL Eigenschaftenstatus]** Ihrer Adobe Experience Platform-Anwendung sollte auf **[!UICONTROL Bereit zum Konfigurieren]** und der **[!UICONTROL Migrationsstatus der mobilen App]** auf **[!UICONTROL Nicht migriert]** eingestellt sein.

![](assets/aep_v4_6.png)

### Q: Warum kann die Adobe Experience Platform SDK-Anwendung mit dem Status &quot;Konfigurierte Eigenschaft&quot;nicht für die Migration verwendet werden? {#property-status}

A: Beim Migrationsprozess werden die SDK v4-Abonnenten und -Attribute beibehalten. Es werden nur die Informationen zum Start aus der Adobe Experience Platform SDK-Anwendung gespeichert. Abonnenten und andere Daten aus der Adobe Experience Platform SDK-Anwendung gehen verloren. Um Datenverluste zu vermeiden, können nur Adobe Experience Platform SDK-Anwendungen mit dem Status **[!UICONTROL Bereit zum Konfigurieren]** **[!UICONTROL Eigenschaft]** migriert werden.

### Q: Wo finde ich nach der Migration meine vorherige SDK v4-Mobilanwendung? {#v4-app-not-visible}

A: Die Mobilanwendung nach der Migration wird über das erweiterte Menü **[!UICONTROL Administration]** > **[!UICONTROL Kanal]** > **[!UICONTROL Mobilanwendung (Adobe Experience Platform SDK)]** angezeigt.

### Q: Wo finde ich nach der Migration meine neu erstellte Adobe Experience Platform SDK-Anwendung? {#aep-not-visible}

A: Die neu erstellte Adobe Experience Platform SDK-Anwendung, die für die Migration verwendet wird, ist nicht als separate Anwendung vorhanden. Es ist nur die migrierte SDK v4-Anwendung verfügbar.

### Q: Wenn für die SDK v4-Mobilanwendung &quot;Organisatorische Einheit&quot;der Wert A (untergeordnetes Element der Organisationseinheit ALL) und für das Adobe Experience Platform-SDK der Wert ALL festgelegt ist. Wie kann ich meine Mobilanwendung migrieren? {#v4-org-unit}

A: Administratoren der **[!UICONTROL Organisatorischen Einheit]** ALL sind berechtigt, beide Mobilanwendungen zu verwalten und für die Migration zuständig.

### Q: Wenn für die SDK v4-Mobilanwendung &quot;Organisatorische Einheit&quot;die Einstellung &quot;A&quot;und für die Adobe Experience Platform SDK-Anwendung die Einstellung &quot;B&quot;festgelegt ist (eine Geschwistereinheit der Organisationseinheit A). Wie kann ich meine Mobilanwendung migrieren? {#aep-org-unit}

A: Die Adobe Experience Platform SDK-Anwendung, die das Asset einer verbundenen **[!UICONTROL Organisatorischen Einheit]** ist, ist für Benutzer der **[!UICONTROL Organisatorischen Einheit]** nicht sichtbar. Die Mobilanwendung steht den Administratoren von **[!UICONTROL Organisatorische Einheit]** ALL zur Verfügung, wir empfehlen diesen Administratoren jedoch nicht, die Mobilanwendung zu migrieren.
In diesem Fall sollten Sie Ihre Mobilanwendungen in derselben **[!UICONTROL Unternehmenseinheit]** oder in einer **[!UICONTROL Unternehmenseinheit]** mit einem übergeordneten Link verschieben.
Weitere Informationen zu **[!UICONTROL Unternehmenseinheit]** finden Sie in diesem [Abschnitt](../../administration/using/organizational-units.md).

### Q: Auf der Seite Ihrer Adobe Experience Platform SDK-Mobilanwendung (migriert von Ihrer v4-Mobilanwendung) werden unter der Dropdownliste Push-Kanal-Einstellungen keine Informationen wie das hochgeladene Datum/der hochgeladene Name für den Android-Schlüssel oder das iOS-Zertifikat {#no-information-v5} angezeigt

A: Das System speichert diese Informationen nicht, wenn die SDK V4-Mobilanwendung erstellt wird. Wenn Sie Ihre SDK V4-Mobilanwendung auf eine Adobe Experience Platform SDK-Mobilanwendung migrieren, enthält Ihre migrierte Mobilanwendung ebenfalls keine derartigen Informationen. Sobald ein Benutzer ein neues iOS-Zertifikat oder einen Android-Schlüssel hochgeladen hat, werden die verschiedenen Details des Schlüssels oder Zertifikats in der Dropdown-Liste **[!UICONTROL Push Kanal settings]** korrekt gespeichert und angezeigt.

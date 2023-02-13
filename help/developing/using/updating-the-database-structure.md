---
title: Datenbankstruktur aktualisieren
description: Hier erfahren Sie, wie Sie die Adobe-Campaign-Datenbank aktualisieren.
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
context-tags: deploy,main;eventCusResource,overview
feature: Data Model
role: Developer
level: Experienced
exl-id: fa39eb54-9ec0-4aff-94a8-5459f4c496d0
source-git-commit: bee4da592e0b3727949bc44c6e41b81d4e7e73d4
workflow-type: ht
source-wordcount: '815'
ht-degree: 100%

---

# Datenbankstruktur aktualisieren{#updating-the-database-structure}

Damit Ihre Änderungen am Datenmodell wirksam werden und Sie sie verwenden können, muss die Datenbankstruktur aktualisiert werden.

>[!NOTE]
>
>Benutzerdefinierte Ressourcen werden im Zuge der automatischen Aktualisierungen durch Adobe automatisch aktualisiert.

## Benutzerdefinierte Ressource veröffentlichen   {#publishing-a-custom-resource}

Zur Übernahme der Änderungen der Ressourcen muss die Datenbank aktualisiert werden.

>[!NOTE]
>
>Wenn ein Feld einer für ein Ereignis verwendeten benutzerdefinierten Ressource geändert oder gelöscht wird, wird die Veröffentlichung des zugehörigen Ereignisses automatisch aufgehoben. Siehe [Veröffentlichung von Transaktionsereignissen aufheben](../../channels/using/publishing-transactional-event.md#unpublishing-an-event).

1. Greifen Sie mithilfe des Adobe Campaign-Logos oben links im Bildschirm und der Schaltflächen **[!UICONTROL Administration]** > **[!UICONTROL Entwicklung]** > **[!UICONTROL Veröffentlichen]** auf das entsprechende Menü zu.
1. Standardmäßig ist die Option **[!UICONTROL Änderungen seit der letzten Veröffentlichung ermitteln]** aktiv. Dies bedeutet, dass nur die Änderungen übernommen werden, die seit der letzten Veröffentlichung vorgenommen wurden.

   >[!NOTE]
   >
   >Die Option **[!UICONTROL Struktur der Datenbank reparieren]** ermöglicht die Wiederherstellung einer korrekten Konfiguration, falls die Veröffentlichung fehlschlägt. Eventuell direkt an der Datenbank und nicht über benutzerdefinierte Ressourcen vorgenommene Änderungen werden gelöscht.

   ![](assets/schema_extension_12.png)

1. Starten Sie die Analyse mithilfe der Schaltfläche **[!UICONTROL Veröffentlichung vorbereiten]**. Beachten Sie, dass Aktualisierungen großer Tabellen nur dann vorgenommen werden sollten, wenn auf der Instanz nicht übermäßig viele Workflows ausgeführt werden.

   Weiterführende Informationen zu Aktionen bei der Profiles &amp; Services API finden Sie im Abschnitt [Ressource mit API-Erweiterung veröffentlichen](#publishing-a-resource-with-api-extension).

   ![](assets/schema_extension_13.png)

   >[!NOTE]
   >
   >Da doppelte Indizes dazu führen, dass die Veröffentlichung fehlschlägt, wird im Vorbereitungsschritt überprüft, ob der für die Ressource definierte Index bereits mit demselben Namen für eine andere Ressource vorhanden ist. In diesem Fall wird eine Fehlermeldung angezeigt, in der Sie aufgefordert werden, den Index umzubenennen. Siehe [Indizes definieren](configuring-the-resource-s-data-structure.md#defining-indexes).

1. Nach erfolgreicher Analyse können Sie unter Verwendung der Schaltfläche **[!UICONTROL Veröffentlichen]** die Konfigurationsänderungen übernehmen.
1. Im Anschluss an die Veröffentlichung werden in der **[!UICONTROL Zusammenfassung]** der entsprechenden Ressourcen der Status **[!UICONTROL Veröffentlicht]** und das letzte Veröffentlichungsdatum angezeigt.

   >[!NOTE]
   >
   >Bei jeder weiteren Änderung einer Ressource ist zur Übernahme der Änderungen der Aktualisierungsvorgang zu wiederholen.

   Sollten Sie vor der Veröffentlichung Ressourcen mit dem Status **[!UICONTROL Initialisierung ausstehend]** haben, fordert Sie ein Hinweis dazu auf, den Vorgang erneut zu prüfen. Denn die durch die Veröffentlichung vorgenommenen Änderungen an der Datenstruktur (Löschen von Spalten oder Tabellen etc.) sind unwiderruflich. Gehen Sie zur Prüfung in den Tab **[!UICONTROL SQL-Script]**. Hier wird der im Zuge der Veröffentlichung ausgeführte SQL-Befehl angezeigt.

   ![](assets/schema_extension_scriptsql.png)

   >[!NOTE]
   >
   >Der Initialisierungsprozess kann durch die Verwendung der Schaltfläche **[!UICONTROL Zurücksetzung abbrechen]** gestoppt werden. Dadurch nimmt die Ressource ihren ursprünglichen Status an.

1. Wenn Ihre Veröffentlichung fehlgeschlagen ist, können Sie zur vorherigen Veröffentlichung zurückkehren, indem Sie die Option **[!UICONTROL Zurück zur letzten erfolgreichen Veröffentlichung]** auswählen.

   Wenn Sie eine Veröffentlichung in einem Fehlerstatus belassen, öffnet sich bei der Anmeldung bei Ihrer Instanz ein Fenster, das Sie an die Fehlerbehebung bei dieser Veröffentlichung erinnert. Ihre Instanz wird erst mit neuen Produktversionen aktualisiert, wenn Ihre Veröffentlichung korrigiert wurde.

   ![](assets/schema_extension_31.png)

## Ressource mit API-Erweiterung veröffentlichen   {#publishing-a-resource-with-api-extension}

In folgenden Fällen können Sie die Profiles &amp; Services API erstellen:

* Beim Erweitern der benutzerdefinierten Ressourcen **[!UICONTROL Profile]** oder **[!UICONTROL Dienste]** können Sie eine Aktualisierung der Profiles &amp; Services API ausführen, um die in der Erweiterung der benutzerdefinierten Ressourcen deklarierten Felder zu integrieren.
* Wenn Sie eine Ressource definieren und eine Verknüpfung zwischen den **[!UICONTROL Profil]**- oder **[!UICONTROL Dienst]**-Ressourcen und der benutzerdefinierten Ressource erstellen, können Sie die neue Ressource mit einer Aktualisierung in die API einschließen.

Sie können diese Option im Veröffentlichungsbildschirm auswählen.

* Wenn die API noch nicht veröffentlicht wurde (d. h. wenn Sie die Ressource nie erweitert haben oder diese Option oder diese oder eine andere Ressource noch nie aktiviert haben), können Sie auswählen, ob Sie sie erstellen möchten oder nicht.

   ![](assets/create-profile-and-services-api.png)

* Wenn die API bereits veröffentlicht wurde (d. h. wenn Sie die Ressource schon erweitert und diese Option aktiviert haben), wird die API-Aktualisierung erzwungen.

   Nachdem die API erstellt wurde, wird sie bei jeder neuen Veröffentlichung automatisch aktualisiert. Dadurch wird verhindert, dass die Profil- oder Dienst-Ressource dieser API fehlerhaft werden und Ihrer Instanz schaden könnte.

Beachten Sie, dass standardmäßig die benutzerdefinierte Ressource integriert ist. Wenn Sie aber zur Gewährleistung eines bestimmten Verhaltens diese Ressource nicht veröffentlichen möchten, können Sie die Option **[!UICONTROL Diese Ressource in APIs verbergen]** in **[!UICONTROL Eigenschaften der Ressource]** auswählen.

![](assets/removefromextoption.png)

Nach dem Schritt **[!UICONTROL Veröffentlichung vorbereiten]** wird in Adobe Campaign im Tab **[!UICONTROL Vorschau der Profiles &amp; Services API]** die Differenz zwischen der aktuellen und der zukünftigen API-Version nach der Veröffentlichung angezeigt. Wenn Sie die API zum ersten Mal erweitern, wird bei der Differenzspeicherung die native Definition der benutzerdefinierten Ressource mit Ihrer Erweiterung verglichen.

Die im Tab angezeigten Informationen sind in drei Abschnitte unterteilt: hinzugefügte, gelöschte und geänderte Elemente.

![](assets/extendpandsapi_diff.png)

Bei der Differenzanalyse handelt es sich um einen notwendigen Schritt, da während der Veröffentlichungsphase das API-Verhalten geändert und höchstwahrscheinlich die umliegende Entwicklung im Dominoeffektverfahren beeinflusst wird.

>[!NOTE]
>
>Bei dieser Veröffentlichung wird die API **[!UICONTROL profilesAndServicesExt]** aktualisiert. Die API **[!UICONTROL profilesAndServices]** wird nicht aktualisiert.

Weitere Informationen zu Adobe Campaign Standard-APIs finden Sie in [diesem Abschnitt](../../api/using/get-started-apis.md).

---
title: Datenbankstruktur aktualisieren
seo-title: Datenbankstruktur aktualisieren
description: Datenbankstruktur aktualisieren
seo-description: Hier erfahren Sie, wie Sie die Adobe-Campaign-Datenbank aktualisieren.
page-status-flag: nie aktiviert
uuid: 6 c 802 f 4 f-d 298-4 ca 4-acdb -09 f 2 ad 3865 b 9
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird entwickelt
content-type: Referenz
topic-tags: adding-or-extending-a-resource
discoiquuid: 2448 b 126-66 b 8-4608-aa 6 c -8028 fb 1902 a 4
context-tags: deploy, main; Eventcusresource, overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 806dc4736ffb395a0eea102090c688102478aaca

---


# Datenbankstruktur aktualisieren{#updating-the-database-structure}

Damit Ihre Änderungen am Datenmodell wirksam werden und Sie sie verwenden können, muss die Datenbankstruktur aktualisiert werden.

>[!NOTE]
>
>Benutzerdefinierte Ressourcen werden im Zuge der automatischen Aktualisierungen durch Adobe automatisch aktualisiert.

## Benutzerdefinierte Ressource publizieren {#publishing-a-custom-resource}

Zur Übernahme der Änderungen der Ressourcen muss die Datenbank aktualisiert werden.

>[!NOTE]
>
>Wenn ein Feld einer für ein Ereignis verwendeten benutzerdefinierten Ressource geändert oder gelöscht wird, wird das zugehörige Ereignis automatisch depubliziert. Siehe [Transaktionsnachrichten konfigurieren](../../administration/using/configuring-transactional-messaging.md).

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]**, then **[!UICONTROL Publishing]**.
1. Standardmäßig ist die Option **[!UICONTROL Änderungen seit der letzten Publikation ermitteln]aktiv. Dies bedeutet, dass nur die Änderungen übernommen werden, die seit der letzten Publikation vorgenommen wurden.**

   >[!NOTE]
   >
   >Die Option **[!UICONTROL Struktur der Datenbank reparieren]ermöglicht die Wiederherstellung einer korrekten Konfiguration, falls die Publikation fehlschlägt.** Eventuell direkt an der Datenbank und nicht über benutzerdefinierte Ressourcen vorgenommene Änderungen werden gelöscht.

   ![](assets/schema_extension_12.png)

1. Starten Sie die Analyse mithilfe der Schaltfläche **[!UICONTROL Publikation vorbereiten.]** Beachten Sie, dass Aktualisierungen großer Tabellen nur dann vorgenommen werden sollten, wenn auf der Instanz nicht übermäßig viele Workflows ausgeführt werden.

   Weiterführende Informationen zu Aktionen bei der Profiles &amp; Services API finden Sie im Abschnitt [Ressource mit API-Erweiterung publizieren](../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension).

   ![](assets/schema_extension_13.png)

1. Nach erfolgreicher Analyse können Sie unter Verwendung der Schaltfläche **[!UICONTROL Publizieren]die Konfigurationsänderungen übernehmen.**
1. Im Anschluss an die Publikation werden in der **[!UICONTROL Zusammenfassung]** der entsprechenden Ressourcen der Status **Publiziert]und das letzte Publikationsdatum angezeigt.[!UICONTROL **

   >[!NOTE]
   >
   >Bei jeder weiteren Änderung einer Ressource ist zur Übernahme der Änderungen der Aktualisierungsvorgang zu wiederholen.

   Sollten Sie vor der Publikation Ressourcen mit dem Status **[!UICONTROL Initialisierung ausstehend]haben, fordert Sie ein Hinweis dazu auf, den Vorgang erneut zu prüfen. In der Tat sind die durch die Publikation vorgenommenen Änderungen an der Datenstruktur (Löschen von Spalten oder Tabellen etc.) unwiderruflich.** Gehen Sie zur Prüfung in den Tab **[!UICONTROL SQL-Script.]** Hier wird der im Zuge der Publikation ausgeführte SQL-Befehl angezeigt.

   ![](assets/schema_extension_scriptsql.png)

   >[!NOTE]
   >
   >Der Initialisierungsprozess kann durch die Verwendung der Schaltfläche **[!UICONTROL Zurücksetzung abbrechen]gestoppt werden.** Dadurch nimmt die Ressource ihren ursprünglichen Status an.

1. If your publication failed, you can always go back to the previous publication by clicking **[!UICONTROL Back to latest successful publication]**.

   Wenn Sie eine Publikation in einem Fehlerstatus belassen, öffnet sich bei der Anmeldung bei Ihrer Instanz ein Fenster, das Sie an die Fehlerbehebung bei dieser Publikation erinnert. Ihre Instanz wird erst mit neuen Produktversionen aktualisiert, wenn Ihre Publikation korrigiert wurde.

   ![](assets/schema_extension_31.png)

## Ressource mit API-Erweiterung publizieren {#publishing-a-resource-with-api-extension}

In folgenden Fällen können Sie die Profiles &amp; Services API erstellen:

* When you extend the custom resources **[!UICONTROL Profiles]** or **[!UICONTROL Services]**, you can perform an update of the Profiles and Services API to integrate the fields declared in the custom resources extension.
* Wenn Sie eine Ressource definieren und eine Verknüpfung zwischen den **[!UICONTROL Profil]**- oder **Dienst]-Ressourcen und der benutzerdefinierten Ressource erstellen, können Sie die neue Ressource mit einer Aktualisierung in die API einschließen.[!UICONTROL **

Sie können diese Option im Publikationsbildschirm auswählen.

* Wenn die API noch nicht publiziert wurde (d. h. wenn Sie die Ressource nie erweitert haben oder diese Option oder diese oder eine andere Ressource noch nie aktiviert haben), können Sie auswählen, ob Sie sie erstellen möchten oder nicht.

   ![](assets/create-profile-and-services-api.png)

* Wenn die API bereits publiziert wurde (d. h. wenn Sie die Ressource schon erweitert und diese Option aktiviert haben), wird die API-Aktualisierung erzwungen.

   Nachdem die API erstellt wurde, wird sie bei jeder neuen Publikation automatisch aktualisiert. Dadurch wird verhindert, dass die Profil- oder Dienst-Ressource dieser API fehlerhaft werden und Ihrer Instanz schaden könnte.

Note that by default, the custom resource is integrated, but, for a specific behavior, if you don't want to publish this resource, you can select the option **[!UICONTROL Hide this resource from APIs]** available in the **[!UICONTROL Resource Properties]**.

![](assets/removefromextoption.png)

After the **[!UICONTROL Prepare Publication]** step, Adobe Campaign displays the delta between the current version of the API and the future version after the publication in the tab **[!UICONTROL Profiles &amp; Services API Preview]**. Wenn Sie die API zum ersten Mal erweitern, wird bei der Differenzspeicherung die native Definition der benutzerdefinierten Ressource mit Ihrer Erweiterung verglichen.

Die im Tab angezeigten Informationen sind in drei Abschnitte unterteilt: hinzugefügte, gelöschte und geänderte Elemente.

![](assets/extendpandsapi_diff.png)

Bei der Differenzanalyse handelt es sich um einen notwendigen Schritt, da während der Publikationsphase das API-Verhalten geändert und höchstwahrscheinlich die umliegende Entwicklung im Dominoeffektverfahren beeinflusst wird.

>[!NOTE]
>
>Bei dieser Publikation wird die API **[!UICONTROL profilesAndServicesExt],** Die API **[!UICONTROL profilesAndServices]wird nicht aktualisiert.**

Lesen Sie für weiterführende Informationen zur Adobe-Campaign-API die entsprechende Adobe-Campaign-Dokumentation auf [Adobe IO](https://docs.campaign.adobe.com/doc/standard/en/adobeio.html).

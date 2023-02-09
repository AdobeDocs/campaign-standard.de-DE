---
title: In-App-Nachricht vorbereiten und senden
description: Mit einer In-App-Nachricht können Sie Ihre App-Abonnenten mit spezifischen Inhalten ansprechen.
audience: channels
content-type: reference
topic-tags: in-app-messaging
context-tags: delivery,triggers,back;deliveryCreation,wizard
feature: In App
role: User
exl-id: ef83d991-302b-491e-9cdb-07f5da7a5971
source-git-commit: 7767b39a48502f97e2b3af9d21a3f49b9283ab2e
workflow-type: tm+mt
source-wordcount: '1337'
ht-degree: 100%

---

# In-App-Nachricht vorbereiten und senden{#preparing-and-sending-an-in-app-message}

In Adobe Campaign sind drei Arten von In-App-Nachrichten verfügbar:

* **[!UICONTROL Nutzer der Zielgruppe auf der Basis ihres Campaign-Profils (inAppProfile)]**: Mit diesem Nachrichtentyp können Sie Adobe Campaign-Profile (CRM-Profile) auswählen, die sich für Ihre Mobile App angemeldet haben. Dieser Nachrichtentyp kann mit allen in Adobe Campaign verfügbaren Profilattributen personalisiert werden, erfordert aber einen sicheren Handshake zwischen dem Mobile SDK und dem In-App-Messaging-Dienst von Campaign, um sicherzustellen, dass Nachrichten mit personenbezogenen und sensiblen Informationen nur von autorisierten Benutzern verwendet werden.

   Um diesen Nachrichtentyp mit den Geräten der Benutzer herunterzuladen, muss das Mobile SDK Verknüpfungsfelder zur Verknüpfung eines mobilen Profils mit einem CRM-Profil in Adobe Campaign senden. Weiterführende Informationen zu SDK APIs zur Unterstützung von In-App-Nachrichten finden Sie auf dieser [Seite](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard/adobe-campaign-standard-api-reference).

* **[!UICONTROL Alle Nutzer einer Mobile App auswählen (inAppBroadcast)]**: Mit diesem Nachrichtentyp können Sie Nachrichten an alle (aktuellen oder künftigen) Benutzer Ihrer Mobile App senden, selbst wenn in Adobe Campaign kein Profil existiert. Bei der Anpassung der Nachrichten ist daher keine Personalisierung möglich, da das Benutzerprofil in Adobe Campaign ggf. gar nicht existiert.
* **[!UICONTROL Nutzer der Zielgruppe auf der Basis ihres mobilen Profils (inApp)]**: Mit diesem Nachrichtentyp können Sie alle bekannten oder anonymen Benutzer einer Mobile App auswählen, von denen ein mobiles Profil in Campaign existiert. Dieser Nachrichtentyp kann nur mit nicht-personenbezogenen und nicht-sensiblen Attributen personalisiert werden und benötigt auch keinen sicheren Handshake zwischen dem Mobile SDK und dem In-App-Messaging-Dienst von Adobe Campaign.

   Weiterführende Informationen zur Verwendung personenbezogener und sensibler Daten finden Sie im Abschnitt [Mobile Profilfelder mit personenbezogenen und sensiblen Daten verwenden](../../channels/using/about-in-app-messaging.md#handling-mobile-profile-fields-with-personal-and-sensitive-data).

![](assets/diagram_inapp.png)

## In-App-Nachricht vorbereiten {#preparing-your-in-app-message}

>[!CAUTION]
>
>Die In-App-Personalisierung wird über ein Verknüpfungsfeld durchgeführt, in dem normalerweise die CRM-ID und/oder die Login-Kennung der Mobile App eingetragen wird. Sie sind allein verantwortlich für die Sicherung dieses Verknüpfungsfeldes und dessen Verwendung in Verbindung mit Adobe Campaign. Wenn Sie Ihr Verknüpfungsfeld nicht ausreichend schützen, könnte die Sicherheit Ihrer personalisierten Nachricht beeinträchtigt werden. Adobe ist nicht für Schäden haftbar, die durch den unbefugten Zugriff oder die unbefugte Verwendung von Profildaten entstehen, falls Sie keine sicheren Verfahren zur Erstellung, Verwaltung und zum Schutz von Verknüpfungsfeldern anwenden.

Die Erstellung einer einzelnen In-App-Nachricht in Adobe Campaign umfasst folgende Schritte:

1. Wählen Sie ausgehend von der Startseite von Adobe Campaign die Karte **[!UICONTROL In-App-Messaging]** aus.

   Sie können eine In-App-Nachricht auch im Tab **Marketingaktivitäten** erstellen, indem Sie die Schaltfläche **[!UICONTROL Erstellen]** auswählen.

   Eine In-App-Nachricht kann auch in einer Kampagne, auf der Startseite von Adobe Campaign oder in einem Workflow erstellt werden.

1. Wählen Sie **In-App-Nachricht** aus.

   ![](assets/inapp_creating.png)

1. Wählen Sie eine zur Zielgruppe der Audience passende Vorlage aus.

   ![](assets/inapp_creating_2.png)

   Standardmäßig haben Sie die Wahl zwischen drei nativen Vorlagen:

   * **[!UICONTROL Nutzer der Zielgruppe auf der Basis ihres Campaign-Profils (inAppProfile)]**
   * **[!UICONTROL Alle Nutzer einer mobilen App auswählen (inAppBroadcast)]**
   * **[!UICONTROL Nutzer der Zielgruppe auf der Basis ihres mobilen Profils (inApp)]**

1. Geben Sie die Eigenschaften der In-App-Nachricht ein und wählen Sie im Feld **[!UICONTROL Mobile App einem Versand zuordnen]** die entsprechende Mobile App aus.

   Wenn keine Programme in der Dropdown-Liste angezeigt werden, stellen Sie sicher, dass sich Ihre Mobile Apps im Status **Konfiguriert** befinden. Programme, die sich im Status **Bereit zur Konfiguration** befinden, erscheinen nicht in der Liste. Weiterführende Informationen zur Konfiguration von Mobile Apps finden Sie auf dieser [Seite](../../administration/using/configuring-a-mobile-application.md#channel-specific-config).

   ![](assets/inapp_creating_3.png)

1. Wählen Sie die Audience für Ihre In-App-Nachricht aus. Ihre Audience wird entsprechend der mit dem Versand verknüpften Mobile App vorab gefiltert.

   Bitte beachten Sie, dass dieser Schritt bei der Option **[!UICONTROL In-App-Broadcast-Nachricht senden (inAppBroadcast)]** nicht nötig ist, da hier alle Benutzer einer Mobile App ausgewählt werden.

   ![](assets/inapp_creating_8.png)

1. Ziehen Sie das Ereignis, das Ihre Nachricht auslösen soll, in den Tab **[!UICONTROL Triggers]**. Durch die Auswahl eines Triggers definieren Sie eine Benutzeraktion, die die Anzeige einer In-App-Nachricht auslöst.

   Vier Ereigniskategorien sind verfügbar:

   * **[!UICONTROL Mobile-App-Ereignisse]**: Benutzerdefinierte Ereignisse, die in Ihrer Mobile App implementiert sind.

      Weiterführende Informationen zum Erstellen von Ereignissen finden Sie auf dieser [Seite](../../administration/using/configuring-a-mobile-application.md).

   * **[!UICONTROL Life-Cycle-Ereignisse]**: Native Life-Cycle-Ereignisse, die vom Adobe Mobile SDK unterstützt werden.

      Weiterführende Informationen zu Life-Cycle-Ereignissen finden Sie auf dieser [Seite](https://experienceleague.adobe.com/docs/mobile-services/android/metrics.html?lang=de).

   * **[!UICONTROL Analytics-Ereignisse]**: Je nach der Konfiguration Ihrer Mobile App werden die folgenden drei Kategorien unterstützt: Adobe Analytics, Kontextdaten oder Ansichtsstatus.

      Bitte beachten Sie, dass diese Ereignisse nur verfügbar sind, wenn Sie eine Adobe Analytics-Lizenz besitzen.

   * **[!UICONTROL Places]**: Die folgenden drei Kategorien nutzen Echtzeit-Standortdaten, um kontextuell relevante mobile Erlebnisse bereitzustellen: Places-Kontextdaten, benutzerdefinierte Places-Metadaten oder Places-Ereignistyp.

      Weiterführende Informationen zu Adobe Places finden Sie in der [Places-Dokumentation](https://experienceleague.adobe.com/docs/places/using/home.html?lang=de).
   ![](assets/inapp_creating_4.png)

1. Bei der Verwendung der Funktion **[!UICONTROL Analytics-Ereignisse]** werden Adobe Analytics- und Ansichtsstatus-Ereignisse abhängig von den in der Analytics-Erweiterung in der Datenerfassungs-UI konfigurierten Report Suites automatisch mit Daten befüllt, während Kontextdaten-Ereignisse manuell hinzugefügt werden müssen.

   Bitte beachten Sie, dass diese Ereignisse nur verfügbar sind, wenn Sie eine Adobe Analytics-Lizenz besitzen.

   ![](assets/inapp_creating_7.png)

1. Wenn Sie einen **[!UICONTROL Places]**-Trigger verwenden, werden Places-Kontextdaten, benutzerdefinierte Places-Metadaten oder der Places-Ereignistyp auf der Basis aller Bibliotheken und ihrer in Adobe Places erstellten POIs automatisch eingefügt.

   Beachten Sie, dass dieser Trigger auf dem Gerät nur für die POIs aus den Bibliotheken angewendet wird, die in der Places-Erweiterung in der Datenerfassungs-UI ausgewählt wurden. Weiterführende Informationen zur Places-Erweiterung und deren Installation finden Sie in dieser [Dokumentation](https://experienceleague.adobe.com/docs/places/using/places-ext-aep-sdks/places-extension/places-extension.html?lang=de).

1. Wählen Sie im Tab **[!UICONTROL Frequenz &amp; Dauer]** die Häufigkeit für Ihren Trigger, das Start- und Enddatum sowie den Wochentag und die Uhrzeit, zu der Ihre In-App-Nachricht aktiv sein soll.

   ![](assets/inapp_creating_5.png)

1. Bearbeiten Sie den Inhalt Ihrer Nachricht und definieren Sie die erweiterten Optionen. Siehe [In-App-Nachricht anpassen](../../channels/using/customizing-an-in-app-message.md).

   ![](assets/inapp_creating_6.png)

1. Wählen Sie **[!UICONTROL Erstellen]** aus.

Ihre In-App-Nachricht ist jetzt bereit für den Versand an Ihre ausgewählte Audience.

**Verwandte Themen:**

* [In-App-Nachricht anpassen](../../channels/using/customizing-an-in-app-message.md)
* [In-App-Bericht](../../reporting/using/in-app-report.md)
* [In-App-Nachricht in einem Workflow senden](../../automating/using/in-app-delivery.md)

## Vorschau einer In-App-Nachricht erstellen {#previewing-the-in-app-message}

Bevor Sie eine In-App-Nachricht senden, können Sie sie an Testprofilen testen, um zu sehen, wie die Nachricht beim Empfang dargestellt wird.

1. Wählen Sie die **[!UICONTROL Vorschau]**-Schaltfläche aus.

   ![](assets/inapp_sending_2.png)

1. Wählen Sie die Schaltfläche **[!UICONTROL Testprofil auswählen]** und danach eines Ihrer Testprofile aus, um mit der Vorschau des Versands zu beginnen. Weiterführende Informationen zu Testprofilen erhalten Sie in [diesem Abschnitt](../../audiences/using/managing-test-profiles.md).
1. Sehen Sie sich Ihre Nachricht auf verschiedenen Geräten an, wie Android-Geräten, iPhones und Tablets. Sie können dabei auch feststellen, ob Ihre Personalisierungsfelder die richtigen Daten abrufen.


   ![](assets/inapp_sending_3.png)

1. Jetzt können Sie Ihre Nachricht senden und ihre Wirkung mit Versandberichten messen.

## In-App-Nachricht senden {#sending-your-in-app-message}

Nach erfolgreicher Vorbereitung und Validierung Ihres Versands können Sie die Nachricht senden.

1. Wählen Sie **[!UICONTROL Vorbereiten]** aus, um die Zielgruppe zu berechnen und die Nachrichten zu erstellen.

   ![](assets/inapp_sending_4.png)

1. Nach dem erfolgreichen Abschluss der Vorbereitung werden im Fenster **Freigabe** die folgenden KPIs angezeigt: **Zielgruppe** und **Zu senden**.

   Sie können durch Auswahl der Schaltfläche ![](assets/lp_link_properties.png) das Freigabe-Fenster auf potenzielle Ausschlüsse oder Versandfehler prüfen.

   ![](assets/inapp_sending_5.png)

1. Wählen Sie **[!UICONTROL Bestätigen]** aus, um mit dem Versand Ihrer In-App-Nachricht zu beginnen.

   ![](assets/inapp_sending_6.png)

1. Prüfen Sie den Status Ihres Versands über das Nachrichten-Dashboard und die entsprechenden Protokolle. Weiterführende Informationen hierzu finden Sie in diesem [Abschnitt](../../sending/using/monitoring-a-delivery.md).

   Die KPI-Zählungen **[!UICONTROL Zugestellt]** und **[!UICONTROL Gesendet]** repräsentieren die erfolgreichen Sendungen von Campaign zum Nachrichtenversanddienst. Bitte beachten Sie, dass diese KPIs kein Hinweis auf die Anzahl der Mobilgeräte ist, die die Nachricht vom Nachrichtenversanddienst erhalten oder heruntergeladen haben.

   ![](assets/inapp_sending_7.png)

1. Messen Sie die Wirksamkeit Ihrer In-App-Nachrichten mit Versandberichten. Weiterführende Informationen zum Reporting finden Sie in [diesem Abschnitt](../../reporting/using/in-app-report.md).

1. Nach dem Versand Ihrer In-App-Nachrichten können Sie jetzt Ihren Versand deaktivieren. Dies kann nützlich sein, wenn Sie beispielsweise einen bestimmten Versand stoppen möchten oder wenn Sie einen neuen Versand mit demselben Trigger ausführen möchten.

   Klicken Sie auf **[!UICONTROL Deaktivieren]** und dann auf **[!UICONTROL OK]**, um die Deaktivierungsanfrage zu starten.

   ![](assets/inapp_sending_8.png)

1. Nachdem die Anfrage gesendet wurde, wird Ihr Versand deaktiviert und es wird keine andere Nachricht gesendet.

   Beachten Sie, dass Ihre Berichte für diesen Versand weiterhin verfügbar sein werden.

   ![](assets/inapp_sending_9.png)

**Verwandte Themen:**

* [In-App-Bericht](../../reporting/using/in-app-report.md)
* [In-App-Nachricht in einem Workflow senden](../../automating/using/in-app-delivery.md)

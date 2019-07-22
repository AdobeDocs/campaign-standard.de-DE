---
title: Bericht zu Push-Benachrichtigungen
seo-title: Bericht zu Push-Benachrichtigungen
description: Bericht zu Push-Benachrichtigungen
seo-description: Im vordefinierten Bericht über Push-Benachrichtigungen erfahren Sie über die Wirkung Ihrer Push-Benachrichtigung.
page-status-flag: nie aktiviert
uuid: 5 b 121 a 37-1 c 09-4749-a 409-6989978 ddc 4 c
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Berichterstellung
content-type: Referenz
topic-tags: list-of-reports
discoiquuid: a 425 cd 59-edfd -42 c 5-a 6 bd -38773 c 353 ff 0
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 7102ed308f94985f8924a13aab2583e50b6c68e4

---


# Bericht zu Push-Benachrichtigungen{#push-notification-report}

>[!CAUTION]
>
>Bitte beachten Sie, dass Sie die Metrik **[!UICONTROL Nachrichtentyp]in die Tabellen ziehen müssen, um Ihre Daten nach Versandtypen (in diesem Fall Push-Benachrichtigungen) aufzuschlüsseln.**

Der Bericht zu **Push-Benachrichtigungen** liefert Details zur Marketing-Performance von Push-Benachrichtigungen in Adobe Campaign. Dieser native Bericht zeigt, wie Benutzer mit Push-Benachrichtigungen, Mobile Apps und Sendungen interagieren.

Die Mobile App muss entsprechend konfiguriert werden, um Push-Benachrichtigungen zu tracken. Weiterführende Informationen dazu finden Sie auf dieser [Seite](https://helpx.adobe.com/campaign/kb/push-tracking.html).

![](assets/dynamic_report_push.png)

Für jede Tabelle werden Zusammenfassungen und Grafiken erstellt. Die Darstellung dieser Details können Sie in deren Einstellungen ändern.

Die erste Tabelle **Push notification Engagement Summary** (Zusammenfassung der Interaktionen mit Push-Benachrichtigungen) ist in drei Kategorien unterteilt: nach Tag, nach Mobile App und nach Versand. Sie enthält alle verfügbaren Daten zu den Reaktionen der Empfänger auf den Versand.

* **[!UICONTROL Verarbeitet/gesendet]**: Gesamtzahl der gesendeten Push-Benachrichtigungen
* **[!UICONTROL Zugestellt]**: Anzahl der erfolgreich gesendeten Push-Benachrichtigungen in Bezug auf die Gesamtzahl der gesendeten Push-Benachrichtigungen
* **[!UICONTROL Impressionen]**: Anzahl der Wiedergaben einer Push-Benachrichtigung an das Gerät, die im Benachrichtigungszentrum unverändert gelassen werden. In den meisten Fällen sollte die Impressionsnummer der bereitgestellten Zahl ähnlich sein. Dadurch wird sichergestellt, dass das Gerät die Meldung erhalten und diese Informationen an den Server zurückgegeben hat.
* **[!UICONTROL Unique impressions]**: Anzahl der Impressionen eines Empfängers
* **[!UICONTROL Durchklickrate]**: Prozentsatz der Benutzer, die mit der Push-Benachrichtigung interagiert haben
* **[!UICONTROL Öffnungsrate]**: Prozentsatz der geöffneten Push-Benachrichtigungen

![](assets/dynamic_report_push_2.png)

Die zweite Tabelle **Push notification Clicks &amp; opens** (Klicks &amp; Öffnungen in Push-Benachrichtigungen) ist in drei Kategorien unterteilt: nach Tag, nach Mobile App und nach Versand. Sie enthält alle verfügbaren Daten zum Verhalten der Empfänger bei jedem Versand.

* **[!UICONTROL Impressions]**: Gesamtzahl der Push-Benachrichtigungen, die von Empfängern aufgerufen wurden
* **[!UICONTROL Unique impressions]**: Anzahl der Impressionen eines Empfängers
* **[!UICONTROL Klicken]** Sie auf: Anzahl der Wiedergaben einer Push-Benachrichtigung an das Gerät und durch Klicken auf den Benutzer. Der Benutzer wollte die Benachrichtigung entweder anzeigen, die dann zur Push-Öffnung verschoben wird, oder sie wird geschlossen.
* **[!UICONTROL Einzelklicks]**: Anzahl der Interaktionen eines einzelnen Benutzers mit der Push-Benachrichtigung, z. B. Klicks auf die Benachrichtigung oder die Schaltfläche
* **[!UICONTROL Öffnen]**: Gesamtanzahl der an das Gerät übermittelten Push-Benachrichtigungen und angeklickte Benutzer, die die App geöffnet haben. Dies ähnelt dem Push-Klick, außer dass ein Push geöffnet wird, wenn die Benachrichtigung geschlossen wurde.
* **[!UICONTROL Einzelöffnungen]**: Die Anzahl der Empfänger, die den Versand geöffnet haben


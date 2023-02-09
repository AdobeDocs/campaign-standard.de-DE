---
title: Erste Schritte mit dem Integrations-Tool
description: Erste Schritte mit dem Integrations-Tool
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-microsoft-dynamics-365
feature: Microsoft CRM Integration
role: Data Architect
level: Intermediate
exl-id: e73e2069-e86d-4be2-bf73-22e6dc164340
source-git-commit: e7fdaa4b1d77afdae8004a88bbe41bbbe75a3f3c
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 100%

---

# Erste Schritte mit der Selfservice-Integrationsanwendung {#gs-self-service-app}

Mit der Selfservice-Integrationsanwendung zur Integration von Adobe Campaign Standard mit Microsoft Dynamics 365 erhalten Sie die Möglichkeit, Datenflüsse zu konfigurieren und festzulegen, ob und in welcher Umgebung sie ausgeführt werden sollen. Sie müssen jedoch einige Voraussetzungen erfüllen, bevor Sie die Selfservice-Integrationsanwendung verwenden können.

## Konzepte und Einschränkungen {#concepts-and-restrictions}

Bevor Sie mit dem Integrations-Tool beginnen, müssen Sie die mit der Integration verbundenen Konzepte und Leitplanken verstehen und einige erste Schritte unternehmen, um Zugriff zu erhalten.

Weitere Informationen finden Sie in den folgenden Abschnitten:

* [Erste Schritte mit der Integration von Microsoft Dynamics 365](../../integrating/using/d365-acs-get-started.md)
* [Best Practices und Einschränkungen bei der Integration](../../integrating/using/d365-acs-notices-and-recommendations.md)
* [Wichtige Schritte zur Implementierung dieser Integration](../../integrating/using/d365-acs-get-started.md#request-and-implement-this-integration)
* [Verwenden der Integration mit Microsoft Dynamics 365](../../integrating/using/d365-acs-using-the-integration.md)

## Voraussetzungen {#self-service-app-prerequisites}

Sie müssen Microsoft Dynamics 365 und Adobe Campaign Standard so konfigurieren, dass die Integrationsanwendung Zugriff auf Ihre Daten hat. Die Konfiguration in Dynamics 365, Adobe Campaign Standard und Adobe I/O wird einige Zeit in Anspruch nehmen. Nach der Konfiguration können Sie die Integration jedoch über die Benutzeroberfläche der Selfservice-Integrationsanwendung steuern.

Weitere Informationen finden Sie in den folgenden Abschnitten:

* [Konfigurieren von Microsoft Dynamics 365 für die Integration mit Campaign](../../integrating/using/d365-acs-configure-d365.md)
* [Konfigurieren von Adobe I/O](../../integrating/using/d365-acs-configure-adobe-io.md)
* [Zuordnen von benutzerdefinierten Campaign-Ressourcen und benutzerdefinierten Microsoft Dynamics 365-Entitäten](../../integrating/using/d365-acs-notices-and-recommendations.md)

## Wichtige Schritte zum Konfigurieren der Selfservice-Integrationsanwendung {#self-service-app-configuration-steps}

Anschließend können Sie mit der Verwendung des Integrations-Tools beginnen. Gehen Sie wie folgt vor:

1. [Zugriff auf die Integrationsanwendung](../../integrating/using/d365-acs-self-service-app-control-access.md)
1. [Konfigurieren der Integrationsanwendung für Ihre Verwendung](../../integrating/using/d365-acs-self-service-app-settings.md)
1. [Implementieren der Datensynchronisation](../../integrating/using/d365-acs-self-service-app-data-sync.md)
1. [Konfigurieren von Synchronisations-Workflows](../../integrating/using/d365-acs-self-service-app-workflows.md)

## Herstellen einer Verknüpfung mit der Integrationsanwendung {#self-service-app-link}

Öffnen Sie einen Browser und navigieren Sie zum Connector, der mit Ihrer Region verknüpft ist:

* [Asien-Pazifik](https://d365-acs-ap.ea.adobe.com/)
* [Europa, Naher Osten oder Afrika (EMEA)](https://d365-acs-em.ea.adobe.com/)
* [Nord- und Südamerika](https://d365-acs-am.ea.adobe.com/)

## Bestätigung der Datenschutzanfrage {#self-service-app-acknowledgement}

Wenn Sie die Selfservice-Benutzeroberfläche zum ersten Mal aufrufen, wird Ihnen eine Datenschutzbestätigung angezeigt. Sie müssen jeweils bestätigen, dass Sie Ihre Rolle bei der Durchführung von Datenschutzanfragen in Campaign und Microsoft Dynamics 365 verstehen, bevor Sie fortfahren können.
In [diesem Abschnitt](../../integrating/using/d365-acs-notices-and-recommendations.md#acs-msdyn-manage-privacy) erfahren Sie mehr über Ihre Verantwortung für den Datenschutz und darüber, wie Sie Datenschutzanfragen verwalten können.

## Einrichten Ihrer Zugangsdaten {#self-service-app-credentials}

Wenn Sie die Benutzeroberfläche zum ersten Mal aufrufen, sollten Sie folgende Seite mit einer Kopfzeile sehen:

![](assets/do-not-localize/d365-to-acs-ui-header.png)

>[!NOTE]
>
> Es ist normal, dass Sie Warnungen erhalten, in denen Sie darauf hingewiesen werden, dass eine Verbindung zu Adobe Campaign Standard oder Microsoft Dynamics 365 &quot;nicht möglich&quot; ist, wenn die Anwendungseinstellungen noch nicht konfiguriert wurden.

Stellen Sie sicher, dass für &quot;ORG&quot; und &quot;INSTANZ&quot; diejenigen Optionen ausgewählt sind, die Sie konfigurieren möchten.  Sind sie nicht ausgewählt, klicken Sie auf die Dropdown-Liste und wählen Sie die richtige Organisation und Instanz aus.

>[!IMPORTANT]
>
> Wenn Sie den Connector zum ersten Mal konfigurieren und/oder diesen Prozess noch nicht kennen, empfehlen wir Ihnen **dringend**, die Staging- oder Entwicklungsinstanz auszuwählen. Sie sollten sicherstellen, dass Ihre Konfiguration funktioniert, bevor Sie die Einrichtung in der Produktion vornehmen.

Wenn Sie die richtige Organisation und Instanz ausgewählt haben, klicken Sie auf das Dreistrich-Symbol, um ein Dropdown-Menü anzuzeigen. Klicken Sie dann im Dropdown-Menü auf **[!UICONTROL Einstellungen...]**, um die Seite aufzurufen, auf der Sie Ihre Zugangsdaten für Microsoft Dynamics 365 und Campaign eingeben (siehe unten).

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-menu-pointers.png)

Füllen Sie auf der Seite **[!UICONTROL Einstellungen]** die folgenden Abschnitte aus:

* Microsoft Dynamics 365-Zugangsdaten
* Adobe-Zugangsdaten

[Hier](../../integrating/using/d365-acs-self-service-app-settings.md) erfahren Sie, wo die Informationen für die einzelnen Eingaben zu finden sind. Wenn Sie fertig sind, klicken Sie unten auf die Schaltfläche **[!UICONTROL Speichern]**.

## Prüfen der Erstkonfiguration {#self-service-app-initial-config}

Wenn Sie die obigen Voraussetzungen erfüllt und Ihre Zugangsdaten korrekt hinzugefügt haben, können Sie mit der Seite **[!UICONTROL Workflows]** fortfahren. Weitere Informationen zu den Workflows der Integrationsanwendung finden Sie auf [dieser Seite](../../integrating/using/d365-acs-self-service-app-workflows.md).

Klicken Sie auf der Seite **[!UICONTROL Workflows]** auf das Stiftsymbol für den Workflow **[!UICONTROL Microsoft Dynamics 365 zu Campaign]**, um die Konfiguration zu bearbeiten.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-ingress-edit-pointer.png)

Auf der Seite **[!UICONTROL Microsoft Dynamics 365 zu Campaign]** können Sie auf die Liste der Tabellen-Mappings zugreifen, die Sie konfiguriert haben.  Standardmäßig wird ein natives Kontakt-/Profil-Mapping aufgerufen. Alle anderen benutzerdefinierten Entitäten müssen separat konfiguriert werden.

![](assets/do-not-localize/d365-to-acs-ui-page-ingress-top-pointers.png)

Überprüfen Sie auf der Seite **[!UICONTROL Tabellen-Mapping bearbeiten]** den Abschnitt **[!UICONTROL Mappings]**, um sicherzustellen, dass die Felder von Microsoft Dynamics 365 dem korrekten Feld in Campaign zugeordnet werden. Fügen Sie hier etwaige weitere Mappings, Ersetzungen oder Filter hinzu. [Weitere Informationen](../../integrating/using/d365-acs-self-service-app-data-sync.md).

Weitere Informationen zum Hinzufügen neuer Mappings finden Sie in [diesem Abschnitt](../../integrating/using/d365-acs-self-service-app-data-sync.md#add-a-new-mapping).

Wenn die Konfiguration korrekt ist, klicken Sie neben dem Workflow **[!UICONTROL Microsoft Dynamics 365 zu Campaign]** auf die Schaltfläche **[!UICONTROL Abspielen]**, um die Integration und den Datenfluss zu starten.

>[!IMPORTANT]
>
>Wir empfehlen **dringend**, dass Sie diese zuerst in Ihrer Staging- oder Entwicklungsumgebung ausführen, bevor Sie sie in der Produktion starten. Überprüfen Sie, ob die Staging-/Entwicklungsinstanz in der Kopfzeile ausgewählt ist.

![](assets/do-not-localize/d365-to-acs-ui-page-workflows-ingress-play-pointer.png)

Nachdem die Ausführung gestartet wurde, sollten Sie in der Lage sein Ihre Konfiguration zu testen, indem Sie Einträge in Microsoft Dynamics 365 hinzufügen oder ändern und diese Änderungen in Adobe Campaign innerhalb weniger Minuten beobachten. Wenn Sie diesen Prozess zu irgendeinem Zeitpunkt anhalten müssen, drücken Sie einfach auf dieselbe Schaltfläche. [Mehr dazu](../../integrating/using/d365-acs-self-service-app-workflows.md#workflow-status)


## Arbeitsbereich der Integrationsanwendung {#self-service-app-workspace}

### Kopfzeile der Anwendung {#app-header}

In der Kopfzeile der Selfservice-Anwendung können Sie festlegen, welche Organisation und Instanz Sie gerade anzeigen und/oder konfigurieren möchten.

Wählen Sie die **ORG** und **INSTANZ** aus, die Sie anzeigen/bearbeiten möchten. Diese Felder erscheinen schreibgeschützt, können jedoch bearbeitet werden, wenn Sie den Mauszeiger darauf platzieren.

Wenn Sie auf die Schaltfläche mit den drei horizontalen Linien ![](assets//do-not-localize/d365-to-acs-icon-hamburger.png) auf der rechten Seite der Kopfzeile klicken, wird ein Dropdown-Menü angezeigt.

Die Optionen im Dropdown-Menü sind:

* **Einstellungen**: Wenn Sie diese Option auswählen, gelangen Sie zu einem Bildschirm, auf dem Sie API-Zugangsdaten für Microsoft Dynamics 365 und Adobe Campaign sowie andere allgemeine Anwendungseinstellungen eingeben können.

* **Dokumentation**: Hier finden Sie einen Link zur Adobe Campaign-Dokumentation, die sich speziell auf diese Integration bezieht.

* **Kundenunterstützung**: Hier finden Sie einen Link zur Experience Cloud-Dokumentation und zum Erstellen eines Tickets bei der Kundenunterstützung.

* **Abmelden**: Damit melden Sie sich bei der Anwendung ab und können sich als anderer Benutzer wieder anmelden.

* **Info**: Damit wird ein Dialogfeld angezeigt, das Informationen über die Anwendung enthält, einschließlich Copyright-Informationen.

### Breadcrumbs {#app-breadcrumbs}

Breadcrumbs werden oben auf einigen Bildschirmen angezeigt, während Sie in der Anwendung navigieren.

**Beispiel:**

Nachfolgend finden Sie ein Beispiel aus dem Bildschirm **[!UICONTROL Tabellen-Mapping bearbeiten]**, in dem die Breadcrumbs und der Seitentitel angezeigt werden. In diesem Fall können Sie auf den Text **[!UICONTROL Workflows]** oder **[!UICONTROL Microsoft Dynamics 365 zu Campaign]** klicken, um zu einem der vorherigen Bildschirme zu wechseln. **[!UICONTROL Tabellen-Mapping bearbeiten]** ist in diesem Fall in den Breadcrumbs nicht anklickbar, da es sich um den aktuellen Bildschirm handelt.

![](assets/do-not-localize/d365-to-acs-breadcrumbs-ingress.png)

### Allgemeine Schaltflächen {#app-buttons}

Die folgenden Symbole werden auf mehreren Seiten der Selfservice-Anwendung verwendet.

![](assets/do-not-localize/d365-to-acs-icon-add.png): Ein neues Element zu einer Liste hinzufügen.

![](assets/do-not-localize/d365-to-acs-icon-edit.png): Vorhandenen Inhalt bearbeiten.

![](assets/do-not-localize/d365-to-acs-icon-delete.png): Ein Element aus einer Liste von Elementen löschen.

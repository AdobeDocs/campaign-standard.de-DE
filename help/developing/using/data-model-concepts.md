---
title: Datenmodelle
description: Hier erfahren Sie über die Datenmodelle von Adobe Campaign und deren Änderungsmöglichkeiten.
page-status-flag: never-activated
uuid: cacd563f-6936-4b3e-83e3-5d4ae31d44e8
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: about-custom-resources
discoiquuid: 4e0468da-3052-4ce5-8174-45aba1f5c4ed
context-tags: cusResource,overview;eventCusResource,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 71ee939b6ef256be8c693ec6e15d9609c7e80677

---


# Datenmodelle{#data-model-concepts}

Adobe Campaign enthält ein vordefiniertes Datenmodell. Dieses Datenmodell kann von [Administratoren](../../administration/using/users-management.md#functional-administrators) mit neuen Ressourcen oder Erweiterungen vorhandener Ressourcen abgeändert werden.

>[!CAUTION]
>
>Die Erstellung und Änderung von Ressourcen sind heikle Aufgaben, die nur von erfahrenen Benutzern durchgeführt werden können.

Das über das Adobe-Campaign-Logo verfügbare Menü **[!UICONTROL Administration]** &gt; **[!UICONTROL Entwicklung]** dient der Verwaltung von **benutzerdefinierten Ressourcen**, ihrer **Publikation** und dem **Zugriff auf Monitoring-Tools**.

Die von Adobe Campaign verwendeten Daten werden mithilfe verschiedener Ressourcen beschrieben. Es besteht die Möglichkeit der **Anreicherung des zur Verfügung gestellten Datenmodells** durch benutzerdefinierte Ressourcen.

Sie können also beispielsweise Tabellen mit Verkaufs- oder Produktdaten erstellen. Native Anwendungsressourcen (Kampagnen, E-Mails oder Audiences) können nicht geändert werden. Sie können jedoch erweitert werden, um neue Felder hinzuzufügen.

Aus Ressourcenerweiterungen stammende Felder werden mit einem Präfix versehen. Auf diese Weise entstehen keine Konflikte mit nativen Anwendungsfeldern.

>[!NOTE]
>
>Eine Darstellung des Datenmodells für vordefinierte Ressourcen finden Sie [hier](https://docs.campaign.adobe.com/doc/standard/en/datamodel/datamodel.html).

Des Weiteren kann in den der neuen Ressource entsprechenden Bildschirmen die **Navigation konfiguriert werden**.

Sie können benutzerdefinierte Ressourcen **exportieren und importieren** , z. B. aus einer Entwicklungsumgebung in eine Produktionsumgebung. For more on this, refer to this [step-by-step use case](../../automating/using/exporting-importing-custom-resources.md).

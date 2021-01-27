---
solution: Campaign Standard
product: campaign
title: Datenmodelle
description: Hier erfahren Sie über die Datenmodelle von Adobe Campaign und deren Änderungsmöglichkeiten.
audience: developing
content-type: reference
topic-tags: about-custom-resources
context-tags: cusResource,overview;eventCusResource,overview
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 100%

---


# Datenmodelle{#data-model-concepts}

Adobe Campaign enthält ein vordefiniertes Datenmodell. Dieses Datenmodell kann von [Administratoren](../../administration/using/users-management.md#functional-administrators) mit neuen Ressourcen oder Erweiterungen vorhandener Ressourcen abgeändert werden.

>[!CAUTION]
>
>Die Erstellung und Änderung von Ressourcen sind heikle Aufgaben, die nur von erfahrenen Benutzern durchgeführt werden können.

Das über das Adobe Campaign-Logo verfügbare Menü **[!UICONTROL Administration]** > **[!UICONTROL Entwicklung]** dient der Verwaltung von **benutzerdefinierten Ressourcen**, ihrer **Publikation** und dem **Zugriff auf Diagnose-Tools**.

Die von Adobe Campaign verwendeten Daten werden mithilfe verschiedener Ressourcen beschrieben. Es besteht die Möglichkeit der **Anreicherung des zur Verfügung gestellten Datenmodells** durch benutzerdefinierte Ressourcen.

Native Ressourcen (wie Kampagnen, E-Mails oder Audiences) können nicht geändert werden. Sie können jedoch durch Hinzufügen neuer Felder erweitert werden.

Aus Ressourcenerweiterungen stammende Felder werden mit einem Präfix versehen. Auf diese Weise entstehen keine Konflikte mit nativen Anwendungsfeldern.

>[!NOTE]
>
>Eine Darstellung des Datenmodells für die nativen Ressourcen finden Sie auf [dieser Seite](../../developing/using/datamodel-introduction.md).

Des Weiteren kann in den der neuen Ressource entsprechenden Bildschirmen die [Navigation konfiguriert werden](configuring-the-screen-definition.md).

Benutzerdefinierte Ressourcen lassen sich **exportieren und importieren** , z. B. aus einer Entwicklungsumgebung in eine Produktionsumgebung. Weiterführende Informationen dazu finden Sie in diesem [schrittweisen Anwendungsbeispiel](../../automating/using/exporting-importing-custom-resources.md).

>[!CAUTION]
>
>Nur funktionale [Administratoren](../../administration/using/users-management.md#functional-administrators) mit **[!UICONTROL Administratorrolle]** und Zugriff auf **alle** Einheiten können auf Versandlogs, Nachrichtenprotokolle, Trackinglogs, Ausschluss-Logs oder Abonnenten-Logs zugreifen. Ein Benutzer ohne Administratorrechte kann diese Protokolle ansprechen, muss aber mit einer verknüpften Tabelle (Profile, Versand) beginnen.

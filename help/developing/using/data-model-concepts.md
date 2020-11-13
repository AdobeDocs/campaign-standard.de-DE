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
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
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

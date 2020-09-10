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
source-git-commit: 3895755aa2eeceb837f78f591bb6504d3eadec1f
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 84%

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
>Nur Funktionale [Administratoren](../../administration/using/users-management.md#functional-administrators)mit **[!UICONTROL Administratorrolle]** und Zugriff auf **alle** Abonnement können auf die Protokolle zum Senden, Melden, Trackinglogs, Ausschließen oder Ausschließen zugreifen. Ein Benutzer, der keine Administratoren ist, kann diese Protokolle zwar Zielgruppe, jedoch auf einer verknüpften Tabelle (Profil, Versand) beginnen.

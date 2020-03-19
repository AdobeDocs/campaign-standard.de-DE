---
title: Liste der Rollen
description: Hier finden Sie die Rollen, die Sie Ihren Benutzern zuweisen können.
page-status-flag: never-activated
uuid: 128aaf9b-9b7d-49f3-9e1f-72e79a29baa0
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: users-and-security
discoiquuid: ceaa3c94-9e1a-4271-b443-b00b4068929f
context-tags: role,overview;role,main
internal: n
snippet: y
translation-type: ht
source-git-commit: 88d0f67683c5209ccf25d1ceae1ab23b3ac14e06

---


# Liste der Rollen{#list-of-roles}

Adobe Campaign bietet standardmäßig eine Auswahl an Benutzerrollen zur Definition von Einzelberechtigungen für Benutzer und Benutzergruppen.

Gemeinsam mit Organisationseinheiten bieten Rollen Benutzern eine gefilterte Ansicht der Benutzeroberfläche und definieren ihren Zugriff auf die unterschiedlichen Funktionen.

Weitere Informationen dazu finden Sie in der Tabelle [Rollen und Berechtigungen](/help/administration/using/assets/acs_rights.pdf), in der die Funktionen beschrieben werden, die je nach den ausgewählten Berechtigungen auf der Benutzeroberfläche verfügbar sind.

![](assets/user_management_3.png)

Rollen können über das Menü **[!UICONTROL Administration > Benutzer &amp; Sicherheit > Rollen]** verwaltet werden.

Standardberechtigungen sind:

* **[!UICONTROL Administration]**: Berechtigt zur allgemeinen Administration.
* **[!UICONTROL Datamodel]**: Berechtigt zur Durchführung von Veröffentlichungen und zur Erstellung von benutzerdefinierten Ressourcen.
* **[!UICONTROL Export]**: Berechtigt zum Export von Daten.
* **[!UICONTROL Allgemeiner Import]**: Berechtigt zum allgemeinen Import von Daten. Dazu muss die Rolle **[!UICONTROL Allgemeiner Import]** mit der **[!UICONTROL Workflow]**-Rolle verknüpft werden.
* **[!UICONTROL Sendungen vorbereiten]**: Berechtigung zum Erstellen, Ändern, Vorbereiten und Löschen von Sendungen. Benutzer mit dieser Rolle können einen Versand vorbereiten, aber nicht durchführen.
* **[!UICONTROL Sendungen starten]**: Berechtigung zum Erstellen, Ändern, Vorbereiten, Senden und Löschen von Sendungen.
* **[!UICONTROL Workflow]**: Berechtigung zum Verwalten der Ausführung von Workflows (Start, Stopp, Pause usw.). Benutzer mit dieser Rolle können auch in einem Workflow keine Sendungen durchführen.

>[!IMPORTANT]
>
>Die Rollen **[!UICONTROL Zustellbarkeit]**, **[!UICONTROL Befehlsausführung]**, **[!UICONTROL Export]**, **[!UICONTROL Zugriff auf Daten]** und **[!UICONTROL Message Center Push]** sind nur für die interne Nutzung durch Adobe-Administratoren vorgesehen. Diese Rollen sollten Benutzern nicht gewährt werden.

**Verwandte Themen:**

* [Über die Zugriffsverwaltung](../../administration/using/about-access-management.md)
* [Gruppen und Benutzer verwalten](../../administration/using/managing-groups-and-users.md)

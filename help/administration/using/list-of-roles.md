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
translation-type: tm+mt
source-git-commit: 18db1b8cade7d88294ef2609dd4fad95c55fbd37

---


# Liste der Rollen{#list-of-roles}

Adobe Campaign bietet standardmäßig eine Auswahl an Benutzerrollen zur Definition von Einzelberechtigungen für Benutzer und Benutzergruppen.

Gemeinsam mit Organisationseinheiten bieten Rollen Benutzern eine gefilterte Ansicht der Benutzeroberfläche und definieren ihren Zugriff auf die unterschiedlichen Funktionen.

Weitere Informationen dazu finden Sie in der Tabelle [Rollen und Berechtigungen](/help/administration/using/assets/acs_rights.pdf), in der die Funktionen beschrieben werden, die je nach den ausgewählten Berechtigungen auf der Benutzeroberfläche verfügbar sind.

![](assets/user_management_3.png)

Rollen können über das **[!UICONTROL Administration > Users & Security > Roles]** Menü verwaltet werden.

Standardberechtigungen sind:

* **[!UICONTROL Administration]**: Allgemeine Verwaltungsrechte.
* **[!UICONTROL Datamodel]**: Berechtigt zur Durchführung von Veröffentlichungen und zur Erstellung von benutzerdefinierten Ressourcen.
* **[!UICONTROL Generic import]**: Recht zum Ausführen eines generischen Imports für Daten. For this to work, you need to link the **[!UICONTROL Generic import]** role to the **[!UICONTROL Workflow]** role.
* **[!UICONTROL Prepare deliveries]**: Recht zum Erstellen, Ändern, Vorbereiten und Löschen von Versänden. Benutzer mit dieser Rolle können einen Versand vorbereiten, aber nicht durchführen.
* **[!UICONTROL Start deliveries]**: Berechtigung zum Erstellen, Ändern, Vorbereiten, Senden und Löschen von Versänden.
* **[!UICONTROL Workflow]**: Berechtigung zum Verwalten der Ausführung von Workflows (Start, Stopp, Pause usw.). Benutzer mit dieser Rolle können auch in einem Workflow keine Sendungen durchführen.

**Verwandte Themen:**

* [Über die Zugriffsverwaltung](../../administration/using/about-access-management.md)
* [Gruppen und Benutzer verwalten](../../administration/using/managing-groups-and-users.md)

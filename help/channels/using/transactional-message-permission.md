---
title: Berechtigung für Transaktionsnachrichten
description: Erfahren Sie mehr über Berechtigungen in Verbindung mit Transaktionsereignissen.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
hide: true
hidefromtoc: true
feature: Transactional Messaging
role: User
level: Intermediate
source-git-commit: d7e0912dd7d19a1f5dd2172235f28a40e130cac1
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 1%

---

# Berechtigung für Transaktionsnachrichten {#transactional-message-permission}

In Adobe Campaign Standard können Benutzer ohne Administrator-Sicherheitsgruppe derzeit nicht auf Ereignisse zugreifen, Ereignisse erstellen oder veröffentlichen, was zu Problemen für Geschäftsbenutzer führt, die Ereignisse konfigurieren und veröffentlichen müssen, aber keine Administratorrechte haben.

Die Zugriffskontrolle auf Transaktionsnachrichten wurde folgendermaßen verbessert:

* Eine neue **[!UICONTROL Rolle]** aufgerufen **MC-Benutzer** wurde hinzugefügt, damit Benutzer, die keine Administratoren sind, Transaktionsereignisse verwalten können. Die **MC-Benutzer** -Rolle bietet diesen Benutzern die Möglichkeit, auf Transaktionsereignisse und -nachrichten zuzugreifen, sie zu erstellen, zu veröffentlichen und deren Veröffentlichung aufzuheben.

* Die untergeordneten Sendungen sind nun auf die **[!UICONTROL Organisationseinheit]** der Sicherheitsgruppe, zu der der Benutzer gehört, der die Nachrichtenvorlage erstellt, anstatt sich auf die **[!UICONTROL Organisationseinheit]** des **Message Center Agent (mcExec)** Sicherheitsgruppe.

* Die Standardeinstellung **Message Center-Ausführung (mcExec)** Kampagne, die die untergeordneten Sendungen von Transaktionsnachrichten erfasst, ist jetzt auf die Organisationseinheit eingestellt **Alle** Möglichkeit für alle Benutzer, Berichte über untergeordnete Sendungen anzuzeigen.

So weisen Sie die **MC-Benutzer** Rolle:

1. Erstellen Sie eine neue **[!UICONTROL Sicherheitsgruppe]** oder ein vorhandenes aktualisieren. [Weitere Informationen](../../administration/using/managing-groups-and-users.md).

1. Klicken **[!UICONTROL Element erstellen]** , um Ihrer Sicherheitsgruppe Rollen zuzuweisen.

   ![](assets/event_access_1.png)

1. MC-Benutzer auswählen **[!UICONTROL Rolle]** und klicken Sie auf **[!UICONTROL Bestätigen]**.

   >[!IMPORTANT]
   >
   > Gehen Sie beim Zuweisen der Benutzerrolle MC vorsichtig vor, da diese Benutzern die Möglichkeit gibt, die Veröffentlichung von Ereignissen aufzuheben.

   ![](assets/event_access_2.png)

1. Klicken Sie nach der Konfiguration auf **[!UICONTROL Speichern]**.

Benutzer, die damit verknüpft sind **[!UICONTROL Sicherheitsgruppe]** kann jetzt auf Transaktionsereignisse und -nachrichten zugreifen, sie erstellen und veröffentlichen.

In der folgenden Tabelle sind die Auswirkungen dieser Funktion auf die Zugriffskontrolle aufgeführt:

| Objekte | Vor dieser Änderung | Nach dieser Änderung |
|:-: | :--: | :-:|
| Message Center Execution (mcExec) campaign | **Message Center-Ausführung (mcExec)** Kampagne auf die Organisationseinheit der **Message Center Agent (mcExec)** Sicherheitsgruppe. | **Message Center-Ausführung (mcExec)** Kampagne auf die Organisationseinheit eingestellt **Alle** , damit alle untergeordneten Sendungen dieser Kampagne zugeordnet werden können.</br> Alle Benutzer können die Berichte über die untergeordneten Sendungen anzeigen, haben jedoch nur Lesezugriff auf den Versandinhalt. |
| Untergeordnete Sendungen | Untergeordnete Sendungen werden auf die **Organisationseinheit** des **Message Center Agent (mcExec)** Sicherheitsgruppe. | Die untergeordneten Sendungen werden auf die **Organisationseinheit** der Sicherheitsgruppe, zu der der Benutzer gehört, der die Nachrichtenvorlage erstellt. |
| Nachrichtenvorlage | Nachrichtenvorlagen werden auf die **Organisationseinheit** des **Message Center Agent (mcExec)** Sicherheitsgruppe. | Nachrichtenvorlagen werden auf die **Organisationseinheit** der Sicherheitsgruppe, zu der der Benutzer gehört, der die Nachrichtenvorlage erstellt. |
| Transaktionsereignisse | Nur Benutzer innerhalb der **Administrator** Sicherheitsgruppe kann Ereignisse erstellen und veröffentlichen. | Die **MC-Benutzer** -Rolle ermöglicht Benutzern das Erstellen und Veröffentlichen von Ereignissen. |
| Transaktionsnachrichtenvorlagen | Transaktionsnachrichten-Vorlagen sind auf die Organisationseinheit eingestellt **Alle**. | Transaktionsnachrichtenvorlage wird auf die **Organisationseinheit** der Sicherheitsgruppe, zu der der Benutzer gehört, der die Nachrichtenvorlage erstellt. |
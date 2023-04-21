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
exl-id: 995da330-6c86-444b-86b2-61d887f37db4
source-git-commit: aa0a6a38a1b53db1e0712d295995dd9ec91794a1
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 100%

---

# Berechtigung für Transaktionsnachrichten {#transactional-message-permission}

Derzeit können Benutzerinnen und Benutzer ohne die Sicherheitsgruppe „Administrator“ in Adobe Campaign Standard nicht auf Ereignisse zugreifen, sie erstellen oder veröffentlichen. Dies führt zu Problemen für Geschäftsanwenderinnen und -anwender, die Ereignisse konfigurieren und veröffentlichen müssen, aber nicht über Administratorrechte verfügen.

Die Zugriffskontrolle auf Transaktionsnachrichten wurde folgendermaßen verbessert:

* Eine neue **[!UICONTROL Rolle]** mit der Bezeichnung **MC USER** wurde hinzugefügt, damit Benutzerinnen und Benutzer, die keine Administratoren sind, Transaktionsereignisse verwalten können. Die Rolle **MC USER** bietet diesen Benutzerinnen und Benutzern die Möglichkeit, auf Transaktionsereignisse und -nachrichten zuzugreifen, sie zu erstellen, zu veröffentlichen und ihre Veröffentlichung aufzuheben.

* Untergeordnete Sendungen sind nun auf die **[!UICONTROL Organisationseinheit]** der Sicherheitsgruppe festgelegt, zu der die Benutzerin oder der Benutzer gehört, die oder der die Nachrichtenvorlage erstellt, anstatt auf die **[!UICONTROL Organisationseinheit]** der Sicherheitsgruppe **Message Center Agent (mcExec)** beschränkt zu sein.

* Die Standardkampagne von **Message Center Execution (mcExec)**, die die untergeordneten Sendungen von Transaktionsnachrichten erfasst, ist jetzt auf die Organisationseinheit **Alle** festgelegt, sodass alle Benutzerinnen und Benutzer Berichte von untergeordneten Sendungen anzeigen können.

So weisen Sie die Rolle **MC USER** zu:

1. Erstellen Sie eine neue **[!UICONTROL Sicherheitsgruppe]** oder aktualisieren Sie eine vorhandene. [Weitere Informationen](../../administration/using/managing-groups-and-users.md).

1. Klicken Sie auf **[!UICONTROL Element erstellen]**, um Ihrer Sicherheitsgruppe Rollen zuzuweisen.

   ![](assets/event_access_1.png)

1. Wählen Sie die **[!UICONTROL Rolle]** „MC USER“ aus und klicken Sie auf **[!UICONTROL Bestätigen]**.

   >[!IMPORTANT]
   >
   > Gehen Sie beim Zuweisen der Rolle „MC USER“ vorsichtig vor, da diese Rolle Benutzerinnen und Benutzer die Möglichkeit gibt, die Veröffentlichung von Ereignissen aufzuheben.

   ![](assets/event_access_2.png)

1. Klicken Sie nach der Konfiguration auf **[!UICONTROL Speichern]**.

Benutzerinnen und Benutzer, die mit dieser **[!UICONTROL Sicherheitsgruppe]** verknüpft sind, können jetzt auf Transaktionsereignisse und -nachrichten zugreifen, sie erstellen und veröffentlichen.

In der folgenden Tabelle sind die Auswirkungen dieser Funktion auf die Zugriffskontrolle aufgeführt:

| Objekte | Vor dieser Änderung | Nach dieser Änderung |
|:-: | :--: | :-:|
| Die Kampagne „Message Center Execution (mcExec)“ | Die Kampagne **Message Center Execution (mcExec)** ist auf die Organisationseinheit der Sicherheitsgruppe **Message Center Agent (mcExec)** festgelegt. | Die Kampagne **Message Center Execution (mcExec)** ist auf die Organisationseinheit **Alle** festgelegt, damit alle untergeordneten Sendungen dieser Kampagne zugeordnet werden können.</br> Alle Benutzerinnen und Benutzer können Berichte über untergeordneten Sendungen anzeigen, haben jedoch nur Lesezugriff auf den Versandinhalt. |
| Untergeordnete Sendungen | Untergeordnete Sendungen sind auf die **Organisationseinheit** der Sicherheitsgruppe **Message Center Agent (mcExec)** festgelegt. | Untergeordnete Sendungen werden auf die **Organisationseinheit** der Sicherheitsgruppe festgelegt, zu der die Benutzerin oder der Benutzer gehört, die oder der die Nachrichtenvorlage erstellt. |
| Nachrichtenvorlage | Nachrichtenvorlagen sind auf die **Organisationseinheit** der Sicherheitsgruppe **Message Center Agent (mcExec)** festgelegt. | Nachrichtenvorlagen werden auf die **Organisationseinheit** der Sicherheitsgruppe festgelegt, zu der die Benutzerin oder der Benutzer gehört, die oder der die Nachrichtenvorlage erstellt. |
| Transaktionsereignisse | Nur Benutzerinnen und Benutzer innerhalb der Sicherheitsgruppe **Administrator** können Ereignisse erstellen und veröffentlichen. | Die Rolle **MC USER** ermöglicht Benutzerinnen und Benutzern das Erstellen und Veröffentlichen von Ereignissen. |
| Vorlagen für Transaktionsnachrichten | Vorlagen für Transaktionsnachrichten sind auf die Organisationseinheit **Alle** festgelegt. | Die Vorlage für Transaktionsnachrichten wird auf die **Organisationseinheit** der Sicherheitsgruppe festgelegt, zu der die Benutzerin oder der Benutzer gehört, die oder der die Nachrichtenvorlage erstellt. |

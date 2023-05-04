---
title: Berechtigung für Transaktionsnachrichten
description: Erfahren Sie mehr über Berechtigungen in Verbindung mit Transaktionsereignissen.
audience: channels
content-type: reference
topic-tags: transactional-messaging
context-tags: null
feature: Transactional Messaging
role: User
level: Intermediate
exl-id: 995da330-6c86-444b-86b2-61d887f37db4
source-git-commit: 7247fe596494690ac0676196fbb72c6139aeb0c7
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 100%

---

# Verbesserungen bei Transaktionsereignissen {#transactional-event-improvements}

>[!AVAILABILITY]
>
>Diese Funktionen sind derzeit nur für eine Gruppe von Organisationen verfügbar (eingeschränkte Verfügbarkeit). Weitere Informationen erhalten Sie von Ihrer Adobe-Kontaktperson.

Derzeit können Benutzerinnen und Benutzer ohne die Sicherheitsgruppe „Administrator“ in Adobe Campaign Standard nicht auf Ereignisse zugreifen, sie erstellen oder veröffentlichen. Dies führt zu Problemen für Geschäftsanwenderinnen und -anwender, die Ereignisse konfigurieren und veröffentlichen müssen, aber nicht über Administratorrechte verfügen. Außerdem ist es nicht möglich, Transaktionsereignisse zu duplizieren.

Die Zugriffskontrolle für Transaktionsnachrichten wurde folgendermaßen verbessert:

* Eine neue **[!UICONTROL Rolle]** mit der Bezeichnung **MC USER** wurde hinzugefügt, damit Benutzerinnen und Benutzer, die keine Admins sind, Transaktionsereignisse verwalten können. Die Rolle **MC USER** bietet diesen Benutzerinnen und Benutzern die Möglichkeit, auf Transaktionsereignisse und -nachrichten zuzugreifen, sie zu erstellen, zu veröffentlichen und ihre Veröffentlichung aufzuheben.

* Ausführungssendungen (d. h. technische Nachrichten, die jedes Mal erstellt werden, wenn eine Transaktionsnachricht bearbeitet und erneut veröffentlicht wird, oder standardmäßig einmal im Monat) sind jetzt auf die **[!UICONTROL Organisationseinheit]** der Sicherheitsgruppe eingestellt, zu der die Person gehört, die das Ereignis erstellt hat, anstatt auf die **[!UICONTROL Organisationseinheit]** der Sicherheitsgruppe **Message Center Agent (mcExec)** beschränkt zu sein.

* **Administratorinnen und Administratoren** können jetzt veröffentlichte Transaktionsereignisse sowie Benutzende mit der Rolle **MC USER** duplizieren, sofern sie sich in derselben **Organisationseinheitshierarchie** befinden wie die Person, die das Ereignis erstellt hat.

## Zuweisen der Rolle „MC USER“ {#assign-role}

So weisen Sie die Rolle **MC USER** für Ihre Sicherheitsgruppe zu:

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

## Zuweisen der MC USER-Sicherheitsgruppe {#assign-group}

1. Wählen Sie in Admin Console die Registerkarte **Produkte** aus.

1. Wählen Sie **Adobe Campaign Standard** und dann Ihre Instanz aus.

1. Wählen Sie aus der Liste **Produktprofile** die Gruppe **MC USER** aus.

1. Klicken Sie auf **Benutzer hinzufügen** und geben Sie den Namen, die Benutzergruppe oder die E-Mail-Adresse des Profils ein, das Sie diesem Produktprofil hinzufügen möchten.

1. Klicken Sie nach der Hinzufügung auf **Speichern**.

Benutzerinnen und Benutzer, die zu dieser **[!UICONTROL Sicherheitsgruppe]** hinzugefügt worden sind, können jetzt auf Transaktionsereignisse und -nachrichten zugreifen, sie erstellen und veröffentlichen.

## Duplizieren von Transaktionsereignissen {#duplicate-transactional-events}

Eine Benutzerin bzw. ein Benutzer mit der **Administrator**-Sicherheitsgruppe<!--([Functional administrators](../../administration/using/users-management.md#functional-administrators)?)--> kann jetzt eine Ereigniskonfiguration duplizieren, wenn das Ereignis **veröffentlicht** worden ist.

Darüber hinaus können Benutzerinnen und Benutzer ohne Administratorrechte mit der **MC USER**-Rolle jetzt auf Ereigniskonfigurationen zugreifen, ihre Berechtigung zum Duplizieren wird jedoch durch die Variable **Organisationseinheit** bestimmt. Wenn die aktuelle Benutzerin bzw. der aktuelle Benutzer zur gleichen Organisationseinheitshierarchie gehört wie die Person, die das Ereignis erstellt hat, ist eine Duplizierung zulässig.

Wenn beispielsweise eine Person, der zur Organisationseinheit „Vertrieb Frankreich“ gehört, eine Ereigniskonfiguration erstellt:

* Eine andere Benutzerin bzw. ein anderer Benutzer in der Organisationseinheit „Vertrieb Paris“, kann dieses Ereignis duplizieren, da „Vertrieb Paris“ Teil der Organisationseinheit „Vertrieb Frankreich“ ist.

* Eine Benutzerin oder ein Benutzer in der Organisationseinheit „Vertrieb San Francisco“, kann dies jedoch nicht tun, da „Vertrieb San Francisco“ unter der Organisationseinheit „Vertrieb USA“ steht, die von der Organisationseinheit „Vertrieb Frankreich“ getrennt ist.

Um eine Ereigniskonfiguration zu duplizieren, gehen Sie wie folgt vor.

1. Klicken Sie auf das **Adobe**-Logo oben links im Bildschirm und anschließend auf **[!UICONTROL Marketing-Pläne]** > **[!UICONTROL Transaktionsnachrichten]** > **[!UICONTROL Ereigniskonfiguration]**.

1. Bewegen Sie den Mauszeiger über die gewünschte veröffentlichte Ereigniskonfiguration und wählen Sie die Schaltfläche **[!UICONTROL Element duplizieren]**.

   ![](assets/message-center_duplicate-button.png)

   >[!CAUTION]
   >
   >Eine nicht veröffentlichte Ereigniskonfiguration kann nicht dupliziert werden. [Weitere Informationen](publishing-transactional-event.md)

1. Das duplizierte Ereignis wird automatisch angezeigt. Es enthält dieselbe Konfiguration wie das ursprüngliche Ereignis, verfügt jedoch über den Status **[!UICONTROL Entwurf]**.

   ![](assets/message-center_duplicated-draft-event.png)

1. Die entsprechende Transaktionsnachricht wird automatisch erstellt. Um darauf zuzugreifen, navigieren Sie zu **[!UICONTROL Transaktionsnachrichten]** > **[!UICONTROL Transaktionsnachrichten]**.

   ![](assets/message-center_duplicated-message.png)

1. Öffnen Sie die neu duplizierte Nachricht. Sie enthält dasselbe Design, das Sie für die ursprüngliche Nachricht definiert haben, hat jedoch den Status **[!UICONTROL Entwurf]**, auch wenn die ursprüngliche Transaktionsnachricht veröffentlicht wurde.

   ![](assets/message-center_duplicated-draft-message.png)

1. Sie können diese Nachricht jetzt bearbeiten und personalisieren. Siehe [Transaktionsnachrichten bearbeiten](../../channels/using/editing-transactional-message.md).

## Auswirkungen {#impacts}

Die nachstehende Tabelle zeigt die Auswirkungen dieser Verbesserungen:

| Objekte | Vor dieser Änderung | Nach dieser Änderung |
|:-: | :--: | :-:|
| Transaktionsereignisse | Nur Benutzerinnen und Benutzer innerhalb der Sicherheitsgruppe **Administrator** können Ereignisse erstellen und veröffentlichen. | Die Rolle **MC USER** ermöglicht Benutzerinnen und Benutzern das Erstellen und Veröffentlichen von Ereignissen. |
| Transaktionsnachrichten | Transaktionsnachrichten sind auf die **Organisationseinheit** der Sicherheitsgruppe **Message Center Agent (mcExec)** eingestellt. | Transaktionsnachrichten sind auf die **Organisationseinheit** der Sicherheitsgruppe eingestellt, zu der die Person gehört, die das Transaktionsereignis bzw. die Transaktionsnachricht erstellt hat. |
| Ausführungssendungen | Ausführungssendungen sind auf die **Organisationseinheit** der Sicherheitsgruppe **Message Center Agent (mcExec)** eingestellt. | Ausführungssendungen werden auf die **Organisationseinheit** der Sicherheitsgruppe eingestellt, zu der die Person gehört, die das Transaktionsereignis/die Transaktionsnachricht erstellt. |
| Veröffentlichte Transaktionsereignisse | Eine Duplizierung ist für niemand möglich. | <ul><li>Benutzerinnen und Benutzer mit der Sicherheitsgruppe **Administrator** können veröffentlichte Ereignisse duplizieren.</li> <li>Benutzerinnen und Benutzer mit der Rolle **MC USER** können veröffentlichte Ereignisse duplizieren, sofern sie sich in derselben **Organisationseinheitshierarchie** befinden wie die Person, die das Ereignis erstellt hat.</li></ul> |


<!--Transactional Message Templates| Transactional Message templates are set to the Organizational unit **All**. | Transaction Message Template will be set to the **Organizational unit** of the security group to which the user creating the message template belongs.-->
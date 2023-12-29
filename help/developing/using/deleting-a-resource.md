---
title: Ressourcen löschen
description: Hier erfahren Sie, wie Sie eine Ressource löschen können.
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
feature: Data Model
role: Developer
level: Experienced
exl-id: 4ddfdbcc-a154-4c10-a97e-73ad888d1f1f
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 100%

---

# Ressourcen löschen{#deleting-a-resource}

Eine Ressource muss den **[!UICONTROL Entwurf]**-Status aufweisen, um gelöscht werden zu können. Die Ressource befindet sich im Status **[!UICONTROL Entwurf]**, wenn:

* soeben erstellt und noch nicht veröffentlicht wurde.
* sie bereits veröffentlicht aber anschließend zurückgesetzt wurde.

>[!IMPORTANT]
>
>Das Zurücksetzen und Löschen einer benutzerdefinierten Ressource sind heikle Verfahren, die sich auf andere Ressourcen auswirken können. Diese Aktionen dürfen nur von einem erfahrenen Benutzer durchgeführt werden.

Um eine veröffentlichte Ressource zurückzusetzen und zu löschen, gehen Sie folgendermaßen vor:

1. Wählen Sie die zurückzusetzende Ressource aus.
1. Verwenden Sie die Schaltfläche **[!UICONTROL Zurücksetzen]** in der Aktionsleiste.

   ![](assets/schema_extension_uc26.png)

1. Bestätigen Sie die Aktion mit der Schaltfläche **[!UICONTROL OK]**.

   >[!IMPORTANT]
   >
   >Diese Aktion kann nicht rückgängig gemacht werden: Die Datenbanktabelle der Ressource oder die Spalten und deren Daten werden permanent gelöscht, wenn die Änderung veröffentlicht wird. Dadurch können auch die Verknüpfungen mit anderen benutzerdefinierten Ressourcen beeinträchtigt werden. Nur die Ressource-Definition wird weiterhin verfügbar sein.

   ![](assets/schema_extension_uc27.png)

   >[!NOTE]
   >
   >Wenn Sie eine Erweiterung der nativen Ressource **Profile (profile)** zurücksetzen, müssen Sie auch etwaige **Testprofil (seedMember)**-Erweiterungen zurücksetzen, die Sie definiert haben. Weiterführende Informationen zur Erweiterung der Profilressource finden Sie in [diesem Abschnitt](../../developing/using/extending-the-profile-resource-with-a-new-field.md).

1. Veröffentlichen Sie die Ressource. Eine detaillierte Anleitung finden Sie im Abschnitt [Benutzerdefinierte Ressource veröffentlichen](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).

   Die Ressource ist nun im Modus **Entwurf** und weist den Aktivierungsstatus **[!UICONTROL Deaktiviert]** auf.

1. Markieren Sie im Modus **[!UICONTROL Liste]** die zu löschende Ressource und wählen Sie dann das Symbol ![](assets/delete_darkgrey-24px.png)**[!UICONTROL Element löschen]** aus.

   ![](assets/schema_extension_uc28.png)

Ihre Ressource wird aus dem Datenmodell gelöscht.

>[!NOTE]
>
>Wenn ein Feld einer für ein Ereignis verwendeten benutzerdefinierten Ressource geändert oder gelöscht wird, wird die Veröffentlichung des zugehörigen Ereignisses automatisch aufgehoben. Siehe [Veröffentlichung von Transaktionsereignissen aufheben](../../channels/using/publishing-transactional-event.md#unpublishing-an-event).

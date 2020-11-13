---
title: Ressourcen löschen
description: 'Hier erfahren Sie, wie Sie eine Ressource löschen können. '
page-status-flag: never-activated
uuid: 5de27589-6fa5-412c-8e5a-a4976de05715
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: adding-or-extending-a-resource
discoiquuid: 0130733d-4e3f-40cd-b959-56381f2c8f44
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '249'
ht-degree: 100%

---


# Ressourcen löschen{#deleting-a-resource}

Eine Ressource muss den **[!UICONTROL Entwurf]**-Status aufweisen, um gelöscht werden zu können. Die Ressource befindet sich im Status **[!UICONTROL Entwurf]**, wenn:

* soeben erstellt und noch nicht publiziert wurde.
* sie bereits publiziert aber anschließend zurückgesetzt wurde.

>[!IMPORTANT]
>
>Das Zurücksetzen und Löschen einer benutzerdefinierten Ressource sind heikle Verfahren, die sich auf andere Ressourcen auswirken können. Diese Vorgänge dürfen nur von einem erfahrenen Benutzer durchgeführt werden.

Um eine publizierte Ressource zurückzusetzen und zu löschen, gehen Sie folgendermaßen vor:

1. Wählen Sie die zurückzusetzende Ressource aus.
1. Verwenden Sie die Schaltfläche **[!UICONTROL Zurücksetzen]** in der Symbolleiste.

   ![](assets/schema_extension_uc26.png)

1. Bestätigen Sie die Aktion mit der Schaltfläche **[!UICONTROL OK]**.

   >[!IMPORTANT]
   >
   >Dieser Vorgang kann nicht rückgängig gemacht werden: Die Datenbanktabelle der Ressource oder die Spalten und deren Daten werden permanent gelöscht, wenn die Änderung publiziert wird. Dadurch können auch die Verknüpfungen mit anderen benutzerdefinierten Ressourcen beeinträchtigt werden. Nur die Ressource-Definition wird weiterhin verfügbar sein.

   ![](assets/schema_extension_uc27.png)

   >[!NOTE]
   >
   >Wenn Sie eine Erweiterung der nativen Ressource **Profile (profile)** zurücksetzen, müssen Sie auch etwaige **Testprofil (seedMember)**-Erweiterungen zurücksetzen, die Sie definiert haben. Weiterführende Informationen zur Erweiterung der Profilressource finden Sie in [diesem Abschnitt](../../developing/using/extending-the-profile-resource-with-a-new-field.md).

1. Publizieren Sie die Ressource. Eine detaillierte Anleitung finden Sie im Abschnitt [Benutzerdefinierte Ressource publizieren](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).

   Die Ressource ist nun im Modus **Entwurf** und weist den Aktivierungsstatus **[!UICONTROL Deaktiviert]** auf.

1. Markieren Sie im Modus **[!UICONTROL Liste]** die zu löschende Ressource und wählen Sie dann das Symbol ![](assets/delete_darkgrey-24px.png)**[!UICONTROL Element löschen]** aus.

   ![](assets/schema_extension_uc28.png)

Ihre Ressource wird aus dem Datenmodell gelöscht.

>[!NOTE]
>
>Wenn ein Feld einer für ein Ereignis verwendeten benutzerdefinierten Ressource geändert oder gelöscht wird, wird das zugehörige Ereignis automatisch depubliziert. Siehe [Transaktionsnachrichten konfigurieren](../../administration/using/configuring-transactional-messaging.md).


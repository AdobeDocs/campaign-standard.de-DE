---
title: Ressourcen löschen
seo-title: Ressourcen löschen
description: Ressourcen löschen
seo-description: 'Hier erfahren Sie, wie Sie eine Ressource löschen können. '
page-status-flag: nie aktiviert
uuid: 5 de 27589-6 fa 5-412 c -8 e 5 a-a 4976 de 05715
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird entwickelt
content-type: Referenz
topic-tags: adding-or-extending-a-resource
discoiquuid: 0130733 d -4 e 3 f -40 cd-b 959-56381 f 2 c 8 f 44
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a12df43de55dedf388a397fbf4670d99e3ea7f3d

---


# Ressourcen löschen{#deleting-a-resource}

Eine Ressource muss den **[!UICONTROL Entwurf-Status aufweisen, um gelöscht werden zu können]**. Dies ist der Fall, wenn sie ****

* soeben erstellt und noch nicht publiziert wurde.
* sie bereits publiziert aber anschließend zurückgesetzt wurde.

>[!CAUTION]
>
>Das Zurücksetzen und Löschen einer benutzerdefinierten Ressource sind heikle Verfahren, die sich auf andere Ressourcen auswirken können. Diese Vorgänge dürfen nur von einem erfahrenen Benutzer durchgeführt werden.

Um eine publizierte Ressource zurückzusetzen und zu löschen, gehen Sie folgendermaßen vor:

1. Wählen Sie die zurückzusetzende Ressource aus.
1. Verwenden Sie die Schaltfläche **[!UICONTROL Zurücksetzen]der Symbolleiste.**

   ![](assets/schema_extension_uc26.png)

1. Bestätigen Sie die Aktion mit der Schaltfläche **[!UICONTROL OK]**.

   >[!CAUTION]
   >
   >Dieser Vorgang kann nicht rückgängig gemacht werden: Die Datenbanktabelle der Ressource oder die Spalten und deren Daten werden permanent gelöscht, wenn die Änderung publiziert wird. Dadurch können auch die Verknüpfungen mit anderen benutzerdefinierten Ressourcen beeinträchtigt werden. Nur die Ressource-Definition wird weiterhin verfügbar sein.

   ![](assets/schema_extension_uc27.png)

   >[!NOTE]
   >
   >Wenn Sie eine Erweiterung der nativen Ressource **Profile (profile)** zurücksetzen, müssen Sie auch etwaige **Testprofil (seedMember)**-Erweiterungen zurücksetzen, die Sie definiert haben. Weiterführende Informationen zur Erweiterung der Profilressource finden Sie in [diesem Abschnitt](../../developing/using/extending-the-profile-resource-with-a-new-field.md).

1. Publizieren Sie die Ressource. Eine detaillierte Anleitung finden Sie im Abschnitt [Benutzerdefinierte Ressource publizieren](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).

   Die Ressource weist nun den Publikationsstatus **Entwurf** und den Aktivierungsstatus **[!UICONTROL Deaktiviert auf]**.

1. Markieren Sie im Modus **[!UICONTROL Liste]** die zu löschende Ressource und wählen Sie dann das Symbol ![](assets/delete_darkgrey-24px.png)Element löschen **aus.**

   ![](assets/schema_extension_uc28.png)

Ihre Ressource wird aus dem Datenmodell gelöscht.

>[!NOTE]
>
>Wenn ein Feld einer für ein Ereignis verwendeten benutzerdefinierten Ressource geändert oder gelöscht wird, wird das zugehörige Ereignis automatisch depubliziert. Siehe [Transaktionsnachrichten konfigurieren](../../administration/using/configuring-transactional-messaging.md).


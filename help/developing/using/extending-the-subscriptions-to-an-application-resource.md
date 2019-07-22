---
title: App-Abonnements-Ressource erweitern
seo-title: App-Abonnements-Ressource erweitern
description: App-Abonnements-Ressource erweitern
seo-description: null
page-status-flag: nie aktiviert
uuid: 8879 b 427-b 31 b -3311-bf 54-258 a 91 b 1 fb 78
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird entwickelt
content-type: Referenz
topic-tags: Anwendungsfälle—expanding-resources
discoiquuid: 59 faa 74 e -86 fc -42 d 3-90 da-f 48580 b 5 ec 13
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 20b4d5dfb297cac4cd69fe6f945b4399abd7f06a

---


# App-Abonnements-Ressource erweitern{#extending-the-subscriptions-to-an-application-resource}

In Adobe Campaign sind Attribute zu mobilen Profilen, die von Mobilgeräten gesendet werden, in der Ressource **[!UICONTROL App-Abonnements (appSubscriptionRcp)]** gespeichert. Dort können die Daten definiert werden, die über die Abonnenten Ihrer Apps gesammelt werden sollen. Weiterführende Informationen zu benutzerdefinierten Ressourcen finden Sie auf dieser [Seite](../../developing/using/key-steps-to-add-a-resource.md).

Diese Ressource kann erweitert werden, um die Daten festzulegen, die vom Mobilgerät an Adobe Campaign gesendet und gesammelt werden sollen.

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]**, then **[!UICONTROL Custom resources]**.
1. Wählen Sie **[!UICONTROL Erstellen]** und danach die Option **Existierende Ressource erweitern]aus.[!UICONTROL **
1. Select the **[!UICONTROL Subscriptions to an application (appSubscriptionRcp)]** resource and click **[!UICONTROL Create]**.

   ![](assets/in_app_personal_data_4.png)

1. Definieren Sie in der Kategorie **[!UICONTROL Felder]** im Tab **[!UICONTROL Datenstruktur]die Kundendaten, die Sie aus Ihrer Mobile App abrufen möchten, indem Sie die Schaltfläche** Feld hinzufügen] verwenden.**[!UICONTROL **

   >[!NOTE]
   >
   >Falls Sie mehrere mobile Apps verwalten, müssen alle Felder aufgelistet werden, die von allen Ihren Apps verwendet werden. Der iOS- oder Android-Aufruf zum Erfassen von personenbezogenen Daten (PII) definiert die pro Anwendung abzurufenden Felder.

   ![](assets/in_app_personal_data.png)

1. Geben Sie für Ihr neues Feld einen **[!UICONTROL Titel]** und eine **Kennung]ein.[!UICONTROL ** Select your field's **[!UICONTROL Type]**.

   ![](assets/schema_extension_uc9.png)

1. Konfigurieren Sie in der Kategorie **[!UICONTROL Profilrelation]den Abstimmschlüssel, der zur Verknüpfung von Profilen der Adobe Campaign-Datenbank mit Abonnenten Ihrer App dient (beispielsweise die E-Mail-Adresse).**

   Beachten Sie, dass Sie für Ihre In-App-Nachrichten in allen Mobile Apps nur einen einzigen Abstimmschlüssel definieren können.

   ![](assets/in_app_personal_data_3.png)

1. **[!UICONTROL Speichern]** und publizieren Sie dann Ihre benutzerdefinierte Ressource. Weiterführende Informationen zur Publikation benutzerdefinierter Ressourcen finden Sie auf dieser [Seite](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).


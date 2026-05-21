---
title: App-Abonnements-Ressource erweitern
description: Erfahren Sie, wie Sie das Abonnement auf eine Anwendungsressource erweitern.
audience: developing
content-type: reference
topic-tags: use-cases--extending-resources
feature: Data Model
role: Developer
level: Experienced
exl-id: ac9c556d-c0f6-4b33-8855-1f5f669c148f
TQID: https://experienceleague.adobe.com/LtTykn3J6LjivrUr-xkhsZMgaVg-uQ2PHqA6wcJipo8
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 265
ht-degree: 100%

---

# App-Abonnements-Ressource erweitern{#extending-the-subscriptions-to-an-application-resource}

In Adobe Campaign sind Attribute zu mobilen Profilen, die von Mobilgeräten gesendet werden, in der Ressource **[!UICONTROL App-Abonnements (appSubscriptionRcp)]** gespeichert. Dort können die Daten definiert werden, die über die Abonnenten Ihrer Apps gesammelt werden sollen. Weiterführende Informationen zu benutzerdefinierten Ressourcen finden Sie auf dieser [Seite](../../developing/using/key-steps-to-add-a-resource.md).

Diese Ressource kann erweitert werden, um die Daten festzulegen, die vom Mobilgerät an Adobe Campaign gesendet und gesammelt werden sollen.

1. Öffnen Sie im erweiterten Menü über das Adobe Campaign-Logo **[!UICONTROL Administration]** > **[!UICONTROL Entwicklung]** > **[!UICONTROL Benutzerdefinierte Ressourcen]**.
1. Wählen Sie **[!UICONTROL Erstellen]** und danach die Option **[!UICONTROL Existierende Ressource erweitern]** aus.
1. Wählen Sie die Ressource **[!UICONTROL App-Abonnements (appSubscriptionRcp)]** und danach **[!UICONTROL Erstellen]** aus.

   ![](assets/in_app_personal_data_4.png)

1. Definieren Sie in der Kategorie **[!UICONTROL Felder]** im Tab **[!UICONTROL Datenstruktur]** die Kundendaten, die Sie aus Ihrer Mobile App abrufen möchten, indem Sie die Schaltfläche **[!UICONTROL Feld hinzufügen]** verwenden.

   >[!NOTE]
   >
   >Falls Sie mehrere mobile Apps verwalten, müssen alle Felder aufgelistet werden, die von allen Ihren Apps verwendet werden. Der iOS- oder Android-Aufruf zum Erfassen von personenbezogenen Daten (PII) definiert die pro Anwendung abzurufenden Felder.

   ![](assets/in_app_personal_data.png)

1. Geben Sie für Ihr neues Feld einen **[!UICONTROL Titel]** und eine **[!UICONTROL Kennung]** ein. Wählen Sie den **[!UICONTROL Typ]** Ihres Feldes aus.

   ![](assets/schema_extension_uc9.png)

1. Konfigurieren Sie in der Kategorie **[!UICONTROL Profilrelation]** den Abstimmschlüssel, der zur Verknüpfung von Profilen der Adobe Campaign-Datenbank mit Abonnenten Ihrer App dient (beispielsweise die E-Mail-Adresse).

   Beachten Sie, dass Sie für Ihre In-App-Nachrichten in allen Mobile Apps nur einen einzigen Abstimmschlüssel definieren können.

   ![](assets/in_app_personal_data_3.png)

1. **[!UICONTROL Speichern]** und veröffentlichen Sie dann Ihre benutzerdefinierte Ressource. Weiterführende Informationen zur Veröffentlichung benutzerdefinierter Ressourcen finden Sie auf dieser [Seite](../../developing/using/updating-the-database-structure.md#publishing-a-custom-resource).

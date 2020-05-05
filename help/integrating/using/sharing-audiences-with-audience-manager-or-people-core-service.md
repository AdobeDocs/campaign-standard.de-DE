---
title: Audiences mit Audience Manager oder People Core Service freigeben
description: Hier erfahren Sie, wie Sie Ihre Audience in die unterschiedlichen Adobe Experience Cloud-Lösungen importieren oder daraus exportieren können.
page-status-flag: never-activated
uuid: a3701e72-5846-4241-afee-d713b499a27a
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
discoiquuid: 77af0772-52b5-46bc-a964-675b45965524
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 68e825bc3b6b7f94f61875e7da2bc8f63f06d9cb

---


# Audiences mit Audience Manager oder People Core Service freigeben{#sharing-audiences-with-audience-manager-or-people-core-service}

## Audience importieren {#importing-an-audience}

Durch die Integration von People Core Service kann eine Audience direkt in Adobe Campaign über einen technischen Workflow importiert werden, um Ihre Datenbank anzureichern. Weiterführende Informationen zur Zielgruppenfreigabe in People Core Service finden Sie in dieser [Dokumentation](https://marketing.adobe.com/resources/help/de_DE/mcloud/t_publish_audience_segment.html).

Der Import von /Segmenten aus People Core Service in Adobe Campaign erfolgt über das Menü **[!UICONTROL Audiences]** Audiences. Nutzer müssen sich einfach nur per IMS verbinden (die Authentifizierung erfolgt über die Adobe ID).

1. Go to the **[!UICONTROL Audiences]** menu.
1. In the action bar, select **[!UICONTROL Create]** to be taken to the screen to create an audience.
1. Vergeben Sie einen Titel für die neue Audience.
1. Set the audience **[!UICONTROL Type]** to **[!UICONTROL Experience Cloud]** to indicate that the audience being created is an audience that was imported from People core service.
1. Wählen Sie im **[!UICONTROL Name of the shared audience]** Feld die zu importierende Audience aus. Nur Segmente können importiert werden. Granulare Daten wie Schlüssel/Wert-Paare, Merkmale und Regeln werden nicht unterstützt.

   ![](assets/aam_import_audience.png)

1. Wählen Sie die entsprechende Option **[!UICONTROL Shared Data Source]**.

   If the selected data source is configured to use an encryption algorithm, an additional option offers you the possibility to **[!UICONTROL Force reconciliation with a profile]**. Check this option if the **[!UICONTROL Channel]** field of the data source is set to Email or Mobile (SMS) and if you want to leverage profile data.

   If you do not select the **[!UICONTROL Force reconciliation with a profile]** and if **[!UICONTROL Channel]** is set in AMC Data source to Email or Mobile (SMS) then all the encrypted declared IDs are decrypted. Eine Audience vom Typ **Datei** mit einer Liste aller E-Mail-Adressen/Mobiltelefonnummern wird erstellt/aktualisiert. Auf diese Weise geht keine E-Mail-Adresse/Mobiltelefonnummer beim Import einer freigegebenen Audience durch diese Integration verloren, selbst wenn dieses Profil in Campaign nicht existiert. Beachten Sie bitte, dass dieser Typ von Audiences nicht direkt verwendet werden kann, da er manuell mit Workflows abgestimmt werden muss.

1. Validieren Sie die Erstellung.

   Die Audience wird dann mithilfe eines technischen Workflows importiert. Sie enthält Datensätze, deren Kennung (&#39;Visitor ID&#39; oder &#39;Declared ID&#39;) mit der Profildimension abgestimmt werden konnte. Von Adobe Campaign nicht erkannte Kennungen, die People-Core-Service-Segmenten entstammen, werden nicht importiert.

Ihre Audience wird jetzt in Ihre Adobe Campaign-Datenbank importiert. Wenn Segmente direkt von People Core Service oder Audience Manager importiert werden, dauert die Synchronisation des Imports 24 bis 36 Stunden. Danach ist die neue Audience in Adobe Campaign auffindbar und verwendbar.

>[!NOTE]
>
>Beim Import von Audiences von Adobe Analytics nach Adobe Campaign müssen diese Audiences zuerst in People Core Service oder Audience Manager freigegeben werden. Dieser Prozess dauert 12 bis 24 Stunden, die zu den 24 bis 36 Stunden für die Synchronisation mit Campaign hinzugezählt werden müssen. In diesem speziellen Fall kann die Zielgruppenfreigabe bis zu 60 Stunden dauern. Weitere Informationen zur Adobe Analytics-Zielgruppenfreigabe in People Core Service und Audience Manager finden Sie in dieser [Dokumentation](https://marketing.adobe.com/resources/help/de_DE/mcloud/t_publish_audience_segment.html).

## Audiences exportieren {#exporting-an-audience}

An audience can be exported from Adobe Campaign to Audience Manager or People core service using a workflow and the **[!UICONTROL Save audience]** activity.

Der Export einer Audience von Adobe Campaign in People Core Service kann in einem neuen Workflow und nur von Benutzern durchgeführt werden, die per IMS verbunden sind (die Authentifizierung erfolgt über die Adobe ID).

1. Erstellen Sie ausgehend von einem Programm, einer Kampagne oder der Marketingaktivitätenliste einen neuen Workflow.
1. Verwenden Sie die diversen zur Verfügung stehenden Aktivitäten, um eine Gruppe von Profilen auszuwählen.
1. After the targeting, drag and drop a **[!UICONTROL Save audience]** activity into the workflow, then open it.
1. Auswählen **[!UICONTROL Share in Adobe Experience Cloud]**.

   ![](assets/aam_save_audience_activity.png)

1. Geben Sie die Audience mithilfe des **[!UICONTROL Shared audience]** Felds an. Wählen Sie dann im sich öffnenden Fenster entweder eine existierende Zielgruppe aus bzw. erstellen Sie eine neue:

   * Wenn Sie eine existierende Zielgruppe verwenden, wird sie mit den neuen Datensätzen ergänzt.
   * To export your profile list into a new audience, complete the **[!UICONTROL Segment name]** field then click **[!UICONTROL Create]** before selecting the newly created audience.
   ![](assets/aam_save_audience_segment_picker.png)

   Um abgestimmt und ausgetauscht werden zu können, müssen die Datensätze eine Adobe-Experience-Cloud-Kennung (&#39;Visitor ID&#39; oder &#39;Declared ID&#39;) aufweisen. Nicht abgestimmte Datensätze werden beim Import und Export der Zielgruppen ignoriert.

1. Schließen Sie den Vorgang ab, indem Sie die Validierungsschaltfläche oben rechts im Fenster verwenden.
1. Wählen Sie die entsprechende Option **[!UICONTROL Shared Data Source]**.
1. If you like, check the **[!UICONTROL Generate an outbound transition]** box to use the profiles that were exported. Es werden nur die Profile exportiert, die abgestimmt werden konnten.
1. Validieren Sie die Konfiguration der Aktivität und speichern Sie Ihren Workflow.
1. Starten Sie Ihren Workflow, um Ihre Audience zu exportieren. Die Synchronisation von Adobe Campaign und People Core Service kann mehrere Stunden in Anspruch nehmen.

Die Synchronisation von Adobe Campaign und People Core Service dauert 24 bis 36 Stunden. Danach ist Ihre neue Audience in People Core Service auffindbar und kann in anderen Adobe Experience Cloud-Lösungen verwendet werden. Weiterführende Informationen zur Verwendung einer in Adobe Campaign freigegebenen Audience in Adobe People Core Service finden Sie in dieser [Dokumentation](https://marketing.adobe.com/resources/help/de_DE/mcloud/t_audience_create.html).

**Verwandte Themen:**

* [Workflows](../../automating/using/get-started-workflows.md)
* [Audiences](../../audiences/using/about-audiences.md)


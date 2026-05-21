---
title: Campaign-Formular in Adobe Experience Manager erstellen
description: Durch die Integration von Adobe Experience Manager können Sie Formulare direkt in AEM einrichten, um Profile zu erstellen und zu aktualisieren oder Abonnements zu verwalten.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
feature: Triggers
old-role: Data Architect
role: Developer
level: Intermediate
exl-id: 61683639-3f71-4652-a138-acfc0e91e868
TQID: https://experienceleague.adobe.com/5wklRtwZ6Wubvyo-yu2ogEHufoqYBh6cvaJEoBC-Lkk
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 100%

---

# Campaign-Formular in Adobe Experience Manager erstellen {#creating-a-campaign-form-in-experience-manager}

Sie können &quot;Formular&quot;-Seiten auf Ihren AEM-Websites erstellen und die Felder dieses Formulars Feldern der Adobe Campaign-Datenbank zuordnen. Damit können Sie Profile erstellen und aktualisieren sowie Dienstanmeldungen verwalten.

Gehen Sie zur Erstellung eines Adobe Campaign-Formulars auf Ihrer AEM-Seite wie folgt vor:

1. Erstellen Sie auf Ihrer AEM-Website ausgehend von der Vorlage **Adobe Campaign-Profil** eine neue Seite.

   ![](assets/aem_content_forms.png)

1. Wählen Sie in den Eigenschaften der Seite den Ihrer Adobe Campaign-Instanz entsprechenden **[!UICONTROL Cloud Service]** aus.

   ![](assets/aem_content_forms_2.png)

1. Wählen Sie ausgehend von der Komponente **[!UICONTROL Formular-Start]** den Formulartyp aus:

   * **Adobe Campaign: Profil speichern**
   * **Adobe Campaign: Dienstanmeldung**
   * **Adobe Campaign: Dienstabmeldung**

1. Bearbeiten Sie den Formularinhalt, indem Sie verschiedene Felder und Komponenten hinzufügen, die Sie den Feldern der Adobe Campaign-Datenbank zuordnen können.
1. Testen und veröffentlichen Sie das Formular, damit sich über Ihre AEM-Seite darauf zugreifen lässt.

Weitere Informationen finden Sie im [entsprechenden Handbuch](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/aem-adobe-campaign/adobe-campaign-forms.html?lang=de).

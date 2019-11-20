---
title: 'Campaign-Formular in Adobe Experience Manager erstellen '
description: Durch die Integration von Adobe Experience Manager können Sie Formulare direkt in AEM einrichten, um Profile zu erstellen und zu aktualisieren oder Abonnements zu verwalten.
page-status-flag: never-activated
uuid: 43057f81-d47d-4b96-b150-217c289cd608
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 4a8b5807-87dd-4db4-bd67-890f0adae932
internal: n
snippet: y
translation-type: ht
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Campaign-Formular in Adobe Experience Manager erstellen {#creating-a-campaign-form-in-experience-manager}

Sie können "Formular"-Seiten auf Ihren AEM-Websites erstellen und die Felder dieses Formulars Feldern der Adobe-Campaign-Datenbank zuordnen. Damit können Sie Profile erstellen und aktualisieren sowie Dienstanmeldungen verwalten.

Gehen Sie zur Erstellung eines Adobe Campaign-Formulars auf Ihrer AEM-Seite wie folgt vor:

1. Erstellen Sie auf Ihrer AEM-Website ausgehend von der Vorlage **Adobe Campaign-Profil** eine neue Seite.

   ![](assets/aem_content_forms.png)

1. Wählen Sie in den Eigenschaften der Seite den Ihrer Adobe-Campaign-Instanz entsprechenden **[!UICONTROL Cloud Service]** aus.

   ![](assets/aem_content_forms_2.png)

1. Wählen Sie ausgehend von der Komponente **[!UICONTROL Formular-Start]** den Formulartyp aus:

   * **Adobe Campaign: Profil speichern**
   * **Adobe Campaign: Dienstanmeldung**
   * **Adobe Campaign: Dienstabmeldung**

1. Bearbeiten Sie den Formularinhalt, indem Sie verschiedene Felder und Komponenten hinzufügen, die Sie den Feldern der Adobe-Campaign-Datenbank zuordnen können.
1. Testen und publizieren Sie das Formular, damit sich über Ihre AEM-Seite darauf zugreifen lässt.

Lesen Sie für weiterführende Informationen das [entsprechende Handbuch](https://docs.adobe.com/docs/en/aem/6-2/author/personalization/adobe-campaign/adobe-campaign-forms.html).

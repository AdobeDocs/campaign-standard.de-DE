---
title: Profil-Ressource um ein neues Feld erweitern
description: Hier erfahren Sie, wie die Profil-Ressource erweitert wird.
page-status-flag: never-activated
uuid: 9b99e95c-93ff-4187-90f7-db0baf5369ad
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: use-cases--extending-resources
discoiquuid: 1e0f8945-fc3c-46a9-a8e5-b181a1f5ffcb
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 07d68b5bf8d800ebd95919f491e98f1b7a015705

---


# Profil-Ressource um ein neues Feld erweitern{#extending-the-profile-resource-with-a-new-field}

## Über Profilerweiterungen {#about-extending-profiles}

Das folgende Anwendungsbeispiel erläutert die Erweiterung der Profil- und der Testprofil-Ressourcen um ein zusätzliches Feld.

In unserem Beispiel wird gezeigt, wie die Profile unter Verwendung einer Landingpage mit dem neuen Feld aktualisiert werden und dann an Profile ein Newsletter gesendet wird, der genau ihren Interessen entspricht.

Gehen Sie dazu wie folgt vor:

* [Schritt 1: Profil-Ressource erweitern](#step-1--extend-the-profile-resource)
* [Schritt 2: Testprofil erweitern](#step-2--extend-the-test-profile)
* [Schritt 3: Benutzerdefinierte Ressource publizieren](#step-3--publish-your-custom-resource)
* [Schritt 4: Profile mit einem Workflow aktualisieren und auswählen](#step-4--update-and-target-profiles-with-a-workflow)

Das folgende Feld wird dann zu unseren Profilen hinzugefügt und kann für einen Versand ausgewählt werden:

![](assets/schema_extension_uc20.png)

Verwandte Themen:

* [Über benutzerdefinierte Ressourcen](../../developing/using/data-model-concepts.md)
* [Verwaltung von Profilen](../../audiences/using/about-profiles.md)
* [Verwaltung von Testprofilen](../../audiences/using/managing-test-profiles.md)

## Schritt 1: Profil-Ressource erweitern  {#step-1--extend-the-profile-resource}

To create the new **Interest** field for our profiles, you first need to extend the out-of-the-box **[!UICONTROL Profiles (profile)]** resource.

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration]** > **[!UICONTROL Development]**, then **[!UICONTROL Custom resources]**.
1. If you have not extended the **[!UICONTROL Profiles]** resource yet, click **[!UICONTROL Create]**.
1. Wählen Sie die **[!UICONTROL Extend an existing resource]** Option.
1. Select the **[!UICONTROL Profile (profile)]** resource.
1. Klicks **[!UICONTROL Create]**.

   ![](assets/schema_extension_uc5.png)

1. Klicken Sie in der **[!UICONTROL Fields]** Kategorie der **[!UICONTROL Data structure]** Registerkarte auf **[!UICONTROL Create element]**.

   >[!NOTE]
   >
   >Note that if you already extended the **[!UICONTROL Profile]** resource for previous purposes, you can start at this step by clicking **[!UICONTROL Add field]**.

   ![](assets/schema_extension_uc6.png)

1. Fügen Sie eine **[!UICONTROL Label]** und eine hinzu **[!UICONTROL ID]**. Select the **[!UICONTROL Text]** type and click **[!UICONTROL Add]**.

   ![](assets/schema_extension_uc9.png)

1. To configure your field, in the **[!UICONTROL Data structure]** tab under the **[!UICONTROL Fields]** drop-down, click ![](assets/schema_extension_uc8.png) then ![](assets/schema_extension_uc7.png) from your previously created field.
1. In diesem Beispiel möchten wir bestimmte Werte hinzufügen, klicken Sie dazu **[!UICONTROL Specify a list of authorized values]**.

   ![](assets/schema_extension_uc10.png)

1. Klicken Sie auf **[!UICONTROL Add an element]** und fügen Sie durch Hinzufügen eines **[!UICONTROL Label]** und eines **[!UICONTROL ID]** und Klicken auf **[!UICONTROL Add]** dann so viele Werte hinzu wie erforderlich.

   In unserem Beispiel sollen die Werte &quot;Bücher&quot;, &quot;Ausstellungen&quot;, &quot;Filme&quot; und &quot;k. A.&quot; erstellt werden, die in den Profilen zur Auswahl stehen werden.

   ![](assets/schema_extension_uc11.png)

1. To add this field in the **[!UICONTROL Profile]** screen, click the **[!UICONTROL Screen definition]** tab.
1. Klicken Sie in der **[!UICONTROL Detail screen configuration]** Dropdownliste auf **[!UICONTROL Add a personalized fields section]** und dann auf **[!UICONTROL Create element]**.

   ![](assets/schema_extension_uc12.png)

1. Select a **[!UICONTROL Type]**. In unserem Beispiel soll ein Eingabefeld hinzugefügt werden. Then, select your previously created field and click **[!UICONTROL Add]**.

   ![](assets/schema_extension_uc2.png)

1. To add a separator to better organize your profile window, click **[!UICONTROL Create an element]** and select **[!UICONTROL Separator]** from the **[!UICONTROL Type]** drop-down.

   ![](assets/schema_extension_uc19.png)

Ihr Feld wird daraufhin konfiguriert. Jetzt wird es auf das Testprofil erweitert.

>[!NOTE]
>
>Wenn Sie die Testprofil-Ressource nicht erweitern müssen, können Sie mit dem Schritt zum Publizieren fortfahren.

## Schritt 2: Testprofil erweitern  {#step-2--extend-the-test-profile}

Um zu überprüfen, ob das neu erstellte Feld korrekt konfiguriert ist, können Sie es testen, indem Sie Ihre Nachricht an Testprofile senden. Zunächst muss das neue Feld auch auf die Testprofile übertragen werden.

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration]** > **[!UICONTROL Development]**, then **[!UICONTROL Custom resources]**.
1. If you have not extended the **[!UICONTROL Profiles]** resource yet, click **[!UICONTROL Create]**.
1. Wählen Sie die **[!UICONTROL Extend an existing resource]** Option.
1. Select the **[!UICONTROL Test profile (seedMember)]** resource.
1. Klicks **[!UICONTROL Create]**.

   ![](assets/schema_extension_uc13.png)

1. Klicken Sie auf der **[!UICONTROL Data structure]** Registerkarte auf **[!UICONTROL Create element]**.

   ![](assets/schema_extension_uc15.png)

1. Select your previously created resource field and click **[!UICONTROL Add]**.

   ![](assets/schema_extension_uc16.png)

1. Carry out the same steps from step 11 to 13 as the extend profile walkthrough above to add this field in the **[!UICONTROL Test profile]** screen.
1. Klicks **[!UICONTROL Save]**.

Ihr neues Feld ist jetzt sowohl in den Profilen als auch in den Testprofilen verfügbar. Damit es korrekt konfiguriert wird, müssen Sie Ihre benutzerdefinierte Ressource publizieren.

## Schritt 3: Benutzerdefinierte Ressource publizieren  {#step-3--publish-your-custom-resource}

Zur Übernahme der Änderungen der Ressourcen und deren Verwendung muss die Datenbank aktualisiert werden.

1. Wählen Sie im erweiterten Menü **Administration** > **Entwicklung** und dann **Publizieren** aus.
1. By default, the option **[!UICONTROL Determine modifications since the last publication]** is checked, which means that only the changes carried out since the last update will be applied.

   ![](assets/schema_extension_uc14.png)

1. Click **[!UICONTROL Prepare publication]** to start the analysis which will update your database.
1. Nach erfolgreicher Analyse können Sie unter Verwendung der Schaltfläche **Publizieren** die Konfigurationsänderungen übernehmen.

   ![](assets/schema_extension_uc17.png)

1. Im Anschluss an die Publikation werden in der **Zusammenfassung** der entsprechenden Ressourcen der Status **Publiziert** und das letzte Publikationsdatum angezeigt.

   ![](assets/schema_extension_uc18.png)

1. Select the **[!UICONTROL Profiles]** tab and click **[!UICONTROL New]** to see if your changes have been correctly implemented.

   ![](assets/schema_extension_uc20.png)

Ihr neues Ressourcenfeld kann jetzt verwendet und beispielsweise bei einem Versand ausgewählt werden.

## Schritt 4: Profile mit einem Workflow aktualisieren und auswählen  {#step-4--update-and-target-profiles-with-a-workflow}

To update profiles with data for the new custom field, you can create a landing page using the **[!UICONTROL Profile acquisition]** template. Weiterführende Informationen zu Landingpages finden Sie auf dieser [Seite](../../channels/using/getting-started-with-landing-pages.md).

In unserem Beispiel sollen in einem Workflow Profile ausgewählt werden, bei denen dieses Feld nicht ausgefüllt ist. Diese sollen eine E-Mail erhalten, in der sie gebeten werden, ihre Profile zu aktualisieren, damit sie Newsletter und Angebote erhalten können. Jedes Profil erhält daraufhin einen personalisierten Newsletter, der an die jeweiligen Interessen angepasst ist.

Zuerst muss eine Landingpage erstellt werden, über die das **Interessen**-Feld der Profile der Zielgruppe aktualisiert wird:

1. Klicken Sie im **[!UICONTROL Marketing activities]** Fenster auf **[!UICONTROL Create]** und wählen Sie **[!UICONTROL Landing page]**.
1. Wählen Sie einen Landingpage-Typ aus. Here, since we want to update our profiles, select **[!UICONTROL Profile acquisition]**.
1. Klicks **[!UICONTROL Create]**.
1. Click the **[!UICONTROL Content]** block to start editing the content of your landing page.

   ![](assets/schema_extension_uc21.png)

1. Passen Sie Ihre Landingpage nach Bedarf an.
1. Wählen Sie das für Ihre Profile konfigurierte Feld aus, in dem diese ihre Interessen auswählen können. Wählen Sie im linken Bereich die zuvor erstellte benutzerdefinierte Ressource **Interessen** aus.

   ![](assets/schema_extension_uc22.png)

1. Speichern Sie Ihre Landingpage und testen Sie sie, um festzustellen, ob die Felder korrekt konfiguriert sind.
1. Click **[!UICONTROL Publish]** when your landing page is ready.

Ihre Landingpage kann jetzt verwendet werden. Um die Profile zu aktualisieren, erstellen Sie einen Workflow, mit dem anschließend ein spezielles Angebot entsprechend den ausgewählten Interessen gesendet wird.

1. Klicken Sie auf der **[!UICONTROL Marketing activities]** Registerkarte auf **[!UICONTROL Create]** und wählen Sie **[!UICONTROL Workflow]**.
1. Drag and drop a **[!UICONTROL Query]** activity to target the profiles or audiences you need.
1. Drag and drop an **[!UICONTROL Email delivery]** activity to start configuring your email which will contain a link to the landing page. Wählen Sie die **[!UICONTROL Add an outbound transition with the population]**.

   ![](assets/schema_extension_uc3.png)

1. Erstellen und gestalten Sie Ihre E-Mail nach Bedarf. Weiterführende Informationen zur Personalisierung von E-Mails finden Sie auf dieser [Seite](../../designing/using/quick-start.md).
1. Fügen Sie zu Ihrer E-Mail eine Schaltfläche hinzu, mit der Profile zu Ihrer Landingpage weitergeleitet werden.
1. Wählen Sie die hinzugefügte Schaltfläche aus und klicken Sie danach auf der linken Seite in den ![](assets/schema_extension_uc7.png)**[!UICONTROL Link]**-Bereich.

   ![](assets/schema_extension_uc23.png)

1. Wählen Sie im **[!UICONTROL Insert link]** Fenster **[!UICONTROL Landing page]** aus der **[!UICONTROL Link type]** Dropdownliste und dann die zuvor erstellte Einstiegsseite aus.

   ![](assets/schema_extension_uc24.png)

1. Klicks **[!UICONTROL Save]**. Ihre E-Mail ist jetzt fertig und Sie können mit Ihrem Workflow fortfahren.
1. Add a **[!UICONTROL Wait]** activity to let some time for your profiles to fill the landing page.
1. Add a **[!UICONTROL Segmentation]** activity to split the outbound transition depending on their **Interests**.
1. Erstellen Sie für jedes **Interesse** ein ausgehendes Segment.

   ![](assets/schema_extension_uc4.png)

1. Add an **[!UICONTROL Email delivery]** activity after each transition and create a personalized email depending on the chosen **Interest**.
1. Wenn die Konfiguration abgeschlossen ist, starten Sie den Workflow.

   ![](assets/schema_extension_uc25.png)

Die Profile erhalten jetzt eine E-Mail, in der sie ersucht werden, dieses Interessen-Feld auszufüllen. In weiterer Folge erhalten sie eine personalisierte E-Mail, die den ausgewählten Interessen entspricht.

---
title: Profil-Ressource um ein neues Feld erweitern
seo-title: Profil-Ressource um ein neues Feld erweitern
description: Profil-Ressource um ein neues Feld erweitern
seo-description: Hier erfahren Sie, wie die Profil-Ressource erweitert wird.
page-status-flag: nie aktiviert
uuid: 9 b 99 e 95 c -93 ff -4187-90 f 7-db 0 baf 369 ad
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird entwickelt
content-type: Referenz
topic-tags: Anwendungsfälle—expanding-resources
discoiquuid: 1 e 0 f 8945-fc 3 c -46 a 9-a 8 e 5-b 181 a 1 f 5 ffcb
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 806dc4736ffb395a0eea102090c688102478aaca

---


# Profil-Ressource um ein neues Feld erweitern{#extending-the-profile-resource-with-a-new-field}

## Über Profilerweiterungen {#about-extending-profiles}

Das folgende Anwendungsbeispiel erläutert die Erweiterung der Profil- und der Testprofil-Ressourcen um ein zusätzliches Feld.

In unserem Beispiel wird gezeigt, wie die Profile unter Verwendung einer Landingpage mit dem neuen Feld aktualisiert werden und dann an Profile ein Newsletter gesendet wird, der genau ihren Interessen entspricht.

Gehen Sie dazu wie folgt vor:

* [Schritt 1: Profil-Ressource erweitern](../../developing/using/extending-the-profile-resource-with-a-new-field.md#step-1--extend-the-profile-resource)
* [Schritt 2: Testprofil erweitern](../../developing/using/extending-the-profile-resource-with-a-new-field.md#step-2--extend-the-test-profile)
* [Schritt 3: Benutzerdefinierte Ressource publizieren](../../developing/using/extending-the-profile-resource-with-a-new-field.md#step-3--publish-your-custom-resource)
* [Schritt 4: Profile mit einem Workflow aktualisieren und auswählen](../../developing/using/extending-the-profile-resource-with-a-new-field.md#step-4--update-and-target-profiles-with-a-workflow)

Das folgende Feld wird dann zu unseren Profilen hinzugefügt und kann für einen Versand ausgewählt werden:

![](assets/schema_extension_uc20.png)

Verwandte Themen:

* [Über benutzerdefinierte Ressourcen](../../developing/using/data-model-concepts.md)
* [Verwaltung von Profilen](../../audiences/using/about-profiles.md)
* [Verwaltung von Testprofilen](../../sending/using/managing-test-profiles-and-sending-proofs.md#managing-test-profiles)

## Schritt 1: Profil-Ressource erweitern {#step-1--extend-the-profile-resource}

Um das neue Feld **Interessen** für unsere Profile zu erstellen, müssen Sie zunächst die native Ressource **[!UICONTROL Profile (profile)]erweitern.**

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]**, then **[!UICONTROL Custom resources]**.
1. If you have not extended the **[!UICONTROL Profiles]** resource yet, click **[!UICONTROL Create]**.
1. Wählen Sie die Option **[!UICONTROL Existierende Ressource erweitern].**
1. Wählen Sie die Ressource **[!UICONTROL Profil (profile)]aus.**
1. Wählen Sie **[!UICONTROL Erstellen aus]**.

   ![](assets/schema_extension_uc5.png)

1. In the **[!UICONTROL Fields]** category of the **[!UICONTROL Data structure]** tab, click **[!UICONTROL Create element]**.

   >[!NOTE]
   >
   >Note that if you already extended the **[!UICONTROL Profile]** resource for previous purposes, you can start at this step by clicking **[!UICONTROL Add field]**.

   ![](assets/schema_extension_uc6.png)

1. Add a **[!UICONTROL Label]** and an **[!UICONTROL ID]**. Select the **[!UICONTROL Text]** type and click **[!UICONTROL Add]**.

   ![](assets/schema_extension_uc9.png)

1. Um das Feld zu konfigurieren, wählen Sie im Tab **[!UICONTROL Datenstruktur]** in der Dropdown-Liste **[!UICONTROL Felder]** die Option ![](assets/schema_extension_uc8.png) und dann ![](assets/schema_extension_uc7.png) im zuvor erstellten Feld aus.
1. In this example we want to add specific values, to do so click **[!UICONTROL Specify a list of authorized values]**.

   ![](assets/schema_extension_uc10.png)

1. Click **[!UICONTROL Add an element]** then add as many value as needed by adding a **[!UICONTROL Label]** and an **[!UICONTROL ID]** and clicking **[!UICONTROL Add]**.

   In unserem Beispiel sollen die Werte Bücher, Ausstellungen, Filme und k.A. Erstellt werden, die den Profilen zur Auswahl stehen werden.

   ![](assets/schema_extension_uc11.png)

1. Um dieses Feld im Bildschirm **[!UICONTROL Profil]** hinzuzufügen, wählen Sie den Tab **Bildschirmdefinition]aus.[!UICONTROL **
1. In the **[!UICONTROL Detail screen configuration]** drop-down, click **[!UICONTROL Add a personalized fields section]** and click **[!UICONTROL Create element]**.

   ![](assets/schema_extension_uc12.png)

1. Select a **[!UICONTROL Type]**. In unserem Beispiel möchten soll ein Eingabefeld hinzugefügt werden. Then, select your previously created field and click **[!UICONTROL Add]**.

   ![](assets/schema_extension_uc2.png)

1. Um ein Trennzeichen zur übersichtlicheren Gestaltung Ihres Profilfensters hinzuzufügen, wählen Sie **[!UICONTROL Element erstellen]** und danach **[!UICONTROL Trennzeichen]in der Dropdown-Liste** Typ] aus.**[!UICONTROL **

   ![](assets/schema_extension_uc19.png)

Ihr Feld wird daraufhin konfiguriert. Jetzt wird es auf das Testprofil erweitert.

>[!NOTE]
>
>Wenn Sie die Testprofil-Ressource nicht erweitern müssen, können Sie mit dem Schritt zum Publizieren fortfahren.

## Schritt 2: Testprofil erweitern {#step-2--extend-the-test-profile}

Um zu überprüfen, ob das neu erstellte Feld korrekt konfiguriert ist, können Sie es testen, indem Sie Ihre Nachricht an Testprofile senden. Zunächst muss das neue Feld auch auf die Testprofile übertragen werden.

1. From the advanced menu, via the Adobe Campaign logo, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Development]**, then **[!UICONTROL Custom resources]**.
1. If you have not extended the **[!UICONTROL Profiles]** resource yet, click **[!UICONTROL Create]**.
1. Wählen Sie die Option **[!UICONTROL Existierende Ressource erweitern].**
1. Wählen Sie die Ressource **[!UICONTROL Testprofil (seedMember)]aus.**
1. Wählen Sie **[!UICONTROL Erstellen aus]**.

   ![](assets/schema_extension_uc13.png)

1. In the **[!UICONTROL Data structure]** tab, click **[!UICONTROL Create element]**.

   ![](assets/schema_extension_uc15.png)

1. Select your previously created resource field and click **[!UICONTROL Add]**.

   ![](assets/schema_extension_uc16.png)

1. Führen Sie dieselben Schritte 11 bis 13 der Anleitung zur Profilerweiterung durch, um dieses Feld im Bildschirm **[!UICONTROL Testprofil]hinzuzufügen.**
1. Wählen Sie **[!UICONTROL Speichern aus]**.

Ihr neues Feld ist jetzt sowohl in den Profilen als auch in den Testprofilen verfügbar. Damit es korrekt konfiguriert wird, müssen Sie Ihre benutzerdefinierte Ressource publizieren.

## Schritt 3: Benutzerdefinierte Ressource publizieren {#step-3--publish-your-custom-resource}

Zur Übernahme der Änderungen der Ressourcen und deren Verwendung muss die Datenbank aktualisiert werden.

1. Wählen Sie im erweiterten Menü **Administration** &gt; **Entwicklung** und dann **Publizieren** aus.
1. Standardmäßig ist die Option **[!UICONTROL Änderungen seit der letzten Publikation ermitteln]aktiv. Dies bedeutet, dass nur die Änderungen übernommen werden, die seit der letzten Publikation vorgenommen wurden.**

   ![](assets/schema_extension_uc14.png)

1. Wählen Sie **[!UICONTROL Publikation vorbereiten]aus, um die Analyse zu starten, durch die Ihre Datenbank aktualisiert wird.**
1. Nach erfolgreicher Analyse können Sie unter Verwendung der Schaltfläche **Publizieren** die Konfigurationsänderungen übernehmen.

   ![](assets/schema_extension_uc17.png)

1. Im Anschluss an die Publikation werden in der **Zusammenfassung** der entsprechenden Ressourcen der Status **Publiziert** und das letzte Publikationsdatum angezeigt.

   ![](assets/schema_extension_uc18.png)

1. Wählen Sie den Tab **[!UICONTROL Profile]** und danach **Neu]aus, um zu überprüfen, ob Ihre Änderungen korrekt implementiert wurden.[!UICONTROL **

   ![](assets/schema_extension_uc20.png)

Ihr neues Ressourcenfeld kann jetzt verwendet und beispielsweise bei einem Versand ausgewählt werden.

## Schritt 4: Profile mit einem Workflow aktualisieren und auswählen {#step-4--update-and-target-profiles-with-a-workflow}

Um Profile mit Daten aus dem neuen benutzerdefinierten Feld zu aktualisieren, können Sie eine Landingpage mithilfe der Vorlage **[!UICONTROL Profilakquise]erstellen.** Weiterführende Informationen zu Landingpages finden Sie auf dieser [Seite](../../channels/using/about-landing-pages.md).

In unserem Beispiel sollen in einem Workflow Profile ausgewählt werden, bei denen dieses Feld nicht ausgefüllt ist. Diese sollen eine E-Mail erhalten, in der sie gebeten werden, ihre Profile zu aktualisieren, damit sie Newsletter und Angebote erhalten können. Jedes Profil erhält daraufhin einen personalisierten Newsletter, der an die jeweiligen Interessen angepasst ist.

Zuerst muss eine Landingpage erstellt werden, über die das **Interessen**-Feld der Profile der Zielgruppe aktualisiert wird:

1. From the **[!UICONTROL Marketing activities]**, click **[!UICONTROL Create]** then select **[!UICONTROL Landing page]**.
1. Wählen Sie einen Landingpage-Typ aus. Here, since we want to update our profiles, select **[!UICONTROL Profile acquisition]**.
1. Wählen Sie **[!UICONTROL Erstellen aus]**.
1. Klicken Sie auf den Baustein **[!UICONTROL Inhalt], um den Inhalt der Landingpage zu bearbeiten.**

   ![](assets/schema_extension_uc21.png)

1. Passen Sie Ihre Landingpage nach Bedarf an.
1. Wählen Sie das für Ihre Profile konfigurierte Feld aus, in dem diese ihre Interessen auswählen können. Wählen Sie im linken Bereich die zuvor erstellte benutzerdefinierte Ressource **Interessen** aus.

   ![](assets/schema_extension_uc22.png)

1. Speichern Sie Ihre Landingpage und testen Sie sie, um festzustellen, ob die Felder korrekt konfiguriert sind.
1. Wenn Ihre Landingpage bereit ist, wählen Sie **[!UICONTROL Publizieren]aus.**

Ihre Landingpage kann jetzt verwendet werden. Um die Profile zu aktualisieren, erstellen Sie einen Workflow, mit dem anschließend ein spezielles Angebot entsprechend den ausgewählten Interessen gesendet wird.

1. From the **[!UICONTROL Marketing activities]** tab, click **[!UICONTROL Create]** then select **[!UICONTROL Workflow]**.
1. Ziehen Sie die Aktivität **[!UICONTROL Abfrage]in den Arbeitsbereich, um die entsprechenden Profile oder Audiences auszuwählen.**
1. Ziehen Sie die Aktivität **[!UICONTROL E-Mail-Versand]in den Arbeitsbereich, um die E-Mail zu konfigurieren, die einen Link zur Landingpage enthält.** Select the **[!UICONTROL Add an outbound transition with the population]**.

   ![](assets/schema_extension_uc3.png)

1. Erstellen und gestalten Sie Ihre E-Mail nach Bedarf. Weiterführende Informationen zur Personalisierung von E-Mails finden Sie auf dieser [Seite](../../designing/using/designing-content-in-adobe-campaign.md).
1. Fügen Sie zu Ihrer E-Mail eine Schaltfläche hinzu, mit der Profile zu Ihrer Landingpage weitergeleitet werden.
1. Wählen Sie die hinzugefügte Schaltfläche aus und klicken Sie danach auf der linken Seite in den ![](assets/schema_extension_uc7.png)**Link[!UICONTROL -Bereich.]**

   ![](assets/schema_extension_uc23.png)

1. Wählen Sie im Fenster **[!UICONTROL Link einfügen]** die Option **[!UICONTROL Landingpage]aus der Dropdown-Liste** Linktyp] und danach die zuvor erstellte Landingpage aus.**[!UICONTROL **

   ![](assets/schema_extension_uc24.png)

1. Wählen Sie **[!UICONTROL Speichern aus]**. Ihre E-Mail ist jetzt fertig und Sie können mit Ihrem Workflow fortfahren.
1. Fügen Sie die Aktivität **[!UICONTROL Warten]hinzu, um Ihren Profilen etwas Zeit zum Ausfüllen des Formulars auf der Landingpage zu geben.**
1. Fügen Sie die Aktivität **[!UICONTROL Segmentierung]** hinzu, um die ausgehende Transition entsprechend den **Interessen** aufzuspalten.
1. Erstellen Sie für jedes **Interesse** ein ausgehendes Segment.

   ![](assets/schema_extension_uc4.png)

1. Fügen Sie nach jeder Transition die Aktivität **[!UICONTROL E-Mail-Versand]** hinzu und erstellen Sie entsprechend den ausgewählten **Interessen** eine personalisierte E-Mail.
1. Wenn die Konfiguration abgeschlossen ist, starten Sie den Workflow.

   ![](assets/schema_extension_uc25.png)

Die Profile erhalten jetzt eine E-Mail, in der sie ersucht werden, dieses Interessen-Feld auszufüllen. In weiterer Folge erhalten sie eine personalisierte E-Mail, die den ausgewählten Interessen entspricht.

---
title: Testen von E-Mail-Nachrichten mit Zielgruppenprofilen
description: Erfahren Sie, wie Sie Nachrichten mit Zielgruppenprofilen und Ersatzadressen testen können.
page-status-flag: never-activated
uuid: eb4d893b-3724-4b15-9312-1ec74784368d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: preparing-and-testing-messages
discoiquuid: 37320ec5-196c-4260-8156-98932da3e4a5
context-tags: seedMember,overview
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b7894637d184c16221e03c909f3c356fbb6c5e79

---


# Testen von E-Mail-Nachrichten mit Zielgruppenprofilen {#testing-message-profiles}

## Übersicht {#overview}

Zusätzlich zu [Testprofilen](../../audiences/using/managing-test-profiles.md) können Sie auch eine E-Mail-Nachricht testen, indem Sie sich in die Position eines der Zielgruppenprofile versetzen. So erhalten Sie eine genaue Darstellung der Nachricht, die das Profil empfangen wird (benutzerdefinierte Felder, dynamische und personalisierte Informationen, einschließlich zusätzlicher Daten von Workflows usw.).

>[!NOTE]
>
> Diese Funktion ist nur bei E-Mail-Nachrichten verfügbar.

Die wichtigsten Schritte sind:

1. Konfigurieren Sie Ihre Nachricht und starten Sie dann die **Vorbereitungsphase**.
1. **Wählen Sie eines oder mehrere Profile** aus den Profilen aus, die zur Zielgruppe der Nachricht gehören.
1. Weisen Sie jedem Profil eine **Ersatzadresse** zu, an die Testsendungen gesendet werden sollen.
1. (Optional) Definieren Sie für jedes Profil ein **Präfix**, das der Betreffzeile des Testversands hinzugefügt werden soll.
1. Nutzen Sie die **Vorschau** in Email Designer, um zu ermitteln, wie die Nachricht für die Profile angezeigt wird.
1. Versenden Sie die Testsendungen.

Weiterführende Informationen zum allgemeinen Verfahren finden Sie im Tutorial-Video, das [hier](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/communication-channels/email/profile-substitution.html) verfügbar ist.

>[!IMPORTANT]
>
>Mit dieser Funktion können Sie personenbezogene Daten des Profils an externe E-Mail-Adressen senden. Beachten Sie, dass eine Ausführung von Datenschutzanfragen (DSGVO und CCPA) in Campaign Standard NICHT zu einer externen Ausführung der Anfrage führen wird.

## Auswählen von Profilen und Ersatzadressen {#selecting-profiles}

Um Zielgruppenprofile zum Testen zu verwenden, müssen Sie diese zunächst auswählen und dann die Ersatzadressen definieren, an die die Testsendungen gesendet werden sollen. Dazu können Sie entweder aus den Zielgruppenprofilen [spezifische Profile auswählen](#selecting-individual-profiles) oder [Profile aus einer vorhandenen Audience importieren](#importing-from-audience).

>[!NOTE]
>
>Sie können maximal 100 Profile zum Testen auswählen.

### Auswählen einzelner Profile {#selecting-individual-profiles}

1. Vergewissern Sie sich im Nachrichten-Dashboard, dass die Nachrichtenvorbereitung erfolgreich war, und klicken Sie dann auf den **[!UICONTROL Audience]**-Bereich.

   ![](assets/substitution_preparation.png)

1. In the **[!UICONTROL Profile substitutions]** tab, click the **[!UICONTROL Create element]** button to select the profiles to use for testing.

   ![](assets/substitution_tab.png)

1. Klicken Sie auf die Schaltfläche zur Profilauswahl, um die Liste der Profile anzuzeigen, die zur Zielgruppe der Nachricht gehören.

   ![](assets/substitution_recipient_selection.png)

1. Select the profile to use for testing, then enter in the **[!UICONTROL Address]** field the desired substitution address, then click **[!UICONTROL Confirm]**. Alle Testsendungen, bei denen das Profil zur Zielgruppe gehört, werden an diese E-Mail-Adresse gesendet und nicht an die in der Datenbank für das Profil definierte Adresse.

   If you want to add a specific prefix to the proofs&#39; subject line, fill in the **[!UICONTROL Subject line prefix]** field.

   ![](assets/substitution_address.png)

   Das Präfix wird wie folgt angezeigt:

   ![](assets/substitution_prefixsample.png)

1. Das Profil wird der Liste mit der entsprechenden Ersatzadresse und dem dazugehörigen Präfix hinzugefügt. Repeat the above steps for all the profiles that you want to use for testing, then click **[!UICONTROL Confirm]**.

   ![](assets/substitution_recipients_confirm.png)

   Wenn Sie einen Testversand für dasselbe Profil an verschiedene Ersatzadressen senden möchten, müssen Sie dieses Profil so oft wie erforderlich hinzufügen.

   Im folgenden Beispiel wird der Testversand, der auf dem Profil „John Smith“ basiert, an zwei verschiedene Ersatzadressen gesendet:

   ![](assets/substitution_multiple_addresses.png)

1. Sobald alle Profile und Ersatzadressen definiert sind, können Sie einen Testversand durchführen, um die Nachricht zu testen. To do this, click the **[!UICONTROL Test]** button, then select the type of test to perform.

   Note that if no test profile has been added to the message target, the **[!UICONTROL Email rendering]** and **[!UICONTROL Proof + Email rendering]** options are not available.  Weiterführende Informationen zum Durchführen eines Testversands finden Sie in [diesem Abschnitt](../../sending/using/sending-proofs.md).

   ![](assets/substitution_send_test.png)

>[!IMPORTANT]
>
>Wenn Sie Änderungen an Ihrer Nachricht vornehmen, stellen Sie sicher, dass Sie die Nachrichtenvorbereitung erneut starten. Andernfalls werden die Änderungen im Testversand nicht übernommen.

### Importieren von Profilen aus einer Audience {#importing-from-audience}

Campaign Standard ermöglicht den Import einer Audience mit Profilen, die Sie zum Testen verwenden können. So können Sie beispielsweise mehrere Nachrichten, die sich an verschiedene Profile richten, an eine einzige E-Mail-Adresse senden.

Moreover, if your audience is already configured with the address and prefix columns, you will be able to import these information in the **[!UICONTROL Profile substitutions]** tab. Ein Beispiel für den Import einer Audience mit Ersatzadressen finden Sie in [diesem Abschnitt](#use-case).

>[!NOTE]
>
>When importing an audience, only the profiles corresponding to the message target are selected and added to the **[!UICONTROL Profile substitutions]** tab.

Gehen Sie wie folgt vor, um Profile, die zum Testen einer Audience verwendet werden sollen, zu importieren:

1. Vergewissern Sie sich im Nachrichten-Dashboard, dass die Nachrichtenvorbereitung erfolgreich war, und klicken Sie dann auf den **[!UICONTROL Audience]**-Bereich.

   ![](assets/substitution_preparation.png)

1. Klicken Sie auf der **[!UICONTROL Profile substitutions]** Registerkarte auf **[!UICONTROL Import from an audience]**.

   ![](assets/substitution_audience_import.png)

1. Wählen Sie die zu verwendende Audience aus und geben Sie dann die Ersatzadresse und das Präfix ein, die für die an die Audience gesendeten Testsendungen verwendet werden sollen.

   ![](assets/substitution_audience_define.png)

   If the substitution addresses and/or prefixes to use have already been defined in your audience, select the **[!UICONTROL From Audience]** option, then specify the column to use to retrieve these information.

   ![](assets/substitution_fromaudience.png)

1. Click the **[!UICONTROL Import]** button. The profiles from the audience corresponding to the message target are added to the **[!UICONTROL Profile substitution]** tab, as well as the associated substitution addresses and prefixes.

![](assets/substitution_audience_imported.png)

>[!NOTE]
>
>Wenn Sie die gleiche Audience mit unterschiedlichen Ersatzadressen und/oder Präfixen erneut importieren, werden die Profile zusätzlich zu den Profilen aus dem vorherigen Import der Liste hinzugefügt.

## Anzeigen einer Vorschau der Nachricht mit Zielgruppenprofilen

>[!NOTE]
>
>Eine Vorschau ist nur mit Email Designer möglich.

To be able to preview messages using targeted profiles, make sure you have added these profiles to the **[!UICONTROL Profile substitution]** list (see [Defining profiles and substitution addresses](#selecting-profiles)).

Wenn Sie in der Nachricht Personalisierungsfelder verwenden möchten, müssen Sie diese hinzufügen, **bevor** Sie die Nachrichtenvorbereitung starten. Andernfalls werden sie in der Vorschau nicht berücksichtigt. Stellen Sie also sicher, dass Sie die Nachrichtenvorbereitung erneut starten, sollten Sie an den Personalisierungsfeldern Änderungen vorgenommen haben.

Gehen Sie wie folgt vor, um Nachrichten bei Verwendung von Profilersetzungen als Vorschau anzuzeigen:

1. Klicken Sie im Nachrichten-Dashboard auf den Inhalts-Snapshot, um die Nachricht in Email Designer zu öffnen.

   ![](assets/substitution_preview_access.png)

1. Wählen Sie die **[!UICONTROL Preview]** Registerkarte und klicken Sie auf **[!UICONTROL Change profile]**.

   ![](assets/substitution_preview_changeprofile.png)

1. Click the **[!UICONTROL Profile Substitution]** tab to display the substitution profiles that have been added for testing.

   Select the profiles that you want to use for preview, then click **[!UICONTROL Select]**.

   ![](assets/substitution_preview_selection.png)

1. Eine Vorschau der Nachricht wird angezeigt. Verwenden Sie die Pfeile, um zwischen den ausgewählten Profilen zu navigieren.

   ![](assets/substitution_preview.png)

## Anwendungsbeispiel {#use-case}

In diesem Beispiel möchten wir einen personalisierten E-Mail-Newsletter an bestimmte Profile senden. Vor dem Versand des Newsletters möchten wir ihn mit einigen der Zielgruppenprofile als Vorschau anzeigen und einen Testversand an interne E-Mail-Adressen durchführen, die in einer externen Datei definiert sind.

Die Umsetzung des Anwendungsbeispiels gliedert sich in folgende Schritte:

1. Erstellen Sie die Audience, die zum Testen verwendet werden soll.
1. Richten Sie einen Workflow ein, um Profile in die Zielgruppe aufzunehmen und den Newsletter zu senden.
1. Konfigurieren Sie die Profilersetzungen der Nachricht.
1. Zeigen Sie eine Vorschau der Nachricht mit Zielgruppenprofilen an.
1. Führen Sie einen Testversand durch.

### Schritt 1: Audience für Testzwecke erstellen

1. Bereiten Sie die zu importierende Datei vor, um die Audience zu erstellen. In unserem Beispiel sollte sie die für den Testversand zu verwendende Ersatzadresse und ein Präfix enthalten, das der Betreffzeile des Testversands hinzugefügt wird.

   In diesem Fall erhält die E-Mail-Adresse „oliver.vaughan@internal.com“ einen Testversand der Nachricht, die an das Profil mit der E-Mail-Adresse „john.doe@mail.com“ gesendet wird. Der Betreffzeile des Testversands wird das Präfix „JD“ hinzugefügt.

   ![](assets/substitution_uc1.png)

1. Richten Sie den Workflow ein, um eine Audience aus der Datei zu erstellen. Fügen Sie dazu die folgenden Aktivitäten hinzu und konfigurieren Sie sie:

   * **[!UICONTROL Load file]** Aktivität: Importiert die CSV-Datei (weitere Informationen zu dieser Aktivität finden Sie in [diesem Abschnitt](../../automating/using/load-file.md)).
   * **[!UICONTROL Reconciliation]** Aktivität: Verknüpft Informationen aus der Datei mit Informationen aus der Datenbank. In diesem Beispiel verwenden wir die E-Mail-Adresse des Profils als Abstimmungsfeld (weitere Informationen zu dieser Aktivität finden Sie in [diesem Abschnitt](../../automating/using/reconciliation.md)).
   * **[!UICONTROL Save audience]** Aktivität: Erstellt eine Audience basierend auf der importierten Datei (weitere Informationen zu dieser Aktivität finden Sie in [diesem Abschnitt](../../automating/using/save-audience.md)).
   ![](assets/substitution_uc2.png)

1. Führen Sie den Workflow aus und klicken Sie dann auf den Tab **[!UICONTROL Audiences]**, um zu überprüfen, ob die Audience mit den gewünschten Informationen erstellt wurde.

   In diesem Beispiel besteht die Audience aus drei Profilen. Jedes der Profile ist mit einer Ersatz-E-Mail-Adresse verknüpft, die den Testversand erhalten wird, inklusive eines Präfixes, das im Betreff des Testversands verwendet wird.

   ![](assets/substitution_uc3.png)

### Schritt 2: Einen Workflow zum Auswählen von Profilen und Senden des Newsletters erstellen

1. Add **[!UICONTROL Query]** and **[!UICONTROL Email delivery]** activities, then configure them according to your needs (see [Query](../../automating/using/query.md) and [Email delivery](../../automating/using/email-delivery.md) sections).

   ![](assets/substitution_uc4.png)

1. Führen Sie den Workflow aus und vergewissern Sie sich, dass die Nachrichtenvorbereitung erfolgreich war.

### Schritt 3: Tab zur Profilersetzung der Nachricht konfigurieren

1. Open the **[!UICONTROL Email delivery]** activity. In the message dashboard, click the **[!UICONTROL Audience]** block.

   ![](assets/substitution_uc5.png)

1. Wählen Sie die **[!UICONTROL Profile substitutions]** Registerkarte und klicken Sie auf **[!UICONTROL Import from an audience]**.

   ![](assets/substitution_uc6.png)

1. Wählen Sie im Feld **[!UICONTROL Audience]** die aus der Datei erstellte Audience aus.

   ![](assets/substitution_uc7.png)

1. Definieren Sie die Ersatzadresse und das Betreffpräfix, die beim Senden der Testsendungen verwendet werden sollen.

   To do this, select the **[!UICONTROL From audience]** option, then select the column from the audience that contains the information.

   ![](assets/substitution_uc8.png)

1. Click the **[!UICONTROL Import]** button. Profile aus der Audience werden der Liste zusammen mit den zugehörigen Ersatzadressen und den Betreffpräfixen hinzugefügt.

   ![](assets/substitution_uc9.png)

   >[!NOTE]
   >
   >In our case, all profiles from the audience are targeted by the **[!UICONTROL Query]** activity. Wenn eines der Profile nicht zur Zielgruppe der Nachricht gehörte, wäre es nicht zur Liste hinzugefügt worden.

### Schritt 4: Vorschau der Nachricht mit Zielgruppenprofilen anzeigen

1. Klicken Sie im Nachrichten-Dashboard auf den Inhalts-Snapshot, um die Nachricht in Email Designer zu öffnen.

   ![](assets/substitution_uc10.png)

1. Wählen Sie die **[!UICONTROL Preview]** Registerkarte und klicken Sie auf **[!UICONTROL Change profile]**.

   ![](assets/substitution_uc_preview.png)

1. Click the **[!UICONTROL Profile Substitution]** tab to display the substitution profiles that have been added previously.

   Select the profiles that you want to use for preview, then click **[!UICONTROL Select]**.

   ![](assets/substitution_uc_selectpreview.png)

1. Eine Vorschau der Nachricht wird angezeigt. Verwenden Sie die Pfeile, um zwischen den ausgewählten Profilen zu navigieren.

   ![](assets/substitution_uc_previewprofile.png)

### Schritt 5: Testsendungen durchführen

1. In the message dashboard, click the **[!UICONTROL Test]** button, then confirm.

   ![](assets/substitution_uc_sendproof.png)

1. The proofs are sent according to what has been configured in the **[!UICONTROL Profile substitutions]** tab.

   ![](assets/substitution_uc_proofs.png)

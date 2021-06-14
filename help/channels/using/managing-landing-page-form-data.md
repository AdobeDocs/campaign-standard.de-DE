---
solution: Campaign Standard
product: campaign
title: Verwalten von Landingpage-Formulardaten
description: Hier erfahren Sie, wie Sie Landingpage-Formulardaten verwalten.
audience: channels
content-type: reference
topic-tags: landing-pages
context-tags: landingPage,main
feature: Landing Pages
role: Business Practitioner
level: Intermediate
exl-id: 7083447c-4cac-41cb-8453-369819e0c7c1
source-git-commit: d84a11d4064938792a2e2c365b6085c263f55648
workflow-type: ht
source-wordcount: '648'
ht-degree: 100%

---

# Landingpage-Formulardaten verwalten{#managing-landing-page-form-data}

## Landingpage über die Dateneigenschaften ändern{#changing-a-landing-page-form-data-properties}

Inhaltsblöcken wie beispielsweise Eingabefeldern, Radiobuttons oder Checkboxes können Datenbankfelder zugeordnet werden. Wählen Sie dazu den Block aus und rufen Sie die **[!UICONTROL Formulardaten]** in der Palette auf.

![](assets/delivery_content_9.png)

* Wählen Sie aus der Dropdown-Liste **Feld** das Datenbankfeld aus, das dem Formularfeld zugeordnet werden soll.
* Wenn die Option **Pflichtfeld** aktiviert ist, kann der Nutzer das Formular nicht absenden, ohne dieses Feld ausgefüllt zu haben. In diesem Fall wird eine Fehlermeldung angezeigt.

## Mapping der Formularfelder  {#mapping-form-fields}

Über Eingabefelder können Daten in der Campaign-Datenbank gespeichert bzw. dort aktualisiert werden. Dazu müssen Sie Blöcken wie Eingabe- oder Auswahlfeldern Datenbankfelder zuordnen. Gehen Sie wie folgt vor:

1. Wählen Sie in der Landingpage einen Block aus.
1. Füllen Sie in der Palette die **[!UICONTROL Formulardaten]** aus.

   ![](assets/editing_lp_content_4.png)

1. Geben Sie bei **[!UICONTROL Feld]** das Datenbankfeld an, das dem Formularfeld zugeordnet werden soll. Landingpages können nur mit **Profilen** gemappt werden.

1. Aktivieren Sie bei Bedarf die Option **[!UICONTROL Pflichtfeld]**. Die Seite kann nur gesendet werden, wenn der Anwender dieses Feld ausgefüllt hat. Wenn ein Pflichtfeld nicht ausgefüllt wurde, erscheint eine Fehlermeldung bei der Validierung der Seite.

1. Im Feld **[!UICONTROL HTML-Typ des Felds]** können Sie darüber hinaus angeben, ob es sich beispielsweise um **[!UICONTROL Text]** **[!UICONTROL Zahl]** oder **[!UICONTROL Datum]** handelt.
Wenn Sie eine obligatorische **[!UICONTROL Checkbox]** auswählen, stellen Sie sicher, dass sie vom Typ **[!UICONTROL Feld]** ist.

>[!NOTE]
>
>Die Standardfelder der nativen Landingpages sind bereits ausgefüllt. Sie können sie nach Bedarf ändern.

## Datenspeicherung und -abstimmung{#data-storage-and-reconciliation}

In den Abstimmparametern wird definiert, wie mit den von Besuchern in der Landingpage gemachten Angaben verfahren werden soll.

Gehen Sie wie folgt vor:

1. Bearbeiten Sie die Landingpage-Eigenschaften über das Symbol ![](assets/edit_darkgrey-24px.png) im Landingpage-Dashboard und rufen Sie die Parameter **[!UICONTROL Vorgang]** auf.

   ![](assets/lp_parameters_4.png)

1. Wählen Sie den **[!UICONTROL Abstimmschlüssel]** aus: Diese Datenbankfelder wie beispielsweise E-Mail, Nachname, Vorname usw. dienen dazu, Besucher bereits in der Adobe Campaign-Datenbank enthaltenen Profilen zuzuordnen. Dies erlaubt je nach gewählter Aktualisierungsstrategie, das existierende Profil zu aktualisieren oder ein neues zu erstellen.
1. Definieren Sie das **[!UICONTROL Mapping der Filterparameter]**: In diesem Bereich können Sie eine Beziehung zwischen den Formularfeldern und den im Abstimmschlüssel verwendeten Feldern herstellen.
1. Wählen Sie eine **[!UICONTROL Aktualisierungsstrategie]**: Wenn der Abstimmschlüssel die Zuordnung eines Besuchers zu einem existierenden Profil der Datenbank ermöglicht, haben Sie die Wahl, das Profil mit den Formulardaten zu aktualisieren oder nicht.

## Zustimmungs-Checkbox {#agreement-checkbox}

Sie können eine Checkbox hinzufügen, die das Profil vor dem Absenden eines Formulars auf der Landingpage markieren muss.

So können Sie beispielsweise die Zustimmung der Benutzer zu Datenschutzrichtlinien einholen oder sie dazu bringen, Ihre Nutzungsbedingungen zu akzeptieren, bevor sie ein Formular absenden.

<!--This is particularly useful in the following case:

When a profile opens the landing page from an Outlook.com mailbox, Outlook checks whether the links on the landing page are suspicious. However, this Outlook security feature (called safelinks) has an unwanted effect: it automatically activates the buttons included on the landing page. Consequently, profiles are automatically subscribed or unsubscribed without confirmation when the landing page is displayed after clicking the email link, even if they do not submit the form.

![](assets/lp_submit_button.png)

To avoid this, Adobe recommends you always add to your landing page a checkbox which enables the profile to agree before proceeding with subscription or unsubscription.-->

>[!IMPORTANT]
>
>Das Markieren dieser Checkbox ist für Benutzer obligatorisch. Wenn sie nicht markiert wird, können Benutzer kein Formular über die Landingpage absenden.

Gehen Sie wie folgt vor, um eine Checkbox einzufügen und zu konfigurieren:

1. Klicken Sie beim Erstellen der Landingpage auf **[!UICONTROL Quelle anzeigen]**.

   ![](assets/lp_show_source.png)

1. Fügen Sie wie im folgenden Beispiel gezeigt manuell eine Checkbox ein:

   ![](assets/lp_checkbox_code.png)

   <!--
   <div id="HtmlPage_htmlPage.line3" data-nl-format="datetime"><input type="checkbox" class="nl-dce-todo" data-nl-bindto="agreement" data-nl-agreementmsg="You must agree with the terms and conditions before proceeding" />I agree with the terms and conditions</div>
   -->

1. Klicken Sie auf **[!UICONTROL Quelle schließen]**.

1. Die neue Checkbox wird angezeigt. Wählen Sie sie aus.

   ![](assets/lp_select_checkbox.png)

1. Die entsprechende Dropdown-Liste wird im Abschnitt **[!UICONTROL Formulardaten]** der Palette angezeigt. Wählen Sie **[!UICONTROL Zustimmung]** aus der Liste aus.

   ![](assets/lp_form_data_drop-down.png)

   >[!NOTE]
   >
   >Das Element **[!UICONTROL Zustimmung]** ist keinem Feld der Campaign-Datenbank zugeordnet.

1. Klicken Sie auf das Symbol ![](assets/lp-properties-icon.png) neben **[!UICONTROL Formulardaten]**, um auf die erweiterten Eigenschaften der Checkbox zuzugreifen.

1. Sie können die Nachricht bei Bedarf bearbeiten.

   ![](assets/lp_agreement_message.png)

   Dieser Text wird als Warnhinweis angezeigt, wenn der Benutzer die Checkbox vor dem Absenden des Formulars nicht markiert hat.

   >[!NOTE]
   >
   >Diese Aktion ist standardmäßig obligatorisch und kann nicht geändert werden.

1. Klicken Sie auf **[!UICONTROL Bestätigen]**.

Jetzt müssen Benutzer immer vor dem Absenden des Formulars auf der Landingpage diese Checkbox markieren. Andernfalls wird ein Warnhinweis angezeigt und der Benutzer kann das Formular erst absenden, nachdem die Checkbox markiert wurde.
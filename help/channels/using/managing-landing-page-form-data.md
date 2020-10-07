---
title: Verwalten von Landingpage-Formulardaten
description: Hier erfahren Sie, wie Sie Landingpage-Formulardaten verwalten.
page-status-flag: never-activated
uuid: 5b222ea2-6628-457f-a618-bfc0e5eb93dd
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: 899c7152-f415-4df9-b4b4-5ff3470a4e32
context-tags: landingPage,main
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 100%

---


# Landingpage-Formulardaten verwalten{#managing-landing-page-form-data}

## Landingpage über die Dateneigenschaften ändern{#changing-a-landing-page-form-data-properties}

Inhaltsblöcken wie beispielsweise Eingabefeldern, Radiobuttons oder Checkboxes können Datenbankfelder zugeordnet werden. Markieren Sie hierfür den entsprechenden Block und konfigurieren Sie den Abschnitt **[!UICONTROL Formulardaten]** in der Palette.

![](assets/delivery_content_9.png)

* Wählen Sie aus der Dropdown-Liste **Feld** das Datenbankfeld aus, das dem Formularfeld zugeordnet werden soll.
* Wenn die Option **Pflichtfeld** aktiviert ist, kann der Nutzer das Formular nicht absenden, ohne dieses Feld ausgefüllt zu haben. In diesem Fall wird eine Fehlermeldung angezeigt.

## Mapping der Formularfelder   {#mapping-form-fields}

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

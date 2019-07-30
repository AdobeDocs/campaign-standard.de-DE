---
title: Anmeldung mit zweifacher Bestätigung einrichten
seo-title: Anmeldung mit zweifacher Bestätigung einrichten
description: Anmeldung mit zweifacher Bestätigung einrichten
seo-description: Mit diesen Schritten können Sie über Landingpages in Adobe Campaign eine Anmeldung mit zweifacher Bestätigung einrichten.
page-status-flag: nie aktiviert
uuid: 23 e 6 c 4 c 2-e 2 c 7-472 f-b 616-36 a 95225 ac 1 d
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Kanäle
content-type: Referenz
topic-tags: landing-pages
discoiquuid: 1 a 24504 e -7 f 9 d -4297-b 39 e-c 5 f 085 b 0 f 388
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6dd0c32259d942a0fb790f345cd13800a57e814a

---


# Anmeldung mit zweifacher Bestätigung einrichten{#setting-up-a-double-opt-in-process}

## Über die Anmeldung mit zweifacher Bestätigung {#about-double-opt-in}

Die Anmeldung mit zweifacher Bestätigung zählt zu den Best Practices beim E-Mail-Versand. Die Plattform wird dadurch vor falschen oder ungültigen E-Mail-Adressen und Spambots geschützt, wodurch Spam-Beschwerden verhindert werden.

Das Prinzip dahinter ist folgendes: Der Besucher füllt ein Formular auf einer Online-Landingpage aus, erhält dann eine E-Mail und muss den Bestätigungs-Link anklicken, um die Anmeldung abzuschließen. Erst dann wird er als ‘Profil' in der Campaign-Datenbank gespeichert.

![](assets/optin_mechanism.png)

Gehen Sie dazu folgendermaßen vor:

1. Erstellen und publizieren Sie eine Landingpage, auf der sich Besucher registrieren und anmelden können. Diese Landingpage ist auf einer Website verfügbar. Besucher, die diese Landingpage ausfüllen und diese Informationen abschicken, werden in der Datenbank gespeichert, aber auf die ‘Blacklist‘ gesetzt, damit sie keine Nachrichten vor der endgültigen Bestätigung erhalten (siehe [Blacklists in Campaign verwenden](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)).
1. Erstellen und senden Sie automatisch die Anmelde-E-Mail mit einem Bestätigungs-Link. Diese E-Mail wird an die Personen gesendet, die ihre Informationen auf der Landingpage abgeschickt haben. Die E-Mail basiert auf einer E-Mail-Vorlage, mit der ‘abgemeldete’ Profile gehandhabt werden können.
1. Richten Sie eine Weiterleitung zu einer Bestätigungs-Landingpage ein. Diese abschließende Landingpage weist eine Bestätigungs-Schaltfläche auf, die die Besucher anklicken müssen. Sie können eine Willkommens-E-Mail erstellen, die nach Abschluss des Bestätigungsprozesses gesendet wird und beispielsweise ein spezielles Angebot für neue Empfänger enthält.

Diese Schritte müssen in Adobe Campaign in einer bestimmten Reihenfolge ausgeführt werden, damit alle Parameter ordnungsgemäß aktiviert werden.

## Schritt 1: Bestätigungs-Landingpage erstellen {#step-1--create-the-confirmation-landing-page}

Um eine Anmeldung mit zweifacher Bestätigung einzurichten, muss zunächst die Bestätigungs-Landingpage erstellt werden: Diese Seite wird angezeigt, wenn ein Besucher die Bestätigungs-E-Mail anklickt, um sich zu registrieren.

Um diese Landingpage zu erstellen und zu konfigurieren, gehen Sie folgendermaßen vor:

1. Erstellen Sie auf der Basis der Vorlage [](../../channels/using/about-landing-pages.md)Profilakquise (Akquise)**eine[!UICONTROL neue Landingpage.]** Geben Sie den Titel '**CONFIRMATION**‘ ein.

   Wenn Sie [Dienste](../../audiences/using/about-subscriptions.md) benötigen, können Sie auch die Vorlage **[!UICONTROL Abonnement (sub)]verwenden.**

1. Edit the landing page properties and under the **[!UICONTROL Access and loading]** section, unselect the option **[!UICONTROL Authorize unidentified visitors]**, select **[!UICONTROL Preload visitor data]** (this one is not mandatory).

   ![](assets/optin_confirmlp_param.png)

1. In the **[!UICONTROL Job]** &gt; **[!UICONTROL Additional data]** section, click **[!UICONTROL Add an element]** and enter the following context path:

   /context/profile/blackList

   Wählen Sie den Wert **Falsch** und danach **[!UICONTROL Hinzufügen aus]**.

   ![](assets/optin_confirmlp_newelement.png)

   Dadurch wird das Blacklist-Feld entfernt, sodass E-Mails gesendet werden können. Später werden wir sehen, dass die ursprüngliche Einstellung des Felds für die Landingpage vor der Bestätigung **Wahr** war, was den Versand von E-Mails an nicht bestätigte Profile verhindert hat. Weiterführende Informationen dazu finden Sie unter [Schritt 3: Akquise-Landingpage erstellen](../../channels/using/setting-up-a-double-opt-in-process.md#step-3--create-the-acquisition-landing-page).

1. Passen Sie den Inhalt der Landingpage an: Sie können personalisierte Daten anzeigen und den Titel der Bestätigungs-Schaltfläche beispielsweise in ‘Klicken Sie hier, um Ihre Anmeldung zu validieren’ ändern.

   ![](assets/optin_confirmlp_design.png)

1. Ändern Sie den Inhalt der Bestätigungsseite so, dass Ihre Abonnenten darüber informiert werden, dass sie registriert sind.

   ![](assets/optin_confimlp_page2.png)

1. [Testen und publizieren](../../channels/using/sharing-a-landing-page.md) Sie die Landingpage.

## Schritt 2: Bestätigungs-E-Mail erstellen {#step-2--create-the-confirmation-email}

Nachdem die Bestätigungs-Landingpage fertig ist, kann die Bestätigungs-E-Mail erstellt werden. Diese E-Mail wird automatisch jedem Besucher gesendet, der die Akquise-Landingpage bestätigt. Diese Bestätigung wird als Ereignis erachtet und die E-Mail gilt als Transaktionsnachricht, die mit einer bestimmten Typologieregel verknüpft ist, wodurch Abmeldungen gehandhabt werden können.

Die Schritte zur Erstellung dieser Elemente werden unten beschrieben. Führen Sie sie aus, bevor Sie die Akquise-Landingpage erstellen, da diese auf die E-Mail-Vorlage verweist.

### Ereignis erstellen {#create-the-event}

Die Bestätigungs-E-Mail ist eine [Transaktionsnachricht](../../channels/using/about-transactional-messaging.md), da sie auf ein Ereignis reagiert, nämlich die Bestätigung des Formulars. Erstellen Sie zuerst das Ereignis und danach die Vorlage der Transaktionsnachricht.

1. Create an event, from the **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]** &gt; **[!UICONTROL Event configuration]** menu, accessible from the Adobe Campaign logo, and enter the label '**CONFIRM**'.
1. Select the **[!UICONTROL Profile]** targeting dimension and click **[!UICONTROL Create]**.

   ![](assets/optin_eventcreate.png)

1. Wählen Sie im Bereich **[!UICONTROL Felder]** die Option **[!UICONTROL Element erstellen]aus und fügen Sie** E-Mail] in der Datenstruktur hinzu, um die Abstimmung zu aktivieren.**[!UICONTROL **
1. Wählen Sie im Bereich **[!UICONTROL Anreicherung]** die Option **[!UICONTROL Element erstellen]** und danach die Zielressource **Profil[!UICONTROL aus]**. Ordnen Sie dies dann im Bereich **** Definition des Joins] nach Bedarf der **[!UICONTROL E-Mail]oder einem anderen zusammengesetzten Abstimmschlüssel zu.[!UICONTROL **

   ![](assets/optin_eventcreate_join.png)

   Wenn Sie Dienste benötigen, können Sie auch **[!UICONTROL serviceName hinzufügen]**.

1. Wählen Sie in der Dropdown-Liste für die **[!UICONTROL Zielgruppen-Anreicherung]die Option****Profil[!UICONTROL .]**
1. Wählen Sie **[!UICONTROL Publizieren], um das Ereignis zu veröffentlichen.**

Das Ereignis ist somit fertig eingerichtet. Jetzt können Sie die E-Mail-Vorlage erstellen. Diese Vorlage muss einen Link zur zuvor erstellten Landingpage **CONFIRMATION** aufweisen. Weiterführende Informationen dazu finden Sie im Abschnitt [Bestätigungsnachricht erstellen](../../channels/using/setting-up-a-double-opt-in-process.md#design-the-confirmation-message).

### Typologieregel erstellen {#create-the-typology-rule}

Erstellen Sie eine eigene [Typologieregel](../../administration/using/about-typology-rules.md) durch Duplizieren einer vordefinierten Regel. Mit dieser Regel können Nachrichten an Profile gesendet werden, die ihre Anmeldung noch nicht bestätigt haben und noch auf der Blacklist stehen. Standardmäßig sind bei Typologieregeln abgemeldete Profile (d. h. Profile auf der Blacklist) ausgeschlossen. Gehen Sie wie folgt vor, um eine solche Typologieregel zu erstellen:

1. From the Adobe Campaign logo, select **[!UICONTROL Administration]** &gt; **[!UICONTROL Channels]** &gt; **[!UICONTROL Typologies]** and click **[!UICONTROL Typologies]**.
1. Duplizieren Sie die Standardtypologie **[!UICONTROL Transaktionsnachricht zum Profil (mcTypologyProfile)]**.
1. Bearbeiten Sie danach die neue Typologie und geben Sie den Titel **TYPOLOGY_PROFILE** ein.
1. Remove the **blacklisted address** rule.
1. Wählen Sie **[!UICONTROL Speichern aus]**.

Diese Typologie kann jetzt mit der Bestätigungs-E-Mail verknüpft werden.

### Bestätigungsnachricht erstellen {#design-the-confirmation-message}

Die Bestätigungs-E-Mail ist eine Transaktionsnachricht, die auf einem zuvor erstellen Ereignis basiert. Führen Sie die folgenden Schritte aus, um eine solche Nachricht zu erstellen:

1. From the Adobe Campaign logo, select **[!UICONTROL Marketing plans]** &gt; **[!UICONTROL Transactional messages]** and click **[!UICONTROL Transactional messages]**.
1. Bearbeiten Sie die E-Mail-Vorlage **CONFIRM** und personalisieren Sie sie. Sie können einen vorhandenen Inhalt hochladen oder eine Standardvorlage verwenden.
1. Fügen Sie einen Link zur Landingpage **CONFIRMATION** hinzu und wählen Sie dann **[!UICONTROL Validieren], um die Änderungen zu speichern.**

   ![](assets/optin_email_selectlp.png)

1. Bearbeiten Sie die Eigenschaften der E-Mail-Vorlage. In the **[!UICONTROL Advanced parameters]** &gt; **[!UICONTROL Preparation]** section, select the **TYPOLOGY_PROFILE** typology created before.
1. Speichern und publizieren Sie die Transaktionsnachricht.

## Schritt 3: Akquise-Landingpage erstellen {#step-3--create-the-acquisition-landing-page}

Erstellen Sie die ursprüngliche Akquise-Landingpage. Sie enthält ein Anmeldeformular, das daraufhin auf Ihrer Website veröffentlicht wird.

Um diese Landingpage zu erstellen und zu konfigurieren, gehen Sie folgendermaßen vor:

1. Erstellen Sie auf der Basis der Vorlage [](../../channels/using/about-landing-pages.md)Profilakquise (Akquise)**eine[!UICONTROL neue Landingpage.]** Geben Sie den Titel '**ACQUISITION**‘ ein.
1. Edit the landing page properties: in the **[!UICONTROL Job]** &gt; **[!UICONTROL Additional data]** section, click **[!UICONTROL Add an element]** and enter the following context path:

   /context/profile/blackList

   und wählen Sie den Wert **Wahr** aus.

   Dies ist nötig, damit Besucher, die ihre Anmeldung noch nicht bestätigt haben, auf die Blacklist gesetzt werden und keine Nachrichten erhalten. Durch die Validierung der CONFIRMATION-Landingpage erhält dieses Feld den Wert **Falsch**. Weiterführende Informationen dazu finden Sie unter [Schritt 1: Bestätigungs-Landingpage erstellen](../../channels/using/setting-up-a-double-opt-in-process.md#step-1--create-the-confirmation-landing-page).

1. In the **[!UICONTROL Job]** &gt; **[!UICONTROL Specific actions]** section, select the option **[!UICONTROL Start sending messages]**.
1. Wählen Sie in der dazugehörigen Dropdown-Liste die von Ihnen erstellte Transaktionsnachrichtenvorlage **CONFIRM** aus.

   ![](assets/optin_acquisition_startoption.png)

1. Passen Sie den Inhalt auf der Landingpage entsprechend Ihrer Marke und den von Ihnen benötigten Daten an. Sie können personalisierte Daten anzeigen und den Titel der Bestätigungs-Schaltfläche beispielsweise in **Anmeldung bestätigen** ändern.

   ![](assets/optin_acquisition_page1.png)

1. Passen Sie die Bestätigungsseite an, damit der neue Abonnent darüber informiert wird, dass er diese Anmeldung bestätigen muss.

   ![](assets/optin_acquisition_page2.png)

1. [Testen und publizieren](../../channels/using/sharing-a-landing-page.md) Sie die Landingpage.

Die Anmeldung mit zweifacher Bestätigung ist jetzt konfiguriert. Sie können diesen Vorgang von Anfang bis Ende ausführen und testen, indem Sie bei der öffentlichen URL dieser **[!UICONTROL ACQUISITION]-Landingpage beginnen.** Diese URL wird im Dashboard der Landingpage angezeigt.

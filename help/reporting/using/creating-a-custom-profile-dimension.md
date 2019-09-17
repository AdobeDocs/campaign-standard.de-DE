---
title: Benutzerdefinierte Profildimension erstellen
seo-title: Benutzerdefinierte Profildimension erstellen
description: Benutzerdefinierte Profildimension erstellen
seo-description: Hier erfahren Sie, wie Sie eine benutzerdefinierte Profildimension auf der Basis von benutzerdefinierten Profildaten erstellen können.
page-status-flag: never-activated
uuid: f75e005b-5328-4c98-9e78-51d54fd0e246
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: customizing-reports
discoiquuid: b6d3de63-3add-4881-8917-04a6f8b6be4d
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 4ad558fce83006879455a791127594157456f0c4

---


# Benutzerdefinierte Profildimension erstellen{#creating-a-custom-profile-dimension}

Berichte können auch auf der Basis von benutzerdefinierten Profildaten erstellt und verwaltet werden, die während der Erweiterung der benutzerdefinierten Ressource "Profil" erzeugt werden.

In diesem Beispiel erstellen wir das benutzerdefinierte Profilfeld **Treueprogramme**, das in drei Stufen unterteilt ist: Gold, Silber und Bronze. Dieses benutzerdefinierte Profil wird dann erweitert, damit es als eine benutzerdefinierte Profildimension in dynamischen Berichten verwendet werden kann.

* [Schritt 1: Erstellen Sie ein neues Profilfeld.](../../reporting/using/creating-a-custom-profile-dimension.md#step-1--create-a-new-profile-field)
* [Schritt 2: Erweitern Sie die Versandlogs mit dem Profilfeld.](../../reporting/using/creating-a-custom-profile-dimension.md#step-2--extend-the-sending-logs-with-the-profile-field)
* [Schritt 3: Erstellen Sie einen Versand an Empfänger, die am Treueprogramm teilnehmen.](../../reporting/using/creating-a-custom-profile-dimension.md#step-3--create-a-delivery-targeting-recipients-enrolled-in-the-loyalty-program)
* [Schritt 4: Erstellen Sie einen dynamischen Bericht, um Empfänger mithilfe der benutzerdefinierten Profildimension zu filtern.](../../reporting/using/creating-a-custom-profile-dimension.md#step-4--create-a-dynamic-report-to-filter-recipients-with-the-custom-profile-dimension)

## Schritt 1: Erstellen Sie ein neues Profilfeld.  {#step-1--create-a-new-profile-field}

Zunächst muss das neue Profilfeld **Treueprogramm** erstellt werden, mit dem unseren Empfängern eine Treuestufe zugewiesen wird: Gold, Silber oder Bronze.

>[!NOTE]
>
>Die Verwaltung benutzerdefinierter Ressourcen muss durch einen Administrator erfolgen.

Gehen Sie dabei folgendermaßen vor:

1. Wählen Sie im erweiterten Menü **[!UICONTROL Administration]** &gt; **[!UICONTROL Entwicklung]** &gt; **[!UICONTROL Benutzerdefinierte Ressourcen]** und dann die benutzerdefinierte Ressource **[!UICONTROL Profil (profile)]** aus.

   ![](assets/custom_profile_1.png)

1. Wählen Sie im Tab **[!UICONTROL Datenstruktur]** in der Kategorie **[!UICONTROL Felder]** die Schaltfläche **[!UICONTROL Feld hinzufügen]** aus.

   ![](assets/custom_profile_2.png)

1. Geben Sie den **[!UICONTROL Titel]** und die **[!UICONTROL Kennung]** ein und wählen Sie die benutzerdefinierte Ressource **[!UICONTROL Typ]** aus. In unserem Beispiel haben wir **[!UICONTROL Text]** ausgewählt, da die Empfänger die Wahl zwischen Gold, Silber und Bronze haben werden.

   ![](assets/custom_profile_3.png)

1. Wählen Sie das Symbol ![ aus, um Ihr Feld zu definieren.](assets/custom_profile_22.png)

   ![](assets/custom_profile_12.png)

1. Hier müssen die zulässigen Werte spezifiziert werden. Wählen Sie dazu die Option **[!UICONTROL Liste zulässiger Werte definieren]** aus und erstellen Sie jeden einzelnen Wert durch die Auswahl von **[!UICONTROL Element erstellen]**.

   ![](assets/custom_profile_13.png)

1. Geben Sie **[!UICONTROL Titel]** und **[!UICONTROL Wert]** ein und wählen Sie dann **[!UICONTROL Hinzufügen]** aus. Für unser Beispiel müssen die Werte "Gold", "Silber" und "Bronze" erstellt werden. Wählen Sie zum Abschluss **[!UICONTROL Bestätigen]** aus.

   ![](assets/custom_profile_14.png)

1. Wählen Sie den Tab **[!UICONTROL Bildschirmdefinition]** aus. Aktivieren Sie in der Dropdown-Liste **[!UICONTROL Konfiguration des Detailbildschirms]** die Option **[!UICONTROL Abschnitt mit Personalisierungsfeldern hinzufügen]**, um in unserem Profil einen neuen Bereich zu erstellen.

   ![](assets/custom_profile_4.png)

1. Wählen Sie die Schaltfläche **[!UICONTROL Element hinzufügen]** aus, um den neuen Bereich zu erstellen. Wählen Sie den **[!UICONTROL Typ]**: **[!UICONTROL Eingabefeld]**, **[!UICONTROL Wert]** oder **[!UICONTROL Liste]** und danach das in diesem neuen Bereich hinzuzufügende Feld.

   ![](assets/custom_profile_5.png)

1. Sie können auch einen Titel zu Ihrem Bereich hinzufügen, indem Sie ihn im Feld **[!UICONTROL Titel des Abschnitts anpassen, in dem die Felder angezeigt werden eingeben]**.

   Wählen Sie **[!UICONTROL Speichern]**, wenn die Konfiguration abgeschlossen ist.

   ![](assets/custom_profile_6.png)

1. Wählen Sie im erweiterten Menü **[!UICONTROL Administration]** &gt; **[!UICONTROL Entwicklung]** &gt; **[!UICONTROL Publikation]**, um Ihre benutzerdefinierte Ressource zu publizieren.
1. Wählen Sie **[!UICONTROL Publikation vorbereiten]** und nach Abschluss der Vorbereitung die Schaltfläche **[!UICONTROL Publizieren]**.

   ![](assets/custom_profile_7.png)

Ihr neues Profilfeld kann jetzt verwendet und von Empfängern ausgewählt werden.

![](assets/custom_profile_8.png)

## Schritt 2: Erweitern Sie die Versandlogs mit dem Profilfeld.  {#step-2--extend-the-sending-logs-with-the-profile-field}

Nach der Erstellung des Profilfeldes müssen die Versandlogs mit unserem Profilfeld erweitert werden, um die zugehörige benutzerdefinierte Profildimension in dynamischen Berichten zu verwenden.

Bevor das Log mit unserem Profilfeld erweitert werden kann, muss das PII-Fenster akzeptiert worden sein, um Zugriff auf den Tab **[!UICONTROL Erweiterung der Versandlogs]** zu erhalten. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

>[!NOTE]
>
>Die Erweiterung von Logs mit Profilfeldern muss durch einen Administrator erfolgen.

1. Wählen Sie im erweiterten Menü **[!UICONTROL Administration]** &gt; **[!UICONTROL Entwicklung]** &gt; **[!UICONTROL Benutzerdefinierte Ressourcen]** und dann die benutzerdefinierte Ressource **[!UICONTROL Profil (profile)]** aus.
1. Öffnen Sie die Dropdown-Liste **[!UICONTROL Erweiterung der Versandlogs]**.
1. Wählen Sie die Schaltfläche **[!UICONTROL Element erstellen]** aus.

   ![](assets/custom_profile_9.png)

1. Wählen Sie das zuvor von Ihnen erstellte Feld und danach **[!UICONTROL Bestätigen aus]**.
1. Aktivieren Sie die Option **[!UICONTROL Dieses Feld in dynamischen Berichten als neue Dimension hinzufügen]**, um Ihre benutzerdefinierte Profildimension zu erstellen.

   ![](assets/custom_profile_10.png)

   Diese Option ist nur verfügbar, wenn zuvor das PII-Fenster akzeptiert wurde. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

1. Wählen Sie **[!UICONTROL Hinzufügen]** aus und speichern Sie danach Ihre benutzerdefinierte Ressource.
1. Da die benutzerdefinierte Ressource verändert wurde, müssen wir sie publizieren, um die neuen Änderungen zu implementieren.

   Wählen Sie im erweiterten Menü **[!UICONTROL Administration]** &gt; **[!UICONTROL Entwicklung]** &gt; **[!UICONTROL Publikation]**, um Ihre benutzerdefinierte Ressource zu publizieren.

1. Wählen Sie **[!UICONTROL Publikation vorbereiten]** und nach Abschluss der Vorbereitung die Schaltfläche **[!UICONTROL Publizieren]**.

   ![](assets/custom_profile_7.png)

Ihr benutzerdefiniertes Profil ist jetzt als benutzerdefinierte Profildimension in Ihren Berichten verfügbar.

Nachdem Ihr Profilfeld erstellt und die Versandlogs damit erweitert wurden, können Sie für Ihre Nachrichten Zielgruppen auswählen.

## Schritt 3: Erstellen Sie einen Versand an Empfänger, die am Treueprogramm teilnehmen.  {#step-3--create-a-delivery-targeting-recipients-enrolled-in-the-loyalty-program}

Nachdem Ihr Profilfeld publiziert wurde, können Sie den Versand starten. In diesem Beispiel möchten wir jeden Empfänger, der am Treueprogramm teilnimmt, eine Nachricht senden.

1. Wählen Sie im Tab **[!UICONTROL Marketingaktivitäten]** die Option **[!UICONTROL Erstellen]** und dann **[!UICONTROL E-Mail]** aus.
1. Wählen Sie einen **[!UICONTROL E-Mail-Typ]** aus und geben Sie dann die Eigenschaften Ihrer E-Mail ein.
1. Um Teilnehmer am Treueprogramm auszuwählen, ziehen Sie die Aktivität **[!UICONTROL Profile (Attribute)]** in den Arbeitsbereich.
1. Wählen Sie das zuvor von Ihnen erstellte Feld aus der Dropdown-Liste **[!UICONTROL Feld]** aus.

   ![](assets/custom_profile_16.png)

1. Wählen Sie die gewünschten **[!UICONTROL Filterbedingungen]** aus. Hier möchten wir Empfänger ansprechen, die an einem der drei Stufen des Treueprogramms teilnehmen.

   ![](assets/custom_profile_17.png)

1. Wählen Sie nach der Definition des Filters **[!UICONTROL Bestätigen]** und danach **[!UICONTROL Weiter]**.
1. Definieren und personalisieren Sie den Nachrichteninhalt, den Absendernamen und den Betreff. Weiterführende Informationen zur Erstellung von E-Mails finden Sie auf dieser [Seite](../../designing/using/overview.md).

   Wählen Sie dann **[!UICONTROL Erstellen aus]**.

1. Danach können Sie sich Ihre Nachricht in der Vorschau ansehen und diese senden. Weiterführende Informationen zum Vorbereiten und Senden einer Nachricht finden Sie auf [dieser Seite](../../sending/using/preparing-the-send.md).

Nachdem Ihre E-Mail an die ausgewählten Empfänger gesendet wurde, können Sie Ihre Daten filtern und die Wirkung des Versands in Berichten überprüfen.

## Schritt 4: Erstellen Sie einen dynamischen Bericht, um Empfänger mithilfe der benutzerdefinierten Profildimension zu filtern.  {#step-4--create-a-dynamic-report-to-filter-recipients-with-the-custom-profile-dimension}

Nach dem Versand Ihrer Nachricht können Sie die Berichte mithilfe Ihrer benutzerdefinierten Profildimension in der Tabelle **[!UICONTROL Profil]** aufschlüsseln.

1. Wählen Sie im Tab **[!UICONTROL Berichte]** einen vordefinierten Bericht oder die Schaltfläche **[!UICONTROL Erstellen]**, um einen neuen Bericht zu erstellen.

   ![](assets/custom_profile_18.png)

1. Wählen Sie in der Kategorie **[!UICONTROL Dimensionen]** die Option **[!UICONTROL Profil]** aus und ziehen Sie die benutzerdefinierte Profildimension **Treueprogramm** in Ihre Freiformtabelle.

   ![](assets/custom_profile_19.png)

1. Ziehen Sie die Metriken **[!UICONTROL Verarbeitet/gesendet]** und **[!UICONTROL Öffnungen]** in den Arbeitsbereich, um mit der Filterung Ihrer Daten zu beginnen.

   ![](assets/custom_profile_20.png)

1. Ziehen Sie bei Bedarf ein Visualisierungselement in den Arbeitsbereich.

   ![](assets/custom_profile_21.png)

**Verwandtes Thema:**

* [Verwenden benutzerdefinierter Profildaten zum Erstellen von aufschlussreichen Berichten](https://helpx.adobe.com/campaign/kb/simplify-campaign-management.html#Reportandshareinsightswithallstakeholders)

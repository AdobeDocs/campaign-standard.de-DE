---
solution: Campaign Standard
product: campaign
title: Profile erstellen
description: Hier erfahren Sie, wie Sie Profile erstellen und mithilfe von APIs Daten zu Ihren Kontakten erheben. Lernen Sie außerdem den Gebrauch von Importfunktionen, die Umsetzung von Online-Akquise-Strategien sowie die automatische oder manuelle Aktualisierung Ihrer Daten.
audience: audiences
content-type: reference
topic-tags: managing-profiles
translation-type: tm+mt
source-git-commit: 2a92600df01fd3c78a2b35c8034a2ce347e5c1d8
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 92%

---


# Profile erstellen{#creating-profiles}

In Adobe Campaign dienen Profile standardmäßig der Bestimmung der Hauptzielgruppe einer Marketingkommunikation.

>[!NOTE]
>
>Die Erstellung von Profilen ist auch mithilfe der Adobe Campaign Standard API möglich. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../api/using/creating-profiles.md).

![](assets/do-not-localize/how-to-video.png) [Entdecken Sie, wie Sie Profile mit einem Videoworkflow importieren](#video)

Ein Profil kann in Campaign folgendermaßen erstellt oder aktualisiert werden:

* Import einer Profilliste von einer Datei über einen [Workflow](../../automating/using/creating-import-workflow-templates.md)
* Datenerhebung online über [Landingpages](../../channels/using/getting-started-with-landing-pages.md)
* Im Bulk-Modus über die [REST-API](../../api/using/get-started-apis.md)
* Synchronisieren von Profilen in [Microsoft Dynamics](../../integrating/using/working-with-campaign-standard-and-microsoft-dynamics-365.md)
* Direkte Dateneingabe über die Benutzeroberfläche, wie unten beschrieben

Hier ist ein Beispiel dafür, wie Sie ein neues Profil direkt in der Benutzeroberfläche erstellen können. Gehen Sie dazu folgendermaßen vor:

1. Öffnen Sie auf der Adobe-Campaign-Startseite die Karte **Kundenprofile** oder den Tab **Profile**, um die Profilliste aufzurufen.

   ![](assets/profile_creation_1.png)

1. Wählen Sie **[!UICONTROL Erstellen]** aus.

   ![](assets/profile_creation.png)

1. Machen Sie die erforderlichen Angaben zum Profil.

   ![](assets/profile_creation1.png)

   * Die Kontaktinformationen, darunter Vorname, Nachname, Geschlecht, Geburtsdatum, Foto oder bevorzugte Sprache (für [mehrsprachige E-Mails](../../channels/using/creating-a-multilingual-email.md)), ermöglichen eine stärkere Personalisierung von Nachrichten.
   * Die Angabe zur **[!UICONTROL Zeitzone]** wird verwendet, um den Versand auf die Zeitzone des Profils abzustimmen. Weiterführende Informationen hierzu finden Sie in diesem [Abschnitt](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md).
   * In der Kategorie **[!UICONTROL Kanäle]** sind die E-Mail-Adresse, Mobiltelefonnummer und Opt-out-Informationen aufgeführt. Hier lässt sich ermitteln, über welche Kanäle Sie das Profil erreichen können.
   * Die Informationen in der Kategorie **[!UICONTROL Nicht mehr kontaktieren]** werden aktualisiert, sobald sich das Profil von einem Kanal abmeldet.
   * In der Kategorie **[!UICONTROL Adresse]** wird die Anschrift festgehalten. Diese muss ausgefüllt und die Option **[!UICONTROL Anschrift angegeben]** aktiviert sein, wenn [Briefpost](../../channels/using/about-direct-mail.md) an dieses Profil versendet werden soll. Ist die Option **[!UICONTROL Anschrift angegeben]** nicht aktiviert, wird dieses Profil vom Briefpostversand ausgeschlossen.
   * In der Kategorie **[!UICONTROL Zugriffsberechtigung]** sind die Organisationseinheiten des Profils festgehalten, um die [Berechtigungen zu verwalten](../../administration/using/about-access-management.md). Informationen zum Hinzufügen der Organisationsfelder zu Profilen finden Sie im Abschnitt [Profile partitionieren](../../administration/using/organizational-units.md#partitioning-profiles).
   * In der Kategorie **[!UICONTROL Rückverfolgung]** werden automatisch Informationen zu dem Benutzer aktualisiert, der das Profil erstellt oder geändert hat.

1. Speichern Sie das Profil mithilfe der Schaltfläche **[!UICONTROL Erstellen]**.

Das Profil wurde der Liste hinzugefügt.

>[!NOTE]
>Das Feld &quot;Bevorzugte Sprache&quot; wird verwendet, um beim Versand mehrsprachiger Nachrichten die Sprache auszuwählen. Weiterführende Informationen zu mehrsprachigen Nachrichten [finden Sie auf dieser Seite](../../channels/using/creating-a-multilingual-email.md).

## Tutorial-Video {#video}

In diesem Video wird gezeigt, wie Profil mit einem Workflow importiert werden.

>[!VIDEO](https://video.tv.adobe.com/v/24993?quality=12)

Weitere Anleitungen zu Campaign Standards finden Sie unter [hier](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/overview.html?lang=de).

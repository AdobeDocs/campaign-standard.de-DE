---
title: Profile erstellen
description: Hier erfahren Sie, wie Sie Profile erstellen und mithilfe von APIs Daten zu Ihren Kontakten erheben. Lernen Sie außerdem den Gebrauch von Importfunktionen, die Umsetzung von Online-Akquise-Strategien sowie die automatische oder manuelle Aktualisierung Ihrer Daten.
audience: audiences
content-type: reference
topic-tags: managing-profiles
feature: Profiles
role: User
level: Beginner
exl-id: 827df9f6-070c-466a-890c-e363de6b129b
TQID: https://experienceleague.adobe.com/STHpDRtsdjT7OMDg3aOtVHdzqLokzOxvM2PI0ho9WLA
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2:
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
subfeature_v2:
  - id: bf97c196-a4d1-4fa3-a151-e68a114c8ac0
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 411
ht-degree: 100%

---

# Profile erstellen{#creating-profiles}

In Adobe Campaign dienen Profile standardmäßig der Bestimmung der Hauptzielgruppe einer Marketingkommunikation.

>[!NOTE]
>
>Die Erstellung von Profilen ist auch mithilfe der Adobe Campaign Standard API möglich. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../api/using/creating-profiles-api.md).

![](assets/do-not-localize/how-to-video.png) [Erfahren Sie im Video, wie man Profile mit einem Workflow importiert](#video)

Ein Profil kann in Campaign folgendermaßen erstellt oder aktualisiert werden:

* Import einer Profilliste von einer Datei über einen [Workflow](../../automating/using/creating-import-workflow-templates.md)
* Datenerhebung online über [Landingpages](../../channels/using/getting-started-with-landing-pages.md)
* Im Bulk-Modus über die [REST-API](../../api/using/get-started-apis.md)
* Synchronisieren von Profilen in [Microsoft Dynamics](../../integrating/using/d365-acs-get-started.md)
* Geben Sie Daten wie unten beschrieben über die Benutzeroberfläche ein

Hier ist ein Beispiel dafür, wie Sie ein neues Profil direkt in der Benutzeroberfläche erstellen können. Gehen Sie dazu folgendermaßen vor:

1. Öffnen Sie auf der Adobe Campaign-Startseite die Karte **Kundenprofile** oder den Tab **Profile**, um die Profilliste aufzurufen.

   ![](assets/profile_creation_1.png)

1. Wählen Sie **[!UICONTROL Erstellen]** aus.

   ![](assets/profile_creation.png)

1. Machen Sie die erforderlichen Angaben zum Profil.

   ![](assets/profile_creation1.png)

   * Die Kontaktinformationen, darunter Vorname, Nachname, Geschlecht, Geburtsdatum, Foto oder bevorzugte Sprache (für [mehrsprachige E-Mails](../../channels/using/creating-a-multilingual-email.md)), ermöglichen eine stärkere Personalisierung von Nachrichten.
   * Die Angabe zur **[!UICONTROL Zeitzone]** wird verwendet, um den Versand auf die Zeitzone des Profils abzustimmen. Weiterführende Informationen hierzu finden Sie in diesem [Abschnitt](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md).
   * In der Kategorie **[!UICONTROL Kanäle]** sind die E-Mail-Adresse, Mobiltelefonnummer und Opt-out-Informationen aufgeführt. Hier lässt sich ermitteln, über welche Kanäle Sie das Profil erreichen können.

     >[!NOTE]
     > Mobiltelefonnummern müssen in der Profiltabelle immer im internationalen Format (`+<country><number>`) angegeben werden.

   * Die Informationen in der Kategorie **[!UICONTROL Nicht mehr kontaktieren]** werden aktualisiert, sobald sich das Profil von einem Kanal abmeldet.
   * In der Kategorie **[!UICONTROL Adresse]** wird die Anschrift festgehalten. Diese muss ausgefüllt und die Option **[!UICONTROL Anschrift angegeben]** aktiviert sein, wenn [Briefpost](../../channels/using/about-direct-mail.md) an dieses Profil versendet werden soll. Ist die Option **[!UICONTROL Anschrift angegeben]** nicht aktiviert, wird dieses Profil vom Briefpostversand ausgeschlossen.
   * In der Kategorie **[!UICONTROL Zugriffsberechtigung]** sind die Organisationseinheiten des Profils festgehalten, um die [Berechtigungen zu verwalten](../../administration/using/about-access-management.md). Informationen zum Hinzufügen der Organisationsfelder zu Profilen finden Sie im Abschnitt [Profile partitionieren](../../administration/using/organizational-units.md#partitioning-profiles).
   * In der Kategorie **[!UICONTROL Rückverfolgung]** werden automatisch Informationen zu dem Benutzer aktualisiert, der das Profil erstellt oder geändert hat.

1. Speichern Sie das Profil mithilfe der Schaltfläche **[!UICONTROL Erstellen]**.

Das Profil wurde der Liste hinzugefügt.

>[!NOTE]
>Das Feld &quot;Bevorzugte Sprache&quot; wird verwendet, um beim Versand mehrsprachiger Nachrichten die Sprache auszuwählen. Weiterführende Informationen zu mehrsprachigen Nachrichten [finden Sie auf dieser Seite](../../channels/using/creating-a-multilingual-email.md).

## Anleitungsvideo {#video}

In diesem Video wird gezeigt, wie man Profile mit einem Workflow importiert.

>[!VIDEO](https://video.tv.adobe.com/v/30222?captions=ger&quality=12)

Weitere Anleitungsvideos zu Campaign Standard finden Sie [hier](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/overview.html?lang=de).

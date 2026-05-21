---
title: Landingpage freigeben
description: Hier erfahren Sie, wie Sie eine Landingpage in Adobe Campaign testen und veröffentlichen können.
audience: channels
content-type: reference
topic-tags: landing-pages
feature: Landing Pages
role: User
level: Intermediate
exl-id: af849377-686f-45b3-bf6e-5069a8966987
TQID: https://experienceleague.adobe.com/8RZopDxY3R2f-67RtWyh7xRwD6-c2BhR-tEmEeLGO3Y
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 389
ht-degree: 100%

---

# Landingpage testen und veröffentlichen{#testing-publishing--landing-page}

## Über die Veröffentlichung von Landingpages {#about-landing-page-publication}

Vor der Veröffentlichung einer Landingpage müssen Sie Tests durchführen: Validieren Sie die Ausführung, konfigurieren Sie den Zugriff darauf und legen Sie das Funktionsende der Landingpage fest. Diese Maßnahmen sind erforderlich und müssen mit Sorgfalt ausgeführt werden.

## Landingpage testen {#testing-the-landing-page-}

Da die Landingpage Auswirkungen auf Ihre Plattform und Ihre Daten hat, muss sie sorgfältig getestet werden. Gehen Sie dazu wie folgt vor:

1. Verwenden Sie hierzu die Schaltfläche **[!UICONTROL Testen]** in der Aktionsleiste der Landingpage.
1. Wenn auf der Landingpage Abonnements verarbeitet werden sollen, wählen Sie auf dem Testbildschirm ein Testprofil und einen Testdienst.

   ![](assets/lp_test_2.png)

1. Geben Sie in den Feldern Daten ein und wählen Sie Optionen aus.
1. Übermitteln Sie die Landingpage und prüfen Sie die entsprechenden Aktualisierungen in der Datenbank.

   >[!IMPORTANT]
   >
   >Wenn das Formular übermittelt wird, werden der Dienst und das Profil aktualisiert.

1. Wiederholen Sie diesen Vorgang mit verschiedenen Profilen und Daten.

Bei Bedarf können Sie in diesem Bildschirm auch eine Miniaturansicht der Landingpage erzeugen.

>[!NOTE]
>
>Um die Vorschau der Landingpage in der Campaign-Benutzeroberfläche anzuzeigen, muss die URL des Anwendungs-Servers sicher sein. Verwenden Sie in diesem Fall https:// anstelle von http://, um diese URL beim [Konfigurieren Ihrer Marke](../../administration/using/branding.md#configuring-and-using-brands) einzurichten.

## Gültigkeitsparameter einrichten {#setting-up-validity-parameters}

Wir empfehlen dringend, aus Gründen der Sicherheit und der Plattform-Performance vor der Veröffentlichung in den Eigenschaften der Landingpage ein Ablaufdatum einzurichten. Bei Erreichen des angegebenen Datums wird die Veröffentlichung der Landingpage automatisch aufgehoben. Gehen Sie dazu wie folgt vor:

1. Bearbeiten Sie die Landingpage-Eigenschaften über die Schaltfläche ![](assets/edit_darkgrey-24px.png) im Landingpage-Dashboard.

   ![](assets/lp_edit_properties_button.png)

1. Definieren Sie im Bereich **[!UICONTROL Veröffentlichung]** das Ablaufdatum und die entsprechende Uhrzeit. Die Veröffentlichung der Landingpage wird automatisch am angegebenen Datum aufgehoben und sie ist dann nicht mehr verfügbar.

   Sie können die Zeitzone auswählen, die für dieses Datum und die Uhrzeit berücksichtigt werden soll.

1. Definieren Sie eine Weiterleitungs-URL, um die Besucher weiterzuleiten, die versuchen, auf eine nicht aktive Landingpage zuzugreifen.

   ![](assets/lp_settings_general.png)

>[!IMPORTANT]
>
>Sie können auch ein Bereitstellungsdatum und die entsprechende Uhrzeit definieren. Die Landingpage wird dann automatisch am angegebenen Datum veröffentlicht.

## Landingpage veröffentlichen {#publishing-a-landing-page}

Wenn Sie eine Landingpage veröffentlichen, ist sie online für Besucher verfügbar.

Die Aufhebung der Veröffentlichung einer Landingpage bzw. ihre Aktualisierung ist jederzeit über die Schaltfläche **[!UICONTROL Veröffentlichen]** möglich. Wenn vor der erneuten Veröffentlichung die Veröffentlichung der Landingpage nicht aufgehoben wurde und ein Fehler auftritt, bleibt die erste Version online.

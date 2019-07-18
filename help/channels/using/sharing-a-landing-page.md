---
title: Landingpage freigeben
seo-title: Landingpage freigeben
description: Landingpage freigeben
seo-description: Hier erfahren Sie, wie Sie eine Landingpage in Adobe Campaign testen und publizieren können.
page-status-flag: nie aktiviert
uuid: fb 7 b 087 a -3292-496 c-bc 41-2 e 3012 bacf 59
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Kanäle
content-type: Referenz
topic-tags: landing-pages
discoiquuid: f 7 d 4 bb 71-f 957-4 f 86-97 c 7-8 ac 0 a 0030026
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Landingpage freigeben{#sharing-a-landing-page}

## Über die Publikation von Landingpages {#about-landing-page-publication}

Vor der Publikation einer Landingpage müssen Sie Tests durchführen: Validieren Sie die Ausführung, konfigurieren Sie den Zugriff darauf und legen Sie das Funktionsende der Landingpage fest. Diese Maßnahmen sind erforderlich und müssen mit Sorgfalt ausgeführt werden.

## Landingpage testen {#testing-the-landing-page-}

Da die Landingpage Auswirkungen auf Ihre Plattform und Ihre Daten hat, muss sie sorgfältig getestet werden. Gehen Sie wie folgt vor:

1. Verwenden Sie hierzu die Schaltfläche **[!UICONTROL Testen]in der Symbolleiste der Landingpage.**
1. Wenn auf der Landingpage Abonnements verarbeitet werden sollen, wählen Sie auf dem Testbildschirm ein Testprofil und einen Testdienst.

   ![](assets/lp_test_2.png)

1. Geben Sie in den Feldern Daten ein und wählen Sie Optionen aus.
1. Übermitteln Sie die Landingpage und prüfen Sie die entsprechenden Aktualisierungen in der Datenbank.

   >[!CAUTION]
   >
   >Wenn das Formular übermittelt wird, werden der Dienst und das Profil aktualisiert.

1. Wiederholen Sie diesen Vorgang mit verschiedenen Profilen und Daten.

   Bei Bedarf können Sie in diesem Bildschirm auch eine Miniaturansicht der Landingpage erzeugen.

## Gültigkeitsparameter einrichten {#setting-up-validity-parameters}

Wir empfehlen dringend, aus Gründen der Sicherheit und der Plattform-Leistung vor der Publikation in den Eigenschaften der Landingpage ein Ablaufdatum einzurichten. Bei Erreichen des angegebenen Datums wird die Landingpage automatisch offline gestellt. Gehen Sie wie folgt vor:

1. Bearbeiten Sie die Landingpage-Eigenschaften über die Schaltfläche ![ im Landingpage-Dashboard.](assets/edit_darkgrey-24px.png)

   ![](assets/lp_edit_properties_button.png)

1. Definieren Sie im Bereich **[!UICONTROL Publikation]das Ablaufdatum und die entsprechende Uhrzeit. Die Landingpage wird automatisch am angegebenen Datum depubliziert und ist dann nicht mehr verfügbar.**

   Sie können die Zeitzone auswählen, die für dieses Datum und die Uhrzeit berücksichtigt werden soll.

1. Definieren Sie eine Weiterleitungs-URL, um die Besucher weiterzuleiten, die versuchen, auf eine nicht aktive Landingpage zuzugreifen.

   ![](assets/lp_settings_general.png)

>[!CAUTION]
>
>Sie können auch ein Publikationsdatum und die entsprechende Uhrzeit definieren. Die Landingpage wird dann automatisch am angegebenen Datum publiziert.

## Landingpage publizieren {#publishing-a-landing-page}

Wenn Sie eine Landingpage publizieren, ist sie online für Besucher verfügbar.

Eine Landingpage-Depublizierung bzw. -Aktualisierung ist jederzeit über die Schaltfläche **[!UICONTROL Publizieren]möglich.** Wenn vor der erneuten Publikation die Landingpage nicht depubliziert wurde und ein Fehler auftritt, bleibt die erste Version online.

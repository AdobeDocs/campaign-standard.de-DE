---
solution: Campaign Standard
product: campaign
title: Integriertes Kundenprofil
description: '"Sie können alle Kundeninteraktionen in einer gemeinsamen Übersicht verfolgen: Das integrierte Kundenprofil von Adobe Campaign wird während des gesamten Lebenszyklus eines Kunden aktualisiert."'
audience: audiences
content-type: reference
topic-tags: managing-profiles
context-tags: marketingHistory,main
translation-type: tm+mt
source-git-commit: b3088ed3bbb8828393e28df8f982ed36e7e74590
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 48%

---


# Integriertes Kundenprofil{#integrated-customer-profile}

Für jeden Kontakt in Ihrer Datenbank ist ein integriertes Kundenprofil verfügbar. In diesem Marketingverlauf finden Sie die wichtigsten Marketinginformationen zu einem Kundenkontakt in einer einzigen Ansicht zusammengefasst. Somit haben Sie von einer zentralen Stelle aus Zugriff auf alle Online-Verhaltensdaten: Kontaktinformationen, erhaltene E-Mails, Trackinglogs, An- und Abmeldungen etc.

Um auf das integrierte Kundenprofil zuzugreifen, gehen Sie folgendermaßen vor:

1. Klicken Sie in der Startseite &quot;Adobe Campaign&quot;auf die Karte **[!UICONTROL Kundendaten]** oder auf die Registerkarte **Profil**, um die Liste der Profil anzuzeigen.

1. Um ein Profil anhand eines bestimmten Felds zu suchen, öffnen Sie den Suchbereich und wählen Sie das Feld aus, in dem Sie die Suche durchführen möchten.


   ![](assets/profile-search.png)

1. Geben Sie den zu suchenden Wert an und drücken Sie dann die Eingabetaste.

   >[!NOTE]
   >
   >Beachten Sie, dass Suchvorgänge auf Basis der Felder für E-Mail, Vorname und Nachname sowie der benutzerdefinierten Felder durchgeführt werden können, die beim Erweitern der Ressource hinzugefügt wurden.
   >
   >Bei Suchvorgängen wird die Groß-/Kleinschreibung beachtet und nur bei Präfixen ausgeführt. So können Sie z. B. nicht mit den letzten Briefen seines Nachnamens nach einem Profil suchen.

1. Wählen Sie einen Kontakt aus, um sein Profil zu öffnen.

   ![](assets/mkt_hist_access.png)

Sie werden zum **Marketingverlauf** des Profils weitergeleitet.

Auf dieser Seite werden Schlüsselinformationen zum Profil sowie die Liste der Ereignisse erfasst.

Klicken Sie auf ein Ereignis in der Liste, um es zu öffnen: Sie können auf die Nachrichten zugreifen, die gesendet wurden, oder auf die Dienste, die das Profil abonniert hat.

![](assets/mkt_hist_view.png)

>[!NOTE]
>
>Der Marketingverlauf kann auch über die Adobe Campaign Standard API aufgerufen werden. Weiterführende Informationen finden Sie in der [entsprechenden Dokumentation](../../api/using/interacting-with-marketing-history.md).

---
title: Aktualisieren der Bounce-Qualifizierung nach einem ISP-Ausfall
description: Erfahren Sie, wie Sie die Bounce-Qualifizierung nach einem ISP-Ausfall aktualisieren.
audience: delivery
exl-id: b06e9009-70c7-459f-8a9f-d5b7020d662f
TQID: https://experienceleague.adobe.com/PcNbVFzTVJhadANGQ5uogj16VHiaNIf7HVn-7X-EbJA
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 77a1b72042c178fd56fefb639aba2674d85c9caa
workflow-type: tm+mt
source-wordcount: 450
ht-degree: 100%

---

# Aktualisieren der Bounce-Qualifizierung nach einem ISP-Ausfall {#update-bounce-qualification.md}

## Kontext

Bei Ausfall eines ISP können über Campaign versendete E-Mails nicht erfolgreich an ihren Empfänger zugestellt werden: Diese E-Mails werden fälschlicherweise als Bounces markiert.

Im Dezember 2020 führte ein globales Problem bei Gmail dazu, dass einige E-Mail-Nachrichten, die an gültige Gmail-Adressen gesendet wurden, von Gmail-Servern fälschlicherweise als ungültige E-Mail-Adressen mit der folgenden Bounce-Antwort zurückgewiesen wurden: *„550-5.1.1 Das E-Mail-Konto, das Sie zu erreichen versucht haben, existiert nicht“*.

Google hat angegeben, dass die Ausfälle und Unterbrechungen von Gmail, die dieses Problem verursacht haben, am 14. Dezember um 6:55AM Uhr und am 15. Dezember um 6:09PM Uhr EST endeten. Unsere Datenanalyse zeigte auch einen sehr kurzen Anstieg der Gmail-Bounce-Nachrichten um 2:06AM Uhr EST am 16. Dezember, wobei der Großteil am 15. Dezember zwischen 14:00 Uhr EST und 18:30 Uhr EST stattfand.

>[!NOTE]
>
>Sie können das Google Workspace-Status-Dashboard auf [dieser Seite](https://www.google.com/appsstatus#hl=de&v=status) überprüfen.


Gemäß der Standardlogik für die Behandlung von Bounces hat Adobe Campaign diese Empfänger automatisch der Quarantäneliste mit dem **[!UICONTROL Status]** **[!UICONTROL Quarantäne]** hinzugefügt. Um dies zu korrigieren, müssen Sie Ihre Quarantänetabelle in Campaign aktualisieren, indem Sie diese Empfänger finden und entfernen oder ihren **[!UICONTROL Status]** auf **[!UICONTROL Gültig]** ändern, damit der nächtliche Bereinigungs-Workflow sie entfernt.

Um die Empfänger zu finden, die von diesem Gmail-Problem betroffen waren, oder für den Fall, dass dies bei einem anderen ISP erneut auftritt, lesen Sie bitte die folgenden Anweisungen.

## Aktualisierungsprozess

Sie müssen eine Abfrage in Ihrer Quarantäne-Tabelle ausführen, um alle Gmail-Empfänger (oder Empfänger anderer ISPs) herauszufiltern, die möglicherweise von dem Ausfall betroffen waren, damit sie aus der Quarantäneliste entfernt und in zukünftige E-Mail-Sendungen von Campaign aufgenommen werden können.

Auf der Grundlage des Zeitrahmens des Vorfalls werden im Folgenden die Richtlinien für diese Abfrage empfohlen.

>[!IMPORTANT]
>
>Diese Daten/Zeiten basieren auf der Eastern Standard Zeitzone (EST). Bitte passen Sie die Zeitzone Ihrer Instanz an.

Für Campaign-Instanzen mit SMTP-Bounce-Antwortinformationen im Feld **[!UICONTROL Fehlertext]** der Quarantäneliste:

* **Fehlertext (Quarantänetext)** enthält „550-5.1.1 Das E-Mail-Konto, das Sie zu erreichen versucht haben, existiert nicht“ UND **Fehlertext (Quarantänetext)** enthält „support.google.com“ **
* **Statusaktualisierung (@lastModified)** später als 14.12.2020 6:55:00 Uhr
* **Statusaktualisierung (@lastModified)** früher als 16.12.2020 6:00:00 Uhr

Sobald Sie die Liste der betroffenen Empfänger haben, können Sie diese entweder auf den Status **[!UICONTROL Gültig]** setzen, damit sie vom Workflow **[!UICONTROL Datenbankbereinigung]** aus der Quarantäneliste entfernt werden, oder sie einfach aus der Tabelle löschen.

**Verwandte Themen:**

* [Ursachen für das Fehlschlagen von Sendungen](../../sending/using/understanding-delivery-failures.md)
* [Bounce-Message-Qualifizierung](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification)



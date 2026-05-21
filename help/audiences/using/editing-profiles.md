---
title: Profile bearbeiten
description: Erfahren Sie, wie Sie vorhandene Profile bearbeiten und auf Kontaktinformationen, bevorzugte Kanäle, Trackinglogs, Abonnements usw. zugreifen.
audience: audiences
content-type: reference
topic-tags: managing-profiles
feature: Profiles
role: User
level: Intermediate
exl-id: d0c7dc09-6f2b-4336-b545-7afe3a704164
TQID: https://experienceleague.adobe.com/hTCybEq1Hfh1fxXd5JGjRWmGZXzXNebtf42NZnEMZ5c
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2:
  - id: b12f6872-9271-4369-85e5-86969a0b99a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 100%

---

# Profile bearbeiten{#editing-profiles}

## Auf Profileigenschaften zugreifen {#accessing-profile-properties}

Gehen Sie wie folgt vor, um ein bereits existierendes Profil zu bearbeiten bzw. seine Daten einzusehen, oder es zu ändern:

1. Öffnen Sie auf der Adobe Campaign-Startseite die Karte **[!UICONTROL Kundenprofile]** oder den Tab **[!UICONTROL Profile]**.
1. Wählen Sie einen Kontakt aus.
1. Greifen Sie über das Symbol **[!UICONTROL Profileigenschaften bearbeiten]** auf die Profilinformationen zu.

   ![](assets/profile_creation2.png)

   Das Fenster der Profileigenschaften enthält mehrere Tabs, mit denen auf alle Profilinformationen zugegriffen werden kann:

   Je nach benutzerdefinierten Ressourcen, die in Adobe Campaign erstellt oder erweitert wurden, stehen mitunter weitere Tabs zur Verfügung. Weiterführende Informationen zu benutzerdefinierten Ressourcen finden Sie in [Über benutzerdefinierte Ressourcen](../../developing/using/data-model-concepts.md).

   >[!NOTE]
   >
   >Mit Ausnahme des Bereichs **[!UICONTROL Rückverfolgung]** können Sie nur die Informationen im Tab **[!UICONTROL Allgemein]** ändern.

Die Bearbeitung von Profilen ist auch mit der Adobe Campaign Standard API möglich. Weiterführende Informationen finden Sie in der [entsprechenden Dokumentation](../../api/using/updating-profiles.md).

Verwandtes Thema:

* [Integriertes Kundenprofil](../../audiences/using/integrated-customer-profile.md)
* [In der Zeitzone des Empfängers senden](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)

## Allgemeine Profildaten {#general-profile-data}

Der Tab **[!UICONTROL Allgemein]** enthält die folgenden Informationen zum Profil:

* Kontaktinformationen wie Vorname, Nachname, Geburtsdatum, Foto, bevorzugte Sprache (für [mehrsprachige E-Mails](../../channels/using/creating-a-multilingual-email.md)) usw. des Empfängers.
* Kanäle, über die das Profil kontaktiert werden kann, d. h. E-Mail-Adresse, Mobiltelefonnummer und zugehörige Opt-out-Informationen.
* Anschrift (für [Briefpost](../../channels/using/about-direct-mail.md)) und die Zeitzone des Kontakts (um [Nachrichten in seiner Zeitzone zu terminieren](../../sending/using/sending-messages-at-the-recipient-s-time-zone.md)).
* Zugriffsberechtigung, in der die Organisationseinheit des Empfängers festgehalten ist (zur [Verwaltung von Berechtigungen](../../administration/using/about-access-management.md)). Siehe auch [Profile partitionieren](../../administration/using/organizational-units.md#partitioning-profiles).

![](assets/profile_creation4.png)

## Versand- und Trackinglogs {#sending-and-tracking-logs}

In den Tabs **[!UICONTROL Versandlogs]** und **[!UICONTROL Trackinglogs]** sind alle Sendungen an das Profil sowie alle zugehörigen Trackingdaten enthalten.

Weiterführende Informationen zu Versand- und Trackinglogs finden Sie in den Abschnitten [Versandlogs](../../sending/using/monitoring-a-delivery.md#delivery-logs) und [Nachrichten tracken](../../sending/using/tracking-messages.md).

## Abonnements {#subscriptions}

Die Abonnements des Kontakts werden im entsprechenden Tab aufgeführt. Weiterführende Informationen zum Abonnement eines Dienstes finden Sie in [diesem Abschnitt](../../audiences/using/about-subscriptions.md).

Der Tab **[!UICONTROL Mobile-App-Abonnements]** bezieht sich auf Push-Benachrichtigungen. Weiterführende Informationen hierzu finden Sie im Kanal [Push-Benachrichtigung](../../channels/using/about-push-notifications.md).

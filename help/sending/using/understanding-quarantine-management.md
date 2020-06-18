---
title: Funktionsweise der Quarantäneverwaltung
description: Hier erfahren Sie, wie die Zustellbarkeit durch die Quarantäneverwaltung optimiert werden kann.
page-status-flag: never-activated
uuid: 3c287865-1ada-4351-b205-51807ff9f7ed
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: monitoring-messages
discoiquuid: de3a50b6-ea8f-4521-996b-c49cc1f3c946
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 121ec37cef6193d3a7085b6d0296b6a2e7cafa06
workflow-type: tm+mt
source-wordcount: '818'
ht-degree: 78%

---


# Funktionsweise der Quarantäneverwaltung{#understanding-quarantine-management}

## Über Quarantänen {#about-quarantines}

Eine E-Mail-Adresse oder Telefonnummer kann in Quarantäne kommen, weil z. B. das Postfach voll ist oder die Adresse nicht existiert.

In diesem [Abschnitt](#conditions-for-sending-an-address-to-quarantine) werden die Regeln, die eine Quarantäne auslösen, näher erläutert.

### Zustellbarkeit durch Quarantänen optimieren  {#optimizing-your-delivery-through-quarantines}

Die Profile, deren E-Mail-Adressen oder Telefonnummern unter Quarantäne sind, werden während der Nachrichtenvorbereitung automatisch ausgeschlossen (siehe [Für einen Versand in Quarantäne befindliche Adressen identifizieren](#identifying-quarantined-addresses-for-a-delivery)). Dies beschleunigt die Zustellung, da sich die Fehlerrate maßgeblich auf die Zustellgeschwindigkeit auswirkt.

Teilweise werden E-Mails von Providern automatisch als Spam eingestuft, wenn die Anzahl ungültiger Adressen zu hoch ist. Quarantäne ermöglicht es Ihnen daher, einer blockierungsliste nicht von diesen Anbietern hinzugefügt zu werden.

Zusätzlich helfen Ihnen Quarantänen, die Kosten des SMS-Versands zu senken, indem fehlerhafte Telefonnummern aus dem Versand ausgeschlossen werden.

Weiterführende Informationen zu Best Practices zur Durchführung und Optimierung von Sendungen finden Sie auf [dieser Seite](https://docs.campaign.adobe.com/doc/standard/getting_started/de/ACS_DeliveryBestPractices.html).

### Quarantäne vs. blockierungsliste {#quarantine-vs-block-list}

Eine **Quarantäne** bezieht sich immer nur auf die Adresse, nicht aber auf das Profil selbst. Sollten zwei Profile dieselbe E-Mail-Adresse verwenden, sind beide von der Quarantäne betroffen.

Falls jedoch ein Profil mit einer E-Mail-Adresse in Quarantäne eine neue Adresse angibt, kann es erneut in Versandzielgruppen aufgenommen werden.

Being on the **block list**, on the other hand, will result in the profile no longer being targeted by any delivery, for example after an unsubscription (opt-out). Weitere Informationen zum blockierungsliste-Verfahren finden Sie unter [Info zu &quot;opt-in&quot;und &quot;opt-out&quot;in der Kampagne](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

>[!NOTE]
>
>Wenn ein Benutzer auf eine SMS-Nachricht mit einem Suchbegriff wie &quot;STOP&quot;antwortet, um sich von SMS-Versänden abzumelden, wird sein Profil nicht wie im E-Mail-Ausschluss zur blockierungsliste hinzugefügt. The profile phone number is sent to quarantine with the **[!UICONTROL On block list]** status. Dieser Status bezieht sich nur auf die Telefonnummer, das Profil befindet sich nicht auf der blockierungsliste, sodass der Benutzer weiterhin E-Mail-Nachrichten erhält. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../channels/using/managing-incoming-sms.md#managing-stop-sms).

## In Quarantäne befindliche Adressen identifizieren  {#identifying-quarantined-addresses}

Die in Quarantäne befindlichen Adressen können für einen bestimmten Versand oder für die gesamte Plattform angezeigt werden.

>[!NOTE]
>
>Um eine Adresse aus der Quarantäne freizugeben, nehmen Sie bitte mit Ihrem technischen Administrator Kontakt auf.

### Für einen Versand in Quarantäne befindliche Adressen identifizieren  {#identifying-quarantined-addresses-for-a-delivery}

Die für einen bestimmten Versand in Quarantäne befindlichen Adressen werden während der Versandvorbereitung im Tab **[!UICONTROL Ausschlusslogs]** des Versand-Dashboards angezeigt (siehe [diesen Abschnitt](../../sending/using/monitoring-a-delivery.md#exclusion-logs)). Weiterführende Informationen zur Versandvorbereitung finden Sie in [diesem Abschnitt](../../sending/using/preparing-the-send.md).

![](assets/exclusion_logs.png)

### Für die gesamte Plattform in Quarantäne befindliche Adressen identifizieren  {#identifying-quarantined-addresses-for-the-entire-platform}

Administratoren können die für die gesamte Plattform in Quarantäne befindlichen Adressen im Menü **[!UICONTROL Administration > Kanäle > Quarantänen > Adressen]** anzeigen.

>[!NOTE]
>
>In diesem Menü werden unter Quarantäne gestellte Elemente für die Kanäle **E-Mail**, **SMS** und **Push-Benachrichtigungen** aufgeführt.

![](assets/quarantines1.png)

>[!NOTE]
>
>Mit zunehmendem Alter der Datenbank steigt auch die Zahl der Adressen in Quarantäne. Wenn man beispielsweise davon ausgeht, dass eine E-Mail-Adresse eine Lebensdauer von etwa drei Jahren hat und dass die Empfängertabelle pro Jahr um 50 % wächst, lässt sich der Quarantänezuwachs wie folgt berechnen: Ende von Jahr 1: (1*0,33)/(1+0,5)=22 %. Ende von Jahr 2: ((1,22*0,33)+0,33)/(1,5+0,75)=32,5 %.

## Ursachen für Quarantänen  {#conditions-for-sending-an-address-to-quarantine}

Adobe Campaign verwaltet Quarantänen entsprechend dem Fehlertyp und dem Grund, der dem Fehler im Zuge der Qualifikation der Fehlermeldungen zugewiesen wurde (siehe [Typen und Ursachen für fehlgeschlagene Sendungen](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons) und [Bounce-Message-Qualifizierung](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification)).

* **Ignorierter Fehler**: Bei ignorierten Fehlern wird eine Adresse nicht unter Quarantäne gestellt.
* **Hardbounce**: Die E-Mail-Adresse kommt sofort in Quarantäne.
* **Softbounce**: In diesem Fall wird die Adresse nicht sofort unter Quarantäne gestellt, sondern der Fehlerzähler nur hinaufgesetzt. Sollte der Zähler eine festgelegte Schwelle überschreiten, kommt die Adresse in Quarantäne. Die Standardkonfiguration sieht eine Schwelle von fünf Fehlern vor, die jeweils in einem Abstand von mindestens 24 Stunden auf den vorhergehenden folgen müssen, um berücksichtigt zu werden. Beim fünften Fehler kommt die Adresse in Quarantäne. Die Schwelle für den Fehlerzähler ist einstellbar. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../administration/using/configuring-email-channel.md#email-channel-parameters).

   Wenn eine Nachricht bei einem erneuten Versuch zugestellt werden kann, wird der Fehlerzähler der in Quarantäne befindlichen Adresse neu initialisiert. Der Status der Adresse wird auf **[!UICONTROL Gültig]** gesetzt und mithilfe des Workflows **[!UICONTROL Datenbankbereinigung]** wird die Adresse nach zwei Tagen aus der Quarantäneliste gelöscht.

Wenn ein Benutzer eine E-Mail als Spam kennzeichnet (**Feedback Loop**), wird die Nachricht automatisch an ein von Campaign verwaltetes technisches Postfach weitergeleitet. The user&#39;s email address is then automatically sent to quarantine with the **[!UICONTROL On block list]** status. Dieser Status bezieht sich nur auf die Adresse, das Profil befindet sich nicht auf der blockierungsliste, sodass der Benutzer weiterhin SMS- und Push-Benachrichtigungen erhält.

>[!NOTE]
Bei der Quarantänefunktion in Adobe Campaign wird die Groß-/Kleinschreibung beachtet. Achten Sie darauf, E-Mail-Adressen in Kleinbuchstaben zu importieren, damit sie später nicht erneut verwendet werden.

Bei Adressen in Quarantäne (siehe [Für die gesamte Plattform in Quarantäne befindliche Adressen identifizieren](#identifying-quarantined-addresses-for-the-entire-platform)) zeigt das Feld **[!UICONTROL Fehlerursache]** an, warum die Quarantäne ausgelöst wurde.

![](assets/quarantines2.png)


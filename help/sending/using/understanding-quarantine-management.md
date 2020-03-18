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
source-git-commit: f7e361d10d039718c421a3684c518347af2be951

---


# Funktionsweise der Quarantäneverwaltung{#understanding-quarantine-management}

## Über Quarantänen {#about-quarantines}

Eine E-Mail-Adresse oder Telefonnummer kann in Quarantäne kommen, weil z. B. das Postfach voll ist oder die Adresse nicht existiert.

In diesem [Abschnitt](#conditions-for-sending-an-address-to-quarantine) werden die Regeln, die eine Quarantäne auslösen, näher erläutert.

### Zustellbarkeit durch Quarantänen optimieren {#optimizing-your-delivery-through-quarantines}

Die Profile, deren E-Mail-Adressen oder Telefonnummern unter Quarantäne sind, werden während der Nachrichtenvorbereitung automatisch ausgeschlossen (siehe [Für einen Versand in Quarantäne befindliche Adressen identifizieren](#identifying-quarantined-addresses-for-a-delivery)). Dies beschleunigt die Zustellung, da sich die Fehlerrate maßgeblich auf die Zustellgeschwindigkeit auswirkt.

Teilweise werden E-Mails von Providern automatisch als Spam eingestuft, wenn die Anzahl ungültiger Adressen zu hoch ist. Durch die Quarantänefunktion vermeiden Sie, von diesen Providern auf eine Blacklist gesetzt zu werden.

Zusätzlich helfen Ihnen Quarantänen, die Kosten des SMS-Versands zu senken, indem fehlerhafte Telefonnummern aus dem Versand ausgeschlossen werden.

Weiterführende Informationen zu Best Practices zur Durchführung und Optimierung von Sendungen finden Sie auf [dieser Seite](https://docs.campaign.adobe.com/doc/standard/getting_started/en/ACS_DeliveryBestPractices.html).

### Quarantäne im Vergleich zur Blacklist {#quarantine-vs-blacklisting}

Eine **Quarantäne** bezieht sich immer nur auf die Adresse, nicht aber auf das Profil selbst. Sollten zwei Profile dieselbe E-Mail-Adresse verwenden, sind beide von der Quarantäne betroffen.

Falls jedoch ein Profil mit einer E-Mail-Adresse in Quarantäne eine neue Adresse angibt, kann es erneut in Versandzielgruppen aufgenommen werden.

Im Gegensatz dazu sind es bei der **Blacklist** die Profile selbst, die vom Versand ausgeschlossen werden. Dies ist z. B. nach einem Opt-out der Fall. Weiterführende Informationen zum Blacklist-Vorgang finden Sie unter [Blacklists in Campaign verwenden](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

>[!NOTE]
>
>Wenn ein Benutzer auf eine SMS-Nachricht mit einem Schlüsselwort wie &quot;STOP&quot; antwortet, um sich vom SMS-Versand abzumelden, wird sein Profil nicht wie bei einem E-Mail-Abmeldevorgang auf die Blacklist gesetzt. The profile phone number is sent to quarantine with the **[!UICONTROL Blacklisted]** status. Der Status bezieht sich ausschließlich auf die Telefonnummer und das Profil wird nicht auf die Blacklist gesetzt, sodass der Empfänger nach wie vor E-Mail-Nachrichten erhält. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../channels/using/managing-incoming-sms.md#managing-stop-sms).

## In Quarantäne befindliche Adressen identifizieren {#identifying-quarantined-addresses}

Die in Quarantäne befindlichen Adressen können für einen bestimmten Versand oder für die gesamte Plattform angezeigt werden.

>[!NOTE]
>
>Um eine Adresse aus der Quarantäne freizugeben, nehmen Sie bitte mit Ihrem technischen Administrator Kontakt auf.

### Für einen Versand in Quarantäne befindliche Adressen identifizieren {#identifying-quarantined-addresses-for-a-delivery}

Quarantined addresses for a specific delivery are listed during the delivery preparation phase, in the **[!UICONTROL Exclusion logs]** tab of the delivery dashboard (see [this section](../../sending/using/monitoring-a-delivery.md#exclusion-logs)). Weiterführende Informationen zur Versandvorbereitung finden Sie in [diesem Abschnitt](../../sending/using/preparing-the-send.md).

![](assets/exclusion_logs.png)

### Für die gesamte Plattform in Quarantäne befindliche Adressen identifizieren {#identifying-quarantined-addresses-for-the-entire-platform}

Administrators can list the addresses in quarantine for the entire platform from the **[!UICONTROL Administration > Channels > Quarantines > Addresses]** menu.

>[!NOTE]
>
>In diesem Menü werden unter Quarantäne gestellte Elemente für die Kanäle **E-Mail**, **SMS** und **Push-Benachrichtigungen** aufgeführt.

![](assets/quarantines1.png)

>[!NOTE]
>
>Mit zunehmendem Alter der Datenbank steigt auch die Zahl der Adressen in Quarantäne. Wenn man beispielsweise davon ausgeht, dass eine E-Mail-Adresse eine Lebensdauer von etwa drei Jahren hat und dass die Empfängertabelle pro Jahr um 50 % wächst, lässt sich der Quarantänezuwachs wie folgt berechnen: Ende von Jahr 1: (1*0,33)/(1+0,5)=22 %. Ende von Jahr 2: ((1,22*0,33)+0,33)/(1,5+0,75)=32,5 %.

## Ursachen für Quarantänen {#conditions-for-sending-an-address-to-quarantine}

Adobe Campaign verwaltet Quarantänen entsprechend dem Fehlertyp und dem Grund, der dem Fehler im Zuge der Qualifikation der Fehlermeldungen zugewiesen wurde (siehe [Typen und Ursachen für fehlgeschlagene Sendungen](../../sending/using/understanding-delivery-failures.md#delivery-failure-types-and-reasons) und [Bounce-Message-Qualifizierung](../../sending/using/understanding-delivery-failures.md#bounce-mail-qualification)).

* **Ignorierter Fehler**: Bei ignorierten Fehlern wird eine Adresse nicht unter Quarantäne gestellt.
* **Hardbounce**: Die E-Mail-Adresse kommt sofort in Quarantäne.
* **Softbounce**: In diesem Fall wird die Adresse nicht sofort unter Quarantäne gestellt, sondern der Fehlerzähler nur hinaufgesetzt. Sollte der Zähler eine festgelegte Schwelle überschreiten, kommt die Adresse in Quarantäne. Die Standardkonfiguration sieht eine Schwelle von fünf Fehlern vor, die jeweils in einem Abstand von mindestens 24 Stunden auf den vorhergehenden folgen müssen, um berücksichtigt zu werden. Die Adresse wird beim fünften Fehler in Quarantäne gesetzt. Die Schwelle für den Fehlerzähler ist einstellbar. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../administration/using/configuring-email-channel.md#email-channel-parameters).

   Wenn eine Nachricht bei einem erneuten Versuch zugestellt werden kann, wird der Fehlerzähler der in Quarantäne befindlichen Adresse neu initialisiert. The address status changes to **[!UICONTROL Valid]** and it is deleted from the list of quarantines after two days by the **[!UICONTROL Database cleanup]** workflow.

Wenn ein Benutzer eine E-Mail als Spam kennzeichnet (**Feedback Loop**), wird die Nachricht automatisch an ein von Campaign verwaltetes technisches Postfach weitergeleitet. The user&#39;s email address is then automatically sent to quarantine with the **[!UICONTROL Blacklisted]** status. Der Status bezieht sich ausschließlich auf die Adresse und das Profil wird nicht auf die Blacklist gesetzt, sodass der Empfänger nach wie vor SMS-Nachrichten und Push-Benachrichtigungen erhält.

>[!NOTE]
Bei der Quarantänefunktion in Adobe Campaign wird die Groß-/Kleinschreibung beachtet. Achten Sie darauf, E-Mail-Adressen in Kleinbuchstaben zu importieren, damit sie später nicht erneut verwendet werden.

In the list of quarantined addresses (see [Identifying quarantined addresses for the entire platform](#identifying-quarantined-addresses-for-the-entire-platform)), the **[!UICONTROL Error reason]** field indicates why the selected address was placed in quarantine.

![](assets/quarantines2.png)


---
title: Fehlerbehebung bei Zustellbarkeitsproblemen in Adobe Campaign Standard
description: Erfahren Sie, wie Sie Zustellbarkeitsprobleme in Adobe Campaign Standard beheben können.
page-status-flag: never-activated
uuid: 286fceee-65a9-4cb9-b205-9ce5d024675c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: sheduling-messages
discoiquuid: 9c7fd670-bba9-4f3c-8cb1-87397a1acd27
context-tags: delivery,schedule,back
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 012546e109b085b7ed968bcefa8f76482656ae0d
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 56%

---


# Fehlerbehebung{#troubleshooting}

Haben Sie ein Problem mit der Zustellbarkeit? Möglicherweise finden Sie hier eine Lösung.

## Gleiche Fehlermeldung bei einem ISP {#same-error-for-an-isp}

**Warum erhalte ich bei einem bestimmten ISP immer dieselbe Fehlermeldung?**

Wenn Sie bei einem ISP immer dieselbe Fehlermeldung erhalten, hat der ISP möglicherweise festgestellt, dass Ihre E-Mail- oder IP-Adresse fehlerhaft ist. Wir empfehlen in diesem Fall folgende Schritte:
* Prüfen Sie, ob Sie eine große Menge an Fehlschlägen in Verbindung mit nicht bestehenden E-Mail-Adressen erhalten (**Unbekannter Nutzer**).
* Aktualisieren Sie Ihre Anmeldeformulare und achten Sie auf etwaige Fehler im Domain-Namen (z. B. gmaul.com oder yaho.com).
* Wenn Fehlermeldungen auftreten, die Ihre E-Mails als Spam einstufen, oder wenn Ihre E-Mails blockiert werden, versuchen Sie, alle Empfänger auszuschließen, die innerhalb von 12 Monaten ab dem Versand ihre E-Mail nicht geöffnet oder darauf geklickt haben.

Wenn das Problem fortbesteht, kontaktieren Sie den Zustellbarkeitsservice oder die entsprechende Geschäftsabteilung oder den Support von Adobe Campaign.

## Blockierungsliste versus Quarantäne {#block-list-versus-quarantine}

* **Was ist der Unterschied zwischen einer E-Mail-Adresse auf einer blockierungsliste und einer isolierten E-Mail-Adresse?**

   * The status **[!UICONTROL On block list]** is a result of a feedback loop (when a person reports a message as spam).

   * Der Status **[!UICONTROL In Quarantäne]** ist das Ergebnis eines Soft- oder Hardbounce.
   Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/understanding-quarantine-management.md#quarantine-vs-block-list).

* **Was bedeuten die unterschiedlichen Gründe für Quarantäne-Fehler?**

   Es gibt 10 mögliche Gründe: nicht definiert, Benutzer unbekannt, Ungültige Domain, Adresse auf blockierungsliste, verweigert, Fehler ignoriert, unerreichbar, Konto deaktiviert, Postfach voll, nicht verbunden.

   Weitere Informationen hierzu finden Sie unter [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md).

## Aus blockierungsliste entfernen {#removing-from-block-list}

* **Einer meiner Empfänger wurde versehentlich der blockierungsliste hinzugefügt. Wie entferne ich sie aus der blockierungsliste, damit ich Beginn die Nachrichten wieder senden kann?**

   * Gehen Sie zu **[!UICONTROL Administration > Kanäle > Quarantänen > Adressen]**.
   * Setzen Sie in den Details des entsprechenden Datensatzes den Wert des **[!UICONTROL Status]**-Feldes auf **[!UICONTROL Gültig]**.
   * Speichern Sie die Daten.

* **Wie kann ich herausfinden, ob sich eine meiner IPs auf einer blockierungsliste befindet? Wie entferne ich meine IP(s) von einer blockierungsliste?**

   Um zu überprüfen, ob Ihre IP-Adresse auf einer blockierungsliste gespeichert ist, können Sie verschiedene Websites verwenden, um sie zu überprüfen, z. B.:
   * [MX Toolbox](https://mxtoolbox.com/)
   * [Meine IP-Adresse](https://whatismyipaddress.com)

   Im Allgemeinen gibt das Ergebnis der IP-Adressprüfung eine Liste zurück, die Details zur blockierungsliste und auch den Namen der Website enthält, die die IP-Adresse blockiert hat.

   Durch Auswahl des entsprechenden Links können Sie die Details der Website aufrufen.

   Anschließend können Sie beantragen, dass Ihre Website von der Website gelöscht wird, die die IP-Adresse zu ihrer blockierungsliste hinzugefügt hat.

   >[!NOTE]
   >
   >Dieser Prozess ist je nach Webseite unterschiedlich. Auf manchen Webseiten müssen Sie ein Konto erstellen, während andere nur die Angabe der IP-Adresse verlangen.

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
source-git-commit: 1f15e28bed22e3defb29f16875fcf4c07f4af5a3
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 61%

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

## Blockierungsliste versus Quarantäne {#denylist-versus-quarantine}

* **Was ist der Unterschied zwischen einer auf die Blockierungsliste gesetzt E-Mail-Adresse und einer isolierten E-Mail-Adresse?**

   * The status **[!UICONTROL Denylisted]** is a result of a feedback loop (when a person reports a message as spam).

   * Der Status **[!UICONTROL In Quarantäne]** ist das Ergebnis eines Soft- oder Hardbounce.
   Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/understanding-quarantine-management.md#quarantine-vs-block-list).

* **Was bedeuten die unterschiedlichen Gründe für Quarantäne-Fehler?**

   Es gibt 10 mögliche Gründe: nicht definiert, Benutzer unbekannt, Ungültige Domain, auf die Blockierungsliste gesetzt Adresse, verweigert, Fehler ignoriert, unerreichbar, Konto deaktiviert, Postfach vollständig, nicht verbunden.

   Weitere Informationen hierzu finden Sie unter [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md).

## Aus Blockierungsliste entfernen {#removing-from-denylist}

* **Einer meiner Empfänger wurde versehentlich auf die Blockierungsliste gesetzt. How do I remove them from the denylist so that I can start sending them messages again?**

   * Gehen Sie zu **[!UICONTROL Administration > Kanäle > Quarantänen > Adressen]**.
   * Setzen Sie in den Details des entsprechenden Datensatzes den Wert des **[!UICONTROL Status]**-Feldes auf **[!UICONTROL Gültig]**.
   * Speichern Sie die Daten.

* **Wie kann ich herausfinden, ob eine meiner IPs auf die Blockierungsliste gesetzt ist? How do I remove my IP(s) from a denylist?**

   Um zu prüfen, ob Ihre IP-Adresse auf die Blockierungsliste gesetzt ist, können Sie sie auf verschiedenen Websites überprüfen, z. B.:
   * [MX Toolbox](https://mxtoolbox.com/)
   * [Wie lautet meine IP-Adresse?](https://whatismyipaddress.com)

   Im Allgemeinen gibt das Ergebnis der IP-Adressprüfung eine Liste zurück, die Details der Blockierungsliste und auch den Namen der Website enthält, die die IP-Adresse blockiert hat.

   Durch Auswahl des entsprechenden Links können Sie die Details der Website aufrufen.

   Anschließend können Sie beantragen, dass Ihre Website von der Website gelöscht wird, die die IP-Adresse zu ihrer Blockierungsliste hinzugefügt hat.

   >[!NOTE]
   >
   >Dieser Prozess ist je nach Website unterschiedlich. Auf manchen Websites müssen Sie ein Konto erstellen, während andere nur die Angabe der IP-Adresse verlangen.

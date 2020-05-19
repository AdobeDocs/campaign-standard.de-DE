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
translation-type: ht
source-git-commit: 87168dca3604073d8a540c579448ab65f07cd976

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

## Blacklist versus Quarantäne {#blacklisting-versus-quarantine}

* **Was ist der Unterschied zwischen einer auf eine Blacklist gesetzten E-Mail-Adresse und einer unter Quarantäne gestellten E-Mail-Adresse?**

   * Der Status **[!UICONTROL Auf Blacklist]** ist das Ergebnis eines Feedback-Loops (wenn ein Empfänger eine E-Mail als Spam meldet).

   * Der Status **[!UICONTROL In Quarantäne]** ist das Ergebnis eines Soft- oder Hardbounce.
   Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/understanding-quarantine-management.md#quarantine-vs-blacklisting).

* **Was bedeuten die unterschiedlichen Gründe für Quarantäne-Fehler?**

   Es gibt zehn Gründe: Unbestimmt, Unbekannter Nutzer, Ungültige Domain, Adresse auf der Blacklist, Zurückgewiesen, Fehler ignoriert, Unerreichbar, Konto deaktiviert, Postfach voll, Nicht angemeldet.

   Weitere Informationen hierzu finden Sie unter [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md).

## Von der Blacklist nehmen{#unblacklisting}

* **Einer meiner Empfänger wurde irrtümlich auf die Blacklist gesetzt. Wie lässt er sich daraus streichen, sodass ich ihm wieder Nachrichten senden kann?**

   * Gehen Sie zu **[!UICONTROL Administration > Kanäle > Quarantänen > Adressen]**.
   * Setzen Sie in den Details des entsprechenden Datensatzes den Wert des **[!UICONTROL Status]**-Feldes auf **[!UICONTROL Gültig]**.
   * Speichern Sie die Daten.

* **Wie kann ich feststellen, ob eine meiner IP-Adressen auf einer Blacklist steht? Wie kann ich meine IP-Adresse wieder aus der Blacklist entfernen?**

   Sie können auf den folgenden Webseiten überprüfen, ob Ihre IP-Adresse auf einer Blacklist steht:
   * https://mxtoolbox.com/
   * https://whatismyipaddress.com/blacklist-check
   * https://www.blacklistalert.org/
   Nach der IP-Adressen-Prüfung erhalten Sie eine Liste mit Details zur Blacklist und auch den Namen der Webseite, von der die IP-Adresse auf die Blacklist gesetzt wurde.

   Durch Auswahl des entsprechenden Links können Sie die Details der Website aufrufen.

   Dann können Sie diese Webseite ersuchen, Ihre Webseite von der Blacklist zu löschen.

   >[!NOTE]
   >
   >Dieser Prozess ist je nach Webseite unterschiedlich. Auf manchen Webseiten müssen Sie ein Konto erstellen, während andere nur die Angabe der IP-Adresse verlangen.

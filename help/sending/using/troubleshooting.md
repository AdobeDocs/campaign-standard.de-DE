---
title: Fehlerbehebung bei Bereitstellungsproblemen in Adobe Campaign Standard
description: Erfahren Sie, wie Sie mit Adobe Campaign Standard Probleme bei der Bereitstellung lösen können.
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
source-git-commit: fc9c6371732aa0eba9e675d2709cd62c25b27b96

---


# Problembehebung{#troubleshooting}

Haben Sie ein Problem mit der Zustellbarkeit? Möglicherweise finden Sie hier eine Lösung.

**Warum erhalte ich bei einem bestimmten ISP immer dieselbe Fehlermeldung?**

Wenn Sie bei einem ISP immer dieselbe Fehlermeldung erhalten, hat der ISP möglicherweise festgestellt, dass Ihre E-Mail- oder IP-Adresse fehlerhaft ist. Wir empfehlen in diesem Fall folgende Schritte:
* Prüfen Sie, ob Sie eine große Menge an Fehlschlägen in Verbindung mit nicht bestehenden E-Mail-Adressen erhalten (**Unbekannter Nutzer**).
* Aktualisieren Sie Ihre Anmeldeformulare, und achten Sie auf etwaige Fehler im Domain-Namen (z. B. gmaul.com oder yaho.com).
* Wenn Fehlermeldungen auftreten, die Ihre E-Mails als Spam einstufen, oder wenn Ihre E-Mails blockiert werden, versuchen Sie, alle Empfänger auszuschließen, die innerhalb von 12 Monaten ab dem Versand ihre E-Mail nicht geöffnet oder darauf geklickt haben.

Wenn das Problem fortbesteht, kontaktieren Sie den Zustellbarkeitsservice oder die entsprechende Geschäftsabteilung oder den Support von Adobe Campaign.

**Was ist der Unterschied zwischen einer auf eine Blacklist gesetzten E-Mail-Adresse und einer unter Quarantäne gestellten E-Mail-Adresse?**

Der Status **[!UICONTROL Auf Blacklist]ist das Ergebnis einer Feedback-Loop (wenn ein Empfänger eine E-Mail als Spam meldet).**

Der Status **[!UICONTROL In Quarantäne]ist das Ergebnis eines Soft- oder Hardbounce.**

**Was bedeuten die unterschiedlichen Gründe für Quarantäne-Fehler?**

Es gibt zehn Gründe: Unbestimmt, Unbekannter Nutzer, Ungültige Domain, Adresse auf der Blacklist, Zurückgewiesen, Fehler ignoriert, Unerreichbar, Konto deaktiviert, Postfach voll, Nicht angemeldet.

Weitere Informationen hierzu finden Sie unter [Das Quarantänemanagement](../../sending/using/understanding-quarantine-management.md).

**Einer meiner Empfänger wurde irrtümlich auf die Blacklist gesetzt. Wie kann ich ihn wieder daraus streichen lassen, damit ich ihm wieder Nachrichten senden kann?**

* Gehen Sie zu **[!UICONTROL Administration &gt; Kanäle &gt; Quarantänen &gt; Adressen]**.
* Setzen Sie in den Details des entsprechenden Datensatzes den Wert des **[!UICONTROL Status]**-Feldes auf **[!UICONTROL Gültig]**.
* Speichern Sie die Daten.

**Wie kann ich feststellen, ob eine meiner IP-Adressen auf einer Blacklist steht? Wie kann ich meine IP-Adresse wieder aus der Blacklist entfernen?**

Sie können auf den folgenden Webseiten überprüfen, ob Ihre IP-Adresse auf einer Blacklist steht:
* https://mxtoolbox.com/
* https://whatismyipaddress.com/blacklist-check
* http://www.blacklistalert.org/

Nach der IP-Adressen-Prüfung erhalten Sie eine Liste mit Details zur Blacklist und auch den Namen der Webseite, von der die IP-Adresse auf die Blacklist gesetzt wurde.

Durch Anklicken des Links können Sie die Details der Webseite aufrufen.

Dann können Sie diese Webseite ersuchen, Ihre Webseite von der Blacklist zu löschen.

Dieser Prozess ist je nach Webseite unterschiedlich. Auf manchen Webseiten müssen Sie ein Konto erstellen, während andere nur die Angabe der IP-Adresse verlangen.

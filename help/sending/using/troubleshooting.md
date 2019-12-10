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
source-git-commit: b2df5ca4d38e35f57815924ffbe0313dc1a22b29

---


# Problembehebung{#troubleshooting}

Haben Sie ein Lieferproblem? Die Lösung finden Sie hier...

**Warum erhalte ich immer dieselbe Fehlermeldung für einen bestimmten ISP?**

Wenn Sie immer dieselbe Fehlermeldung für einen ISP erhalten, wurde Ihre E-Mail oder IP vom ISP möglicherweise als fehlerhaft erkannt. Führen Sie die folgenden Empfehlungen aus:
* Überprüfen Sie, ob ein großer Prozentsatz von Fehlern in Verbindung mit nicht vorhandenen E-Mail-Adressen (**Benutzerdefinierte** Fehler) vorliegt.
* Aktualisieren Sie Ihre Abonnementformulare, um Fehler in den eingegebenen Domänennamen zu erkennen (z. B.: gmaul.com oder yaho.com).
* Wenn Sie Fehler bemerken, die darauf hindeuten, dass Ihre Nachrichten als Spam deklariert werden oder dass Ihre Nachrichten ständig blockiert werden, versuchen Sie, die Empfänger auszuschließen, die in den letzten 12 Monaten keine Ihrer Nachrichten geöffnet oder angeklickt haben.

Wenn das Problem weiterhin besteht, wenden Sie sich an den kommerziellen Dienst oder den Bereitstellungsdienst oder den Adobe Campaign-Support.

**Was ist der Unterschied zwischen einer auf der schwarzen Liste stehenden E-Mail-Adresse und einer unter Quarantäne stehenden E-Mail-Adresse?**

Der Status **[!UICONTROL Blacklist]** ist das Ergebnis einer Feedback-Schleife (wenn eine Person eine Nachricht als Spam meldet).

Der Status **[!UICONTROL Quarantäne]** ist das Ergebnis eines weichen oder harten Absprungs.

**Was bedeuten die unterschiedlichen Gründe für einen Quarantänefehler?**

Es gibt zehn mögliche Gründe: nicht definiert, Benutzer unbekannt, ungültige Domäne, Blacklist-Adresse, verweigert, Fehler ignoriert, nicht erreichbar, Konto deaktiviert, Postfach voll, nicht verbunden.

Weitere Informationen hierzu finden Sie unter [Das Quarantänemanagement](../../sending/using/understanding-quarantine-management.md).

**Einer meiner Empfänger wurde versehentlich auf die schwarze Liste gesetzt. Wie kann ich die schwarze Liste aufheben, damit ich wieder mit dem Senden beginnen kann?**

* Gehen Sie zu **[!UICONTROL Administration &gt; Kanäle &gt; Quarantäne &gt; Adressen]**.
* Legen Sie in den Details des entsprechenden Datensatzes den Wert des Felds **[!UICONTROL Status]** auf **[!UICONTROL Gültig]** fest.
* Speichern Sie den Datensatz.

**Wie kann ich herausfinden, ob eine meiner IPs auf der schwarzen Liste steht? Wie kann ich die schwarze Liste meiner IP(s) aufheben?**

Um zu überprüfen, ob Ihre IP-Adresse auf eine schwarze Liste gesetzt ist, können Sie sie auf verschiedenen Websites überprüfen:
* http://mxtoolbox.com/
* http://whatismyipaddress.com/blacklist-check
* http://www.blacklistalert.org/

Im Allgemeinen gibt das Ergebnis der IP-Adressprüfung eine Liste zurück, die Details der schwarzen Liste und auch den Namen der Website, die die IP-Adresse schwarz aufgeführt.

Durch Klicken auf den Link können Sie auf die Website-Details zugreifen.

Anschließend können Sie beantragen, dass Ihre Website von der Website gelöscht wird, die die IP-Adresse auf eine schwarze Liste gesetzt hat.

Der Löschvorgang kann je nach Website unterschiedlich sein. Bei einigen Websites müssen Sie ein Konto erstellen, bei anderen müssen Sie lediglich die IP-Adresse angeben.

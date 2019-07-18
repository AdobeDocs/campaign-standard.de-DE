---
title: Funktionsweise des Opt-in- und Opt-out-Verfahrens in Campaign
seo-title: Funktionsweise des Opt-in- und Opt-out-Verfahrens in Campaign
description: Funktionsweise des Opt-in- und Opt-out-Verfahrens in Campaign
seo-description: Wird ein Profil durch Opt-out auf die Blacklist gesetzt, werden keinerlei Nachrichten mehr an dieses gesendet, auch nicht über einzelne Kanäle.
page-status-flag: nie aktiviert
uuid: 501 d 9485-976 b -4 de 7-b 242-6886 f 2814 c 6 c
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Zielgruppen
content-type: Referenz
topic-tags: understanding-opt-in-and-opt-out-processes
discoiquuid: 2 f 26 ec 22-0809-4541-b 2 a 1-e 84 ff 868 ba 6 e
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Funktionsweise des Opt-in- und Opt-out-Verfahrens in Campaign{#about-opt-in-and-opt-out-in-campaign}

Wird ein Profil durch Opt-out auf die Blacklist gesetzt, werden keinerlei Nachrichten mehr an dieses gesendet, auch nicht über einzelne Kanäle.

Um Profilen die Möglichkeit zu geben, sich durch Opt-in oder Opt-out an- bzw. abzumelden, müssen Sie eine eigene Landingpage erstellen. Weiterführende Informationen dazu erfahren Sie im Abschnitt [Opt-in- und Opt-out-Landingpages einrichten](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#setting-up-opt-in-and-opt-out-landing-pages).

Das Opt-in- bzw. Opt-out-Verfahren für Profile kann auch manuell durch einen Benutzer durchgeführt werden. Weiterführende Informationen dazu erfahren Sie im Abschnitt [Opt-in und Opt-out für ein Profil verwalten](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#managing-opt-in-and-opt-out-from-a-profile).

Opt-out-Profile werden automatisch zum Zeitpunkt der Versandanalyse ausgeschlossen. Dies beschleunigt den Versand, da die Zahl der fehlgeschlagenen Zustellungen reduziert wird (denn die Fehlerrate wirkt sich erheblich auf den Versanddurchsatz aus).

>[!NOTE]
>
>Im Unterschied zur Quarantäne, die sich auf **eine E-Mail-Adresse** und **eine Telefonnummer** bezieht, gilt das Opt-out für **Profile**. Wird ein Profil mit Opt-out abgemeldet, werden somit alle damit verknüpften Adressen vom Versand ausgeschlossen. Wenn die Datenbank beispielsweise zwei Profile eines Empfängers enthält und nur eines durch Opt-out abgemeldet wird, erhält er weiterhin Nachrichten. Um alle seine Adressen auszuschließen, fügen Sie sie zu den Quarantäne-Neuzugängen hinzu. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-the-entire-platform).

Weiterführende Informationen zum Abonnement von Diensten finden Sie auf [dieser Seite](../../audiences/using/about-subscriptions.md).

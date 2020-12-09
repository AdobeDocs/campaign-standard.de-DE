---
solution: Campaign Standard
product: campaign
title: Funktionsweise des Opt-in- und Opt-out-Verfahrens in Campaign
description: Opt-out eines Profils führt dazu, dass keinerlei Nachrichten mehr an dieses gesendet werden, auch nicht über einzelne Kanäle.
audience: audiences
content-type: reference
topic-tags: understanding-opt-in-and-opt-out-processes
translation-type: ht
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: ht
source-wordcount: '220'
ht-degree: 100%

---


# Funktionsweise des Opt-in- und Opt-out-Verfahrens in Campaign{#about-opt-in-and-opt-out-in-campaign}

Opt-out eines Profils führt dazu, dass keinerlei Nachrichten mehr an dieses gesendet werden, auch nicht über einzelne Kanäle.

Um Profilen die Möglichkeit zu geben, sich durch Opt-in oder Opt-out an- bzw. abzumelden, müssen Sie eine eigene Landingpage erstellen. Weiterführende Informationen dazu erfahren Sie im Abschnitt [Opt-in- und Opt-out-Landingpages einrichten](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#setting-up-opt-in-and-opt-out-landing-pages).

Das Opt-in- bzw. Opt-out-Verfahren für Profile kann auch manuell durch einen Benutzer durchgeführt werden. Weiterführende Informationen dazu erfahren Sie im Abschnitt [Opt-in und Opt-out für ein Profil verwalten](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md#managing-opt-in-and-opt-out-from-a-profile).

Opt-out-Profile werden automatisch zum Zeitpunkt der Versandanalyse ausgeschlossen. Dies beschleunigt den Versand, da die Zahl der fehlgeschlagenen Zustellungen reduziert wird (denn die Fehlerrate wirkt sich erheblich auf den Versanddurchsatz aus).

>[!NOTE]
>
>Im Unterschied zur Quarantäne, die sich auf **eine E-Mail-Adresse** und **eine Telefonnummer** bezieht, gilt das Opt-out für **Profile**. Wird ein Profil mit Opt-out abgemeldet, werden somit alle damit verknüpften Adressen vom Versand ausgeschlossen. Wenn die Datenbank beispielsweise zwei Profile eines Empfängers enthält und nur eines durch Opt-out abgemeldet wird, erhält er weiterhin Nachrichten. Um alle seine Adressen auszuschließen, fügen Sie sie zu den Quarantäne-Neuzugängen hinzu. Weiterführende Informationen hierzu finden Sie auf dieser [Seite](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-the-entire-platform).

Weiterführende Informationen zum Abonnement von Diensten finden Sie auf [dieser Seite](../../audiences/using/about-subscriptions.md).

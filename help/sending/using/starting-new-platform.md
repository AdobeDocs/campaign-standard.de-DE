---
title: Einrichten einer neuen Plattform mit Adobe Campaign Standard
description: Erfahren Sie, wie Sie mit Adobe Campaign Standard eine neue Plattform einrichten und dabei die Reputation Ihrer Domain und IP-Adresse wahren können.
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
source-git-commit: f83cf866f1c9fa53687e6cee26306d33327bd822

---


# Einrichten einer neuen Plattform{#starting-new-platform}

Für eine neue Plattform ist die Wahrung der Reputation Ihrer Domain und IP-Adresse ausschlaggebend. Im Folgenden finden Sie Empfehlungen zum Einrichten einer neuen Plattform.

Mit dem Versand von E-Mails von einer neuen Plattform zu beginnen ist ein heikler Schritt, da die Plattform noch keinen Nutzungsverlauf und keine Reputation besitzt (sofern die Versand-IPs noch nie für diesen Zweck verwendet wurden). ISPs sind normalerweise misstrauisch gegenüber IP-Adressen, die noch nie für den E-Mail-Versand verwendet wurden und plötzlich große Mengen an E-Mails versenden. Spammer verwenden normalerweise &quot;unbekannte&quot; IP-Adressen (d. h. Adressen, die auf keiner Blacklist stehen), um eine möglichst große Menge an Nachrichten zu versenden, bevor sie entdeckt werden.

Erwarten Sie nicht, dass der Versand gleich zu Beginn der Produktionsphase in der gewünschten Geschwindigkeit durchgeführt werden kann. Sie sollten auch nicht versuchen, Nachrichten in dieser Geschwindigkeit zu versenden, da dies ISPs veranlassen könnte, die Absenderadresse zu blockieren, was die Anfangsphase erheblich beeinträchtigen würde.

Das Starten einer Plattform erfolgt oft, wenn eine Liste von Adressen zum ersten Mal verwendet wird und die möglicherweise nicht vollständig qualifiziert sind. Wenn Sie an ungültige Adressen oder an Honeypot-Adressen senden, wird dies dazu beitragen, den Ruf der Plattform zu mindern.
* Wenn Sie eine Liste ungültiger Adressen haben, ist es in Ihrem besten Interesse, diese in die Quarantäne-Tabelle zu importieren (**[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Quarantines]** > **[!UICONTROL Addresses]**), bevor Sie sie zum ersten Mal senden. For more on this, see this [section](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-the-entire-platform).
* Wenn Sie dennoch die ungültigen Adressen rekalifizieren möchten, ist es bei weitem besser, dies zu tun, sobald der Ruf der Plattform etabliert ist, und nach und nach, um die Verwendung schlechter Adressen im Laufe der Zeit zu &quot;verwässern&quot;.

Zusammenfassend sollten Sie zu Projektbeginn diese Prinzipien befolgen:
* **Delegieren Sie eine dedizierte Subdomäne** an Adobe, die speziell für von Adobe gesendete E-Mail-Kampagnen gilt.
* **Importieren Sie ungültige/inaktive Adressen in die Tabelle** &quot;Quarantäne&quot;(sofern diese Informationen vorliegen).
* **Versand-Durchsatzrate** begrenzen (technische Einstellung: Begrenzung der Anzahl der Mtachilds).
* **Schrittweise Erhöhung der gesendeten** Mengen: Zielgruppe nicht die gesamte Datenbank vom Beginn, sondern fügen Sie bei jedem Senden einen zusätzlichen Bruchteil der Liste hinzu. Dies sollte es Ihnen ermöglichen, das Volumen bei jedem Schritt zu erhöhen und gleichzeitig die Gesamtrate ungültiger Adressen zu reduzieren.
* **Regelmäßig** Nachrichten senden: In gewissem Maße ist es besser, regelmäßig kleine Schüsse zu senden, anstatt große Kampagnen sporadisch.
* **Achten Sie genau auf die Versandberichte: Eine hohe Fehlerrate könnte auf eine falsche technische Konfiguration hinweisen.**

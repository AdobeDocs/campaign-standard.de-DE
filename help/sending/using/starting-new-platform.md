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
translation-type: ht
source-git-commit: 89965d859986b9176de6b6bf96df1fbbb89b5b8f

---


# Einrichten einer neuen Plattform{#starting-new-platform}

Für eine neue Plattform ist die Wahrung der Reputation Ihrer Domain und IP-Adresse ausschlaggebend. Im Folgenden finden Sie Empfehlungen zum Einrichten einer neuen Plattform.

Mit dem Versand von E-Mails von einer neuen Plattform zu beginnen ist ein heikler Schritt, da die Plattform noch keinen Nutzungsverlauf und keine Reputation besitzt (sofern die Versand-IPs noch nie für diesen Zweck verwendet wurden). ISPs sind normalerweise misstrauisch gegenüber IP-Adressen, die noch nie für den E-Mail-Versand verwendet wurden und plötzlich große Mengen an E-Mails versenden. Spammer verwenden normalerweise &quot;unbekannte&quot; IP-Adressen (d. h. Adressen, die auf keiner Blacklist stehen), um eine möglichst große Menge an Nachrichten zu versenden, bevor sie entdeckt werden.

Erwarten Sie nicht, dass der Versand gleich zu Beginn der Produktionsphase in der gewünschten Geschwindigkeit durchgeführt werden kann. Sie sollten auch nicht versuchen, Nachrichten in dieser Geschwindigkeit zu versenden, da dies ISPs veranlassen könnte, die Absenderadresse zu blockieren, was die Anfangsphase erheblich beeinträchtigen würde.

Bei der erstmaligen Nutzung einer Plattform ist die anfangs verwendete Adressliste möglicherweise fehlerhaft. Wenn Sie einen Versand an ungültige Adressen oder an eine Spam-Falle (Honeypot) durchführen, schadet dies der Reputation Ihrer Plattform. Sollten Sie bereits über eine Liste ungültiger Adressen verfügen, importieren Sie diese daher vor dem ersten Versand in die Quarantänetabelle (**[!UICONTROL Administration]**>**[!UICONTROL  Kanäle]** > **[!UICONTROL Quarantänen]**>**[!UICONTROL  Adressen]**). Wenn Sie die ungültigen Adressen wieder aktivieren möchten, empfehlen wir, dies erst dann zu tun, wenn die Reputation der Plattform sichergestellt ist, und nur schrittweise, um die Verwendung ungültiger Adressen über einen längeren Zeitraum zu &quot;verwässern&quot;.

Zusammenfassend sollten Sie zu Projektbeginn diese Prinzipien befolgen:
* **Weisen Sie den über Adobe-Anwendungen versendeten E-Mail-Kampagnen eine spezifische Sub-Domain zu.**
* **Importieren Sie ungültige/nicht aktive Adressen in die Quarantänetabelle (sofern Sie über solche Informationen verfügen).**
* **Begrenzen Sie die Durchsatzrate (technische Einstellung: Begrenzung der Anzahl der MTA-Kindprozesse).**
* **Erhöhen Sie schrittweise das Versandvolumen: Versenden Sie nicht von Anfang an E-Mails an die gesamte Datenbank, sondern fügen Sie mit jedem Versand einen weiteren Teil der Liste hinzu. Dies ermöglicht Ihnen, das Volumen Schritt für Schritt zu erhöhen und gleichzeitig den Anteil an ungültigen Adressen zu verringern.**
* **Legen Sie einen regelmäßigen Versand fest: Es ist besser, regelmäßig kleine Sendungen vorzunehmen als selten große Kampagnen durchzuführen.**
* **Achten Sie genau auf die Versandberichte: Eine hohe Fehlerrate könnte auf eine falsche technische Konfiguration hinweisen.**

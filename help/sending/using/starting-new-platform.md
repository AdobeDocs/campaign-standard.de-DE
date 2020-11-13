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
translation-type: ht
source-git-commit: 100f7eef03d10a66832920708ad415f8f0d3883c
workflow-type: ht
source-wordcount: '448'
ht-degree: 100%

---


# Einrichten einer neuen Plattform{#starting-new-platform}

Für eine neue Plattform ist die Wahrung der Reputation Ihrer Domain und IP-Adresse ausschlaggebend. Im Folgenden finden Sie Empfehlungen zum Einrichten einer neuen Plattform.

Mit dem Versand von E-Mails von einer neuen Plattform zu beginnen ist ein heikler Schritt, da die Plattform noch keine Nutzungserfahrung und keine Reputation besitzt (sofern die Versand-IPs noch nie für diesen Zweck verwendet wurden). ISPs sind normalerweise misstrauisch gegenüber IP-Adressen, die noch nie für den E-Mail-Versand verwendet wurden und plötzlich große Mengen an E-Mails versenden. Tatsächlich nutzen Spammer im Allgemeinen &quot;unbekannte&quot; IP-Adressen (Adressen, die noch nie auf Blockierungslisten waren), um vor der Erkennung eine maximale Anzahl von Nachrichten zu senden.

Erwarten Sie nicht, dass der Versand gleich zu Beginn der Produktionsphase in der gewünschten Geschwindigkeit durchgeführt werden kann. Sie sollten auch nicht versuchen, Nachrichten in dieser Geschwindigkeit zu versenden, da dies ISPs veranlassen könnte, die Absenderadresse zu blockieren, was die Anfangsphase erheblich beeinträchtigen würde.

Der Start einer Plattform erfolgt oft dadurch, dass eine Liste von Adressen zum ersten Mal verwendet wird, die möglicherweise nicht vollständig qualifiziert sind. Wenn Sie einen Versand an ungültige Adressen oder an Honeypot-Adressen durchführen, mindert dies die Reputation der Plattform.
* Wenn Sie über eine Liste ungültiger Adressen verfügen, sollten Sie diese in die Quarantänetabelle importieren (**[!UICONTROL Administration]** > **[!UICONTROL Kanäle]** > **[!UICONTROL Quarantänen]** > **[!UICONTROL Adressen]**), bevor Sie zum ersten Mal einen Versand durchführen. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses-for-the-entire-platform).
* Wenn Sie die ungültigen Adressen dennoch erneut qualifizieren möchten, ist es besser, dies schrittweise zu tun, wenn die Reputation der Plattform bereits etabliert ist. Dadurch kann die Verwendung ungültiger Adressen über einen längeren Zeitraum &quot;verwässert&quot; werden.

Zusammenfassend sollten Sie zu Projektbeginn diese Prinzipien befolgen:
* **Konfigurieren Sie eine dedizierte Subdomain** für die Arbeit mit Campaign, die für von Adobe gesendete E-Mail-Kampagnen spezifisch ist.
* **Importieren Sie ungültige/nicht aktive Adressen in die Quarantänetabelle** (sofern Sie über solche Informationen verfügen).
* **Begrenzen Sie die Durchsatzrate** (technische Einstellung: Begrenzung der Anzahl der MTA-Kindprozesse).
* **Erhöhen Sie schrittweise das Versandvolumen**: Versenden Sie nicht von Anfang an E-Mails an die gesamte Datenbank, sondern fügen Sie mit jedem Versand einen weiteren Teil der Liste hinzu. Dies ermöglicht Ihnen, das Volumen Schritt für Schritt zu erhöhen und gleichzeitig den Anteil an ungültigen Adressen zu verringern.
* **Legen Sie einen regelmäßigen Versand fest:** Es ist besser, regelmäßig kleine Sendungen vorzunehmen als selten große Kampagnen durchzuführen.
* **Achten Sie genau auf die Versandberichte: Eine hohe Fehlerrate könnte auf eine falsche technische Konfiguration hinweisen.**

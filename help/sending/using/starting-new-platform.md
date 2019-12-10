---
title: Neue Plattform mit Adobe Campaign Standard starten
description: Erfahren Sie, wie Sie mit Adobe Campaign Standard eine neue Plattform einrichten und dabei den Ruf Ihrer Domäne und IP-Adresse wahren.
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
source-git-commit: 89965d859986b9176de6b6bf96df1fbbb89b5b8f

---


# Starten einer neuen Plattform{#starting-new-platform}

Die Wahrung des Namens Ihrer Domäne und IP-Adresse ist unverzichtbar. Hier finden Sie einige Ratschläge zum Einrichten einer neuen Plattform.

E-Mails auf einer neuen Plattform zu senden, ist ein sensibler Schritt, da die Plattform keine Nutzungsgeschichte und keinen Ruf hat (wenn die sendenden IPs zu diesem Zweck nie verwendet wurden). ISPs sind natürlich verdächtig gegenüber IP-Adressen, die nie zum Senden von E-Mails verwendet wurden und die plötzlich große Mengen E-Mail-Traffic senden. In der Regel verwenden Spammer "unbekannte"IP-Adressen (d. h. Adressen, die noch nie auf der schwarzen Liste stehen), um die größtmögliche Anzahl von Nachrichten vor der Erkennung zu senden.

Man kann nicht erwarten, dass die Produktionsgeschwindigkeit zu Beginn der Produktionsphase erreicht wird. Darüber hinaus sollten Sie nicht versuchen, Nachrichten mit diesem Tempo zu senden, da dies dazu führen könnte, dass die ISPs die sendenden Adressen blockieren und den Rest der Anlaufphase ernsthaft gefährden.

Das Starten einer Plattform geschieht oft, wenn eine Liste von Adressen zum ersten Mal verwendet wird und die möglicherweise nicht vollständig qualifiziert sind. Wenn Sie an ungültige Adressen oder an Honeypot-Adressen senden, wird dies dazu beitragen, den Ruf der Plattform zu mindern. Wenn Sie eine Liste mit ungültigen Adressen haben, ist es in Ihrem besten Interesse, diese in die Quarantänetabelle (**[!UICONTROL Administration]** &gt; **[!UICONTROL Kanäle]** &gt; **[!UICONTROL Quarantäne]** &gt; **[!UICONTROL Adressen]**) zu importieren, bevor Sie sie zum ersten Mal senden. Wenn Sie dennoch die ungültigen Adressen rekalifizieren möchten, ist es bei weitem besser, dies zu tun, sobald der Ruf der Plattform etabliert ist, und nach und nach, um die Verwendung schlechter Adressen im Laufe der Zeit zu "verwässern".

Zusammenfassende Darstellung der Grundsätze, die bei der Gründung zu beachten sind:
* **Delegieren einer speziellen Subdomäne** an Adobe, die speziell für von Adobe gesendete E-Mail-Kampagnen gilt
* **Importieren Sie ungültige/inaktive Adressen in die Quarantänetabelle** (sofern diese Informationen vorliegen)
* **Lieferdurchsatz** begrenzen (technische Einstellung: Begrenzung der Anzahl der Mtachilds)
* **Schrittweise Erhöhung der gesendeten** Mengen: Sie sollten nicht von Anfang an die gesamte Datenbank als Ziel auswählen, sondern jedes Mal, wenn Sie eine Liste senden, einen zusätzlichen Bruchteil hinzufügen; Dies sollte Ihnen ermöglichen, das Volumen bei jedem Schritt zu erhöhen und gleichzeitig die Gesamtrate ungültiger Adressen zu verringern
* **Regelmäßig** Nachrichten senden: Bis zu einem gewissen Grad ist es besser, regelmäßig kleine Aufnahmen zu senden, anstatt große Kampagnen sporadisch
* **Überwachen Sie die Bereitstellungsberichte** genau: hohe Fehleranzeigen können bedeuten, dass eine technische Einstellung schlecht konfiguriert ist.

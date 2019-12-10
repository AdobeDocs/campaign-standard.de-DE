---
title: Verbessern Ihres Rufs mit Adobe Campaign Standard
description: Erfahren Sie, wie Sie Ihren Ruf in Adobe Campaign Standard verbessern können, indem Sie doppelte E-Mail-Adressen und Quarantäne verwalten.
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
source-git-commit: 44049443f8028ed26089ee0d49944ebac6a62111

---


# Verbessern Ihres Rufs{#improving-reputation}

Löschen Sie doppelte E-Mail-Adressen aus Ihrem Ziel, um zu vermeiden, dass Ihre Empfänger erschöpft sind. Dieser Schritt schützt Ihren Ruf und sorgt für eine gute Quarantäne-Verwaltung. Adobe Campaign bietet die erforderlichen Werkzeuge, um diese Empfehlungen zu implementieren und das Risiko einer schwarzen Liste durch den ISP zu vermeiden.

Nachstehend finden Sie Einzelheiten zum Duplikat- und Quarantänemanagement.

## Duplikate {#duplicates}

Die Verwendung doppelter E-Mail-Adressen kann mehrere Folgen haben:
* Die gleiche Nachricht wird mehrmals gesendet. Selbst wenn Campaign vor dem Senden standardmäßig eine Deduplizierung durchführt, kann nichts verhindern, dass dieselbe Nachricht von verschiedenen Aktionen gesendet wird, die denselben Inhalt haben, wenn ein Ziel geteilt wird.
* Nicht berücksichtigte Abonnementanforderungen Wenn sich ein Empfänger nach Erhalt einer Nachricht abmeldet, ist sein doppeltes Profil weiterhin für zukünftige Nachrichten zulässig.

Abgesehen von dieser Nebenstufe der Opt-in-Verfahren wird diese Situation die Nutzer wahrscheinlich dazu veranlassen, die Nachrichten als Spam zu betrachten und ein Blacklist-Verfahren beim ISP auszulösen.

Bei der Ausführung von Vorgängen in der Datenbank müssen Sie besonders vorsichtig sein. Um Doppelungen möglichst zu vermeiden, müssen folgende Maßnahmen durchgeführt werden:
* **Importe müssen sorgfältig konfiguriert werden.** Dies ist besonders wichtig bei der Wahl des Aussöhnungsschlüssels.
* **Achten Sie beim Ändern von E-Mail-Adressen darauf.** Geänderte E-Mail-Adressen können auch eine Quelle von Duplikaten sein. Insbesondere können zwei Adressen mit verschiedenen Domänen an denselben Posteingang weitergeleitet werden, zum Beispiel bei einem Unternehmen, das den Namen geändert hat und die ehemalige Domäne für einen bestimmten Zeitraum beibehalten hat: joe.doe@amce-co.com und joe.doe@acme-rebranded.com.
* **Achten Sie bei automatischen Importen darauf.** Unabhängig davon, ob es sich um Listen oder aus anderen Datenbanken handelt, sind diese Elemente bei der Profilverwaltung zu berücksichtigen. Was passiert, wenn Sie ein Profil in einer anderen Partition löschen oder verschieben? Es kann in der ursprünglichen Partition durch einen automatischen Import neu erstellt werden, z. B. wenn eine Bestellung aufgegeben wird.
* **Profile sollten in verschiedene Ordner sortiert werden.**

Es gibt jedoch Fälle, in denen Duplikate zwischen den verschiedenen Partitionen normal sind. Wenn beispielsweise eine Person für Dritte oder andere Unternehmen geschickt wird, ist es logisch, dass dieselbe Person aus unterschiedlichen Gründen Empfänger ist. Es ist jedoch selten normal, Duplikate innerhalb derselben Partition zu finden.

## Quarantänen {#quarantines}

Adobe Campaign verwaltet eine Liste von unter Quarantäne gestellten Adressen. Die Empfänger, deren Adressen unter Quarantäne gestellt werden, werden während der Lieferanalyse standardmäßig ausgeschlossen: sie sind nicht zielgerichtet.

Das Quarantänemanagement ist in [diesem Abschnitt](../../sending/using/understanding-quarantine-management.md)ausführlich beschrieben.

Eine E-Mail-Adresse kann beispielsweise isoliert werden, wenn der Posteingang voll ist oder die Adresse nicht vorhanden ist. In allen Fällen entspricht die Quarantäne den spezifischen Vorschriften in [diesem Abschnitt](../../sending/using/understanding-quarantine-management.md#conditions-for-sending-an-address-to-quarantine).

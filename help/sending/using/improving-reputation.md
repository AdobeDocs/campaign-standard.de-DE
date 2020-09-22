---
title: Verbessern Ihrer Reputation mit Adobe Campaign Standard
description: Erfahren Sie, wie Sie Ihre Reputation mit Adobe Campaign Standard verbessern können, indem Sie doppelte E-Mail-Adressen und Quarantänen verwalten.
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
source-git-commit: 1b1fb4a0dc0f7881e24e10f8ac171feab2ac8cba
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 89%

---


# Verbessern Ihrer Reputation{#improving-reputation}

Um zu vermeiden, dass sich Ihre Empfänger belästigt fühlen, löschen Sie doppelte E-Mail-Adressen aus Ihrer Zielgruppe. Dies sichert Ihre Reputation als Absender und ermöglicht eine ordnungsgemäße Quarantäneverwaltung. Adobe Campaign Angebot die erforderlichen Instrumente, um diese Empfehlungen umzusetzen und die Gefahr zu vermeiden, dass der ISP der Blockierungsliste hinzugefügt wird.

Unten finden Sie Details zur Duplikaten- und Quarantäneverwaltung.

## Duplikate {#duplicates}

Das Vorhandensein doppelter E-Mail-Adressen kann unterschiedliche Konsequenzen haben:
* Dieselbe Nachricht wird mehrfach gesendet. Selbst wenn Campaign vor dem Versand standardmäßig eine Deduplizierung vornimmt, kann die Nachricht durch unterschiedliche Aktionen dennoch mit demselben Inhalt gesendet werden, beispielsweise bei Verwendung einer Aufspaltung der Zielpopulation.
* Abmeldungen werden missachtet. Wenn sich ein Empfänger nach dem Erhalt einer Nachricht abmeldet, können an sein dupliziertes Profil weiterhin Nachrichten gesendet werden.

Abgesehen von dieser Nebenwirkung der Abmeldeverfahren wird diese Situation die Nutzer wahrscheinlich dazu veranlassen, die Nachrichten als Spam zu betrachten und eine Blockierungsliste beim ISP auszulösen.

Bei der Bearbeitung der Datenbank muss besonders vorsichtig vorgegangen werden. Gehen Sie folgendermaßen vor, um Duplikate zu vermeiden:
* **Importe müssen sorgfältig konfiguriert werden.** Das gilt besonders für die Wahl des Abstimmschlüssels.
* **Gehen Sie bei der Änderung von E-Mail-Adressen sorgfältig vor.** Die Änderung von E-Mail-Adressen kann ebenfalls eine Ursache für Duplikate sein. So können zwei Adressen mit unterschiedlichen Domains zum selben Postfach gesendet werden, beispielsweise wenn ein Unternehmen seinen Namen geändert hat, aber für eine gewisse Zeit seine frühere Domain behält: max.mustermann@amce-co.com und max.mustermann@acme-rebranded.com.
* **Gehen Sie bei automatischen Importen sorgfältig vor.** Egal ob die Elemente aus Listen oder aus anderen Datenbanken stammen, sind sie bei der Profilverwaltung zu berücksichtigen. Was geschieht, wenn Sie ein Profil löschen oder in eine andere Partition verschieben? Es kann ggf. in der ursprünglichen Partition durch einen automatischen Import neu erstellt werden, z. B. bei Aufgabe einer Bestellung.
* **Sortieren Sie die Profile und speichern Sie sie in unterschiedlichen Ordnern.**

In gewissen Fällen sind Duplikate in unterschiedlichen Partitionen jedoch normal. Bei Sendungen an Drittparteien oder unterschiedliche Abteilungen in einem Unternehmen kann es beispielsweise vorkommen, dass dieselbe Person mehrfache Sendungen mit unterschiedlichem Zweck empfängt. Duplikate innerhalb derselben Partition treten jedoch nur sehr selten auf.

## Quarantänen {#quarantines}

Adobe Campaign verwaltet eine Liste von unter Quarantäne gestellten Adressen. Empfänger, deren Adressen unter Quarantäne gestellt wurden, werden bei der Versandanalyse standardmäßig ausgeschlossen: Sie gehören nicht zur Zielgruppe.

Die Quarantäneverwaltung wird in diesem [Abschnitt](../../sending/using/understanding-quarantine-management.md) genauer beschrieben.

Eine E-Mail-Adresse kann zum Beispiel unter Quarantäne gestellt werden, weil das Postfach voll ist oder die Adresse nicht existiert. In jedem Fall erfüllt die Quarantäne die spezifischen Vorgaben in [diesem Abschnitt](../../sending/using/understanding-quarantine-management.md#conditions-for-sending-an-address-to-quarantine).

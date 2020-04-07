---
title: Kontrollregeln
description: Hier erfahren Sie, wie Sie mithilfe von Kontrollregeln die Qualitätsprüfung für Ihre Nachrichten verbessern.
page-status-flag: never-activated
uuid: 33a1c90c-534e-4fe1-982c-f4e1858d4d2d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: working-with-typology-rules
discoiquuid: 305cadde-6424-4c6f-b11b-1e8bdbad6ef1
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 40de67f4c918b26de6d306ce6af5cb8832741d6f

---


# Kontrollregeln {#control-rules}

Mit Steuerungsregeln können Sie die Gültigkeit und Qualität der Nachrichten vor dem Senden überprüfen, z. B. Zeichenanzeige, SMS-Größe, Adressformat usw.

>[!NOTE]
>
>Aus Sicherheitsgründen sind Steuerungsregeln schreibgeschützt und können nicht geändert werden.

## Standard-Kontrollregeln {#default-control-rules}

Ein Satz von Standardregeln stellt die Standardsteuerelemente sicher. Die nachstehende Tabelle enthält Informationen zu diesen Regeln sowie zu deren Kanal- und [Ausführungsphase](#control-rules-execution-phases).

| Titel | Channel | Ausführungsphase | Description |
---------|----------|---------|---------
| **[!UICONTROL A/B Test]** | Email | Zu Beginn der Personalisierung | Extrahiert die Testpopulation für einen Versand mit A/B-Test. |
| **[!UICONTROL Check delivery size]** | Alle | Nach der Zielgruppenbestimmung | Überprüft die Größe der Meldungen. |
| **[!UICONTROL Check email content is not empty]** | Email | Nach der Zielgruppenbestimmung | Erzeugt einen Fehler, wenn der Inhalt der Nachricht leer ist. |
| **[!UICONTROL Check In-App content for broadcast template]** | In-App | Personalisierung im Beginn | Überprüft, ob In-App-Inhalte/Auslöser für die Sendevorlage nicht leer sind. |
| **[!UICONTROL Check In-App content for profile template]** | In-App | Zu Beginn der Personalisierung | Überprüft, ob In-App-Inhalte/Auslöser für die Vorlage des Profils nicht leer sind. |
| **[!UICONTROL Check In-App content for subscriber template]** | In-App | Zu Beginn der Personalisierung | Überprüft, ob In-App-Inhalte/Auslöser für die Abonnentenvorlage nicht leer sind. |
| **[!UICONTROL Check proof size]** | Alle | Nach der Zielgruppenbestimmung | Erzeugt eine Fehlermeldung, wenn die Population der Testversand-Zielgruppe 100 Empfänger überschreitet. |
| **[!UICONTROL Check social network sharing link]** | Email | Zu Beginn der Personalisierung | Überprüft das Vorhandensein eines Links zu einer Mirrorseite, wenn ein Link zur Weitergabe über soziale Netzwerke (ViralLinks) in den Inhalt aufgenommen wird. |
| **[!UICONTROL Check subject]** | Email | Zu Beginn der Personalisierung | Überprüft, ob Betreff und Absenderadresse keine Sonderzeichen enthalten, die Probleme bei bestimmten Postübermittlern verursachen können, und prüft, ob der Betreff der Nachricht ausgefüllt wurde. |
| **[!UICONTROL Check unsubscription link]** | Email | Zu Beginn der Personalisierung | Prüft, ob in jedem Inhalt (HTML und Text) mindestens eine Abmeldung (Ausschluss-URL) vorhanden ist. |
| **[!UICONTROL Check URL labels]** | Email | Zu Beginn der Personalisierung | Überprüft, ob jede Tracking-URL eine Beschriftung enthält. |
| **[!UICONTROL Check URLs]** | Email | Zu Beginn der Personalisierung | Überprüft die Tracking-URLs (Vorhandensein des Zeichens &quot;&amp;&quot;). |

## Ausführungsphasen von Steuerungsregeln (Kontroll-, Regelausführungsphasen)

Steuerungsregeln können auf verschiedene Phasen des Lebenszyklus des Versands angewendet werden:

* **Beginn des Targeting**: Die Steuerungsregel kann an dieser Stelle angewendet werden, sodass der Personalisierungsschritt im Ereignis eines Fehlers nicht ausgeführt wird.

* **Nach dem Targeting**: Die Ausführung nach dem Targeting ermöglicht es Ihnen, das Volumen der Zielgruppe zu kennen, um die Kontrollregel anzuwenden.

   So wird beispielsweise die Kontrollregel **Prüfung der Testversandgröße** nach der Zielgruppenbestimmung angewendet: Diese Regel verhindert die Vorbereitung der Nachrichtenpersonalisierung, wenn zu viele Testversand-Empfänger vorhanden sind.

* **Zu Beginn der Personalisierung**: Gilt, wenn sich die Prüfung auf die Genehmigung zur Personalisierung der Nachricht bezieht. Die Nachrichtenpersonalisierung erfolgt während der Analysephase.

* **Am Ende der Analyse**: Wenn ein Scheck personalisiert werden muss, muss er abgeschlossen sein.

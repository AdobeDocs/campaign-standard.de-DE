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
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '488'
ht-degree: 100%

---


# Kontrollregeln {#control-rules}

Mit Kontrollregeln können Sie die Gültigkeit und Qualität der Nachrichten vor dem Versand überprüfen. Dabei werden beispielsweise die Zeichenanzeige, die Größe von SMS-Nachrichten und das Adressformat überprüft.

>[!NOTE]
>
>Aus Sicherheitsgründen sind Kontrollregeln schreibgeschützt und können nicht geändert werden.

## Standard-Kontrollregeln {#default-control-rules}

Ein Satz von Standardregeln stellt die Standardkontrollen sicher. Die nachstehende Tabelle enthält Informationen zu diesen Regeln sowie zu deren Kanal und [Ausführungsphasen](#control-rules-execution-phases).

| Titel | Kanal | Ausführungsphase | Beschreibung |
---------|----------|---------|---------
| **[!UICONTROL A/B-Test]** | E-Mail | Zu Beginn der Personalisierung | Extrahiert die Testpopulation für einen Versand mit A/B-Test. |
| **[!UICONTROL Prüfung der Versandgröße]** | Alle | Nach der Zielgruppenbestimmung | Überprüft die Größe der Nachrichten. |
| **[!UICONTROL Prüfen, dass der E-Mail-Inhalt nicht leer ist]** | E-Mail | Nach der Zielgruppenbestimmung | Erzeugt einen Fehler, wenn der Inhalt der Nachricht leer ist. |
| **[!UICONTROL Prüfung des In-App-Inhalts auf Broadcast-Vorlage]** | In-App | Zu Beginn der Personalisierung | Stellt sicher, dass In-App-Inhalte/Triggers für die Broadcast-Vorlage nicht leer sind. |
| **[!UICONTROL Prüfung des In-App-Inhalts auf Profil-Vorlage]** | In-App | Zu Beginn der Personalisierung | Stellt sicher, dass In-App-Inhalte/Triggers für die Profilvorlage nicht leer sind. |
| **[!UICONTROL Prüfung des In-App-Inhalts auf Abonnentenvorlage]** | In-App | Zu Beginn der Personalisierung | Stellt sicher, dass In-App-Inhalte/Triggers für die Abonnentenvorlage nicht leer sind. |
| **[!UICONTROL Prüfung der Testversandgröße]** | Alle | Nach der Zielgruppenbestimmung | Erzeugt eine Fehlermeldung, wenn die Population der Testversand-Zielgruppe 100 Empfänger überschreitet. |
| **[!UICONTROL Prüfung der Teilen-Links zu den sozialen Netzwerken]** | E-Mail | Zu Beginn der Personalisierung | Überprüft, wenn im Inhalt ein Link zum Teilen in sozialen Netzwerken (ViralLinks) enthalten ist, ob der dann nötige Mirrorseiten-Link ebenfalls enthalten ist. |
| **[!UICONTROL Prüfung des Betreffs]** | E-Mail | Zu Beginn der Personalisierung | Stellt sicher, dass der Betreff und die Absenderadresse keine Sonderzeichen enthalten, die bei bestimmten Mail Transfer Agents Probleme verursachen können, und dass der Nachrichtenbetreff ausgefüllt wurde. |
| **[!UICONTROL Prüfung des Abmelde-Links]** | E-Mail | Zu Beginn der Personalisierung | Prüft, ob in jedem Inhalt (HTML und Text) mindestens eine URL vom Typ &quot;Abmeldung&quot; (Opt-out) enthalten ist. |
| **[!UICONTROL Prüfung der URL-Titel]** | E-Mail | Zu Beginn der Personalisierung | Überprüft, ob jede Tracking-URL einen Titel hat. |
| **[!UICONTROL Prüfung der URLs]** | E-Mail | Zu Beginn der Personalisierung | Überprüft die Tracking-URLs (Vorhandensein des &quot;&amp;&quot;-Zeichens). |

## Ausführungsphasen von Kontrollregeln {#control-rules-execution-phases}

Kontrollregeln können auf verschiedene Phasen des Lebenszyklus eines Versands angewendet werden:

* **Zu Beginn der Zielgruppenbestimmung**: Die Kontrollregel kann in dieser Phase angewendet werden, sodass der Personalisierungsschritt im Fall eines Fehlers nicht ausgeführt wird.

* **Nach der Zielgruppenbestimmung**: Durch eine Ausführung nach der Zielgruppenbestimmung kennen Sie den Umfang der Zielgruppe und können die Kontrollregel entsprechend anwenden.

   So wird beispielsweise die Kontrollregel **Prüfung der Testversandgröße** nach der Zielgruppenbestimmung angewendet: Diese Regel verhindert die Vorbereitung der Nachrichtenpersonalisierung, wenn zu viele Testversand-Empfänger vorhanden sind.

* **Zu Beginn der Personalisierung**: Gilt, wenn sich die Prüfung auf die Validierung der Nachrichtenpersonalisierung bezieht. Die Nachrichtenpersonalisierung erfolgt während der Analysephase.

* **Am Ende der Analyse**: Wenn eine Prüfung verlangt, dass die Nachrichtenpersonalisierung abgeschlossen ist.

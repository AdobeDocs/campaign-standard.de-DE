---
title: Prognostizierende Benutzerinteraktionsfunktionen
description: Erfahren Sie, wie Sie mit Prognosen zur Sendezeit und Interaktionsbewertung arbeiten.
page-status-flag: never-activated
uuid: c2c13934-9819-4e18-b5c7-60915c907f37
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: sending
content-type: reference
topic-tags: ai-powered-emails
discoiquuid: 609355f6-9003-41b9-9981-ea787419fbf5
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c277a6cb18e9a1d83f8a2632049e7cea36414052
workflow-type: tm+mt
source-wordcount: '1070'
ht-degree: 2%

---


# Optimieren von Design und Versand mit AI-basierten E-Mails{#journey-ai}

## Get started with AI-powered emails{#journey-ai-ovv}

Mithilfe der Kampagne können Sie die Gestaltung und den Versand von Kundenreisen optimieren, um die Interaktionsvorlieben jedes Einzelnen vorherzusagen. Mit der Journey-API kann Adobe Campaign Öffnungsraten, optimale Sendezeiten und wahrscheinliche Abwanderungszahlen anhand historischer Interaktionsmetriken analysieren und vorhersagen.

**Modelle für maschinelles Lernen**

Adobe Campaign Standard Angebot zwei neue Modelle für maschinelles Lernen: **Predictive Send Time Optimizations** und **Predictive Interaktionsbewertung**. Diese beiden Modelle werden zusammen als &quot;Journey AI&quot; bezeichnet, eine Klasse von maschinellen Lernmodellen, die sich speziell auf die Gestaltung und Bereitstellung besserer Kundenreisen beziehen.

* **Predictive Sende-Zeitoptimierung**: Prognostizierende Zeitoptimierung für den Versand sagt voraus, welche die beste Sendezeit für jedes Empfänger-Profil für E-Mail-Öffnen oder -Klicks ist. Für jedes Profil des Empfängers geben die Ergebnisse die beste Sendezeit für jeden Wochentag an und welcher Wochentag ist der beste, um optimale Ergebnisse zu erzielen.

* **Bewertung** der voraussichtlichen Interaktion: Prognostische Interaktionsbewertungen prognostizieren die Wahrscheinlichkeit, mit der ein Empfänger mit einer Nachricht interagiert, sowie die Wahrscheinlichkeit, dass er sich innerhalb der nächsten 7 Tage nach dem nächsten E-Mail-Versand abmeldet (abbestellt). Die Wahrscheinlichkeiten werden je nach dem spezifischen Risiko des Rückzugs, mittel oder niedrig, weiter in Behälter unterteilt. Dasselbe Modell bietet den Kunden auch den Rang eines Risikoperzentils, um zu verstehen, wo der Rang eines bestimmten Kunden im Verhältnis zu anderen steht.

>[!CAUTION]
>Diese Funktion ist im Lieferumfang des Produkts nicht verfügbar. Die Implementierung erfordert die Einbindung von Adobe Consulting. Wenden Sie sich an Ihren Kundenbetreuer, um weitere Informationen zu erhalten.
>
>Die Funktion erfordert die Verwendung einer Azurblauen Datenspeicherung, die vom Kunden bereitgestellt werden muss.

## Predictive send time optimization{#predictive-send-time}

### Optimieren von Klicks und Öffnen{#about-predictive-send-time}

Prognostizierende Zeitoptimierung für den Versand prognostiziert, welche die beste Sendezeit für jedes Empfänger-Profil für E-Mail-Öffnen und -Klicks ist. Für jedes Profil des Empfängers geben die Ergebnisse die beste Sendezeit für jeden Wochentag an und welcher Wochentag ist der beste, um optimale Ergebnisse zu erzielen.

Im Predictive Send Time Optimization-Modell gibt es zwei Untermodelle:
* Prognosezeit für das Öffnen ist die beste Zeit, zu der eine Kommunikation an den Kunden gesendet werden muss, um das Öffnen zu maximieren.
* Prognosezeit für Klicks ist die beste Zeit, zu der eine Kommunikation an den Kunden gesendet werden muss, um Klicks zu maximieren.

**Modelleingabe**: Versandlogs, Trackinglogs und Profil-Attribute (Nicht-PII)

**Modellausgabe**: Optimale Zeit zum Senden einer Nachricht (für Öffnen und Klicks)


Ausgabedetails

* Berechnen Sie die beste Tageszeit für den Versand einer E-Mail an den 7 Wochentagen in Intervallen von 1 Stunde (z.B.: 9:00 Uhr, 10:00 Uhr, 11:00 Uhr)
* Das Modell zeigt den besten Tag in der Woche und die beste Stunde an diesem Tag an
* Jede optimale Zeit wird zweimal berechnet: einmal zur Maximierung der offenen Rate und einmal zur Maximierung der Klickrate
* Es werden 16 Felder angegeben (14 für Wochentage und 2 für die ganze Woche):
   * beste Zeit, eine E-Mail zu senden, um Klicks für Montag zu optimieren - Werte zwischen 0 und 23
   * beste Zeit, eine E-Mail zu senden, um die Öffnung für Montag zu optimieren - Werte zwischen 0 und 23
   * beste Zeit, um eine E-Mail zu senden, um Klicks für Dienstag zu optimieren - Werte zwischen 0 und 23
   * ...
   * beste Zeit, um eine E-Mail zu senden, um Klicks für Sonntag zu optimieren - Werte zwischen 0 und 23
   * beste Zeit, eine E-Mail zu senden, um die Öffnung für Sonntag zu optimieren - Werte zwischen 0 und 23
   * ...
   * Der beste Tag, um eine E-Mail zu senden, um die Optimierung geöffnet für die ganze Woche - Montag bis Sonntag
   * beste Zeit, eine E-Mail zu senden, um die Öffnung für die ganze Woche - Werte zwischen 0 und 23

>[!NOTE]
>
>Diese Prognosefunktionen gelten nur für E-Mail-Versand.
>
>Das Modell benötigt mindestens einen Monat Daten, um signifikante Ergebnisse zu erzielen.


### Profil-Ergebnisse aufrufen{#access-predictive-send-time-scores}

Nach der Implementierung in die Kampagne bereichern maschinelle Lernfunktionen die Daten von Profilen mit neuen Registerkarten mit den besten open/click-Ergebnissen. Die Metriken werden von der Journey AI berechnet und mithilfe von Technischen Workflows in die Kampagne gebracht.

Um auf diese Metriken zugreifen zu können, müssen Sie:

1. Öffnen Sie ein Profil und klicken Sie auf &quot;Bearbeiten&quot;.

1. Klicken Sie auf die Registerkarte **Zeitbewertung nach Klick** senden oder **Zeitbewertung nach Öffnen** senden.

Standardmäßig erhalten die Profil-Ergebnisse die beste Wochentagszeit und die beste Gesamtwochenzeit.

![](assets/do-not-localize/SendTimeScore.png)

### Senden von Nachrichten im besten Moment{#use-predictive-send-time}

Damit die E-Mails zum optimalen Zeitpunkt pro Profil gesendet werden, muss der Versand mit der Option **[!UICONTROL Senden zu einem durch eine Formel]**definierten benutzerspezifischen Zeitpunkt geplant werden.
Erfahren Sie, wie das Versanddatum [in diesem Abschnitt](../../sending/using/computing-the-sending-date.md)berechnet wird.

Die Formel muss mit der jeweils besten Uhrzeit des jeweiligen Tages gefüllt werden, an dem der Versand ausgeht.

![](assets/do-not-localize/ComputeSendingDate.png)

Beispiel für die Formel:

```
AddHours([currentDelivery/scheduling/@contactDate], 
[cusSendTimeScoreByClickprofile_link/@EMAIL_BEST_TIME_TO_CLICK_WEDNESDAY])
```

![](assets/do-not-localize/SendingDateFormula.png)

>[!NOTE]
>
>Das Datenmodell kann je nach Implementierung unterschiedlich sein.



## Bewertung der voraussichtlichen Interaktion {#predictive-scoring}

Mit der Ergebnisbewertung der prognostizierten Interaktion können Sie:

* **Wählen Sie eine Audience** aus: Mithilfe der Aktivität &quot;Abfrage&quot;können Sie die Audience auswählen, mit der eine bestimmte Nachricht gesendet werden soll
* **Eine Audience** ausschließen: mithilfe der Abfrage-Aktivität können Sie die Audience entfernen, die Sie abbestellen möchten
* **Personalisieren**: personalisieren Sie die Nachricht basierend auf der Interaktionsstufe (hochengagierte Benutzer erhalten eine andere Nachricht als nicht engagierte)

Dieses Modell verwendet mehrere Ergebnisse, um Folgendes anzugeben:

* **Interaktionsbewertung öffnen/Interaktionsbewertung** anklicken: Dieser Wert entspricht der Wahrscheinlichkeit, mit der ein Abonnent eine bestimmte Nachricht (Öffnen oder Klicken) erhält. Die Werte liegen zwischen 0,0 und 1,0.
* **Wahrscheinlichkeit** der Abmeldung: dieser Wert entspricht der Wahrscheinlichkeit, dass Empfänger sich bei einer geöffneten E-Mail von einem E-Mail-Kanal abmelden. Die Werte liegen zwischen 0,0 und 1,0.
* **Treuestufe**:  dieser Wert unterteilt Benutzer in drei Stufen: niedrig, mittel und hoch. Hoch ist höchstwahrscheinlich bei der Marke zu bleiben und niedriger Wert wahrscheinlich abmelden.
* **Perzentil-Retentionsgrad**: profil-Rang in Bezug auf die Wahrscheinlichkeit der Abmeldung. Die Werte liegen zwischen 0,0 und 1,0. Wenn der prozentuale Anteil der Retentionsrate beispielsweise 0,953 beträgt, bleibt dieser Empfänger eher bei der Marke und wird sich weniger abmelden als 95,3 % aller Empfänger.

>[!NOTE]
>
>Diese Prognosefunktionen gelten nur für E-Mail-Versand.
>
>Das Modell benötigt mindestens einen Monat Daten, um signifikante Ergebnisse zu erzielen.


**Modelleingabe**: Versandlogs, Trackinglogs und spezifische Profil-Attribute

**Modellausgabe**: Ein Profil-Attribut, das die Bewertung und Kategorie des Profils beschreibt


### Einsatz des Interaktionswerts für den E-Mail-Kanal

Um auf diese Metriken zugreifen zu können, müssen Sie:

1. Öffnen Sie ein Profil und klicken Sie auf &quot;Bearbeiten&quot;.

1. Klicken Sie auf die Registerkarte **Interaktionswerte für E-Mail-Kanal** .

Durch die Verwendung einer Abfrage-Aktivität in einem Workflow können Sie das Ergebnis zur Optimierung Ihrer Audience verwenden.

Beispielsweise mit den Kriterien für die **Treuestuh** :

![](assets/do-not-localize/predictive_score_query.png)
























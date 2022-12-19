---
title: Prädiktive Benutzerinteraktionsfunktionen
description: Erfahren Sie, wie Sie die prädiktive Sendezeit und Interaktionsbewertung verwenden.
audience: sending
content-type: reference
topic-tags: ai-powered-emails
feature: Send Time Optimization
role: User
level: Intermediate
exl-id: e1cb04e6-eb38-4bcc-b071-321cc11ccc7e
source-git-commit: c5b417144836a86307d91cec981db23581807ff7
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 100%

---

# Gestaltung und Versand mit KI-gestützten E-Mails optimieren{#journey-ai}

## Erste Schritte mit KI-gestützten E-Mails{#journey-ai-ovv}

Mit Campaign können Sie die Gestaltung und den Versand von Customer Journeys optimieren, um die Interaktionsvorlieben von Kontakten vorherzusagen. Mit Journey AI kann Adobe Campaign Öffnungsraten, optimale Sendezeiten und wahrscheinliche Abwanderungszahlen anhand historischer Interaktionsmetriken analysieren und vorhersagen.

**Modelle für maschinelles Lernen**

Adobe Campaign Standard bietet zwei neue Modelle für maschinelles Lernen: **Prädiktive Sendezeitoptimierung** und **Prädiktive Interaktionsbewertung**. Diese beiden Modelle werden zusammen als Journey AI bezeichnet, eine Klasse von Modellen für maschinelles Lernen, die speziell für die Gestaltung und die Bereitstellung besserer Customer Journeys entwickelt wurden.

* **Prädiktive Sendezeitoptimierung**: Die prädiktive Sendezeitoptimierung sagt für jedes Empfängerprofil voraus, welches die beste Sendezeit für E-Mail-Öffnungen oder Klicks ist. Für jedes Empfängerprofil geben die Bewertungen an, was die beste Sendezeit für jeden Wochentag ist und welcher Wochentag beim Senden die besten Ergebnisse liefert.

* **Prädiktive Interaktionsbewertung**: Die prädiktive Interaktionsbewertung sagt die Wahrscheinlichkeit voraus, dass sich ein Empfänger mit einer Nachricht beschäftigt, sowie die Wahrscheinlichkeit, dass er sich innerhalb von sieben Tagen nach dem nächsten E-Mail-Versand abmeldet. Die Wahrscheinlichkeiten werden je nach dem spezifischen Risiko des Rückzugs (mittel oder niedrig) weiter in Behälter unterteilt. Zusammen mit diesen liefert das Modell auch den Risikoperzentil-Rang, damit die Kunden den Rang eines bestimmten Kunden im Verhältnis zu anderen verstehen können.

>[!IMPORTANT]
>Diese Funktion ist im Lieferumfang des Produkts nicht verfügbar. Die Implementierung erfordert die Einbindung von Adobe Consulting. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um weitere Informationen zu erhalten.

## Prädiktive Sendezeitoptimierung{#predictive-send-time}

### Klicks und Öffnungen optimieren{#about-predictive-send-time}

Die prädiktive Sendezeitoptimierung sagt für jedes Empfängerprofil voraus, welches die beste Sendezeit für E-Mail-Öffnungen und Klicks ist. Für jedes Empfängerprofil geben die Bewertungen an, was die beste Sendezeit für jeden Wochentag ist und welcher Wochentag beim Senden die besten Ergebnisse liefert.

Im prädiktiven Sendezeitoptimierungsmodell gibt es zwei Untermodelle:
* Die prädiktive Sendezeit für Öffnungen ist die beste Zeit, zu der eine Kommunikation an den Kunden gesendet werden muss, um Öffnungen zu maximieren.
* Die prädiktive Sendezeit für Klicks ist die beste Zeit, zu der eine Kommunikation an den Kunden gesendet werden muss, um Klicks zu maximieren.

**Modelleingabe**: Versandlogs, Trackinglogs und Profilattribute (Nicht-PII)

**Modellausgabe**: Optimale Zeit zum Senden einer Nachricht (für Öffnungen und Klicks)


Ausgabedetails

* Berechnen Sie die beste Tageszeit für den Versand einer E-Mail an den sieben Wochentagen in Intervallen von einer Stunde (z. B.: 9:00 Uhr, 10:00 Uhr, 11:00 Uhr).
* Das Modell zeigt den besten Tag der Woche und die beste Stunde an diesem Tag an.
* Jede optimale Zeit wird zweimal berechnet: einmal zur Maximierung der Öffnungsrate und einmal zur Maximierung der Klickrate.
* Es werden 16 Felder angegeben (14 für die Wochentage und 2 für die ganze Woche):
   * beste Zeit, um eine E-Mail zu senden, um Klicks für Montag zu optimieren – Werte zwischen 0 und 23
   * beste Zeit, um eine E-Mail zu senden, um Öffnungen für Montag zu optimieren – Werte zwischen 0 und 23
   * beste Zeit, um eine E-Mail zu senden, um Klicks für Dienstag zu optimieren – Werte zwischen 0 und 23
   * ...
   * beste Zeit, um eine E-Mail zu senden, um Klicks für Sonntag zu optimieren – Werte zwischen 0 und 23
   * beste Zeit, um eine E-Mail zu senden, um Öffnungen für Sonntag zu optimieren – Werte zwischen 0 und 23
   * ...
   * bester Tag, um eine E-Mail zu senden, um die Öffnungen für die ganze Woche zu optimieren – Montag bis Sonntag
   * beste Zeit, um eine E-Mail zu senden, um Öffnungen für die ganze Woche zu optimieren – Werte zwischen 0 und 23

>[!NOTE]
>
>Diese prädiktiven Funktionen gelten nur für den E-Mail-Versand.
>
>Das Modell benötigt mindestens einen Monat an Daten, um signifikante Ergebnisse zu erzielen.


### Profilbewertungen aufrufen{#access-predictive-send-time-scores}

Nach der Implementierung in Campaign reichern die Funktionen für maschinelles Lernen die Profildaten mit neuen Tabs mit den besten Öffnungs- /Klickbewertungen an. Die Metriken werden von Journey AI berechnet und mithilfe technischer Workflows in Campaign übernommen.

Um auf diese Metriken zuzugreifen:

1. Öffnen Sie ein Profil und klicken Sie auf &quot;Bearbeiten&quot;.

1. Klicken Sie auf den Tab **Sendezeitbewertung nach Klick** oder **Sendezeitbewertung nach Öffnung**.

Standardmäßig geben die Profilbewertungen die beste Tageszeit für jeden Wochentag und die beste Zeit für die gesamte Woche an.

![](assets/do-not-localize/SendTimeScore.png)

### Nachrichten zum besten Zeitpunkt senden{#use-predictive-send-time}

Damit die E-Mails zum optimalen Zeitpunkt pro Profil gesendet werden, muss der Versand mit der Option **[!UICONTROL Zu einem durch eine Formel definierten Datum senden]** geplant werden.
Erfahren Sie [in diesem Abschnitt](../../sending/using/computing-the-sending-date.md), wie Sie das Versanddatum berechnen.

Die Formel muss mit der besten Tageszeit des jeweiligen Tages ausgefüllt werden, an dem der Versand ausgeführt werden soll.

![](assets/do-not-localize/ComputeSendingDate.png)

Beispiel einer Formel:

```
AddHours([currentDelivery/scheduling/@contactDate], 
[cusSendTimeScoreByClickprofile_link/@EMAIL_BEST_TIME_TO_CLICK_WEDNESDAY])
```

![](assets/do-not-localize/SendingDateFormula.png)

>[!NOTE]
>
>Das Datenmodell kann je nach Implementierung unterschiedlich sein.


## Prädiktive Interaktionsbewertung {#predictive-scoring}

Mit der prädiktiven Interaktionsbewertung können Sie Folgendes:

* **Eine Audience auswählen**: Mithilfe der Abfrageaktivität können Sie die Audience auswählen, an die eine bestimmte Nachricht gesendet werden soll.
* **Eine Audience ausschließen**: Mithilfe der Abfrageaktivität können Sie die Audience entfernen, die sich abmelden möchte.
* **Personalisieren**: Personalisieren Sie die Nachricht basierend auf dem Grad der Interaktion (stark interaktive Benutzer erhalten eine andere Nachricht als nicht interaktive).

Dieses Modell verwendet mehrere Bewertungen, um Folgendes anzugeben:

* **Interaktionsbewertung für Öffnungen/Interaktionsbewertung für Klicks**: Dieser Wert entspricht der Wahrscheinlichkeit, mit der sich ein Abonnent mit einer bestimmte Nachricht beschäftigt (Öffnung oder Klick). Die Werte liegen zwischen 0,0 und 1,0.
* **Abmeldewahrscheinlichkeit**: Dieser Wert entspricht der Wahrscheinlichkeit, dass der Empfänger sich von einem E-Mail-Kanal abmeldet, nachdem er eine E-Mail geöffnet hat. Die Werte liegen zwischen 0,0 und 1,0.
* **Bindungsgrad**: Dieser Wert unterteilt Benutzer in drei Stufen: niedrig, mittel und hoch. Dabei bedeutet &quot;hoch&quot;, dass sie höchstwahrscheinlich bei der Marke bleiben, und &quot;niedrig&quot;, dass sie sich wahrscheinlich abmelden.
* **Perzentilrang der Bindung**: Rang des Profils in Bezug auf die Abmeldewahrscheinlichkeit. Die Werte liegen zwischen 0,0 und 1,0. Wenn der Perzentilrang der Bindung beispielsweise 0,953 beträgt, bleibt dieser Empfänger mit größerer Wahrscheinlichkeit bei der Marke und hat eine geringere Wahrscheinlichkeit, sich abzumelden, als 95,3 % aller Empfänger.

>[!NOTE]
>
>Diese prädiktiven Funktionen gelten nur für den E-Mail-Versand.
>
>Das Modell benötigt mindestens einen Monat an Daten, um signifikante Ergebnisse zu erzielen.


**Modelleingabe**: Versandlogs, Trackinglogs und spezifische Profilattribute

**Modellausgabe**: Ein Profilattribut, das die Bewertung und Kategorie des Profils beschreibt.


### Interaktionsbewertung für den E-Mail-Kanal verwenden

Um auf diese Metriken zuzugreifen:

1. Öffnen Sie ein Profil und klicken Sie auf &quot;Bearbeiten&quot;.

1. Klicken Sie auf den Tab **Interaktionsbewertungen für E-Mail-Kanal**.

Wenn Sie eine Abfrageaktivität in einem Workflow verwenden, können Sie die Bewertung zur Optimierung Ihrer Audience nutzen.

Beispielsweise mit den Kriterien für den **Bindungsgrad**:

![](assets/do-not-localize/predictive_score_query.png)
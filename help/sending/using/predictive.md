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
TQID: https://experienceleague.adobe.com/fDzmrslmo3YdV0vVeGlC2SOWdATbYlUyGD6C-kLbSMY
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 1126
ht-degree: 100%

---

# Prädiktive Benutzerinteraktionsfunktionen {#journey-ai}

Mit Campaign können Sie die Gestaltung und den Versand von Customer Journeys optimieren, um die Interaktionsvorlieben von Kontakten vorherzusagen. Mit der auf KI und maschinellem Lernen basierenden Sendezeitoptimierung und der prädiktiven Interaktionsbewertung von Adobe Campaign können Öffnungsraten, optimale Sendezeiten und wahrscheinliche Abwanderung auf der Grundlage historischer Interaktionsmetriken analysiert und vorhergesagt werden.

>[!IMPORTANT]
>
>Diese Funktion ist nicht im Produkt vorkonfiguriert. Die Implementierung erfordert die Einbindung von Adobe Consulting. Wenden Sie sich an Ihren Adobe-Support-Mitarbeiter, um weitere Informationen zu erhalten.

Adobe Campaign bietet zwei neue Modelle für maschinelles Lernen: **Prädiktive Sendezeitoptimierung** und **Prädiktive Interaktionsbewertung**. Bei diesen beiden Modellen handelt es sich um Modelle für maschinelles Lernen, die speziell für die Erstellung und Bereitstellung besserer Customer Journeys entwickelt wurden.

* **Die prädiktive Sendezeitoptimierung** prognostiziert für jedes Empfängerprofil den besten Sendezeitpunkt für E-Mail-Öffnungen oder -Klicks und für Öffnungen von Push-Nachrichten. Für jedes Empfängerprofil kann anhand von Werten festgestellt werden, was die beste Sendezeit für jeden Wochentag ist und welcher Wochentag beim Senden die besten Ergebnisse liefert.

* Die **prädiktive Interaktionsbewertung** sagt die Wahrscheinlichkeit voraus, mit der ein Empfänger mit einer Nachricht interagiert, sowie die Wahrscheinlichkeit, mit der er sich innerhalb der nächsten sieben Tage nach dem nächsten E-Mail-Versand abmeldet. Die Wahrscheinlichkeiten werden je nach vorhergesagter Interaktion mit Ihrem Inhalt in verschiedene Kategorien eingeteilt: hoch, mittel oder niedrig. Diese Modelle liefern auch den Perzentilrang des Abo-Abmelderisikos für die Kundinnen und Kunden, um zu verdeutlichen, wo der Rang einer/eines bestimmten Kundin/Kunden im Vergleich zu anderen liegt.

## Prädiktive Sendezeitoptimierung{#predictive-send-time}

Die prädiktive Sendezeitoptimierung prognostiziert für jedes Empfängerprofil den besten Sendezeitpunkt für E-Mail-Öffnungen oder -Klicks und für Push-Nachrichten-Öffnungen. Für jedes Empfängerprofil kann anhand von Werten festgestellt werden, was die beste Sendezeit für jeden Wochentag ist und welcher Wochentag beim Senden die besten Ergebnisse liefert.

Innerhalb des prädiktiven Sendezeit-Optimierungsmodells gibt es zwei Untermodelle:

* **Die prädiktive Sendezeit für Öffnungen ist die beste Zeit, zu der eine Kommunikation an den Kunden gesendet werden muss, um Öffnungen zu maximieren.**

* **Die prädiktive Sendezeit für Klicks ist die beste Zeit, zu der eine Kommunikation an den Kunden gesendet werden muss, um Klicks zu maximieren.**

**Modelleingabe**: Versandlogs, Trackinglogs und Profilattribute (Nicht-PII)

**Modellausgabe**: Optimale Zeit zum Senden einer Nachricht (für Öffnungen und Klicks)

Ausgabedetails

* Berechnet die beste Tageszeit für den Versand einer E-Mail an den sieben Wochentagen in Intervallen von einer Stunde (z. B.: 9:00 Uhr, 10:00 Uhr, 11:00 Uhr)
* Das Modell zeigt den besten Tag der Woche und die beste Stunde an diesem Tag an.
* Jede optimale Zeit wird zweimal berechnet: einmal zur Maximierung der Öffnungsrate und einmal zur Maximierung der Klickrate.
* Es werden 16 Felder angegeben (14 für die Wochentage und 2 für die ganze Woche):

* Die beste Zeit zum Senden einer E-Mail, um Klicks für Montag zu optimieren – Werte zwischen 0 und 23

* Die beste Zeit zum Senden einer E-Mail, um Öffnungen für Montag zu optimieren – Werte zwischen 0 und 23
* ...
* Die beste Zeit zum Senden einer E-Mail, um Klicks für Sonntag zu optimieren – Werte zwischen 0 und 23
* Die beste Zeit zum Senden einer E-Mail, um Öffnungen für Sonntag zu optimieren – Werte zwischen 0 und 23
* ...
* Der beste Tag zum Senden einer E-Mail, um die Öffnungen für die ganze Woche zu optimieren – Montag bis Sonntag
* Die beste Zeit zum Senden einer E-Mail, um Öffnungen für die ganze Woche zu optimieren – Werte zwischen 0 und 23

>[!NOTE]
>
>Das Modell benötigt mindestens einen Monat an Daten, um signifikante Ergebnisse zu erzielen.
>
>Diese prädiktiven Funktionen sind nur für E-Mail- und Push-Kanäle verfügbar.

Nach der Implementierung in Campaign reichern die Funktionen für maschinelles Lernen die Profildaten mit neuen Registerkarten mit den besten Öffnungs-/Klickbewertungen an. Die Metriken werden mithilfe technischer Workflows berechnet und in Campaign eingebracht.

Um auf diese Metriken zuzugreifen:

1. Öffnen Sie ein Profil und klicken Sie auf &quot;Bearbeiten&quot;.

1. Klicken Sie auf den Tab **Sendezeitbewertung nach Klick** oder **Sendezeitbewertung nach Öffnung**.

Standardmäßig geben die Profilbewertungen die beste Tageszeit für jeden Wochentag und die beste Zeit für die gesamte Woche an.

![](assets/do-not-localize/SendTimeScore.png)

### Nachrichten zum besten Zeitpunkt senden{#use-predictive-send-time}

Damit die E-Mails zum optimalen Zeitpunkt je nach Profil gesendet werden, muss der Versand mit der Option **[!UICONTROL Zu einem durch eine Formel definierten Datum senden]** geplant werden.

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

Die Bewertung prädiktiver Interaktionen sagt die Wahrscheinlichkeit voraus, mit der Empfangende mit einer Nachricht interagieren, sowie die Wahrscheinlichkeit, mit der sie sich innerhalb der nächsten sieben Tage nach dem nächsten E-Mail-Versand abmelden.

Die Wahrscheinlichkeiten werden je nach vorhergesagter Interaktion mit Ihrem Inhalt in verschiedene Kategorien eingeteilt: hoch, mittel oder niedrig. Diese Modelle liefern auch den Perzentilrang des Abo-Abmelderisikos für die Kundinnen und Kunden, um zu verdeutlichen, wo der Rang einer/eines bestimmten Kundin/Kunden im Vergleich zu anderen liegt.

Mit der Bewertung prädiktiver Interaktionen können Sie Folgendes tun:

* **Eine Zielgruppe auswählen**: Mithilfe der Abfrageaktivität können Sie die Zielgruppe auswählen, an die eine bestimmte Nachricht gesendet werden soll.
* **Ausschluss einer Zielgruppe**: Mithilfe der Abfrageaktivität können Sie die Zielgruppe entfernen, die mit höherer Wahrscheinlichkeit das Abo beendet
* **Personalisieren**: Personalisieren Sie die Nachricht basierend auf dem Grad der Interaktion (hochgradig interaktive Benutzende erhalten eine andere Nachricht als nicht interaktive).

Dieses Modell verwendet mehrere Bewertungen, um Folgendes anzugeben:

* **Interaktionsbewertung für Öffnungen/Interaktionsbewertung für Klicks**: Dieser Wert entspricht der Wahrscheinlichkeit, mit der sich ein Abonnent mit einer bestimmte Nachricht beschäftigt (Öffnung oder Klick). Die Werte liegen zwischen 0,0 und 1,0.
* **Abmeldewahrscheinlichkeit**: Dieser Wert entspricht der Wahrscheinlichkeit, dass der Empfänger ein E-Mail-Kanal-Abo beendet, nachdem er eine E-Mail geöffnet hat. Die Werte liegen zwischen 0,0 und 1,0.
* **Bindungsgrad**: Dieser Wert unterteilt Benutzende in drei Stufen: niedrig, mittel und hoch. Dabei bedeutet &quot;hoch&quot;, dass sie höchstwahrscheinlich bei der Marke bleiben, und &quot;niedrig&quot;, dass sie sich wahrscheinlich abmelden.
* **Perzentilrang der Bindung**: Rang des Profils in Bezug auf die Abmeldewahrscheinlichkeit. Die Werte liegen zwischen 0,0 und 1,0. Wenn der Perzentilrang der Bindung beispielsweise 0,953 beträgt, bleibt dieser Empfänger bzw. diese Empfängerin mit größerer Wahrscheinlichkeit bei der Marke und hat eine geringere Wahrscheinlichkeit das Abo zu beenden als 95,3 % aller Empfänger bzw. Empfängerinnen.

>[!NOTE]
>
>Diese prädiktiven Funktionen gelten nur für den E-Mail-Versand.
>
>Das Modell benötigt mindestens einen Monat an Daten, um signifikante Ergebnisse zu erzielen.

**Modelleingabe**: Versandlogs, Trackinglogs und spezifische Profilattribute

**Modellausgabe**: Ein Profilattribut, das die Bewertung und Kategorie des Profils beschreibt.

Um auf diese Metriken zuzugreifen:

1. Öffnen Sie ein Profil und klicken Sie auf &quot;Bearbeiten&quot;.

1. Klicken Sie auf den Tab **Interaktionsbewertungen für E-Mail-Kanal**.

Wenn Sie eine Abfrageaktivität in einem Workflow verwenden, können Sie die Bewertung zur Optimierung Ihrer Zielgruppe nutzen. Beispielsweise mit den Kriterien für den **Bindungsgrad**:

![](assets/do-not-localize/predictive_score_query.png)
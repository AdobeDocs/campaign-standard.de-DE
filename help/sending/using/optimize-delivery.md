---
title: Optimieren des Nachrichtenversands
seo-title: Optimieren des Nachrichtenversands
page-status-flag: never-activated
uuid: a540efc7-105d-4c7f-a2ee-ade4d22b3445
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
discoiquuid: 0cbc4e92-482f-4dac-a1fb-b738e7127938
index: y
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 80%

---


# Versand optimieren {#optimize-delivery}

Bevor Sie mit dem Erstellen von Sendungen beginnen, können Sie mehrere Maßnahmen treffen, um den vorgelagerten Versandprozess zu optimieren.

Im folgenden Abschnitt werden Best Practices und empfohlene Verfahren für die optimale Konfiguration von Adobe Campaign erläutert. Durch die Einhaltung dieser Empfehlungen vermeiden Sie mögliche Probleme später im Prozess.

## Leistung der Plattform

Mehrere Faktoren können die Server-Leistung direkt beeinflussen und die Plattform verlangsamen:

* Anzahl und Art der Personalisierungselemente: Durch Personalisierung in E-Mails werden Daten für jeden Empfänger aus der Datenbank abgerufen. Bei vielen Personalisierungselementen erhöht sich dadurch die Datenmenge, die zur Vorbereitung des Versands benötigt wird.  Learn more about email personalization in [this section](../../designing/using/personalization.md)

* Laden des Servers: Wenn Kampagne mehrere Aufgaben gleichzeitig verarbeitet, kann dies die Leistung verlangsamen. Der Server muss alle eingehenden und ausgehenden Daten für alle Versand koordinieren, um sicherzustellen, dass die Daten korrekt und pünktlich sind.

   **Tipp**: Koordinieren Sie die zeitliche Durchführung von Sendungen mit anderen Team-Mitgliedern, um eine optimale Leistung zu gewährleisten.

* The [workflow execution](../../automating/using/about-workflow-execution.md): monitoring your workflows is essential to avoid platform performance issues. Follow the guidelines listed [in this page](../../automating/using/monitoring-workflow-execution.md). Weitere Informationen finden Sie im Abschnitt Best Practices für den [Workflow](../../automating/using/best-practices-workflows.md) .

* You can leverage [Campaign Contol Panel capabilities](https://docs.adobe.com/content/help/de-DE/control-panel/using/discover-control-panel/key-features.html) to monitor your platform, using [performance monitoring](https://docs.adobe.com/content/help/de-DE/control-panel/using/performance-monitoring/about-performance-monitoring.html) functionalities.

## Prüfen der Netzwerkkonfiguration {#network-config}

Um den Versand großer Mengen von E-Mails zu optimieren und zu verhindern, dass Sie für einen Spammer gehalten werden, achten Sie auf eine ordnungsgemäße Netzwerkkonfiguration, mit der nicht versucht wird, die Identität des Servers zu verbergen.

**Tipp**: Verwenden Sie eine transparente Absenderadresse entsprechend der Website Ihrer Marke. Nehmen wir an, das Unternehmen TravelAgency verwaltet die Hotelkette Valentino. Für seine Website verwendet es die Domain valentino.com. Um das Valentino-Hotel in Paris zu bewerben, verwendet es die Subdomain paris.valentino.com. Eine entsprechende Absenderadresse könnte deshalb hotel@paris.valentino.com lauten.

## Verwaltung der Zustellbarkeit {#deliverability-management}

Sie müssen die Zustellbarkeitsrate Ihrer Nachrichten steigern, damit Ihre Nachrichten in die Empfängerpostfächer zugestellt und nicht als unzustellbar zurückgesendet oder als Spam gekennzeichnet werden.

* Was ist Zustellbarkeit?

   * Sie bezeichnet die Faktoren, die darüber bestimmen, ob eine E-Mail vom Server eines Empfängers akzeptiert wird. ISPs (Internet Service Provider) filtern E-Mails heraus, die sie als Spam erachten, oder verhindern das Herunterladen von Bildern. Wenn sie feststellen, dass von einer Domain zu viele E-Mails gesendet werden, begrenzen sie die Anzahl der von diesem Absender akzeptierten E-Mails.

   * Konzentrieren Sie sich bei der Zustellbarkeit Ihrer E-Mail auf vier Hauptkategorien: Datenqualität, Nachricht und Inhalt, Versandinfrastruktur und Reputation. Detailliertere Informationen zu diesem Thema finden Sie in [diesem Abschnitt](../../sending/using/about-deliverability.md).

* Wenden Sie beim Starten einer neuen Plattform die [auf dieser Seite](../../sending/using/starting-new-platform.md)beschriebenen Empfehlungen an.

* Setzen Sie sich mit Ihrem Adobe-Support-Mitarbeiter in Verbindung, wenn Sie Hilfe benötigen.

## Quarantäneverwaltung {#quarantine-management}

Achten Sie in Ihrem eigenen Interesse auf eine gute Quarantäneverwaltung.

Wenn Sie auf einer neuen Plattform erstmals E-Mails versenden, verwenden Sie möglicherweise eine Liste mit fehlerhaften Adressen. Wenn Sie Nachrichten an ungültige Adressen oder an Honeypot-Adressen (Postfächer, die ausschließlich der Täuschung von Spammern dienen) senden, mindert dies die Reputation Ihrer Plattform. Gute Verwaltungsprozesse für Quarantänen tragen dazu bei, die Adressqualität zu erhalten, Blockierungslisten durch Internetzugangsanbieter zu vermeiden und die Fehlerquote zu reduzieren, wodurch Versand und Durchsatz schneller werden.

**Tipps**

* Empfänger, deren Adressen sich in Quarantäne befinden, werden zum Zeitpunkt der Versandanalyse standardmäßig ausgeschlossen und fließen somit nicht in die Berechnung der Zielgruppe ein. Dies beschleunigt die Zustellung, da sich die Fehlerrate maßgeblich auf die Zustellgeschwindigkeit auswirkt. Eine E-Mail-Adresse kann zum Beispiel unter Quarantäne gestellt werden, weil das Postfach voll ist oder die Adresse nicht existiert. [Mehr dazu](../../sending/using/understanding-quarantine-management.md#identifying-quarantined-addresses)

* Adobe Campaign verwaltet fehlerhafte Adressen je nach zurückgegebenem Fehlertyp. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/understanding-quarantine-management.md).

* Teilweise werden E-Mails von Providern automatisch als Spam eingestuft, wenn die Anzahl ungültiger Adressen zu hoch ist. Durch die Quarantäne können Sie also vermeiden, von diesen Providern auf eine Blockierungsliste gesetzt zu werden.

* Die Quarantäneverwaltung hilft Ihnen auch, die Kosten des SMS-Versands zu senken, indem fehlerhafte Telefonnummern aus dem Versand ausgeschlossen werden.

## Anmeldemöglichkeit mit doppelter Bestätigung (Double opt-in){#double-opt-in}

Um den Nachrichtenversand an ungültige Adressen zu vermeiden, unnütze Kommunikation zu minimieren und die Reputation des Absenders zu schützen, empfiehlt Adobe die doppelte Anmeldung zur Bestätigung eines Abonnements. Damit können Sie sicherstellen, dass sich ein Empfänger absichtlich angemeldet hat.

Einzelheiten zur Implementierung dieses Mechanismus sind in [diesem Abschnitt](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md) beschrieben.

Weitere Informationen finden Sie unter [Erste Schritte mit Profilen und Audiencen](../../audiences/using/get-started-profiles-and-audiences.md).

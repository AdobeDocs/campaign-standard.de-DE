---
solution: Campaign Standard
product: campaign
title: Limits bei der Integration mit Microsoft Dynamics 365
description: Limits bei der Integration von Microsoft Dynamics 365 mit Campaign Standard
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 100%

---


# Limits und Grenzen bei der Integration

## Limits bei der Integration

Die folgenden Limits sollten bei der Verwendung dieser Integration berücksichtigt werden. Wenden Sie sich an Ihren technischen Adobe-Support-Mitarbeiter, wenn Sie glauben, dass Sie diese Limits überschreiten.

* Sie müssen das richtige Campaign-Package lizenzieren, um das durch die Integration generierte Aufrufvolumen der ASC-Engine zu unterstützen. Eine Überschreitung des zulässigen Aufrufvolumens der Engine könnte zu einer Verschlechterung der Leistung von Campaign führen.

   Verwenden Sie Folgendes, um das durch die Integration generierte Engine-Aufrufvolumen abzuschätzen:

   * Einfügungen von Datensätzen (d. h. neuer Datensatz): 1 Engine-Aufruf
   * Löschungen von Datensätzen: 1 Engine-Aufruf
   * Aktualisierungen von Datensätzen: 2 Engine-Aufrufe (nur 1 Aufruf, wenn der Zieldatensatz mit dem Quelldatensatz identisch ist, d. h., wenn keine Änderung am ACS-Datensatz erfolgt)

   Bei der Schätzung des Gesamtaufrufvolumens der ACS-Engine ist es wichtig, andere Quellen für Engine-Aufrufe zu berücksichtigen, einschließlich Landingpages, Web-Anwendungen, JSSP, APIs, Registrierungen von Mobile Apps usw.

   Informationen zum Campaign-Package finden Sie hier: https://helpx.adobe.com/de/legal/product-descriptions/campaign-standard.html

* Die Integration unterstützt maximal 30 Millionen Kontakte.

* Das Standardintegrationsangebot umfasst die Unterstützung für bis zu fünf benutzerdefinierte Entitäten.

* Benutzerdefinierte Entitäten mit mehr als 500.000 Datensätzen erfordern zusätzliche Beratungsstunden, um (pro benutzerdefinierter Entität) einen einmaligen ersten dateibasierten Import über den Campaign-Workflow durchzuführen (was zusätzliche Kosten verursacht).

* Das Standardintegrationsangebot bietet Unterstützung für benutzerdefinierte Entitäten mit einer Größe von bis zu 50 Spalten.

* Sie müssen Ihre benutzerdefinierten Ressourcen erstellen und veröffentlichen, bevor Sie die Integration implementieren.

* Die maximale Tabellentiefe beim Verknüpfen von Tabellen beträgt zwei (d. h. Tabelle1->Tabelle2->Tabelle3).

* Dynamics 365-Datentypen werden nur eingeschränkt unterstützt. Wenn Ihr Datenmodell einen anderen Datentyp als einfache Datentypen enthält (z. B. Zeichenfolgen, Ganzzahlen, Dezimalzahlen usw.), müssen Sie Ihr Datenmodell möglicherweise aktualisieren, bevor Sie die Integration verwenden.

* Die Beibehaltung bestehender Daten in benutzerdefinierten Entitäten in Campaign kann zusätzliche Beratungskosten zur Vorbereitung der Daten auf die Integration verursachen.

* Möglicherweise müssen zwischen Adobe und dem Kunden Wartungsfenster für das Onboarding eingerichtet werden, da die anfängliche Erfassung zu Verlangsamungen bei Campaign führen kann.

* Es wird empfohlen, bekannte Fälle von erheblichen Zunahmen oder &quot;Spitzen&quot; bei der Nutzung der Integration (z. B. starker Anstieg neuer oder aktualisierter Datensätze) mitzuteilen, da diese zu Verlangsamungen bei der Datensynchronisation führen kann.

* Im Rahmen der Integration wird erwartet, dass Sie die Konfigurationsschritte vor der Integration in Microsoft Azure und Dynamics 365 ausführen. Sie Konfigurationsschritte finden Sie [auf dieser Seite](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

* Es wird erwartet, dass Sie Ihre Dynamics 365- und Campaign-Datenmodelle in die Integration einbinden und pflegen.

## Grenzen der Integration

Die Integration wurde entwickelt, um den allgemeinen Anwendungsfall der allgemeinen Datenbewegung zwischen Dynamics 365 und Campaign zu lösen. Es ist jedoch nicht beabsichtigt, jeden kundenspezifischen Anwendungsfall zu behandeln:

* Durch die Integration werden keine datenschutzbezogenen Löschvorgänge (z. B. DSGVO) veranlasst. Die Verantwortung für die Erfüllung von Datenschutzanfragen der Endbenutzer liegt beim Kunden. Solche Anfragen sollten sowohl in Campaign (über den Adobe Experience Platform Privacy Service) als auch in Dynamics 365 unabhängig voneinander gestellt werden. Die Integration kann bei Bedarf reguläre Löschvorgänge auslösen, um die Datensynchronisation zu unterstützen.

* Mit Ausnahme der Opt-out-Informationen (sofern vom Kunden konfiguriert) werden keine Profil- oder benutzerdefinierten Entitätsdaten von Campaign zu Dynamics 365 synchronisiert.

* Die Abonnementverwaltung (d. h. Abonnieren/Abbestellen von Abonnements) in Campaign wird nicht nativ unterstützt.

* Das Erstellen und Auslösen von Campaign-E-Mail-Kampagnen in Dynamics 365 wird nicht unterstützt.

* Die Integration unterstützt keine erneute Modellierung von Daten zwischen den Dynamics 365- und Campaign-Datenmodellen. Es wird erwartet, dass die Integration eine Dynamics 365-Tabelle mit einer Campaign-Tabelle synchronisiert.

* Die aktuelle Version der Integration bietet keine Selfservice-Benutzeroberfläche.

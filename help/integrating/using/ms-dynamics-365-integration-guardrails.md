---
title: Integrationsgarantien für Microsoft Dynamics 365
description: Microsoft Dynamics 365 mit Campaign Standard-Integrationsgarantien
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: e90f878814e65a9a61ee4013d94fd0bf3b1f7875
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---


# Integrationsgarantien und -grenzen

## Integrationsgarantien

Die folgenden Garantien sollten bei der Planung der Verwendung dieser Integration berücksichtigt werden. Wenden Sie sich an Ihren technischen Kundenbetreuer, wenn Sie glauben, dass Sie diese Adobe überschreiten.

* Sie müssen das richtige Kampagne-Paket lizenzieren, um das durch die Integration generierte ACS-Engine-Aufrufvolumen zu unterstützen. Eine Überschreitung des zulässigen Anrufvolumens der Engine könnte zu einer Verschlechterung der Leistung der Kampagne führen.

   Verwenden Sie die folgenden Optionen, um die Anzahl der Motoraufrufe aus der Integration abzuschätzen:

   * Datensatzeinfügungen (d. h. neuer Datensatz): 1 Triebwerksaufruf
   * Löschen von Datensätzen: 1 Triebwerksaufruf
   * Aktualisierungen aufzeichnen: 2 Engine-Aufrufe (nur 1 Aufruf, wenn der Zieldatensatz identisch mit dem Quelldatensatz ist, d. h. wenn keine Änderung am ACS-Datensatz vorgenommen wird))

   Bei der Schätzung des Gesamtaufrufvolumens der ACS-Engine ist es wichtig, andere Quellen für Motorabrufe zu berücksichtigen, einschließlich Landingpages, WebApps, JSSP, APIs, Registrierungen mobiler Apps usw.

   Informationen zum Paket zur Ansicht Kampagne finden Sie hier: https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html

* Die Integration unterstützt maximal 30 Millionen Kontakte.

* Das Standard-Integrationsangebot umfasst Unterstützung für bis zu fünf benutzerdefinierte Entitäten

* Benutzerdefinierte Entitäten mit mehr als 500.000 Datensätzen benötigen zusätzliche Beratungsstunden, um einen einmaligen (pro benutzerdefinierte Entität) initialen dateibasierten Import über den Arbeitsablauf der Kampagne durchzuführen (was zusätzliche Kosten verursacht).

* Die standardmäßige Integration bietet Unterstützung für benutzerdefinierte Entitäten mit einer Größe von bis zu 50 Spalten.

* Sie müssen Ihre benutzerdefinierten Ressourcen erstellen und veröffentlichen, bevor Sie die Integration implementieren.

* Die maximale Tabellentiefe beim Verknüpfen von Tabellen beträgt zwei (d. h. Tabelle1->Tabelle2->Tabelle3)

* Dynamische 365-Datentypen werden nur eingeschränkt unterstützt. Wenn Ihr Datenmodell einen anderen Datentyp als einfache Datentypen enthält (z. B. Zeichenfolgen, Ganzzahlen, Dezimalstellen usw.), müssen Sie Ihr Datenmodell möglicherweise aktualisieren, bevor Sie die Integration verwenden.

* Die Beibehaltung vorhandener Daten in Kampagne von benutzerdefinierten Entitäten kann zusätzliche Beratungskosten zur Vorbereitung der Daten auf die Integration verursachen.

* Das Einbordgehen von Wartungsfenstern muss möglicherweise zwischen der Adobe und dem Kunden erfolgen, da die anfängliche Erfassung zu einer Verlangsamung der Kampagne führen kann.

* Es wird empfohlen, bekannte Fälle von signifikantem Anstieg oder &quot;Spitzen&quot;bei der Nutzung der Integration zu kommunizieren (z. B. starke Zunahme neuer oder aktualisierter Datensätze), da dies zu einer Verlangsamung der Datensynchronisierung führen könnte.

* Als Teil der Integration werden Sie erwartet, die vor der Integration Konfigurationsschritte in Microsoft Azurblase und Dynamics 365. Konfigurationsschritte [auf dieser Seite](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md)

* Es wird erwartet, dass Sie Ihre Dynamics 365- und Kampagne-Datenmodelle in die Integration einbinden und diese beibehalten werden.

## Integrationsgrenzen

Die Integration wurde konzipiert, um den allgemeinen Verwendungsfall der gemeinsamen Datenbewegung zwischen Dynamics 365 und Kampagne zu lösen, ist jedoch nicht dazu gedacht, jeden Anwendungsfall, der für jeden Kunden spezifisch ist, zu behandeln:

* Durch die Integration werden keine Datenschutzerklärungen (z.B. GDPR) gelöscht. Die Verantwortung für die Erfüllung der Datenschutzanforderungen für Endnutzer liegt beim Kunden; Solche Anträge sollten sowohl in Kampagne (über die Adobe Experience Platform Privacy Service) als auch in Dynamics 365 unabhängig gestellt werden. Die Integration kann bei Bedarf regelmäßige Löschvorgänge auslösen, um die Datensynchronisierung zu unterstützen.

* Es werden keine Profil- oder benutzerdefinierten Entitätsdaten von der Kampagne auf Dynamics 365 synchronisiert, mit Ausnahme der Ausschluss-Informationen (sofern vom Kunden konfiguriert).

* Kampagne Abonnement Management (d.h. Abonnements/Abbestellungen) wird nicht nativ unterstützt.

* Das Erstellen und Auslösen von Kampagne-E-Mail-Kampagnen aus Dynamics 365 wird nicht unterstützt.

* Die Integration unterstützt nicht die Umformung von Daten zwischen den Dynamics 365- und Kampagne-Datenmodellen. Es wird erwartet, dass die Integration eine Dynamics 365-Tabelle mit einer Kampagne-Tabelle synchronisiert.

* Mit der aktuellen Version der Integration gibt es keine Selbstbedienungs-Benutzeroberfläche.

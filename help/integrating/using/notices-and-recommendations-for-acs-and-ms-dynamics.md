---
title: Informationen zur Microsoft Dynamics 365-Integration
description: Erfahren Sie mehr über Hinweise und Empfehlungen zum Arbeiten mit Campaign Standard und Microsoft Dynamics 365
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
source-git-commit: 277663c4cf0e810f691eeebfade17bf8dd73698e

---


# Informationen zur Microsoft Dynamics 365-Integration

## Regionalunterstützung

Diese Integration ist in den Regionen Nordamerika, EMEA und APAC verfügbar.

Wenn Sie sich in EMEA- oder APAC-Regionen befinden, werden einige Ihrer Daten im Rahmen dieser Integration in den USA verarbeitet. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../reporting/using/about-dynamic-reports.md#dynamic-reporting-usage-agreement).

## Quelle der Wahrheit für die einseitige Kontaktsynchronisierung

Für die Synchronisierung von Kontakten und benutzerdefinierten Entitäten behandelt diese Integration Dynamics 365 als Quelle der Wahrheit. Änderungen an synchronisierten Attributen sollten in Microsoft Dynamics 365, nicht in Adobe Campaign Standard vorgenommen werden. Wenn Änderungen in der Kampagne vorgenommen werden, können sie während der Synchronisierung in einer Kampagne überschrieben werden, da die Synchronisierung in eine Richtung verläuft.  Darüber hinaus ist die Kontaktsynchronisierung so konzipiert, dass alle Kontaktdatensätze abgerufen werden, unabhängig davon, ob sie in Microsoft Dynamics 365 als aktiv oder inaktiv markiert sind.

## Datenschutzanforderungen verwalten

Diese Integration wurde entwickelt, um Endbenutzerdaten (einschließlich, aber nicht beschränkt auf personenbezogene Daten, sofern diese in Ihren Endbenutzerdaten enthalten sind) zwischen Microsoft Dynamics 365 und Adobe Campaign Standard zu übertragen.  Als für die Verarbeitung der Daten verantwortliche Person ist Ihre Firma für die Einhaltung der für die Erhebung und Nutzung personenbezogener Daten geltenden Datenschutzgesetze und -vorschriften verantwortlich.

Für diese Integration müssen Sie jede Anforderung der betroffenen Person in jedem System unabhängig bearbeiten, damit die Änderung in beiden Datenbanken angezeigt wird. Die Änderung sollte zunächst in Microsoft Dynamics 365 und dann in Adobe Campaign Standard ausgeführt werden. Die einzige Ausnahme ist, dass eine datenschutzbezogene Löschanforderung in Campaign Standard, wenn ein Kontakt in Dynamics 365 gelöscht wird, der Datenschutzwarteschlange hinzugefügt wird.

Nachstehend finden Sie Links, die Sie bei der Implementierung von Zugriffsrechten und/oder beim Löschen datenschutzbezogener Anforderungen in jedem System unterstützen:

* [Microsoft Dynamics 365](https://docs.microsoft.com/en-us/microsoft-365/compliance/gdpr-dsr-dynamics365?toc=/microsoft-365/enterprise/toc.json)

* [Adobe Campaign Standard](https://www.adobe.io/apis/experiencecloud/gdpr/docs.html)

## Kontaktlöschung

Da Dynamics 365 die Quelle der Wahrheit ist, werden sich die Kontaktlöschungen in Dynamics 365 in der Kampagne widerspiegeln.

Wenn ein Kontakt in Dynamics 365 gelöscht wird, stellt die Integration eine datenschutzbezogene Löschanforderung im Bildschirm &quot;Kampagne Privacy request/tools&quot;in die Warteschlange.  Wenn Sie den zweistufigen Vorgang für datenschutzbezogene Löschanforderungen deaktiviert haben, übernimmt die Kampagne den Löschvorgang für Sie.

Wenn der zweistufige Vorgang jedoch aktiviert ist, müssen Sie nach Ausführung der Technischen Workflows zum Datenschutz in den Bildschirm &quot;Datenschutzanfragen/Tools&quot;wechseln und bestätigen, dass die Datensätze gelöscht werden sollen.  Erst dann übernimmt die Kampagne die Löschung.

Weitere Informationen finden Sie unter [Ausführung datenschutzbezogener Löschanforderungen in Adobe Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/privacy/execute-privacy-requests.html)

>[!CAUTION]
>
>Wenn Sie den zweistufigen Vorgang für Datenschutzanforderungen in der Kampagne aktiviert haben, werden Ihre Löschvorgänge in Dynamics 365 nicht automatisch in der Kampagne angezeigt.  Sie müssen den Bildschirm &quot;Kampagne Privacy Request&quot;aufrufen, um die Löschungen zu bestätigen.

>[!NOTE]
>
>Diese Integration erstellt eine Anforderung mit der externen ID (d. h. der Dynamics 365-Kontakt-ID) als Profil-/Datensatzkennung.

## Ausschluss

Aufgrund der unterschiedlichen Ausschlussattribute von Dynamics 365 und der Kampagne und der unterschiedlichen Geschäftsanforderungen der einzelnen Kunden wurde die Abmeldezuordnung für den Kunden als Abschließen beibehalten. Es ist wichtig, sicherzustellen, dass die Ausschlussoption ordnungsgemäß zwischen den Systemen zugeordnet wird, damit die Voreinstellungen für die Ausschlussoption für Endbenutzer beibehalten werden und sie keine Kommunikation über einen Kanal erhalten, für den sie sich entschieden haben.

Beachten Sie, dass bei Abmeldezuordnungen nur Kampagnen mit dem Präfix &quot;blackList&quot;(z. B. blackListEmail) oder dem spezifischen Attribut für CCPA-Abmeldeoption verwendet werden können.  In Dynamics 365 haben die meisten Ausschluss-Felder das Präfix &quot;doNot&quot;. Sie können jedoch auch benutzerdefinierte Attribute verwenden, die Sie zu Ausschluss-Zwecken erstellt haben, wenn die Datentypen kompatibel sind.

Bei der Bereitstellung der Integration können Sie angeben, welche Ausschluss-Konfiguration Sie für Ihr Unternehmen benötigen:

* Dynamics 365 ist eine Quelle der Wahrheit für Opt-outs: Die Attribute für das Ausschluss werden in eine Richtung von Dynamics 365 auf den Campaign Standard synchronisiert.
* Campaign Standard ist die Quelle der Wahrheit für Opt-out-Möglichkeiten: Ausschlussattribute werden in einer Richtung von Campaign Standard zu Dynamics 365 synchronisiert.
* Dynamik 365 UND Campaign Standard sind beide Wahrheitsquellen: Ausschluss-Attribute werden bidirektional zwischen Campaign Standard und Dynamics 365 synchronisiert

Folgen Sie den Anweisungen nach der Bereitstellung im [Unifi-Benutzerhandbuch](https://drive.google.com/drive/folders/16seHF45e6bFxHX15zWLqFLEXymCuA_wn) , um diese Werte korrekt zuzuordnen.

Die bidirektionale Opt-out-Konfiguration verwendet Logik, um zu bestimmen, welcher Wert auf beiden Systemen geschrieben werden soll.  Die Logik vergleicht Zeitstempel zwischen den beiden Systemen (Änderung auf Rekordebene in Dynamics 365, Änderung der Kampagne auf Attributebene), um festzustellen, welches System vorherrscht.  Wenn die Kampagne den aktuelleren Zeitstempel enthält, hat der Wert &quot;Kampagne&quot;Vorrang.  Wenn Dynamics 365 den aktuelleren Zeitstempel enthält oder wenn sie gleich sind, gewinnt opt-out=TRUE (vorausgesetzt, einer der Werte ist TRUE).

**Ausschlussmöglichkeiten nach dem kalifornischen Verbraucherschutzgesetz (CCPA) und ähnlichen Rechtsvorschriften.**

Die bidirektionale Opt-out-Konfigurationsfunktion ist derzeit nicht in der Lage, die Einhaltung bestimmter gesetzlicher Vorschriften des CCPA und/oder anderer Datenschutzgesetze standardmäßig zu unterstützen. Kunden, die die CCPA oder ähnliche gesetzliche Anforderungen in Bezug auf Opt-outs erfüllen müssen, sind für die Implementierung ihrer eigenen Lösung für bidirektionale Synchronisierungen verantwortlich.

>[!NOTE]
>
>Es wird empfohlen, dass Sie eine Option für eine einmalige Abmeldung auswählen, wenn Ihre Firma keine bidirektionale Abmeldeunterstützung benötigt.

>[!NOTE]
>
>Bitte überprüfen Sie die standardmäßigen und spezifischen Typologieregeln in Adobe Campaign und aktualisieren Sie diese gegebenenfalls, bevor Sie hier Änderungen vornehmen, um sicherzustellen, dass diese korrekt auf alle ausgehenden Mitteilungen angewendet werden. Achten Sie beispielsweise darauf, dass alle Zuordnungen zu den Ausschluss-Voreinstellungen die Absichten-/Kommunikationsoptionen des Empfängers exakt widerspiegeln und den Versand von Beziehungen oder Transaktionsnachrichten wie z. B. die Auftragsbestätigungen des Kunden nicht versehentlich beenden.

## Bestehende Daten zur Kampagne

Durch diese Integration werden Kontakte und benutzerdefinierte Entitäten von Dynamics 365 zur Kampagne synchronisiert. Kampagnen, die außerhalb der Integration erstellt wurden (d. h. nicht vom Synchronisierungsauftrag erstellt wurden), werden von der Integration nicht berührt, einschließlich der zum Zeitpunkt der Integrationskonfiguration vorhandenen Kampagnen.

Da diese Integration das **[!UICONTROL externalId]** Feld in Campaign Standard nutzt, um Kampagne-Profil-Datensätze mit Dynamics 365 Kontaktdatensätzen zu synchronisieren, muss dieses Feld der Kampagne (**[!UICONTROL externalId]** ) mit dem Dynamics 365 ausgefüllt werden, **[!UICONTROL contactId]** damit die von Dynamics 365 synchronisierten Datensätze synchronisiert werden können.  Bei benutzerdefinierten Entitäten muss dieses Feld ebenfalls korrekt vorhanden und ausgefüllt sein, damit die Synchronisierung fortgesetzt werden kann.  Denken Sie jedoch daran, dass Dynamics 365 immer noch die Wahrheitsquelle sein wird und dass die Kampagne Profil-Daten überschrieben werden können, wenn die Integration Updates auf der Dynamics 365-Seite erkennt.  Abhängig von Ihrer vorhandenen Bereitstellung können auch andere Schritte erforderlich sein, um die Integration zu aktivieren. Daher wird empfohlen, eng mit Ihrem technischen Kontakt zu Adobe zusammenzuarbeiten.

>[!NOTE]
>
>Aufgrund der Komplexität der vorhandenen Kundenbereitstellungen sollten Sie bei der Planung und Einrichtung der Integration mit Ihrem technischen Kontakt von Adobe zusammenarbeiten.

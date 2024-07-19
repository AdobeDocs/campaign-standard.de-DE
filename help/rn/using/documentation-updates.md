---
title: Aktualisierungen der Dokumentation
description: Hier erhalten Sie Informationen über die letzten Dokumentationsaktualisierungen für Adobe Campaign Standard
feature: Overview
role: User
level: Beginner
exl-id: 3f77825e-cb98-4cb1-9775-a8b6995e9da1
source-git-commit: dcfd4e2610cbf9d250359cab6ed43e8c97dd4536
workflow-type: tm+mt
source-wordcount: '7297'
ht-degree: 100%

---

# Aktualisierungen der Dokumentation{#documentation-updates}

Zusätzlich zu den [Versionshinweisen](../../rn/using/release-notes.md) von Adobe Campaign werden auf dieser Seite alle neuen Aktualisierungen in der Adobe Campaign Standard-Dokumentation aufgeführt.

## Version 24.1 – Winter 2024 {#release-24-1}

Die Versionshinweise für die Version Winter 2024 von Campaign Standard 24.1 wurden veröffentlicht. [Weitere Informationen](release-notes.md)

## Dezember 2023 {#doc-updates-dec-2023}

Einige wichtige Änderungen am FCM-Dienst (Android Firebase Cloud Messaging) werden 2024 veröffentlicht und wirken sich auf Ihre Implementierung von Adobe Campaign aus. Weitere Informationen finden Sie in [dieser Technote](../../administration/using/push-technote.md).

## Version 23.2 – Herbst 2023 {#release-23-2}

* Die Versionshinweise für die Version Herbst/Winter von Campaign Standard 23.2 wurden veröffentlicht. [Weitere Informationen](release-notes.md)

* JWT (JSON Web Tokens) wird gerade eingestellt und durch OAuth ersetzt. Die Umstellung erfolgt schrittweise innerhalb der kommenden Campaign-Versionen. Die Dokumentation wird entsprechend diesen Aktualisierungen ebenfalls aktualisiert.

## Oktober 2023 {#doc-updates-oct-2023}

* Die neue Benutzeroberfläche für Experience Cloud Triggers ist jetzt verfügbar. Sie bietet ein intuitives Erlebnis, um das Verhalten von Verbraucherinnen und Verbrauchern zu verwalten und Benutzererlebnisse zu personalisieren. [Weitere Informationen](https://experienceleague.adobe.com/docs/experience-cloud/triggers/overview.html?lang=de){target="_blank"}.

* Es wurde ein Hinweis zur Verwendung von Fallen-Testprofilen in Kombination mit Filter- oder Ermüdungsregeln hinzugefügt. [Weitere Informationen](../../sending/using/using-traps.md)

## Version 23.1 – Frühjahr/Sommer 2023 {#release-23-1}

Die Versionshinweise für die Version Frühjahr/Sommer von Campaign Standard 23.1 wurden veröffentlicht. [Weitere Informationen](release-notes.md)

## November 2022 {#doc-updates-november-2022}

Es wurde ein Hinweis hinzugefügt, in dem empfohlen wird, Leerzeichen im ID-Feld von Sendungen zu vermeiden. [Weitere Informationen](../../channels/using/creating-an-email.md)

Auf der Seite der Workflow-Aktivität **[!UICONTROL Datei extrahieren]** wurden Informationen zum Extrahieren von Daten in eine CSV-Datei mit einer bestimmten Codierung hinzugefügt. [Weitere Informationen](../../automating/using/extract-file.md)

## Version 22.3 – Herbst/Winter 2022 {#release-22-3}

Die Versionshinweise für die Version Herbst/Winter von Campaign Standard 22.3 wurden veröffentlicht. [Weitere Informationen](release-notes.md)

<!--Data retention periods have been updated to reflect changes coming with 22.3 release. [Read more](../../administration/using/data-retention.md)-->


## Version 22.2 – Juni 2022 {#release-22-2}

**In der Version enthaltene Verbesserung**

**Adobe Notification Service** - Campaign wird mit dem Adobe Notification Service geliefert, der es Experience Cloud-Lösungen ermöglicht, Nutzer in Experience Cloud über Aktivitäten zu informieren, die für sie wichtig sind. [Weitere Informationen](../../administration/using/sending-internal-notifications.md)

**Sonstige Änderungen**

Die Integrationen mit Adobe Experience Platform Data Connector und dem Service Audience Destinations werden nun nicht mehr unterstützt. [Weitere Informationen](deprecated-features.md)

Die Verwendung des SMTP-Testmodus wurde detailliert beschrieben. [Weitere Informationen](../../administration/using/configuring-email-channel.md#smtp-test-mode)

## März 2022 {#doc-updates-march-2022}

Es wurde ein Hinweis eingefügt, wonach das Versenden von Nachweisen mit Profilersatz den Protokollen der ausgewählten Profile Einträge hinzufügt. [Weitere Informationen](../../sending/using/testing-messages-using-target.md)

## Version 22.1 – Februar 2022 {#release-22-1}

**In der Version enthaltene Verbesserungen**

Verbesserter Mechanismus zur Wiederholung von Sendungen mit Inhalten, die von einer URL importiert wurden. [Weitere Informationen](../../designing/using/using-existing-content.md#retrieving-content-from-a-url-automatically-at-preparation-time)

Die Zugriffsebene der Optionen, die den Audit steuern, wurde aktualisiert: frühere Optionen zum Aktivieren/Deaktivieren des [Audit-Protokolls](../../administration/using/audit.md) waren für [funktionale Administratoren](../../administration/using/users-management.md#functional-administrators) nicht zugänglich. Jetzt wurde die Zugriffsebene der Audits geändert, um funktionalen Administratoren die Kontrolle zu ermöglichen. [Weitere Informationen](../../administration/using/audit.md#enable-disable-audit)

Das neue Dropdown-Menü **Vorgangsverlauf** wurde zum Nachrichten-Dashboard hinzugefügt. [Weitere Informationen](../../sending/using/monitoring-a-delivery.md)

**Sonstige Änderungen**

Es wurde ein Warnhinweis zu Schlüsselwörtern hinzugefügt, die automatische SMS-Antworten auslösen: Sie dürfen nur alphanumerische Zeichen enthalten. [Weitere Informationen](../../channels/using/managing-incoming-sms.md)

Es wurde ein Hinweis zum Abschnitt über A/B-Test-E-Mails hinzugefügt: Wenn die Gesamtpopulation weniger als 50.000 umfasst, muss jede Variante mindestens 10 % der Gesamtpopulation ausmachen. Andernfalls wird in den Protokollen eine Warnung angezeigt. [Weitere Informationen](../../channels/using/designing-an-a-b-test-email.md)

Die Beschreibung der Option **[!UICONTROL Quelldateien nach der Übertragung löschen]** in der Aktivität **Dateiübertragung** wurde aktualisiert, einschließlich einer Erinnerung daran, die Größe des archivierten Inhalts im SFTP-Verzeichnis manuell zu überwachen, falls die Option nicht ausgewählt ist. [Weitere Informationen](../../automating/using/transfer-file.md)

Alle veralteten Links in den Abschnitten zum **Datenschutz** wurden aktualisiert. [Weitere Informationen](../../start/using/privacy.md)

Im Inhaltsverzeichnis der Campaign Standard-Dokumentation wurde ein direkter Link zur Control Panel-Dokumentation von Campaign hinzugefügt.

## Version 21.3 – September 2021 {#release-21-3---september-2021}

**Neue Funktionen in dieser Version**

Verbesserte einheitliche Experience Cloud-Benutzeroberfläche – [mehr dazu](../../start/using/interface-description.md#top-bar)

Neue Funktion &quot;Audit-Protokoll&quot; – [mehr dazu](../../administration/using/audit.md)

Workflow-Diagnosemodus – [mehr dazu](../../automating/using/managing-execution-options.md)

**Weitere Dokumentationsaktualisierungen zu dieser Version**

Es wurde ein neuer Abschnitt hinzugefügt, in dem beschrieben wird, wie eine Adresse aus der Quarantäneliste entfernt werden kann. [Weitere Informationen](../../sending/using/understanding-quarantine-management.md#removing-a-quarantined-address)

Der Abschnitt **Quarantäne vs. Blockierungsliste** wurde klarer formuliert. [Weitere Informationen](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist)

## Juli 2021 {#doc-updates-july-2021}

Es wurde ein neuer Abschnitt hinzugefügt, in dem beschrieben wird, wie Benutzern das Anmelden oder Abmelden bei mehreren Diensten von einer Landingpage aus ermöglicht werden kann. [Weitere Informationen](../../channels/using/managing-landing-page-form-data.md#multiple-subscriptions)

Der Abschnitt **Verwalten von Landingpage-Formulardaten** wurde aktualisiert und präzisiert. [Weitere Informationen](../../channels/using/managing-landing-page-form-data.md)

## Version 21.2 – Juni 2021 {#release-21-2---june-2021}

**Neue Funktionen in dieser Version**

Validierung von Landingpages – Sie können Ihren Landingpages jetzt eine Option für eine obligatorische Vereinbarung hinzufügen. [Weitere Informationen](../../channels/using/managing-landing-page-form-data.md#agreement-checkbox)

Der Abschnitt **E-Mail-Größe** wurde mit Informationen zur maximalen Größe einer E-Mail aktualisiert, die jetzt standardmäßig mit 100 MB festgelegt ist. [Weitere Informationen](../../sending/using/design-and-personalize.md#email-size)

**Weitere Dokumentationsaktualisierungen zu dieser Version**

Es wurden Informationen zum Ändern des Zielgruppen-Mappings in einer Transaktions-Push-Benachrichtigung hinzugefügt. [Weitere Informationen](../../channels/using/transactional-push-notifications.md#change-target-mapping)

## Mai 2021 {#doc-updates-may-2021}

Der Berichtabschnitt **Aktive Profile** wurde aktualisiert. [Weitere Informationen](../../audiences/using/active-profiles.md)

Die Seite **Versionsplanung** wurde mit neuen Daten aktualisiert. [Weitere Informationen](../../rn/using/release-planning.md)


## April 2021 {#doc-updates-april-2021}

Ein neuer Abschnitt beschreibt die Verwendung von Adobe Experience Platform-Quellen und -Zielen, um Daten zwischen Campaign Standard und der Adobe Echtzeit-Kundendatenplattform (RTCDP) auszutauschen. [Weitere Informationen](../../integrating/using/get-started-sources-destinations.md)

## März 2021 {#doc-updates-march-2021}

Neue Seite mit **Hilfe und Support-Optionen**. [Weitere Informationen](../../support.md)

Der Abschnitt, in dem die wichtigsten Schritte zum Senden einer Nachricht aufgeführt sind, wurde um weitere Informationen und Verweise erweitert. [Weitere Informationen](../../channels/using/key-steps-to-send-a-message.md)

Es wurden Informationen hinzugefügt, die präzisieren, dass bei der Auswahl einer Audience in einer Abfrage deren Definition kopiert und nicht referenziert wird. [Weitere Informationen](../../audiences/using/selecting-an-audience-in-a-message.md)

Informationen zu Audience Destinations Service und Adobe Experience Platform Data Connector wurden in einem neuen Abschnitt zusammengefasst.

Eine **Declared ID**-Datenquelle kann jetzt auch mit der People Core Service-Integration verwendet werden. In der Dokumentation zur Integration von Campaign mit Audience Manager oder People Core Service wurden Informationen hinzugefügt. [Weitere Informationen](../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md)

Es wurden Informationen zur Implementierung des lokalen Trackings für Mobile Apps hinzugefügt. [Weitere Informationen](../../administration/using/local-tracking.md)

Der Abschnitt [Zustellbarkeit](../../sending/using/about-deliverability.md) wurde aktualisiert und enthält nun Links zum neuen [Adobe-Handbuch mit Best Practices zur Zustellbarkeit](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/introduction.html?lang=de). Alle allgemeinen Informationen zur Zustellbarkeit, die für verschiedene Adobe-Lösungen gelten können, wurden in den [Anhang des Handbuchs mit Best Practices](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/general-resources.html?lang=de#additional-resources) verschoben.

## Version 21.1 – Februar 2021 {#release-21-1---february-2021}

**Neue Funktionen in dieser Version**

E-Mail-Feedback-Service – [mehr dazu](../../sending/using/confirming-the-send.md#message-indicators)

Verbesserungen bei der Adobe Experience Manager-Integration – [mehr dazu](../../integrating/using/creating-multilingual-email-aem.md)

Einheitliche Experience Cloud-Benutzeroberfläche – [mehr dazu](../../start/using/interface-description.md#top-bar)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Es wurden Informationen hinzugefügt, die beschreiben, wie anhand der E-Mail, des Vornamens, des Nachnamens oder eines beliebigen benutzerdefinierten Felds nach einem Profil gesucht werden kann. [Weitere Informationen](../../audiences/using/integrated-customer-profile.md)

Es wurden Informationen über die neue Funktion GetOption hinzugefügt, mit der Sie den Wert einer bestimmten Funktion zurückgeben können, wenn Sie einen Workflow mit externen Parametern aufrufen. [Weitere Informationen](../../automating/using/customizing-workflow-external-parameters.md#using-events-variables)

Es wurden Informationen über die neue Ausgabevariable **[!UICONTROL filesCount]** hinzugefügt, die nach Verwendung der Aktivität **[!UICONTROL Dateiübertragung]** verfügbar ist. [Weitere Informationen](../../automating/using/transfer-file.md#output-variables)

Der Abschnitt **E-Mail-Kanal konfigurieren** wurde um Erläuterungen zu den aktuellen E-Mail-Einstellungen ergänzt. Einige Parameter früherer Versionen, die noch für bestimmte Kunden verwendet werden, sind unten auf der Seite aufgelistet. [Weitere Informationen](../../administration/using/configuring-email-channel.md)

Es wurden Informationen hinzugefügt, wie sichergestellt werden kann, dass ein geplanter Workflow nicht neu geplant wird, solange eine oder mehrere Aufgaben aus einer früheren Ausführung noch ausstehen. [Weitere Informationen](../../automating/using/scheduled-workflows-execution.md)

## Dezember 2020 {#doc-updates-december-2020}

Die Funktion **Prädiktive Betreffzeile** wurde eingestellt. [Weitere Informationen](../../rn/using/deprecated-features.md)

Der Abschnitt **Erste Schritte mit Transaktionsnachrichten** enthält jetzt [erweiterte Schemata](../../channels/using/getting-started-with-transactional-msg.md#transactional-messaging-operating-principle) für ein besseres Verständnis des Vorgangs.

Es steht nun ein durchgängiger Anwendungsfall zur Veranschaulichung des Implementierungsprozesses für Transaktionsnachrichten zur Verfügung. [Weitere Informationen](../../channels/using/transactional-messaging-use-case.md)

Der Abschnitt **Datenschutz** wurde [hierher](../../start/using/privacy.md) verschoben.

Eine neue **Barrierefreiheit**-Seite ist verfügbar: Sie enthält Informationen zur Unterstützung der Barrierefreiheit im Adobe Campaign Standard-Arbeitsbereich. [Weitere Informationen](../../start/using/accessibility.md)

Es wurde ein Warnhinweis hinzugefügt, wonach die Anzahl der veröffentlichten Transaktionsnachrichten für eine optimale Performance unter 100 bleiben sollte. [Weitere Informationen](../../channels/using/transactional-messaging-limitations.md#transactional-message-number)

Die Seite für das Protokoll und die Einstellungen des SMS-Connectors wurde [hierher](../../administration/using/sms-protocol.md) verschoben.

Der Abschnitt über das **Verwenden von Produktlisten in einer Transaktionsnachricht** wurde [hierher](../../designing/using/using-product-listings.md) verschoben.

## November 2020 {#doc-updates-november-2020}

Im Abschnitt zu **persönlichen Daten und Personas** wurde ein Anwendungsszenario ergänzt, das veranschaulicht, wie die verschiedenen Personas in Bezug auf Datenschutz interagieren – [Weitere Informationen](../../start/using/privacy.md#use-case-scenario)

Ein neuer Abschnitt mit häufig gestellten Fragen zum Datenschutz wurde hinzugefügt – [Weitere Informationen](../../start/using/privacy-faq.md)

Der Abschnitt zum **Datenschutz** wurde um zwei neue Seiten erweitert: [Datenschutzverwaltung](../../start/using/privacy-management.md) und [Verwaltung von Datenschutzanfragen](../../start/using/privacy-requests.md).

Der Abschnitt **Transaktionsnachrichten** wurde neu organisiert und zur besseren Navigation an einer Stelle zusammengefasst. [Weitere Informationen](../../channels/using/getting-started-with-transactional-msg.md)

Im Abschnitt „Adobe Experience Platform Data Connector“ wurden Informationen zum Validierungsfehler bei der Datenzuordnung im Zusammenhang mit der Datenschutzverwaltung und zu dessen Behebung hinzugefügt –

## Version 20.4 – Oktober 2020 {#release-20-4---october-2020}

**Neue Funktionen in der Version**

Kontrollgruppen – [mehr dazu](../../sending/using/control-group.md)

Externe API (OAuth-Unterstützung) – [mehr dazu](../../automating/using/external-api.md)

Integration von Journey-KI – [mehr dazu](../../sending/using/predictive.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Der Abschnitt zum Aufrufen eines Workflows mit externen Parametern wurde um neue Funktionen erweitert, die im Ausdruckseditor zur Verfügung stehen – [Weitere Informationen](../../automating/using/customizing-workflow-external-parameters.md)

Den Best Practices bei Workflows wurde eine Empfehlung zur Anzahl der pro Workflow zu verwendenden Aktivitäten hinzugefügt – [Weitere Informationen](../../automating/using/best-practices-workflows.md#number-activities)

Es wurde ein neuer Abschnitt zu Best Practices beim Versand hinzugefügt – [Weitere Informationen](../../sending/using/delivery-best-practices.md)

Es wurde ein Abschnitt hinzugefügt, in dem die neuen Filter beschrieben werden, mit denen die Ereigniskonfigurationen nach ihrem Status und dem letzten Eingang eines Ereignisses durchsucht werden können – [Weitere Informationen](../../channels/using/configuring-transactional-event.md#searching-transactional-events)

## September 2020 {#doc-updates-september-2020}

Der Abschnitt **Ereignis-Transaktionsnachrichten** wurde neu strukturiert und inhaltlich klarer erläutert – [Weitere Informationen](../../channels/using/editing-transactional-message.md)

Es wurde ein Warnhinweis hinzugefügt, der Benutzer über Einschränkungen bei Berechtigungen im Zusammenhang mit dem Protokollzugriff warnt – [Weitere Informationen](../../administration/using/users-management.md)

Es wurde ein neuer Abschnitt hinzugefügt, in dem der Prozess zum Erstellen einer neuen Marke detailliert beschrieben wird – [Weitere Informationen](../../administration/using/branding.md#creating-a-brand)

Die neue Integration von Campaign Standard mit Microsoft Dynamics 365 ist jetzt verfügbar – [Weitere Informationen](../../integrating/using/d365-acs-get-started.md)

Im Bericht zu den aktiven Profilen wurden Informationen zu anonymen Quellen hinzugefügt – [Weitere Informationen](../../audiences/using/active-profiles.md)

## August 2020 {#doc-updates-august-2020}

Ein neuer aktualisierter Abschnitt über die ersten Schritte mit Transaktionsnachrichten ist verfügbar. [Weitere Informationen](../../channels/using/getting-started-with-transactional-msg.md)

Der Abschnitt **Einschränkungen bei Transaktionsnachrichten** wurde [hierher](../../channels/using/transactional-messaging-limitations.md) verschoben.

Der Abschnitt **Versandvorbereitung** wurde [hierher](../../sending/using/preparing-the-send.md) verschoben.

## Juli 2020 {#doc-updates-july-2020}

Es wurde ein neuer Abschnitt mit Richtlinien für die Überwachung in Campaign Standard hinzugefügt – [Weitere Informationen](../../administration/using/monitoring-guidelines.md)

Der Abschnitt zu den Schutzmechanismen und Begrenzungen für externe APIs wurde aktualisiert – [Weitere Informationen](../../automating/using/external-api.md#guardrails)

Die Seite mit der Übersicht über die Datenschutzverwaltung wurde aktualisiert und enthält nun Informationen zum thailändischen Datenschutzgesetz (PDPA) und zum brasilianischen Datenschutzgesetz (Lei Geral de Proteção de Dados, LGPD). [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/campaign-privacy-overview.html#whatisgdpr)

Das Handbuch zu mobilen Kanälen wurde überarbeitet und verbessert. Eine neue Anleitung zum Konfigurieren von mobilen Kanälen mit technischer Dokumentation zur Mobilkonfiguration wurde hinzugefügt – [Weitere Informationen](../../administration/using/push-tracking.md)

Die Seite zur Datenschutzverwaltung in Campaign Standard wurde aktualisiert und enthält eine Klarstellung, wie Datenschutzanfragen über die Privacy Core Service-Integration verwaltet werden – [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/acs-privacy.html#ManagingPrivacyRequests)

Neue KI-gestützte E-Mail-Funktionen: Sendezeitoptimierung und Profilbewertung – [Weitere Informationen](../../sending/using/predictive.md)

## Juni 2020 {#doc-updates-june-2020}

Anwendungsbeispiele für Workflows wurden aktualisiert und in thematische Bereiche neu angeordnet – [Weitere Informationen](../../automating/using/about-workflow-use-cases.md)

Es wurden Anwendungsfälle zum [Verschlüsseln](../../automating/using/managing-encrypted-data.md#use-case-gpg-encrypt) und [Entschlüsseln](../../automating/using/managing-encrypted-data.md#use-case-gpg-decrypt) von Daten mit dem Control Panel und mit Campaign-Workflows hinzugefügt.

Verweise auf die alte Support-Website wurden durch die neue URL ersetzt – [mehr dazu](../../support.md)

Die benutzerdefinierte Konfiguration des Litmus-Kontos wurde aus der Rendering-Funktion des Posteingangs entfernt – [Weitere Informationen](../../sending/using/email-rendering.md)

Die Integration von Campaign Standard mit Microsoft Dynamics 365 ist derzeit nicht verfügbar. Ein neuer Connector wird derzeit entwickelt und wird in Zukunft verfügbar sein. Die entsprechenden Hilfeseiten wurden entfernt – [Weitere Informationen](../../integrating/using/d365-acs-get-started.md)

## Mai 2020 {#doc-updates-may-2020}

Die Übersichtsseite zu Campaign Standard wurde erweitert und in thematische Themen unterteilt – [Weitere Informationen](../../start/using/about-campaign-standard.md)

Der Abschnitt zu den E-Mail-Kanal-Parametern wurde näher erläutert und enthält jetzt weitere Informationen zu den Feldern für zulässige Masken und zur Kennung für die Versandberichte – [Weitere Informationen](../../administration/using/configuring-email-channel.md)

Der Abschnitt zur Konfiguration einer Mobile App mit Adobe Experience Platform SDKs ist jetzt in der Hauptdokumentation verfügbar und enthält weitere Informationen zum technischen Workflow „Mobile App AEPSDK von Launch synchronisieren“. [Weitere Informationen](../../administration/using/configuring-a-mobile-application.md)

## Version 20.3 – Mai 2020 {#release-20-3---may-2020}

**Neue Funktionen in der Version**

Thailändisches Datenschutzgesetz (PDPA) – [mehr dazu](https://helpx.adobe.com/content/help/de/campaign/kb/acs-privacy.html)

Externe API-Aktivität (GA) – [mehr dazu](../../automating/using/external-api.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

In den Workflow-Eigenschaften wurden Informationen zum **[!UICONTROL Verlauf in Tagen]** hinzugefügt. Darin sind jetzt Dateien enthalten, die von der Aktivität **[!UICONTROL Dateiübertragung]** heruntergeladen wurden – [Weitere Informationen](../../automating/using/managing-execution-options.md)

Im Abschnitt zur Profilersetzung wurden Informationen zum Limit von 500 Zeichen beim Betreffpräfix hinzugefügt – [Weitere Informationen](../../sending/using/testing-messages-using-target.md)

Ein neuer Abschnitt zum Thema Datenschutz und Einverständnis wurde der Hauptdokumentation hinzugefügt – [Weitere Informationen](../../start/using/privacy.md)

Es wurde ein Anwendungsfall hinzugefügt, mit dem Sie E-Mails des alten Editors in den E-Mail-Designer konvertieren können – [Weitere Informationen](../../designing/using/converting-emails-from-legacy-editor.md)

Es wurde ein Abschnitt mit häufig gestellten Fragen zum E-Mail-Designer hinzugefügt – [Weitere Informationen](../../designing/using/faq-email-designer.md)

## April 2020 {#doc-updates-april-2020}

Die Dokumentation zur Integration von Microsoft Dynamics 365 mit Adobe Campaign Standard ist jetzt in der Hauptdokumentation verfügbar – [Weitere Informationen](../../integrating/using/d365-acs-get-started.md)

Zusätzliche Ressourcen wurden zur Startseite der Dokumentation hinzugefügt – [Weitere Informationen](../../campaign-standard-home.md)

Informationen zum Experience Cloud ID-Dienst (ECID) wurden der Dokumentation zu Adobe Experience Platform Data Connector hinzugefügt –

Der Abschnitt zu den Transaktionsnachrichten wurde um Informationen zum Zugriff auf die neuesten Transaktionsereignisse und aktualisierte Screenshots erweitert. [Weitere Informationen](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event)

Die Dokumentation zu Typologien und Typologieregeln wurde verbessert und mit zusätzlichen Informationen zu integrierten Typologieregeln aktualisiert – [Weitere Informationen](../../sending/using/about-typology-rules.md)

Bei der Aktivität **[!UICONTROL Dateiübertragung]** wurden der Aktion **[!UICONTROL Dateiauflistung]** Informationen hinzugefügt – [Weitere Informationen](../../automating/using/transfer-file.md)

Die Dokumentation zu weiteren Zustellversuchen nach einem temporären Versandfehler wurde aktualisiert und enthält nun weitere Details dazu, wie zusätzliche Zustellversuche nach der Aktualisierung auf den erweiterten MTA verwaltet werden – [Weitere Informationen](../../sending/using/understanding-delivery-failures.md#retries-after-a-delivery-temporary-failure)

Der Abschnitt &quot;Transaktionsnachricht löschen&quot; wurde verbessert und deutlicher erklärt – [Weitere Informationen](../../channels/using/publishing-transactional-message.md#deleting-a-transactional-message)

Der Abschnitt **Vorschau von Sendungen** wurde mit Beispielen für den mobilen Versand aktualisiert – [Weitere Informationen](../../sending/using/previewing-messages.md)

Best Practices für Transaktionsnachrichten und das Löschen nicht verwendeter Echtzeit-Ereignisse wurden hinzugefügt – [Weitere Informationen](../../channels/using/configuring-transactional-event.md#creating-an-event)

Der Abschnitt zum Konfigurieren des E-Mail-Kanals wurde aktualisiert und enthält nun Informationen zu allen E-Mail-Einstellungen, die jetzt vom erweiterten MTA von Adobe Campaign verwaltet werden – [Weitere Informationen](../../administration/using/configuring-email-channel.md)

Der Abschnitt zu den Transaktionsnachrichten wurde aktualisiert und enthält nun weiterführende Informationen zu den Berechtigungen, die zum Bearbeiten von Ereigniskonfigurationen und zum Anreichern von Sammlungen in Transaktionsnachrichten erforderlich sind. [Weitere Informationen](../../channels/using/configuring-transactional-event.md)

## Version 20.2 – April 2020 {#release-20-2---april-2020}

**Neue Funktionen in der Version**

Azure Blob-Integration – [mehr dazu](../../administration/using/external-accounts.md#microsoft-azure-external-account)

E-Mail-Tests mit Zielgruppenprofilen – [mehr dazu](../../sending/using/testing-messages-using-target.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Beim Rendering von In-App-Nachrichten wurde eine Einschränkung hinzugefügt. [Weitere Informationen](../../channels/using/customizing-an-in-app-message.md)

Es wurden Informationen zur Verwendung von Aggregaten in einer **[!UICONTROL Abfrage]**-Aktivität hinzugefügt – [Weitere Informationen](../../automating/using/query.md#adding-an-aggregate)

Beim Konfigurieren einer Mobile App wurden eine Einschränkung mit MCPNS hinzugefügt – [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html)

Dem Administratorhandbuch wurde ein neuer Abschnitt mit Konfigurationsrichtlinien hinzugefügt. Der Abschnitt zu kompatiblen Browsern und Betriebssystemen wurde aus den ersten Schritten in diesen Abschnitt verschoben. Dieser Abschnitt enthält auch die Technote zu Campaign Standard-Netzwerkendpunkten – [Weitere Informationen](../../administration/using/about-configuration-guidelines.md)

Es gibt jetzt einen neuen Abschnitt zum Löschen einer Ereigniskonfiguration – [Weitere Informationen](../../channels/using/publishing-transactional-event.md#deleting-an-event)

Die Abschnitte für den Transaktionsnachrichtenversand wurden entsprechend den zahlreichen geringfügigen Aktualisierungen und Verbesserungen der Benutzeroberfläche aktualisiert – [Weitere Informationen](../../channels/using/getting-started-with-transactional-msg.md)

Informationen zu den Schutzmaßnahmen für externe API-Aktivitäten wurden aktualisiert – [Weitere Informationen](../../automating/using/external-api.md)

## März 2020 {#doc-updates-march-2020}

Genauere Informationen über den erweiterten MTA wurden der Hauptdokumentation hinzugefügt, insbesondere bezüglich der Regeln zum Umgang mit E-Mails und der Qualizierung von Bounce Messages – [Weitere Informationen](../../administration/using/configuring-email-channel.md#email-processing-rules)

Der Abschnitt zum Archivieren mit E-Mail-BCC wurde verschoben und aktualisiert – [Weitere Informationen](../../sending/using/archiving.md)

Die Dokumentation zur Konfiguration einer mobilen App und zugehörige Seiten wurden aktualisiert, da SDK V4 entfernt wurde – [Weitere Informationen](https://experienceleague.adobe.com/docs/discontinued/using/mobile-services.html?lang=de)

Die Dokumentation zur Integration von Adobe Campaign Standard mit Adobe Experience Manager wurde aktualisiert und verbessert – [Weitere Informationen](../../integrating/using/configure-experience-manager.md)

Die Dokumentation zu Campaign E-Mail-Designer und zugehörige Seiten wurden aktualisiert, da [!DNL Adobe Creative SDK] entfernt wurde – [Weitere Informationen](../../rn/using/deprecated-features.md)

Ein neuer Abschnitt über Best Practices für Datenmodelle in Campaign Standard ist jetzt verfügbar – [Weitere Informationen](../../developing/using/data-model-best-practices.md)

Informationen wurden zur nativen Berechtigung **[!UICONTROL Workflows]** hinzugefügt – [Weitere Informationen](../../administration/using/list-of-roles.md)

Es wurden Informationen zum Feld **[!UICONTROL Verlauf in Tagen]** hinzugefügt, das in den Eigenschaften von Workflows verfügbar ist – [Weitere Informationen](../../automating/using/about-workflow-execution.md)

## Version 20.1 – Februar 2020 {#release-20-1---february-2020}

**Neue Funktionen in dieser Version**

Adobe Experience Platform Data Connector (Beta-Version)

Audience Destinations (Beta-Version)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Die Dokumentation zur Datenschutzverwaltung wurde aktualisiert und enthält Informationen zum Erstellen des CCPA-Opt-out-Felds für benutzerdefinierte Profilressourcen – [Weitere Informationen](https://helpx.adobe.com/content/help/de/campaign/kb/acs-privacy.html)

Die Versionshinweise wurden neu organisiert und verbessert – [Weitere Informationen](../../rn/using/release-notes.md)

Es wurden Informationen zur Sicherheitsgruppe „Administratoren“ hinzugefügt, in denen darauf hingewiesen wird, dass die Organisationseinheit **[!UICONTROL Alle (all)]** ihr zugewiesen ist und nicht geändert werden kann – [Weitere Informationen](../../administration/using/managing-groups-and-users.md)

Es wurden Informationen darüber hinzugefügt, wie man eine bestimmte Zeitzone definiert, die standardmäßig in einem Workflow verwendet werden soll – [Weitere Informationen](../../automating/using/building-a-workflow.md)

Im Handbuch zum Arbeiten mit APIs wurden Informationen zum neuen Parameter **_forcePagination=true** hinzugefügt, mit dem Sie Paginierungen bei großen Tabellen durchführen können – [Weitere Informationen](../../api/using/pagination.md)

Ein neuer Abschnitt, in dem die in einem Nachrichten-Dashboard angezeigten Warnhinweise beschrieben werden, ist verfügbar – [Weitere Informationen](../../channels/using/message-dashboard.md#warnings)

Die Dokumentation zum erweiterten MTA von Adobe Campaign ist jetzt verfügbar. In ihr wird die aktualisierte Versandinfrastruktur beschrieben, die besseren Durchsatz sowie verbesserte Zustellbarkeit und Bounce-Handhabung ermöglicht. – [mehr dazu](https://helpx.adobe.com/de/campaign/kb/campaign-enhanced-mta.html)

Es wurden Hinweise hinzugefügt, die darüber informieren, dass die URLs des Anwendungs-Servers und des Mirrorseiten-Servers sicher sein müssen, damit die Vorschau der Landingpage und der Mirrorseite über die Benutzeroberfläche von Campaign angezeigt werden kann – [Weitere Informationen](../../administration/using/branding.md#configuring-and-using-brands)

Der Abschnitt zum Exportieren von Protokollen wurde aktualisiert, um über die Verfügbarkeit der Versandlog-ID in den Ressourcen Versandlogs und Trackinglogs zu informieren, mit der für jedes Protokoll eine eindeutige Kennung exportiert werden kann – [Weitere Informationen](../../automating/using/exporting-logs.md)

## Januar 2020 {#doc-updates-january-2020}

Die Dokumentation zur Zustellbarkeit wurde um einen neuen Abschnitt zur IP-Zertifizierung ergänzt. <!--[Read more](../../sending/using/ip-certification.md)-->

Es steht ein neuer Abschnitt zur Verfügung, in dem beschrieben wird, wie Sie einen Workflow für einen kanalübergreifenden Versand erstellen – [Weitere Informationen](../../automating/using/workflow-cross-channel-delivery.md)

Der Abschnitt über die Indikatorberechnung für dynamische Berichte wurde aktualisiert – [Weitere Informationen](../../reporting/using/indicator-calculation.md)

Eine neue Seite mit allgemeinen Richtlinien für Mobile-Sendungen in Adobe Campaign Standard wurde hinzugefügt – [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/acs-mobile.html)

Die Dokumentation zum Verwenden von Campaign und Experience Manager wurde um den Abschnitt **Tipps zur Verwendung der Integration zwischen Campaign und Experience Manager** ergänzt – [Weitere Informationen](../../integrating/using/integrating-with-experience-manager.md#tips-aem)

Die Startseite der API-Dokumentation wurde durch Weiterleitungen zu den verschiedenen Themen verbessert – [Weitere Informationen](../../api/using/get-started-apis.md)

## November – Dezember 2019 {#doc-updates-december-2019}

Die Dokumentation zum Konfigurieren eines externen S3-Kontos wurde aktualisiert – [Weitere Informationen](../../administration/using/external-accounts.md#amazon-s3-external-account)

Der Abschnitt zum Entwerfen von E-Mail-Inhalten wurde neu strukturiert – [Weitere Informationen](../../designing/using/designing-content-in-adobe-campaign.md)

Die ersten Schritte zum Thema Zustellbarkeit wurden in die Hauptdokumentation integriert und aktualisiert – [Weitere Informationen](../../sending/using/about-deliverability.md)

Die ersten Schritte zum Thema Exportieren/Importieren benutzerdefinierter Ressourcen wurden in die Hauptdokumentation integriert – [Weitere Informationen](../../automating/using/exporting-importing-custom-resources.md)

Ein neues Anwendungsbeispiel wurde hinzugefügt, in dem beschrieben wird, wie eine Kontrollgruppe mithilfe eines Workflows in Campaign Standard erstellt wird –

Informationen zu den Eigenschaften von Landingpages wurden in einen eigenen Abschnitt verschoben. [Weitere Informationen](../../channels/using/configuring-landing-page.md)

Die Control Panel-Dokumentation wurde in den neuen kollaborativen Dokumentationssatz integriert. [Weitere Informationen](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=de)

Die Tabelle mit **Indikatorberechnungen** wurde aktualisiert – [Weitere Informationen](../../reporting/using/indicator-calculation.md)

Der API-Dokumentationssatz wurde in die Dokumentation von Campaign Standard integriert –[Weitere Informationen](../../api/using/get-started-apis.md)

Die ersten Schritte zum Thema Erstellen einer personalisierten E-Mail wurden verschoben und aktualisiert – [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/acs-get-started-with-emails.html)

Die ersten Schritte zum Thema Best Practices für den Versand wurden aktualisiert. [Weitere Informationen](../../sending/using/delivery-best-practices.md)

Das Datenmodell wurde in die Dokumentation von Campaign Standard integriert – [Weitere Informationen](../../developing/using/datamodel-audience.md)

Der API-Dokumentation wurde der neue API-Endpunkt **/customResources** hinzugefügt. [Weitere Informationen](../../api/using/interacting-with-custom-resources.md)

## Version 19.4 – Oktober 2019 {#release-19-4---october-2019}

**Neue Funktionen in der Version**

California Consumer Privacy Act (CCPA) – [mehr dazu](https://helpx.adobe.com/content/help/de/campaign/kb/acs-privacy.html#ccpa)

Microsoft Dynamics 365-Integration (GA) – [mehr dazu](../../integrating/using/d365-acs-get-started.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Die Liste der Fehlermeldungen für Adobe Campaign wurde aktualisiert – [Weitere Informationen](https://experienceleague.adobe.com/developer/campaign-errors/error_codes.html?lang=de)

Die ersten Schritte zum Thema DSGVO wurden verbessert und erweitert. Es handelt sich nun um eine Dokumentation rund um die Gewährleistung von Datenschutz gemäß den Bestimmungen der DSGVO und des CCPA. [Weitere Informationen](https://helpx.adobe.com/content/help/de/campaign/kb/campaign-privacy.html)

Eine neue Grafik wurde hinzugefügt, die den Veröffentlichungsprozess von Transaktionsnachrichten aufzeigt – [Weitere Informationen](../../channels/using/publishing-transactional-message.md#transactional-messaging-pub-process)

Die ersten Schritte zum Thema Best Practices beim Versand wurden aktualisiert – [Weitere Informationen](../../sending/using/delivery-best-practices.md)

Ein neuer Abschnitt wurde hinzugefügt: Dieser beinhaltet eine Übersicht über die verschiedenen Methoden zur Anreicherung der Campaign Standard-Datenbank – [Weitere Informationen](../../audiences/using/enriching-campaign-database.md)

Ein neuer Abschnitt bezüglich der Formatierung von Links mithilfe von E-Mail-Designer wurde ergänzt – [Weitere Informationen](../../designing/using/styles.md#about-styling-links)

Der API-Dokumentation wurden Informationen zum Datenschutz hinzugefügt; [klicken Sie hier](../../api/using/creating-a-privacy-request.md).

## September – Oktober 2019 {#doc-updates-october-2019}

Es wurde ein neuer Abschnitt bezüglich der Campaign Standard-Einstellungen hinzugefügt – [Weitere Informationen](../../administration/using/about-campaign-standard-settings.md)

Es wurde ein neuer Abschnitt hinzugefügt, in dem das automatische Versenden einer benutzerdefinierten Bestätigungs-E-Mail an Profile erläutert wird, die sich für einen spezifischen Dienst angemeldet haben – [Weitere Informationen](../../audiences/using/confirming-subscription-to-a-service.md)

Der Abschnitt „Transaktionsnachrichten“ wurde entsprechend den neuesten Aktualisierungen der Benutzeroberfläche betreffend der Bearbeitung von Inhalten sowie E-Mail-Designer angepasst – [Weitere Informationen](../../channels/using/editing-transactional-message.md)

Das Kapitel „Landingpages“ wurde umstrukturiert. Es wurde außerdem um einen neuen Abschnitt erweitert, in dem die Schritte zur Einrichtung einer Landingpage beschrieben werden – [Weitere Informationen](../../channels/using/getting-started-with-landing-pages.md)

Im Abschnitt &quot;Push-Benachrichtigungen&quot; wurde ein neuer Abschnitt hinzugefügt, in dem beschrieben wird, wie Sie Profilinformationen erstellen und aktualisieren, die auf den Abonnementdaten für Mobile Apps basieren – [Weitere Informationen](../../channels/using/updating-profile-with-mobile-app-data.md)

Ein neues Beispiel wurde hinzugefügt, das zeigt, wie eine E-Mail mit zusätzlichen Daten gesendet werden kann, die aus der Aktivität &quot;Datei laden&quot; abgerufen wurden – [Weitere Informationen](../../automating/using/sending-email-enriched-fields.md)

Ein neuer Abschnitt zur Verwendung von Fallen wurde hinzugefügt – [Weitere Informationen](../../sending/using/using-traps.md)

Auf der Seite zur Konfiguration einer Mobile App mit Adobe Experience Platform SDKs wurde zur Option **Launch_URL_Campaign** ein Hinweis hinzugefügt – [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html)

Das Handbuch zu E-Mail-Designer wurde neu organisiert – [Weitere Informationen](../../designing/using/designing-content-in-adobe-campaign.md)

## August 2019 {#doc-updates-august-2019}

Ein neuer Abschnitt mit Anwendungsfällen zu Workflows, bei denen Abfragen erforderlich sind, wurde hinzugefügt – [Weitere Informationen](../../automating/using/workflow-created-query-with-complement.md)

Im Abschnitt mit der Workflow-Fehlerbehebung wurde eine Beschreibung hinzugefügt, wie SQL-Abfragen in der Protokolltabelle angezeigt werden können – [Weitere Informationen](../../automating/using/best-practices-workflows.md#troubleshooting-data-management-activities)

Ein neuer Hilfeartikel wurde hinzugefügt, der Informationen über Subdomains und die Verwaltung von Zertifikaten im Control Panel enthält – [Weitere Informationen](https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=de)

Der Abschnitt, in dem Inhaltsvorlagen und Fragmente beschrieben werden, wurde aktualisiert – [Weitere Informationen](../../designing/using/using-reusable-content.md#content-templates)

Ein neuer Abschnitt zum Speichern von E-Mail-Inhalt als Vorlage in E-Mail-Designer wurde hinzugefügt – [Weitere Informationen](../../designing/using/using-reusable-content.md#saving-content-as-template)

## Version 19.3 – Juli 2019 {#release-19-3---july-2019}

**Neue Funktionen in der Version**

Externe API-Aktivität (öffentliche Betaversion) – [mehr dazu](../../automating/using/external-api.md)

Bericht zu Workflow-Segmenten – [mehr dazu](../../reporting/using/creating-a-report-workflow-segment.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Das Implementierungshandbuch für Campaign Standard ist jetzt online –[Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/campaign-standard-implementation-guide.html)

Zur Implementierung und Nutzung des Microsoft Dynamics 365-Connectors wurden neue Hilfeartikel erstellt – Beachten Sie, dass diese Funktion derzeit nur eingeschränkt verfügbar ist –[Weitere Informationen](../../integrating/using/d365-acs-get-started.md)

Im Abschnitt [Workflow mit Parametern aufrufen](../../automating/using/calling-a-workflow-with-external-parameters.md) wurde ein Hinweis zur Versandvorbereitung und zum Aggregat-Zeitraum hinzugefügt.

Außerdem wurde der Abschnitt mit Informationen darüber ergänzt, wie der Titel eines Versands mit Ereignisvariablen personalisiert werden kann, die in der Aktivität „Externes Signal“ des Workflows deklariert wurden. [Weitere Informationen](../../automating/using/external-signal.md)

Ein neuer Abschnitt wurde hinzugefügt, in dem erläutert wird, wie ein Benutzer in Adobe Campaign Standard erstellt werden kann – [Weitere Informationen](../../administration/using/users-management.md)

Jetzt ist ein neuer Artikel mit Tipps verfügbar, um Marketing-Kampagnen zu vereinfachen, einschließlich Links zur Produktdokumentation und zu Tutorials –[Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/simplify-campaign-management.html)

Für dynamische Berichte wurde ein Abschnitt zur Fehlerbehebung hinzugefügt – [Weitere Informationen](../../reporting/using/troubleshooting.md)

Ein Diagramm mit einer Erklärung, wie unterschiedliche In-App-Vorlagen personenbezogene Daten handhaben, wurde hinzugefügt – [Weitere Informationen](../../channels/using/preparing-and-sending-an-in-app-message.md)

Der Abschnitt zum Speichern von E-Mail-Inhalt als Fragment in E-Mail-Designer wurde aktualisiert – [Weitere Informationen](../../designing/using/using-reusable-content.md#saving-content-as-a-fragment)

Ein Warnhinweis wurde hinzugefügt, in dem erklärt wird, wie sich zusätzliche Leerzeichen auf das Layout eines E-Mail-Inhalts auswirken können – [Weitere Informationen](../../designing/using/personalization.md#creating-custom-content-blocks)

Ein neuer Abschnitt zu empfohlenen Updates von E-Mail-Designer wurde hinzugefügt – [Weitere Informationen](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-updates)

<!-- A new section on how to send proofs using real customer data has been added. [Read more](../../sending/using/managing-test-profiles-and-sending-proofs.md#sending-proofs-using-additional-data) -->

Ein neuer Abschnitt über Best Practices bei Workflows wurde hinzugefügt – [Weitere Informationen](../../automating/using/best-practices-workflows.md)

Die Liste der Fehlermeldungen für Campaign Standard und Classic wurde aktualisiert – [Weitere Informationen](https://experienceleague.adobe.com/developer/campaign-errors/error_codes.html?lang=de)

Eine Warnung in der Dokumentation über benutzerdefinierte Ressourcen wurde hinzugefügt. Es wird empfohlen, für die Kennung benutzerdefinierter Ressourcen maximal 30 Zeichen zu verwenden. Dies gilt auch für Felder von benutzerdefinierten Ressourcen, Schlüsseln, Indizes und Links – [Weitere Informationen](../../developing/using/creating-or-extending-the-resource.md)

## Juni – Juli 2019 {#doc-updates-2019}

Eine neue Seite zu Einschränkungen bei Landingpages wurde hinzugefügt – [Weitere Informationen](../../channels/using/getting-started-with-landing-pages.md#landing-page-limitations)

Ein Anwendungsbeispiel wurde hinzugefügt, das zeigt, wie ein Profil mithilfe eines zusammengesetzten Identifizierungsschlüssels aufgerufen werden kann – [Weitere Informationen](../../developing/using/uc-calling-resource-id-key.md)

Eine Empfehlung bezüglich der Verwendung wiederkehrender Sendungen ohne Aggregat-Zeitraum beim Aufruf eines Workflows mit Parametern wurde hinzugefügt – [Weitere Informationen](../../automating/using/calling-a-workflow-with-external-parameters.md)

Die Liste der Fehlermeldungen für Campaign Standard und Classic wurde aktualisiert – [Weitere Informationen](https://experienceleague.adobe.com/developer/campaign-errors/error_codes.html?lang=de)

Eine Warnung in der Dokumentation über benutzerdefinierte Ressourcen wurde hinzugefügt. Es wird empfohlen, für die Kennung benutzerdefinierter Ressourcen maximal 30 Zeichen zu verwenden. Dies gilt auch für Felder von benutzerdefinierten Ressourcen, Schlüsseln, Indizes und Links – [Weitere Informationen](../../developing/using/creating-or-extending-the-resource.md)

## Version 19.2 – Mai 2019 {#release-19-2---may-2019}

**Neue Funktionen in der Version**

Control Panel – [mehr dazu](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=de)

Lokale Benachrichtigungen – [mehr dazu](../../channels/using/customizing-an-in-app-message.md#customizing-a-local-notification-message-type)

Verbesserung bei Workflows – Hinzufügen einer Payload zur Aktivität &quot;Externes Signal&quot; – [mehr dazu](../../automating/using/calling-a-workflow-with-external-parameters.md)

Verbesserung bei Landingpages – Google reCAPTCHA – [mehr dazu](../../channels/using/configuring-landing-page.md#setting-google-recaptcha)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Der Artikel &quot;Adobe Campaign und Delegation des Domain-Namens&quot; wurde aktualisiert – [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/domain-name-delegation.html)

Ein neuer Artikel zur Releaseplanung wurde veröffentlicht, in der bekannt gegeben wird, wann die nächste Version verfügbar ist – [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/acs-release-planning.html)

Die Links zur kontextuellen Hilfe, die direkt in Adobe Campaign verfügbar sind, wurden aktualisiert.

Die folgende [Seite](https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/overview.html?lang=de) ist von nun an die offizielle Videoseite für Adobe Campaign Standard.

Ein Abschnitt zur Datenbeibehaltung wurde hinzugefügt, einschließlich der standardmäßigen Aufbewahrungswerte für Standardtabellen – [Weitere Informationen](../../administration/using/data-retention.md)

Ein Abschnitt zu Aktualisierungen und Wartungsverfahren wurde hinzugefügt – [Weitere Informationen](../../administration/using/updates-and-maintenance-operations.md)

Informationen zur neuen Sortieroption in der Aktivität **Dateitransfer** wurden hinzugefügt – [Weitere Informationen](../../automating/using/transfer-file.md)

Die [REST-APIs-Dokumentation](../../api/using/get-started-apis.md) wurde aktualisiert:

* Ein neuer Abschnitt wurde hinzugefügt mit allgemeinen Informationen zur Verwendung von Campaign Standard-REST-APIs.
* Eine Sammlung vordefinierter API-Anfragen für häufige Anwendungsfälle wurde bereitgestellt.
* Ein neuer Abschnitt zur Verwaltung von Organisationseinheiten wurde hinzugefügt.
* Informationen zur Erstellung eines Dienstes wurden hinzugefügt.
* Informationen, wie ein Workflow mit Parametern ausgeführt werden kann, wurden hinzugefügt.

Informationen zur neuen **Test**-Aktivität wurden hinzugefügt – [Weitere Informationen](../../automating/using/test.md)

Das Automating-Benutzerhandbuch wurde mit Links zu verwandten Workflow-Aktivitäten aktualisiert – [Weitere Informationen](../../automating/using/workflow-interface.md#palette)

Der Abschnitt über die Indikatorberechnung für dynamische Berichte wurde aktualisiert – [Weitere Informationen](../../reporting/using/indicator-calculation.md)

Eine Kompatibilitätstabelle für dynamische Berichte wurde hinzugefügt, um die Kompatibilität zwischen Dimensionen und Metriken zu veranschaulichen – [Weitere Informationen](https://experienceleague.adobe.com/docs/campaign-standard/assets/dynamic_report_compatibility.pdf)

Die Liste der Funktionen für Workflows wurde aktualisiert – [Weitere Informationen](../../automating/using/list-of-functions.md)

Das Kapitel über die Inhaltserstellung wurde aktualisiert und enthält jetzt einen neuen Abschnitt mit einer genauen Beschreibung der unterschiedlichen Methoden zur Erstellung einer E-Mail mit E-Mail-Designer unter Verwendung vorhandener Inhalte – [Weitere Informationen](../../designing/using/using-existing-content.md)

Ein neuer Abschnitt zum Speichern von E-Mail-Inhalt als Fragment in E-Mail-Designer wurde hinzugefügt – [Weitere Informationen](../../designing/using/using-reusable-content.md#saving-content-as-a-fragment)

Der Abschnitt zur Link-Verwaltung wurde mit zusätzlichen Informationen zur Verwaltung getrackter URLs in E-Mail-Designer ergänzt – [Weitere Informationen](../../designing/using/links.md#inserting-a-link)

Ein neuer Abschnitt wurde hinzugefügt, in dem der Wiederholungsvorgang bei Transaktionsnachrichten beschrieben wird – [Weitere Informationen](../../channels/using/transactional-message-execution.md#transactional-message-retry-process)

Der Abschnitt zur Veröffentlichung einer Ressource mit einer API-Erweiterung wurde verständlicher gemacht und mit den aktuellen Änderungen in der Benutzeroberfläche ergänzt – [Weitere Informationen](../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension)

Der Abschnitt über die Archivierung von E-Mails wurde umbenannt und neu strukturiert – [Weitere Informationen](../../sending/using/archiving.md)

Der Abschnitt zur E-Mail-Erstellung wurde aktualisiert und enthält jetzt die aktuellen Änderungen in der Benutzeroberfläche – [Weitere Informationen](../../channels/using/creating-an-email.md)

Der Knowledge-Base-Artikel zum [SMS-Schnittstellenprotokoll und dessen Konfiguration](https://helpx.adobe.com/de/campaign/kb/sms-connector-protocol-and-settings.html) wurde aktualisiert und enthält jetzt die neue Option des externen SMS-Kontos zur Begrenzung der Anzahl der zulässigen MTA-Instanzen bei der Verbindung mit dem SMPP-Provider.

Das Erste-Schritte-Handbuch wurde erweitert und neu strukturiert – [Weitere Informationen](../../start/using/about-campaign-standard.md)

Die Seite mit veralteten und entfernten Funktionen wurde aktualisiert – [Weitere Informationen](../../rn/using/deprecated-features.md)

Der Abschnitt zur Dreamweaver-Integration wurde aktualisiert und verbessert – [Weitere Informationen](../../designing/using/using-integrations.md#editing-content-in-dreamweaver)

## Version 19.1 – Februar 2019 {#release-19-1---february-2019}

**Neue Funktionen in der Version**

Verbesserungen bei Push-Kanal-Berichten – [mehr dazu](../../reporting/using/push-notification-report.md)

Integration von Adobe Launch für Mobile Apps – [mehr dazu ](../../administration/using/configuring-a-mobile-application.md#using-adobe-experience-platform-sdk)

Mobile In-App-Nachrichten – [mehr dazu](../../channels/using/about-in-app-messaging.md)

Workflow-Verbesserungen – mehr dazu [hier](../../automating/using/workflow-interface.md#duplicating-workflow-activities) und [hier](../../automating/using/load-file.md#configuration)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Eine neue Einführung zur Erstellung von E-Mail-Inhalten und andere Verbesserungen bei E-Mail-Designer wurden zum Abschnitt zur Bearbeitung von E-Mail-Inhalten hinzugefügt – [Weitere Informationen](../../designing/using/designing-content-in-adobe-campaign.md#email-designer-home-page)

Ein neuer Abschnitt zu Beschränkungen bei Transaktionsnachrichten wurde hinzugefügt – [Weitere Informationen](../../channels/using/transactional-messaging-limitations.md)

Ein neuer Abschnitt wurde hinzugefügt, in dem die unterschiedlichen Möglichkeiten zum Erstellen von E-Mails in Adobe Campaign verglichen werden – [Weitere Informationen](../../designing/using/using-integrations.md#email-design-options-comparison)

Der Abschnitt zur Erstellung von benutzerdefinierten Inhaltsbausteinen wurde durch Informationen zu Zielgruppendimensionen ergänzt – [Weitere Informationen](../../designing/using/personalization.md#creating-custom-content-blocks)

Eine Warnung wurde hinzugefügt, die Benutzer darauf hinweist, dass E-Mail-Designer nicht Internet Explorer 11 unterstützt – [Weitere Informationen](../../administration/using/about-configuration-guidelines.md)

Zum Abschnitt über das Löschen einer Ressource wurde eine Warnung hinzugefügt, die Benutzer auf die Auswirkungen eines neuen Entwurfs hinweist – [Weitere Informationen](../../developing/using/deleting-a-resource.md)

Das Kapitel über das Hinzufügen bzw. Erweitern einer Ressource wurde aktualisiert – [Weitere Informationen](../../developing/using/creating-or-extending-the-resource.md)

Ein Anwendungsbeispiel zum Erweitern der benutzerdefinierte Ressource für Profile wurde hinzugefügt – [Weitere Informationen](../../developing/using/extending-the-profile-resource-with-a-new-field.md)

Eine Beschreibung zum Verknüpfen von benutzerdefinierten Ressourcen wurde hinzugefügt – [Weitere Informationen](../../developing/using/configuring-the-resource-s-data-structure.md#defining-links-with-other-resources)

Eine neue Technote wurde hinzugefügt, in der beschrieben wird, wie ein Bild in einer Push-Benachrichtigung in Adobe Campaign Standard angezeigt wird – [Weitere Informationen](../../administration/using/image-push-notification.md)

Eine neue Technote zur Implementierung von Tracking von Push-Benachrichtigungen wurde hinzugefügt – [Weitere Informationen](../../administration/using/push-tracking.md)

Die Liste der Fehlermeldungen für Campaign Standard und Classic wurde aktualisiert – [Weitere Informationen](https://experienceleague.adobe.com/developer/campaign-errors/error_codes.html?lang=de)

Die Dokumentation zur Integration von Triggers mit Campaign wurde aktualisiert – [Weitere Informationen](../../integrating/using/about-adobe-experience-cloud-triggers.md)

Die Links zur kontextuellen Hilfe, die direkt in Adobe Campaign verfügbar sind, wurden aktualisiert.

Ein Hinweis zum Hinzufügen von Zeitstempeln zum Namen der die Zurückweisungen enthaltenden Datei wurde hinzugefügt – [Weitere Informationen](../../automating/using/load-file.md#configuration)

Informationen zum Import von Feldern, die aus Spalten mit fixer Länge bestehen, wurden hinzugefügt – [Weitere Informationen](../../automating/using/load-file.md#configuration)

Informationen zur Option, mit der die Zurückweisungen in einer Datei gespeichert werden können, wurden hinzugefügt. Mit dieser Option kann eine Anschlussvorgangsetappe auf die Datei angewendet werden, die zurückgewiesene Datensätze enthält – [Weitere Informationen](../../automating/using/load-file.md#configuration)

Ein neuer Abschnitt zum Duplizieren von Workflow-Aktivitäten mit Copy &amp; Paste wurde hinzugefügt – [Weitere Informationen](../../automating/using/workflow-interface.md#duplicating-workflow-activities)

Zur neuen Option wurden Informationen in der Abfrage-Aktivität ([mehr dazu](../../automating/using/query-samples.md)) und der Segmentierungs-Aktivität ([mehr dazu](../../automating/using/segmentation.md)) hinzugefügt. Mit dieser Option kann an die Aktivität eine ausgehende Transition angeschlossen werden, wenn sie keine Daten abgerufen hat.

Im Abschnitt zur Daten-Update-Aktivität wurden Informationen hinzugefügt, in der das neue Batch-Größe-Feld beschrieben wird, mit dem die maximale Batch-Größe der hochzuladenden Daten definiert werden kann – [Weitere Informationen](../../automating/using/update-data.md#configuration)

Im Abschnitt zur Dateiextraktions-Aktivität wurde eine Beschreibung einer neuen Option hinzugefügt, mit der der Dateierstellungsprozess deaktiviert werden kann, wenn die ausgehende Transition leer ist – [Weitere Informationen](../../automating/using/extract-file.md#configuration)

## Version 19.0 – Januar 2019 {#release-19-0---january-2019}

**Neue Funktionen in der Version**

Allgemeine Verfügbarkeit von E-Mail-Designer – [mehr dazu](../../designing/using/designing-content-in-adobe-campaign.md)

Produktlisten in Transaktions-E-Mails – [mehr dazu](../../designing/using/using-product-listings.md)

Mobile-Ansicht in E-Mail-Designer – [mehr dazu](../../designing/using/plain-text-html-modes.md#switching-to-mobile-view)

Verbesserung von In-App-Messaging (Betaversion) – [mehr dazu](../../channels/using/about-in-app-messaging.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Das Handbuch zur Inhaltserstellung wurde aktualisiert und enthält jetzt Informationen zur allgemeinen Verfügbarkeit von E-Mail-Designer und der Einstellung des Legacy-E-Mail-Inhaltseditors – [Weitere Informationen](../../designing/using/designing-content-in-adobe-campaign.md)

Die Dokumentation zum [In-App Messaging](../../channels/using/about-in-app-messaging.md) und zu [Push-Benachrichtigungen](../../channels/using/about-push-notifications.md) wurde aktualisiert.

Informationen zu den unterschiedlichen Arten von Audiences in Adobe Campaign wurden hinzugefügt – [Weitere Informationen](../../audiences/using/about-audiences.md)

Das Kapitel &quot;Benutzer &amp; Sicherheit&quot; wurde aktualisiert, da die Verwendung geografischer Einheiten eingestellt wurde – [Weitere Informationen](../../administration/using/organizational-units.md)

Informationen zur neuen Option der Datenladeaktivität wurden hinzugefügt. Damit kann eine Anschlussvorgangsetappe auf die Datei angewendet werden, die zurückgewiesene Datensätze enthält (z. B. Komprimierung im ZIP-Format) – [Weitere Informationen](../../automating/using/load-file.md)

Informationen zum neuen Feld in der Daten-Update-Aktivität wurden hinzugefügt. Diese Option ermöglicht jetzt die Konfiguration der maximalen Batch-Größe für hochzuladende Daten – [Weitere Informationen](../../automating/using/update-data.md)

Die Dokumentation zum [Import von Inhalt aus einer URL](../../designing/using/using-existing-content.md#importing-content-from-a-url) wurde um Informationen zu E-Mail-Designer erweitert.

Microsoft Edge (Aktuelle Version) wurde zur Liste kompatibler Browser für Computer hinzugefügt – [Weitere Informationen](../../administration/using/about-configuration-guidelines.md)

Informationen zu einer neuen Option in der Dateiextraktionsaktivität wurden hinzugefügt. Damit kann jetzt verhindert werden, dass eine Datei erstellt wird, wenn die eingehende Transition leer ist – [Weitere Informationen](../../automating/using/extract-file.md)

Der Abschnitt zur Konfiguration einer Mobile App mit SDK V4 wurde [hierher](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdkv4.html) verschoben.

Der Abschnitt zur Konfiguration einer Mobile App mit Adobe Experience Platform SDKs wurde [hierher](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdk.html) verschoben.

Videos wurden aktualisiert und [hierher](https://experienceleague.adobe.com/docs/campaign-learn/campaign-standard-tutorials/overview.html?lang=de) verschoben.

Der Abschnitt zu den Typen von Benutzern wurde aktualisiert – [Weitere Informationen](../../administration/using/users-management.md)

## Version 18.9 - September 2018   {#release-18-9---september-2018}

**Neue Funktionen in der Version**

Verbesserung von In-App-Messaging (Betaversion) – [mehr dazu](../../channels/using/about-in-app-messaging.md)

Integration von Adobe Launch für Mobile Apps (Betaversion) – [mehr dazu ](../../sending/using/managing-typologies.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Aktualisiertes Handbuch zu Push-Benachrichtigungen einschließlich Änderungen der Benutzeroberfläche – [Weitere Informationen](../../channels/using/about-push-notifications.md)

Zusätzliche Informationen zum Löschen einer Audience – [Weitere Informationen](../../audiences/using/creating-audiences.md#deleting-audiences)

Aktualisierter Abschnitt zu Push-Benachrichtigungen in nativen Berichten. [Weitere Informationen](../../reporting/using/push-notification-report.md)

## Version 18.7 - Juli 2018   {#release-18-7---july-2018}

**Neue Funktionen in der Version**

[Versand mit hoher Priorität](../../channels/using/customizing-a-push-notification.md#change-the-notification-behavior-for-android) und [Typologiefilter](../../sending/using/managing-typologies.md) für Abonnenten mobiler Apps.

Automatischer Import von Inhalten von einer URL während der Nachrichtenvorbereitung – [Weitere Informationen](../../designing/using/using-existing-content.md#retrieving-content-from-a-url-automatically-at-preparation-time)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Eine neue Technote zum SMS-Schnittstellenprotokoll und dessen Konfiguration wurde hinzugefügt – [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/sms-connector-protocol-and-settings.html)

Die Dokumentation zur Integration von Experience Manager mit Adobe Campaign wurde aktualisiert – [Weitere Informationen](../../reporting/using/creating-a-custom-profile-dimension.md)

Das Handbuch zur Inhaltserstellung wurde neu strukturiert, um die Funktionsweise der beiden Editoren zu veranschaulichen, mit denen E-Mail-Content erstellt werden kann – [Weitere Informationen](../../designing/using/designing-content-in-adobe-campaign.md)

Hier erfahren Sie, wie Sie mit Creative SDK die Bearbeitung externer Inhalte ermöglichen können, indem Sie aus vorhandenen E-Mails Fragmente erstellen – [Weitere Informationen](../../designing/using/designing-from-scratch.md)

In diesem [Abschnitt](../../designing/using/using-existing-content.md#editing-existing-contents-with-the-email-designer) ist jetzt eine Liste der HTML-Attribute zur Gewährleistung der Kompatibilität mit Creative Designer verfügbar.

Informationen zur Standardsprache bei einer mehrsprachigen Vorlage wurden hinzugefügt – [Weitere Informationen](../../channels/using/multilingual-messages-template.md)

Ab Version 18.7 enthält das Handbuch für Benutzer &amp; Sicherheit nicht mehr die eingestellte Funktion der geografische Einheit für neue Campaign-Standard-Instanzen und für bestehende Instanzen, für die keine geografischen Einheiten erstellt wurden – [Weitere Informationen](../../rn/using/deprecated-features.md)

## Version 18.6 – Juni 2018 {#release-18-6---june-2018}

**Neue Funktionen in der Version**

Die API-Dokumentation wurde mit Informationen zur API **Verlauf** aktualisiert. Ein Anwendungsbeispiel wurde hinzugefügt, in dem erläutert wird, wie die Mirrorseite für eine an ein Profil gesendete Nachricht abgerufen werden kann – [Weitere Informationen](../../api/using/interacting-with-marketing-history.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Die Dokumentation zur Integration von Triggers mit Campaign wurde aktualisiert und umstrukturiert – [Weitere Informationen](../../integrating/using/about-adobe-experience-cloud-triggers.md)

Eine schrittweise Anleitung zur Erstellung einer benutzerdefinierten Profildimension wurde hinzugefügt – [Weitere Informationen](../../reporting/using/creating-a-custom-profile-dimension.md)

Die Dokumentation &quot;Campaign und Audience Manager oder People Core Service verwenden&quot; wurde umstrukturiert – [Weitere Informationen](../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md)

Die Definition der Benutzerrolle &quot;Sendungen vorbereiten&quot; wurde aktualisiert – [Weitere Informationen](../../administration/using/list-of-roles.md)

Im Abfrageaktivität-Abschnitt wurde ein Beispiel hinzugefügt, in dem erläutert wird, wie Profile ausgewählt werden können, die einen bestimmten Link in einem Versand angeklickt haben – [Weitere Informationen](../../automating/using/query-samples.md#targeting-profiles-who-clicked-a-specific-link-)

In der API-Dokumentation wurde ein Abschnitt zu **benutzerdefinierten Filtern** hinzugefügt – [Weitere Informationen](../../api/using/filtering.md)

## Version 18.5 – Mai 2018 {#release-18-5---may-2018}

**Neue Funktionen in der Version**

DSGVO: Core Service-Integration – [mehr dazu](../../start/using/privacy-management.md)

Verbesserung von Push-Benachrichtigungen – detailliertes Versand-Feedback – [mehr dazu](../../channels/using/preparing-and-sending-a-push-notification.md#sending-the-notification)

Erweiterung von Versandlogs – [mehr dazu](../../developing/using/configuring-the-resource-s-data-structure.md#defining-sending-logs-extension)

Dynamische Berichte mit benutzerdefinierten Profildaten – [mehr dazu](../../channels/using/creating-a-multilingual-push-notification.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Die Liste von in Analytics vorhandenen Campaign-Metriken wurde hinzugefügt – [Weitere Informationen](../../integrating/using/campaign-dimensions-and-metrics-in-analytics.md)

Informationen zum Lizenz-Menüeintrag im Menü &quot;Administration&quot; wurden hinzugefügt – [Weitere Informationen](../../administration/using/licenses.md)

Informationen wurden hinzugefügt, wie benutzerdefinierte Felder in einer Push-Benachrichtigung verwendet werden können – [Weitere Informationen](../../channels/using/customizing-a-push-notification.md#add-custom-fields)

Das Handbuch über Best Practices beim Versand wurde aktualisiert – [Weitere Informationen](../../sending/using/delivery-best-practices.md)

Informationen zu Trackinglog-Typen wurden hinzugefügt – [Weitere Informationen](../../sending/using/tracking-messages.md#tracking-logs)

Der Abschnitt zur Abfrageaktivität wurde mit Abfragebeispielen ergänzt – [Weitere Informationen](../../automating/using/query.md#query-samples)

Der Abschnitt zu den Blockierungslisten wurde in „Funktionsweise des Opt-in- und Opt-out-Verfahrens“ umbenannt. Jetzt enthält der Abschnitt Informationen, wie ein Opt-in zu bestimmten Kanälen verwaltet wird und wie Landingpages zum Verwalten von Opt-ins und Opt-outs erstellt werden – [Weitere Informationen](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

Best Practices für die Verwendung der von Adobe gehosteten SFTP-Server – [Weitere Informationen](../../administration/using/external-accounts.md#sftp-external-account)

Die Liste der unterstützten Analytics-Lösungen/Core Services für die Integration mit Triggers wurde aktualisiert – [Weitere Informationen](../../integrating/using/configuring-triggers-in-experience-cloud.md#configuring-solutions-and-services)

Für mehr Übersichtlichkeit wurde das Inhaltseditor-Handbuch neu strukturiert – [Weitere Informationen](../../designing/using/designing-content-in-adobe-campaign.md)

## Version 18.3 - März 2018   {#release-18-3---march-2018}

**Neue Funktionen in der Version**

EU-Datenschutz-Grundverordnung (DSGVO) – [mehr dazu](../../start/using/privacy.md)

Creative Designer für E-Mails – [mehr dazu](../../designing/using/designing-content-in-adobe-campaign.md)

Mehrsprachige Push-Benachrichtigungen – [mehr dazu](../../channels/using/creating-a-multilingual-push-notification.md)

Verwendung benutzerdefinierter Ressourcen in Transaktionsnachrichten – [mehr dazu](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Die GDPR API enthält Funktionen zur automatischen Verarbeitung von DSGVO-Abfragen – [Weitere Informationen](../../api/using/creating-a-privacy-request.md)

Informationen zur Einrichtung von Landingpages wurden hinzugefügt, über die sich Empfänger auf die Blockierungsliste setzen lassen können – [Weitere Informationen](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md)

Der Abschnitt [Transaktionsnachrichten konfigurieren](../../channels/using/configuring-transactional-event.md) wurde neu angeordnet und ein [schrittweises Anwendungsbeispiel](../../channels/using/transactional-messaging-use-case.md) wurde hinzugefügt.

Eine Technote wurde hinzugefügt, in der erklärt wird, wie eine mehrsprachige CSV-Datei für Push-Benachrichtigungen erstellt wird – [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/acs-generate-csv-multilingual-push.html)

Informationen zur Importvorlage **Aktualisierung von Briefpost-Quarantänen und Versandlogs** wurden hinzugefügt – [Weitere Informationen](../../automating/using/importing-data-with-import-templates.md#setting-up-import-templates)

Die Liste der technischen Workflows wurde aktualisiert – [Weitere Informationen](../../administration/using/technical-workflows.md)

Der Abschnitt zur Planungsaktivität wurde aktualisiert – [Weitere Informationen](../../automating/using/scheduler.md)

Die Liste der Hilfematerialien zur Integration von Campaign und Adobe-Lösungen wurde aktualisiert – [Weitere Informationen](../../integrating/using/get-started-campaign-integrations.md)

Die kontextuelle Hilfe von Campaign Standard wurde aktualisiert.

## Version 18.2 - Februar 2018   {#release-18-2---february-2018}

**Neue Funktionen in der Version**

Anmeldung: Eine Liste mit Profilen für mehrere Dienste an- oder abmelden – [mehr dazu](../../automating/using/subscription-services.md)

Aktivität „Anreicherung“: Reichern Sie Daten auf der Basis eingehender Transitionen an – [mehr dazu](../../automating/using/enrichment.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Die meisten URLs für die Integration von Campaign und Adobe-Lösungen wurden geändert! Überprüfen Sie Ihre Lesezeichen! – [Weitere Informationen](../../integrating/using/get-started-campaign-integrations.md)

Datamodel v1 ist jetzt mit der SQL-Struktur für native Ressourcen verfügbar – [mehr dazu](../../developing/using/datamodel-introduction.md)

Zusätzliche Informationen zur Vorbereitung einer Nachricht in einem Versand – [mehr dazu](../../sending/using/preparing-the-send.md)

Die Versionshinweise wurden auf verschiedenen Seiten neu angeordnet, sodass Sie eine umfassendere Übersicht über alle Versionen erhalten.

Der Abschnitt über **[!UICONTROL die Verwendung von Typologien]** wurde übersichtlicher gestaltet – [Weitere Informationen](../../sending/using/about-typology-rules.md)

Eine neue Option ist jetzt verfügbar, mit der die Performance gesteigert werden kann, wenn in einer **[!UICONTROL Abfrage]** zahlreiche Zusatzdaten definiert werden – [Weitere Informationen](../../automating/using/query-samples.md)

Das Beispiel für den Profilimport wurde aktualisiert und enthält jetzt Tipps, wie Sie Ihre Profile für den Empfang von Briefpost konfigurieren können – [Weitere Informationen](../../automating/using/about-data-import-and-export.md)

In Workflows ist eine neue Aktivität verfügbar: die Aktivität **[!UICONTROL Anreicherung]** – [Weitere Informationen](../../automating/using/enrichment.md)

Die Aktivität **[!UICONTROL An-/Abmeldedienst]** wurde aktualisiert und unterstützt jetzt mehr Anwendungsfälle, einschließlich der Verwendung einer einzigen Datei zur Aktualisierung von Anmeldungen bei mehreren Diensten – [Weitere Informationen](../../automating/using/subscription-services.md)

Eine schrittweise Anleitung zur Versandvorbereitung wurde hinzugefügt – [Weitere Informationen](../../sending/using/preparing-the-send.md)

Ein Abschnitt mit der Liste der Berechtigungen wurde entfernt. – [mehr dazu](https://experienceleague.adobe.com/docs/campaign-standard/assets/acs_rights.pdf) (PDF)

Eine schrittweise Anleitung zur Verwendung der automatischen SMS-Antwortfunktion wurde hinzugefügt – [Weitere Informationen](../../channels/using/managing-incoming-sms.md#managing-stop-sms)

Eine Anleitung wurde hinzugefügt, in der beschrieben wird, wie Nachrichten entsprechend der Zeitzone der Benutzer in einem wiederkehrenden Workflow gesendet werden können – [Weitere Informationen](../../automating/using/recurring-push-notifications.md)

Der Abschnitt **[!UICONTROL Push-Benachrichtigung anpassen]** wurde neu gestaltet und mit schrittweisen Anleitungen ergänzt – [Weitere Informationen](../../channels/using/customizing-a-push-notification.md)

Neuer Abschnitt zur Verwaltung von Blockierungslisten – [Weitere Informationen](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

Aktualisierte Informationen zu Versandproblemen und Quarantänen – [Weitere Informationen](../../sending/using/monitoring-a-delivery.md)

Neue Abschnitte zu [Zielgruppen-Mappings](../../administration/using/target-mappings-in-campaign.md), [Zielgruppendimensionen und Ressourcen](../../automating/using/query.md#targeting-dimensions-and-resources).

## Version 18.1 - Januar 2018   {#release-18-1---january-2018}

**Neue Funktionen in der Version**

Reporting für die Ermüdungsverwaltung – [mehr dazu](../../sending/using/fatigue-rules.md#viewing-the-fatigue-rule-summary-report)

Berichtfreigabe – [mehr dazu](../../reporting/using/reporting-interface.md#share-tab)

Verbesserungen bei Push-Benachrichtigungen – mehr dazu [hier](../../channels/using/preparing-and-sending-a-push-notification.md#preparing-the-notification) und [hier](../../channels/using/customizing-a-push-notification.md#change-the-notification-behavior-for-ios)

Zeitzonenoptimierte Sendungen – [mehr dazu](../../automating/using/scheduler.md)

Aktivierung der API-Signal-Aktivität – [mehr dazu](../../api/using/triggering-a-signal-activity.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Der Abschnitt zur Diensterstellung wurde aktualisiert – [Weitere Informationen](../../audiences/using/creating-a-service.md)

Anwendungsbeispiele zum besseren Verständnis von Sicherheitsgruppen und Einheiten wurden hinzugefügt – [Weitere Informationen](../../administration/using/organizational-units.md)

Verbesserte Definitionen und Berechnungen von Dimensionen, Metriken und Segmenten in dynamischen Berichten – [Weitere Informationen](../../reporting/using/list-of-components.md)

Zusätzliche Informationen zum Abrufen von eingehenden SMS-Nachrichten mit einem Workflow – [Weitere Informationen](../../administration/using/configuring-sms-channel.md)

Zusätzliche Informationen zu Verlaufsparametern der Dateiübertragungsaktivität – [Weitere Informationen](../../automating/using/transfer-file.md)

Die Anleitungen zur Konfiguration der Integration mit Audience Manager oder People Core Service wurden aktualisiert – [Weitere Informationen](../../integrating/using/integration-with-audience-manager-or-people-core-service.md)

## Version 17.10 - Oktober 2017   {#release-17-10---october-2017}

**Neue Funktionen in der Version**

Ermüdungsverwaltung – [mehr dazu](../../sending/using/fatigue-rules.md)

Inhaltserstellung: Import aus einer URL – [mehr dazu](../../designing/using/using-existing-content.md#importing-content-from-a-url)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Das Beispiel für einen A/B-Test wurde aktualisiert – [Weitere Informationen](../../channels/using/designing-an-a-b-test-email.md)

Neue Technote zur Erstellung oder Aktualisierung von Profildaten, wenn von einer Mobile App PII-Abrufdaten gesendet werden – [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/acs-updating-profile-based-on-subscription.html)

Abschnitt über neue Export-Tracking-Funktionen wurde hinzugefügt – [Weitere Informationen](../../administration/using/auditing-export-logs.md)

Details wurden zum nativen Package-Export hinzugefügt – [Weitere Informationen](../../automating/using/managing-packages.md)

Definition externer Konten und Beispiele wurden aktualisiert – [Weitere Informationen](../../administration/using/external-accounts.md)

Zahlreiche Screenshots wurden entsprechend den Änderungen in den Abfrageeditor-Kategorien aktualisiert.

Der Abschnitt [Versandwarnung](../../sending/using/receiving-alerts-when-failures-happen.md) wurde verschoben und neu angeordnet.

Der Abschnitt &#39;Benutzerdefinierte Ressourcen&#39; wurde besser erklärt, indem das [Definieren von Filtern](../../developing/using/configuring-filter-definition.md) genauer beschrieben wurde.

Die [Technote](https://helpx.adobe.com/de/campaign/kb/integrate-mobile-sdk.html) zur Integration von Adobe Experience Cloud Mobile SDK mit einer Mobile App zum Empfang von Push-Benachrichtigungen in Adobe Campaign Standard wurde aktualisiert und ausführlicher gestaltet.

Eine Technote wurde hinzugefügt, in der der Aufbau der in einer Mobile App empfangenen Payload erläutert wird. [mehr dazu](../../administration/using/push-payload.md)

Der [Abschnitt](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdkv4.html) zur Push-Kanal-Konfiguration wurde durch neue Payload-Daten ergänzt, die je nach Betriebssystem hinzugefügt werden, wenn Postbacks in der Adobe Mobile Services-Benutzeroberfläche definiert werden.

In der SMS-Dokumentation wurde der Abschnitt zu [automatischen SMS-Antworten](../../channels/using/managing-incoming-sms.md#managing-stop-sms) genauer erklärt.

Neuer Abschnitt zum Workflow-Management über die API – [Weitere Informationen](../../api/using/controlling-a-workflow.md)

Neuer Abschnitt zu Primärschlüsseln und zur Verwendung einer Kennung als Schlüssel in der API – [Weitere Informationen](../../api/using/get-started-apis.md)

Informationen zum Filtern mit einzelnen und mehreren Filtern in der API hinzugefügt – [Weitere Informationen](../../api/using/filtering.md)

## Version 17.9 – September 2017 {#release-17-9---september-2017}

**Neue Funktionen in der Version**

Bibliothek mit E-Mail-Vorlagen – [mehr dazu](../../designing/using/using-reusable-content.md#content-templates)

Dynamische Berichte mit Profildaten – [mehr dazu](../../reporting/using/about-dynamic-reports.md)

Verbesserung bei der gesammelten Anmeldung – [mehr dazu](../../automating/using/subscription-services.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Detaillierte Liste aller in dynamischen Berichten verfügbaren Komponenten sowie Formeländerungen – [Weitere Informationen](../../reporting/using/list-of-components.md)

Detaillierte Liste von mit Adobe Analytics geteilten KPIs – [Weitere Informationen](../../integrating/using/campaign-dimensions-and-metrics-in-analytics.md)

Neues Video zu dynamischen Berichten –

Empfehlungen für das S3-Konto wurden hinzugefügt – [Weitere Informationen](../../administration/using/external-accounts.md#amazon-s3-account-recommendations)

Der Abschnitt über die unterschiedlichen Benutzertypen wurde aktualisiert – [Weitere Informationen](../../administration/using/users-management.md)

Der Abschnitt über die Personalisierung von Bildquellen wurde aktualisiert – [Weitere Informationen](../../designing/using/personalization.md#personalizing-an-image-source)

Eine Dokumentation zu Berichten über aktive Profile wurde hinzugefügt – [Weitere Informationen](../../audiences/using/active-profiles.md)

Die Dokumentation zur [Versandwarnung](../../sending/using/receiving-alerts-when-failures-happen.md#delivery-alerting-reasons) wurde aktualisiert und enthält jetzt einen Abschnitt zur Problembehebung sowie Tipps zu den verfügbaren Optionen beim Empfang von Warnungen.

Ein neues Erste-Schritte-Handbuch ist verfügbar: Es enthält Best Practices für den Versand mit Adobe Campaign, von der Erstellung von Nachrichten über die Zielgruppenbestimmung bis zum Senden und Verfolgen von Nachrichten – [Weitere Informationen](../../sending/using/delivery-best-practices.md)

Die Dokumentation zu Folgenachrichten wurde mit einem verbesserten Anwendungsbeispiel ergänzt – [Weitere Informationen](../../channels/using/follow-up-messages.md#sending-a-follow-up-message)

Eine Dokumentation zur ACS-ID wurde hinzugefügt – [Weitere Informationen](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources)

Neue Verschlüsselungs- und Hashing-Funktionen sowie Beispiele wurden hinzugefügt – [Weitere Informationen](../../automating/using/list-of-functions.md)

Aktualisierter Abschnitt zur Workflow-Aktivität &quot;Dateiübertragung&quot; – [Weitere Informationen](../../automating/using/transfer-file.md)

Zur Option &quot;Vor dem Nachrichtenversand Bestätigung einholen&quot; in der Workflow-Aktivität &quot;E-Mail-Versand&quot; wurden Informationen hinzugefügt – [Weitere Informationen](../../automating/using/email-delivery.md)

## Version 17.7 - Juli 2017   {#release-17-7---july-2017}

**Neue Funktionen in der Version**

Mehrsprachige Sendungen (E-Mail &amp; SMS) – [mehr dazu](../../channels/using/creating-a-multilingual-email.md)

Benachrichtigungen in Adobe Campaign – [mehr dazu](../../administration/using/sending-internal-notifications.md)

Versandwarnung – [mehr dazu](../../sending/using/receiving-alerts-when-failures-happen.md)

Verschlüsselte Declared ID in Datenquellen – [mehr dazu](../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md)

KPI-Freigabe von Campaign für Analytics – [mehr dazu](../../integrating/using/about-campaign-analytics-integration.md)

Briefpost-Kanal: Rücksendungen an den Absender – [mehr dazu](../../channels/using/return-to-sender.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Die Erste-Schritte-Handbücher und die Anleitungsvideos befinden sich jetzt in einem eigenen Abschnitt.

Die Dokumentation zum E-Mail-Rendering wurde aktualisiert – [Weitere Informationen](../../sending/using/email-rendering.md)

Die Tabelle mit Indikatorberechnungen für Berichte wurde aktualisiert – [Weitere Informationen](../../reporting/using/indicator-calculation.md)

Die Dokumentation zur Berichterstellung wurde mit vier neuen Metriken ergänzt – [Weitere Informationen](../../reporting/using/list-of-components.md)

Eine Dokumentation zur Erstellung eindeutiger Profilkennungen wurde hinzugefügt – [Weitere Informationen](../../developing/using/configuring-the-resource-s-data-structure.md#generating-a-unique-id-for-profiles-and-custom-resources)

Zur Anmeldung mit zweifacher Bestätigung wurde eine schrittweise Anleitung hinzugefügt – [Weitere Informationen](../../channels/using/setting-up-a-double-opt-in-process.md)

Der Abschnitt zur Liste der Rollen wurde aktualisiert – [Weitere Informationen](../../administration/using/list-of-roles.md)

## Version 17.5 - Mai 2017   {#release-17-5---may-2017}

**Neue Funktionen in der Version**

Briefpost – [mehr dazu](../../channels/using/about-direct-mail.md)

E-Mail-BCC – [mehr dazu](../../sending/using/archiving.md)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Das Handbuch &quot;Sendungen&quot; wurde umstrukturiert und in &quot;Kanäle&quot; umbenannt – [Weitere Informationen](../../channels/using/get-started-communication-channels.md)

Zahlreiche Screenshots wurden entsprechend den Änderungen der Benutzeroberfläche aktualisiert.

Eine neue Technote ist verfügbar: &quot;Integrating the Adobe Mobile SDK with your mobile app&quot; – [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/integrate-mobile-sdk.html)

Eine Anleitung zur Konfiguration der Integration von People Core Service oder Audience Manager mit Adobe Campaign wurde hinzugefügt – [Weitere Informationen](../../integrating/using/integration-with-audience-manager-or-people-core-service.md)

Die Tabelle mit Berechtigungen wurde überarbeitet, sodass die Funktion gewisser Rollen jetzt klarer ist. [Weitere Informationen](https://experienceleague.adobe.com/docs/campaign-standard/assets/acs_rights.pdf)

Die Links zur kontextuellen Hilfe, die direkt in Adobe Campaign verfügbar sind, wurden aktualisiert.

## Version 17.4 - April 2017   {#release-17-4---april-2017}

**Neue Funktionen in der Version**

Verbesserte Bildbearbeitungsfähigkeiten mit dem Creative SDK – [mehr dazu](../../designing/using/images.md#modifying-images-with-the-adobe-creative-sdk)

Transaktions-Push-Benachrichtigungen – [mehr dazu](../../channels/using/transactional-push-notifications.md)

Wiederkehrende Push-Benachrichtigungen – [mehr dazu](../../automating/using/push-notification-delivery.md)

Amazon Simple Storage Service (S3) Connector – [mehr dazu](../../administration/using/external-accounts.md)

Integration von Dreamweaver live – [mehr dazu](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/designing-content/email-designer/dreamweaver-integration.html?lang=de)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Ein Abschnitt zu den unterschiedlichen Typen von Adobe Campaign-Benutzern wurde hinzugefügt – [Weitere Informationen](../../administration/using/users-management.md)

Das Workflow-Hasndbuch wurde umstrukturiert und erweitert. Dies ermöglicht das einfache Auffinden von Informationen zum [Erstellen](../../automating/using/building-a-workflow.md) und [Ausführen](../../automating/using/about-workflow-execution.md) eines Workflows, zur [Zielgruppenauswahl](../../automating/using/about-targeting-activities.md) und [Verwaltung](../../automating/using/about-targeting-activities.md#enriching-data) Ihrer Daten, zum [Import und Export](../../automating/using/about-data-import-and-export.md) von Daten und zur Nutzung von Workflow-Daten für die Aktualisierung der Datenbank oder für Sendungen.

Die Indikatorberechnung ist jetzt für dynamische Berichte verfügbar, einschließlich einer vollständigen Beschreibung und der Berechnungsformel – [Weitere Informationen](../../reporting/using/indicator-calculation.md)

Ein neuer Abschnitt zur Konfiguration von Adobe Mobile Services wurde hinzugefügt, sodass Push-Benachrichtigungen und Point-of-Interest-Daten in Adobe Campaign verwendet werden können – [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdkv4.html)

Die Abschnitte zur Mobile-App-Konfiguration und -Implementierung wurden aktualisiert, einschließlich detaillierter Schritte zum Einrichten und Senden von Push-Benachrichtigungen – [Weitere Informationen](https://helpx.adobe.com/de/campaign/kb/configuring-app-sdkv4.html)

Der Abschnitt zum Arbeiten mit Bildern in Campaign wurde aktualisiert – [Weitere Informationen](../../designing/using/images.md#setting-up-image-properties)

Die Integration mit Adobe Analytics for Mobile (Point of Interest) wurde aktualisiert, einschließlich Konfigurationsschritten und Anwendungsbeispielen – [Weitere Informationen](../../integrating/using/about-campaign-points-of-interest-data-integration.md)

## Version 17.2 - März 2017   {#release-17-2---march-2017}

**Neue Funktionen in der Version**

Dynamische Berichterstellung – [mehr dazu](../../reporting/using/about-dynamic-reports.md)

Dreamweaver-Integration (Labs) – [mehr dazu](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/designing-content/email-designer/dreamweaver-integration.html?lang=de)

Manuelle Optimierung des Versandzeitpunkts – [mehr dazu](../../sending/using/optimizing-the-sending-time.md)

Push-Benachrichtigungen: Verbesserungen – [mehr dazu](../../channels/using/about-push-notifications.md)

Workflows: Neue Signal-Aktivität – [mehr dazu](../../automating/using/external-signal.md)

Workflows: Neue Audience-lesen-Aktivität – [mehr dazu](../../automating/using/read-audience.md)

Points of Interest-Daten – [mehr dazu](../../integrating/using/about-campaign-points-of-interest-data-integration.md)

Verknüpfte Ressourcen in REST APIs – [mehr dazu](../../developing/using/updating-the-database-structure.md#publishing-a-resource-with-api-extension)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Triggers-Integration: zwei Anwendungsbeispiele wurden hinzugefügt – [Weitere Informationen](../../integrating/using/abandonment-triggers-use-cases.md)

Die API-Dokumentation für Entwickler wurde durch neue Informationen und Code-Snippets ergänzt und ist jetzt benutzerfreundlicher – [Weitere Informationen](../../api/using/get-started-apis.md)

Zu den neuen Workflow-Aktivitäten [Audience lesen](../../automating/using/read-audience.md) und [Externes Signal](../../automating/using/external-signal.md) wurden Beispiele hinzugefügt.

## Version 17.1 - Januar 2017   {#release-17-1---january-2017}

**Neue Funktionen in der Version**

Protokollexport für die externe Berichterstattung – [mehr dazu](../../automating/using/exporting-logs.md)

Transactional Messaging-API – [mehr dazu](../../api/using/get-started-apis.md)

Marketing-Funktionen für Transaktionsnachrichten – [mehr dazu](../../channels/using/editing-transactional-message.md#profile-transactional-message-specificities)

**Weitere Aktualisierungen der Dokumentation zu dieser Version**

Workflow-Aktivität Inkrementelle Abfrage: neuer inkrementeller Modus – [mehr dazu](../../automating/using/incremental-query.md)

Aktivitäts-Update für Planungs-Workflow – [mehr dazu](../../automating/using/scheduler.md)

URL-Änderung: Assets Core Service – [mehr dazu](../../integrating/using/working-with-campaign-and-assets-core-service.md)

URL-Änderung: People Core Service – [mehr dazu](../../integrating/using/about-campaign-audience-manager-or-people-core-service-integration.md)

Das Handbuch zu Profilen und Audiences wurde umstrukturiert – [Weitere Informationen](../../audiences/using/get-started-profiles-and-audiences.md)

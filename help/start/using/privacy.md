---
title: Datenschutz und Zustimmung in Adobe Campaign Standard
description: In diesem Abschnitt erhalten Sie einen Überblick über den Datenschutz, die personenbezogenen Daten und die Verwaltung der Einwilligung in Adobe Campaign Standard sowie die dazu verfügbaren Tools.
page-status-flag: never-activated
uuid: ed9e631c-5ad1-49f1-be1e-b710bc64dc91
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: discovering-the-interface
discoiquuid: 5227ca05-3856-4e54-aec6-14444d6534e3
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: faddcc870adcf9e71e50004a69a219b16ddc044f

---


# Privacy and Consent{#privacy-and-consent}

## Allgemeine Empfehlungen {#general-recommendations}

Adobe Campaign ist ein leistungsstarkes Instrument zur Erfassung und Verarbeitung sehr großer Datenmengen, einschließlich personenbezogener Daten und sensibler Daten. Deshalb muss die Privatsphäre sorgfältig verwaltet werden.

* Gehen Sie stets verantwortungsbewusst und ethisch vor, um persönliche Daten zu nutzen.

* Senden Sie keine unerwünschten E-Mails, Push-Benachrichtigungen und SMS-Nachrichten (&quot;Spam&quot;). Adobe ist fest davon überzeugt, dass Permission Marketing den Lebensdauerwert und die Kundenloyalität fördert. Daher verbietet Adobe die Verwendung von Adobe Campaign zum Senden unerwünschter Nachrichten strikt.

### Datenschutzbestimmungen {#privacy-regulations}

Arbeiten Sie zur korrekten Handhabung der Privatsphäre und Verwaltung personenbezogener Daten innerhalb der Rechtsvorschriften, die für die Region/die Regionen gelten, in der/denen Sie tätig sind. Zu diesen Verordnungen gehören:
* [GDPR](https://ec.europa.eu/info/law/law-topic/data-protection/reform/what-does-general-data-protection-regulation-gdpr-govern_en) (Europäische Datenschutzverordnung)
* [DPA](https://www.gov.uk/data-protection) (Umsetzung des GDPR durch das Vereinigte Königreich)
* [Europäische Richtlinie über den Schutz der Privatsphäre und die elektronische Kommunikation](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:02002L0058-20091219)
* [CAN-SPAM Act](https://www.ftc.gov/tips-advice/business-center/guidance/can-spam-act-compliance-guide-business) (US-Gesetz zur Festlegung der Regeln und Anforderungen für kommerzielle E-Mails)
* [CCPA](https://leginfo.legislature.ca.gov/faces/codes_displayText.xhtml?lawCode=CIV&amp;division=3.&amp;title=1.81.5.&amp;part=4.&amp;chapter=&amp;article=) (California Consumer Privacy Act)
* [PDPA](https://secureprivacy.ai/thailand-pdpa-summary-what-businesses-need-to-know/) (Thailand Personal Data Protection Act)

>[!NOTE]
>
>Weitere Informationen zur Anwendung von GDPR, CCPA und PDPA auf Adobe Campaign finden Sie auf [dieser Seite](https://helpx.adobe.com/campaign/kb/campaign-privacy-overview.html#whatisgdpr).

### Adobe Experience Cloud privacy {#experience-cloud-privacy}

Adobe Campaign ist Teil der Adobe Experience Cloud-Lösungen. Die Art und Weise, wie der Datenschutz in der Kampagne behandelt wird, befolgt die allgemeinen Grundsätze der Adobe Experience Cloud, z. B.:

* **Welche Informationen werden bei Verwendung von Adobe Experience Cloud erfasst?**

   Als Firma mit Adobe Experience Cloud-Lösungen wählen Sie aus, welche Informationen erfasst und an Ihr Adobe Experience Cloud-Konto gesendet werden sollen. Beispiele für Informationen, die gesammelt werden können, sind die Aktivität zum Browsen im Internet, IP-Adressen, Standortinformationen von Mobilgeräten, Erfolgsraten von Kampagnen, gekaufte oder in den Einkaufswagen gelegte Artikel usw.

   >[!NOTE]
   >
   >Wie bei allen Adobe-Produkten erfasst Kampagne Informationen über App- und Website-Benutzer. Weitere Informationen finden Sie in den [Adobe-Datenschutzrichtlinien](https://www.adobe.com/privacy/policy.html).

* **Verwendung von Adobe Experience Cloud zur Informationserfassung**

   * Adobe Experience Cloud-Lösungen verwenden Cookies und ähnliche Technologien, wie Web-Beacons (auch als Tags oder Pixel bezeichnet), um die Erfassung von Informationen zu ermöglichen. Weitere Informationen zu Cookies und Verfolgungsfunktionen mit Adobe Campaign finden Sie in [diesem Abschnitt](#tracking-capabilities).
   * Sie können Adobe Experience Cloud-Technologien auch in Ihren mobilen Apps verwenden. Weitere Informationen zum Senden von mobilen Versänden mit Kampagne finden Sie auf [dieser Seite](https://helpx.adobe.com/de/campaign/kb/acs-mobile.html).

* **Datenschutzeinstellungen der Benutzer für Ihre Verwendung von Adobe Experience Cloud**

   Adobe fordert Sie auf, die Datenschutzrichtlinien Ihrer Kunden anzugeben, die Folgendes beschreiben:

   * Ihre Datenschutzpraktiken in Verbindung mit Adobe Experience Cloud
   * Wie Benutzer ihre Voreinstellungen für die Erfassung oder Verwendung ihrer Informationen in Verbindung mit Adobe Experience Cloud festlegen können
   >[!NOTE]
   >
   >Wie bei allen Adobe-Produkten können Kampagnen die Freigabe von Informationen, die über Apps und Websites erfasst wurden, deaktivieren. Weitere Informationen finden Sie in den häufig gestellten Fragen zu [Adobe Experience Cloud-Nutzungsinformationen](https://www.adobe.com/privacy/experience-cloud-usage-info-faq.html).

Weitere Informationen zum Datenschutz in der Adobe Experience Cloud finden Sie auf [dieser Seite](https://www.adobe.com/de/privacy/marketing-cloud.html).

## Persönliche Daten und Personen {#personal-data}

Bei der Verwaltung der Privatsphäre ist es wichtig zu definieren, welche Daten mit Sorgfalt verarbeitet werden und von wem.
* **Personenbezogene Daten** sind Informationen, die eine lebende Person direkt oder indirekt identifizieren können.
* **Sensible personenbezogene Daten** sind Informationen über die Rasse, politische Ansichten, religiöse Überzeugungen, kriminellen Hintergrund, genetische Informationen, Gesundheitsdaten, sexuelle Präferenz, biometrische Informationen sowie die Mitgliedschaft in der Vereinigung.

Die [wichtigsten Rechtsvorschriften](#privacy-regulations) beziehen sich auf die verschiedenen Stellen, die Daten wie folgt verwalten:
* Ein **für die Verarbeitung Verantwortlicher** ist die Behörde, die die Mittel und den Zweck der Erhebung, Nutzung und Weitergabe personenbezogener Daten bestimmt.
* Ein **Datenprozessor** ist eine natürliche oder juristische Person, die personenbezogene Daten gemäß den Anweisungen des für die Verarbeitung Verantwortlichen sammelt, verwendet oder weitergibt.
* Eine **betroffene** Person ist eine lebende Person, deren personenbezogene Daten erhoben, verwendet oder weitergegeben werden und die direkt oder indirekt anhand dieser personenbezogenen Daten identifiziert werden kann.

Als Firma zum Sammeln und Freigeben von personenbezogenen Daten sind Sie der Datenverantwortliche, Ihre Kunden sind die Datensubjekte und Adobe Campaign fungiert als Datenverarbeiter bei der Verarbeitung ihrer personenbezogenen Daten, wie von Ihnen angegeben. Beachten Sie, dass es Ihre Verantwortung als Data Controller ist, die Beziehung zu den Datensubjekten zu bearbeiten, z. B. bei der Verwaltung von [Datenschutzanforderungen](#privacy-requests).

Bei der Integration von Kampagne mit anderen Experience Cloud-Lösungen, bei denen Audiencen von einem System auf ein anderes übertragen werden können, wie z. B. der [Audience Destination Service](../../audiences/using/aep-about-audience-destinations-service.md), [Adobe Analytics](../../integrating/using/about-campaign-analytics-integration.md), [Audience Manager oder People Core Service](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md)oder mit anderen Lösungen wie [Microsoft Dynamics 365](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md), müssen Sie dem Schutz personenbezogener Daten besondere Aufmerksamkeit widmen.

## Datenakquise {#data-acquisition}

Mit Adobe Campaign können Sie Daten, einschließlich persönlicher und sensibler Daten, erfassen. Daher ist es wichtig, dass Sie die Zustimmung Ihrer Empfänger erhalten und überwachen.

* Lassen Sie Empfänger immer dem Empfang von Nachrichten zustimmen. Um dies zu erreichen, sollten Sie so schnell wie möglich die Ausstiegsanträge berücksichtigen und die Einwilligung im Rahmen eines Dublette-Opt-in-Verfahrens überprüfen. Weitere Informationen hierzu finden Sie unter [Verwalten der Teilnahme und Abmeldung in der Kampagne](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md) und [Einrichten einer Dublette-Teilnahme](../../channels/using/setting-up-a-double-opt-in-process.md).
* Importieren Sie keine betrügerischen Listen und verwenden Sie Traps, um sicherzustellen, dass Ihre Clientdatei nicht betrügerisch verwendet wird. Weitere Informationen hierzu finden Sie unter [Verwenden von Fallen](../../sending/using/using-traps.md).
* Mithilfe der Einwilligung und der Rechteverwaltung können Sie die Präferenzen Ihrer Empfänger nachverfolgen und verwalten, wer in Ihrem Unternehmen auf welche Daten zugreifen kann. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](#consent).
* Erleichtern und verwalten Sie Datenschutzanfragen Ihrer Empfänger. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](#privacy-requests).

## Datenschutzverwaltung {#privacy-management}

Das Datenschutzmanagement bezieht sich auf alle Prozesse und Tools, die Ihnen bei der Einhaltung der Datenschutzbestimmungen helfen können (GDPR, CCPA usw.). Verschaffen Sie sich einen Überblick über die Datenschutzverwaltung auf [dieser Seite](https://helpx.adobe.com/de/campaign/kb/campaign-privacy-overview.html).

Adobe Campaign bietet Ihnen verschiedene Funktionen zur Datenschutzverwaltung:
* Verwaltung der Zustimmung, Datenaufbewahrung und Benutzerrollen. Siehe [diesen Abschnitt](#consent).
* Datenschutzanforderungen (Zugriffsrecht und Recht auf Vergessen). Siehe [diesen Abschnitt](#privacy-requests).
* Ausschluss für den Verkauf von persönlichen Informationen (CCPA-spezifisch). Siehe [diesen Abschnitt](https://helpx.adobe.com/de/campaign/kb/acs-privacy.html#ccpa).

Die wichtigsten Datenschutzfunktionen in der Kampagne und ein Beispiel der beteiligten Personen werden in [diesem Abschnitt](https://helpx.adobe.com/campaign/kb/campaign-privacy-more.html#gdprpersonasandflow)dargestellt.


### Einverständnis, Datenbeibehaltung und Benutzerrollen {#consent}

Ursprünglich wurden in Adobe Campaign wichtige Funktionen Angebot, die für die Privatsphäre von wesentlicher Bedeutung sind:

* **Verwaltung** der Zustimmung: Mithilfe des Abonnement-Management-Prozesses können Sie die Voreinstellungen Ihrer Empfänger verwalten und nachverfolgen, welche Empfänger sich für welche Abonnement entschieden haben. Weitere Informationen finden Sie unter [Abonnements](../../audiences/using/about-subscriptions.md) und [Landingpages](../../channels/using/getting-started-with-landing-pages.md).
* **Datenspeicherung**: Alle integrierten Standard-Protokolltabellen haben voreingestellte Aufbewahrungszeiträume, wodurch ihre Datenspeicherung in der Regel auf maximal 6 Monate begrenzt wird. Mit Workflows können weitere Aufbewahrungszeiträume eingerichtet werden. Wenden Sie sich für weitere Informationen an die Adobe-Berater oder technischen Administratoren.
* **Rights Management**: Adobe Campaign bietet Ihnen die Möglichkeit, die den verschiedenen Operatoren der Kampagne zugewiesenen Rechte über verschiedene vordefinierte oder benutzerdefinierte Rollen zu verwalten. Auf diese Weise können Sie verwalten, wer in Ihrer Firma auf verschiedene Datentypen zugreifen, sie ändern oder exportieren kann. For more on this, see [About access management](../../administration/using/about-access-management.md).

Weitere Informationen zu diesen Funktionen und deren Verwaltung in Adobe Campaign finden Sie auf [dieser Seite](https://helpx.adobe.com/campaign/kb/campaign-privacy-overview.html#consent).

### Privacy requests {#privacy-requests}

Adobe Campaign bietet zusätzliche Funktionen, mit denen Sie Ihre Bereitschaft als Data Controller für bestimmte Datenschutzanforderungen erleichtern können:

* Das **Recht auf Zugang** ist das Recht der betroffenen Person, von der für die Verarbeitung Verantwortlichen eine Bestätigung darüber zu erhalten, ob und warum sie betreffende personenbezogene Daten verarbeitet werden.

* Das **Recht auf Vergessenwerden** (Löschungsanfrage) berechtigt den Datenverantwortlichen, seine persönlichen Daten zu löschen.

>[!NOTE]
>
>Diese Tools helfen Ihnen bei der Einhaltung Ihrer Datenschutzbestimmungen für GDPR, CCPA und PDPA. Weitere Informationen zu diesen verschiedenen Vorschriften finden Sie auf [dieser Seite](https://helpx.adobe.com/campaign/kb/campaign-privacy-overview.html#whatisgdpr).

<!--* **GDPR** (General Data Protection Regulation) is the European Union’s (EU) privacy law that harmonizes and modernizes data protection requirements. GDPR applies to Adobe Campaign customers who hold data for Data Subjects residing in the EU.

* **CCPA** (California Consumer Privacy Act) provides California residents new rights in regards to their personal information and imposes data protection responsibilities on certain entities whom conduct business in California.

* **Thailand's PDPA** (Personal Data Protection Act) is the new privacy law that harmonizes and modernizes data protection requirements for Thailand. This regulation applies to Adobe Campaign customers who hold data for Data Subjects residing in this country.-->

Die **Anforderungen für Zugriff** und **Löschen** werden auf [dieser Seite](https://helpx.adobe.com/campaign/kb/acs-privacy.html#righttoaccess)angezeigt. Die Implementierungsschritte zum Erstellen dieser Anforderungen sind auf [dieser Seite](https://helpx.adobe.com/de/campaign/kb/acs-privacy.html#ManagingPrivacyRequests)beschrieben. Übungen sind auch [hier](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/privacy/privacy-overview.html)verfügbar.

## Verfolgungsfunktionen {#tracking-capabilities}

Dank der Tracking-Funktionen ermöglicht Ihnen Adobe Campaign die Verfolgung des Verhaltens Ihrer Versand-Empfänger mithilfe von Sitzungs-Cookies und dauerhaften Cookies. For more on tracking, see [this page](../../sending/using/tracking-messages.md).

>[!NOTE]
>
>Vorschriften wie die Allgemeine Datenschutzverordnung (GDPR) sehen vor, dass Firmen die Zustimmung der Benutzer der Website erfordern, bevor sie Cookies installieren. Sie müssen die Benutzer über eine Autorisierungsanfrage darüber informieren, dass Ihre Sites mit Web-Verfolgungswerkzeugen ausgestattet sind.

Sie können auch [verfolgte Links](../../designing/using/links.md#about-tracked-urls) in Ihren Nachrichten hinzufügen, um die Auswirkungen Ihres Versands- und Empfänger-Verhaltens im integrierten Bericht zu [Trackingindikatoren](../../reporting/using/tracking-indicators.md) zu messen, oder eigene [dedizierte Berichte](../../reporting/using/about-dynamic-reports.md)erstellen.

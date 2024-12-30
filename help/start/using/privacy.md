---
title: Datenschutz und Einverständniserklärung in Adobe Campaign Standard
description: In diesem Abschnitt erhalten Sie einen Überblick über den Datenschutz, die personenbezogenen Daten und die Einverständnisverwaltung in Adobe Campaign Standard sowie über die dazu verfügbaren Instrumente.
page-status-flag: never-activated
uuid: ed9e631c-5ad1-49f1-be1e-b710bc64dc91
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: discovering-the-interface
discoiquuid: 5227ca05-3856-4e54-aec6-14444d6534e3
feature: Privacy
role: User
level: Intermediate
exl-id: 0fc71c2f-f294-43f7-825c-73ab4d43fcf7
source-git-commit: 6b683ccd93e10f78ff643eed9f374a794c085cb1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Datenschutz und Einverständniserklärung{#privacy-and-consent}

## Allgemeine Empfehlungen {#general-recommendations}

Adobe Campaign ist ein leistungsstarkes Tool zur Erfassung und Verarbeitung sehr großer Datenmengen, einschließlich personenbezogener Daten und vertraulicher Informationen. Aus diesem Grund muss der Datenschutz sorgfältig gehandhabt werden.

* Gehen Sie stets verantwortungsvoll und ethisch korrekt mit personenbezogenen Informationen um.

* Senden Sie keine unerwünschten E-Mails, Push-Benachrichtigungen und SMS-Nachrichten (&quot;Spam&quot;). Adobe glaubt fest an Permission Marketing, um den Kundenlebenszeitwert und die Treue zu fördern, und verbietet daher strikt die Verwendung von Adobe Campaign zum Versenden von unerbetenen Nachrichten.

### Datenschutzbestimmungen {#privacy-regulations}

Um den Datenschutz korrekt zu handhaben und personenbezogene Daten korrekt zu verwalten, müssen Sie die für die Region(en) geltenden Gesetze einhalten, in denen Sie tätig sind. Zu diesen Verordnungen gehören:
* [DSGVO](https://ec.europa.eu/info/law/law-topic/data-protection/reform/what-does-general-data-protection-regulation-gdpr-govern_de) (Europäische Datenschutz-Grundverordnung)
* [DPA](https://www.gov.uk/data-protection) (Umsetzung der DSGVO durch das Vereinigte Königreich)
* [Europäische Richtlinie über Datenschutz und elektronische Kommunikation](https://eur-lex.europa.eu/legal-content/DE/TXT/?uri=CELEX:02002L0058-20091219)
* [CAN-SPAM Act](https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business) (US-Gesetz zur Festlegung der Regeln und Anforderungen für kommerzielle E-Mails)
* [CCPA](https://leginfo.legislature.ca.gov/faces/codes_displayText.xhtml?lawCode=CIV&amp;division=3.&amp;title=1.81.5.&amp;part=4.&amp;chapter=&amp;article=) (kalifornisches Verbraucherschutzgesetz)
* [PDPA](https://secureprivacy.ai/thailand-pdpa-summary-what-businesses-need-to-know/) (thailändisches Gesetz zum Schutz personenbezogener Daten)

>[!NOTE]
>
>Weitere Informationen zur Anwendung von DSGVO, CCPA und PDPA auf Adobe Campaign finden Sie auf [dieser Seite](../../start/using/privacy-management.md#privacy-management-regulations).

### Adobe Experience Cloud – Datenschutz {#experience-cloud-privacy}

Adobe Campaign ist Teil der Adobe Experience Cloud-Lösungen. Die Art und Weise, wie der Datenschutz in Campaign gehandhabt wird, entspricht den allgemeinen Grundsätzen von Adobe Experience Cloud, z. B.:

* **Welche Informationen werden bei Verwendung von Adobe Experience Cloud erfasst?**

  Als Unternehmen, das Adobe Experience Cloud-Lösungen nutzt, entscheiden Sie selbst, welche Informationen erfasst und an Ihr Adobe Experience Cloud-Konto gesendet werden sollen. Beispiele für die Arten von Informationen, die erfasst werden können, sind Webbrowsing-Aktivitäten, IP-Adressen, Standortinformationen von Mobilgeräten, Erfolgsquoten von Kampagnen, gekaufte oder in den Warenkorb gelegte Artikel usw.

  >[!NOTE]
  >
  >Wie bei allen Produkten von Adobe erfasst Campaign Informationen über App- und Website-Benutzer. Weitere Informationen finden Sie in der [Datenschutzerklärung von Adobe](https://www.adobe.com/de/privacy/policy.html).

* **Verwendung von Adobe Experience Cloud zur Erfassung von Informationen**

   * Adobe Experience Cloud-Lösungen verwenden Cookies und ähnliche Technologien, wie Webbeacons (auch als Tags oder Pixel bezeichnet), um die Erfassung von Informationen zu ermöglichen. Weitere Informationen zu Cookies und Tracking-Funktionen mit Adobe Campaign finden Sie in [diesem Abschnitt](#tracking-capabilities).
   * Sie können Adobe Experience Cloud-Technologien auch in Ihren mobilen Apps verwenden. Weitere Informationen zum Versand an Mobilgeräte finden Sie auf [dieser Seite](../../channels/using/mobile-guide.md).

* **Datenschutzoptionen Ihrer Benutzer bezüglich Ihrer Verwendung von Adobe Experience Cloud**

  Adobe fordert Sie auf, Ihren Kunden Datenschutzrichtlinien bereitzustellen, in denen Folgendes beschrieben wird:

   * Ihre Datenschutzpraktiken in Verbindung mit Adobe Experience Cloud
   * Die Art und Weise, auf die Benutzer ihre Voreinstellungen für die Erfassung oder Verwendung ihrer Informationen in Verbindung mit Adobe Experience Cloud festlegen können

  >[!NOTE]
  >
  >Wie bei allen Produkten von Adobe können Campaign-Benutzer die Weitergabe von Informationen, die über Apps und Websites erfasst wurden, deaktivieren. Weitere Informationen finden Sie in den [häufig gestellten Fragen zu den Adobe Experience Cloud-Nutzungsinformationen](https://www.adobe.com/de/privacy/experience-cloud-usage-info-faq.html).

Weitere Informationen zum Datenschutz in Adobe Experience Cloud finden Sie auf [dieser Seite](https://www.adobe.com/de/privacy/marketing-cloud.html).

## Personenbezogene Daten und Personas {#personal-data}

Bei der Verwaltung des Datenschutzes ist es wichtig zu definieren, welche Daten von wem mit Sorgfalt behandelt werden sollen.
* **Personenbezogene Daten** sind Informationen, die eine lebende Person direkt oder indirekt identifizieren können.
* **Vertrauliche personenbezogene Daten** sind Informationen zu Rasse, politischen Ansichten, religiösen Überzeugungen, kriminellem Hintergrund, genetischen Informationen, Gesundheitsdaten, sexuellen Vorlieben, biometrischen Informationen sowie zur Gewerkschaftsmitgliedschaft.

Die [wichtigsten Rechtsvorschriften](#privacy-regulations) beziehen sich auf die verschiedenen Einheiten, die Daten wie folgt verwalten:
* Ein **Datenverantwortlicher** ist die Autorität, die die Mittel und den Zweck der Erfassung, Verwendung und Weitergabe personenbezogener Daten festlegt.
* Ein **Auftragsverarbeiter** ist eine natürliche oder juristische Person, die personenbezogene Daten gemäß den Anweisungen des Datenverantwortlichen erfasst, verwendet oder weitergibt.
* Eine **betroffene Person** ist eine lebende Person, deren personenbezogene Daten erfasst, verwendet oder weitergegeben werden und die direkt oder indirekt anhand dieser personenbezogenen Daten identifiziert werden kann.

Als Unternehmen, das personenbezogene Daten erfasst und weitergibt, sind Sie daher der Datenverantwortliche, Ihre Kunden sind die betroffenen Personen und Adobe Campaign fungiert als Auftragsverarbeiter, wenn wir deren personenbezogene Daten gemäß Ihren Anweisungen verarbeiten. Beachten Sie, dass es in Ihrer Verantwortung als Datenverantwortlicher liegt, die Beziehung zu den betroffenen Personen zu verwalten, z. B. bei der Verwaltung von [Datenschutzanfragen](#privacy-requests).

Bei der Integration von Campaign mit anderen Experience Cloud-Lösungen, bei denen Zielgruppen von einem System in ein anderes übertragen werden können, wie [Adobe Analytics](../../integrating/using/about-campaign-analytics-integration.md), [Audience Manager oder People Core Service](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md), oder mit anderen Lösungen wie [Microsoft Dynamics 365](../../integrating/using/d365-acs-get-started.md), müssen Sie dem Schutz personenbezogener Daten besondere Aufmerksamkeit schenken.

## Datenakquise {#data-acquisition}

Mit Adobe Campaign können Sie Daten, einschließlich personenbezogener und vertraulicher Daten, erfassen. Es ist daher unerlässlich, dass Sie das Einverständnis Ihrer Empfänger erhalten und überwachen.

* Fordern Sie die Empfänger immer auf, dem Empfang von Nachrichten zuzustimmen. Dazu müssen Sie Opt-out-Anfragen so schnell wie möglich erfüllen und das Einverständnis durch einen Anmeldeprozess mit zweifacher Bestätigung überprüfen. Weitere Informationen hierzu finden Sie unter [Opt-in- und Opt-out-Verfahren in Campaign](../../audiences/using/managing-opt-in-and-opt-out-in-campaign.md) und unter [Anmeldung mit zweifacher Bestätigung einrichten](../../channels/using/setting-up-a-double-opt-in-process.md).
* Importieren Sie keine betrügerischen Listen und verwenden Sie Fallen, um zu überprüfen, ob Ihre Kundendatei nicht betrügerisch verwendet wird. Weitere Informationen hierzu finden Sie unter [Fallen verwenden](../../sending/using/using-traps.md).
* Mithilfe von Einverständnisverwaltung und Berechtigungs-Management können Sie die Voreinstellungen Ihrer Empfänger erfassen und verwalten, wer in Ihrem Unternehmen auf welche Daten zugreifen kann. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](#consent).
* Erleichtern und verwalten Sie Datenschutzanfragen von Ihren Empfängern. Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](#privacy-requests).

## Datenschutzverwaltung {#privacy-management}

Die Datenschutzverwaltung bezieht sich auf alle Prozesse und Tools, mit denen Sie die Datenschutzbestimmungen (DSGVO, CCPA usw.) einhalten können. Verschaffen Sie sich auf [dieser Seite](../../start/using/privacy-management.md#privacy-management-regulations) einen Überblick über die Datenschutzverwaltung.

Adobe Campaign bietet Ihnen verschiedene Funktionen zur Datenschutzverwaltung:
* Einverständnisverwaltung, Datenbeibehaltung und Benutzerrollen. Siehe [diesen Abschnitt](#consent).
* Datenschutzanfragen (Recht auf Zugriff und Recht auf Vergessenwerden). Siehe [diesen Abschnitt](#privacy-requests).
* Abmeldung (Opt-out) vom Verkauf von personenbezogenen Daten (CCPA-spezifisch). Siehe [diesen Abschnitt](../../start/using/privacy-requests.md#sale-of-personal-information-ccpa).

Die wichtigsten Datenschutzfunktionen in Campaign und ein Beispiel der beteiligten Rollen werden in [diesem Abschnitt](#personal-data) dargestellt.


### Einverständnis, Datenbeibehaltung und Benutzerrollen {#consent}

Zunächst bietet Adobe Campaign wichtige Funktionen, die für den Datenschutz unerlässlich sind:

* **Einverständnisverwaltung**: Mithilfe der Abonnementverwaltung können Sie die Voreinstellungen Ihrer Empfänger verwalten und erfassen, welche Empfänger sich für welche Art von Abonnements entschieden haben. Weitere Informationen finden Sie unter [Abonnements](../../audiences/using/about-subscriptions.md) und [Landingpages](../../channels/using/getting-started-with-landing-pages.md).
* **Datenbeibehaltung**: Alle integrierten standardmäßigen Protokolltabellen in Campaign verfügen über eine vordefinierte Beibehaltungsdauer, die üblicherweise auf maximal sechs Monate begrenzt ist. Mit Workflows können weitere Beibehaltungszeiträume eingerichtet werden. Weitere Informationen hierzu erhalten Sie von den Adobe-Beratern oder technischen Administratoren.
* **Berechtigungs-Management**: Adobe Campaign bietet Ihnen die Möglichkeit, die den unterschiedlichen Campaign-Benutzern zugewiesenen Rechte mithilfe von vordefinierten oder benutzerdefinierten spezifischen Rollen zu verwalten. Damit können Sie festlegen, wer in Ihrem Unternehmen auf unterschiedliche Arten von Daten zugreifen, diese ändern und exportieren kann. Weitere Informationen hierzu finden Sie unter [Über die Zugriffsverwaltung](../../administration/using/about-access-management.md).

Weitere Informationen zu diesen Funktionen und deren Verwaltung in Adobe Campaign finden Sie auf [dieser Seite](../../start/using/privacy-management.md#consent-retention-roles).

### Datenschutzanfragen {#privacy-requests}

Adobe Campaign bietet zusätzliche Funktionen, mit denen Sie sich als Datenverantwortlicher auf bestimmte Datenschutzanfragen vorbereiten können:

* Das **Recht auf Zugriff** ist das Recht der betroffenen Person, vom Datenverantwortlichen eine Auskunft darüber zu erhalten, ob und warum personenbezogene Daten über sie verarbeitet werden oder nicht.

* Das **Recht auf Vergessenwerden** (Löschanfrage) berechtigt die betroffene Person dazu, vom Datenverantwortlichen die Löschung ihrer personenbezogenen Daten zu verlangen.

>[!NOTE]
>
>Diese Tools helfen Ihnen bei der Einhaltung der Datenschutzbestimmungen von DSGVO, CCPA und PDPA. Weitere Informationen zu diesen Vorschriften finden Sie auf [dieser Seite](../../start/using/privacy-management.md#privacy-management-regulations).

**Zugriffs**- und **Löschanfragen** werden auf [dieser Seite](../../start/using/privacy-management.md#right-access-forgotten) erläutert. Die Implementierungsschritte zum Erstellen dieser Anfragen werden auf [dieser Seite](../../start/using/privacy-requests.md#about-privacy-requests) beschrieben. [Tutorials sind](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/privacy/privacy-overview.html?lang=de) ebenfalls verfügbar.

## Tracking-Funktionen {#tracking-capabilities}

Über Tracking-Funktionen ermöglicht Adobe Campaign mittels Sitzungs- und permanenten Cookies die Verfolgung des Verhaltens von Versandempfängern. Weiterführende Informationen zum Tracking finden Sie in [diesem Abschnitt](../../sending/using/tracking-messages.md).

>[!NOTE]
>
>Vorschriften, wie die EU-Datenschutz-Grundverordnung (DSGVO), besagen, dass Unternehmen die Zustimmung der Website-Benutzer benötigen, bevor sie Cookies installieren. Sie müssen Benutzer über eine Autorisierungsanfrage darüber informieren, dass Ihre Websites mit Webtrackingtools ausgestattet sind.

Sie können Ihren Nachrichten auch [getrackte Links](../../designing/using/links.md#about-tracked-urls) hinzufügen, um die Auswirkungen Ihres Versands und das Verhalten der Empfänger im integrierten Bericht [Trackingindikatoren](../../reporting/using/tracking-indicators.md) zu messen, oder Ihre eigenen [dedizierten Berichte](../../reporting/using/about-dynamic-reports.md) erstellen.

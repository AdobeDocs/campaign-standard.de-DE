---
solution: Campaign Standard
product: campaign
title: Datenschutzmanagement in Adobe Campaign Standard
description: Erfahren Sie mehr über die Adobe Campaign Standard-Funktionen zur Datenschutzverwaltung.
audience: start
content-type: reference
topic-tags: discovering-the-interface
translation-type: tm+mt
source-git-commit: a9afa91302684ddd37a94a9999d90bf8c8e7abee
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 91%

---


# Datenschutzverwaltung {#privacy-management}

Adobe Campaign offers a set of tools to help you comply with [Privacy regulations](#privacy-management-regulations) (including GDPR, CCPA, PDPA, LGPD).

Im Folgenden finden Sie die fünf wichtigsten Funktionen, die Adobe Campaign bietet, um die Bereitschaft zu GDPR und anderen Datenschutzbestimmungen sicherzustellen:

![](assets/privacy-gdpr-use-cases.png)

* **Zugriffsrecht**

* **Recht auf Löschen**

Weitere Informationen dazu finden Sie unter [Zugriffsrecht und Recht auf Vergessen](#right-access-forgotten).

* **Einverständnisverwaltung**

* **Datenbeibehaltung**

* **Rights Management**

Weitere Informationen finden Sie unter [Zustimmung, Treue und Rollen](#consent-retention-roles).

<!--This section presents general information on what Privacy management is and the features provided by Adobe Campaign to manage the [Right to Access and Right to be Forgotten](#right-access-forgotten).

It also contains information on important features to manage Privacy ([consent, data retention and user roles](#consent-retention-roles)), as well as best practices to help you with your Privacy compliance when using Adobe Campaign.-->

## Regulations on Privacy management {#privacy-management-regulations}

Die Funktionen von Adobe Campaign helfen Ihnen bei der Einhaltung der folgenden Verordnungen:

* Die **DSGVO** ([Datenschutz-Grundverordnung](https://ec.europa.eu/info/law/law-topic/data-protection/reform/what-does-general-data-protection-regulation-gdpr-govern_de)) ist das Datenschutzgesetz der Europäischen Union (EU), in dem die Anforderungen an den Datenschutz in den Ländern der EU harmonisiert und neu geregelt werden. Unter den folgenden Links finden Sie allgemeine Informationen zum GDPR:

   * https://www.adobe.com/de/privacy/general-data-protection-regulation.html
   * https://www.adobe.com/de/marketing-cloud/campaign/general-data-protection-regulation.html

* Der **CCPA** ([California Consumer Privacy Act](https://leginfo.legislature.ca.gov/faces/codes_displayText.xhtml?lawCode=CIV&amp;division=3.&amp;title=1.81.5.&amp;part=4.&amp;chapter=&amp;article=)) gibt in Kalifornien ansässigen Personen neue Rechte in Bezug auf ihre personenbezogenen Daten und verpflichtet bestimmte in Kalifornien tätige Unternehmen zur Einhaltung von Datenschutzvorschriften.
* Der **PDPA** ([Personal Data Protection Act](https://secureprivacy.ai/thailand-pdpa-summary-what-businesses-need-to-know/)) ist das neue Datenschutzgesetz, in dem die Anforderungen an den Datenschutz in Thailand vereinheitlicht und neu geregelt werden.
* Das **LGPD** ([Lei Geral de Proteção de Dados](https://iapp.org/media/pdf/resource_center/Brazilian_General_Data_Protection_Law.pdf)) gilt ab Frühjahr 2021 für alle Firmen, die personenbezogene Daten in Brasilien erheben oder verarbeiten.

Alle diese Verordnungen gelten für Adobe Campaign-Kunden, die Daten für betroffene Personen mit Wohnsitz in den oben genannten Regionen oder Ländern (EU, Kalifornien, Thailand, Brasilien) besitzen.

>[!NOTE]
>
>Weitere Informationen zu personenbezogenen Daten und zu den verschiedenen Entitäten, die Daten verwalten (Datenverantwortlicher, Auftragsverarbeiter und betroffene Person), finden Sie unter [Personenbezogene Daten und Personas](../../start/using/privacy.md#personal-data).

## Recht auf Zugriff und Recht auf Vergessenwerden {#right-access-forgotten}

Um Sie bei der Einhaltung der Datenschutzverordnungen zu unterstützen, ermöglicht Ihnen Adobe Campaign jetzt die Durchführung von **Zugriffs-** und **Löschanfragen**.

* Das **Recht auf Zugriff** ist das Recht der betroffenen Person, vom Datenverantwortlichen eine Auskunft darüber zu erhalten, ob ihre personenbezogenen Daten verarbeitet werden, wo dies geschieht und zu welchem Zweck. Der Datenverantwortliche muss eine Kopie der personenbezogenen Daten kostenlos in elektronischer Form zur Verfügung stellen.

* Das **Recht auf Vergessenwerden** (Löschanfrage), auch Datenlöschung genannt, bedeutet, dass das Datensubjekt vom Datenverantwortlichen verlangen kann, seine personenbezogenen Daten zu löschen, seine Daten nicht weiterzuverbreiten und mögliche Dritte anzuhalten, die Datenverarbeitung einzustellen.

Weitere Informationen zum Erstellen von **Zugriffs-** und **Löschanfragen** und zur Verarbeitung dieser Anfragen durch Adobe Campaign finden Sie in den [Implementierungsschritten](../../start/using/privacy-requests.md#about-privacy-requests).

[Hier](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/privacy/privacy-overview.html?lang=de#privacy) finden Sie auch Tutorials zur Datenschutzverwaltung in Campaign Standard.

>[!NOTE]
>
>Weitere Informationen zu personenbezogenen Daten und zu den verschiedenen Entitäten, die Daten verwalten (Datenverantwortlicher, Auftragsverarbeiter und betroffene Person), finden Sie unter [Personenbezogene Daten und Personas](../../start/using/privacy.md#personal-data).

## Einverständnis, Datenbeibehaltung und Benutzerrollen {#consent-retention-roles}

Zusätzlich zu den neuen Funktionen für das **Recht auf Zugriff** und das **Recht auf Vergessenwerden** bietet Adobe Campaign weitere für den Datenschutz wichtige Funktionen:

* [Einverständnisverwaltung](#consent-management): Abonnement-Funktion für die Verwaltung von Einstellungen
* [Datenbeibehaltung](#data-retention): Fristen für die Datenbeibehaltung für alle Standard-Log-Tabellen; zusätzliche Fristen für die Datenbeibehaltung können mit Workflows eingerichtet werden
* [Berechtigungs-Management](#rights-management): Der Datenzugriff wird über spezifische Berechtigungen verwaltet

### Einverständnisverwaltung {#consent-management}

Einverständnis bedeutet die Zustimmung des Datensubjekts zur Verarbeitung seiner personenbezogenen Daten. Der Datenverantwortliche ist dafür zuständig, das erforderliche Einverständnis für diese Verarbeitung einzuholen. Adobe Campaign stellt zwar Funktionen bereit, die den Kunden bei der Verwaltung der Einverständniserklärungen unterstützen, Adobe ist jedoch nicht für das Einverständnis als solches verantwortlich. Kunden sollten ihre Rechtsabteilung zurate ziehen, um Prozesse und Verfahren für das Einholen des Einverständnisses auszuarbeiten.

Die Funktionen, die bei der Verwaltung bestimmter Aspekte des Einverständnisses helfen, waren bei Adobe Campaign schon immer von zentraler Bedeutung. Im Rahmen der Abonnementverwaltung können Kunden nachverfolgen, welche Empfänger sich für welche Abonnements entschieden haben, ob es sich um Newsletter, tägliche oder wöchentliche Promotions oder andere Marketing-Programme handelt.

![](assets/privacy-consent-management.png)

Weitere Informationen zur Einverständnisverwaltung finden Sie unter [Informationen zu Abonnements](../../audiences/using/about-subscriptions.md) und [Erste Schritte mit Landingpages](../../channels/using/getting-started-with-landing-pages.md).

Zusätzlich zu den von Adobe Campaign bereitgestellten Tools für die Einverständnisverwaltung können Sie verfolgen, ob ein Benutzer dem Verkauf seiner personenbezogenen Daten widersprochen hat. Siehe [diesen Abschnitt](../../start/using/privacy-requests.md#sale-of-personal-information-ccpa).

### Datenbeibehaltung {#data-retention}

Die nativen Log-Tabellen in Campaign verfügen über eine vordefinierte Beibehaltungsdauer, die üblicherweise auf maximal sechs Monate begrenzt ist.

Im Folgenden finden Sie die standardmäßige Beibehaltungsdauer für Standardtabellen. Beachten Sie, dass diese Beibehaltungswerte von den technischen Adobe-Administratoren während der Implementierung festgelegt werden und daher je nach Kundenanforderungen variieren können.

* **Konsolidiertes Tracking**: 6 Monate
* **Versandlogs**: 6 Monate
* **Trackinglogs**: 6 Monate
* **Ereignisse**: 1 Monat
* **Statistiken zur Ereignisverarbeitung**: 6 Monate
* **Ereignisse mit Verlauf**: 6 Monate
* **Vorläufige Entitäten**: 7 Tage
* **Ignorierte Pipeline-Ereignisse**: 1 Monat
* **Versandwarnungen**: 1 Monat
* **Export-Audit**: 6 Monate

Ähnlich wie beim Löschvorgang kann auch mithilfe von Standard-Workflow-Funktionen die Beibehaltungsdauer für benutzerdefinierte Tabellen festgelegt werden.

Wenden Sie sich an einen Adobe-Berater oder technischen Administrator, um mehr über die Beibehaltung zu erfahren oder um festzustellen, ob Sie eine Beibehaltung für benutzerdefinierte Tabellen festlegen müssen.

### Rights Management {#rights-management}

Adobe Campaign bietet Ihnen die Möglichkeit, die den unterschiedlichen Campaign-Benutzern zugewiesenen Rechte mithilfe von vordefinierten oder benutzerdefinierten spezifischen Rollen zu verwalten.

Ein Vorteil ist, dass Sie damit verwalten können, wer in Ihrer Firma auf verschiedene Datentypen zugreifen kann. So können Sie beispielsweise verschiedene Marketing-Experten für verschiedene geografische Gebiete (Geos) verwenden, und jeder Marketing-Experte kann nur auf Daten aus seinem geografischen Gebiet zugreifen.

Diese Funktion ermöglicht es Ihnen außerdem, verschiedene Funktionen für jeden Benutzer zu konfigurieren, z. B. die Einschränkung, wer Sendungen durchführen darf, oder, was für die Datenschutzverwaltung relevanter ist, wer Daten ändern oder exportieren darf.

![](assets/privacy-user-management.png)

Weitere Informationen zur Zugriffsverwaltung finden Sie in [diesem Abschnitt](../../administration/using/about-access-management.md).
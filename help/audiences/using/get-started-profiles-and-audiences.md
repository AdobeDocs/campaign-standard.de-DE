---
title: Erste Schritte mit Profilen und Zielgruppen
description: Definieren Sie Zielgruppen-Populationen, wählen Sie Audiences, filtern Sie Empfänger, erfassen Sie Daten und aktualisieren Sie Profile.
audience: audiences
content-type: reference
topic-tags: about-profiles-and-audiences
feature: Profiles
role: User
level: Beginner
exl-id: b4de2f1a-09ec-486d-b1ef-66208cbe211f
TQID: https://experienceleague.adobe.com/SC-25nzjfan6OmPZny5QnaeheMiHf2OiJXO9SGVimfo
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2:
  - id: a075b2c1-7748-4328-b7f6-343aa314616a
  - id: a658c786-869b-4194-a780-2594d663adda
  - id: afa4204e-6d08-4e29-bc35-26aafb656d48
subfeature_v2:
  - id: af6750fd-3c1b-4ad2-9fe3-99e81510998d
  - id: d6330382-c886-4f7a-a4f7-74e3f36c0d9c
  - id: f5293531-9312-4099-bfa3-9e67df6a8750
  - id: f529d0bd-1401-4c88-9833-43228cc1d40f
  - id: fcb46c0f-76e1-48bc-9dd0-fcf9d97526cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 621
ht-degree: 99%

---

# Erste Schritte mit Profilen und Zielgruppen{#about-profiles-and-audiences}

<table>
<tr>
<td><img src="assets/do-not-localize/icon_segment.svg" width="60px"><p><a href="#segmenting-targeting">Segmentierung und Zielgruppenbestimmung</a></p></td>
<td><img src="assets/do-not-localize/icon_permission.svg" width="60px"><p><a href="#permission">Einverständnis der Benutzer</a></p></td>
<td><img src="assets/do-not-localize/icon_privacy.svg" width="60px"><p><a href="#privacy">Einhaltung von Datenschutzbestimmungen</a></p></td></tr>
</table>

Mit in Campaign integrierten Kundenprofilen können Sie jede Interaktion mit Kunden auf allen Kanälen in einer einzigen Ansicht verfolgen und Ihren Kunden relevante und personalisierte Nachrichten übermitteln.

Segmentieren Sie Ihre Datenbank in Audiences, um die Zielgruppen Ihrer Marketing-Kampagnen zu optimieren.

Verwalten Sie die Berechtigungen und Einverständniserklärungen der Kunden mithilfe von Diensten und Landingpages, um einfache Opt-in- und Opt-out-Mechanismen einzurichten.

## Segmentierung und Targeting {#segmenting-targeting}

<img src="assets/do-not-localize/icon_segment.svg" width="60px">

Bei der Erstellung von Kampagnen oder Nachrichten kann die Versandzielgruppe aus in der Campaign-Datenbank vorhandenen Kontakten nach einfachen oder erweiterten Kriterien oder durch die Auswahl von Audiences zusammengestellt werden.

Mit **integrierten Kundenprofilen**, **benutzerdefinierten Segmenten** und **Kontrollgruppen** können Sie Kunden auf allen Ihren Kanälen effektiver identifizieren. Wenn Sie Ihre Kunden, deren Interessen, demografische Daten und Kanalpräferenzen kennen, ist es einfacher, personalisierte, ansprechende Erlebnisse zu erstellen.

In Adobe Campaign werden umfassende Kundenprofile in Echtzeit erstellt, wodurch Sie relevante und personalisierte Angebote entsprechend den Präferenzen Ihrer Kunden versenden können. Zusätzlich verfügt Adobe Campaign zur Definition von Audiences über erweiterte Funktionen zur Analyse, Datenverwaltung und Zielgruppenbestimmung.

**Profile sind einzelne in der Datenbank gespeicherte Kontakte.** Jedes Profil entspricht einem Datensatz in der Datenbank, welcher alle nötigen Informationen zu seiner Qualifizierung, Verwendung in Zielgruppen und zum Tracking enthält: Adobe Campaign verfolgt alle von Online- und Offline-Kanälen ausgehenden Interaktionen und führt sie zu einem gemeinsamen Profil zusammen.

**Zielgruppen bestehen aus Listen mit Profilen, die nach einem oder mehreren Kriterien zusammengestellt werden.** Workflows und der Abfrage-Editor erlauben die Erstellung von Zielgruppen entsprechend den verfügbaren Informationen, dem Verhalten und dem Marketing-Verlauf Ihrer Kontakte, um Ihre Marketing-Kampagnen perfekt auf die angesprochenen Zielgruppen zuzuschneiden. Sie können beispielsweise angemeldete Profile filtern, Probe-Audiences oder auf einer unbegrenzten Anzahl an Kriterien basierende Zielgruppen erstellen.

mehr dazu:

* [Über Profile](../../audiences/using/about-profiles.md)
* [Aktive Profile](../../audiences/using/active-profiles.md)
* [Verwaltung von Testprofilen](../../audiences/using/managing-test-profiles.md)
* [Anreicherung der Campaign-Datenbank](../../audiences/using/enriching-campaign-database.md)
* [Über Zielgruppen](../../audiences/using/about-audiences.md)
* [Zielgruppe in einer Nachricht auswählen](../../audiences/using/selecting-an-audience-in-a-message.md)
* [Hinzufügen einer Kontrollgruppe](../../sending/using/control-group.md)

## Einverständnis der Benutzer {#permission}

<img src="assets/do-not-localize/icon_permission.svg"  width="60px">

Bevor Sie einem Kontakt Nachrichten senden, müssen Sie sicherstellen, dass Sie sein Einverständnis dazu haben. Andernfalls könnten Ihre E-Mails als Spam gekennzeichnet werden, was Ihre Plattform-Zustellbarkeit beeinträchtigt. Um eine funktionierende Profildatenbank aufzubauen, ist es daher wichtig, sich diese Zustimmung im Vorfeld zu sichern.

Wir empfehlen in Campaign **einfache Anmelde- und Abmeldemöglichkeiten** über [Dienste](../../audiences/using/creating-a-service.md) und [Landingpages](../../channels/using/getting-started-with-landing-pages.md) zu verwenden, um Ihre Kontaktinformationen zu aktualisieren und Ihre Datenbank zu erweitern.

Durch die Bereitstellung von **Abmelde-Links** in Ihren Nachrichten können Profile bei Bedarf auf die Blockierungsliste gesetzt werden, was die Zustellbarkeit Ihrer Plattform verbessert. Weiterführende Informationen zur Verwaltung von Blockierungslisten finden Sie im Abschnitt [Funktionsweise des Opt-in- und Opt-out-Verfahrens in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

>[!IMPORTANT]
>
>Sie müssen die [Adobe Campaign-Nutzungsbedingungen](https://www.adobe.com/de/legal/terms/aup.html) beachten.

mehr dazu:

* [Über Abonnements](../../audiences/using/about-subscriptions.md)
* [Funktionsweise des Opt-in- und Opt-out-Verfahrens in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md)

## Einhaltung von Datenschutzbestimmungen {#privacy}

<img src="assets/do-not-localize/icon_privacy.svg" width="60px">

Adobe Campaign bietet eine Reihe von Tools, die Sie bei der **Einhaltung von Datenschutzbestimmungen** wie DSGVO, CCPA und anderen unterstützen.

In diesem [Artikel](https://helpx.adobe.com/de/campaign/kb/campaign-privacy.html) erfahren Sie mehr über die Datenschutzverwaltung und die Funktionen, die wir zur Verwaltung von Recht auf Zugriff, Recht auf Vergessenwerden, Einwilligung, Datenspeicherung und Benutzerrollen bereitstellen.

Datenschutz und Einverständniserklärung in Campaign und deren Verwaltung werden in [diesem Abschnitt](../../start/using/privacy.md) vorgestellt. Darüber hinaus finden Sie Best Practices, die Ihnen bei der Einhaltung Ihrer Datenschutzbestimmungen helfen, wenn Sie unseren Service nutzen.

## Zusätzliche Ressourcen

* [Adobe Experience Platform-Zielgruppen in Campaign aufnehmen](../../integrating/using/ingest-aep-data.md)
* [Microsoft Dynamics 365 verwenden](../../integrating/using/d365-acs-get-started.md)
* [Für Adobe freigegebene Zielgruppen](../../integrating/using/sharing-audiences-with-audience-manager-or-people-core-service.md)
* [Workflows zum Importieren von Profilen verwenden](../../automating/using/creating-import-workflow-templates.md)
* [Videos zu Profilen und Audiences](https://experienceleague.adobe.com/docs/campaign-standard-learn/tutorials/profiles-and-audiences/creating-profiles-and-audiences.html?lang=de)

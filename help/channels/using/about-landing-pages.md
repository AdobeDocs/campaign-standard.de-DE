---
title: Über Landingpages
description: Hier erfahren Sie über Landingpages bei Campaign und deren Lebenszyklus.
page-status-flag: never-activated
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 00fc2e12669a00c788355ef4e492375957cdad2e

---


# Über Landingpages{#about-landing-pages}

Campaign bietet eine Landingpage-Funktion an. Landingpages sind Webformulare, mit denen Sie Informationen zu Ihren Audiences erfassen, Abonnements für einen Dienst anbieten, Daten darstellen und Ihre Datenbank erweitern können. Landingpages können außerdem zur Akquise oder Aktualisierung bestehender Profile verwendet werden.

Weitere Informationen zu den erforderlichen Schritten zum Einrichten einer Landingpage finden Sie in [diesem Abschnitt](../../channels/using/main-steps-to-set-up-a-landing-page.md).

**Verwandte Themen:**

* [Anleitungsvideo zum Erstellen einer Landingpage](https://helpx.adobe.com/campaign/kt/acs/using/acs-create-edit-landing-page-feature-video-use.html)
* [Über eine Landingpage bei einem Dienst anmelden](../../audiences/using/creating-a-service.md)

## Lebenszyklus von Landingpages{#landing-pages-life-cycle}

Ein vollständiger Landingpage-Lebenszyklus umfasst die folgenden Phasen:

1. Erstellung: Erstellen Sie den Inhalt der Landingpage.
1. Test: Testen Sie die Landingpage mit einem Testprofil.
1. Publikation: Publizieren Sie die Landingpage.
1. Ablauf oder Depublikation: Depublizieren Sie die Landingpage manuell oder warten Sie, bis die Landingpage abgelaufen und nicht mehr verfügbar ist.

![](assets/lp_livecycle.png)

Nach der Erstellung und Publikation einer Landingpage können Sie diese auf einer Webseite zugänglich machen oder einen [direkten Link auf die Landingpage in eine E-Mail einfügen](../../designing/using/links.md#inserting-a-link).

## Einschränkungen bei Landingpages{#landing-page-limitations}

Im folgenden Abschnitt finden Sie die Einschränkungen, die Sie kennen sollten, bevor Sie mit dem Einrichten von Landingpages beginnen.

**Schreiben und Aktualisieren von Daten**

* Landingpages sind auf **[!UICONTROL Profil]** und **[!UICONTROL Abonnement]**-Ressourcen beschränkt. Die Speicherung und Aktualisierung von Datensätzen ist im **[!UICONTROL Profil]** und über die Anmeldung zu/Abmeldung von einem **[!UICONTROL Dienst]** möglich.
Weiterführende Informationen zur Ressourcenkonfiguration finden Sie im Abschnitt [Datenstruktur der Ressource konfigurieren](../../developing/using/configuring-the-resource-s-data-structure.md).

>[!CAUTION]
>
>Die Ansicht oder Aktualisierung von auf einer Landingpage eingegebenen Daten ist über keine andere Ressource als **[!UICONTROL Profil]** und **[!UICONTROL Abonnement]** möglich.

**Vorausfüllen**

* Auf einer Landingpage ist keine automatische Anzeige von Daten möglich. Außerdem können keine Dienste angezeigt werden, für die Profile bereits ein Abonnement besitzen. Weiterführende Informationen zu Diensten finden Sie auf dieser [Seite](../../audiences/using/creating-a-service.md).

* Der Zugriff auf eine Landingpage mit einem vorausgefüllten Formular (Daten werden bereits mit der Seite geladen) kann ausschließlich über eine Adobe Campaign-E-Mail erfolgen. Über eine Seite einer Website ist der Zugriff auf ein derartiges Formular nicht möglich.

**Abstimmung**

* Das Abstimmungsverhalten sieht folgendermaßen aus: Sobald eine Übereinstimmung gefunden wird, endet der Abstimmungsprozess. Dies bedeutet, dass die Abstimmung nur für einen Profildatensatz durchgeführt werden kann und nicht für mehrere Datensätze, falls Duplikate vorhanden sind.

Sie möchten beispielsweise die folgende Akquise-Landingpage an Ihre Profile senden, um Ihre Campaign-Datenbank mit den Mobiltelefonnummern der Profile zu aktualisieren.

![](assets/landing_page_limitation_1.png)

Wenn eines Ihrer Profile auf Ihrer Landingpage neue Daten eingibt, aber bereits ein dupliziertes Profil vorhanden ist, wird das passende Profil mit dem frühesten Erstellungsdatum aktualisiert, da Profile nach ihrem Erstellungsdatum priorisiert werden.

Hier wurde nur das erste Profil aktualisiert, da dessen Eintrag früher erfolgte.

![](assets/landing_page_limitation_2.png)

**Testen von Landingpages**

* Landingpages funktionieren nur mit Profilen, nicht aber mit Testprofilen, weshalb Landingpages nicht im Zuge eines E-Mail-Testversands getestet werden können.

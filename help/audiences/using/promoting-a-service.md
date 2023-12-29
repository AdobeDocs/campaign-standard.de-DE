---
title: Dienst bewerben
description: Mit Adobe Campaign können Sie einen Dienst bewerben und Ihre Kunden über Landingpages, E-Mails oder direkt auf Ihrer Website ansprechen.
audience: audiences
content-type: reference
topic-tags: managing-subscriptions
feature: Audiences
role: User
level: Intermediate
exl-id: c1f8770a-8b25-41db-aa52-828e181a563d
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 78%

---

# Dienst bewerben{#promoting-a-service}

Es gibt verschiedene Möglichkeiten, um Abonnements für einen Dienst anzubieten. Zusätzlich können Sie Ihren Besuchern ermöglichen, ihre Abonnements zu verwalten.

Mit Campaign können Sie einen Dienst folgendermaßen bewerben:

* [Einfügen von Anmelde-Links für und Abmelde-Links von Diensten in E-Mails](../../designing/using/links.md#inserting-a-link)

* [Einfügen von Links auf einer Anmelde- oder Abmelde-Landingpage in E-Mails](../../designing/using/links.md). In diesem Fall muss der Dienst direkt in den Eigenschaften der zugehörigen Landingpages referenziert werden (siehe [Verknüpfen einer Landingpage mit einem Service](../../channels/using/configuring-landing-page.md#linking-a-landing-page-to-a-service)).

  >[!NOTE]
  >
  >Es ist auch wichtig, den Abonnenten die Möglichkeit zu geben, sich abzumelden. Fügen Sie dazu einen Dienst ein <b>Abmelde-Link</b> in der Bestätigungs-E-Mail (definiert in den Diensteigenschaften), die automatisch an die neuen Abonnenten gesendet wird, sowie in zukünftigen Newsletter-E-Mails.

* Durch Einbettung einer An- oder Abmelde-Landingpage in eine Webseite: Die Landingpage-URLs müssen verschlüsselte Parameter wie den zugeordneten Dienst und die Kennung des die Seite aufrufenden Profils enthalten. Diese Kennung kann in den Landingpage-Parametern definiert werden (siehe [Konfigurieren einer Landingpage](../../channels/using/configuring-landing-page.md)).

---
title: Einschränkungen der Einstiegsseite
seo-title: Einschränkungen der Einstiegsseite
description: Einschränkungen der Einstiegsseite
seo-description: Hier erfahren Sie über Landingpages bei Campaign und deren Lebenszyklus.
page-status-flag: nie aktiviert
uuid: b 316 bf 47-7 d 98-46 fa-ab 4 f -67 ff 50 de 8095
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Kanäle
content-type: Referenz
topic-tags: landing-pages
discoiquuid: ca 8 d 1698-6 e 8 a -4 f 5 a-b 17-74 a 152 e 14286
context-tags: Landingpage, Wizard; Landingpage, overview; Landingpage, main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 0b2377a2bfdb8745ec9c3e418d8bed00e18447ff

---


# Landing page limitations{#landing-page-limitations}

**Schreiben und Aktualisieren von Daten**

* Landing pages are limited to **[!UICONTROL Profile]** and **[!UICONTROL Subscription]** resources only. Record can be saved and updated from **[!UICONTROL Profile]** and a subscription/unsubscription to a **[!UICONTROL Service]**.
To learn more on resources configuration, see [Configuring the resource's data structure](../../developing/using/configuring-the-resource-s-data-structure.md).

[!CAUTION]
> A landing page cannot display or update data from any other resource than **[!UICONTROL Profile]** and **[!UICONTROL Subscription]**.

**Vorausladen**

* Die Einstiegsseite kann keine Datensatzliste automatisch anzeigen, es kann keine Dienste aufgelistet werden, die bereits abonnent sind. For more information on services, refer to this [page](../../audiences/using/creating-a-service.md).

* Auf die Einstiegsseite mit einem vorausgefüllten Formular (Daten werden bereits mit der Seite geladen) kann nur über eine Adobe Campaign-E-Email zugegriffen werden. Es ist nicht möglich, auf ein solches Formular von einer Website aus zuzugreifen.

**Abstimmung**

* Das Abstimmungsverhalten lautet: sobald eine Übereinstimmung gefunden wird, wird der Aussöhnungsprozess beendet. Dies bedeutet, dass die Abstimmung nur für einen Profildatensatz durchgeführt werden kann und nicht für mehrere Datensätze, wenn Duplikate vorhanden sind.

Sie möchten beispielsweise die folgende Akquise-Landingpage an Ihre Profile senden, um Ihre Kampagnendatenbank mit den Mobiltelefonnummern Ihrer Profile zu aktualisieren.

![](assets/landing_page_limitation_1.png)

Wenn ein Profil Ihre Landingpage mit neuen Informationen füllt, aber bereits ein dupliziertes Profil aufweist, wird das passende Profil mit dem frühesten Erstellungsdatum aktualisiert, da Profile je nach Erstellungsdatum priorisiert werden.

Hier wurde nur das erste Profil aktualisiert, da es der älteste Eintrag war.

![](assets/landing_page_limitation_2.png)

**Testen der Einstiegsseite**

* Einstiegsseiten funktionieren nur in Profilen und keine Testprofile, das bedeutet, dass Einstiegsseiten nicht als Teil eines E-Mail-Tests getestet werden können.

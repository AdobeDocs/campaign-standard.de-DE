---
title: Landingpage-Vorlagen
description: Hier finden Sie weitere Informationen zu Landingpage-Vorlagen.
page-status-flag: never-activated
uuid: b316bf47-7d98-46fa-ab4f-67ff50de8095
contentOwner: lemaitre
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: landing-pages
discoiquuid: ca8d1698-6e8a-4f5a-b017-74a152e14286
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: efb1f14e0094e200d186423f98bfad65d25cfab2

---


# Über Landingpage-Vorlagen {#landing-page-templates}

Campaign ist mit einer Reihe nativer Landingpage-Vorlagen ausgestattet:

* **[!UICONTROL Acquisition]**: Dies ist die Standardvorlage für Landingpages, mit der Sie Daten in der Kampagnen-Datenbank erfassen und aktualisieren können.
* **[!UICONTROL Subscription]**: Diese Vorlage sollte zum Angebot von Abonnements an einen Dienst verwendet werden.
* **[!UICONTROL Unsubscription]**: Diese Vorlage kann von einer E-Mail an Abonnenten mit einem Dienst verknüpft werden, damit sie diesen Dienst abbestellen können.
* **[!UICONTROL Blacklist]**: Verwenden Sie diese Vorlage, wenn ein Kontakt nicht mehr von Campaign kontaktiert werden möchte. Weiterführende Informationen zum Blacklisting erfahren Sie im Abschnitt [Funktionsweise des Opt-in- und Opt-out-Verfahrens in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

Diese Vorlagen werden bei der Erstellung einer neuen Landingpage standardmäßig vorgeschlagen.

![](assets/lp_creation_1.png)

To access landing page templates, click the Adobe Campaign logo on the upper left corner and select **[!UICONTROL Resources]** > **[!UICONTROL Templates]** > **[!UICONTROL Landing page templates]**.

>[!NOTE]
>
>Adobe empfiehlt, eigene Vorlagen zu erstellen, indem eine integrierte Vorlage dupliziert wird. Manche Parameter können nur in Landingpage-Vorlagen festgelegt und nicht direkt in Landingpages geändert werden.

Bei der Erstellung einer Vorlage wird empfohlen, den Tags ein **&#39;type&#39;**-Attribut beizufügen. Die Interpretation dieser Information durch den Editor hilft dem Benutzer bei der Zuordnung von Datenbankfeldern zu Formularfeldern bei der Konfiguration von Webanwendungen.

Beispiel eines HTML-Codes in einer Vorlage:

```
<input id="email" type="email" name="email"/>
```

Eine offizielle Liste aller möglichen &quot;type&quot;-Attribute ist unter folgender Adresse abrufbar: [https://www.w3schools.com/tags/att_input_type.asp](https://www.w3schools.com/tags/att_input_type.asp)
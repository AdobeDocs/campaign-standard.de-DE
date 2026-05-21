---
title: Landingpage-Vorlagen
description: Hier finden Sie weitere Informationen zu Landingpage-Vorlagen.
audience: channels
content-type: reference
topic-tags: landing-pages
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
feature: Landing Pages
role: User
level: Intermediate
exl-id: 29d1badf-9ce3-470c-9bdc-169586d2e943
TQID: https://experienceleague.adobe.com/vJyIRO33IjK6o3--ekx-Iw9K-GcIZMViLz9wEr-kxY0
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 239
ht-degree: 100%

---

# Über Landingpage-Vorlagen {#landing-page-templates}

Campaign ist mit einer Reihe nativer Landingpage-Vorlagen ausgestattet:

* **[!UICONTROL Akquise]**: Dies ist die Standardvorlage für Landingpages, mit der Sie Daten in der Campaign-Datenbank erfassen und aktualisieren können.
* **[!UICONTROL Anmeldung]**: Mit dieser Vorlage können Sie Abonnements für einen Dienst anbieten.
* **[!UICONTROL Abmeldung]**: Mit dieser Vorlage können Sie eine Verbindung zwischen einer gesendeten E-Mail und Abonnenten eines Dienstes herstellen, sodass sich diese von dem Dienst abmelden können.
* **[!UICONTROL Blockierungsliste]**: Verwenden Sie diese Vorlage, wenn ein Kontakt nicht mehr von Campaign kontaktiert werden möchte. Weiterführende Informationen zur Verwaltung von Blockierungslisten finden Sie im Abschnitt [Funktionsweise des Opt-in- und Opt-out-Verfahrens in Campaign](../../audiences/using/about-opt-in-and-opt-out-in-campaign.md).

Diese Vorlagen werden bei der Erstellung einer neuen Landingpage standardmäßig vorgeschlagen.

![](assets/lp_creation_1.png)

Um auf Landingpage-Vorlagen zuzugreifen, wählen Sie das Adobe Campaign-Logo in der linken oberen Ecke aus und danach **[!UICONTROL Ressourcen]** > **[!UICONTROL Vorlagen]** > **[!UICONTROL Landingpage-Vorlagen]**.

>[!NOTE]
>
>Adobe empfiehlt, eigene Vorlagen durch das Duplizieren nativer Vorlagen zu erstellen. Manche Parameter können nur in Landingpage-Vorlagen festgelegt und nicht direkt in Landingpages geändert werden.

Bei der Erstellung einer Vorlage wird empfohlen, den Tags ein **&#39;type&#39;**-Attribut beizufügen. Die Interpretation dieser Information durch den Editor hilft dem Benutzer bei der Zuordnung von Datenbankfeldern zu Formularfeldern bei der Konfiguration von Webanwendungen.

Beispiel eines HTML-Codes in einer Vorlage:

```
<input id="email" type="email" name="email"/>
```

Eine offizielle Liste aller möglichen &quot;type&quot;-Attribute ist unter folgender Adresse abrufbar: [https://www.w3schools.com/tags/att_input_type.asp](https://www.w3schools.com/tags/att_input_type.asp)

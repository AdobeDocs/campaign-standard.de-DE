---
solution: Campaign Standard
product: campaign
title: Aktive Profile
description: Sie können auf einen eigenen Bericht mit Kundenmetriken zugreifen und aktive Profile in Ihrer Campaign-Datenbank darstellen.
audience: audiences
content-type: reference
topic-tags: managing-profiles
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 100%

---


# Aktive Profile{#active-profiles}

Adobe Campaign erstellt einen Bericht, in dem die Anzahl der aktiven Profile dargestellt wird. Dieser Bericht hat nur informativen Charakter und keine direkte Auswirkung auf die Rechnungsstellung. Nur Administratoren haben Zugriff auf diesen Bericht. Er kann unter **[!UICONTROL Administration > Kundenmetriken abgerufen werden]**.

![](assets/audience_active_profiles1.png)

>[!NOTE]
>
>Wenn Sie auf AWS gehostet werden und Campaign Standard aus Build 10368 verwenden, können Sie die Anzahl der in Ihren Instanzen verwendeten aktiven Profile auch direkt im Control Panel überwachen. Weitere Informationen hierzu finden Sie in der [Control Panel-Dokumentation](https://docs.adobe.com/content/help/de-DE/control-panel/using/performance-monitoring/active-profiles-monitoring.html).
>
>Beachten Sie, dass die Metrik der aktiven Profile nur für **Marketing-Instanzen** verfügbar und relevant ist. Sie ist für Ausführungsinstanzen, d. h. MID (Mid-Sourcing)- und RT (Message Center-/Echtzeit-Messaging)-Instanzen, weder anwendbar noch verfügbar.


Die Profile, die während der Versandvorbereitung ausgeschlossen wurden (Typologieregeln, Quarantänen, Kontrollgruppen), werden nicht berücksichtigt. Ein Profil, das mehrere Sendungen erhalten hat, wird nur einmal gezählt. Am Ende des Berichts finden Sie die Liste der aktiven Profile für jede Zielgruppendimension.

Dieser Bericht wird monatlich durch den technischen Workflow **[!UICONTROL Rechnungsstellung]** erstellt. Er enthält die Anzahl der aktiven Profile, die während der letzten 12 Monate (rollierend) ausgewählt wurden.

Beachten Sie, dass die Profile, die während der Versandvorbereitung ausgeschlossen wurden (Typologieregeln, Quarantänen), nicht berücksichtigt werden. Außerdem wird ein Profil, das mehrere Sendungen erhalten hat, nur einmal gezählt.

![](assets/audience_active_profiles2.png)

Am Ende des Berichts finden Sie die Liste der aktiven Profile, die vom Rechnungsstellungs-Workflow verarbeitet wurden.

* Die Quelle **[!UICONTROL NmsRecipient]** umfasst alle Kunden, die mithilfe von Informationen aus ihrem Campaign Standard-Profil kontaktiert wurden.

* Auf der anderen Seite werden Kunden, die nur unter Verwendung einer bestimmten Information (E-Mail-Adresse, Telefonnummer) ohne Bezug zu ihrem Kampagnen-Profil kontaktiert wurden, der Quelle **[!UICONTROL Anonym]** zugeordnet.

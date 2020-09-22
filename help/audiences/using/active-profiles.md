---
title: Aktive Profile
description: Sie können auf einen eigenen Bericht mit Kundenmetriken zugreifen und aktive Profile in Ihrer Campaign-Datenbank darstellen.
page-status-flag: never-activated
uuid: ee8ac493-c297-49ca-aed4-3976d8a685a4
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-profiles
discoiquuid: e029213f-0b65-41b1-8adf-34fa813b0c70
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1147c4512b1485ae5d927a32970adcd41b540e7
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 43%

---


# Aktive Profile{#active-profiles}

Adobe Campaign erstellt einen Bericht, in dem die Anzahl der aktiven Profile dargestellt wird. Dieser Bericht hat nur informativen Charakter und keine direkte Auswirkung auf die Rechnungsstellung. Nur Administratoren haben Zugriff auf diesen Bericht. Er kann unter **[!UICONTROL Administration > Kundenmetriken abgerufen werden]**.

![](assets/audience_active_profiles1.png)

>[!NOTE]
>
>Wenn Sie auf AWS gehostet werden und Campaign Standard aus Build 10368 verwenden, können Sie die Anzahl der in Ihren Instanzen verwendeten aktiven Profile auch direkt im Control Panel überwachen. Weitere Informationen hierzu finden Sie in der [Control Panel-Dokumentation](https://docs.adobe.com/content/help/de-DE/control-panel/using/performance-monitoring/active-profiles-monitoring.html).
>
>Beachten Sie, dass die Metrik Aktive Profil nur für **Marketinginstanzen** verfügbar und relevant ist. Sie ist weder für Ausführungsinstanzen anwendbar noch verfügbar, d. h. MID (MID)- oder RT (Message Center/Real-time Messaging)-Instanzen.


Die Profil, die bei der Zubereitung des Versands ausgeschlossen wurden (Typologieregeln, Quarantänen, Kontrollgruppen), werden nicht berücksichtigt. Ein Profil, das mehrere Sendungen erhalten hat, wird nur einmal gezählt. Am Ende des Berichts finden Sie die Liste der aktiven Profile für jede Zielgruppendimension.

Dieser Bericht wird monatlich durch den technischen Arbeitsablauf für die **[!UICONTROL Rechnungsstellung]** erstellt. Es enthält die Anzahl der aktiven Profil, die während der letzten 12 Monate als Ziel ausgewählt wurden.

Beachten Sie, dass die Profil, die bei der Vorbereitung des Versands ausgeschlossen wurden (Typologieregeln, Quarantänen), nicht berücksichtigt werden. Darüber hinaus wird ein Profil, das von mehreren Versänden als Ziel ausgewählt wurde, nur einmal gezählt.

![](assets/audience_active_profiles2.png)

Am Ende des Berichts finden Sie die Liste der aktiven Profil, die vom Abrechnungs-Workflow verarbeitet werden:

* Die **[!UICONTROL NmsRecipient]** -Quelle umfasst alle Kunden, die mithilfe von Informationen aus ihrem Campaign Standard-Profil kontaktiert wurden.

* Auf der anderen Seite werden Kunden, die ausschließlich mit einer bestimmten Information (E-Mail-Adresse, Telefonnummer) und ohne Bezug zum Profil ihrer Kampagne angeworben wurden, unter die **[!UICONTROL anonyme]** Quelle fallen.

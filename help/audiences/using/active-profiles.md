---
solution: Campaign Standard
product: campaign
title: Kampagne Aktive Profil
description: Erfahren Sie, wie Sie auf Kundenmetriken und aktive Profil zugreifen können
feature: Profile
role: Business Practitioner
level: Intermediate
exl-id: 22516348-7695-4579-99eb-480e5b723ccc
source-git-commit: d2fcf2ca22bb5fe3632280f922dfed0972f6eb09
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 26%

---

# Kundenmetriken {#customer-metrics}

Funktionsadministratoren der Kampagne können auf den Bericht **[!UICONTROL Kundenmetriken]** von **[!UICONTROL Administration > Kundenmetriken]** zugreifen.

![](assets/audience_active_profiles1.png)

Dieser Bericht zeigt an:

* die Experience Cloud-ID
* die IMS-Organisations-ID
* die Anzahl der **aktiven Profil**
* die Liste der in der Instanz verfügbaren Zielgruppendimensionen

Dieser Bericht wird monatlich durch den technischen Workflow **[!UICONTROL Rechnungsstellung]** erstellt.

## Aktive Profile{#active-profiles}

Gemäß Ihrem Vertrag wird jeder Ihrer Instanzen der Kampagne eine bestimmte Anzahl aktiver Profil bereitgestellt. Bitte beachten Sie Ihre Lizenzvereinbarung hinsichtlich der Anzahl der erworbenen aktiven Profil.

>[!NOTE]
>
>Als Admin-Benutzer können Sie auch direkt über die Systemsteuerung die Anzahl der aktiven Profil überwachen, die auf Ihren Instanzen verwendet werden. Weitere Informationen hierzu finden Sie in der [Control Panel-Dokumentation](https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/active-profiles-monitoring.html?lang=de).


Ein &quot;Profil&quot;ist ein Datensatz mit Informationen, die einen Endkunden, Potenzieller Kunde oder Interessenten repräsentieren. Profil werden als **aktiv** angesehen, wenn sie von einem Versand der Kampagne innerhalb der letzten 12 Monate über einen beliebigen Kanal angesprochen wurden. Die Profil, die bei der Vorbereitung des Versands (z. B. nach Typologieregeln oder Quarantänen) ausgeschlossen wurden, werden nicht berücksichtigt. Ein Profil, das mehrere Sendungen erhalten hat, wird nur einmal gezählt. Dieser Bericht hat nur informativen Charakter und keine direkte Auswirkung auf die Rechnungsstellung.

![](assets/audience_active_profiles2.png)

Am Ende des Berichts finden Sie die Liste der aktiven Profile für jede Zielgruppendimension. Er zeigt die Anzahl der aktiven Profil, die während der letzten 12 Monate als Ziel ausgewählt wurden.

* Die **[!UICONTROL NmsRecipient]**-Quelle enthält alle Profil, die mithilfe von Informationen aus ihrem Campaign Standard-Profil kontaktiert wurden.

* Die Kundenquelle **[!UICONTROL anonym]** zeigt die Anzahl der Profil an, die ausschließlich mit einer bestimmten Information (E-Mail-Adresse, Telefonnummer) als Ziel ausgewählt wurden, ohne dass dabei das Profil der Kampagne im Zusammenhang stand.

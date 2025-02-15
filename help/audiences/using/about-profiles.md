---
title: Über Profile
description: Kontakte werden als Profile in der Campaign-Datenbank gespeichert und während ihres gesamten Lebenszyklus aktualisiert.
audience: audiences
content-type: reference
topic-tags: managing-profiles
context-tags: recipient,overview
feature: Profiles
role: User
level: Beginner
exl-id: 65310e00-567f-4fae-89bc-b1d5591fca77
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 100%

---

# Über Profile{#about-profiles}

Die Adobe Campaign-Plattform ermöglicht die Verwaltung von Kontakten über den gesamten Zyklus hinweg, von der Erstellung bzw. dem Import über die Zielgruppenbestimmung und das Tracking bis hin zur Aktualisierung. Kontakte werden in der Datenbank in Form von Profilen mit den entsprechenden Informationen – Nachname, Vorname, Adressdaten, Abonnements, Sendungen etc. – gespeichert.

>[!NOTE]
>
>Profile sind auch über die Adobe Campaign Standard API verfügbar. Weiterführende Informationen finden Sie im [entsprechenden Handbuch](../../api/using/retrieving-profiles.md).

![](assets/marketing_history.png)

Bei der Erstellung von Kampagnen kann die Versandzielgruppe aus Profilen nach einfachen oder erweiterten Kriterien zusammengestellt werden. Technisch betrachtet ist ein Profil ein Eintrag in einer Datenbank, der alle zur Zielgruppenbestimmung, zur Qualifizierung und zum Tracking von Verhalten erforderlichen Informationen enthält.

Bei einem Profil kann es sich – je nach den in der Organisation verwendeten Bezeichnungen – um Kunden, Interessenten, Newsletter-Abonnenten, Empfänger, Benutzer etc. handeln. Unterschiedliche Typen von Profilen werden mit [Zielgruppendimensionen](../../automating/using/query.md#targeting-dimensions-and-resources) definiert.

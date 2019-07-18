---
title: An den Absender zurücksenden
seo-title: An den Absender zurücksenden
description: An den Absender zurücksenden
seo-description: Hier erfahren Sie, wie Sie sich vom Vorhandensein einer falschen Anschrift informieren lassen und diese von der künftigen Kommunikation ausschließen können.
page-status-flag: nie aktiviert
uuid: 11981 c 2 f -0 b 7 f -4166-9 daa-ec 6 a 6 b 4 d 367 7
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Kanäle
content-type: Referenz
topic-tags: Direktnachricht
discoiquuid: 5 f 20 ff 3 f -8242-4735-8 c 60-c 77610 edff 52
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 855db33971afdf9f02bf1b00be67c9e3f50bee06

---


# An den Absender zurücksenden{#return-to-sender}

Der Austausch einfach strukturierter Dateien, die Rücksendeinformation enthalten, mit Briefpost-Dienstleistern wird unterstützt. Auf diese Weise können entsprechende Anschriften von der künftigen Kommunikation ausgeschlossen werden. Zusätzlich können Sie sich über fehlerhafte Adressen informieren lassen und mit dem Kunden über andere Kanäle in Kontakt treten oder ihn auffordern, seine Anschrift zu aktualisieren.

Beispiel: Ein Kontakt ist umgezogen und hat Ihnen nicht seine neue Anschrift mitgeteilt. Der Provider ruft die Liste mit fehlerhaften Adressen ab und sendet diese Informationen an Adobe Campaign, wo die fehlerhaften Adressen automatisch auf die Blacklist gesetzt werden.

Damit dies funktioniert, ist im Inhalt der Standard-Versandvorlage für die Briefpost eine Versandlog-ID enthalten. Dadurch kann Adobe Campaign das Profil und die Versanddaten mit den vom Provider zurückgesendeten Informationen synchronisieren.

![](assets/direct_mail_return_sender_1.png)

Eine Importvorlage ist verfügbar unter **[!UICONTROL Adobe Campaign &gt; Ressourcen &gt; Vorlagen &gt; Importvorlagen &gt; Aktualisierung von Briefpost-Quarantänen und Versandlogs]**. Duplizieren Sie diese Vorlage, um Ihre eigene zu erstellen. Weiterführende Informationen zur Verwendung von Importvorlagen finden Sie unter [Importvorlagen verwenden](../../automating/using/defining-import-templates.md).

![](assets/direct_mail_return_sender_2.png)

Nach Abschluss des Imports führt Adobe Campaign automatisch die folgenden Aktionen aus:

* Falsche Adressen werden auf Profilebene auf die Blacklist gesetzt.
* Die wichtigsten Versandindikatoren (KPIs) werden aktualisiert.
* Die Versandlogs werden aktualisiert.


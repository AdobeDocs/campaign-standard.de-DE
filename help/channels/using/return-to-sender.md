---
title: An den Absender zurücksenden
description: Hier erfahren Sie, wie Sie sich vom Vorhandensein einer falschen Anschrift informieren lassen und diese von der künftigen Kommunikation ausschließen können.
page-status-flag: never-activated
uuid: 11981c2f-0b7f-4166-9daa-ec6a6b4d5367
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: direct-mail
discoiquuid: 5f20ff3f-8242-4735-8c60-c57610edff52
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '227'
ht-degree: 100%

---


# An den Absender zurücksenden{#return-to-sender}

Der Austausch einfach strukturierter Dateien, die Rücksendeinformation enthalten, mit Briefpost-Dienstleistern wird unterstützt. Auf diese Weise können entsprechende Anschriften von der künftigen Kommunikation ausgeschlossen werden. Zusätzlich können Sie sich über fehlerhafte Adressen informieren lassen und mit dem Kunden über andere Kanäle in Kontakt treten oder ihn auffordern, seine Anschrift zu aktualisieren.

Beispiel: Ein Kontakt ist umgezogen und hat Ihnen nicht seine neue Anschrift mitgeteilt. Der Provider ruft die Liste mit fehlerhaften Adressen ab und sendet diese Informationen an Adobe Campaign, wo die fehlerhaften Adressen automatisch auf die Blockierungsliste gesetzt werden.

Damit dies funktioniert, ist im Inhalt der Standard-Versandvorlage für die Briefpost eine Versandlog-ID enthalten. Dadurch kann Adobe Campaign das Profil und die Versanddaten mit den vom Provider zurückgesendeten Informationen synchronisieren.

![](assets/direct_mail_return_sender_1.png)

Eine Importvorlage ist verfügbar unter **[!UICONTROL Adobe Campaign > Ressourcen > Vorlagen > Importvorlagen > Aktualisierung von Briefpost-Quarantänen und Versandlogs]**. Duplizieren Sie diese Vorlage, um Ihre eigene zu erstellen. Weiterführende Informationen zur Verwendung von Importvorlagen finden Sie unter [Importvorlagen verwenden](../../automating/using/importing-data-with-import-templates.md#setting-up-import-templates).

![](assets/direct_mail_return_sender_2.png)

Nach Abschluss des Imports führt Adobe Campaign automatisch die folgenden Aktionen aus:

* Falsche Adressen werden der Blockierungsliste auf Profilebene hinzugefügt.
* Die wichtigsten Versandindikatoren (KPIs) werden aktualisiert.
* Die Versandlogs werden aktualisiert.

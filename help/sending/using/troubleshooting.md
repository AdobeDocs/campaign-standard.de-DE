---
title: Fehlerbehebung bei Zustellbarkeitsproblemen in Adobe Campaign Standard
description: Erfahren Sie, wie Sie Zustellbarkeitsprobleme in Adobe Campaign Standard beheben können.
audience: sending
content-type: reference
topic-tags: sheduling-messages
context-tags: delivery,schedule,back
feature: Deliverability
role: User
level: Intermediate
exl-id: 0470b986-c00a-4441-8621-82c7112a9953
TQID: https://experienceleague.adobe.com/UyKD0H4ffjVDfJRubitjN0pJs2DQbswTlOPNzvU6zLo
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
feature_v2:
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
subfeature_v2:
  - id: a39dbcf0-89cb-4765-9bcb-cf9dfbe2875f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 85d9a6a6a6b20412c2edadfc5ced5f5e248d1ac4
workflow-type: tm+mt
source-wordcount: 484
ht-degree: 84%

---

# Fehlerbehebung{#troubleshooting}

Haben Sie ein Problem mit der Zustellbarkeit? Vielleicht finden Sie hier die Lösung.

## Gleiche Fehlermeldung bei einem ISP {#same-error-for-an-isp}

**Warum erhalte ich bei einem bestimmten ISP immer dieselbe Fehlermeldung?**

Wenn Sie immer dieselbe Fehlermeldung für einen ISP erhalten, wurde Ihre E-Mail oder IP möglicherweise vom ISP als fehlerhaft erkannt. Führen Sie die folgenden Empfehlungen aus:

* Prüfen Sie, ob Sie eine große Menge an Fehlschlägen in Verbindung mit nicht bestehenden E-Mail-Adressen erhalten (**Unbekannter Nutzer**).
* Aktualisieren Sie Ihre Anmeldeformulare und achten Sie auf etwaige Fehler im Domain-Namen (z. B. gmaul.com oder yaho.com).
* Wenn Fehlermeldungen auftreten, die Ihre E-Mails als Spam einstufen, oder wenn Ihre E-Mails blockiert werden, versuchen Sie, alle Empfänger auszuschließen, die innerhalb von 12 Monaten ab dem Versand ihre E-Mail nicht geöffnet oder darauf geklickt haben.

Wenn das Problem fortbesteht, kontaktieren Sie den Zustellbarkeitsservice oder die entsprechende Geschäftsabteilung oder den Support von Adobe Campaign.

## Blockierungsliste versus Quarantäne {#denylist-versus-quarantine}

* **Was ist der Unterschied zwischen einer E-Mail-Adresse auf einer Blockierungsliste und einer E-Mail-Adresse in Quarantäne?**

   * Der Status **[!UICONTROL Auf Blockierungsliste]** ist das Ergebnis eines [Feedback-Loops](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/transition-process/infrastructure.html?lang=de#feedback-loops) (wenn ein Empfänger eine Nachricht als Spam meldet).

   * Der Status **[!UICONTROL In Quarantäne]** ist das Ergebnis eines Soft- oder Hardbounce.

  Weiterführende Informationen hierzu finden Sie in [diesem Abschnitt](../../sending/using/understanding-quarantine-management.md#quarantine-vs-denylist).

* **Was bedeuten die unterschiedlichen Gründe für Quarantäne-Fehler?**

  Es gibt zehn Gründe: Unbestimmt, Unbekannter Nutzer, Ungültige Domain, Adresse auf der Blockierungsliste, Zurückgewiesen, Fehler ignoriert, Unerreichbar, Konto deaktiviert, Postfach voll, Nicht angemeldet.

  Weitere Informationen hierzu finden Sie unter [Funktionsweise der Quarantäneverwaltung](../../sending/using/understanding-quarantine-management.md).

## Aus Blockierungsliste entfernen {#removing-from-denylist}

* **Einer meiner Empfänger wurde versehentlich der Blockierungsliste hinzugefügt. Wie kann ich ihn aus der Blockierungsliste entfernen, damit ich ihm wieder Nachrichten senden kann?**

   * Gehen Sie zu **[!UICONTROL Administration > Kanäle > Quarantänen > Adressen]**.
   * Setzen Sie in den Details des entsprechenden Datensatzes den Wert des **[!UICONTROL Status]**-Feldes auf **[!UICONTROL Gültig]**.
   * Speichern Sie die Daten.

* **Wie kann ich feststellen, ob eine meiner IP-Adressen auf einer Blockierungsliste steht? Wie kann ich meine IP-Adresse(n) wieder aus der Blockierungsliste entfernen?**

  Um zu überprüfen, ob Ihre IP-Adresse auf einer Blockierungsliste steht, können Sie verschiedene Websites verwenden, um sie zu überprüfen, z. B.:
   * [MX Toolbox](https://mxtoolbox.com/)
   * [Wie lautet meine IP-Adresse?](https://whatismyipaddress.com)

  Nach der IP-Adressen-Prüfung erhalten Sie eine Liste mit Details zur Blockierungsliste und auch den Namen der Website, von der die IP-Adresse auf die Blockierungsliste gesetzt wurde.

  Durch Auswahl des entsprechenden Links können Sie die Details der Website aufrufen.

  Dann können Sie diese Website ersuchen, Ihre Website von der Blockierungsliste zu löschen.

  >[!NOTE]
  >
  >Der Löschvorgang kann je nach Website variieren. Bei einigen Sites müssen Sie ein Konto erstellen, während andere nur die IP-Adresse angeben müssen.

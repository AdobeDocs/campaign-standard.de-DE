---
title: Best Practices bei der Inhaltserstellung
seo-title: Best Practices bei der Inhaltserstellung
description: Best Practices bei der Inhaltserstellung
seo-description: Beachten Sie die folgenden Hinweise, um eine optimale Funktionsweise des Editors zu gewährleisten.
page-status-flag: never-activated
uuid: ad74f49d-999f-4140-89b0-d1ead8642d89
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: about-content-design
discoiquuid: d33f5f14-a4e3-4327-bd16-eb3135a32076
internal: n
snippet: y
translation-type: ht
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Best Practices bei der Inhaltserstellung{#content-design-best-practices}

Bitte beachten Sie folgende Hinweise, um eine optimale Funktionsweise des Editors zu gewährleisten:

* SCSS-Stylesheets werden nicht unterstützt. Verwenden Sie beim Import von ZIP-Dateien mit HTML-Inhalten reguläre CSS-Stylesheets.
* Bei der Bearbeitung von **E-Mail-Inhalt**:

   Sehen Sie sich Ihre Nachrichten in der Vorschau an, bevor Sie sie senden. Adobe Campaign ermöglicht es Ihnen, mithilfe von Litmus das E-Mail-Rendering zu testen. Weiterführende Informationen dazu finden Sie im Abschnitt [E-Mail-Rendering](../../sending/using/email-rendering.md).

* Bei der Bearbeitung von **Inhalt der Landingpage**:

   * Bevor Sie in Adobe Campaign eine HTML-Vorlage importieren, ist sicherzustellen, dass die Vorlage korrekt geöffnet und in den verschiedenen Browsern angezeigt werden kann.
   * Wenn die HTML-Seite JavaScript-Elemente enthält, müssen diese außerhalb des Editors fehlerfrei ausführbar sein. Vermeiden Sie im Allgemeinen die Verwendung von Scripts in Nachrichten, um die korrekte Verarbeitung durch E-Mail-Clients zu gewährleisten.
   * Bei der Erstellung einer Vorlage wird empfohlen, den Tags ein **'type'**-Attribut beizufügen. Die Interpretation dieser Information durch den Editor hilft dem Benutzer bei der Zuordnung von Datenbankfeldern zu Formularfeldern bei der Konfiguration von Webanwendungen.

      Beispiel eines HTML-Codes in einer Vorlage:

      ```
      <input id="email" type="email" name="email"/>
      ```

      Eine offizielle Liste aller möglichen 'type'-Attribute ist unter folgender Adresse abrufbar: [http://www.w3schools.com/tags/att_input_type.asp](http://www.w3schools.com/tags/att_input_type.asp).

Weitere Empfehlungen zum Erstellen und zu allgemeinen Themen in Bezug auf Nachrichten finden Sie in diesem Adobe Campaign-Handbuch: [Best Practices beim Versand mit Adobe Campaign](https://docs.campaign.adobe.com/doc/standard/getting_started/de/ACS_DeliveryBestPractices.html).

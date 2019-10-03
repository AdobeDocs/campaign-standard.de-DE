---
title: Über die Inhaltserstellung von Landingpages
seo-title: Über die Inhaltserstellung von Landingpages
description: Über die Inhaltserstellung von Landingpages
seo-description: Hier erhalten Sie die wichtigsten Informationen zum Inhaltseditor für Landingpages.
page-status-flag: never-activated
uuid: 8b230690-8a63-44da-b4ed-8e9d8fd84262
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-landing-page-content
discoiquuid: 212720d2-5d57-4e7a-bb72-10512050e78c
internal: n
snippet: y
translation-type: ht
source-git-commit: ea825afe573959d95d0f7f3f6e79dd38ac5a678a

---

# Über die Inhaltserstellung von Landingpages{#about-landing-page-content-design}

Der Standard-Inhaltseditor ermöglicht die Erstellung und Änderung des Inhalts Ihrer Landingpages in Adobe Campaign.

In diesem Abschnitt erfahren Sie die wichtigsten Informationen zum Inhaltseditor für Landingpages:

* [Benutzeroberfläche des Inhaltseditors für Landingpages](../../channels/using/landing-page-content-editor-interface.md)
* [Struktur und Stil von Landingpages verwalten](../../channels/using/managing-landing-page-structure-and-style.md)
* [Landingpage über die Dateneigenschaften ändern](../../channels/using/changing-a-landing-page-form-data-properties.md)

Weiterführende Informationen zu den wichtigsten Marketingaktivitäten finden Sie in diesen Abschnitten:

* Lesen Sie zur Personalisierung des Inhalts einer Landingpage die Abschnitte [Personalisierungsfelder einfügen](../../designing/using/personalization.md#inserting-a-personalization-field) und [Inhaltsbausteine](../../designing/using/personalization.md#adding-a-content-block).
* Lesen Sie zur Definition dynamischer Inhalte in einer Landingpage den Abschnitt [Dynamische Inhalte in einer Landingpage definieren](../../channels/using/defining-dynamic-content-in-a-landing-page.md).
* Lesen Sie zum Einfügen von Links in eine Landingpage den Abschnitt [Link einfügen](../../designing/using/links.md#inserting-a-link).
* Lesen Sie zum Einfügen von Bildern in eine Landingpage den Abschnitt [Bilder einfügen](../../designing/using/images.md).

Lesen Sie diesbezüglich auch die [allgemeinen Best Practices für die Gestaltung von Inhalten](../../designing/using/overview.md#content-design-best-practices).

>[!NOTE]
>
>Wenn Ihre Instanz vor der Adobe-Campaign-Standard-Version 19.0 installiert wurde, haben Sie noch Zugriff auf den Legacy-E-Mail-Inhaltseditor. Die Benutzeroberfläche, Verwendung und Konfiguration entsprechen größtenteils der für Landingpages geltenden unten stehenden Beschreibung. Es kann jedoch sein, dass nicht alle Funktionen im Legacy-E-Mail-Inhaltseditor verfügbar oder auf dem aktuellen Stand sind, da er ab der Version 19.0 eingestellt wird. Wenn Sie Ihren E-Mail-Inhalt rasch auf einer Drag &amp; Drop-Benutzeroberfläche mithilfe einer Fülle von Funktionen bearbeiten möchten, verwenden Sie [Email Designer](../../designing/using/overview.md).

## Best Practices für den Entwurf von Landingpages{#landing-pages-best-practices-design}

* Bei der Bearbeitung von **Inhalt der Landingpage**:

   * Bevor Sie in Adobe Campaign eine HTML-Vorlage importieren, ist sicherzustellen, dass die Vorlage korrekt geöffnet und in den verschiedenen Browsern angezeigt werden kann.
   * Wenn die HTML-Seite JavaScript-Elemente enthält, müssen diese außerhalb des Editors fehlerfrei ausführbar sein. Vermeiden Sie im Allgemeinen die Verwendung von Scripts in Nachrichten, um die korrekte Verarbeitung durch E-Mail-Clients zu gewährleisten.
   * Bei der Erstellung einer Vorlage wird empfohlen, den Tags ein **'type'**-Attribut beizufügen. Die Interpretation dieser Information durch den Editor hilft dem Benutzer bei der Zuordnung von Datenbankfeldern zu Formularfeldern bei der Konfiguration von Webanwendungen.
   Beispiel eines HTML-Codes in einer Vorlage:

   ```
   <input id="email" type="email" name="email"/>
   ```

   Eine offizielle Liste aller möglichen 'type'-Attribute ist unter folgender Adresse abrufbar: [http://www.w3schools.com/tags/att_input_type.asp](http://www.w3schools.com/tags/att_input_type.asp).
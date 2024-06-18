---
title: Personalisierte Inhalte erstellen
audience: delivery
content-type: reference
topic-tags: deliveries-best-practices
index: y
description: Erfahren Sie, wie Sie gängige Probleme bei der Gestaltung Ihres Nachrichteninhalts vermeiden, die die Ausführung des Versands behindern könnten. 
feature: Deliverability
role: User
level: Intermediate
exl-id: 938989c9-ef19-4297-9b8b-c38eb1cec1f0
source-git-commit: fcb5c4a92f23bdffd1082b7b044b5859dead9d70
workflow-type: ht
source-wordcount: '1049'
ht-degree: 100%

---

# Personalisierte Inhalte erstellen {#build-personalized-content}

Versuchen Sie beim Entwerfen Ihres Nachrichteninhalts gängige Probleme zu vermeiden, die den Versand verhindern könnten. In den meisten Fällen beziehen sich mögliche Fehler auf [Personalisierung](../../designing/using/personalization.md), Formatierung bei der [Verwendung eines vorhandenen Inhalts](../../designing/using/using-existing-content.md) – und [Konvertierung eines HTML-Inhalts](../../designing/using/using-existing-content.md#converting-an-html-content) – sowie auf [Bilder](../../designing/using/images.md).

## Optimieren der Personalisierung {#optimize-personalization}

Um allgemeine Probleme bei der Zustellung Ihrer Nachrichten zu verhindern und das Benutzererlebnis zu verbessern, können Sie Ihre Nachrichten in Adobe Campaign personalisieren.

Sie können die Empfängerdaten verwenden, die in der Adobe-Campaign-Datenbank gespeichert sind oder mithilfe von Tracking, Landingpages, Abonnements etc. erfasst wurden.
Die Grundlagen der Personalisierung werden in [diesem Abschnitt](../../designing/using/personalization.md) dargestellt.

Stellen Sie sicher, dass Ihr Nachrichteninhalt korrekt aufgebaut ist, um oft mit der Personalisierung in Verbindung stehende Probleme zu verhindern.

Dynamische Inhalte können manuell hinzugefügt werden, um Ihren Empfängern entsprechend den im Ausdruckseditor definierten Bedingungen unterschiedliche Inhalte anzuzeigen. Wenn Sie dynamische Inhalte hinzufügen, müssen Sie immer eine Standardvariante für Empfänger angeben, die nicht die ausgewählten Bedingungen erfüllen.
Weiterführende Informationen dazu finden Sie in [diesem Abschnitt](../../designing/using/personalization.md#defining-dynamic-content-in-an-email).

**Tipps:** Sehen Sie sich Ihre E-Mail mit unterschiedlichen Testprofilen in der Vorschau an, um zu überprüfen, ob der dynamische Inhalt korrekt konfiguriert wurde.

## Erstellen optimierter Inhalte {#optimize-content}

Beachten Sie beim Erstellen Ihrer E-Mails die folgenden allgemeinen Best Practices.

* Halten Sie das Design einfach.

* Denken Sie an Benutzer mit Smartphones und Tablets.

* Vermeiden Sie vollständig bildbasierte E-Mails.

* Verwenden Sie E-Mail-sichere Schriftarten.

* Kodieren Sie Sonderzeichen.

### Betreff

Achten Sie besonders auf den [Betreff](../../designing/using/subject-line.md), um die Öffnungsraten zu verbessern:

* Vermeiden Sie einen zu langen Betreff. Verwenden Sie maximal 50 Zeichen.

* Vermeiden Sie die wiederholte Verwendung von Wörtern wie „gratis“ oder „Angebot“, die als Spam angesehen werden könnten.

* Vermeiden Sie Großbuchstaben und Sonderzeichen wie „!“, „£“, „€“ oder „$“.

### Mirrorseite

Beziehen Sie stets einen Link zur Mirrorseite ein. Die bevorzugte Position ist am Anfang der E-Mail – [Weitere Informationen](../../designing/using/personalization.md#adding-a-content-block)

### Abmelde-Link

Ein Abmelde-Link muss unbedingt vorhanden sein. Er muss gut sichtbar und gültig sein, und das Formular muss funktionieren. Hier erfahren Sie [die Richtlinien zu Abmelde-Links](../../designing/using/personalization.md#about-targeting-dimension).

Bei der Analyse einer Nachricht wird standardmäßig von einer [Typologieregel](../../sending/using/control-rules.md) überprüft, ob ein Abmelde-Link vorhanden ist. Ist dies nicht der Fall, wird ein Warnhinweis erstellt.

**Tipp**: Da menschliche Fehler immer möglich sind, prüfen Sie vor jedem Versand, ob der Abmelde-Link ordnungsgemäß funktioniert. Achten Sie beispielsweise beim Testversand darauf, dass der Link gültig ist, das Formular online ist und dass sich das Feld „Diese Person nicht mehr kontaktieren“ auf „Ja“ ändert.

[In diesem Abschnitt](../../designing/using/personalization.md#adding-a-content-block) erfahren Sie, wie man einen Ausschluss-Link einfügt.

### Größe der E-Mail  {#email-size}

Um Performance- oder Zustellbarkeitsprobleme zu vermeiden, wird eine E-Mail mit einer maximalen Größe von **35 KB** empfohlen.

Um Ihre E-Mail unter dem Grenzwert zu halten, beachten Sie Folgendes:

* Entfernen Sie redundante oder nicht verwendete Stile.

* Verschieben Sie einen Teil des E-Mail-Inhalts auf eine [Landingpage](../../channels/using/getting-started-with-landing-pages.md).

* Minimieren Sie den Code.

Testen Sie alle Änderungen vor dem endgültigen Senden.

In Adobe Campaign ist die standardmäßige Maximalgröße einer E-Mail mit **100 MB** festgelegt. <!--This limit enables to prevent any error that could indefinitely increase the size of an email, which can lead to a system crash.-->

Wenn das Limit erreicht wird, schlägt die Nachricht, die das Limit überschreitet, fehl und es wird eine Fehlermeldung in den Versandlogs angezeigt. Die anderen Nachrichten desselben Versands sind nicht betroffen. In diesem Fall müssen Sie den dynamischen Teil der E-Mail-Vorlage oder die vom Versand verwendeten Inhaltsfragmente anpassen. <!--If you need assistance, or if you have any question or request about the **[!UICONTROL Maximum message size]** option, reach out to your Adobe contact.-->

Adobe empfiehlt, den Standardwert für die maximale Nachrichtengröße beizubehalten. Dieser Wert kann jedoch nur durch [funktionale Administratoren](../../administration/using/users-management.md#functional-administrators) in der Option **[!UICONTROL Maximale Nachrichtengröße]** über das Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Optionen]** geändert werden.

>[!IMPORTANT]
>
>Wenn Sie diesen Wert auf null setzen, wird keine Maximalgröße angewendet.

### Länge der SMS

Standardmäßig kommt in Bezug auf die maximal zulässige Zeichenanzahl einer SMS der Mobilfunkstandard GSM (Global System for Mobile Communications) zur Anwendung. SMS, die das GSM-Alphabet verwenden, sind auf 160 Zeichen begrenzt oder auf 153 Zeichen pro SMS bei Nachrichten, die in mehreren Teilen gesendet werden.

Die Transliteration besteht darin, ein Zeichen einer SMS durch ein anderes zu ersetzen, wenn dieses Zeichen vom GSM-Standard nicht berücksichtigt wird. Beachten Sie, dass durch das Einfügen von Personalisierungsfeldern in den Inhalt Ihrer SMS-Nachricht Zeichen eingeführt werden können, die von der GSM-Kodierung nicht berücksichtigt werden. Sie können die Transliteration von Zeichen zulassen, indem Sie das entsprechende Kästchen auf der Registerkarte „SMPP-Kanaleinstellungen“ des entsprechenden **[!UICONTROL externen Kontos]** markieren.
Weiterführende Informationen finden Sie [in diesem Abschnitt](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration).

**Tipps**:

* Aktivieren Sie die Transliteration nicht, wenn Sie alle Zeichen Ihrer SMS beibehalten möchten, um beispielsweise Eigennamen unverändert zu übermitteln.

* Sollte Ihre SMS jedoch eine hohe Anzahl an Zeichen enthalten, die vom GSM-Standard nicht unterstützt werden, aktivieren Sie die Transliteration, um Ihre Versandkosten zu begrenzen.

Weiterführende Informationen finden Sie [in diesem Abschnitt](../../administration/using/configuring-sms-channel.md#sms-encoding--length-and-transliteration).

### Responsives E-Mail-Design

Responsives E-Mail-Design stellt sicher, dass eine E-Mail auf jedem Gerät optimal angezeigt wird.

* Verwenden Sie responsive E-Mail-HTML anstelle von Web-HTML.

* Verwenden Sie den Vorschaumodus und Testsendungen, um das Rendering auf möglichst vielen Geräten zu testen. Erfahren Sie, wie Sie vor dem Senden einer Nachricht eine [Vorschau](../../sending/using/previewing-messages.md) erstellen.

* Campaign Email Designer enthält Vorlagen für responsive Designs für Mobilgeräte. Weiterführende Informationen finden Sie auf [dieser Seite](../../designing/using/using-reusable-content.md#content-templates).

## Verwalten von Bildern {#manage-images}

Befolgen Sie bei der Verwendung von Bildern die unten stehenden Richtlinien.

### Verhindern der Bildblockierung

Manche E-Mail-Clients blockieren Bilder standardmäßig. Einstellungen können aber auch vom Benutzer so konfiguriert werden, dass Bilder blockiert werden, um den Datenverbrauch zu reduzieren. Wenn keine Bilder heruntergeladen werden, kann die gesamte Nachricht verloren gehen. Um dies zu vermeiden:

* Achten Sie auf eine ausgewogene Mischung aus Bild und Text. Vermeiden Sie vollständig bildbasierte E-Mails.

* Wenn in einem Bild Text enthalten sein muss, verwenden Sie „alt“ (formatierten Alternativtext) oder „title text“ (Titeltext), um die Botschaft richtig zu übermitteln. Gestalten Sie „alt“/„title text“, um sein Erscheinungsbild zu verbessern.

* Vermeiden Sie eine Verwendung von Hintergrundbildern, da diese von einigen E-Mail-Clients nicht unterstützt werden.

### Verwenden responsiver Bilder

Verwenden Sie responsive, in der Größe veränderbare Bilder. Beachten Sie, dass sich dies auf die Kosten auswirken kann, da die Erstellung länger dauert.

### Verwenden absoluter Bildreferenzen

Damit Empfänger auf die Bilder zugreifen können, müssen die in E-Mails und öffentlichen Ressourcen verwendeten Bilder, die mit Kampagnen verknüpft sind, auf einem extern zugänglichen Server gespeichert sein.

## Sehen Sie sich Ihre Nachricht in der Vorschau an {#preview-msg}

Adobe empfiehlt eine Vorschau Ihrer Nachricht, um die Personalisierung zu überprüfen und festzustellen, wie Ihre Empfänger den Versand sehen werden.

In Email Designer können Sie mit der Schaltfläche **[!UICONTROL Vorschau]** das Rendering der einzelnen Inhalte für einen Empfänger anzeigen. Die Personalisierungsfelder und bedingten Inhaltselemente werden durch die entsprechenden Informationen für das ausgewählte Profil ersetzt – [Weitere Informationen](../../sending/using/previewing-messages.md)

---
title: Dynamische Inhalte aus Target einfügen
seo-title: Dynamische Inhalte aus Target einfügen
description: Dynamische Inhalte aus Target einfügen
seo-description: Hier erfahren Sie, wie Sie dynamischen Inhalt von Adobe Target in Adobe-Campaign-Sendungen einfügen können.
page-status-flag: nie aktiviert
uuid: b 3 cc 045 f -7924-480 e -8 c 61-8246510 f 3 adb
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird integriert
content-type: Referenz
topic-tags: working-with-campaign-and-target
discoiquuid: 45 ddf 7 b 7-98 f 7-4 fdd-bb 4 a -49 ec 8490 e 877
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: eed2e3597548c97345f51fe62dd2b56af5042e87

---


# Dynamische Inhalte aus Target einfügen{#adding-target-dynamic-content}

Die Integration mit Adobe Target ermöglicht es Ihnen, einem Versand dynamische Bilder hinzuzufügen, um den Inhalt zu personalisieren.

Ein dynamisches Bild kann während der Bearbeitung einer E-Mail hinzugefügt werden und verändert sich je nach Empfänger.

Bevor Sie auf das Bild in Adobe Campaign zugreifen, müssen Sie die folgenden Schritte in Adobe Target durchführen:

* [Umleitungsangebote](https://docs.adobe.com/content/help/en/target/using/experiences/offers/offer-redirect.html), in denen die URL der zu verwendenden Bilder anzugeben ist;
* [Zielgruppen](https://marketing.adobe.com/resources/help/en_US/target/ov/c_about_segments.html), die die durch Ihre Aktivität anzusprechenden Kontakte enthalten;
* Aktivität vom Typ [formularbasierter Experience Composer](https://marketing.adobe.com/resources/help/en_US/target/target/t_form_experience_composer.html), in der eine Rawbox auszuwählen und entsprechend der Anzahl erstellter Umleitungsangebote Erlebnisse zu definieren sind. Für jedes Erlebnis ist eins der erstellten Umleitungsangebote auszuwählen.
* Erstellen Sie Segmente mit Informationen von Adobe Campaign, um Erlebnisse zu spezifizieren. Wenn Sie in den Angebotsauswahlregeln Daten aus Adobe Campaign verwenden möchten, müssen diese in der Adobe-Target-Rawbox angegeben werden.

1. Erstellen Sie in Adobe Campaign einen E-Mail-Versand.
1. Markieren Sie im Inhaltseditor einer E-Mail oder einer Landingpage einen Bild-Block und wählen Sie über das Kontextmenü die Option **[!UICONTROL Dynamisches Bild von Adobe Target]aus.**

   ![](assets/tar_insert_dynamic_image.png)

1. Wählen Sie das Bild aus, das standardmäßig in der E-Mail angezeigt werden soll. Sie können die Bild-URL angeben oder ein in [Assets](../../integrating/using/working-with-campaign-and-assets-core-service.md) freigegebenes Bild verwenden.

   Im Rahmen der Integration werden nur statische Bilder unterstützt. Der weitere Inhalt kann nicht personalisiert werden.

1. Geben Sie den Namen der in Adobe Target definierten Rawbox an.
1. Wenn Sie in Ihren Einstellungen in Adobe Target Berechtigungen auf Unternehmensebene verwenden, fügen Sie in diesem Feld die entsprechende Eigenschaft hinzu. Weiterführende Informationen zu Berechtigungen auf Unternehmensebene in Target finden Sie auf [dieser Seite](https://marketing.adobe.com/resources/help/en_US/target/target/properties-overview.html). Dieses Feld ist optional und nicht erforderlich, wenn Sie keine Berechtigungen auf Unternehmensebene in Target verwenden. 
1. In **[!UICONTROL Additional decision parameters]**, specify the mapping between the fields defined in the Adobe Target segments and the Adobe Campaign fields.

   Die in Adobe Campaign verwendeten Felder müssen zuvor in der Rawbox angegeben werden. In unserem Beispiel definieren wir unterschiedliche Erlebnisse je nach dem Geschlecht des Empfängers.

   ![](assets/tar_additional_decisionning_parameters.png)

1. Sehen Sie sich die Vorschau der E-Mail an, um festzustellen, ob je nach ausgewähltem Profil das angezeigte Bild wechselt. Die Anzeige erfolgt in Abhängigkeit von den Parametern, die in Adobe Campaign und in der Aktivität in Adobe Target konfiguriert wurden.

Ihre Versand mit dem dynamischen Bild kann jetzt durchgeführt werden. Die Ergebnisse sind in Adobe Target zu sehen.

**Verwandte Themen:**

* [Adobe-Target-Portal](https://marketing.adobe.com/resources/help/en_US/target/a4t/c_campaign_and_target.html)
* [Über die Inhaltserstellung in E-Mails](../../designing/using/about-email-content-design.md)
* Video [Personalize Email Images in Real-Time](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html)


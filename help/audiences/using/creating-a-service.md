---
title: Dienst erstellen
seo-title: Dienst erstellen
description: Dienst erstellen
seo-description: Hier erfahren Sie, wie Sie Ihren ersten Dienst erstellen und ihn so konfigurieren, dass Sie E-Mail-Bestätigungen an Ihre Abonnenten senden können.
page-status-flag: nie aktiviert
uuid: 0 d 95 d 852-0 f 22-4 b 7 b-b 301-8 fb 4844 c 3 ca 2
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: Zielgruppen
content-type: Referenz
topic-tags: managing-subscriptions
discoiquuid: 6 b 7788 fe-fa 6 c -472 a -97 db -765595 ce 1589
context-tags: service, Assistent; service, main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6a877d878f01fa1e541dc20b8b0941602113d15b

---


# Dienst erstellen{#creating-a-service}

Um Anmeldungen verwalten zu können, müssen Sie zunächst einen Dienst erstellen und konfigurieren. Durch die Konfiguration eines neuen Dienstes können Sie die Bestätigungs-E-Mails spezifizieren, welche die Nutzer erhalten, die sich vom Dienst an- oder abmelden. Außerdem definieren Sie dabei die Anmelde- und -Abmelde-Landingpages, die dem Dienst zugeordnet sind. Beispielsweise leitet ein in eine E-Mail eingefügter Anmelde-Link für einen Dienst den Nutzer zu der im Dienst angegebenen Anmelde-Landingpage weiter.

So konfigurieren Sie einen Dienst:

1. Greifen Sie mithilfe des Adobe-Campaign-Logos oben links im Bildschirm auf das erweiterte Menü **Profile &amp; Audiences** &gt; **Dienste** zu und fügen Sie einen neuen Dienst hinzu oder öffnen Sie einen bestehenden. Bei Erstellung eines neuen Dienstes führt der Assistent Sie Schritt für Schritt durch die Konfiguration.

   Eine Standard-Dienstvorlage steht zur Verfügung. Diese Vorlage ist so vorkonfiguriert, dass sie Standard-Landingpages und -Bestätigungs-E-Mails enthält. Sie haben jedoch die Möglichkeit der Erstellung anderer Vorlagen, wenn Sie spezielle Parameter angeben möchten. Weiterführende Informationen finden Sie im Abschnitt [Marketingaktivitäten-Vorlagen](../../start/using/about-templates.md).

1. Gehen Sie mithilfe der Schaltfläche ![ in die **Eigenschaften des Dienstes** und konfigurieren Sie die Bestätigungsnachrichten, die bei Anmeldungen oder Abmeldungen versendet werden sollen.](assets/edit_darkgrey-24px.png)

   ![](assets/lp_service_parameters.png)

1. Wählen Sie eine Bestätigungsnachrichtenvorlage für An- und Abmeldungen aus. Drei Modi sind verfügbar:

   * **[!UICONTROL Keine Nachricht]**: Mit diesem Modus können Sie einen Dienst ohne Bestätigungsnachricht erstellen.
   * **[!UICONTROL Standardnachricht]**: Bei diesem Modus wird die standardmäßige Bestätigungs-Transaktionsnachricht für An- oder Abmeldungen verwendet. Die Standard-Bestätigungsnachrichten sind allgemein gehalten und für alle Dienste identisch, die den Standardmodus verwenden.
   * **[!UICONTROL Benutzerdefinierte Nachricht]**: In diesem Modus können Sie benutzerdefinierte Bestätigungsnachrichten verwenden, die für jeden Dienst anders sind. Wählen Sie hierfür die Option **[!UICONTROL Benutzerdefinierte Konfiguration des Anmeldeereignisses]aus. Diese Konfiguration ist mit einer bestimmten Transaktionsnachrichtenvorlage verknüpft.** Weiterführende Informationen zur Konfiguration von Transaktionsereignissen und -nachrichten finden Sie in [Transaktionsnachrichten](../../channels/using/about-transactional-messaging.md).

1. Speichern Sie den Dienst. Dieser kann nun verwendet werden.

Nachdem ein Dienst erstellt wurde, können Sie damit beginnen, ihn zu bewerben.

**Verwandte Themen:**

* Video [Managing a service and subscriptions](https://helpx.adobe.com/campaign/kt/acs/using/acs-services-and-subscriptions-feature-video-use.html)
* [Dienst bewerben](../../audiences/using/promoting-a-service.md)
* [Erstellen einer Audience aus Abonnenten](../../audiences/using/creating-audiences.md#creating-list-audiences)
* [Formular einem Dienst zuordnen](../../channels/using/designing-a-landing-page.md#linking-a-form-to-a-service)


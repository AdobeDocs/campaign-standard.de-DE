---
title: Dienst erstellen
seo-title: Dienst erstellen
description: Dienst erstellen
seo-description: Hier erfahren Sie, wie Sie Ihren ersten Dienst erstellen und ihn so konfigurieren, dass Sie E-Mail-Bestätigungen an Ihre Abonnenten senden können.
page-status-flag: never-activated
uuid: 0d95d852-0f22-4b7b-b301-8fb4844c3ca2
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: audiences
content-type: reference
topic-tags: managing-subscriptions
discoiquuid: 6b7788fe-fa6c-472a-97db-765595ce1589
context-tags: service,wizard;service,main
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 32a11ad57eee6bc0b7ab693fbaa55811f36f94dc

---


# Dienst erstellen{#creating-a-service}

Um Anmeldungen verwalten zu können, müssen Sie zunächst einen Dienst erstellen und konfigurieren. Durch die Konfiguration eines neuen Dienstes können Sie die Bestätigungs-E-Mails spezifizieren, welche die Nutzer erhalten, die sich vom Dienst an- oder abmelden. Außerdem definieren Sie dabei die Anmelde- und -Abmelde-Landingpages, die dem Dienst zugeordnet sind. Beispielsweise leitet ein in eine E-Mail eingefügter Anmelde-Link für einen Dienst den Nutzer zu der im Dienst angegebenen Anmelde-Landingpage weiter.

So konfigurieren Sie einen Dienst:

1. From the advanced menu **[!UICONTROL Profiles &amp; audiences]** &gt; **[!UICONTROL Services]** via the Adobe Campaign logo, add a new service or select an existing service. Bei Erstellung eines neuen Dienstes führt der Assistent Sie Schritt für Schritt durch die Konfiguration.

   Eine Standard-Dienstvorlage steht zur Verfügung. Diese Vorlage ist so vorkonfiguriert, dass sie Standard-Landingpages und -Bestätigungs-E-Mails enthält. Sie haben jedoch die Möglichkeit der Erstellung anderer Vorlagen, wenn Sie spezielle Parameter angeben möchten. Weiterführende Informationen finden Sie im Abschnitt [Marketingaktivitäten-Vorlagen](../../start/using/about-templates.md).

1. Gehen Sie mithilfe der Schaltfläche **in die**![Eigenschaften des Dienstes](assets/edit_darkgrey-24px.png) und konfigurieren Sie die Bestätigungsnachrichten, die bei Anmeldungen oder Abmeldungen versendet werden sollen.

   ![](assets/lp_service_parameters.png)

1. Füllen Sie das Feld **[!UICONTROL Dienstbezeichnung]** aus. Die Dienstbezeichnung ist bei Verwendung einer benutzerdefinierten Bestätigungsmeldung obligatorisch.

1. Wählen Sie eine Bestätigungsnachrichtenvorlage für An- und Abmeldungen aus. Drei Modi sind verfügbar:

   * **[!UICONTROL Keine Nachricht]**: Mit diesem Modus können Sie einen Dienst ohne Bestätigungsnachricht erstellen.
   * **[!UICONTROL Standardnachricht]**: Bei diesem Modus wird die standardmäßige Bestätigungs-Transaktionsnachricht für An- oder Abmeldungen verwendet. Die Standard-Bestätigungsnachrichten sind allgemein gehalten und für alle Dienste identisch, die den Standardmodus verwenden.

      >[HINWEIS]
      >
      >Sie können eine Standardnachricht ändern, indem Sie im Abschnitt " **[!UICONTROL Diensteigenschaften]** "auf ihre Beschriftung klicken oder sie in der Transaktionsmeldungsliste von Adobe Campaign auswählen, nachdem Sie das Feld "Interne Transaktionsmeldungen **[!UICONTROL anzeigen"aktiviert haben]** .

   * **[!UICONTROL Benutzerdefinierte Nachricht]**: In diesem Modus können Sie benutzerdefinierte Bestätigungsnachrichten verwenden, die für jeden Dienst anders sind. Wählen Sie hierfür die Option **[!UICONTROL Benutzerdefinierte Konfiguration des Anmeldeereignisses]** aus. Diese Konfiguration ist mit einer bestimmten Transaktionsnachrichtenvorlage verknüpft.[](../../channels/using/about-transactional-messaging.md) Weitere Informationen finden Sie unter [Bestätigen des Abonnements für einen Dienst](../../audiences/using/confirming-subscription-to-a-service.md).

1. Speichern Sie den Dienst. Dieser kann nun verwendet werden.

Nachdem ein Dienst erstellt wurde, können Sie damit beginnen, ihn zu bewerben.

**Verwandte Themen:**

* Video [Managing a service and subscriptions](https://helpx.adobe.com/campaign/kt/acs/using/acs-services-and-subscriptions-feature-video-use.html)
* [Dienst bewerben](../../audiences/using/promoting-a-service.md)
* [Erstellen einer Audience aus Abonnenten](../../audiences/using/creating-audiences.md#creating-list-audiences)
* [Formular einem Dienst zuordnen](../../channels/using/designing-a-landing-page.md#linking-a-form-to-a-service)


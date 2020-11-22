---
solution: Campaign Standard
product: campaign
title: Erste Schritte mit der Administration von Campaign Standard
description: Entdecken Sie die Benutzer- und -Berechtigungsverwaltung, Monitoring-Richtlinien, kanalspezifische Konfigurationen und Richtlinien für die Anwendungskonfiguration.
audience: administration
content-type: reference
topic-tags: about-administrating-adobe-campaign
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 100%

---


# Erste Schritte mit der Administration von Campaign Standard {#about-administrating-adobe-campaign}

<table>
<tr><td><img src="assets/do-not-localize/icon_menu.svg" width="60px"><p><a href="#administration-menu">Menü "Administration"</a></p></td>
<td><img src="assets/do-not-localize/icon_users.svg" width="60px"><p><a href="#users-security">Benutzer und Sicherheit</a></p></td>
<td><img src="assets/do-not-localize/icon_channels.svg" width="60px"><p><a href="#channels-configuration">Konfiguration von Kanälen</a></p></td>
<td><img src="assets/do-not-localize/icon_settings.svg" width="60px"><p><a href="#application-settings">Anwendungskonfiguration</a></p></td></tr>
</table>

Als Cloud-basierte Lösung bietet Adobe Campaign Administratoren unterschiedliche Konfigurationsmöglichkeiten. Obwohl die Konfiguration der Infrastruktur von Adobe durchgeführt wird, können funktionale Administratoren verschiedene Konfigurationsvorgänge ausführen, die nachfolgend beschrieben werden.

>[!NOTE]
>
>Wenn Sie Fragen oder Anliegen zur Implementierung und Konfiguration haben, kontaktieren Sie Ihren Adobe-Kundenbetreuer.

## Menü &quot;Administration&quot; {#administration-menu}

<img src="assets/do-not-localize/icon_menu.svg" width="60px">

Die verschiedenen Verwaltungsoperationen von Adobe Campaign werden über das Menü **[!UICONTROL Administration]** ausgeführt, das durch Anklicken des Adobe Campaign-Logos oben links aufgerufen werden kann. Auf diesen Bereich der Benutzeroberfläche können nur funktionale Plattform-Administratoren zugreifen.

Folgende Menüs stehen zur Verfügung:

* [Benutzer &amp; Sicherheit](../../administration/using/about-access-management.md) - ermöglicht die Verwaltung der Zugriffsberechtigungen zur Plattform (Benutzer, Benutzerrollen, Sicherheitsgruppen, Geografische Einheiten und Organisationseinheiten).
* [Kanäle](../../administration/using/about-channel-configuration.md): Dieses Menü enthält die technischen Parameter, die mit den Plattformkanälen (E-Mail, SMS) verknüpft sind sowie die Typologie- und Quarantäneverwaltung.
* [Anwendungskonfiguration](../../administration/using/external-accounts.md) - ermöglicht die Konfiguration verschiedener Anwendungselemente (externe Konten, Optionen, technische Workflows).
* [Entwicklung](../../developing/using/data-model-concepts.md) - ermöglicht die Erstellung und Verwaltung benutzerdefinierter Ressourcen sowie den Zugriff auf Monitoring-Tools.
* [Instanzenkonfiguration](../../administration/using/branding.md) - erlaubt die Definition verschiedener Marken und ihrer Parameter (Logo, Trackingverwaltung, Domain der Landingpage-URLs etc.).
* [Freigabe](../../automating/using/managing-packages.md) - bietet Zugriff auf die Package-Exporte und -Importe.
* [Kundenmetriken](../../audiences/using/active-profiles.md): Adobe Campaign erstellt einen Bericht, in dem die Anzahl der aktiven Profile dargestellt wird. Dieser Bericht hat nur informativen Charakter und keine direkte Auswirkung auf die Rechnungsstellung.
* [Datenschutz-Tools](https://docs.campaign.adobe.com/doc/standard/getting_started/de/ACS_GDPR.html): In diesem Menü können Sie einen DSGVO-konformen Zugriff erstellen sowie Abfragen löschen und ihre Entwicklung verfolgen.

## Benutzer und Sicherheit {#users-security}

<img src="assets/do-not-localize/icon_users.svg"  width="60px">

Hier können Sie Benutzer einladen, auf die Anwendung zuzugreifen, und **Sicherheitsgruppen** verwalten. Sicherheitsgruppen sind Benutzer, die innerhalb Ihres Unternehmens dieselben Rollen und Rechte haben. Adobe Campaign bietet standardmäßig eine Auswahl an **Benutzerrollen** zur Definition von Einzelberechtigungen für Benutzer und Benutzergruppen. Gemeinsam mit **Organisationseinheiten** bieten Rollen Benutzern eine gefilterte Ansicht der Benutzeroberfläche und definieren ihren Zugriff auf die unterschiedlichen Funktionen.

Mit Campaign Standard können Sie auch sicherheitsrelevante Informationen überwachen. Sie können Informationen zu den von Benutzern durchgeführten Datenexporten über den Bildschirm **[!UICONTROL Export-Audits]** abrufen und den Bildschirm **[!UICONTROL Lizenzen]** nutzen, um alle installierten Campaign-Lizenzen innerhalb Ihrer Organisation sowie verschiedene Informationen wie die Build-Nummer, die Versionsnummer und die Vertragsbedingungen zu überwachen.

Mehr dazu:

* [Benutzerverwaltung](../../administration/using/users-management.md)
* [Organisationseinheiten](../../administration/using/organizational-units.md)
* [Liste der Rollen](../../administration/using/list-of-roles.md)
* [Gruppen und Benutzer verwalten](../../administration/using/managing-groups-and-users.md)
* [Log-Exporte überprüfen](../../administration/using/auditing-export-logs.md)
* [Lizenzen](../../administration/using/licenses.md)

## Konfiguration von Kanälen {#channels-configuration}

<img src="assets/do-not-localize/icon_channels.svg" width="60px">

Alle Kommunikationskanäle in Adobe Campaign müssen korrekt konfiguriert sein, damit Nachrichten effektiv gesendet werden können. Im Menü **[!UICONTROL Kanal]** können Sie die technischen Parameter verwalten, die mit den verschiedenen Kanälen verknüpft sind.

Konfigurieren Sie verschiedene **E-Mail**-Parameter: Verarbeitungsregeln für Bounce, Quarantänen, E-Mail-Eigenschaften und Routing-Parameter, Typologieregeln. Definieren Sie Routing-Konfigurationen und -Eigenschaften für den **SMS**-Kanal sowie SMS-Kodierung und -Formate.

Richten Sie **Mobile Apps** ein, um In-App-Nachrichten und Push-Benachrichtigungen mit Adobe Experience Platform-SDKs zu senden und **Transaktionsnachrichten** zu konfigurieren, indem Sie Ereignisse erstellen und einrichten.

Mehr dazu:

* [Über die Konfiguration von Kanälen](../../administration/using/about-channel-configuration.md)
* [E-Mail-Kanal konfigurieren](../../administration/using/configuring-email-channel.md)
* [SMS-Kanal konfigurieren](../../administration/using/configuring-sms-channel.md)
* [Mobile App konfigurieren](../../administration/using/configuring-a-mobile-application.md)
* [Transaktionsnachrichten konfigurieren](../../administration/using/configuring-transactional-messaging.md)

## Anwendungskonfiguration {#application-settings}

<img src="assets/do-not-localize/icon_settings.svg" width="60px">

Campaign Standard enthält verschiedene Anwendungselemente, die entsprechend Ihren Anforderungen konfiguriert werden können.

Richten Sie **externe Konten** ein, über die Adobe Campaign mit externen Servern verbunden werden kann. Greifen Sie auf Campaign Standard-Zielgruppen-Mapping zu und überwachen Sie Ihre Plattform mithilfe von **technischen Workflows**.

Definieren Sie eine oder mehrere **Marken** für Ihr Unternehmen und konfigurieren Sie bei wichtigen Systemaktivitäten den Versand von **Benachrichtigungen in Echtzeit** innerhalb der Anwendung.

Mehr dazu:

* [Über Campaign Standard-Einstellungen](../../administration/using/about-campaign-standard-settings.md)
* [Externe Konten](../../administration/using/external-accounts.md)
* [Zielgruppen-Mappings in Campaign](../../administration/using/target-mappings-in-campaign.md)
* [Technische Workflows](../../administration/using/technical-workflows.md)
* [Marken](../../administration/using/branding.md)
* [Interne Benachrichtigungen senden](../../administration/using/sending-internal-notifications.md)

## Zusätzliche Ressourcen

* [Benutzerzugriffsrechte verwalten (Video)](https://docs.adobe.com/content/help/de-DE/campaign-standard-learn/tutorials/administrating/managing-user-access-rights.html)
* [Control Panel-Dokumentation](https://docs.adobe.com/content/help/de-DE/control-panel/using/control-panel-home.html)

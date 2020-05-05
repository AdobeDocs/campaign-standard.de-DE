---
title: Erste Schritte mit der Campaign Standard-Verwaltung
description: Adobe Campaign bietet Ihnen ein umfassendes Set von Tools zur Administration der Anwendung. Hier erfahren Sie, wie Sie Benutzer verwalten und Kanäle konfigurieren können.
page-status-flag: never-activated
uuid: 64c34729-5c98-4db0-9131-af6dd0e78fb4
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: about-administrating-adobe-campaign
discoiquuid: 5587530a-2308-4be1-9f56-19eeb7a924d5
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 40bb454d13de14658bfc30a6454a1a896bf3ad70

---


# Erste Schritte mit der Campaign Standard-Verwaltung {#about-administrating-adobe-campaign}

<table>
<tr><td><img src="assets/do-not-localize/icon_menu.svg" width="60px"><p><a href="#administration-menu">Administrationsmenü</a></p></td>
<td><img src="assets/do-not-localize/icon_users.svg" width="60px"><p><a href="#users-security">Benutzer und Sicherheit</a></p></td>
<td><img src="assets/do-not-localize/icon_channels.svg" width="60px"><p><a href="#channels-configuration">Konfiguration von Kanälen</a></p></td>
<td><img src="assets/do-not-localize/icon_settings.svg" width="60px"><p><a href="#application-settings">Anwendungskonfiguration</a></p></td></tr>
</table>

Als Cloud-basierte Lösung bietet Adobe Campaign Administratoren unterschiedliche Konfigurationsmöglichkeiten. Obwohl die Infrastrukturkonfiguration von Adobe durchgeführt wird, können funktionale Administratoren verschiedene Konfigurationsvorgänge ausführen, die nachfolgend beschrieben werden.

>[!NOTE]
>
>Wenn Sie Fragen oder Anliegen zur Implementierung und Konfiguration haben, kontaktieren Sie Ihren Adobe-Kundenbetreuer.

## Administrationsmenü {#administration-menu}

<img src="assets/do-not-localize/icon_menu.svg" width="60px">

Die verschiedenen Adobe Campaign-Admin-Vorgänge werden über das **[!UICONTROL Administration]** Menü ausgeführt, das Sie durch Klicken auf das Adobe Campaign-Logo in der oberen linken Ecke erreichen können. Auf diesen Bereich der Benutzeroberfläche können nur funktionale Plattform-Administratoren zugreifen.

Folgende Menüs stehen zur Verfügung:

* [Benutzer &amp; Sicherheit](../../administration/using/about-access-management.md) - ermöglicht die Verwaltung der Zugriffsberechtigungen zur Plattform (Benutzer, Benutzerrollen, Sicherheitsgruppen, Geografische Einheiten und Organisationseinheiten).
* [Kanäle](../../administration/using/about-channel-configuration.md) - enthält die technischen Parameter in Bezug auf die Plattformkanäle (E-Mail, SMS) sowie die Typologie- und Quarantäneverwaltung.
* [Anwendungskonfiguration](../../administration/using/external-accounts.md) - ermöglicht die Konfiguration verschiedener Anwendungselemente (externe Konten, Optionen, technische Workflows).
* [Entwicklung](../../developing/using/data-model-concepts.md) - ermöglicht die Erstellung und Verwaltung benutzerdefinierter Ressourcen sowie den Zugriff auf Monitoring-Tools.
* [Instanzenkonfiguration](../../administration/using/branding.md) - erlaubt die Definition verschiedener Marken und ihrer Parameter (Logo, Trackingverwaltung, Domain der Landingpage-URLs etc.).
* [Freigabe](../../automating/using/managing-packages.md) - bietet Zugriff auf die Package-Exporte und -Importe.
* [Kundenmetriken](../../audiences/using/active-profiles.md): Adobe Campaign erstellt einen Bericht, in dem die Anzahl der aktiven Profile dargestellt wird. Dieser Bericht hat nur informativen Charakter und keine direkte Auswirkung auf die Rechnungsstellung.
* [Datenschutz-Tools](https://docs.campaign.adobe.com/doc/standard/getting_started/de/ACS_GDPR.html): In diesem Menü können Sie einen DSGVO-konformen Zugriff erstellen sowie Abfragen löschen und ihre Entwicklung verfolgen.

## Benutzer und Sicherheit {#users-security}

<img src="assets/do-not-localize/icon_users.svg"  width="60px">

Laden Sie Benutzer ein, auf die Anwendung zuzugreifen und **Sicherheitsgruppen** zu verwalten, bei denen es sich um Benutzer handelt, die innerhalb Ihres Unternehmens dieselben Rollen und Rechte haben. By default, Adobe Campaign offers a set of **roles** which allows you to define unitary authorizations assigned to users and user groups. Combined with **organizational units**, roles give users a filtered view of the interface and define their access to the different features.

Mit dem Standard für Kampagnen können Sie auch sicherheitsrelevante Informationen überwachen. Sie können Informationen zu Datenexporten abrufen, die von Benutzern über den **[!UICONTROL Export audits]** Bildschirm ausgeführt werden, und den **[!UICONTROL Licenses]** Bildschirm nutzen, um alle in Ihrem Unternehmen installierten Kampagnen-Lizenzen sowie verschiedene Informationen wie die Buildnummer, die Release-Version und die Vertragsbedingungen zu überwachen.

mehr dazu:

* [Benutzerverwaltung](../../administration/using/users-management.md)
* [Organisationseinheiten](../../administration/using/organizational-units.md)
* [Liste der Rollen](../../administration/using/list-of-roles.md)
* [Gruppen und Benutzer verwalten](../../administration/using/managing-groups-and-users.md)
* [Log-Exporte überprüfen](../../administration/using/auditing-export-logs.md)
* [Lizenzen](../../administration/using/licenses.md)

## Konfiguration von Kanälen {#channels-configuration}

<img src="assets/do-not-localize/icon_channels.svg" width="60px">

Alle Kommunikations-Kanal in Adobe Campaign müssen korrekt konfiguriert sein, um Nachrichten effektiv senden zu können. Das Menü ermöglicht Ihnen die Verwaltung der technischen , die mit den verschiedenen Kanälen verknüpft sind, **[!UICONTROL Channel]** zu verwalten.

Konfigurieren Sie verschiedene **E-Mail** -Parameter: Verarbeitungsregeln für Absprung, Quarantänen, E-Mail-Eigenschaften und Routing-Parameter, typische Regeln. Definieren Sie Routing-Konfigurationen und -Eigenschaften für den **SMS** -Kanal sowie SMS-Kodierung und -Formate.

Richten Sie **Mobilanwendungen** ein, um In-App-Nachrichten und Push-Benachrichtigungen mit Adobe Experience Platform-SDKs zu senden und **Transaktionsnachrichten** durch Erstellen und Einrichten von Ereignissen zu konfigurieren.

mehr dazu:

* [Über die Konfiguration von Kanälen](../../administration/using/about-channel-configuration.md)
* [E-Mail-Kanal konfigurieren](../../administration/using/configuring-email-channel.md)
* [SMS-Kanal konfigurieren](../../administration/using/configuring-sms-channel.md)
* [Mobile App konfigurieren](../../administration/using/configuring-a-mobile-application.md)
* [Transaktionsnachrichten konfigurieren](../../administration/using/configuring-transactional-messaging.md)

## Anwendungskonfiguration {#application-settings}

<img src="assets/do-not-localize/icon_settings.svg" width="60px">

Campaign Standard verfügt über verschiedene Anwendungselemente, die entsprechend Ihren Anforderungen konfiguriert werden können.

Set up **external accounts**, which are used to connect Adobe Campaign to external servers. Greifen Sie auf Campaign Standard-Zielgruppen-Mapping zu und überwachen Sie Ihre Plattform mithilfe von **Technischen Workflows**.

Definieren Sie eine oder mehrere **Marken** für Ihr Unternehmen und konfigurieren Sie im Falle wichtiger Systemanforderungen das Senden von **Echtzeitbenachrichtigungen** innerhalb der Anwendung.

mehr dazu:

* [Über Campaign Standard-Einstellungen](../../administration/using/about-campaign-standard-settings.md)
* [Externe Konten](../../administration/using/external-accounts.md)
* [Zielgruppen-Mappings in Campaign](../../administration/using/target-mappings-in-campaign.md)
* [Technische Workflows](../../administration/using/technical-workflows.md)
* [Marken](../../administration/using/branding.md)
* [Interne Benachrichtigungen senden](../../administration/using/sending-internal-notifications.md)

## Zusätzliche Ressourcen

* [Verwalten von Benutzerzugriffsrechten (Video)](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/managing-user-access-rights.html)
* [Dokumentation zur Systemsteuerung](https://docs.adobe.com/content/help/de-DE/control-panel/using/control-panel-home.html)

---
title: Microsoft Dynamics 365-Integration anfordern und konfigurieren
description: Erfahren Sie, wie Sie Microsoft Dynamics 365 mit Campaign Standard-Integration anfordern und konfigurieren.
page-status-flag: never-activated
uuid: ed6c1b76-87f7-4d23-b5e2-0765297a905c
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-experience-manager
discoiquuid: 6c0c3c5b-b596-459e-87dd-a06bb7d633d2
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 277663c4cf0e810f691eeebfade17bf8dd73698e

---


# Microsoft Dynamics 365-Integration anfordern und konfigurieren

Um diese Integration bereitzustellen, müssen Sie die folgenden Schritte ausführen.

Bitte beachten Sie, dass diese Integration einen Drittanbieter, Unifi, verwendet.  Im Zusammenhang mit Supportanfragen muss Adobe möglicherweise Ihre Adobe Campaign-Instanzinformationen an Unifi weitergeben.

Bitte befolgen Sie die unten stehenden Flussdiagramme und Flussdiagramme, um die Integration anzufordern und zu konfigurieren.

![](assets/provisioning-wf.png)

Flussdiagrammdetails (Maps zu den oben genannten Schritten):

1. Sie müssen bereits über Campaign Standard und Microsoft Dynamics 365 verfügen, mit Administratorzugriff auf Beginn, der diese Integration implementiert.

1. Lesen Sie diesen Artikel, überprüfen Sie Hinweise und Konfigurationsschritte.

1. Senden Sie eine Kontoanforderung an adobe-support@unifisoftware.com. Unifi benötigt beim Anfordern eines Kontos die folgenden Informationen:
   * Vorname des Benutzers
   * Nachname des Benutzers
   * Benutzer-E-Mail
   * Name der Firma
   * Region (Nordamerika, EMEA oder APAC)
   * Nutzungstyp:  &quot;Kundentyp&quot;(Kundenbenutzer, die ihre Produktionsdaten in dieser Integration verwenden) oder &quot;Partnertyp&quot;(Partnerberater, die die Integration testen, um ein besseres Verständnis zu erhalten, damit sie ihren Kunden bei der Kampagne helfen können) oder &quot;Interner Typ&quot;(interne Adobe-Benutzer, die die Integration testen, um ein besseres Verständnis der Lösung zu erhalten)
   * Datenstatus des Campaign Standards (beginnend mit einer sauberen Datenbank oder mit der Integration vorhandener Daten)
   * Kampagne Tenant ID (siehe Integrationsabschnitt für Kampagne konfigurieren, Schritt 3 zum Abrufen Ihrer Mandant-ID)
   * URL der Kampagne-Instanz
   Erwartungsfreie Ansprechzeit: 1 Stunde während der regulären Geschäftszeiten in den USA (9:00 bis 17:00 Uhr Pacific Time, Mo - Fr, ohne Urlaub).

1. Führen Sie die Nachbereitungsschritte für Microsoft Dynamics 365 und für den Campaign Standard durch.
Senden Sie außerdem ein Ticket an den Adobe-Kundendienst (entweder direkt oder über Ihren Adobe-Kontakt), um das Flag für die Single-Sign-On-Funktion in Ihrer Kampagne-Instanz aktivieren zu lassen. Partner sollten sich an ihre Adobe-Partner-Sandbox wenden und sich stattdessen an den Adobe-Kundendienst wenden, um das Feature-Flag zu aktivieren.
Wenn Sie bereits vorhandene Daten in Kampagne haben, die Sie in die Integration einbeziehen möchten, befolgen Sie die Anleitung unter &quot;Vorhandene Kampagnen-Daten&quot;und wenden Sie sich an Ihren technischen Ansprechpartner bei Adobe, bevor Sie fortfahren.

1. Führen Sie die ersten Schritte zum Einstieg in Unifi durch, indem Sie zu Unifi navigieren, auf die Einstiegsbildschirme klicken, Dynamics 365 und die Anmeldedaten des Campaign Standards eingeben und Unifi nach Abschluss benachrichtigen.

1. Unifi fragt den Kunden nach der gewünschten Abmeldekonfiguration und der Abmeldeattributzuordnung.

1. Der Kunde gibt die ausgewählte Ausschluss-Konfiguration und die Zuordnung des Ausschluss-Attributs an.
Erwartungsfreie Ansprechzeit: 1 Werktag (Mo - Fr, ohne Feiertage)

1. Die Konfiguration von Unifi umfasst die Überprüfung von OOTB-Zuordnungen, Filtern, Aufträgen usw. und gegebenenfalls Änderungen vorzunehmen.  Weitere Informationen finden Sie im Unifi-Benutzerhandbuch.
Dieser Schritt umfasst das Festlegen der Laufzeitfrequenz der Unifi-Zeitpläne
* Legen Sie die Häufigkeit der Zeitpläne im Bildschirm &quot;Zeitpläne&quot;in Unifi fest; Führen Sie für die Zeitpläne &quot;Ingress&quot;und &quot;Enress&quot;diese jedoch einmal manuell aus, bevor Sie die Zeitplanfrequenz festlegen
* Die folgenden Zeitplanhäufigkeiten werden empfohlen: Fortschritt (15 Minuten), Fortschritt (15 Minuten), Löschen (einmal täglich), Ausschluss (einmal am Tag)

**Es wird empfohlen, bei der Konfiguration von Unifi mit der Beratung von Unifi und/oder Adobe zusammenzuarbeiten (wenden Sie sich an Ihr Adobe-Kontoteam).**

Um die Integration zwischen Adobe Campaign Standard und Microsoft Dynamics 365 zu ermöglichen, müssen Kunden ein Benutzerkonto bei Unifi, einem Drittanbieter, erstellen, wie in diesem Dokument beschrieben.   Als Endbenutzer des Unifi-Systems sollte sich der Kunde für alle Anfragen im Zusammenhang mit Datenanforderungen, die vom Kunden innerhalb des Unifi-Systems initiiert werden, an Unifi wenden.

## Diese Integration konfigurieren

Für diese Integration müssen drei Systeme bereitgestellt und konfiguriert werden: Adobe Campaign Standard, Microsoft Dynamics 365 für Vertrieb und Unifi. Konfigurationsartikel sind unten verknüpft.

>[!CAUTION]
>
>Für jedes System müssen diese Schritte von einem Administrator ausgeführt werden.
>
>Die Schritte in den unten stehenden Artikeln führen Sie durch das Erstellen von Integrationen/Registrierungen, bei denen Berechtigungen und/oder Administratorzugriff zugewiesen werden.  Es liegt in Ihrer Verantwortung, sicherzustellen, dass diese Schritte vor der Ausführung den Richtlinien Ihrer Firma entsprechen, und sie sorgfältig durchzuführen.

In ADOBE CAMPAIGN müssen Sie den API-Zugriff einrichten und eine neue Integration für Unifi konfigurieren. Lesen Sie dazu [diesen Artikel](../../integrating/using/configure-adobe-io-for-ms-dynamic.md).

In MICROSOFT DYNAMICS 365 müssen Sie eine neue App-Registrierung erstellen und einem Anwendungsbenutzer die Verwendung der Integration ermöglichen.  Informationen zum Konfigurieren von Microsoft Dynamics 365 für diese Integration finden Sie in [diesem Artikel](../../integrating/using/configure-microsoft-dynamics-365-for-campaign-integration.md).

In UNIFI müssen Sie die Integration einrichten und die Zuordnung konfigurieren oder benutzerdefinierte Attribute hinzufügen. Informationen zum Konfigurieren von Unifi für diese Integration finden Sie in [diesem Artikel](../../integrating/using/configure-unifi-for-microsoft-dynamics-365-integration.md).

## Support anfordern

Wenn Probleme auftreten, wenden Sie sich bitte an den Unifi-Kundensupport: [support@unifisoftware.atlassian.net](mailto:support@unifisoftware.atlassian.net).

Erwartungsfreie Ansprechzeit: 4 Stunden während der regulären Geschäftszeiten in den USA (9:00 bis 17:00 Uhr Pacific Time, Mo - Fr, ohne Urlaub).

>[!CAUTION]
>
>Im Zusammenhang mit Ihrer Supportanfrage wird Adobe möglicherweise aufgefordert, Ihre Adobe Campaign-Instanzinformationen für Unifi freizugeben.
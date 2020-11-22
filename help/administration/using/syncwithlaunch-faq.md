---
solution: Campaign Standard
product: campaign
title: Häufig gestellte Fragen zur Synchronisierung mit dem technischen Workflows für Launch
description: Häufig gestellte Fragen zum technischen Workflow für Launch.
audience: administration
content-type: reference
topic-tags: users-and-security
translation-type: tm+mt
source-git-commit: 501f52624ce253eb7b0d36d908ac8502cf1d3b48
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 100%

---


# Häufig gestellte Fragen zur Synchronisation von Adobe Launch {#syncwithlaunch-faq}

Sie können die Adobe Launch-Eigenschaften für Smartphones und Tablets über den eigenen technischen Workflow **[!UICONTROL Synchronisieren mit Launch]** in Adobe Campaign Standard importieren. Weiterführende Informationen dazu finden Sie auf dieser [Seite](../../administration/using/technical-workflows.md)

Im folgenden Abschnitt werden häufig gestellte Fragen zu dieser Synchronisierung aufgelistet.

## Ich habe eine Eigenschaft in [!DNL Launch] erstellt (Benutzer ohne Administratorrechte der Organisationseinheit „ALLE“). Meine mobile App befindet sich im Status „Bereit zum Konfigurieren“ in Adobe Campaign, kann jedoch nicht geöffnet/konfiguriert werden. {#configuring-property}

Nur ein Administrator der Organisationseinheit „ALLE“ kann mobile Apps in Adobe Campaign Standard konfigurieren. Einmal konfiguriert, können nur Benutzer der zugeordneten Organisationseinheit die App bearbeiten. Weiterführende Informationen zu Organisationseinheiten finden Sie auf dieser [Seite](../../administration/using/organizational-units.md).

## Ich kann eine konfigurierte mobile App in Adobe Campaign Standard nicht bearbeiten, und die mobilen Apps befinden sich im schreibgeschützten Modus. {#read-mode-mobile-app}

Überprüfen Sie die Organisationseinheit der mobilen App im Abschnitt **[!UICONTROL Zugriffsberechtigung]**. Nur Benutzer der zugeordneten Organisationseinheit können die mobile App bearbeiten.

Weiterführende Informationen zu Organisationseinheiten finden Sie auf dieser [Seite](../../administration/using/organizational-units.md).

## Ich bin ein Administrator mit der Organisationseinheit „ALLE“ in Adobe Campaign Standard, kann jedoch keine mobilen Apps konfigurieren. {#org-unit-mobile}

Ein Administrator mit der Organisationseinheit „ALLE“ sollte über Rechte für alle Eigenschaften für Mobilgeräte in [!DNL Launch] verfügen, um die mobile App zu konfigurieren.

Weiterführende Informationen zu Organisationseinheiten finden Sie auf dieser [Seite](../../administration/using/organizational-units.md).

## Ich habe eine Eigenschaft für Smartphones und Tablets in [!DNL Launch] erstellt, aber meine Eigenschaft ist in Adobe Campaign Standard nicht sichtbar. {#visibility-mobile-property}

1. Überprüfen Sie, ob die Adobe Campaign Standard-Erweiterung in der Eigenschaft für Mobilgeräte in [!DNL Launch] installiert ist.

1. Stellen Sie sicher, dass die Endpunkte der Instanz in der Erweiterung korrekt konfiguriert sind.

1. Überprüfen Sie, ob „Launch_URL_Campaign“ oder „NmsServer_URL“ korrekt sind.

1. Vergewissern Sie sich anschließend, dass die Synchronisierung zwischen [!DNL Launch] und Adobe Campaign mit dem technischen Workflow **[!UICONTROL syncWithLaunch]** abgeschlossen ist.

## Wie kann ich überprüfen, ob die Synchronisierung zwischen Adobe Campaign und Launch abgeschlossen ist? {#sync-campaign-launch}

1. Wählen Sie in Adobe Campaign Standard im erweiterten Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Workflows]** aus.

1. Öffnen Sie den Workflow **[!UICONTROL syncWithLaunch]**.

1. Überprüfen Sie, ob der Workflow ohne Fehler beendet wurde.

1. Überprüfen Sie in den Protokollen, ob die Workflow-Synchronisation aktiviert und erfolgreich abgeschlossen wurde.

## Ich habe den pkey für eine konfigurierte mobile App in Launch zurückgesetzt. Wie konfiguriere ich den pkey in Launch erneut? {#configuring-pkey}

1. Öffnen Sie die Eigenschaft für Smartphones und Tablets in Adobe Launch.

1. Legen Sie eine neue URL in der Adobe Campaign Standard-Erweiterung fest, für die der pkey zurückgesetzt wurde.

1. Speichern Sie diese und lassen Sie den Workflow zwischen Adobe Campaign und [!DNL Launch] synchronisieren.

1. Nach Abschluss der Synchronisation öffnen Sie die Eigenschaft für Smartphones und Tablets in [!DNL Launch].

1. Legen Sie die richtige URL in der Adobe Campaign Standard-Erweiterung fest, für die der pkey zurückgesetzt wurde.

1. Speichern Sie diese und lassen Sie die Workflow-Synchronisation erneut laufen.

1. Erst dann erscheint die Eigenschaft im Status **[!UICONTROL Bereit zum Konfigurieren]** in Adobe Campaign und kann jetzt konfiguriert werden.

## Ich möchte eine Eigenschaft für Smartphones und Tablets in Adobe Campaign konfigurieren. Muss ich warten, bis der technische Workflow zwischen Adobe Launch und Adobe Campaign synchronisiert ist?

Sie können den Workflow sofort ausführen:

1. Wählen Sie in Adobe Campaign Standard im erweiterten Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Workflows]** aus.

1. Öffnen Sie den Workflow **[!UICONTROL syncWithLaunch]**.

1. Klicken Sie auf die Aktivität **[!UICONTROL Planung]** und wählen Sie **[!UICONTROL Vorgezogene Ausführung]** aus.

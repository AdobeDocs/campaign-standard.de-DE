---
title: Häufig gestellte Fragen zur Synchronisierung mit dem technischen Workflow für Launch
description: Häufig gestellte Fragen zum technischen Workflow für Adobe Launch
audience: administration
feature: Instance Settings
role: Admin
level: Experienced
exl-id: aaaceb3a-5e54-47da-9be4-b70747282830
source-git-commit: 7767b39a48502f97e2b3af9d21a3f49b9283ab2e
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 63%

---

# Häufig gestellte Fragen zu Tags bei der Adobe Experience Platform-Synchronisierung {#syncwithlaunch-faq}

Sie können mobile Tag-Eigenschaften über die **[!UICONTROL Mit Launch synchronisieren]** spezifischer technischer Workflow. Weiterführende Informationen dazu finden Sie auf dieser [Seite](../../administration/using/technical-workflows.md)

Im folgenden Abschnitt werden häufig gestellte Fragen zu dieser Synchronisierung aufgelistet.

## Ich habe eine Tag-Eigenschaft erstellt (kein Administrator der Organisationseinheit &quot;ALLE&quot;). Meine Mobile App befindet sich im Status &quot;Bereit zum Konfigurieren&quot; in Adobe Campaign, kann jedoch nicht geöffnet/konfiguriert werden. {#configuring-property}

Nur ein Administrator der Organisationseinheit „ALLE“ kann mobile Apps in Adobe Campaign Standard konfigurieren. Einmal konfiguriert, können nur Benutzer der zugeordneten Organisationseinheit die App bearbeiten. Weiterführende Informationen zu Organisationseinheiten finden Sie auf dieser [Seite](../../administration/using/organizational-units.md).

## Ich kann eine konfigurierte Mobile App in Adobe Campaign Standard nicht bearbeiten, und die Mobile Apps befinden sich im schreibgeschützten Modus. {#read-mode-mobile-app}

Überprüfen Sie die Organisationseinheit der Mobile App im Abschnitt **[!UICONTROL Zugriffsberechtigung]**. Nur Benutzer der zugeordneten Organisationseinheit können die mobile App bearbeiten.

Weiterführende Informationen zu Organisationseinheiten finden Sie auf dieser [Seite](../../administration/using/organizational-units.md).

## Ich bin ein Administrator mit der Organisationseinheit &quot;ALLE&quot; in Adobe Campaign Standard, kann jedoch keine Mobile Apps konfigurieren. {#org-unit-mobile}

Ein Administrator mit der Organisationseinheit &quot;ALLE&quot;sollte über Berechtigungen für alle Tag-Eigenschaften für Mobilgeräte verfügen, um die Mobile App zu konfigurieren.

Weiterführende Informationen zu Organisationseinheiten finden Sie auf dieser [Seite](../../administration/using/organizational-units.md).

## Ich habe eine mobile Tag-Eigenschaft erstellt, meine Eigenschaft ist jedoch in Adobe Campaign Standard nicht sichtbar. {#visibility-mobile-property}

1. Überprüfen Sie, ob die Adobe Campaign Standard-Erweiterung in der mobilen Eigenschaft in der Datenerfassungs-Benutzeroberfläche installiert ist.

1. Stellen Sie sicher, dass die Endpunkte der Instanz in der Erweiterung korrekt konfiguriert sind.

1. Überprüfen Sie, ob „Launch_URL_Campaign“ oder „NmsServer_URL“ korrekt sind.

1. Überprüfen Sie dann, ob die Synchronisierung mit der **[!UICONTROL syncWithLaunch]** technischer Arbeitsablauf.

## Wie kann ich überprüfen, ob die Synchronisierung zwischen Adobe Campaign und Tags in Adobe Experience Platform abgeschlossen ist? {#sync-campaign-launch}

1. Wählen Sie in Adobe Campaign Standard im erweiterten Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Workflows]** aus.

1. Öffnen Sie den Workflow **[!UICONTROL syncWithLaunch]**.

1. Überprüfen Sie, ob der Workflow ohne Fehler beendet wurde.

1. Überprüfen Sie in den Protokollen, ob die Workflow-Synchronisation aktiviert und erfolgreich abgeschlossen wurde.

## Ich habe den pkey für eine konfigurierte Tag-Mobile-Anwendung zurückgesetzt. Wie kann der pkey in der Datenerfassungs-Benutzeroberfläche neu konfiguriert werden? {#configuring-pkey}

1. Öffnen Sie die Eigenschaft für Mobilgeräte in der Datenerfassungs-Benutzeroberfläche.

1. Legen Sie eine neue URL in der Adobe Campaign Standard-Erweiterung fest, für die der pkey zurückgesetzt wurde.

1. Speichern Sie sie und lassen Sie den Workflow synchronisieren.

1. Öffnen Sie nach Abschluss der Synchronisierung die Eigenschaft für Mobilgeräte in der Benutzeroberfläche für die Datenerfassung.

1. Legen Sie die richtige URL in der Adobe Campaign Standard-Erweiterung fest, für die der pkey zurückgesetzt wurde.

1. Speichern Sie diese und lassen Sie die Workflow-Synchronisation erneut laufen.

1. Erst dann erscheint die Eigenschaft im Status **[!UICONTROL Bereit zum Konfigurieren]** in Adobe Campaign und kann jetzt konfiguriert werden.

## Ich möchte eine Eigenschaft für Smartphones und Tablets in Adobe Campaign konfigurieren. Muss ich warten, bis der technische Workflow zwischen Tags in Adobe Experience Platform und Adobe Campaign synchronisiert ist?

Sie können den Workflow sofort ausführen:

1. Wählen Sie in Adobe Campaign Standard im erweiterten Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Workflows]** aus.

1. Öffnen Sie den Workflow **[!UICONTROL syncWithLaunch]**.

1. Klicken Sie auf die Aktivität **[!UICONTROL Planung]** und wählen Sie **[!UICONTROL Vorgezogene Ausführung]** aus.

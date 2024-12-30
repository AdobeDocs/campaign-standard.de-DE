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
source-wordcount: '0'
ht-degree: 0%

---

# Häufig gestellte Fragen zur Synchronisierung von Tags in Adobe Experience Platform {#syncwithlaunch-faq}

Sie können die Tag-Eigenschaften für Mobilgeräte über den eigenen technischen Workflow **[!UICONTROL Synchronisieren mit Launch]** in Adobe Campaign Standard importieren. Weiterführende Informationen dazu finden Sie auf dieser [Seite](../../administration/using/technical-workflows.md)

Im folgenden Abschnitt werden häufig gestellte Fragen zu dieser Synchronisierung aufgelistet.

## Ich habe eine Tag-Eigenschaft erstellt (Benutzer ohne Administratorrechte der Organisationseinheit &quot;ALLE&quot;). Meine Mobile App befindet sich im Status &quot;Bereit zum Konfigurieren&quot; in Adobe Campaign, kann jedoch nicht geöffnet/konfiguriert werden. {#configuring-property}

Nur ein Administrator der Organisationseinheit „ALLE“ kann mobile Apps in Adobe Campaign Standard konfigurieren. Einmal konfiguriert, können nur Benutzer der zugeordneten Organisationseinheit die App bearbeiten. Weiterführende Informationen zu Organisationseinheiten finden Sie auf dieser [Seite](../../administration/using/organizational-units.md).

## Ich kann eine konfigurierte Mobile App in Adobe Campaign Standard nicht bearbeiten, und die Mobile Apps befinden sich im schreibgeschützten Modus. {#read-mode-mobile-app}

Überprüfen Sie die Organisationseinheit der Mobile App im Abschnitt **[!UICONTROL Zugriffsberechtigung]**. Nur Benutzer der zugeordneten Organisationseinheit können die mobile App bearbeiten.

Weiterführende Informationen zu Organisationseinheiten finden Sie auf dieser [Seite](../../administration/using/organizational-units.md).

## Ich bin ein Administrator mit der Organisationseinheit &quot;ALLE&quot; in Adobe Campaign Standard, kann jedoch keine Mobile Apps konfigurieren. {#org-unit-mobile}

Ein Administrator mit der Organisationseinheit &quot;ALLE&quot; sollte über Rechte für alle Eigenschaften für Mobilgeräte verfügen, um die Mobile App zu konfigurieren.

Weiterführende Informationen zu Organisationseinheiten finden Sie auf dieser [Seite](../../administration/using/organizational-units.md).

## Ich habe eine Tag-Eigenschaft für Mobilgeräte erstellt, aber meine Eigenschaft ist in Adobe Campaign Standard nicht sichtbar. {#visibility-mobile-property}

1. Überprüfen Sie, ob die Adobe Campaign Standard-Erweiterung in der Datenerfassungs-UI in der Eigenschaft für Mobilgeräte installiert ist.

1. Stellen Sie sicher, dass die Endpunkte der Instanz in der Erweiterung korrekt konfiguriert sind.

1. Überprüfen Sie, ob „Launch_URL_Campaign“ oder „NmsServer_URL“ korrekt sind.

1. Vergewissern Sie sich anschließend mit dem technischen Workflow **[!UICONTROL syncWithLaunch]**, dass die Synchronisierung abgeschlossen ist.

## Wie kann ich überprüfen, ob die Synchronisierung zwischen Adobe Campaign und Tags in Adobe Experience Platform abgeschlossen ist? {#sync-campaign-launch}

1. Wählen Sie in Adobe Campaign Standard im erweiterten Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Workflows]** aus.

1. Öffnen Sie den Workflow **[!UICONTROL syncWithLaunch]**.

1. Überprüfen Sie, ob der Workflow ohne Fehler beendet wurde.

1. Überprüfen Sie in den Protokollen, ob die Workflow-Synchronisation aktiviert und erfolgreich abgeschlossen wurde.

## Ich habe den pkey für eine konfigurierte Tag-Mobile-App zurückgesetzt.. Wie kann der pkey in der Datenerfassungs-UI neu konfiguriert werden? {#configuring-pkey}

1. Öffnen Sie die Eigenschaft für Mobilgeräte in der Datenerfassungs-UI.

1. Legen Sie eine neue URL in der Adobe Campaign Standard-Erweiterung fest, für die der pkey zurückgesetzt wurde.

1. Speichern Sie diese und lassen Sie die Workflow-Synchronisierung laufen.

1. Öffnen Sie nach Abschluss der Synchronisierung die Eigenschaft für Mobilgeräte in der Datenerfassungs-UI.

1. Legen Sie die richtige URL in der Adobe Campaign Standard-Erweiterung fest, für die der pkey zurückgesetzt wurde.

1. Speichern Sie diese und lassen Sie die Workflow-Synchronisation erneut laufen.

1. Erst dann erscheint die Eigenschaft im Status **[!UICONTROL Bereit zum Konfigurieren]** in Adobe Campaign und kann jetzt konfiguriert werden.

## Ich möchte eine Eigenschaft für Smartphones und Tablets in Adobe Campaign konfigurieren. Muss ich warten, bis der technische Workflow zur Synchronisierung von Tags zwischen Adobe Experience Platform und Adobe Campaign beginnt?

Sie können den Workflow sofort ausführen:

1. Wählen Sie in Adobe Campaign Standard im erweiterten Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Workflows]** aus.

1. Öffnen Sie den Workflow **[!UICONTROL syncWithLaunch]**.

1. Klicken Sie auf die Aktivität **[!UICONTROL Planung]** und wählen Sie **[!UICONTROL Vorgezogene Ausführung]** aus.

---
title: Häufig gestellte Fragen zur Synchronisierung mit dem technischen Arbeitsablauf beim Start
description: Allgemeine Fragen zum technischen Arbeitsablauf zum Starten.
page-status-flag: never-activated
uuid: 4f538452-cc67-4e03-9e2f-2d9eecc081c7
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: administration
content-type: reference
topic-tags: users-and-security
discoiquuid: 54028f63-c9ca-4397-a079-e27e0cfdebf6
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 6c5cf90211451587537b9a6121430fc4f352384c
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 6%

---


# Häufig gestellte Fragen zur Synchronisierung mit dem technischen Arbeitsablauf beim Start {#syncwithlaunch-faq}

Sie können mobile Adobe Launch-Eigenschaften über den eigenen technischen Arbeitsablauf **[!UICONTROL Synchronisieren mit Launch]** in den Adobe Campaign Standard importieren. Weiterführende Informationen dazu finden Sie auf dieser [Seite](../../administration/using/technical-workflows.md)

Im folgenden Abschnitt werden allgemeine Fragen zu dieser Synchronisierung Liste.

>[!NOTE]
>
>You will need to submit a ticket to Adobe Customer Care (either directly or through your Adobe contact) to have the **[!UICONTROL syncWithLaunch]** technical workflow enabled in your Campaign instance.

## Ich habe eine Eigenschaft in [!DNL Launch] (nicht-admin von Org-unit ALL) erstellt. Meine Anwendung befindet sich im Status &quot;Bereit zum Konfigurieren&quot;in Adobe Campaign, kann jedoch nicht geöffnet/konfiguriert werden. {#configuring-property}

Nur Administrator der Organisationseinheit ALL kann mobile Anwendungen in Adobe Campaign Standard konfigurieren. Nach der Konfiguration kann die Anwendung nur von Benutzern der zugeordneten Organisationseinheit bearbeitet werden. For more information on organizational unit, refer to this [page](../../administration/using/organizational-units.md).

## Ich kann eine konfigurierte Mobilanwendung nicht in Adobe Campaign Standard bearbeiten, und Mobilanwendungen befinden sich nur im Lesemodus. {#read-mode-mobile-app}

Überprüfen Sie die organisatorische Einheit der mobilen Anwendung im Abschnitt **[!UICONTROL Zugriffsgenehmigung]** . Die Mobilanwendung kann nur von Benutzern der zugeordneten Organisationseinheit bearbeitet werden.

For more information on organizational unit, refer to this [page](../../administration/using/organizational-units.md).

## Ich bin Administrator mit der Organisationseinheit ALL im Adobe Campaign Standard, aber ich kann keine Mobilanwendung konfigurieren. {#org-unit-mobile}

Ein Administrator mit einer auf ALL gesetzten Organisationseinheit sollte über Rechte für alle mobilen Eigenschaften verfügen, um die Mobilanwendung zu konfigurieren. [!DNL Launch]

For more information on organizational unit, refer to this [page](../../administration/using/organizational-units.md).

## Ich habe eine mobile Eigenschaft in erstellt, [!DNL Launch] aber meine Eigenschaft ist im Adobe Campaign Standard nicht sichtbar. {#visibility-mobile-property}

1. Überprüfen Sie, ob die Adobe Campaign Standard-Erweiterung in der Eigenschaft mobile in installiert ist [!DNL Launch].

1. Überprüfen Sie, ob die Endpunkte der Instanz in der Erweiterung korrekt konfiguriert sind.

1. Überprüfen Sie, ob &quot;Launch_URL_Kampagne&quot;oder &quot;NmsServer_URL&quot;korrekt sind.

1. Vergewissern Sie sich dann, dass die Synchronisierung zwischen [!DNL Launch] und Adobe Campaign mit dem technischen **[!UICONTROL Arbeitsablauf syncWithLaunch]** abgeschlossen ist.

## Wie überprüfen Sie, ob die Synchronisierung zwischen Adobe Campaign und Start abgeschlossen ist? {#sync-campaign-launch}

1. Wählen Sie in Adobe Campaign Standard im erweiterten Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Workflows]** aus.

1. Öffnen Sie den Workflow **[!UICONTROL syncWithLaunch]** .

1. Überprüfen Sie, ob der Workflow ohne Fehler beendet wurde.

1. Überprüfen Sie in den Protokollen, dass die Workflow-Synchronisierung aktiviert ist und erfolgreich abgeschlossen wurde.

## Ich setzte den Schlüssel für eine konfigurierte Mobilanwendung in Launch zurück. Wie kann der Schlüssel bei Launch neu konfiguriert werden? {#configuring-pkey}

1. Öffnen Sie die mobile Eigenschaft in Adobe Launch.

1. Legen Sie eine neue URL in der Adobe Campaign Standard-Erweiterung fest, für die der PKey zurückgesetzt wurde.

1. Speichern Sie es und lassen Sie den Workflow zwischen Adobe Campaign und [!DNL Launch]synchronisieren.

1. Nach Abschluss der Synchronisierung öffnen Sie die mobile Eigenschaft in [!DNL Launch].

1. Legen Sie die richtige URL in der Adobe Campaign Standard-Erweiterung fest, für die PKey zurückgesetzt wurde.

1. Speichern Sie sie und lassen Sie die Workflow-Synchronisierung erneut laufen.

1. Nur dann wird die Eigenschaft im Status &quot; **[!UICONTROL Bereit zum Konfigurieren]** &quot;in Adobe Campaign angezeigt und kann jetzt konfiguriert werden.

## Ich möchte eine mobile Eigenschaft in Adobe Campaign konfigurieren. Muss ich warten, bis der technische Arbeitsablauf zwischen Adobe Launch und Adobe Campaign synchronisiert wird?

Sie können den Workflow sofort ausführen:

1. Wählen Sie in Adobe Campaign Standard im erweiterten Menü **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Workflows]** aus.

1. Öffnen Sie den Workflow **[!UICONTROL syncWithLaunch]** .

1. Klicken Sie auf die Aktivität **[!UICONTROL Planung]** und wählen Sie **[!UICONTROL Sofortige Ausführung]**.

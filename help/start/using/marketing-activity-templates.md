---
title: Über Vorlagen
description: '"Mit Vorlagen in Adobe Campaign können Sie Parameter entsprechend Ihren Anforderungen vorab konfigurieren: Vorlagen können eine vollständige oder teilweise Konfiguration der Marketing-Aktivität aufweisen, damit auch technisch weniger versierte Benutzer Adobe Campaign problemlos verwenden können."'
page-status-flag: never-activated
uuid: 018534b6-61a3-433e-bb60-49883c8b9386
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: managing-templates
discoiquuid: 95218ebe-5430-42a2-b900-1dadbbc92d99
translation-type: ht
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: ht
source-wordcount: '408'
ht-degree: 100%

---


# Vorlagen für Marketingaktivitäten {#marketing-activity-templates}

## Über Vorlagen {#about-templates}

Bei der Erstellung einer Marketingaktivität ist im ersten Schritt des Assistenten ein Aktivitätstyp auszuwählen. Die verfügbaren Typen basieren jeweils auf einer Vorlage. Diese Vorlagen erlauben es, je nach Bedarf gewisse Parameter im Voraus zu konfigurieren. Vorlagen können vollständig oder nur teilweise konfiguriert sein. Die Vorlagenverwaltung erfolgt durch den funktionalen Administrator.

Der Endbenutzer verfügt über eine vereinfachte Benutzeroberfläche. Zur Erstellung einer neuen Marketingaktivität wählt er den gewünschten, auf einer Vorlage basierenden Typ aus. Technische Konfigurationen können ignoriert werden. Dies wurde bereits vom funktionalen Administrator in der Vorlage vorkonfiguriert.

Beispielsweise können Sie im Fall einer E-Mail-Vorlage den HTML-Inhalt, die Audience und andere Versandparameter automatisch ausfüllen lassen: den Zeitplan, die Testprofile, die allgemeinen Eigenschaften Ihrer Sendungen, die erweiterten Parameter etc. Dadurch sparen Sie Zeit bei der Erstellung einer neuen Aktivität.

![](assets/template_1.png)

Für jede Marketing-Aktivität sind standardmäßig eine oder mehrere minimal konfigurierte Vorlagen in der Anwendung enthalten. Diese vordefinierten Vorlagen können nicht geändert oder gelöscht werden.

Für folgende Marketingaktivitäten stehen Vorlagen zur Verfügung:

* Programme
* Kampagnen
* E-Mail-Versand
* SMS-Versand
* Push-Benachrichtigungen
* Landingpages
* Workflows
* Dienste
* Import
* Transaktionsnachrichten

## Neue Vorlage erstellen {#creating-a-new-template}

Nachrichtenvorlagen können vom funktionalen Administrator der Plattform im Menü **[!UICONTROL Ressourcen > Vorlagen]** verwaltet werden. Vordefinierte Vorlagen können nicht geändert oder gelöscht werden. Zur Erstellung einer neuen Vorlage ist eine existierende Vorlage zu duplizieren.

1. Wählen Sie eine vorhandene Vorlage aus Im vorliegenden Beispiel soll eine **[!UICONTROL Versandvorlage]** konfiguriert werden.

   ![](assets/template_2.png)

1. Bewegen Sie die Maus darüber und wählen Sie dann die Option **[!UICONTROL Element duplizieren]** aus.

   ![](assets/template_3.png)

1. Konfigurieren Sie die gewünschten Einstellungen wie beim [Erstellen einer neuen Marketingaktivität](../../start/using/marketing-activities.md#creating-a-marketing-activity).

   ![](assets/template_4.png)

Diese Vorlagen können bei der Erstellung einer Marketingaktivität von Benutzern mit Standardberechtigung im ersten Bildschirm des Assistenten ausgewählt werden.

## Vorlagen verwenden {#using-a-template}

Im Folgenden wird die Verwendung einer zuvor erstellten Vorlage dargestellt.

>[!NOTE]
>
>Die Erstellung einer auf Vorlagen basierenden Marketingaktivität erfolgt i. d. R. durch Benutzer mit Standardberechtigung.

1. Erstellen Sie eine neue Marketingaktivität.

   ![](assets/template_5.png)

1. Wählen Sie im ersten Schritt des Assistenten die Vorlage aus, die Sie verwenden möchten.

   ![](assets/template_6.png)

   Die Marketingaktivität übernimmt die in der Vorlage definierten Parameter.

   ![](assets/template_7.png)

---
title: Fehlerbehebung bei Integrationsproblemen
description: Hier erfahren Sie, wie Sie Probleme bei der gemeinsamen Nutzung von Ressourcen beheben können.
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
feature: Triggers
role: Data Architect
level: Intermediate
exl-id: 5882ada6-dff4-4fd1-a433-0eb31570f73c
source-git-commit: a6471d2970a55373574301fb5d49ee73103fa870
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 100%

---

# Fehlerbehebung{#troubleshooting}

Bei der Verwendung der Integration mit Audience Manager oder People Core Service können Fehler auftreten.

Achten Sie in diesem Fall darauf, dass die folgenden Elemente richtig konfiguriert sind:

* **Externe Konten**

   Vergewissern Sie sich, dass die folgenden externen S3-Konten richtig in **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Externe Konten]** konfiguriert sind. Die genannten S3-Server sollten während der Bereitstellung konfiguriert worden sein.

   * **[!UICONTROL importSharedAudience]**: S3-Konto für den Zielgruppen-Import.
   * **[!UICONTROL exportSharedAudience]**: S3-Konto für den Zielgruppen-Export.

* **Freigegebene Datenquellen**

   Vergewissern Sie sich unter **[!UICONTROL Administration]** > **[!UICONTROL Anwendungskonfiguration]** > **[!UICONTROL Freigegebene Datenquellen]**, dass die freigegebene Datenquelle richtig konfiguriert ist.

   Wenn mehrere Datenquellen definiert sind, wird die Option **[!UICONTROL Priorität]** verwendet. Mit dieser Option wird festgelegt, welche Datenquelle mit den entsprechend der definierten Reihenfolge erhaltenen Alias abgeglichen wird. **[!UICONTROL Priorität]** wird nur für die Triggers-Implementierung benötigt.

   Prüfen Sie, ob der Abstimmschlüssel korrekt ist. Der Export und Import von Audiences wird mit dem Hash-Wert/verschlüsselten Wert dieses Felds durchgeführt.

   Prüfen Sie im Fall von Hashing oder Verschlüsselung der Declared ID, ob dieselben Parameter/Verschlüsselungsalgorithmen auf Ihrer Website verwendet werden.

   Nur ein Verschlüsselungsalgorithmus wird unterstützt: AES im CBC-Modus mit Schlüsselgrößen von 128, 192 oder 256 Bit mit PKCS-Padding.

   Wenn der AES-Verschlüsselungsalgorithmus ausgewählt wird, müssen die folgenden zusätzlichen Felder richtig definiert werden:

   * **Verschlüsselungsschlüssel** für AES
   * **Verschlüsselung IV** (Initialisierungsvektor) für AES
   * **Kanal** (E-Mail/SMS/Sonstige): Dieses Feld ermöglicht die direkte Entschlüsselung von E-Mail-Adressen und SMS-Nummern. Achten Sie darauf, dass der Abstimmschlüssel mit der Einstellung im Feld **Channel** übereinstimmt. Wenn Sie &quot;Sonstige&quot; auswählen, wird diese Entschlüsselung nicht durchgeführt, sondern der Abstimmschlüssel wird für die Abstimmung der Daten verwendet.

   Möglicherweise werden Audiences in Experience Cloud nicht freigegeben, da der technische Workflow angehalten oder ausgesetzt wurde. Öffnen Sie den Workflow **[!UICONTROL Freigegebene Zielgruppe importieren]** durch direkte Auswahl der Option **[!UICONTROL Workflow Freigegebene Zielgruppe importieren zeigen]** in Ihrer Datenquelle.

Es kann vorkommen, dass manche Daten bei der Freigabe einer Audience über People Core Service oder beim Import einer Audience fehlen. Es werden nämlich nur Datensätze übertragen, deren Kennung (&#39;Visitor ID&#39; oder &#39;Declared ID&#39;) mit der Profildimension abgestimmt werden konnte. Von Adobe Campaign nicht erkannte Kennungen, die People-Core-Service-Segmenten entstammen, werden nicht importiert.

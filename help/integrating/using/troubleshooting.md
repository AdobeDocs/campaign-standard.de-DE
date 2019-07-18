---
title: Problembehebung
seo-title: Problembehebung
description: Problembehebung
seo-description: Hier erfahren Sie, wie Sie Probleme bei der gemeinsamen Nutzung von Ressourcen beheben können.
page-status-flag: nie aktiviert
uuid: 1 c 764 dd 8-e 09 f -4 e 8 e -9 ccd -88 ab 3 d 714284
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: wird integriert
content-type: Referenz
topic-tags: working-with-campaign-and-audience-manager-or-people-core-service
discoiquuid: c 28 e 1 d 90-8074-4127-a 6 fc-ed 39 d 69 cdb 19
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 698466596fdacd005dc4d72b8071208c8c39f77d

---


# Problembehebung{#troubleshooting}

Bei der Verwendung der Integration mit Audience Manager oder People Core Service können Fehler auftreten.

Achten Sie in diesem Fall darauf, dass die folgenden Elemente richtig konfiguriert sind:

* **Externe Konten**

   In **[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]** &gt; **[!UICONTROL External accounts]**, make sure that the following external S3 accounts are correctly configured. Die genannten S3-Server sollten während der Bereitstellung konfiguriert worden sein.

   * **[!UICONTROL importSharedAudience]**: S3-Konto für den Zielgruppen-Import.
   * **[!UICONTROL exportSharedAudience]**: S3-Konto für den Zielgruppen-Export.

* **Freigegebene Datenquellen**

   In **[!UICONTROL Administration]** &gt; **[!UICONTROL Application settings]** &gt; **[!UICONTROL Shared Data Sources]**, check that the shared data source is set properly.

   **[!UICONTROL Wenn mehrere Datenquellen definiert sind, wird die Option Priorität]** verwendet. Mit dieser Option wird festgelegt, welche Datenquelle mit den entsprechend der definierten Reihenfolge erhaltenen Alias abgeglichen wird. **[!UICONTROL Priorität]** wird nur für die Triggers-Implementierung benötigt.

   Prüfen Sie, ob der Abstimmschlüssel korrekt ist. Der Export und Import von Audiences wird mit dem Hash-Wert/verschlüsselten Wert dieses Felds durchgeführt.

   Prüfen Sie im Fall von Hashing oder Verschlüsselung der Declared ID, ob dieselben Parameter/Verschlüsselungsalgorithmen auf Ihrer Website verwendet werden.

   Nur ein Verschlüsselungsalgorithmus wird unterstützt: AES im CBC-Modus mit Schlüsselgrößen von 128, 192 oder 256 Bit mit PKCS-Padding.

   Wenn der AES-Verschlüsselungsalgorithmus ausgewählt wird, müssen die folgenden zusätzlichen Felder richtig definiert werden:

   * **Verschlüsselungsschlüssel** für AES
   * **Verschlüsselung IV** (Initialisierungsvektor) für AES
   * **Kanal** (E-Mail/SMS/Sonstige): Dieses Feld ermöglicht die direkte Entschlüsselung von E-Mail-Adressen und SMS-Nummern. Achten Sie darauf, dass der Abstimmschlüssel mit der Einstellung im Feld **Channel** übereinstimmt. Wenn Sie "Sonstige" auswählen, wird diese Entschlüsselung nicht durchgeführt, sondern der Abstimmschlüssel wird für die Abstimmung der Daten verwendet.
   Möglicherweise werden Audiences in Experience Cloud nicht freigegeben, da der technische Workflow angehalten oder ausgesetzt wurde. Öffnen Sie den Workflow **[!UICONTROL Freigegebene Zielgruppe importieren]** durch direkte Auswahl der Option **Workflow Freigegebene Zielgruppe importieren zeigen]in Ihrer Datenquelle.[!UICONTROL **

Es kann vorkommen, dass manche Daten bei der Freigabe einer Audience über People Core Service oder beim Import einer Audience fehlen. Es werden nämlich nur Datensätze übertragen, deren Kennung ('Visitor ID' oder 'Declared ID') mit der Profildimension abgestimmt werden konnte. Von Adobe Campaign nicht erkannte Kennungen, die People-Core-Service-Segmenten entstammen, werden nicht importiert.

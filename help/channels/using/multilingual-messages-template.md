---
title: Mehrsprachige Vorlage erstellen
description: Hier erhalten Sie Informationen über die Definition und Ausführung mehrsprachiger E-Mail- und SMS-Sendungen im Rahmen eines einzigen Versands in der bevorzugten Sprache Ihrer automatisch segmentierten Kunden. Zusätzlich können Sie Leistungsberichte zu jedem Versand aufgeschlüsselt nach Sprachen und Personen erstellen.
page-status-flag: never-activated
uuid: 7a2cd5f7-c0fc-4825-a770-a62816c66b3f
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: start
content-type: reference
topic-tags: managing-templates
discoiquuid: 064c5c4a-f579-4bab-adf3-51c92eb4518f
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: cb5cc55c431cbe6050699a35ef2fff270f869dee

---


# Vorlagen für mehrsprachige Nachrichten {#multilingual-messages-template}

Eine mehrsprachige Vorlage dient zur Verwaltung mehrsprachiger Nachrichten. This kind of template is available for ****Email** and **SMS messages**  and useable in standalone mode, within a workflow or in a recurring delivery.

Bei mehrsprachigen Vorlagen basiert die Sprachverwaltung auf Varianten. **Jede Variante steht für eine Sprache**. In Adobe Campaign Standard können bis zu 40 Varianten erstellt werden.

Adobe Campaign comes with a default language which is set to **EN**. Die Standardsprache kann geändert werden, sollte aber niemals gelöscht werden.

Während der Vorlagenerstellung können Sie die Anzahl der Varianten entsprechend der Anzahl der für die Nachricht erforderlichen Sprachen hinzufügen.

Gehen Sie wie folgt vor, um eine SMS- oder E-Mail-Vorlage zu erstellen:

1. Duplizieren Sie eine vorhandene mehrsprachige Vorlage (SMS oder E-Mail).

   ![](assets/multi_template_duplicate.png)

   >[!NOTE]
   >
   >Sie können auch eine vorhandene Standardvorlage in eine mehrsprachige Vorlage umwandeln, indem Sie in den Vorlageneigenschaften die Schaltfläche **[!UICONTROL Inhaltsvariante initialisieren]**auswählen.

1. Passen Sie in den Eigenschaften Titel, Tracking etc. an.
1. Ändern Sie die Anzahl der gewünschten Varianten durch Anklicken der Variantenkachel. Das Variantenfenster öffnet sich.

   ![](assets/multi_template_variants.png)

   Dort können Sie Varianten hinzufügen oder entfernen. Um eine Variante hinzuzufügen, füllen Sie das Fenster **[!UICONTROL Neue Inhaltsvariante]**aus.

   ![](assets/multi_template_newvariant.png)

   >[!NOTE]
   >
   >Löschen Sie nicht die Standardvariante, da diese an die Profile gesendet wird, für die keine bevorzugte Sprache ausgewählt wurde.

1. Customize label variant if needed and click **[!UICONTROL Confirm]**.
1. Sie können den Inhalt für jede Variante auch direkt hinzufügen.

Jetzt können Sie basierend auf dieser mehrsprachigen Vorlage eine E-Mail oder SMS erstellen.

**Verwandte Themen:**

* [Mehrsprachige E-Mail erstellen](../../channels/using/creating-a-multilingual-email.md)
* [Profile erstellen](../../audiences/using/creating-profiles.md)

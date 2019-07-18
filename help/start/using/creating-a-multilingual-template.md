---
title: Mehrsprachige Vorlage erstellen
seo-title: Mehrsprachige Vorlage erstellen
description: Mehrsprachige Vorlage erstellen
seo-description: Hier erhalten Sie Informationen über die Definition und Ausführung mehrsprachiger E-Mail- und SMS-Sendungen im Rahmen eines einzigen Versands in der bevorzugten Sprache Ihrer automatisch segmentierten Kunden. Zusätzlich können Sie Leistungsberichte zu jedem Versand aufgeschlüsselt nach Sprachen und Personen erstellen.
page-status-flag: nie aktiviert
uuid: 7 a 2 cd 5 f 7-c 0 fc -4825-a 770-a 62816 c 66 b 3 f
contentOwner: sauviat
products: SG_ CAMPAIGN/STANDARD
audience: start
content-type: Referenz
topic-tags: managing-templates
discoiquuid: 064 c 5 c 4 a-f 779-4 bab-adf 3-51 c 92 eb 4518 f
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: b7df681c05c48dc1fc9873b1339fbc756e5e0f5f

---


# Mehrsprachige Vorlage erstellen{#creating-a-multilingual-template}

Eine mehrsprachige Vorlage dient zur Verwaltung mehrsprachiger Nachrichten.

Diese Vorlagenart ist verfügbar für **E-Mail- und SMS-Nachrichten** und kann im Einzelmodus, innerhalb eines Workflows oder in einem wiederkehrenden Versand verwendet werden.

Bei mehrsprachigen Vorlagen basiert die Sprachverwaltung auf Varianten. **Jede Variante steht für eine Sprache.**

In Adobe Campaign Standard können bis zu 40 Varianten erstellt werden.

Die in Adobe Campaign standardmäßig eingestellte Sprache ist EN. Die Standardsprache kann geändert werden, sollte aber niemals gelöscht werden.

Während der Vorlagenerstellung können Sie die Anzahl der Varianten entsprechend der Anzahl der für die Nachricht erforderlichen Sprachen hinzufügen.

Führen Sie zur Erstellung einer SMS- oder E-Mail-Vorlage die folgenden Schritte aus:

1. Duplizieren Sie eine vorhandene mehrsprachige Vorlage (SMS oder E-Mail).

   ![](assets/multi_template_duplicate.png)

   >[!NOTE]
   >
   >Sie können auch eine vorhandene Standardvorlage in eine mehrsprachige Vorlage umwandeln, indem Sie in den Vorlageneigenschaften die Schaltfläche **[!UICONTROL Inhaltsvariante initialisieren]auswählen.**

1. Passen Sie in den Eigenschaften Titel, Tracking etc. an.
1. Ändern Sie die Anzahl der gewünschten Varianten durch Anklicken der Variantenkachel. Das Variantenfenster öffnet sich.

   ![](assets/multi_template_variants.png)

   Dort können Sie Varianten hinzufügen oder entfernen. Um eine Variante hinzuzufügen, füllen Sie das Fenster **[!UICONTROL Neue Inhaltsvariante]aus.**

   ![](assets/multi_template_newvariant.png)

   >[!NOTE]
   >
   >Löschen Sie nicht die Standardvariante, da diese an die Profile gesendet wird, für die keine bevorzugte Sprache ausgewählt wurde.

1. Passen Sie bei Bedarf den Titel an und wählen Sie die Bestätigen-Schaltfläche aus.
1. Sie können den Inhalt für jede Variante auch direkt hinzufügen.

Jetzt können Sie basierend auf dieser mehrsprachigen Vorlage eine E-Mail oder SMS erstellen.

**Verwandte Themen:**

* [Mehrsprachige E-Mail erstellen](../../channels/using/creating-a-multilingual-email.md)
* [Profile erstellen](../../audiences/using/creating-profiles.md)


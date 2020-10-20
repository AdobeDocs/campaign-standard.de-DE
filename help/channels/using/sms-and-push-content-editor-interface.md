---
title: Benutzeroberfläche des Inhaltseditors für SMS und Push-Benachrichtigungen
description: Hier erhalten Sie Informationen zur Verwendung der verschiedenen Bereiche des Editors bei der Bearbeitung des Inhalts Ihrer SMS-Nachrichten und Push-Benachrichtigungen.
page-status-flag: never-activated
uuid: 4af5d247-555b-45c5-95a7-cb27f356b5a0
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: designing
content-type: reference
topic-tags: editing-sms-and-push-content
discoiquuid: 4e214eb9-d299-4095-b786-8d1de9b1c8a2
context-tags: delivery,smsContent,back
translation-type: tm+mt
source-git-commit: 1321c84c49de6d9a318bbc5bb8a0e28b332d2b5d
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 100%

---


# Benutzeroberfläche des Inhaltseditors für SMS und Push-Benachrichtigungen{#sms-and-push-content-editor-interface}

Der Inhaltseditor für SMS und Push-Benachrichtigungen besteht aus zwei Bereichen, mit denen eine Nachricht angezeigt und bearbeitet werden kann.

1. In der **Symbolleiste** bieten Schaltflächen Zugriff auf die verfügbaren Aktionen. Hier haben Sie die Möglichkeit, Personalisierungsfelder einzufügen, bedingte Texte hinzuzufügen und SMS-Inhalt in der Vorschau anzusehen. Siehe auch den Abschnitt [Symbolleiste des Inhaltseditors für SMS und Push-Benachrichtigungen](#sms-and-push-content-editor-action-bar).
1. Im **Arbeitsbereich** des Bildschirms können Sie Text direkt eingeben und auswählen, wo eine Personalisierung eingefügt werden soll. Siehe auch den Abschnitt [Bearbeitungsmodi von Inhalten von SMS und Push-Benachrichtigungen](#sms-and-push-content-edition-modes).

## Symbolleiste des Inhaltseditors für SMS und Push-Benachrichtigungen  {#sms-and-push-content-editor-action-bar}

Die Symbolleiste enthält Schaltflächen, die die Bearbeitung des angezeigten Inhalts ermöglichen.

<table> 
 <thead> 
  <tr> 
   <th> Symbol<br /> </th> 
   <th> Schaltflächenname<br /> </th> 
   <th> Kanal<br /> </th> 
   <th> Beschreibung<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> <img height="21px" src="assets/viewon_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Vorschau</span> <br /> </td> 
   <td> Nur SMS<br /> </td> 
   <td> Stellt eine E-Mail so dar, wie sie beim Empfänger erscheint. Siehe <a href="../../sending/using/previewing-messages.md">Vorschau der Nachricht erzeugen</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/undo_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Rückgängig</span> <br /> </td> 
   <td> SMS und Push-Benachrichtigung<br /> </td> 
   <td> Macht die letzte Aktion rückgängig.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/redo_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Wiederherstellen</span> <br /> </td> 
   <td> SMS und Push-Benachrichtigung<br /> </td> 
   <td> Stellt die letzte rückgängig gemachte Aktion wieder her.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/personalization_field_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Personalisierungsfeld einfügen</span> <br /> </td> 
   <td> SMS und Push-Benachrichtigung<br /> </td> 
   <td> Fügt den Wert eines Datenbankfelds in den Inhalt ein. Siehe <a href="../../designing/using/personalization.md#inserting-a-personalization-field" target="_blank">Personalisierungsfelder einfügen</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/personalization_block_darkgrey-24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Inhaltsbaustein einfügen</span> <br /> </td> 
   <td> SMS und Push-Benachrichtigung<br /> </td> 
   <td> Fügt einen personalisierten Inhaltsbaustein ein. Siehe <a href="../../designing/using/personalization.md#adding-a-content-block" target="_blank">Inhaltsbausteine</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/dynamiccontent_24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Dynamischen Text aktivieren</span> <br /> </td> 
   <td> SMS und Push-Benachrichtigung<br /> </td> 
   <td> Ermöglicht das Einfügen von dynamischem Text in den Nachrichtenkörper. Siehe <a href="../../channels/using/defining-dynamic-text.md" target="_blank">Dynamische Texte definieren</a>.<br /> </td> 
  </tr> 
  <tr> 
   <td> <img height="21px" src="assets/dynamiccontentdisable_24px.png" /> <br /> </td> 
   <td> <span class="uicontrol">Dynamischen Text deaktivieren</span> <br /> </td> 
   <td> SMS und Push-Benachrichtigung<br /> </td> 
   <td> Ermöglicht das Löschen von dynamischem Text.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Bearbeitungsmodi von Inhalten von SMS und Push-Benachrichtigungen {#sms-and-push-content-edition-modes}

Der Inhaltseditor für SMS und Push-Benachrichtigungen bietet die folgenden Funktionen:

* Text erfassen
* Personalisierungsfeld hinzufügen; Weiterführende Informationen dazu finden Sie im Abschnitt [Personalisierungsfelder einfügen](../../designing/using/personalization.md#inserting-a-personalization-field).
* Inhaltsbaustein hinzufügen; Weiterführende Informationen dazu finden Sie im Abschnitt [Inhaltsbausteine](../../designing/using/personalization.md#adding-a-content-block).
* Dynamischen Text hinzufügen; Weiterführende Informationen dazu finden Sie im Abschnitt [Dynamische Texte definieren](../../channels/using/defining-dynamic-text.md).
* Den Namen des SMS-Absenders personalisieren (nur für SMS). Weiterführende Informationen dazu finden Sie im Abschnitt [SMS-Konfiguration](../../administration/using/configuring-sms-channel.md#configuring-sms-properties).

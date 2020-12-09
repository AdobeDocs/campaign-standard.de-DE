---
solution: Campaign Standard
product: campaign
title: Einschränkungen bei Transaktionsnachrichten
description: Erfahren Sie mehr über die wichtigsten Einschränkungen und Empfehlungen für Transaktionsnachrichten in Adobe Campaign Standard.
audience: channels
content-type: reference
topic-tags: landing-pages
context-tags: landingPage,wizard;landingPage,overview;landingPage,main
translation-type: tm+mt
source-git-commit: c276c468627208b584a0342414cdbe382e349f50
workflow-type: tm+mt
source-wordcount: '675'
ht-degree: 83%

---


# Best Practices und Einschränkungen für Transaktionsnachrichten {#transactional-messaging-limitations}

<img src="assets/do-not-localize/icon_concepts.svg" width="60px">

Im folgenden Abschnitt werden die Best Practices und Einschränkungen Liste, die Sie kennen sollten, bevor Sie mit der Erstellung von Transaktionsnachrichten beginnen.

<!--For more on transactional messages, including on how to configure and create them, see [Getting started with transactional messaging](../../channels/using/getting-started-with-transactional-msg.md).-->

## Berechtigungen {#permissions}

Nur Benutzer mit der Rolle [Administration](../../administration/using/users-management.md#functional-administrators) können transaktionale Ereignis konfigurieren und auf Transaktionsnachrichten zugreifen.

## Konfiguration und Veröffentlichung von Ereignissen {#design-and-publication}

Beim Konfigurieren und Veröffentlichen von transaktionalen Ereignissen können einige der erforderlichen Schritte nicht rückgängig gemacht werden. Achten Sie bitte auf folgende Einschränkungen:

* Die verfügbaren Kanal für Transaktionsnachrichten sind: **[!UICONTROL E-Mail]**, **[!UICONTROL Mobil (SMS)]** und **[!UICONTROL Push-Benachrichtigung]**.
* Für jede Ereigniskonfiguration kann jeweils nur ein Kanal verwendet werden. Siehe [Ereignis erstellen](../../channels/using/configuring-transactional-event.md#creating-an-event).
* Nach der Erstellung des Ereignisses lässt sich der Kanal nicht mehr ändern. Deshalb müssen Sie den Mechanismus festlegen, über den eine Nachricht im Fall einer erfolglosen Sendung über einen anderen Kanal mit einem Workflow gesendet werden kann. Siehe [Workflow-Daten und -Prozesse](../../automating/using/get-started-workflows.md).
* Nach der Erstellung des Ereignisses können Sie die Zielgruppendimension (**[!UICONTROL Echtzeit-Ereignis]** or **[!UICONTROL Profil]**) nicht mehr ändern. Siehe [Ereignis erstellen](../../channels/using/configuring-transactional-event.md#creating-an-event).
* Es ist nicht möglich, eine Publikation rückgängig zu machen, Sie können aber ein Ereignis depublizieren: Dadurch wird der Zugriff auf das Ereignis und die damit verknüpften Transaktionsnachrichten gesperrt. Siehe [Ereignis depublizieren](../../channels/using/publishing-transactional-event.md#unpublishing-an-event).
* Die einzige Transaktionsnachricht, die mit einem Ereignis verknüpft werden kann, ist die Nachricht, die automatisch beim Publizieren dieses Ereignisses erstellt wird. Siehe [Vorschau erstellen und Ereignis publizieren](../../channels/using/publishing-transactional-event.md#previewing-and-publishing-the-event).

## Personalisierung         {#personalization}

Die Möglichkeiten zur Personalisierung eines Nachrichteninhalts hängt vom Typ der Transaktionsnachricht ab. Unten finden Sie die Spezifikationen.

### Ereignisbasierte Transaktionsnachrichten

* Die Personalisierungsinformationen stammen von den im Ereignis selbst enthaltenen Daten. Siehe [Ereignis-basierte Transaktionsnachricht-Konfiguration](../../channels/using/configuring-transactional-event.md#event-based-transactional-messages).
* Sie können in einer Ereignis-Transaktionsnachricht **keine** Inhaltsbausteine für **[!UICONTROL Abmelde-Links]** verwenden.
* Beim ereignisbasierten Transaktionsnachrichtenversand sollen ausschließlich die Daten verwendet werden, die im gesendeten Ereignis der Personalisierung von Empfängern und Nachrichteninhalten dienen. Der Inhalt Ihrer Transaktionsnachricht lässt sich jedoch durch die Verwendung von in der Adobe-Campaign-Datenbank enthaltenen Informationen anreichern. Siehe [Anreichern eines Ereignisses](../../channels/using/configuring-transactional-event.md#enriching-the-transactional-message-content) und [Personalisieren einer Transaktionsnachricht](../../channels/using/editing-transactional-message.md#personalizing-a-transactional-message).
* Da Ereignis-Transaktionsnachrichten keine Profilinformationen enthalten, sind sie nicht mit Ermüdungsregeln kompatibel (auch nicht, wenn sie mit Profilen angereichert werden). 

### Profilbasierte Transaktionsnachrichten  

* Die Personalisierungsinformationen können von den im Ereignis enthaltenen Daten oder von den abgestimmten Profildaten stammen. Siehe [Profil-basierte Transaktionsnachricht-Konfiguration](../../channels/using/configuring-transactional-event.md#profile-based-transactional-messages) und [Profil-basierte Transaktionsnachricht-Spezifikationen](../../channels/using/editing-transactional-message.md#profile-transactional-message-specificities).
* Sie **können in einer Profil-Transaktionsnachricht** Inhaltsbausteine für **[!UICONTROL Abmelde-Links]** verwenden. Siehe [Inhaltsbausteine](../../designing/using/personalization.md#adding-a-content-block).
* Ermüdungsregeln sind mit Profil-Transaktionsnachrichten kompatibel. Näheres dazu finden Sie unter [Ermüdungsregeln](../../sending/using/fatigue-rules.md).

### Produktlisten

Beachten Sie, dass Produktauflistungen nur in transaktionalen **E-Mail-Nachrichten** verfügbar sind. Siehe [Produktlisten in Transaktionsnachrichten verwenden](../../channels/using/editing-transactional-message.md#using-product-listings-in-a-transactional-message).

## Marken {#permissions-and-branding}

Beim [Branding](../../administration/using/branding.md) bieten Transaktionsnachrichten weniger Flexibilität als Standardnachrichten. Adobe empfiehlt, alle in Transaktionsnachrichten verwendeten Marken mit der Organisationseinheit **[!UICONTROL Alle]**[ zu verknüpfen](../../administration/using/organizational-units.md). Weiterführende Informationen dazu finden Sie in der unten stehenden Erläuterung.

Bei der Bearbeitung einer Transaktionsnachricht können Sie sie mit einer Marke verknüpfen, um einige Parameter automatisch einzufügen, wie z. B. den Markennamen oder das Markenlogo. In den Eigenschaften der Transaktionsnachricht ist standardmäßig die **[!UICONTROL Standardmarke]** ausgewählt.

![](assets/message-center_branding.png)

Alle in einer Transaktionsnachricht verwendeten Objekte (einschließlich der Marke) müssen in der Organisationseinheit **[!UICONTROL Message Center]** sichtbar sein, d. h. diese Objekte müssen sich in der Organisationseinheit **[!UICONTROL Message Center]** oder **[!UICONTROL Alle]** befinden.

Wenn aber die in den Nachrichteneigenschaften ausgewählte Marke mit einer anderen Organisationseinheit als **[!UICONTROL Message Center]** oder **[!UICONTROL Alle]** verknüpft ist, tritt ein Fehler auf und die Transaktionsnachricht kann nicht gesendet werden.

Deshalb müssen Sie im Fall von Multibranding bei Transaktionsnachrichten alle Marken entweder mit der Organisationseinheit **[!UICONTROL Message Center]** oder **[!UICONTROL Alle]** verknüpfen.

## Transaktionsnachrichten exportieren und importieren {#exporting-and-importing-transactional-messages}

* Um eine Transaktionsnachricht zu exportieren, müssen Sie bei der [Erstellung des Package-Exports](../../automating/using/managing-packages.md#creating-a-package) die entsprechende Ereigniskonfiguration einbeziehen.
* Nachdem die Transaktionsnachricht [in einem Package importiert wurde](../../automating/using/managing-packages.md#importing-a-package), wird sie nicht mehr in der Liste der Transaktionsnachrichten angezeigt. [Publizieren](../../channels/using/publishing-transactional-event.md) Sie die Ereigniskonfiguration, um die damit verbundene Transaktionsnachricht verfügbar zu machen.
